# Ejercicio 2: MySQL Inicial

En este ejercicio configurarás un contenedor MySQL con credenciales seguras y crearás una base de datos inicial con tablas.

---

## **Instrucciones**

1. Crea un contenedor MySQL con las siguientes credenciales:
   - Usuario: `root`
   - Contraseña: `root`
   - Base de datos inicial: `testdb`

   Ejecuta el siguiente comando:
   ```bash
   docker run -d --name mysql-db -e MYSQL_ROOT_PASSWORD=root -e MYSQL_DATABASE=testdb -p 3306:3306 mysql:5.7
   ```

2. Conéctate al contenedor MySQL desde tu máquina o usando un cliente MySQL:
   ```bash
   docker exec -it mysql-db mysql -u root -p
   ```

3. Dentro de la consola MySQL, crea una tabla inicial:
   ```sql
   CREATE TABLE test_table (
       id INT AUTO_INCREMENT PRIMARY KEY,
       name VARCHAR(255)
   );
   ```

4. Inserta algunos datos en la tabla:
   ```sql
   INSERT INTO test_table (name) VALUES ('Ejemplo1'), ('Ejemplo2');
   ```

5. Verifica que los datos se han insertado correctamente:
   ```sql
   SELECT * FROM test_table;
   ```

---

## **Notas**

- Si necesitas conectarte desde un cliente MySQL externo, usa `localhost:3306` con las credenciales proporcionadas.
- Para detener el contenedor, usa:
  ```bash
  docker stop mysql-db
  ```

---

## **Output esperado**

1. Un archivo `mysql-init.sql` en `2_administracion_sistemas/exercise/02-mysql-inicial/` que contenga los comandos SQL utilizados:
   - Creación de la tabla.
   - Inserción de datos.
   - Consulta para verificar los datos.
2. Un archivo `mysql-output.txt` que incluya la salida del comando `SELECT * FROM test_table`.

---

¡Buena suerte con el ejercicio!
