# Introducción a Flexbox

Flexbox, o "Flexible Box Layout Module", es un modelo de diseño en CSS3 que permite distribuir espacio y alinear elementos de forma eficiente y predecible dentro de un contenedor, incluso cuando el tamaño de los elementos es desconocido o dinámico. Flexbox es ideal para crear layouts de una dimensión, es decir, layouts que son filas o columnas de elementos.

## Conceptos Básicos de Flexbox

### Contenedor Flex y Elementos Flex

- **Contenedor Flex**: El elemento padre que tiene la propiedad `display: flex` o `display: inline-flex`.
- **Elementos Flex**: Los elementos hijos directos del contenedor flex.

### Propiedades del Contenedor Flex

1. **display**: Define el contenedor flex. 
   ```css
   .contenedor {
       display: flex; /* o inline-flex */
   }
   ```

2. **flex-direction**: Define la dirección del eje principal.
   - `row` (por defecto): De izquierda a derecha.
   - `row-reverse`: De derecha a izquierda.
   - `column`: De arriba a abajo.
   - `column-reverse`: De abajo a arriba.
   ```css
   .contenedor {
       flex-direction: row; /* row, row-reverse, column, column-reverse */
   }
   ```

3. **flex-wrap**: Define si los elementos flex deben envolver o no.
   - `nowrap` (por defecto): Los elementos no envuelven.
   - `wrap`: Los elementos envuelven a la siguiente línea.
   - `wrap-reverse`: Los elementos envuelven a la siguiente línea en reversa.
   ```css
   .contenedor {
       flex-wrap: wrap; /* nowrap, wrap, wrap-reverse */
   }
   ```

4. **justify-content**: Define la alineación de los elementos a lo largo del eje principal.
   - `flex-start` (por defecto): Elementos al inicio del contenedor.
   - `flex-end`: Elementos al final del contenedor.
   - `center`: Elementos en el centro del contenedor.
   - `space-between`: Espacio igual entre elementos.
   - `space-around`: Espacio igual alrededor de los elementos.
   ```css
   .contenedor {
       justify-content: center; /* flex-start, flex-end, center, space-between, space-around */
   }
   ```

5. **align-items**: Define la alineación de los elementos a lo largo del eje transversal.
   - `stretch` (por defecto): Estira los elementos para llenar el contenedor.
   - `flex-start`: Elementos al inicio del eje transversal.
   - `flex-end`: Elementos al final del eje transversal.
   - `center`: Elementos en el centro del eje transversal.
   - `baseline`: Elementos alineados según su línea base.
   ```css
   .contenedor {
       align-items: center; /* stretch, flex-start, flex-end, center, baseline */
   }
   ```

6. **align-content**: Define la alineación de las líneas de elementos flex cuando hay espacio extra en el eje transversal (se aplica cuando hay múltiples líneas de elementos).
   - `stretch` (por defecto): Las líneas se estiran para llenar el contenedor.
   - `flex-start`: Líneas al inicio del contenedor.
   - `flex-end`: Líneas al final del contenedor.
   - `center`: Líneas en el centro del contenedor.
   - `space-between`: Espacio igual entre las líneas.
   - `space-around`: Espacio igual alrededor de las líneas.
   ```css
   .contenedor {
       align-content: center; /* stretch, flex-start, flex-end, center, space-between, space-around */
   }
   ```

### Propiedades de los Elementos Flex

1. **order**: Define el orden de los elementos flex.
   ```css
   .elemento {
       order: 2; /* Valor por defecto es 0 */
   }
   ```

2. **flex-grow**: Define la capacidad de un elemento para crecer en relación a los otros elementos flex.
   ```css
   .elemento {
       flex-grow: 2; /* Valor por defecto es 0 */
   }
   ```

3. **flex-shrink**: Define la capacidad de un elemento para reducir su tamaño en relación a los otros elementos flex.
   ```css
   .elemento {
       flex-shrink: 1; /* Valor por defecto es 1 */
   }
   ```

4. **flex-basis**: Define el tamaño inicial de un elemento antes de que el espacio restante sea distribuido.
   ```css
   .elemento {
       flex-basis: 100px; /* Valor por defecto es auto */
   }
   ```

5. **flex**: Una propiedad abreviada para `flex-grow`, `flex-shrink` y `flex-basis`.
   ```css
   .elemento {
       flex: 1 1 100px; /* flex-grow flex-shrink flex-basis */
   }
   ```

6. **align-self**: Permite la alineación de un solo elemento, ignorando la propiedad `align-items` del contenedor.
   ```css
   .elemento {
       align-self: center; /* auto, flex-start, flex-end, center, baseline, stretch */
   }
   ```

## Ejemplos Prácticos

### Ejemplo 1: Centrando un elemento horizontalmente y verticalmente

HTML:
```html
<div class="contenedor">
    <div class="elemento">Centrado</div>
</div>
```

CSS:
```css
.contenedor {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh; /* Altura del viewport */
}

.elemento {
    background-color: lightblue;
    padding: 20px;
}
```

### Ejemplo 2: Distribuyendo elementos equitativamente

HTML:
```html
<div class="contenedor">
    <div class="elemento">1</div>
    <div class="elemento">2</div>
    <div class="elemento">3</div>
</div>
```

