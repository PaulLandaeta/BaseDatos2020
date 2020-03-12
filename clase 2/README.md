# Base Datos 

## Crear Base de Datos Cuarentena 

```sql
$ create database cuarentena;
```

Usar la base de datos 

```sql
$ use cuarentena;
```

## Crear tablas 

Crear Tablas solo con primary Key. 

Tabla Persona 
```sql
$ create table Persona(
    CI int not null,
    nombres varchar(30),
    apellidos varchar(30),
    fechaNacimiento DATETIME,
    PRIMARY KEY (CI)
);
```
Tabla Especialidad
```sql
$ create table Especialidad(
    ID int not null AUTO_INCREMENT,
    nombre varchar(30),
    PRIMARY KEY (ID)
);
```
Tabla Consultorio
```sql
$ create table Consultorio(
    ID int not null AUTO_INCREMENT,
    piso int not null,
    nro int not null,
    PRIMARY KEY (ID)
);
```
Crear Tablas con Foreign Key 

Tabla Paciente
```sql
CREATE TABLE Paciente (
    ID int NOT NULL AUTO_INCREMENT,
    PersonaID int,
    PRIMARY KEY (ID),
    FOREIGN KEY (PersonaID) REFERENCES Persona(CI)
);
```
Tabla Doctor 
```sql
CREATE TABLE Doctor (
    ID int NOT NULL AUTO_INCREMENT,
    ConsultorioID int,
    EspecialidadID int,
    PRIMARY KEY (ID),
    FOREIGN KEY (ConsultorioID) REFERENCES Consultorio(ID),
    FOREIGN KEY (EspecialidadID) REFERENCES Especialidad(ID),
    FOREIGN KEY (PersonaID) REFERENCES Persona(CI)
);
```
Clave Compuesta

Tabla Consulta 
```sql
CREATE TABLE Consulta (
    PacienteID int,
    DoctorID int,
    fecha DATETIME, 
    FOREIGN KEY (PacienteID) REFERENCES Paciente(ID),
    FOREIGN KEY (DoctorID) REFERENCES Doctor(ID),
    CONSTRAINT PK_Consulta PRIMARY KEY (PacienteID,DoctorID)
);
```