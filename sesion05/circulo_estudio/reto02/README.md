[`Introducción a Bases de Datos`](../../../README.md) > [`Sesión 05`](../../README.md) > [`Círculo de estudio`](../README.md)

#### Reto 2

##### Objetivos 🎯

- Poner en práctica la creación de tablas en **SQL**.


##### Requisitos 📋

- MySQL Workbench instalado.

##### Desarrollo 🚀

Vayamos a la primera parte de la solución: 

*Crear las tablas necesarias para cargar la información. Esto lo puedes hacer usando el comando `CREATE TABLE`. También necesitarás crear el esquema de la base de datos. Esto no lo vimos en el contenido de la sesión con el fin de que pongas en práctica tus habilidades de investigación... Necesitarás investigar un poco para responder a la pregunta ¿Cómo se crea un esquema de base de datos en MySQL.* **Importante**: Para no sobreescribir los cambios de otras personas, coloca como nombre de tu esquema tu nombre.

Te sugerimos seguir los siguientes pasos para llegar a la solución. Sin embargo, puedes resolverlo de la forma que creas más conveniente:

---
> **Paso 1.** Con tu investigación crear el esquema.
>
> <details><summary>Solución</summary>
>
> Para crear el esquema usamos el siguiente código:
>
> ```sql
> CREATE SCHEMA mariareyes;
> ```
> </details>
---
> **Paso 2.** Crear las tablas usando **SQL**.
>
> <details><summary>Solución</summary>
>
> Para crear las tablas usamos el siguiente código:
>
> ```sql
> USE mariareyes;
>
> CREATE TABLE Alumnos (
>   matricula INT PRIMARY KEY,
>   nombre VARCHAR(45),
>   apellido VARCHAR (45)
> );
> 
> CREATE TABLE Tareas (
>   id_tarea INT PRIMARY KEY,
>   matricula INT,
>   numero_tarea INT,
>   calificacion FLOAT,
>   FOREIGN KEY (matricula) REFERENCES Alumnos(matricula)
> );
>
> CREATE TABLE Examenes (
>   id_examen INT PRIMARY KEY,
>   matricula INT,
>   numero_examen INT,
>   calificacion FLOAT,
>   FOREIGN KEY (matricula) REFERENCES Alumnos(matricula)
> );
>
> ```
> </details>
---

[`Anterior`](../reto01/README.md) | [`Siguiente`](../reto03/README.md)
