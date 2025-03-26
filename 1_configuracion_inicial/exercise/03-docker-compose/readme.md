# Ejercicio 3: Configuración con Docker Compose

En este ejercicio aprenderás a usar `docker-compose` para configurar y ejecutar múltiples servicios en contenedores, trabajando con un servidor Nginx y una aplicación web simple.

---

## **Objetivos**
1. Entender cómo funciona `docker-compose` y su archivo de configuración (`docker-compose.yml`).
2. Configurar un servicio Nginx que sirva una aplicación web.
3. Levantar y gestionar múltiples servicios con un solo comando.

---

## **Instrucciones**

### 1. Crear el archivo `docker-compose.yml`
En esta carpeta, crea un archivo llamado `docker-compose.yml` con el siguiente contenido:
```yaml
version: '3.8'

services:
  web:
    image: nginx:latest
    ports:
      - "8080:80"
    volumes:
      - ./html:/usr/share/nginx/html
  app:
    image: httpd:latest
    ports:
      - "8081:80"
    volumes:
      - ./app:/usr/local/apache2/htdocs/
```

- **`web`**: Configura un contenedor de Nginx que sirve archivos estáticos desde la carpeta `./html`.
- **`app`**: Configura un contenedor de Apache HTTP Server que sirve archivos desde la carpeta `./app`.

---

### 2. Crear las carpetas `html` y `app`
Crea las carpetas `html` y `app` en esta carpeta, y añade un archivo `index.html` a cada una:

#### En `html/index.html`:
```html
<!DOCTYPE html>
<html>
<head>
  <title>Servidor Nginx</title>
</head>
<body>
  <h1>¡Hola desde el servidor Nginx! 🚀</h1>
</body>
</html>
```

#### En `app/index.html`:
```html
<!DOCTYPE html>
<html>
<head>
  <title>Servidor Apache</title>
</head>
<body>
  <h1>¡Hola desde el servidor Apache! 🌐</h1>
</body>
</html>
```

---

### 3. Levantar los servicios
Ejecuta el siguiente comando para levantar los servicios definidos en `docker-compose.yml`:
```bash
docker-compose up
```

Accede a los servicios en:
- Nginx: `http://localhost:8080`
- Apache: `http://localhost:8081`

---

### 4. Verificar los servicios
Lista los contenedores en ejecución:
```bash
docker ps
```

---

### 5. Detener y eliminar los servicios
Para detener los servicios, ejecuta:
```bash
docker-compose down
```

---

## **Tareas Opcionales**
1. Modifica el archivo `docker-compose.yml` para agregar una red personalizada que conecte ambos servicios.
2. Usa `docker-compose logs` para inspeccionar los registros de los contenedores.
3. Añade un tercer servicio (por ejemplo, una base de datos como MySQL) al archivo `docker-compose.yml`.

---

## **Recursos Adicionales**
- [Documentación de Docker Compose](https://docs.docker.com/compose/)
- [Ejemplos de Docker Compose](https://docs.docker.com/samples/)

---

¡Genial! Ahora has aprendido a gestionar múltiples servicios con `docker-compose` 🎉
