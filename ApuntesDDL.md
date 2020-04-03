# Apuntes SQL DDL.
## INDICE:
### SENTENCIAS:
* ALTER
* CREATE
* DROP
### CONSTRAINS:
* PRIMARY KEY
* FOREING KEY
* UNIQUE
* CHECK
* NOT NULL
* TIPOS  DE DATOS
* CREACIÓN DE DOMINIOS

## SENTENCIAS
* CREATE
* ALTER
* DROP

### CREATE
Es una sentencia SQL DDL que permite crear la base de datos, tablas...

```SQL
 CREATE (DATABASE|SCHEMA)
[IF NOT EXIST] nameDB
[CHARACTER SET CharsetName]

```
* Se usa tanto **DATABSAE** como **SCHEMA** ya que son sinónimos.
* **IF NOT EXIST** se utiliza en los casos que ya esta creada la tabla.
* **CHARSET SET** nos permite cambiar el tipo de caracteres admitidos.

### ALTER
Es una sentencia SQL DDL que permite crear, eliminar y modificar columnas.

```SQL
ALTER TABLE table_name
ADD column_name datatype,
DROP column_name [CASCADE|RESTRICT]
```
* **ADD** se utiliza para crear columnas.
* **DROP** se utiliza para eliminar columnas, al eliminar se puede utilizar: **CASCADE** para eliminar la columna y todo lo que depende de ella. **RESTRICT** para eliminar la columna y en el caso de que existan una o mas estructuras que dependan de la misma.

Para **MODIFICAR** una columna se utiliza:

```SQL
ALTER TABLE table_name
ALTER COLUMN column_name datatype;
```









