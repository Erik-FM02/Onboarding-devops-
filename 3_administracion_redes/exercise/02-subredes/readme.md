# **Ejercicio 2: Subredes**  

En este ejercicio aprenderás a crear subredes públicas y privadas dentro de una VPC simulada en LocalStack.  

---

## **Instrucciones**  

1. **Verifica que LocalStack esté en ejecución**  
   - Asegúrate de que Docker Compose está corriendo correctamente y que puedes interactuar con LocalStack mediante la CLI de AWS.  

2. **Crea dos subredes dentro de la VPC:**  
   - Una subred **pública** con el rango `10.0.1.0/24`.  
   - Una subred **privada** con el rango `10.0.2.0/24`.  
   - Usa el comando de AWS CLI para crear cada subred, especificando la VPC correspondiente y el bloque CIDR adecuado.  

3. **Asocia la subred pública a la tabla de enrutamiento:**  
   - Para que la subred pública tenga acceso a internet, debes asociarla a una **tabla de enrutamiento** que tenga una ruta hacia una **puerta de enlace de Internet**.  
   - Utiliza el comando adecuado para establecer esta asociación.  

4. **Guarda la configuración en un archivo:**  
   - Una vez creadas las subredes y realizadas las asociaciones necesarias, almacena los **IDs de las subredes** y sus **tablas de enrutamiento** en un archivo llamado `subnets-config.txt`.  

---

## **Objetivo**  

Al finalizar el ejercicio, deberás tener una **VPC con dos subredes** configuradas correctamente y documentadas en el archivo de salida.  
