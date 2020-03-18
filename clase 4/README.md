# Base Datos 

## Consultas en la base de datos bookStore.sql

Usar la base de datos 

```sql
use bookStore;
```

## Seleccionar todos los registros y atributos de una tabla 

SQL 
```sql
Select * from TableName
```
## Seleccionar todos los registros y atributos de la tabla usuario

```sql
Select * from usuario
```
## Seleccionar todos los registros y especificos atributos 

```sql
Select column1,column2,column3.... from TableName
```

```sql
Select usuario,activo from usuario
```

## Seleccionar registros unicos 

```sql
Select DISTINCT column from TableName
```

```sql
SELECT DISTINCT activo FROM usuario;
```

## Selecionar los registros y ordenarlos.

```sql
SELECT column1, column2 
FROM TableName
ORDER BY column1;
```

```sql
SELECT usuario, idempleado,activo 
FROM usuario
ORDER BY usuario;
```

Descendente

```sql
SELECT usuario, idempleado,activo 
FROM usuario
ORDER BY usuario desc;
```

### Seleccionar los registros por una condición.

```sql
SELECT column1, column2 
FROM TableName
where condition 
```

```sql
SELECT usuario, idempleado,activo 
FROM usuario
where activo = 1
ORDER BY usuario DESC;
```

Operadores 

| Operador | Descripción |
| ------------- | ------------- |
| =  | Igual  |
| <>  | Diferente  |
| !=  | Diferente  |
| >   | Mayor Que  |
| >=  | Mayor o Igual Que  |
| <   | Menor Que  |
| <=  | Menor o Igual Que  |
| IN ( )  | Valores que Coinciden en una Lista  |
| NOT  | Negar una Condición  |
| BETWEEN  | Valores en un Rango (incluye los extremos)  |
| IS NULL  | Verifica si el Valor es NULL  |
| IS NOT NULL  | Verifica si el Valor es diferente de NULL  |
| LIKE  | Definir un patrón de búsqueda y utiliza % y _  |
| EXISTS  | La condición se cumple si la subconsulta devuelve al menos una fila  |
	

Por Ejemplo 

>Buscar los usuarios que empiezan con e 

```sql
SELECT usuario, idempleado,activo 
FROM usuario
where usuario like 'e%'
ORDER BY usuario DESC;
```

## Renombramiento

```sql
select usuario as user, idempleado as id, activo as estado 
from usuario 
```

## Union

```sql
select column1,column2
from table1 
union
select column1,column2
from table2
```

## Joins

Inner Join

```sql
select column1,column2
from table1 
inner join table2 on table1.column = table2.column
```

```sql
select *
from empleado
inner join venta on empleado.idempleado = venta.idempleado
```

Left Join 

```sql
select column1,column2
from table1 
left join table2 on table1.column = table2.column
```

Right Join

```sql
select column1,column2
from table1 
Right join table2 on table1.column = table2.column
```
