# Ejercicio 3: Backup y Restauración de Base de Datos en Docker

## Objetivo
En este ejercicio, tendrás que aprender a **crear y restaurar copias de seguridad** de una base de datos MySQL dentro de un contenedor. Lo harás utilizando las herramientas de **Docker** para gestionar los contenedores y las bases de datos.

## Requisitos previos:
1. Haber trabajado previamente con contenedores Docker y bases de datos MySQL.
2. Conocer el comando `docker exec` y cómo interactuar con contenedores desde la terminal.

---

## Tareas a realizar:

### Parte 1: Creación de un contenedor MySQL
1. Crea un contenedor MySQL en Docker. Este contenedor debe ser accesible desde tu máquina local en el puerto **3306**. Además, establece una base de datos llamada **`testdb`** y asegúrate de configurar correctamente las credenciales del usuario **root**.

### Parte 2: Copia de seguridad de la base de datos
2. Realiza una **copia de seguridad** de la base de datos `testdb`. Para esto, necesitarás un comando que extraiga el contenido de la base de datos y lo guarde en un archivo SQL. Piensa en cómo interactuar con el contenedor MySQL para realizar esta operación.

### Parte 3: Eliminación y restauración
3. Una vez hayas completado la copia de seguridad, detén y elimina el contenedor MySQL.  
4. Luego, **crea un nuevo contenedor MySQL vacío** utilizando la misma configuración (puerto, contraseña y base de datos).

### Parte 4: Restauración de la base de datos
5. **Restaura la base de datos** a partir de la copia de seguridad que hiciste en el paso anterior. Asegúrate de que los datos estén correctamente restaurados en el nuevo contenedor.

### Parte 5: Verificación
6. Verifica que la base de datos y sus datos se hayan restaurado correctamente. Conéctate al contenedor restaurado y **ejecuta una consulta SQL** para comprobar que la tabla y los datos están presentes.

---

## Preguntas para reflexionar:
- ¿Cómo puedes acceder a un contenedor MySQL y ejecutar comandos directamente dentro de él?
- ¿Qué pasos son necesarios para realizar un backup de una base de datos MySQL en un contenedor Docker?
- ¿Qué ocurre si intentas restaurar una base de datos sin haber creado previamente la estructura de tablas?
- ¿Cómo puedes gestionar múltiples contenedores de bases de datos sin que se mezclen los datos?

---

## Pistas:
- Puedes buscar cómo hacer un backup de una base de datos en MySQL usando `mysqldump`.
- Asegúrate de que el nuevo contenedor tenga las credenciales correctas para la restauración.
- Investiga los comandos de Docker para gestionar contenedores y volúmenes de forma eficiente.

---

## Nota importante:
No se proporcionan los comandos exactos para cada paso. Este ejercicio está diseñado para que explores las herramientas por ti mismo. Usa la documentación oficial de Docker y MySQL para obtener más información si la necesitas.
