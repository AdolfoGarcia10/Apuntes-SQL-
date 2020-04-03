# Apuntes DML.

## ÍNDICE:
* [INSERT](#insert)
* [UPDATE](#update)
* [DELETE](#delete)

### INSERT:

Se utiliza para añadir registros a una tabla. 

Sintaxis:

 ```sql
INSERT INTO <nombredelatabla>
[(<atributo1>,<atributo2>,...)]
VALUES 
      (<valor1A>,valor2A,...),
      (<valor1B>,<valor2B>,...)
 ```

### UPDATE:

Se utiliza para actualizar y modificar los valores de los registros.

Sintaxis:

 ```sql
UPDATE <nombredelatabla>
SET <atributo1> = <valor1>
    <atributo2> = <valor2>
[WHERE <predicado>]
 ```
### DELETE:

Se utiliza para eliminar los registros de una tabla.

Sintaxis:

 ```sql
DELETE FROM <nombre-de-la-tabla>
[WHERE <predicado>]
 ```
