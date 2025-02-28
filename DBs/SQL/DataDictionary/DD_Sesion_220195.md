<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="author" content="WB Datadict">
  <meta name="description" content="tabla_bd Data Dictionary.">
  <title>tabla_bd Data Dictionary</title>
  <script>
    // Highlight table corresponding to the current fragment in the URL.
    document.addEventListener("DOMContentLoaded", function(){
      var tables = document.querySelectorAll("table");
      document.querySelectorAll("nav a").forEach(function(link) {
          link.addEventListener("click", function() {
            // Remove all classes from tables.
            tables.forEach(function(table) {
                table.classList.remove("focused");
            });
            // Get a.href value and extract its fragment id.
            // Highlight table using fragment id.
            document.querySelector(this.hash).classList.add("focused");
          });
      });
    });
  </script>
  <style type="text/css">
    a {
        text-decoration: none;
    }
    abbr {
        cursor: help;
    }
    header {
        color: #6A6A6A;
        text-align: right;
    }
    table {
        border-collapse: collapse;
        margin-bottom: 30px;
        width: 100%;
    }
    table caption {
        font-size: 120%;
        font-weight: bold;
    }
    table, td, th {
        border-color: silver;
        border-style: solid;
        border-width: 1px;
    }
    caption {
        color: black;
    }
    td, th {
        padding: 1em;
    }
    tr:hover {
        color: #333;
        background-color: #F2F2F2;
    }
    th {
        background-color: #F5F5F5;
    }
    td {
        color: #6A6A6A;
    }
    ul {
        font-style: italic;
    }
    .centered {
        text-align: center;
    }
    .field {
        color: #4C4C4C;
        font-weight: bold;
    }
    .focused {
        outline-color: aqua;
        outline-style: solid;
        outline-width: thin;
    }
  </style>
</head>

<body>
  <header>
    <h1>tabla_bd<br> Data Dictionary</h1>
    <p>
      <em>2025-02-28</em>
    </p>
    <p>
      <em></em>
    </p>
  </header>

  <nav><h2>Index</h2><ul><li><a href='#tbb_sesiones'>tbb_sesiones</a></li></ul></nav>

  <div><table id='tbb_sesiones'><caption>tbb_sesiones</caption><tr><td colspan='12'>La tabla TBB_SESIONES almacena la información de las sesiones programadas en el gimnasio. Cada sesión está vinculada a un cliente, un entrenador, una sucursal y un horario específico. Además, contiene datos sobre la duración, tipo y estado de la sesión, permitiendo un control detallado sobre el registro de actividades del gimnasio.</td></tr><tr><th>Column name</th><th>DataType</th><th><abbr title='Primary Key'>PK</abbr></th><th><abbr title='Foreign Key'>FK</abbr></th><th><abbr title='Not Null'>NN</abbr></th><th><abbr title='Unique'>UQ</abbr></th><th><abbr title='Binary'>BIN</abbr></th><th><abbr title='Unsigned'>UN</abbr></th><th><abbr title='Zero Fill'>ZF</abbr></th><th><abbr title='Auto Increment'>AI</abbr></th><th>Default</th><th>Comment</th></tr><tr><td class='field'>ID_SESION</td><td>INT</td><td class='centered'>&#10004;</td><td class='centered'>&nbsp;</td><td class='centered'>&#10004;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&#10004;</td><td></td><td>Descripcion: Es el identificador único de la sesión en la base de datos. Permite diferenciar una sesión de otra.\nNaturaleza: Cuantitativa\nDominio: Númerico, Entero, AUTO_INCREMENT\nComposición: [0|1|2|.....]</td></tr><tr><td class='field'>ID_CLIENTE</td><td>INT</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&#10004;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td></td><td>Descripcion: Referencia al cliente que participará en la sesión. Un cliente puede tener múltiples sesiones registradas.\nNaturaleza: Cuantitativa\nDominio: Númerico, Entero\nComposición: [0|1|2|.....]</td></tr><tr><td class='field'>ID_ENTRENADOR</td><td>INT</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&#10004;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td></td><td>Descripcion: Identificador del entrenador a cargo de la sesión. Un entrenador puede manejar varias sesiones al día.\nNaturaleza: Cuantitativa\nDominio: Númerico, Entero\nComposición: [0|1|2|.....]</td></tr><tr><td class='field'>ID_SUCURSAL</td><td>INT</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&#10004;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td></td><td>Descripcion: Especifica en qué sucursal del gimnasio se llevará a cabo la sesión.\nNaturaleza: Cuantitativa\nDominio: Númerico, Entero\nComposición: [0|1|2|.....]</td></tr><tr><td class='field'>ID_HORARIO</td><td>INT</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&#10004;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td></td><td>Descripcion: Referencia al horario preestablecido de la sesión. Cada sesión debe cumplir con un horario definido.\nNaturaleza: Cuantitativa\nDominio: Númerico, Entero\nComposición: [0|1|2|.....]</td></tr><tr><td class='field'>FECHA</td><td>DATE</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&#10004;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td></td><td>Descripcion: Indica el día en que la sesión tendrá lugar. No se permiten sesiones en el pasado.\nNaturaleza: Cuantitativa\nDominio: Números enteros positivos limitados por el calendario y límites de mes y/o año.\nComposición: \nAño = [0000 - 9999]\nMes = [01 - 12]\nDía = [01 - 31]</td></tr><tr><td class='field'>HORA_INICIO</td><td>TIME</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&#10004;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td></td><td>Descripcion: Hora exacta en que la sesión comienza. Se debe validar que no haya traslapes con otras sesiones.\nNaturaleza: Cuantitativa\nDominio: Números enteros positivos, limitados por el reloj de 24 horas.\nComposición: \nHora = [00 - 23]\nMinutos = [00 - 59]\nSegundos = [00 - 59]</td></tr><tr><td class='field'>HORA_FIN</td><td>TIME</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&#10004;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td></td><td>Descripcion: Hora exacta en que la sesión termina. Debe ser mayor que HORA_INICIO.\nNaturaleza: Cuantitativa\nDominio: Números enteros positivos, limitados por el reloj de 24 horas.\nComposición: \nHora = [00 - 23]\nMinutos = [00 - 59]\nSegundos = [00 - 59]</td></tr><tr><td class='field'>DURACION_MINUTOS</td><td>INT</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td>NULL</td><td>Descripcion:Cantidad total de minutos que dura la sesión. Se calcula como HORA_FIN - HORA_INICIO.\nNaturaleza:Cuantitativa\nDominio:Números enteros positivos mayores a 0\nComposicion: \nHora= [01|02|...|12]\nMinutos= [01|02|...|60]\n Segundos= [01|02|...|60]</td></tr><tr><td class='field'>TIPO_SESION</td><td>ENUM('Personal', 'Grupal', 'Evaluación')</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&#10004;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td></td><td>Descripcion: Tipo de sesión según su modalidad. Puede ser individual o grupal.\nNaturaleza: Cualitativa\nDominio: Conjunto de valores predefinidos\nComposición: [&apos;Personal&apos;, &apos;Grupal&apos;, &apos;Evaluación&apos;]</td></tr><tr><td class='field'>ESTATUS</td><td>ENUM('Programada', 'Completada', 'Cancelada')</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&#10004;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td>'Programada'</td><td>Descripcion: Estado actual de la sesión, indicando si está programada, completada o cancelada.\nNaturaleza: Cualitativa\nDominio: Conjunto de valores predefinidos\nComposición: [&apos;Programada&apos;, &apos;Completada&apos;, &apos;Cancelada&apos;]</td></tr></table></div>
</body>
</html>
