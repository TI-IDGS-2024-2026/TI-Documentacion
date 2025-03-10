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
      <em>2025-03-06</em>
    </p>
    <p>
      <em></em>
    </p>
  </header>

  <nav><h2>Index</h2><ul><li><a href='#tbb_personas'>tbb_personas</a></li><li><a href='#tbc_servicio'>tbc_servicio</a></li></ul></nav>

  <div><table id='tbb_personas'><caption>tbb_personas</caption><tr><td colspan='12'>Esta tabla almacenara los datos de las personas asociadas a los usuarios de la plataforma de administracion de gimnasio, es importante denotar que la presona es una superentidad de : CLIENTE, COLABORADOR, PROVEDOR </td></tr><tr><th>Column name</th><th>DataType</th><th><abbr title='Primary Key'>PK</abbr></th><th><abbr title='Foreign Key'>FK</abbr></th><th><abbr title='Not Null'>NN</abbr></th><th><abbr title='Unique'>UQ</abbr></th><th><abbr title='Binary'>BIN</abbr></th><th><abbr title='Unsigned'>UN</abbr></th><th><abbr title='Zero Fill'>ZF</abbr></th><th><abbr title='Auto Increment'>AI</abbr></th><th>Default</th><th>Comment</th></tr><tr><td class='field'>ID</td><td>INT</td><td class='centered'>&#10004;</td><td class='centered'>&nbsp;</td><td class='centered'>&#10004;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&#10004;</td><td></td><td>Descripcion: Atributo identificador numero auto incremental que distingue de manera unica a la persona. \nNaturaleza: Cuantitativo\nDominio: Enteos positivos\nComposicion: 1{0-9}</td></tr><tr><td class='field'>Titulo_Cortesia</td><td>VARCHAR(20)</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td>NULL</td><td>Descripcion: Abreviatur o Palabra de Cortesia para dirigirse de manera formal a la persona, por ejemplo:Sr., Sra.,Ing., Dra, etc.\nNaturaleza: Cualitativa \nDominio: Caracteres Alfanumericos y puntos (.)\nComposicion: 0{A-Z|a-z|.}20</td></tr><tr><td class='field'>Nombre</td><td>VARCHAR(80)</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&#10004;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td></td><td>Descripcion: Valos asociado a la persona dentro de su registro civil\nNaturaleza: Cualitativa \nDominio: Caracteres Alfanumericos, vocales con tilde, espacios separados \nComposicion: 0{A-Z|a-z| |}80</td></tr><tr><td class='field'>Primer_Apellido</td><td>VARCHAR(80)</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&#10004;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td></td><td>Descripcion: Valos asociado a la persona dentro de su registro civil, generalmente conocido como Apellido Paterno\nNaturaleza: Cualitativa \nDominio: Caracteres Alfanumericos, vocales con tilde, espacios separados \nComposicion: 0{A-Z|a-z| |}80</td></tr><tr><td class='field'>Segundo_Apellido</td><td>VARCHAR(80)</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td>NULL</td><td>Descripcion: Valos asociado a la persona dentro de su registro civil, generalmente conocido como Apellido Materno\nNaturaleza: Cualitativa \nDominio: Caracteres Alfanumericos, vocales con tilde, espacios separados \nComposicion: 0{A-Z|a-z| |}80</td></tr><tr><td class='field'>Fecha_Nacimiento</td><td>DATE</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&#10004;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td></td><td>Descripcion: Fecha que determina la edad de la persona, indicado el dia, mes y a�o de natalicio\nNaturaleza: Cuantitativo\nDominio: Numeros Enteros Positivos imitados por el calendario y limites de mes y/o a�o bisiesto.\nComposicion:\n\nA�o = 4{0-9}4\nMes =  [01|02|...|12]\nDia =  [01|02|..|31]\nFecha_Nacimiento = A�o+&apos;-&apos;+Mes+&apos;-&apos;+Dia</td></tr><tr><td class='field'>Fotografia</td><td>VARCHAR(100)</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td>NULL</td><td>Descripcion: Nombre y extension del archivo de la imagen de portada de la persona.\nNaturaleza: Cualitativa \nDominio: Caracteres Alfanumericos, mas la extension permitida de imagenes como .jpg, .png, etc. \nComposicion:\n\nNombre_Archivo = 0{A-z|0-9}96\nExtension_Archivo = 0{A-z}4\nFotografia = Nombre_Archivo+&apos;-&apos;+Extension_Archivo</td></tr><tr><td class='field'>Genero</td><td>ENUM('H', 'M', 'N/B')</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&#10004;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td></td><td>Descripcion: Datos alusivo al genero biologico de la persona\nNaturaleza: Cualitativo\nDominio: Conjunto de valoesr Permitidos\nComposicion: \n\nGenero = [&apos;H&apos;,&apos;M&apos;,&apos;N/B&apos;] </td></tr><tr><td class='field'>Tipo_Sangre</td><td>ENUM('A+', 'A-', 'B+', 'B-', 'ABP-', 'AB+', 'O-', 'O+')</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&#10004;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td></td><td>Descripcion: Datos referentes al tipo y grupo sanguineo\\\\nNaturaleza: Cualitativo\\\\nDominio: Conjunto de valores Permitidos\\\\nComposicion: \\\\n\\\\nGenero = [&apos;AP&apos;, &apos;AN&apos;, &apos;BP&apos;, &apos;BN&apos;, &apos;ABP&apos;, &apos;ABN&apos;, &apos;OP&apos;, &apos;ON&apos;] </td></tr><tr><td class='field'>Estatus</td><td>BIT(1)</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&#10004;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td>b'1'</td><td>Descripcion: Dato de Auditoria que define el estatus actual del regitro, siendo 0 para un datos no activos y 1 para datos activos para uso en el sistema\nNaturaleza: Cuantativo\nDominio: Booleano\nComposicion: [0|1]\n</td></tr><tr><td class='field'>Fecha_Registro</td><td>DATETIME</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&#10004;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td>CURRENT_TIMESTAMP</td><td>Descripcion: Dato de Auditoria que documenta la fecha y hora de creacion del registro\nNaturaleza: Cuantitativo\nDominio: Numeros Enteros Positivos imitados por el calendario y limites de mes y/o a�o bisiesto.\nComposicion:\n\nA�o = 4{0-9}4\nMes =  [01|02|...|12]\nDia =  [01|02|..|31]\n\nHora = [00|01|...|23]\nMinutos = [00|01|...|59]\nSeguntodos = [00|01|...|59]\n\nFecha_Registro= A�o+&apos;-&apos;+Mes+&apos;-&apos;+Dia+&apos;-&apos;+Hora+&apos;-&apos;+Munutos+&apos;-&apos;+Segundos</td></tr><tr><td class='field'>Fecha_Actualizacion</td><td>DATETIME</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td>NULL</td><td>Descripcion: Dato de Auditoria que documenta la fecha y hora de la ultima modificacion del registro\nNaturaleza: Cuantitativo\nDominio: Numeros Enteros Positivos imitados por el calendario y limites de mes y/o a�o bisiesto.\nComposicion:\n\n\nA�o = 4{0-9}4\nMes =  [01|02|...|12]\nDia =  [01|02|..|31]\n\nHora = [00|01|...|23]\nMinutos = [00|01|...|59]\nSeguntodos = [00|01|...|59]\n\nFecha_Actualizacion = A�o+&apos;-&apos;+Mes+&apos;-&apos;+Dia+&apos;-&apos;+Hora+&apos;-&apos;+Munutos+&apos;-&apos;+Segundos</td></tr></table><table id='tbc_servicio'><caption>tbc_servicio</caption><tr><td colspan='12'>Esta tabla almacenar� los datos de los servicios ofrecidos por el gimnasio, los cuales pueden ser de diferentes tipos. Es importante destacar que la tabla servicios esta vinculada con las tablas: SUCURSALES, COLABORADORES, CLIENTES</td></tr><tr><th>Column name</th><th>DataType</th><th><abbr title='Primary Key'>PK</abbr></th><th><abbr title='Foreign Key'>FK</abbr></th><th><abbr title='Not Null'>NN</abbr></th><th><abbr title='Unique'>UQ</abbr></th><th><abbr title='Binary'>BIN</abbr></th><th><abbr title='Unsigned'>UN</abbr></th><th><abbr title='Zero Fill'>ZF</abbr></th><th><abbr title='Auto Increment'>AI</abbr></th><th>Default</th><th>Comment</th></tr><tr><td class='field'>Id</td><td>INT</td><td class='centered'>&#10004;</td><td class='centered'>&nbsp;</td><td class='centered'>&#10004;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&#10004;</td><td></td><td>Descripcion: Atributo identificador n�mero auto incremental que distingue de manera �nica al servicio. \\\\nNaturaleza: Cuantitativo\\\\nDominio: Enteros positivos\\\\nComposicion: 1{0-9}</td></tr><tr><td class='field'>Sucursal_ID</td><td>INT</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&#10004;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td></td><td>Descripci�n: Identificador de la sucursal en la que se ofrece el servicio, relacionado con la tabla Sucursal para indicar la ubicaci�n del servicio.\\nNaturaleza: Cuantitativo\\nDominio: Enteros positivos\\nComposici�n: 1{0-9}</td></tr><tr><td class='field'>Cliente_ID</td><td>INT</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&#10004;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td></td><td>Descripci�n:Identificador �nico que determina qui�n solicito el servicio, relacionado con la tabla Cliente para identificar al cliente.\\\\\\\\nNaturaleza: Cuantitativo\\\\\\\\nDominio: Enteros positivos\\\\\\\\nComposici�n: 1{0-9}</td></tr><tr><td class='field'>Colaborador_ID</td><td>INT</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&#10004;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td></td><td>Descripci�n:Identificador �nico que determina al responsable qui�n creo el registro.\\\\\\\\nNaturaleza: Cuantitativo\\\\\\\\nDominio: Enteros positivos\\\\\\\\nComposici�n: 1{0-9}</td></tr><tr><td class='field'>Nombre</td><td>VARCHAR(80)</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&#10004;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td></td><td>Descripci�n: Valor asociado al servicio que se ofrece al cliente o usuario.\nNaturaleza: Cualitativo\nDominio: Cadena de texto\nComposici�n: 0{A-z }80</td></tr><tr><td class='field'>Descripcion</td><td>TEXT</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td>NULL</td><td>Descripci�n:Contiene una descripci�n detallada del servicio, proporcionando informaci�n adicional sobre sus caracter�sticas y beneficios..\nNaturaleza: Cualitativo\nDominio: Cadena de texto\nComposici�n: {A-z|,|.| |}</td></tr><tr><td class='field'>Costo</td><td>DECIMAL(10,2)</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td>NULL</td><td>Descripci�n: Representa el valor monetario asociado con el servicio, indicado en formato decimal con precisi�n de hasta dos decimales.\nNaturaleza: Cuantitativo\nDominio: N�meros decimales\nComposici�n: 1{0-9}+(.[0-9]{1,2})</td></tr><tr><td class='field'>Tipo_Servicio</td><td>ENUM('Entrenamiento', 'Clase Grupal', 'Nutrici�n', 'Fisioterapia', 'Spa', 'Otros')</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&#10004;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td></td><td>Descripci�n: Especifica el tipo de servicio ofrecido, pudiendo ser individual, grupal, virtual o presencial.\\nNaturaleza: Cualitativo\\nDominio: Conjunto de valores limitados (&apos;individual&apos;, &apos;grupal&apos;)\\nComposici�n:\\n\\nTipo_Servicio = [&apos;Individual&apos;,&apos;Grupal&apos;]</td></tr><tr><td class='field'>Estatus</td><td>BIT(1)</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td>b'1'</td><td>Descripcion: Dato de Auditoria que define el estatus actual del regitro, siendo 0 para un datos no activos y 1 para datos activos para uso en el sistema\\\\nNaturaleza: Cuantativo\\\\nDominio: Booleano\\\\nComposicion: [0|1]\\\\n</td></tr><tr><td class='field'>Fecha_Creacion</td><td>DATETIME</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td>NULL</td><td>Descripcion: Dato de Auditoria que documenta la fecha y hora de creacion del registro\\nNaturaleza: Cuantitativo\\nDominio: Numeros Enteros Positivos imitados por el calendario y limites de mes y/o a�o bisiesto.\\nComposicion:\\n\\nA�o = 4{0-9}4\\nMes =  [01|02|...|12]\\nDia =  [01|02|..|31]\\n\\nHora = [00|01|...|23]\\nMinutos = [00|01|...|59]\\nSeguntodos = [00|01|...|59]\\n\\nFecha_Registro= A�o+&apos;-&apos;+Mes+&apos;-&apos;+Dia+&apos;-&apos;+Hora+&apos;-&apos;+Munutos+&apos;-&apos;+Segundos</td></tr><tr><td class='field'>Fecha_Actualizacion</td><td>VARCHAR(45)</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td class='centered'>&nbsp;</td><td>NULL</td><td>Descripcion: Dato de Auditoria que documenta la fecha y hora en la que fue modificado el registro\\\\nNaturaleza: Cuantitativo\\\\nDominio: Numeros Enteros Positivos imitados por el calendario y limites de mes y/o a�o bisiesto.\\\\nComposicion:\\\\n\\\\nA�o = 4{0-9}4\\\\nMes =  [01|02|...|12]\\\\nDia =  [01|02|..|31]\\\\n\\\\nHora = [00|01|...|23]\\\\nMinutos = [00|01|...|59]\\\\nSeguntodos = [00|01|...|59]\\\\n\\\\nFecha_Registro= A�o+&apos;-&apos;+Mes+&apos;-&apos;+Dia+&apos;-&apos;+Hora+&apos;-&apos;+Munutos+&apos;-&apos;+Segundos</td></tr></table></div>
</body>
</html>
