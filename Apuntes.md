# Apuntes SQL DQL.
## Sentencias SQL
1. EL SELECT.
2. EL FROM.
3. EL WHERE.
4. EL ORDER BY
5. EL IN
6. EL BETWEEN
## 1. EL SELECT.
El SELECT es una sentencia SQL que se utiliza para seleccionar datos de una base de datos.
```sql
SELECT  column1, column2, ...
FROM table_name;
```

##  2. EL FROM.
El FROM es una sentencia SQL que se utiliza para especificar qué tabla para seleccionar o borrar los datos.

```sql
SELECT column1, column2, ...
FROM table_name;
```

##  3.  EL WHERE.
El WHERE es una sentencia SQL que se utiliza para filtrar y dentro de ella pueden ir otras sentencias.

```sql
SELECT column1, column2, ...
FROM table_name
WHERE condition;
```
##  4. EL ORDER BY.
El  ORDER BY  es una sentencia SQL que se utiliza para ordenar los resultados. Puede
ser:

**ASC**: orden ascendente aunque el ORDER BY ya es ASC por defecto.

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
##  5. EL IN.
El  IN es una sentencia SQL que permite especificar varios valores en una sentencia WHERE.

```sql
SELECT column_name(s)
FROM table_name
WHERE column_name IN (value1, value2, ...);
```
## 6. EL BETWEEN.
El  BETWEEN es una sentencia SQL que compara los valores en un rango determinado.

```sql
SELECT column_name(s)
FROM table_name
WHERE column_name BETWEEN value1 AND value2;
```




