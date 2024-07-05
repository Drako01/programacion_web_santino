# Tutorial Completo de HTML5 y CSS3

## 1. Armado de Formularios

Los formularios permiten a los usuarios enviar datos a un servidor. A continuación, se describe cómo crear formularios básicos y avanzados en HTML5.

### Formulario Básico

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <title>Formulario Básico</title>
</head>
<body>
    <h1>Formulario de Registro</h1>
    <form action="/submit" method="post">
        <div>
            <label for="nombre">Nombre:</label>
            <input type="text" id="nombre" name="nombre" required>
        </div>
        <div>
            <label for="email">Email:</label>
            <input type="email" id="email" name="email" required>
        </div>
        <div>
            <label for="pais">País de Origen:</label>
            <select name="pais" id="pais">
                <option value="" disabled selected>Seleccione una Opción</option>
                <option value="arg">Argentina</option>
                <option value="br">Brasil</option>
                <option value="ur">Uruguay</option>
                <option value="cl">Chile</option>
                <option value="pr">Paraguay</option>
            </select>
        </div>
        <div>
            <label for="mensaje">Mensaje:</label>
            <textarea id="mensaje" name="mensaje"></textarea>
        </div>
        <button type="submit">Enviar</button>
    </form>
</body>
</html>
```

### Elementos del Formulario

- `<form>`: Define el formulario.
  - `action`: La URL a la que se envían los datos del formulario.
  - `method`: El método HTTP para enviar los datos (`get` o `post`).

- `<label>`: Etiqueta descriptiva para el campo.
- `<input>`: Campo de entrada de datos.
  - `type`: Define el tipo de campo (`text`, `email`, `password`, etc.).
  - `id` y `name`: Atributos que identifican el campo y lo asocian con una etiqueta.
  - `required`: Hace que el campo sea obligatorio.
  
- `<select>`: Menú desplegable.
  - `<option>`: Opciones dentro del menú desplegable.
  - `disabled`: Deshabilita la opción.
  - `selected`: Selecciona la opción por defecto.
  
- `<textarea>`: Campo de texto multilínea.
- `<button>`: Botón para enviar el formulario.

### Formulario Avanzado con CSS

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <title>Formulario Avanzado</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f4;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
        }
        form {
            background: #fff;
            padding: 20px;
            border-radius: 5px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }
        div {
            margin-bottom: 15px;
        }
        label {
            display: block;
            margin-bottom: 5px;
        }
        input, select, textarea, button {
            width: 100%;
            padding: 10px;
            border: 1px solid #ccc;
            border-radius: 5px;
            font-size: 16px;
        }
        button {
            background-color: #28a745;
            color: white;
            border: none;
            cursor: pointer;
        }
        button:hover {
            background-color: #218838;
        }
    </style>
</head>
<body>
    <form action="/submit" method="post">
        <h1>Formulario de Registro</h1>
        <div>
            <label for="nombre">Nombre:</label>
            <input type="text" id="nombre" name="nombre" required>
        </div>
        <div>
            <label for="email">Email:</label>
            <input type="email" id="email" name="email" required>
        </div>
        <div>
            <label for="pais">País de Origen:</label>
            <select name="pais" id="pais">
                <option value="" disabled selected>Seleccione una Opción</option>
                <option value="arg">Argentina</option>
                <option value="br">Brasil</option>
                <option value="ur">Uruguay</option>
                <option value="cl">Chile</option>
                <option value="pr">Paraguay</option>
            </select>
        </div>
        <div>
            <label for="mensaje">Mensaje:</label>
            <textarea id="mensaje" name="mensaje"></textarea>
        </div>
        <button type="submit">Enviar</button>
    </form>
</body>
</html>
```

## 2. Manejo de Media Queries

Las media queries permiten aplicar diferentes estilos CSS según las características del dispositivo, como el ancho de la pantalla. Esto hace que tu sitio web sea responsivo.

