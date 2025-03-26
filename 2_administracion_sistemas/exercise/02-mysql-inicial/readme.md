# Ejercicio 2: MySQL Inicial

## Objetivo
En este ejercicio configurarás un contenedor MySQL con credenciales seguras y crearás una base de datos inicial con tablas. Aprenderás a trabajar con contenedores Docker y a gestionar bases de datos MySQL dentro de un contenedor.

## Requisitos previos:
1. Tener conocimientos básicos de **Docker** y **MySQL**.
2. Saber cómo interactuar con contenedores Docker y cómo ejecutar comandos en una base de datos MySQL.

---

## Tareas a realizar:

### Parte 1: Creación del contenedor MySQL
1. **Crea un contenedor MySQL** en Docker utilizando las siguientes credenciales:
   - Usuario: **root**
   - Contraseña: **root**
   - Base de datos inicial: **testdb**

   El contenedor debe ser accesible desde tu máquina local en el puerto **3306**. Investiga cómo configurar estos parámetros correctamente al crear un contenedor.

### Parte 2: Conexión al contenedor
2. Una vez que el contenedor esté en funcionamiento, **conéctate a la base de datos MySQL** desde tu máquina o utilizando un cliente MySQL externo. Asegúrate de usar las credenciales proporcionadas para autenticarte correctamente.

### Parte 3: Creación de la base de datos y tabla
3. Dentro de la consola MySQL:
   - **Crea una tabla** llamada `test_table` con las siguientes columnas:
     - `id`: Un campo **INT** que se auto-incremente y sea la clave primaria.
     - `name`: Un campo **VARCHAR** que permita almacenar nombres de hasta 255 caracteres.
   - **Inserta algunos datos** en la tabla creada. Puedes agregar, por ejemplo, dos o tres nombres de ejemplo.

### Parte 4: Verificación
4. **Verifica que los datos se han insertado correctamente** ejecutando una consulta `SELECT` sobre la tabla `test_table` para asegurarte de que los registros se han guardado.

---

## Pistas:
- Investiga cómo iniciar un contenedor de Docker con variables de entorno para establecer la contraseña y la base de datos inicial.
- Recuerda usar el comando `docker exec` para ejecutar comandos dentro de un contenedor Docker.
- Si necesitas conectarte desde un cliente MySQL, usa el puerto **3306** de tu localhost con las credenciales proporcionadas.

---

## Salida esperada:
1. Un archivo llamado `mysql-init.sql` en el directorio `2_administracion_sistemas/exercise/02-mysql-inicial/` que contenga los siguientes comandos SQL utilizados:
   - Creación de la tabla.
   - Inserción de datos.
   - Consulta para verificar los datos.
   
2. Un archivo llamado `mysql-output.txt` que incluya la salida del comando `SELECT * FROM test_table`, mostrando los datos que insertaste.

---

## Nota importante:
No se proporcionan los comandos exactos para cada paso. Este ejercicio está diseñado para que explores cómo trabajar con contenedores Docker y bases de datos MySQL de manera autónoma. Usa la documentación oficial de **Docker** y **MySQL** para encontrar la información necesaria.

¡Buena suerte con el ejercicio!
