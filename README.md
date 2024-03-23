# Tutorial de SQL

Tabla de Contenido
- [Tutorial de SQL](#tutorial-de-sql)
  - [Diagrama de ER (CHEN)](#diagrama-de-er-chen)
  - [Instalación del Gestor de Base de datos y su navegador](#instalación-del-gestor-de-base-de-datos-y-su-navegador)
  - [Algunos de los comandos más importantes de SQL](#algunos-de-los-comandos-más-importantes-de-sql)
  - [¿Qué es una tabla?](#qué-es-una-tabla)
  - [Identificadores (Identifiers)](#identificadores-identifiers)
  - [Base de Datos Northwind](#base-de-datos-northwind)

## Diagrama de ER (CHEN)
El diagrama de ER (CHEN) o ER (CHEN) diagram, es un diagrama que nos permite observar de manera gráfica cada una de nuestras entidades asi como sus relaciones y sus atributos.
Las partes más importantes son las siguientes:
- **Entidad**: Representación de algo, las entidades comúnmente se encierran en un rectángulo.
- **Atributos**: Que es lo que conforma la entidad, los atributos son encerrados en un ovalo.
  - Atributos simple: Son datos únicos, no están compuestos por nada más.
  - Atributos Compuesto: Son atributos que están compuestos por más atributos.
  - Atributos Multi-valor: Son aquellos que contienen mas de un valor, se representan con un ovalo dentro de otro ovalo.
  - Atributos Derivados: Son aquellos que se obtienen de algún otro atributo, se representa con un ovalo con lineas punteadas.
- **Key**: Identificador único de alguna entidad, estos se representan con su nombre subrayado dentro de un ovalo.

![](src\img\er-example.png)  


## Instalación del Gestor de Base de datos y su navegador
Para el tutorial se usará **SQLite** ya que es el más utilizado.
El procedimiento para instalar SQLite es el siguiente.
- Nos dirigimos al siguiente enlace [SQLite Download](https://www.sqlite.org/download.html)
- Descargaremos la version que vayamos a utilizar, ya sea Windows, Linux o Mac.
- En el caso de Windows lo primero que se descarga son los [Tools](https://www.sqlite.org/2024/sqlite-tools-win-x64-3450200.zip) de Precompiled Binaries for Windows.
- Extraemos la carpeta que se descargo.
- Creamos una carpeta dentro de nuestro disco que almacena Windows, en este caso se nombrará sqlite3.
- Copiamos el contenido de la carpeta descargada a la carpeta que creamos.
- Copiamos la dirección de la carpeta que creamos.
- Abrimos "Editar las variables de entorno del sistema".
- Ingresamos a **Variable de entorno**.
- Damos doble click en path.
- Le damos en Nuevo, pegamos la ruta de nuestra carpeta y le damos en aceptar.
- Le damos en aceptar nuevamente y listo, ya podemos cerrar el Editor de variables de entorno.

Para instalar el navegador sqlite3 browser:
- Nos dirigimos al siguiente enlace [sqlite3 browser](https://sqlitebrowser.org/dl/) y descargamos el [DB Browser for SQLite](https://download.sqlitebrowser.org/DB.Browser.for.SQLite-3.12.2-win64.msi) para nuestro sistema operativo.
- Ejecutamos el archivo descargado.
- Aceptamos las licencias y lo instalamos.
- Se nos creara el ejecutable **DB Browser (SQLite)** y ya podremos hacer uso del navegador.

## Algunos de los comandos más importantes de SQL
- **SELECT**: Extrae información de una base de datos.
  -  SELECT fields FROM database_name;
- **UPDATE**: Actualiza información de una base de datos.
- **DELETE**: Elimina información de una base de datos.
  - DELETE FROM database_name;
- **INSERT INTO**: Inserta nueva información dentro de una base de datos.
  - INSERT INTO database_name (fiel 1, fiel 2, fiel ....) VALUES (fiel value 1, fiel value 2, fiel value ....);
- **CREATE DATABASE**: Crea una nueva base de datos.
- **ALTER DATABASE**: Modifica una base de datos.
- **CREATE TABLE**: Crea una nueva tabla.
- **ALTER TABLE**: Modifica una tabla.
- **DROP TABLE**: Elimina una tabla.
- **CREATE INDEX**: Crea un index (llave de búsqueda).
- **DROP INDEX**: Elimina un index.
- *: Se utiliza para indicar todos.
- Para finalizar una sentencia SQL se usa;
- Las bases de datos SQLite se guardan con la extension .db.

Para más información se puede consultar la página de [w3schools](https://www.w3schools.com/mysql/mysql_sql.asp).

## ¿Qué es una tabla?
Una tabla puede verse como una entidad, es una estructura de datos que ser organiza en filas y columnas. 
- Las columnas se usan para representar un campo (field), esto pude verse como uns atributo. Los campos están compuestos por:
  - **Type**: Es el tipo de dato que se almacenara. 
    - Integer: Si es un número entero.
    - Text: Si es texto.
    - BLOB: Si es un archivo binario (img, docs, etc).
    - Real: Si es un número real (8-bytes).
    - Numeric: Si es un numero con una precision muy alta, ej: pi (3.1415....).
  - **Defect**: Es el valor por defecto que se le asigna al campo en caso de que no se le asigne algún otro.
  - **NN o Not Null**: Indica que ese campo no puede ser nulo, tiene que tener un valor si o si.
  - **PK o Primary Key**: Es el identificador primario con el cual podremos identificar nuestro registro, este valor no se puede repetir.
  - **AI Autoincrement**: Se encarga de auto incrementar el valor que tiene nuestra llave primaria.
  - **U o Unique**:
  - **Check o Check Constraint**:
  - **Collation**:
  - **FK o Foreign Key**: Es una llave que hace referencia a una llave primaria de otra tabla, esto con el fin de obtener el registro de otra tabla.
- Las filas son registros (record), básicamente contiene la información de todos los campos.
- Field value o valor del campo no es mas que el valor que tiene un registro en un campo (columna) especifico.

## Identificadores (Identifiers)
Los identificadores nos sirven para poder asignarle a cada registro un valor único con el cual lo podremos identificar de manera inmediata en un futuro.
Existen dos tipos de identificadores:
- Primary Key: Es el identificador primario con el cual podremos identificar nuestro registro, este valor no se puede repetir.
- Foreign Key: Es una llave que hace referencia a una llave primaria de otra tabla, esto con el fin de obtener el registro de otra tabla. Una buena practica es nombrar esta llave con el nombre que tiene en su tabla original.

La forma de relacionar una tabla con otra es mediante una foreign key.

## Base de Datos Northwind
Es una base de datos de prueba con la cual podremos practicar, la podemos descargar en el siguiente enlace: [Northwind DB](https://en.wikiversity.org/wiki/Database_Examples/Northwind/SQLite).

<!-- Image -->
![](src\img\Northwind_E-R_Diagram.png)  