### Ejemplo de Media Queries

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <title>Media Queries</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: lightgray;
        }
        .container {
            width: 100%;
            padding: 20px;
            background-color: lightgray;
            text-align: center;
        }
        @media (min-width: 600px) {
            .container {
                background-color: lightblue;
            }
        }
        @media (min-width: 800px) {
            .container {
                background-color: lightgreen;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Contenido Responsivo</h1>
        <p>Redimensiona la ventana del navegador para ver los cambios de color.</p>
    </div>
</body>
</html>
```

### Explicación

- `@media`: Define una media query.
- `(min-width: 600px)`: Aplica los estilos dentro de la media query solo si el ancho de la pantalla es al menos 600px.
- `.container`: Clase que cambia de color según el ancho de la pantalla.

### Más Ejemplos de Media Queries

#### Ocultar Elementos en Pantallas Pequeñas

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <title>Ocultar Elementos</title>
    <style>
        .sidebar {
            display: block;
            width: 200px;
            background-color: #ddd;
            padding: 10px;
        }
        @media (max-width: 600px) {
            .sidebar {
                display: none;
            }
        }
    </style>
</head>
<body>
    <div class="sidebar">
        <h2>Barra Lateral</h2>
        <p>Contenido de la barra lateral.</p>
    </div>
</body>
</html>
```

#### Ajuste de Fuentes y Espaciado

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <title>Ajuste de Fuentes</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            line-height: 1.6;
        }
        @media (max-width: 600px) {
            body {
                font-size: 14px;
                line-height: 1.4;
            }
        }
        @media (min-width: 601px) and (max-width: 1024px) {
            body {
                font-size: 16px;
                line-height: 1.5;
            }
        }
        @media (min-width: 1025px) {
            body {
                font-size: 18px;
                line-height: 1.6;
            }
        }
    </style>
</head>
<body>
    <h1>Ajuste de Fuentes y Espaciado</h1>
    <p>Este texto ajusta su tamaño y espaciado según el ancho de la pantalla.</p>
</body>
</html>
```

## 3. Pseudoclases en CSS

Las pseudoclases en CSS se utilizan para definir un estado especial de un elemento. Algunas pseudoclases comunes son `:hover`, `:focus`, `:active`, y `:nth-child()`.

### Ejemplo de Pseudoclases

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <title>Pseudoclases</title>
    <style>
        a:link {
            color: blue;
        }
        a:visited {
            color: purple;
        }
        a:hover {
            color: red;
        }
        a:active {
            color: orange;
        }
        input:focus

 {
            border-color: blue;
        }
        li:nth-child(odd) {
            background-color: lightgray;
        }
        li:nth-child(even) {
            background-color: white;
        }
    </style>
</head>
<body>
    <h1>Enlaces</h1>
    <a href="https://www.example.com">Visita Ejemplo</a>
    <h1>Campos de Entrada</h1>
    <input type="text" placeholder="Escribe algo...">
    <h1>Lista</h1>
    <ul>
        <li>Elemento 1</li>
        <li>Elemento 2</li>
        <li>Elemento 3</li>
        <li>Elemento 4</li>
    </ul>
</body>
</html>
```

### Explicación

- `:link`: Aplica estilos a enlaces que no han sido visitados.
- `:visited`: Aplica estilos a enlaces que han sido visitados.
- `:hover`: Aplica estilos cuando el ratón está sobre el enlace.
- `:active`: Aplica estilos cuando se hace clic en el enlace.
- `:focus`: Aplica estilos cuando el campo de entrada está enfocado.
- `:nth-child(n)`: Aplica estilos al n-ésimo hijo de su elemento padre (en este caso, los elementos `li`).

## 4. Armado de Tablas

Las tablas se utilizan para mostrar datos tabulares en HTML. Aquí se explica cómo crear tablas básicas y avanzadas.

### Tabla Básica

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <title>Tabla Básica</title>
</head>
<body>
    <h1>Lista de Estudiantes</h1>
    <table border="1">
        <thead>
            <tr>
                <th>Nombre</th>
                <th>Edad</th>
                <th>Grado</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>Alejandro</td>
                <td>20</td>
                <td>3º</td>
            </tr>
            <tr>
                <td>Maria</td>
                <td>22</td>
                <td>4º</td>
            </tr>
            <tr>
                <td>Juan</td>
                <td>19</td>
                <td>2º</td>
            </tr>
        </tbody>
    </table>
</body>
</html>
```

### Elementos de la Tabla

- `<table>`: Define la tabla.
- `<thead>`: Encabezado de la tabla.
- `<tr>`: Fila de la tabla.
- `<th>`: Celda de encabezado.
- `<tbody>`: Cuerpo de la tabla.
- `<td>`: Celda de datos.

### Tabla Avanzada con CSS

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <title>Tabla Avanzada</title>
    <style>
        body {
            font-family: Arial, sans-serif;
        }
        table {
            width: 100%;
            border-collapse: collapse;
        }
        th, td {
            padding: 10px;
            text-align: left;
            border-bottom: 1px solid #ddd;
        }
        tr:hover {
            background-color: #f5f5f5;
        }
        th {
            background-color: #f2f2f2;
        }
    </style>
</head>
<body>
    <h1>Lista de Estudiantes</h1>
    <table>
        <thead>
            <tr>
                <th>Nombre</th>
                <th>Edad</th>
                <th>Grado</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>Alejandro</td>
                <td>20</td>
                <td>3º</td>
            </tr>
            <tr>
                <td>Maria</td>
                <td>22</td>
                <td>4º</td>
            </tr>
            <tr>
                <td>Juan</td>
                <td>19</td>
                <td>2º</td>
            </tr>
        </tbody>
    </table>
</body>
</html>
```

### Explicación

- `border-collapse`: Colapsa los bordes de la tabla en uno solo.
- `padding`: Espaciado dentro de las celdas.
- `text-align`: Alineación del texto en las celdas.
- `border-bottom`: Borde inferior de las celdas.
- `tr:hover`: Cambia el fondo de la fila al pasar el ratón por encima.
- `background-color`: Color de fondo de las celdas.

## Conclusión

Este tutorial cubre los conceptos básicos y avanzados de formularios, media queries, pseudoclases y tablas en HTML5 y CSS3. Con esta base, estarás bien equipado para crear sitios web interactivos y responsivos.



---

## [Autor: Alejandro Di Stefano](https://github.com/Drako01)




