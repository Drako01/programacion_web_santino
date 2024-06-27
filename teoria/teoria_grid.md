# Teoría de CSS Grid

CSS Grid Layout es un sistema de diseño bidimensional que permite la creación de interfaces web complejas mediante el uso de filas y columnas. A continuación, se presenta un resumen de los conceptos fundamentales de CSS Grid.

## Conceptos Básicos

### Contenedor Grid
Para utilizar CSS Grid, se debe definir un contenedor como grid. Esto se hace utilizando la propiedad `display: grid;` en el contenedor.

```css
.container {
    display: grid;
}
```

### Columnas y Filas
Las columnas y filas se definen utilizando las propiedades `grid-template-columns` y `grid-template-rows`.

```css
.container {
    display: grid;
    grid-template-columns: 100px 200px;
    grid-template-rows: 100px 200px;
}
```
Este ejemplo crea un grid con dos columnas (de 100px y 200px) y dos filas (de 100px y 200px).

### Unidades de Medida
Se pueden utilizar diferentes unidades de medida para definir el tamaño de las columnas y filas:
- **px**: píxeles
- **%**: porcentaje
- **fr**: fracciones del espacio disponible
- **auto**: tamaño automático basado en el contenido
- **min-content** y **max-content**: tamaño mínimo y máximo del contenido

```css
.container {
    display: grid;
    grid-template-columns: 1fr 2fr;
    grid-template-rows: auto 100px;
}
```

### Colocación de Elementos
Los elementos dentro del grid se pueden colocar explícitamente utilizando las propiedades `grid-column` y `grid-row`.

```css
.item1 {
    grid-column: 1 / 3;
    grid-row: 1 / 2;
}
```
Esto coloca el primer elemento (`item1`) desde la columna 1 hasta la columna 3 y en la fila 1.

## Propiedades del Contenedor Grid

### `grid-gap`, `row-gap`, y `column-gap`
Estas propiedades definen el espacio entre las filas y las columnas.

```css
.container {
    display: grid;
    grid-gap: 10px;
    row-gap: 15px;
    column-gap: 20px;
}
```

### `grid-template-areas`
Permite nombrar áreas del grid para una colocación más fácil de los elementos.

```css
.container {
    display: grid;
    grid-template-areas:
        "header header"
        "sidebar content"
        "footer footer";
}

.header { grid-area: header; }
.sidebar { grid-area: sidebar; }
.content { grid-area: content; }
.footer { grid-area: footer; }
```

### `grid-auto-rows` y `grid-auto-columns`
Define el tamaño de las filas y columnas generadas automáticamente.

```css
.container {
    display: grid;
    grid-auto-rows: 100px;
    grid-auto-columns: 100px;
}
```

## Propiedades de los Elementos Grid

### `grid-column` y `grid-row`
Especifican el inicio y el final de las columnas y filas en las que se coloca un elemento.

```css
.item {
    grid-column: 1 / 3;
    grid-row: 2 / 4;
}
```

### `grid-area`
Combina las propiedades `grid-column` y `grid-row` en una sola.

```css
.item {
    grid-area: 1 / 1 / 3 / 3;
}
```

### `justify-self` y `align-self`
Controlan la alineación de un elemento dentro de su celda.

```css
.item {
    justify-self: center;
    align-self: end;
}
```

## Ejemplo Completo

HTML:
```html
<div class="container">
    <div class="header">Header</div>
    <div class="sidebar">Sidebar</div>
    <div class="content">Content</div>
    <div class="footer">Footer</div>
</div>
```

CSS:
```css
.container {
    display: grid;
    grid-template-areas:
        "header header"
        "sidebar content"
        "footer footer";
    grid-gap: 10px;
}

.header {
    grid-area: header;
    background-color: #f3f3f3;
}

.sidebar {
    grid-area: sidebar;
    background-color: #f9f9f9;
}

.content {
    grid-area: content;
    background-color: #e3e3e3;
}

.footer {
    grid-area: footer;
    background-color: #d3d3d3;
}
```

## Recursos Adicionales
- [MDN Web Docs sobre CSS Grid](https://developer.mozilla.org/es/docs/Web/CSS/CSS_Grid_Layout)
- [CSS Tricks: A Complete Guide to Grid](https://css-tricks.com/snippets/css/complete-guide-grid/)

---

## Resumen:

**1. Introducción a CSS Grid Layout**
   - CSS Grid Layout es un sistema de diseño en CSS para crear interfaces web complejas.
   - Utiliza una cuadrícula de filas y columnas para distribuir el contenido.

**2. Contenedor Grid**
   - Se define con `display: grid;`.
   - Ejemplo: 
     ```css
     .container {
         display: grid;
     }
     ```

**3. Definición de Filas y Columnas**
   - Usar `grid-template-columns` y `grid-template-rows`.
   - Ejemplo: 
     ```css
     .container {
         display: grid;
         grid-template-columns: 100px 200px;
         grid-template-rows: 100px 200px;
     }
     ```

**4. Unidades de Medida**
   - `px`, `%`, `fr`, `auto`, `min-content`, `max-content`.
   - Ejemplo: 
     ```css
     .container {
         display: grid;
         grid-template-columns: 1fr 2fr;
         grid-template-rows: auto 100px;
     }
     ```

**5. Colocación de Elementos**
   - Usar `grid-column` y `grid-row`.
   - Ejemplo: 
     ```css
     .item1 {
         grid-column: 1 / 3;
         grid-row: 1 / 2;
     }
     ```

**6. Espaciado entre Filas y Columnas**
   - Usar `grid-gap`, `row-gap`, `column-gap`.
   - Ejemplo: 
     ```css
     .container {
         display: grid;
         grid-gap: 10px;
         row-gap: 15px;
         column-gap: 20px;
     }
     ```

**7. Áreas del Grid**
   - Usar `grid-template-areas`.
   - Ejemplo: 
     ```css
     .container {
         display: grid;
         grid-template-areas:
             "header header"
             "sidebar content"
             "footer footer";
     }
     ```

**8. Tamaño Automático de Filas y Columnas**
   - Usar `grid-auto-rows`, `grid-auto-columns`.
   - Ejemplo: 
     ```css
     .container {
         display: grid;
         grid-auto-rows: 100px;
         grid-auto-columns: 100px;
     }
     ```

**9. Propiedades de los Elementos**
   - `grid-column`, `grid-row`, `grid-area`.
   - Ejemplo: 
     ```css
     .item {
         grid-column: 1 / 3;
         grid-row: 2 / 4;
     }
     ```
     ```css
     .item {
         grid-area: 1 / 1 / 3 / 3;
     }
     ```

**10. Alineación de Elementos**
   - Usar `justify-self`, `align-self`.
   - Ejemplo: 
     ```css
     .item {
         justify-self: center;
         align-self: end;
     }
     ```

---

Este material proporciona una base completa y detallada sobre CSS Grid, combinando teoría y ejemplos prácticos.

---

## [Autor: Alejandro Di Stefano](https://github.com/Drako01)




