
# Ejercicio 3: S3 para Backups

En este ejercicio aprenderás a configurar un bucket S3 en LocalStack para almacenar datos simulados.

---

## **Instrucciones**

1. Asegúrate de tener LocalStack corriendo con Docker Compose.

2. Crea un bucket S3:
   ```bash
   aws s3api create-bucket --bucket my-backup-bucket --endpoint-url=http://localhost:4566
   ```

3. Sube un archivo de prueba al bucket:
   ```bash
   echo "Backup data" > backup.txt
   aws s3 cp backup.txt s3://my-backup-bucket/ --endpoint-url=http://localhost:4566
   ```

4. Lista los archivos en el bucket:
   ```bash
   aws s3 ls s3://my-backup-bucket/ --endpoint-url=http://localhost:4566
   ```

---

## **Output esperado**

- Un archivo `backup-config.txt` que contenga:
  - El nombre del bucket.
  - Una lista de los archivos en el bucket.

---
