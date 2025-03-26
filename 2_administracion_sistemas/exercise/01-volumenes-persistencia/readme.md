# Ejercicio 1: Volúmenes y Persistencia

En este ejercicio aprenderás a configurar volúmenes Docker para mantener datos persistentes entre reinicios de contenedores.

---

## **Instrucciones**

1. Crea un contenedor Nginx que utilice un volumen para almacenar datos:
   ```bash
   docker run -d --name nginx-vol -v nginx-data:/usr/share/nginx/html nginx
   ```

2. Accede al contenedor y crea un archivo en el volumen:
   ```bash
   docker exec -it nginx-vol bash -c 'echo "¡Hola desde un volumen Docker!" > /usr/share/nginx/html/index.html'
   ```

3. Detén y elimina el contenedor:
   ```bash
   docker stop nginx-vol && docker rm nginx-vol
   ```

4. Inicia un nuevo contenedor usando el mismo volumen:
   ```bash
   docker run -d --name nginx-vol2 -v nginx-data:/usr/share/nginx/html nginx
   ```

5. Valida que los datos persisten accediendo a `http://localhost:8080` o inspeccionando el volumen.

---

## **Output esperado**

1. Un archivo `volume-test.txt` en `2_administracion_sistemas/exercise/01-volumenes-persistencia/` que contenga la salida del siguiente comando:
   ```bash
   docker volume inspect nginx-data
   ```

---

¡Buena suerte!
