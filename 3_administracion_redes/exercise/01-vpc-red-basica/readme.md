# 🏗 Ejercicio 1: VPC y Red Básica

En este ejercicio configurarás una red virtual simulada (VPC) usando **LocalStack**.

---

## **Instrucciones**

### Paso 1: Configurar LocalStack

Para comenzar, deberás crear un archivo `docker-compose.yml` para configurar LocalStack. A continuación se muestra un ejemplo básico de cómo debe lucir tu archivo:

```yaml
version: '3.8'
services:
  localstack:
    image: localstack/localstack
    ports:
      - "4566:4566"
      - "4571:4571"
    environment:
      - DOCKER_HOST=unix:///var/run/docker.sock
      - LOCALSTACK_API_KEY=your_api_key # Opcional, para funcionalidades avanzadas
    volumes:
      - "./localstack:/var/lib/localstack"
---

### Paso 2: Iniciar LocalStack

Una vez que hayas creado el archivo `docker-compose.yml`, ¿cómo iniciarías el servicio LocalStack en segundo plano?

**Pista:** Busca el comando adecuado para arrancar los servicios definidos en el archivo `docker-compose.yml`.

---

### Paso 3: Crear una VPC

Ahora, usando AWS CLI, deberás crear una VPC. ¿Qué parámetros necesitas para crear una VPC? Piensa en el rango CIDR.

**Pista:** Investiga qué comando de AWS CLI permite crear una VPC y qué parámetros necesita.

---

### Paso 4: Crear una tabla de enrutamiento

Asocia una tabla de enrutamiento a la VPC que has creado en el paso anterior. 

**Pista:** Consulta los comandos de AWS CLI relacionados con la creación de tablas de enrutamiento.

---

### Paso 5: Configurar un Gateway de Internet

Crea un gateway de Internet y asócialo a la tabla de enrutamiento.

**Pista:** Investiga qué comandos son necesarios para crear y asociar un gateway de Internet a una VPC.

---

## **Output esperado**

El resultado final debe ser un archivo `vpc-config.txt` que contenga:

- ID de la VPC.
- Rango CIDR.
- IDs de la tabla de enrutamiento y el gateway.

---
