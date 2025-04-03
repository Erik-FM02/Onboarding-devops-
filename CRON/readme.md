# **Ejercicio Avanzado: Programación de Tareas con Cron y Scripts en Linux**

## **Objetivo**  
Investigar y aplicar el uso de `cron` para automatizar tareas en Linux, integrándolo con scripts avanzados que ejecuten diferentes funciones de mantenimiento y seguridad en el sistema.  

---

## **Tareas**  

### **Tarea 1: Investigación sobre Cron y Scripts en Bash**  
- Explica qué es `cron` y cómo funciona en Linux.  
- Investiga la sintaxis de las expresiones de tiempo en `cron` (ejemplo: `* * * * *`).  
- Explica cómo se listan, crean y eliminan trabajos de `cron` con `crontab`.  
- Investiga cómo se crean scripts en Bash y cómo se ejecutan desde `cron`.  

---

### **Tarea 2: Automatización de Limpieza de Archivos y Logs**  
- Crea un script en Bash que elimine automáticamente archivos temporales en `/tmp` que tengan más de 7 días.  
- Programa una tarea en `cron` que ejecute este script una vez al día.  
- Verifica que el script se ejecuta correctamente y registra su actividad en un archivo de logs.  

---

### **Tarea 3: Programación de Backups Automáticos**  
- Crea un script que realice un backup de un directorio específico y lo comprima en formato `.tar.gz`.  
- Configura `cron` para ejecutar este script automáticamente cada día a las 02:00 AM.  
- Asegúrate de que el script almacene un registro de las copias de seguridad en un archivo de log.  

---

### **Tarea 4: Reinicio de Servicios Automático**  
- Escribe un script que verifique si un servicio (por ejemplo, `nginx` o `apache2`) está en ejecución y lo reinicie si está caído.  
- Programa una tarea en `cron` para ejecutar este script cada 5 minutos.  
- Prueba el script deteniendo el servicio manualmente y verifica que `cron` lo reinicia.  

---
### **Tarea 5 : Despliegue y Monitoreo de Contenedores con Cron y Docker**
#### **Objetivo:**  
Automatizar el despliegue y monitoreo de un contenedor Docker usando `cron`, asegurando que se reinicie si deja de ejecutarse.  

#### **Instrucciones:**  
1. **Investigación previa:**  
   - Explica cómo interactúan `cron` y `Docker` en sistemas Linux.  
   - Investiga cómo se puede comprobar el estado de un contenedor con `docker ps`.  
   - Busca cómo reiniciar un contenedor si ha dejado de ejecutarse.  

2. **Creación del entorno:**  
   - Usa Docker para crear y ejecutar un contenedor con un servicio web (por ejemplo, un contenedor de `nginx`).  
   - Asegúrate de que el contenedor se ejecute en segundo plano.  

3. **Automatización con Cron:**  
   - Escribe un script en Bash que verifique si el contenedor sigue activo.  
   - Si el contenedor se ha detenido, el script debe reiniciarlo automáticamente.  
   - Configura `cron` para ejecutar este script cada 2 minutos.  

4. **Pruebas:**  
   - Detén el contenedor manualmente (`docker stop <nombre_contenedor>`) y verifica que el script lo reinicia.  
   - Revisa los logs del sistema para asegurarte de que la tarea de `cron` se ejecuta correctamente.  


---
