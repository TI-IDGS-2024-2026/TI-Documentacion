# Schema documentation Aldo

Generated by MySQL Workbench Model Documentation v1.0.0 - Copyright (c) 2015 Hieu Le


## Table: `tbc_consumibles` 

### Description: 
Tabla que contendrá la información de los CONSUMIBLES utilizados en el hospital. Esta tabla almacenará los datos relevantes como nombre, código de identificación, cantidad disponible, fecha de vencimiento, proveedor y ubicación de cada consumible. Los consumibles son elementos de uso temporal en los procedimientos médicos y administrativos del hospital. 



### Columns: 

| Column | Data type | Attributes | Default | Description |
| --- | --- | --- | --- | ---  |
| `id` | INT | PRIMARY, Auto increments, Not null |   | Descripción: Identificador principal del conjunto de registros.\\nNaturaleza: Cualitativo.\\nDominio: Caracteres Hexadecimales (0-F)\\nComposición: 8(0-F)8+'-'+4(0-F)4+'-'+4(0-F)4+'-'+4(0-F)4+'-'+12(0-F)11 |
| `nombre` | VARCHAR(100) | Not null |   | Descripción: Nombre completo de la persona.\\\\nNaturaleza: Cualitativo\\\\nDominio: Caracteres alfabéticos\\\\nComposición: 1(a-z, A-Z, ' ')80 |
| `descripcion` | TEXT | Not null |   | Descripción: Detalle del consumible.\\\\nNaturaleza: Cualitativo\\\\nDominio: Caracteres alfanuméricos\\\\nComposición: 1(a-z, A-Z, 0-9, ' ')255 |
| `tipo` | VARCHAR(50) | Not null |   | Descripción: Clasificación del consumible.\\\\nNaturaleza: Cualitativo\\\\nDominio: Caracteres alfabéticos\\\\nComposición: 1(a-z, A-Z, ' ')50 |
| `departamento` | VARCHAR(50) | Not null |   | Descripción: Área del hospital donde se usa el consumible.\\\\nNaturaleza: Cualitativo\\\\nDominio: Caracteres alfabéticos\\\\nComposición: 1(a-z, A-Z, ' ')50 |
| `cantidad_existencia` | INT | Not null |   | Descripción: Número de unidades disponibles.\\\\nNaturaleza: Cuantitativo\\\\nDominio: Números enteros\\\\nComposición: 1(0-9)11 |
| `detalle` | TEXT |  | `NULL` | Descripción: Información adicional del consumible.\\\\nNaturaleza: Cualitativo\\\\nDominio: Caracteres alfanuméricos\\\\nComposición: 1(a-z, A-Z, 0-9, ' ')255 |
| `fecha_registro` | DATETIME | Not null |   | Descripción: Fecha de ingreso del consumible.\\\\nNaturaleza: Temporal\\\\nDominio: Fecha y hora\\\\nComposición: YYYY-MM-DD HH:MM:SS |
| `fecha_actualizacion` | DATETIME | Not null |   | Descripción: Última fecha de modificación.\\\\nNaturaleza: Temporal\\\\nDominio: Fecha y hora\\\\nComposición: YYYY-MM-DD HH:MM:SS |
| `estatus` | BIT |  | `NULL` | Descripción: Estado del consumible (activo/inactivo).\\\\nNaturaleza: Cualitativo\\\\nDominio: Caracteres alfabéticos\\\\nComposición: 1(a-z, A-Z)10 |
| `observaciones` | TEXT |  | `NULL` | Descripción: Notas adicionales sobre el consumible.\\\\nNaturaleza: Cualitativo\\\\nDominio: Caracteres alfanuméricos\\\\nComposición: 1(a-z, A-Z, 0-9, ' ')255 |
| `espacio_medico` | VARCHAR(50) |  | `NULL` | Descripción: Ubicación del consumible en el hospital.\\\\nNaturaleza: Cualitativo\\\\nDominio: Caracteres alfanuméricos\\\\nComposición: 1(a-z, A-Z, 0-9, ' ')100 |


### Indices: 

| Name | Columns | Type | Description |
| --- | --- | --- | --- |
| PRIMARY | `id` | PRIMARY |   |