CSS:
```css
.contenedor {
    display: flex;
    justify-content: space-between;
}

.elemento {
    background-color: lightblue;
    padding: 20px;
}
```

### Ejemplo 3: Barra de navegación

HTML:
```html
<nav class="navbar">
    <ul class="nav-list">
        <li class="nav-item">Inicio</li>
        <li class="nav-item">Servicios</li>
        <li class="nav-item">Contacto</li>
    </ul>
</nav>
```

CSS:
```css
.navbar {
    background-color: #333;
    padding: 10px;
}

.nav-list {
    display: flex;
    justify-content: space-around;
    list-style-type: none;
    margin: 0;
    padding: 0;
}

.nav-item {
    color: white;
}
```

### Ejemplo 4: Flex-grow y Flex-shrink

HTML:
```html
<div class="contenedor">
    <div class="elemento" style="flex-grow: 1;">1</div>
    <div class="elemento" style="flex-grow: 2;">2</div>
    <div class="elemento" style="flex-grow: 1;">3</div>
</div>
```

CSS:
```css
.contenedor {
    display: flex;
}

.elemento {
    background-color: lightblue;
    padding: 20px;
    border: 1px solid #000;
}
```

### Ejemplo 5: Galería de imágenes

HTML:
```html
<div class="galeria">
    <div class="imagen">Imagen 1</div>
    <div class="imagen">Imagen 2</div>
    <div class="imagen">Imagen 3</div>
    <div class="imagen">Imagen 4</div>
</div>
```

CSS:
```css
.galeria {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-around;
}

.imagen {
    background-color: lightblue;
    padding: 20px;
    margin: 10px;
    flex-basis: 200px;
    text-align: center;
}
```

### Ejemplo 6: Layout de página completa

HTML:
```html
<div class="pagina">
    <header class="header">Header</header>
    <div class="contenido">
        <aside class="sidebar">Sidebar</aside>
        <main class="main">Contenido principal</main>
    </div>
    <footer class="footer">Footer</footer>
</div>
```

CSS:
```css
.pagina {
    display: flex;
    flex-direction: column;
    height: 100vh;
}

.header, .footer {
    background-color: #333;
    color: white;
    padding: 20px;
    text-align: center;
}

.contenido {
    display: flex;
    flex: 1;
}

.sidebar {
    background-color: #f4f4f4;
    padding: 20px;
    flex-basis: 200px;
}

.main {
    background-color: #e2e2e2;
    padding: 20px;
    flex: 1;
}
```



### Ejemplo 7: Formulario alineado

HTML:
```html
<form class="formulario">
    <label for="nombre">Nombre:</label>
    <input type="text" id="nombre" name="nombre">
    <label for="email">Email:</label>
    <input type="email" id="email" name="email">
    <button type="submit">Enviar</button>
</form>
```

CSS:
```css
.formulario {
    display: flex;
    flex-direction: column;
    width: 300px;
    margin: 0 auto;
}

.formulario label, .formulario input, .formulario button {
    margin-bottom: 10px;
}
```

### Ejemplo 8: Layout de dos columnas

HTML:
```html
<div class="contenedor">
    <div class="columna izquierda">Columna Izquierda</div>
    <div class="columna derecha">Columna Derecha</div>
</div>
```

CSS:
```css
.contenedor {
    display: flex;
}

.columna {
    padding: 20px;
    flex: 1;
}

.izquierda {
    background-color: lightblue;
}

.derecha {
    background-color: lightcoral;
}
```

### Ejemplo 9: Tarjetas de producto alineadas

HTML:
```html
<div class="tarjetas">
    <div class="tarjeta">
        <img src="producto1.jpg" alt="Producto 1">
        <h3>Producto 1</h3>
        <p>Descripción del producto 1</p>
    </div>
    <div class="tarjeta">
        <img src="producto2.jpg" alt="Producto 2">
        <h3>Producto 2</h3>
        <p>Descripción del producto 2</p>
    </div>
    <div class="tarjeta">
        <img src="producto3.jpg" alt="Producto 3">
        <h3>Producto 3</h3>
        <p>Descripción del producto 3</p>
    </div>
</div>
```

CSS:
```css
.tarjetas {
    display: flex;
    justify-content: space-around;
}

.tarjeta {
    background-color: white;
    border: 1px solid #ddd;
    padding: 20px;
    text-align: center;
    flex-basis: 200px;
}
```

### Ejemplo 10: Diseño de sección de testimonios

HTML:
```html
<section class="testimonios">
    <div class="testimonio">
        <p>"Excelente servicio y atención."</p>
        <cite>- Cliente 1</cite>
    </div>
    <div class="testimonio">
        <p>"Productos de alta calidad."</p>
        <cite>- Cliente 2</cite>
    </div>
    <div class="testimonio">
        <p>"Recomendado al 100%."</p>
        <cite>- Cliente 3</cite>
    </div>
</section>
```

CSS:
```css
.testimonios {
    display: flex;
    flex-direction: column;
    align-items: center;
}

.testimonio {
    background-color: #f9f9f9;
    border: 1px solid #ddd;
    padding: 20px;
    margin-bottom: 20px;
    width: 80%;
    text-align: center;
}
```



---

## [Autor: Alejandro Di Stefano](https://github.com/Drako01)