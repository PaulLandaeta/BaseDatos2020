# Base Datos 

## Importar la base de datos cuarentena.sql 


Usar la base de datos 

```sql
$ use cuarentena;
```

## Insertar Datos 

SQL 
```sql
INSERT INTO table_name (column1, column2, column3, ...)
VALUES (value1, value2, value3, ...);
```

Insertar datos a las tablas con un primary Key. 

Tabla Persona 
```sql
INSERT INTO Persona (CI, nombres, apellidos, fechaNacimiento)
VALUES (8301163, 'Paul', 'Landaeta Flores', '1991-03-25');
```
Tabla Especialidad
```sql
INSERT INTO Especialidad 
VALUES (0,'oftalmologia');
INSERT INTO Especialidad 
VALUES (0,'pediatria');
```
Tabla Consultorio
```sql
insert into Consultorio 
values (0, 1,102), 
       (0, 1,101);
```
Insertar datos a las tablas con Foreign Key 

Tabla Paciente
```sql
insert into Paciente
values (0,8301162,'2020-03-17')
```
Tabla Doctor 
```sql
insert into Doctor
values (0,234567,2,1)
```
Clave Compuesta

Tabla Consulta 
```sql
insert into Consulta 
values (1,1,'2020-03-17')
```
