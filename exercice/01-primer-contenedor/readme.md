# Ejercicio 1: Primer Contenedor

En este ejercicio aprenderás a ejecutar tu primer contenedor utilizando Docker. Esto incluye descargar una imagen de Docker Hub, ejecutar un contenedor, interactuar con él y detenerlo.

---

## **Objetivos**
1. Descargar y ejecutar una imagen oficial de Docker.
2. Entender los conceptos básicos de contenedores.
3. Ejecutar comandos básicos de Docker CLI para gestionar contenedores.

---

## **Instrucciones**

### 1. Descargar una imagen de Docker Hub
Usa el siguiente comando para descargar la imagen oficial de Nginx:
```bash
docker pull nginx
```

Esto descargará la última versión de la imagen de Nginx desde Docker Hub.

---

### 2. Ejecutar el contenedor
Ejecuta el contenedor de Nginx usando el siguiente comando:
```bash
docker run -d -p 8080:80 nginx
```

- **`-d`**: Ejecuta el contenedor en segundo plano (modo detached).
- **`-p 8080:80`**: Mapea el puerto 8080 de tu máquina al puerto 80 del contenedor.

Abre tu navegador y accede a `http://localhost:8080` para verificar que el servidor Nginx está corriendo.

---

### 3. Listar contenedores en ejecución
Verifica que el contenedor está corriendo con:
```bash
docker ps
```

---

### 4. Detener el contenedor
Detén el contenedor utilizando su ID o nombre:
```bash
docker stop <container_id>
```

---

## **Tareas Opcionales**
1. Inspecciona el contenedor:
   - Usa `docker inspect <container_id>` para obtener detalles del contenedor.
2. Verifica los logs del contenedor:
   - Usa `docker logs <container_id>` para ver los registros de Nginx.

---

## **Recursos Adicionales**
- [Docker CLI Reference](https://docs.docker.com/engine/reference/commandline/docker/)
- [Documentación oficial de Nginx en Docker Hub](https://hub.docker.com/_/nginx)

---

¡Enhorabuena por completar tu primer ejercicio con Docker! 🎉
