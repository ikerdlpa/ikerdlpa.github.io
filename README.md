<html>
<head>
    <h1 style="text-align:center; font-size:150px;">MUN UVM 24</h1>
</head>
<body>
    <h2 style="text-align:center; font-size:100px;">Comités</h2>
    <ul>
        <li><a href="pagina_comite1.html">Comité 1</a></li>
        <li><a href="pagina_comite2.html">Comité 2</a></li>
        <li><a href="pagina_comite3.html">Comité 3</a></li>
        <li><a href="pagina_comite4.html">Comité 4</a></li>
    </ul>
</body>
  <h3 style="text-align:center; font-size:75px; ">Siempre responsables de lo que se ha cultivado</h3>

<head>
    <title>Asistencia</title>
    <style>
        table {
            border-collapse: collapse;
            width: 50%;
            margin: 20px auto;
        }

        th, td {
            border: 1px solid black;
            padding: 8px;
            text-align: center;
        }

        th {
            background-color: #f2f2f2;
        }

        td button {
            background-color: transparent;
            border: none;
            cursor: pointer;
        }

        .presente {
            background-color: green;
        }
    </style>
</head>
<body>
    <h1>Asistencia</h1>
    
    <table>
        <tr>
            <th>País</th>
            <th>Presente</th>
        </tr>
    </table>

    <ul>
        <li><button onclick="agregarPais('País 1')">+ País 1</button></li>
        <li><button onclick="agregarPais('País 2')">+ País 2</button></li>
        <li><button onclick="agregarPais('País 3')">+ País 3</button></li>
    </ul>

    <script>
        function agregarPais(pais) {
            var table = document.querySelector("table");
            var row = table.insertRow(-1);
            var cell1 = row.insertCell(0);
            var cell2 = row.insertCell(1);

            cell1.innerHTML = pais;
            cell2.innerHTML = '<button onclick="marcarPresente(this)">Presente</button>';
        }

        function marcarPresente(button) {
            button.parentElement.parentElement.classList.toggle('presente');
        }
    </script>
</body>
</html>
