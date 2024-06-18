# Guía Completa de Metodología BEM y Conceptos Básicos de CSS

## Metodología BEM
BEM es una metodología para nombrar clases en CSS que hace que el código sea más entendible y mantenible. BEM significa Bloques, Elementos y Modificadores.

### Bloques
Un bloque es un componente independiente que representa una parte funcional de la interfaz. Por ejemplo:
```html
<div class="menu"></div>
```

### Elementos
Un elemento es una parte de un bloque que realiza una función específica. Se denota con dos guiones bajos `__`. Por ejemplo:
```html
<div class="menu__item"></div>
```
```html
<div class="card">
  <div class="card__header"></div>
  <div class="card__body"></div>
  <div class="card__footer"></div>
</div>
```

### Modificadores
Un modificador es una variación o estado de un bloque o elemento. Se denota con dos guiones `--`. Por ejemplo:
```html
<div class="menu menu--active"></div>
<div class="menu__item menu__item--selected"></div>
```
```html
<div class="button button--large button--primary"></div>
<div class="card card--highlighted"></div>
```

## Box Modeling (Modelo de Caja)
El modelo de caja describe cómo se componen los elementos HTML en términos de margen, borde, relleno y contenido.

- **Contenido:** El área donde se muestra el texto o las imágenes.
- **Relleno (Padding):** El espacio entre el contenido y el borde.
- **Borde (Border):** El borde alrededor del relleno y el contenido.
- **Margen (Margin):** El espacio fuera del borde.

```css
.element {
  margin: 10px;   /* margen externo */
  border: 2px solid black;  /* borde del elemento */
  padding: 10px;  /* espacio interno */
  width: 100px;   /* ancho del contenido */
}
```

Ejemplo visual de un box model:

```html
<div class="box-model-example">
  Contenido
</div>
```

```css
.box-model-example {
  margin: 20px;
  border: 5px solid red;
  padding: 15px;
  width: 200px;
  background-color: lightblue;
}
```

## Display
El `display` es una propiedad que determina cómo se comporta un elemento en la página.

### Display Block
Un elemento con `display: block` ocupa todo el ancho disponible y empieza en una nueva línea.

```css
.block-element {
  display: block;
}
```

Ejemplo:
```html
<div class="block-element">Elemento bloque 1</div>
<div class="block-element">Elemento bloque 2</div>
```

### Display Inline
Un elemento con `display: inline` no comienza en una nueva línea y solo ocupa el ancho necesario.

```css
.inline-element {
  display: inline;
}
```

Ejemplo:
```html
<span class="inline-element">Elemento inline 1</span>
<span class="inline-element">Elemento inline 2</span>
```

### Display Inline-block
Un elemento con `display: inline-block` se comporta como un `inline`, pero permite definir dimensiones como un `block`.

```css
.inline-block-element {
  display: inline-block;
  width: 100px;
  height: 100px;
}
```

Ejemplo:
```html
<div class="inline-block-element">Elemento inline-block 1</div>
<div class="inline-block-element">Elemento inline-block 2</div>
```

## Posiciones
La propiedad `position` especifica el método de posicionamiento de un elemento.

### Relativa
Un elemento con `position: relative` se posiciona relativo a su posición normal.

```css
.relative-element {
  position: relative;
  top: 10px;   /* se desplaza hacia abajo 10px desde su posición original */
  left: 10px;  /* se desplaza hacia la derecha 10px desde su posición original */
}
```

Ejemplo:
```html
<div class="relative-element">Elemento relativo</div>
```

### Absoluta
Un elemento con `position: absolute` se posiciona respecto a su contenedor más cercano que no tenga `position: static`.

```css
.absolute-element {
  position: absolute;
  top: 10px;    /* se posiciona 10px desde la parte superior del contenedor */
  left: 10px;   /* se posiciona 10px desde la parte izquierda del contenedor */
}
```

Ejemplo:
```html
<div class="container" style="position: relative;">
  <div class="absolute-element">Elemento absoluto</div>
</div>
```

### Fixed
Un elemento con `position: fixed` se posiciona relativo a la ventana del navegador.

```css
.fixed-element {
  position: fixed;
  top: 10px;    /* se posiciona 10px desde la parte superior de la ventana */
  left: 10px;   /* se posiciona 10px desde la parte izquierda de la ventana */
}
```

Ejemplo:
```html
<div class="fixed-element">Elemento fijo</div>
```

### Sticky
Un elemento con `position: sticky` se comporta como `relative` hasta que se cumple una condición de scroll, luego se comporta como `fixed`.

```css
.sticky-element {
  position: sticky;
  top: 10px;    /* se adhiere 10px desde la parte superior del contenedor cuando se hace scroll */
}
```

Ejemplo:
```html
<div class="sticky-element">Elemento sticky</div>
```

## Z-index
La propiedad `z-index` controla la superposición de elementos en el eje Z (profundidad). Solo funciona en elementos posicionados (que no tengan `position: static`).

```css
.z-index-element {
  position: relative; /* o absolute, fixed, sticky */
  z-index: 10;        /* valor de la superposición */
}
```

Ejemplo:
```html
<div class="z-index-element" style="z-index: 10; position: absolute;">Elemento con z-index 10</div>
<div class="z-index-element" style="z-index: 5; position: absolute;">Elemento con z-index 5</div>
```

En este ejemplo, el primer elemento con `z-index: 10` se mostrará sobre el segundo elemento con `z-index: 5`.



## [Autor: Alejandro Di Stefano](https://github.com/Drako01)