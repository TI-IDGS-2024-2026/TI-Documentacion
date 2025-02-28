<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="author" content="WB Datadict">
  <meta name="description" content="bd_servicio Data Dictionary.">
  <title>bd_servicio Data Dictionary</title>
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
    <h1>bd_servicio<br> Data Dictionary</h1>
    <p>
      <em>2025-02-28</em>
    </p>
    <p>
      <em></em>
    </p>
  </header>

  <nav><h2>Index</h2><ul><li><a href='#tbc_servicio'>tbc_servicio</a></li></ul></nav>

  <div><table id='tbc_servicio'><caption>tbc_servicio</caption><tr><td colspan='12'>Esta tabla almacenará los datos de los servicios ofrecidos por el gimnasio, los cuales pueden ser de diferentes tipos. Es importante destacar que la tabla servicios esta vinculada con las tablas: SUCURSALES y COLABORADORES</td></tr><tr><th>Column name</th><th>DataType</th><th><abbr title='Primary Key'>PK</abbr></th><th><abbr title='Foreign Key'>FK</abbr></th><th><abbr title='Not Null'>NN</abbr></th><th><abbr title='Unique'>UQ</abbr></th><th><abbr title='Binary'>BIN</abbr></th><th><abbr title='Unsigned'>UN</abbr></th><th><abbr title='Zero Fill'>ZF</abbr></th><th><abbr title='Auto Increment'>AI</abbr></th><th>Default</th><th>Comment</th></tr><tr><td class='field'>Id</td><td>INT</td><td class='centered'>&#10004;</td><td class='centered'>&nbsp;</td><td class='centered'>&#10004;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&#10004;</td><td></td><td>Descripcion: Atributo identificador número auto incremental que distingue de manera única al servicio. \\\\nNaturaleza: Cuantitativo\\\\nDominio: Enteros positivos\\\\nComposicion: 1{0-9}</td></tr><tr><td class='field'>Nombre</td><td>VARCHAR(80)</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&#10004;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td></td><td>Descripción: Valor asociado al servicio que se ofrece al cliente o usuario.\nNaturaleza: Cualitativo\nDominio: Cadena de texto\nComposición: 0{A-z }80</td></tr><tr><td class='field'>Descripcion</td><td>TEXT</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td>NULL</td><td>Descripción:Contiene una descripción detallada del servicio, proporcionando información adicional sobre sus características y beneficios..\nNaturaleza: Cualitativo\nDominio: Cadena de texto\nComposición: {A-z|,|.| |}</td></tr><tr><td class='field'>Costo</td><td>DECIMAL(10,2)</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td>NULL</td><td>Descripción: Representa el valor monetario asociado con el servicio, indicado en formato decimal con precisión de hasta dos decimales.\nNaturaleza: Cuantitativo\nDominio: Números decimales\nComposición: 1{0-9}+(.[0-9]{1,2})</td></tr><tr><td class='field'>Tipo_Servicio</td><td>ENUM('Individual', 'Grupal')</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&#10004;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td></td><td>Descripción: Especifica el tipo de servicio ofrecido, pudiendo ser individual, grupal, virtual o presencial.\nNaturaleza: Cualitativo\nDominio: Conjunto de valores limitados (&apos;individual&apos;, &apos;grupal&apos;)\nComposición:\n\nTipo_Servicio = [&apos;Individual&apos;,&apos;Grupal&apos;]</td></tr><tr><td class='field'>Fecha_Creacion</td><td>DATETIME</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td>NULL</td><td>Descripcion: Dato de Auditoria que documenta la fecha y hora de creacion del registro\\nNaturaleza: Cuantitativo\\nDominio: Numeros Enteros Positivos imitados por el calendario y limites de mes y/o año bisiesto.\\nComposicion:\\n\\nAño = 4{0-9}4\\nMes =  [01|02|...|12]\\nDia =  [01|02|..|31]\\n\\nHora = [00|01|...|23]\\nMinutos = [00|01|...|59]\\nSeguntodos = [00|01|...|59]\\n\\nFecha_Registro= Año+&apos;-&apos;+Mes+&apos;-&apos;+Dia+&apos;-&apos;+Hora+&apos;-&apos;+Munutos+&apos;-&apos;+Segundos</td></tr><tr><td class='field'>Estatus</td><td>BIT(1)</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td>b'1'</td><td>Descripcion: Dato de Auditoria que define el estatus actual del regitro, siendo 0 para un datos no activos y 1 para datos activos para uso en el sistema\\nNaturaleza: Cuantativo\\nDominio: Booleano\\nComposicion: [0|1]\\n</td></tr><tr><td class='field'>Sucursal_ID</td><td>INT</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&#10004;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td></td><td>Descripción: Identificador de la sucursal en la que se ofrece el servicio, relacionado con la tabla Sucursal para indicar la ubicación del servicio.\nNaturaleza: Cuantitativo\nDominio: Enteros positivos\nComposición: 1{0-9}</td></tr><tr><td class='field'>Colaborador_ID</td><td>INT</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&#10004;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td></td><td>Descripción:Identificador del usuario que creó el servicio, relacionado con la tabla Usuario para conocer quién gestionó el registro del servicio.\nNaturaleza: Cuantitativo\nDominio: Enteros positivos\nComposición: 1{0-9}</td></tr></table></div>
</body>
</html>
