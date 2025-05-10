# Módulo I - Introducción a las Bases de Datos

**Licenciatura en Tecnologías de la Información (Plan 2024)**

**Tema central:** Fundamentos de Bases de Datos - Conceptos y estructura básica

[⬅ Volver](../README.md)  


---

## 🔹 Introducción
Las bases de datos permiten almacenar, recuperar y manipular datos de forma 
estructurada. Son clave en la gestión de información. Este módulo explorará los
conceptos fundamentales y la evolución histórica de las bases de datos.

---

## Datos e información

### Dato
- Hehcos sin interpretación
- Tipos:
  - **Cualitativos**: describen (ej. Verde, soltero).
  - **Cuantitativos**: miden (ej. 5, 3.14, fechas, etc).

---

## 🔹 ¿Qué es una base de datos?
- Conjunto estrucutrado e interrelacionado de datos.
- Gestionado por un SGDB (Sistema de Gestión de Bases de Datos).
- Permite almacenar, consultar y administrar la información.

## 🔹 Definiciones destacadas
- **Silberschatz et al. (2014):** conjunto de datos interrelacionados y programas que permiten su acceso y modificación.
- **Martin (1995):** colección de datos sin redundancia innecesaria, independiente de las aplicaciones que la usan.
- **Connolly y Begg (2005):** colección compartida de datos relacionados diseñada para satisfacer las necesidades de una organización.

Una base de datos debe:
- Representar un aspecto del mundo real.
- Contener datos coherentes y con propósito definido.
- Ser diseñada y gestionada de forma estructurada.

---

## 🔹 Objetivos de las bases de datos

- **Integridad de los datos:** prevenir errores por hardware o ingreso incorrecto de información.
- **Consistencia:** asegurar que los datos no entren en contradicción.
- **Seguridad y protección:** evitar accesos no autorizados y proteger la privacidad.
- **Independencia lógica y física:** permitir cambios en el sistema sin alterar los datos.
- **Acceso concurrente:** múltiples usuarios pueden acceder a la BD sin conflictos.
- **Reducción de redundancia:** minimizar duplicaciones innecesarias.
- **Atomicidad:** una operación debe completarse por completo o no realizarse en absoluto.


---

## 🔹 Lenguajes de bases de datos (SQL)

SQL es el lenguaje estándar para interactuar con las bases de datos. Se divide en varios subconjuntos:

### DDL - Data Definition Language
Permite definir la estrucutra de la base de datos:
- `CREATE`  crea tablas, vistas, etc.
- `ALTER`: modifica estructuras existentes.
- `DROP`: elimina objetos.
- `TRUNCATE`: elimina filas de una tabla sin registro de cambios.


### DML - Data Manipulation Language
Permite manipular los datos:

- `SELECT`: consultar datos.
- `INSERT`: agregar nuevos registros.
- `UPDATE`: modificar registros existentes.
- `DELETE`: eliminar registros.


### DCL - Data Control Language
Controla permisos de acceso:

- `GRANT`: otorga permisos.
- `REVOKE`: revoca permisos previamente concedidos.


### TCL - Transaction Control Language
Gestiona transacciones:

- `COMMIT`: guarda los cambios de forma permanente.
- `ROLLBACK`: revierte cambios no deseados.
- `SAVEPOINT`: establece puntos intermediarios para recuperación.

> ❗ Una transacción es una unidad lógica de trabajo que consiste en una o más operaciones sobre una base de datos, que deben ejecutarse completamente o no ejecutarse en absoluto, garantizando integridad, coherencia y fiabilidad de los datos. :p

---

## 🔹 Sistema de Gestión de Bases de Datos (SGBD)
El SGBD es un software que permite definir, crear, mantener y controlar el acceso a una base de datos. Proporciona una interfaz para realizar operaciones de consulta, inserción, modificación y eliminación de datos.

### Funciones de un SGBD

- **Interacción con el gestor de archivos:** permite el acceso físico a los datos almacenados.
- **Control de concurrencia:** asegura la consistencia cuando varios usuarios acceden simultáneamente.
- **Implementación de la integridad:** verifica el cumplimiento de reglas definidas.
- **Catálogo del sistema:** contiene descripciones de tablas, columnas, restricciones, usuarios y estadísticas.
- **Seguridad:** restringe el acceso a usuarios no autorizados.
- **Recuperación:** permite restaurar el sistema ante fallos técnicos o errores humanos.

---

## 🔹 Propiedades ACID de las transacciones en bases de datos - EXTRA
Las transacciones deben cumplir cuatro propiedades fundamentales conocidas como **ACID**: 
Atomicidad, Consistencia, Aislamiento y Durabilidad. Estas propiedades aseguran que los datos
permanezcan correctos y estables, incluso frente a errores o ejecuciones simultáneas.


## 1. Atomicidad (*Atomacity*)
Una transacción debe ejecutarse **completa o no ejecutarse en absoluto**. No se permiten
estados indeterminados.

- Si ocurre un error, todos los cambios se revierten (rollback).
- Se asegura mediante logs de transacciones y mecanismos de recuperación.

Ejemplo: En una transferencia bancaria, si se descuenta dinero de una cuenta, pero
no se acredita en la otra, todo debe deshacerse.


## 2. Consistencia (*Consistency*)
La base de datos debe pasar de un **estado válido a otro estado válido** después de cada
transacción.

- Todas las restriccions, reglas de integridad y dependencias deben mantenerese.
- Una transacción inválida es automáticamente rechazada.

Ejemplo: No puede insertarse un dato que viole una clave primaria o una restricción de integridad referencial.*


## 3. Aislamiento (*Isolation*)
Cada transacción debe ejecutarse **como si fuera la única en el sistema**, sin interferencias externas.

- Los efectos de una treansacción no son visibles a otras hasta que finalice.
- Controlado mediante niveles de aislamiento: `Read Uncommited`, `Read Committed`, `Repeatable Read`, `Serializable`.

Ejemplo: Dos usuarios no deberían poder comprar el mismo producto limitado al mismo tiempo.


## Durabilidad (*Durability*)
Una vez que una transacción ha sido confirmada (**commit**), sus efectos deben **permanecer** incluso ante fallos del sistema.

- Los cambios se guardan en medios persistentes (disco).
- Se utilizan logs de recuperación y escritura asegurada.

Ejemplo:  Si se realiza un pago y el sistema se apaga luego, el pago debe quedar registrado de todos modos.


> 🔹 Las propiedades **ACID** aseguran que las bases de datos sean **ROBUSTAS, COHERENTES y SEGURAS**, especialmente en entornos críticos como los bancos, sistemas médicos o aplicaciones empresariales.



