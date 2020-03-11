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

SQL Syntax 

```sql
CREATE TABLE table_name (
    column1 datatype,
    column2 datatype,
    column3 datatype,
   ....
);
```

MySQL

```sql
$ create table nombreTabla(
    nombre varchar(30),
    clave varchar(10)
);
```

Donde `nombreTabla` sera el nombre de la tabla a crear.


### Modificar una Tabla 

Agregar un atributo 

```sql
ALTER TABLE table_name
ADD column_name datatype;
```

Eliminar un atributo 

```sql
ALTER TABLE table_name
DROP COLUMN column_name;
```

Modificar un atributo 

```sql
ALTER TABLE table_name
MODIFY COLUMN column_name datatype; 
```

### Borrar una Tabla 

```sql
$ drop table nombreTabla;
```

para evitar el error si no existe la tabla usar: 

```sql
$ drop table if exists nombreTabla;
```

### Crear Tabla con PK

```sql
CREATE TABLE Persons (
    ID int NOT NULL,
    LastName varchar(255) NOT NULL,
    FirstName varchar(255),
    Age int,
    PRIMARY KEY (ID)
);
```

Clave compuesta 

```sql
CREATE TABLE Persons (
    ID int NOT NULL,
    LastName varchar(255) NOT NULL,
    FirstName varchar(255),
    Age int,
    CONSTRAINT PK_Person PRIMARY KEY (ID,LastName)
);
```

### Foreign Key 
```sql
CREATE TABLE Orders (
    OrderID int NOT NULL,
    OrderNumber int NOT NULL,
    PersonID int,
    PRIMARY KEY (OrderID),
    FOREIGN KEY (PersonID) REFERENCES Persons(PersonID)
);
```



Cheat Sheet [MySQL](https://cheatography.com/davechild/cheat-sheets/mysql/)

