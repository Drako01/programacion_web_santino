# Ejercicios de Metodología BEM y Conceptos Básicos de CSS

## Metodología BEM

### Ejercicio 1: Crear un Bloque
Crea un bloque llamado `header` con contenido de texto que diga "Este es el encabezado".

### Ejercicio 2: Crear Elementos
Dentro del bloque `header`, agrega dos elementos llamados `header__title` y `header__subtitle` con el texto "Título" y "Subtítulo", respectivamente.

### Ejercicio 3: Agregar Modificadores
Añade un modificador `header--large` al bloque `header` para cambiar su tamaño.

### Ejercicio 4: Modificadores en Elementos
Agrega un modificador `header__title--highlighted` al elemento `header__title` para cambiar su color de fondo.

### Ejercicio 5: Crear Múltiples Bloques
Crea dos bloques llamados `card` y `footer`. Cada bloque debe tener elementos internos utilizando la metodología BEM.

## Box Modeling (Modelo de Caja)

### Ejercicio 6: Aplicar Márgenes
Crea un `div` con clase `box` y aplica un margen de 20px alrededor de él.

### Ejercicio 7: Aplicar Relleno
Añade un relleno de 15px dentro del `div` con clase `box`.

### Ejercicio 8: Aplicar Bordes
Aplica un borde de 5px sólido y de color azul al `div` con clase `box`.

### Ejercicio 9: Cambiar el Ancho y Alto
Modifica el `div` con clase `box` para que tenga un ancho de 200px y un alto de 100px.

### Ejercicio 10: Combinar Propiedades del Modelo de Caja
Combina márgenes, rellenos y bordes para crear un diseño de caja completa.

## Display

### Ejercicio 11: Display Block
Crea dos `div` con clase `block-element` y configúralos con `display: block`. Cada `div` debe tener un color de fondo diferente y ocupar todo el ancho disponible.

### Ejercicio 12: Display Inline
Crea tres `span` con clase `inline-element` y configúralos con `display: inline`. Cada `span` debe tener un color de fondo diferente.

### Ejercicio 13: Display Inline-block
Crea cuatro `div` con clase `inline-block-element` y configúralos con `display: inline-block`. Cada `div` debe tener un ancho de 50px y un alto de 50px, con diferentes colores de fondo.

## Posiciones

### Ejercicio 14: Posición Relativa
Crea un `div` con clase `relative-element` y configúralo con `position: relative`. Desplázalo 10px desde la parte superior y 20px desde la parte izquierda.

### Ejercicio 15: Posición Absoluta
Crea un `div` contenedor con clase `container` y un `div` hijo con clase `absolute-element`. Configura el `div` hijo con `position: absolute` y posiciónalo 30px desde la parte superior y 40px desde la parte izquierda del contenedor.

### Ejercicio 16: Posición Fija
Crea un `div` con clase `fixed-element` y configúralo con `position: fixed`. Posiciónalo 50px desde la parte superior y 60px desde la parte izquierda de la ventana del navegador.

### Ejercicio 17: Posición Sticky
Crea un `div` con clase `sticky-element` y configúralo con `position: sticky`. Haz que se adhiera 10px desde la parte superior del contenedor cuando se haga scroll.

## Z-index

### Ejercicio 18: Aplicar Z-index
Crea dos `div` con clases `z-index-element1` y `z-index-element2`. Configura el primer `div` con `z-index: 10` y el segundo con `z-index: 5`. Asegúrate de que ambos `div` tengan `position: relative`.

### Ejercicio 19: Superposición con Z-index
Crea tres `div` superpuestos con diferentes colores de fondo. Utiliza `z-index` para controlar cuál `div` se muestra encima de los demás.

### Ejercicio 20: Z-index en un Contenedor
Crea un contenedor con tres `div` hijos. Configura los `div` hijos con diferentes valores de `z-index` y observa cómo cambia su superposición.

## Ejercicios Combinados

### Ejercicio 21: Crear una Tarjeta de Perfil
Crea un componente de tarjeta de perfil utilizando la metodología BEM. La tarjeta debe tener un bloque `profile-card`, un elemento `profile-card__header`, `profile-card__body` y `profile-card__footer`. Usa modificadores para cambiar el estilo de la tarjeta en diferentes estados.

### Ejercicio 22: Layout de Navegación
Crea un menú de navegación con bloques `nav`, `nav__item`, y `nav__link`. Utiliza `display: inline-block` para los elementos de navegación y `display: block` para los enlaces.

### Ejercicio 23: Galería de Imágenes
Crea una galería de imágenes con bloques `gallery` y elementos `gallery__item`. Usa `display: inline-block` para los elementos de la galería y ajusta el modelo de caja para espaciar las imágenes.

### Ejercicio 24: Cabecera Fija
Crea una cabecera fija utilizando `position: fixed` para el bloque `header`. Asegúrate de que la cabecera se mantenga en la parte superior de la ventana al hacer scroll.

### Ejercicio 25: Sidebar Sticky
Crea una barra lateral sticky utilizando `position: sticky` para el bloque `sidebar`. La barra lateral debe mantenerse en su posición cuando se hace scroll hasta cierto punto.

### Ejercicio 26: Diseño de Tarjetas con Flexbox
Utiliza Flexbox para crear un diseño de tarjetas. Crea un contenedor con clase `card-container` y varios elementos `card`. Aplica propiedades de Flexbox al contenedor para distribuir las tarjetas uniformemente.

### Ejercicio 27: Modales Superpuestos
Crea dos modales superpuestos utilizando `position: absolute` y `z-index`. Asegúrate de que uno de los modales se muestre encima del otro.

### Ejercicio 28: Footer Pegajoso
Crea un footer pegajoso utilizando `position: fixed` para el bloque `footer`. El footer debe permanecer en la parte inferior de la ventana del navegador.

### Ejercicio 29: Layout de Artículo
Crea un layout de artículo con un bloque `article`, un elemento `article__header`, `article__content`, y `article__footer`. Usa la metodología BEM y aplica estilos para espaciar y alinear correctamente el contenido.

### Ejercicio 30: Página Completa
Combina todos los conceptos aprendidos para crear una página completa con un header fijo, un sidebar sticky, un layout de contenido principal, y un footer. Usa BEM para nombrar las clases y aplica las propiedades de CSS adecuadas para el layout y estilo.


## [Autor: Alejandro Di Stefano](https://github.com/Drako01)