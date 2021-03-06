# Apuntes SQL DQL.
## Sentencias SQL

## INDICE:
* [EL SELECT.](#EL-SELECT)
* [EL FROM.](#EL-FROM)
* [EL WHERE.](#EL-WHERE)
* [EL ORDER BY.](#EL-ORDER-BY)
* [EL IN.](#el-in)
* [EL BETWEEN.](#el-between)
* [El AND, OR Y NOT.](#el-and-or-y-not)
* [EL LIKE.](#el-like)
* [EL REPLACE.](#el-replace)
* [SUM, COUNT, MAX, MIN Y AVG.](#sum-count-max-min-y-avg)
* [EL ROUND.](#el-round)
* [EL HAVING.](#el-having)
* [EL CONCAT.](#el-concat)
* [EL LENGTH.](#el-length)
* [LEFT Y RIGHT.](#left-y-right)
* [EL JOIN.](#el-join)
* [LEFT JOIN Y RIGHT JOIN.](#left-join-y-right-join)

## EL SELECT.
El **SELECT** es una sentencia **SQL** que se utiliza para seleccionar datos de una base de datos.
```sql
SELECT  column1, column2, ...
FROM table_name;
```

##  EL FROM.
El **FROM** es una sentencia **SQL** que se utiliza para especificar qué tabla para seleccionar o borrar los datos.

```sql
SELECT column1, column2, ...
FROM table_name;
```

##  EL WHERE.
El **WHERE** es una sentencia **SQL** que se utiliza para filtrar y dentro de ella pueden ir otras sentencias.

```sql
SELECT column1, column2, ...
FROM table_name
WHERE condition;
```
##  EL ORDER BY.
El  **ORDER BY**  es una sentencia **SQL** que se utiliza para ordenar los resultados. Puede
ser:

**ASC**: orden ascendente aunque el **ORDER BY** ya es **ASC** por defecto.

```sql
  SELECT name, population
  FROM world
  WHERE population > x
  ORDER BY population asc;
```

**DCS**: orden descendente.

```sql
  SELECT name, population
  FROM world
  WHERE population > x
  ORDER BY population dsc;
```
##  EL IN.
El  **IN** es una sentencia **SQL** que permite especificar varios valores en una sentencia **WHERE**.

```sql
SELECT column_name(s)
FROM table_name
WHERE column_name IN (value1, value2, ...);
```
## EL BETWEEN.
El  **BETWEEN** es una sentencia **SQL** que compara los valores en un rango determinado.

```sql
SELECT column_name(s)
FROM table_name
WHERE column_name BETWEEN value1 AND value2;
```
## El AND ,OR Y NOT.

**AND**: es un operador que sirve para cumplir 2 o mas condiciones cuando ambas sean ciertas.

```sql
SELECT column1, column2, ...
FROM table_name
WHERE condition1 AND condition2 AND condition3 ...;
```
**OR**: es un operador que sirve para cumplir 2 o mas condiciones cuando al menos una de ellas es correcta.

```sql
SELECT column1, column2, ...
FROM table_name
WHERE condition1 OR condition2 OR condition3 ...;
```
**NOT**: es un operador que sirve para cumplir 1 condición cuando esta no es correcta.

```sql
SELECT column1, column2, ...
FROM table_name
WHERE NOT condition;
```
## EL LIKE.

El **LIKE** es un operador que utiliza en una cláusula **WHERE** para buscar un patrón específico en una columna.


```sql
SELECT column1, column2, ...
FROM table_name
WHERE columnN LIKE pattern;
```

## EL REPLACE.

El **REPLACE** es una función **SQL** sirve para intercambiar elementos de la consulta.

```sql
SELECT city
 REPLACE (city, 'NY', 'New York')
FROM world
WHERE name LIKE '%_NY';
```
## SUM, COUNT, MAX, MIN Y AVG.

| Símbolo   | Significado                                                      |
| --------- | -----------------------------------------------------------------|
| **SUM**   | Devuelve la suma de todos los valore de una columna              | 
| **COUNT** | Devuelve el numero de tuplas                                     | 
| **MAX**   | Da el valor máximo de una columna                                | 
| **MIN**   | Da el valor mínimo de una columna                                |
| **AVG**   | Devuelve la media del valor numérico de las tuplas de una columna|

## EL ROUND

El **ROUND** es un operador de **SQL** que sirve para redondear un numero a un número "x" de decimales.

```sql
SELECT column1, column2, ROUND (x/y,z)
FROM table_name
WHERE columnN LIKE pattern;
```
### Siendo:

* **X**: un atributo.

* **Y**: un número.

* **Z**: el numero de decimales.

## El HAVING.

El **HAVING** se usa prácticamente igual que un **WHERE** y a diferencia de el este se caracteriza por tener que ir siempre acompañado de un **GROUP BY**.

```sql
SELECT column_name(s)
FROM table_name
WHERE condition
GROUP BY column_name(s)
HAVING condition
ORDER BY column_name(s);
```

## EL CONCAT.

El **CONCAT** sirve para unir datos.

```sql
SELECT name, 
CONCAT(ROUND(100* population /
                               (SELECT population
                                  FROM world 
                                 WHERE name = 'Germany'),
               0),
         '%')
FROM world
WHERE continent = 'Europe';
```

## EL LENGTH.

El **LENGTH** se una para saber el numero de letras que tiene una palabra.

### COMO SE USA:

```sql
LENGTH (cadena o nombre)
```
## LEFT Y RIGHT

### LEFT
Es una función que se usa para devolver los x **primeros** valores de una palabra. Se utiliza de esta forma:

```sql
SELECT colum1, LEFT(colum1, X)
FROM table_name
WHERE columN > Y;
```
Siendo **X** el numero de letras que queramos.

### RIGHT
Es una función que se usa para devolver los x **últimos** valores de una palabra. Se utiliza de esta forma:

```sql
SELECT colum1, RIGHT(colum1, X)
FROM table_name
WHERE columN > Y;
```
Siendo **X** el numero de letras que queramos.

## EL  JOIN.

El **JOIN** se utiliza para juntar un numero x de tablas en una única tabla.

```sql
SELECT goal.player
FROM game JOIN goal ON game.id = goal.matchid
WHERE teamid='GER';
```
### ON.
El **ON** acompaña al **JOIN** prácticamente en todas las consultas y se utiliza para la unión de las tablas.

## LEFT JOIN Y RIGHT JOIN.

Tiene la misma función que el **JOIN** pero se diferencian en:

### LEFT JOIN.

Muestra todos los valores de la **izquierda** aunque en la derecha haya nulos.

```sql
SELECT goal.player
FROM game LEFT JOIN goal ON game.id = goal.matchid
WHERE teamid='GER';
```

### RIGHT JOIN.

Muestra todos los valores de la **derecha**  aunque en la izquierda haya nulos.

```sql
SELECT goal.player
FROM game RIGHT JOIN goal ON game.id = goal.matchid
WHERE teamid='GER';
```















