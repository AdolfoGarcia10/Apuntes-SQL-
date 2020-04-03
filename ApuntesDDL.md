# Apuntes SQL DDL.
## INDICE:
### [SENTENCIAS:](#sentencias)
* [ALTER](#alter)
* [CREATE](#create)
* [DROP](#drop)
### [CONSTRAINS:](#constrains)
* [PRIMARY KEY](#primary-key)
* [FOREING KEY](#foreign-key)
* [UNIQUE](#unique)
* [CHECK](#check)
* [NOT NULL](#not-null)

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
```SQL
ALTER TABLE table_name
ALTER COLUMN column_name datatyPE;
```
###  DROP
Es una sentencia SQL DDL que permite eliminar.

```SQL
DROP SCHEMA
[IF EXISTS] <Nombre-de-la-base-de-datos>
[CASCADE|RESTRICT];
```
* **CASCADE** y **RESTRICT** sirven para eliminar la base de datos la única diferencia es que para usar restrict la base de datos tiene que estar vacía.

## CONSTRAINTS

### PRIMARY KEY
Sintaxis:
```sql
[CONSTRAINT <nombre-de-la-restricción>]
PRIMARY KEY (<atributo>);
```
* Es opcional y sirve para declarar la clave principal.

### FOREIGN KEY
Sintaxis:
```sql
[CONSTRAINT <nombre-de-la-restricción>]
FOREIGN KEY (<atributo>)
REFERENCES <nombre-de-la-tabla-referenciada>[(atributos-referenciados)]
[ON DELETE CASCADE|NO ACTION|SET NULL|SET DEFAULT]
[ON CASCADE CASCADE|NO ACTION|SET NULL|SET DEFAULT];
```
* **ON DELETE** se utiliza para modificar el comportamiento de la FOREING KEY cuando se elimina la tabla principal.
* **ON UPDATE** se utiliza para modificar el comportamiento de la FOREING KEY cuando se actualiza o modifica la tabla principal.
* **CASCADE** se utiliza para que al borrar/modifica en la tabla principal se borre/modifique también en la tabla secundaria.
* **SET NULL** se utiliza cuando los datos de la tabla principal se modifica o elimina para establecer los datos como **NULL**.
* **SET DEFAULT** se utiliza cuando los datos de la tabla principal se modifica o elimina para establecer los datos como **DEFAULT**.

### NOT NULL
Se utiliza para que las columnas no acepten valores nulos. 

Sintaxis:
```sql
CREATE TABLE Departamento (
Nome_Departamento CHAR(10) PRIMARY KEY,
Teléfono CHAR(9) NOT NULL,;
```
### UNIQUE
Se utiliza agregar a una columna unicidad es decir que no se repite. 

Sintaxis:
```sql
CREATE TABLE Departamento (
Nome_Departamento CHAR(10) NOT NULL UNIQUE,
Teléfono CHAR(9) NOT NULL;
```
### CHECK

Se utiliza para limitar el valor que pueden ser utilizados en una columna o en una tabla.

Sintaxis:
```sql
[CONSTRAINT <restriction_name> CHECK (<predicado(<atributo>)>)]
[[NOT] DEFERRABLE] 
[INITIALLY / INMEDIATE  DETERRED],
```

























