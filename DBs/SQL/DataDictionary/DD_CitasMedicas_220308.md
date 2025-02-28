## Table: `tbb_citas_medicas`

### Description:

Esta tabla se utiliza para almacenar información sobre las citas médicas programadas dentro del sistema. Esta tabla contiene las siguientes columnas.

### Columns:

| Column | Data type | Attributes | Default | Description |
| --- | --- | --- | --- | --- |
| `ID` | CHAR(36) | PRIMARY, Not null |   | Descripción: Identificador único de la cita médica.<br>Naturaleza: Cuantitativa.<br>Dominio: Caracteres Hexadecimales (0-F)<br>Composición: 8(0-F)8+'-'+4(0-F)4+'-'+4(0-F)4+'-'+4(0-F)4+'-'+12(0-F)12 |
| `ID_Alumno` | CHAR(36) | Not null |   | Descripción: Identificador único del alumno al que pertenece la cita.<br>Naturaleza: Cuantitativa.<br>Dominio: Caracteres Hexadecimales (0-F)<br>Composición: 8(0-F)8+'-'+4(0-F)4+'-'+4(0-F)4+'-'+4(0-F)4+'-'+12(0-F)12 |
| `Fecha_Hora` | DATETIME | Not null |   | Descripción: Fecha y hora programada para la cita médica.<br>Naturaleza: Cuantitativa.<br>Dominio: Fecha y hora válidas.<br>Composición: Formato estándar "YYYY-MM-DD HH:MM:SS" |
| `Motivo` | TEXT |   | `NULL` | Descripción: Motivo de la consulta médica.<br>Naturaleza: Cualitativa.<br>Dominio: Caracteres alfabéticos.<br>Composición: Texto libre sin límite específico. |
| `Estatus` | ENUM('Programada', 'Realizada', 'Cancelada') |   | 'Programada' | Descripción: Estado actual de la cita médica.<br>Naturaleza: Cualitativa.<br>Dominio: Valores predefinidos.<br>Composición: ['Programada'|'Realizada'|'Cancelada'] |
| `Fecha_Registro` | DATETIME | Not null | `CURRENT_TIMESTAMP` | Descripción: Fecha y hora en que se creó el registro de la cita.<br>Naturaleza: Cuantitativa.<br>Dominio: Fecha y hora válidas.<br>Composición: Formato "YYYY-MM-DD HH:MM:SS" |
| `Fecha_Actualizacion` | DATETIME |   | `NULL` | Descripción: Fecha y hora de la última actualización de la cita.<br> Naturaleza: Cuantitativa.<br>Dominio: Fecha y hora válidas.<br>Composición: Formato "YYYY-MM-DD HH:MM:SS" |

### Indices:

| Name | Columns | Type | Description |
| --- | --- | --- | --- |
| PRIMARY | `ID` | PRIMARY | Identificador único de la cita médica |

