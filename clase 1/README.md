# Base Datos 
>Una base de datos es tan solo un conjunto de tablas o relaciones.

### Mostrar las bases de datos existentes 

```sql
$ show databases;
```
### Create una base de Datos

```sql
$ create database baseDeDatos;
```
Donde `baseDeDatos` sera el nombre de la base de datos a crear.

Usar la base de datos 

```sql
$ use baseDeDatos;
```

### Create una Tabla 

```sql
$ create table nombreTabla(
    nombre varchar(30),
    clave varchar(10)
);
```

Donde `nombreTabla` sera el nombre de la tabla a crear.

### Borrar una Tabla 

```sql
$ drop table nombreTabla;
```

para evitar el error si no existe la tabla usar: 

```sql
$ drop table if exists nombreTabla;
```