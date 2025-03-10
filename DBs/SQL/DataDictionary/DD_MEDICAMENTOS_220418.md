


## Table: `tbc_medicamentos`

### Description: 

Esta tabla contiene la informaciOn detallada sobre los medicamentos disponibles en el sistema. Incluye datos sobre el nombre comercial, nombre generico, via de administracion, presentacion, tipo, cantidad disponible y fechas de registro y actualizacion de los medicamentos.

### Columns: 

| Column | Data type | Attributes | Default | Description |
| --- | --- | --- | --- | ---  |
| `ID` | INT | PRIMARY, Auto increments, Not null |   | Descripcion: Identificador principal del conjunto de registros.\\\\\\\\nNaturaleza: "Cualitativo/Cuantitativo"\\\\\\\\nDominio: Caracteres Hexadecimales (0-F)\\\\\\\\nComposicion: 8(0-F)8+'-'+4(0-F)4+'-'+4(0-F)4+'-'+4(0-F)4+'-'+'-'+12(0-F)11 |
| `Nombre_comercial` | VARCHAR(80) | Not null |   | Descripcion: Nombre comercial bajo el cual se vende el medicamento.\\nNaturaleza: Cualitativo\\nDominio: Caracteres alfabaticos.\\nComposicion: Entre 1 y 80 caracteres (a-z | A-Z | 0-9). |
| `Nombre_generico` | VARCHAR(80) | Not null |   | Descripcion: Nombre generico del medicamento, sin marcas comerciales.\\nNaturaleza: Cualitativo\\nDominio: Caracteres alfabaticos.\\nComposicion: Entre 1 y 80 caracteres (a-z | A-Z). |
| `Via_administracion` | ENUM | Not null |   | Descripcion: Forma en que el medicamento debe ser administrado al paciente.\\nNaturaleza: Cualitativo\\nDominio: Valores especificos.\\nComposicion: [Oral | Intravenoso | Rectal | Cutaneo | Subcutaneo | Oftilmica | tica | Nasal | Topica | Parental ]. |
| `Presentacion` | ENUM | Not null |   | Descripcion: Forma en la que se encuentra el medicamento.\\nNaturaleza: Cualitativo\\nDominio: Valores especificos.\\nComposicion: [Comprimidos | Grageas | Capsulas | Jarabes | Gotas | Solucion | Pomada | Jabon | Supositorios | Viales]. |
| `Tipo` | ENUM | Not null |   | Descripcion: Clasificacion del medicamento segun su funcion terapeutica.\\nNaturaleza: Cualitativo\\nDominio: Valores especificos.\\nComposicion: [Analgesicos | Antibiiticos | Antidepresivos | Antihistamanicos | Antiinflamatorios | Antipsicticos]. |
| `Cantidad` | INT | Not null |   | Descripcion: Numero de unidades disponibles del medicamento.\\nNaturaleza: Cuantitativo\\nDominio: Numeros enteros positivos.\\nComposicion: Valor numerico entero mayor o igual a 0. |
| `Volumen` | DECIMAL | Not null |   | Descripcion: Cantidad del medicamento expresada en unidades de medida.\\nNaturaleza: Cuantitativo\\nDominio: Numeros decimales positivos.\\nComposicion: Valor numerico en formato decimal con dos cifras despues del punto. |
| `Fecha_registro` | DATETIME | Not null | `CURRENT_TIMESTAMP` | Descripci�n: Fecha y hora en la que el medicamento fue ingresado al sistema.\\nNaturaleza: Cuantitativo\\nDominio: Fecha y hora en formato (YYYY-MM-DD HH:MM:SS).\\nComposicion: Año = 4(1-9)4\\nMes = [1|2|...|12]\\nDia = [1|2|...|31]\\nHora = [00|01|...|23]Minuto = [00|01|...|59]\\nSegundo = [00|01|...|59]\\nFecha_Registro = Año + '-' + Mes + '-' + Dia + ' ' + Hora + ':' + Minuto + ':' + Segundo |
| `Fecha_actualizacion` | DATETIME |  | `NULL` | Descripci�n: Fecha y hora de la �ltima modificaci�n en la informacion del medicamento.\\nNaturaleza: Cuantitativo\\nDominio: Fecha y hora en formato (YYYY-MM-DD HH:MM:SS).\\nComposicion: Año = 4(1-9)4\\nMes = [1|2|...|12]\\nDia = [1|2|...|31]\\nHora = [00|01|...|23]Minuto = [00|01|...|59]\\nSegundo = [00|01|...|59]\\nFecha_Registro = Año + '-' + Mes + '-' + Dia + ' ' + Hora + ':' + Minuto + ':' + Segundo |


### Indices: 

| Name | Columns | Type | Description |
| --- | --- | --- | --- |
| PRIMARY | `ID` | PRIMARY |   |

