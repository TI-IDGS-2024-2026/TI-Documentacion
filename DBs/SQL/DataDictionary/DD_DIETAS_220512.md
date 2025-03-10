# 🗃️ Database Schema Documentation

> Generated by MySQL Workbench Model Documentation v3.0

## 📂 Schema: `gimnasio_8b_idgs_220512`

**📝 Description**: No description provided.

## 🗂️ Table: `tbd_dietas`

**📝 Description**:  Esta tabla almacenará la información de las dietas registradas en el sistema de administración del gimnasio, incluyendo su identificación, nombre, detalle, descripción, objetivo, estatus y fechas de registro y actualización.

### 🗄️ Columns

| Column | DataType | PK | FK | NN | UQT | BIN | UN | ZF | AI | Default | Comment |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| `ID` | `INT` | 🔑 |  | 🚫 |  |  |  |  | ⚡ |  | Descripción: Atributo identificador entero auto incremento que distingue de manera única a cada dieta.<br>Naturaleza: Cuantitativa<br>Dominio: Enteros Positivos<br>Composición: 1{0-9} |
| `Nombre` | `VARCHAR(50)` |  |  | 🚫 |  |  |  |  |  |  | Descripción: Nombre asignado a la dieta, utilizado para su identificación dentro del sistema.<br>Naturaleza: Cualitativa<br>Dominio: Caracteres Alfabéticos y espacio separador<br>Composición: 0{AZ\|az\| }50 |
| `Detalle` | `LONGTEXT` |  |  |  |  |  |  |  |  | `NULL` | Descripción: Información detallada sobre la dieta, incluidos alimentos permitidos, restricciones y recomendaciones generales.\<br>\<br>Naturaleza: Cualitativa\<br>\<br>Dominio: Caracteres Alfanuméricos, signos de puntuación y espacios\<br>\<br>Composición: 0{AZ\|az\| }50 |
| `Descripcion` | `LONGTEXT` |  |  | 🚫 |  |  |  |  |  |  | Descripción: Explicación general sobre la dieta, describiendo su propósito, beneficios y características principales.\<br>\<br>Naturaleza: Cualitativa\<br>\<br>Dominio: Caracteres Alfanuméricos, signos de puntuación y espacios\<br>\<br>Composición: 0{AZ\|az\| }50 |
| `Objetivo` | `LONGTEXT` |  |  | 🚫 |  |  |  |  |  |  | Descripción: Propósito principal de la dieta, como pérdida de peso, aumento de masa muscular, definición o mantenimiento de una alimentación equilibrada.\<br>\<br>Naturaleza: Cualitativa\<br>\<br>Dominio: Caracteres Alfanuméricos, signos de puntuación y espacios\<br>\<br>Composición:{AZ\|az\| }50 |
| `Estatus` | `BIT(1)` |  |  | 🚫 |  |  |  |  |  | `b'1'` | Descripción: Dato de auditoría que define el estatus actual del registro, siendo 0 para datos no activos y 1 para datos activos para uso en el sistema.<br>Naturaleza: Cuantitativa<br>Dominio: Booleano<br>Composición: Estado = \[0\|1\] |
| `Fecha_Registro` | `DATETIME` |  |  | 🚫 |  |  |  |  |  | `CURRENT_TIMESTAMP` | Descripción: Dato de auditoría que documenta la fecha y hora de creación del registro.<br>Naturaleza: Cuantitativa<br>Dominio: Fecha y Hora<br>Composición:<br>Año = 4{0-9}4<br>Mes = \[01\|02\|...\|12\]<br>Día = \[01\|02\|...\|31\]<br>Hora = \[00\|01\|...\|23\]<br>Minuto = \[00\|01\|...\|59\]<br>Segundo = \[00\|01\|...\|59\]<br>Fecha_Registro = Año + '-' + Mes + '-' + Día + ' ' + Hora + ':' + Minuto + ':' + Segundo |
| `Fecha_Actualizacion` | `DATETIME` |  |  |  |  |  |  |  |  | `NULL` | Descripción: Dato de auditoría que documenta la fecha y hora de la última modificación del registro.<br>Naturaleza: Cuantitativa<br>Dominio: Fecha y Hora<br>Composición:<br>Año = 4{0-9}4<br>Mes = \[01\|02\|...\|12\]<br>Día = \[01\|02\|...\|31\]<br>Hora = \[00\|01\|...\|23\]<br>Minuto = \[00\|01\|...\|59\]<br>Segundo = \[00\|01\|...\|59\]<br>Fecha_Actualizacion = Año + '-' + Mes + '-' + Día + ' ' + Hora + ':' + Minuto + ':' + Segundo |


### 🔑 Indices

| Name | Columns | Type | Description |
| --- | --- | --- | --- |
| `PRIMARY` | `ID` | PRIMARY |  |


