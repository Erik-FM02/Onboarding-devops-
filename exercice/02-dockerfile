# Ejercicio 2: Crear una Imagen Personalizada

En este ejercicio aprenderás a crear una imagen personalizada de Docker utilizando un `Dockerfile`. Añadirás contenido propio a un contenedor basado en la imagen de Nginx.

---

## **Objetivos**
1. Crear un `Dockerfile` para personalizar una imagen.
2. Construir una nueva imagen basada en Nginx.
3. Ejecutar un contenedor usando la imagen personalizada.

---

## **Instrucciones**

### 1. Crear el archivo `Dockerfile`
En esta carpeta, crea un archivo llamado `Dockerfile` con el siguiente contenido:
```dockerfile
# Usa la imagen oficial de Nginx como base
FROM nginx:latest

# Copia un archivo HTML personalizado al contenedor
COPY index.html /usr/share/nginx/html/index.html

# Expone el puerto 80
EXPOSE 80
```

Este `Dockerfile` realiza lo siguiente:
- Usa la imagen oficial de Nginx como base.
- Copia un archivo `index.html` personalizado al directorio de contenido estático de Nginx.
- Expone el puerto 80 del contenedor.

---

### 2. Crear un archivo `index.html`
Crea un archivo `index.html` en esta misma carpeta con contenido personalizado, por ejemplo:
```html
<!DOCTYPE html>
<html>
<head>
  <title>¡Hola desde Docker!</title>
</head>
<body>
  <h1>Bienvenido a tu contenedor personalizado 🚀</h1>
</body>
</html>
```

---

### 3. Construir la imagen
Ejecuta el siguiente comando para construir la imagen personalizada:
```bash
docker build -t mi-nginx-personalizado .
```

- **`-t`**: Etiqueta la imagen con un nombre (`mi-nginx-personalizado`).
- **`.`**: Especifica que el contexto de construcción es el directorio actual.

---

### 4. Ejecutar el contenedor
Ejecuta un contenedor usando tu imagen personalizada:
```bash
docker run -d -p 8080:80 mi-nginx-personalizado
```

Abre tu navegador y accede a `http://localhost:8080` para ver tu contenido personalizado.

---

### 5. Verificar las imágenes disponibles
Lista las imágenes en tu máquina local con:
```bash
docker images
```

---

## **Tareas Opcionales**
1. Cambia el contenido del archivo `index.html` y reconstruye la imagen.
2. Usa el comando `docker history <image_id>` para explorar las capas de tu imagen personalizada.
3. Optimiza el tamaño de la imagen reduciendo las capas en el `Dockerfile`.

---

## **Recursos Adicionales**
- [Documentación de Dockerfile](https://docs.docker.com/engine/reference/builder/)
- [Docker Best Practices](https://docs.docker.com/develop/dev-best-practices/)

---

¡Felicidades por crear tu primera imagen personalizada! 🎉
