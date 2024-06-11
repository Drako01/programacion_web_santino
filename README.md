# Cómo configurar Git y GitHub en Mac

En la configuración de Git y Github vamos a ver los pasos desde su instalación y configuración con nuestra pc, hasta cómo actualizar un repositorio local. Si tienes dudas, puedes dejarlas en los comentarios y estaré en breve contigo!

### Cómo instalar Git en Mac
Por defecto, Git no está instalado en nuestro Mac y para instalarlo vamos a necesitar la terminal. Abre la terminar y escribe el siguiente comando y oprime enter:

```
git --version
```

Inmediatamente verás un aviso el cual dirá que tu Mac necesita unos comandos adicionales para poder procesarlo. Aquí debes aceptar su instalación.

Una vez terminada la instalación, vuelve a escribir el comando anterior y tendrás que ver como respuesta, el número de la versión actual de Git.






### Configurar GitHub en Mac

Configurar GitHub en Mac
Para este paso, en la configuración de Git y Github debemos crear primero una cuenta en Github. Haz click en el enlace y crea una cuenta. Los datos que solicitarán son como cualquier cuenta de red social, pero aquí hay un punto importante: el usuario.

El usuario de Github es demasiado importante porque con este se alojarán prácticamente todos los repositorios que vamos a crear. Te recomiendo que lo crees y no lo modifiques en el tiempo.

Una vez esté creada la cuenta, vamos a la terminal y vamos a escribir estos comandos:
```
git config --global user.name ""
```
Entre comillas, escribe tu usuario de GitHub y oprime enter. luego, escribe el siguiente comando:
```
git config --global user.mail ""
```
Entre comillas escribe el correo de tu cuenta de GitHub y oprime enter. Una vez termines este proceso, vamos a verificar que quedo correctamente configurado con el siguiente comando:
```
git config --list
```
Aquí verás tu usuario y correo en la terminal. Esto nos confirmará que la instalación y configuración estuvo bien hecha.

### Instalar y configurar Visual Studio Code con GitHub
Ahora, en uno de los pasos más importantes de Git y Github es la selección e instalación del editor de código. Hay varios editores de código, pero por el momento te voy a recomendar el que utilizo y es Visual Studio Code 
Una vez esté instalado, vamos a abrirlo y en la parte inferior izquierda vamos a ver el ícono de usuario en la barra lateral. Ahora, sigue estos pasos:

* Haz click en el ícono de usuario y luego selecciona «entrar y sincronizar».
* Se abrirá una opción en la barra centrar con dos opciones. Selecciona «entrar con GitHub».
* Esto te llevará a GitHub y deberás aceptar la conexión.
* Vuelve a VSCode y haz click en Open, en la ventana emergente.

Listo! hemos configurado la cuenta de gitHub en nuestro VSCode.

### Crear y clonar repositorio

Este paso será un poco complicado pero lo haré lo más explicativo posible. Lo primero será entrar a nuestra cuenta de GitHub y en la parte superior derecha, haz click en el «+», luego «nuevo repositorio».

En el formulario de creación:

* Añade un nombre para el repositorio.
* Selecciona la privacidad. Puedes dejarla pública.
* Añade un archivo readme al repositorio.
* Haz click en Crear repositorio.

Listo! ya hemos creado el repositorio, ahora viene el paso complicado, vamos a clonarlo. Antes de continuar haz click en CODE > COPIA LA URL DEL REPOSITORIO.

### Clonar repo en Mac

Este repositorio local nos permitirá trabajar en nuestro proyecto desde nuestro pc y al mismo tiempoa actualizarlo, lo cual veremos en el siguiente paso. Ahora, el repositorio se descargará como una carpeta en tu mac así que debemos seleccionar la ubicación.

Esta ubicación no se debe modificar con el tiempo, o deberás hacer cambios adicionales en la configuración y clonación. Así que entra a finder y busca una carpeta donde quieras guardar el repositorio.

Una vez la tengas vamos a encontrar esta ubicación desde la terminal. Para encontrar esta ruta, vamos a usar dos comandos: ls y cd. Ls nos permitirá ver el contenido de la ubicación o carpeta actual. Cd nos permitirá movernos de carpeta en carpeta. Vamos a comenzar:

* Al abrir terminal verás el signo $. El texto anterior será LA UBICACIÓN ACTUAL en la terminal. En mi caso, aparece eduardoarias, el cual es el nombre de mi usuario en mac.
Ahora debemos comenzar a movernos hasta encontrar la ubicación que escogimos para guardar el repo.
* Escribe ls y luego ENTER. Verás el contenido de la ubicación actual. Por ejemplo, verás las carpetas del usuario principal de tu mac como: documentos, librería, descargas y más.
* Escribe cd junto con el nombre EXACTO de la carpeta siguiente a la ubicación que escogiste. Por ejemplo, si lo quieres guardar en el escritorio, entonces escribe: cd Escritorio y luego enter.
* Ahora verás que la terminal cambió: antes del signo $ verás otro texto que indica la ubicación actual de la terminal. De esta forma nos moveremos carpeta por carpeta en nuestra mac, usando estos comandos.

Una vez encontremos la carpeta que contendrá el repositorio (lo sabrás porque dirá el nombre de la carpeta contenedora antes del signo $), vamos a escribir el siguiente comando:


```
git clone urldelrepositorio
```
reemplaza urldelrepositorio por la url que nos da GitHub. Esta URL fue la que copiamos en el paso anterior en la creación del repo.

Oprime enter y listo! verás que se creó la carpeta automáticamente en tu Mac, con el repo de GitHub.

### Actualizar repositorio en GitHub desde Mac
Ahora, como paso final en la configuración de Git y GitHub será la actualización de versión del repo desde nuestro Mac. Es prácticamente lo que haremos todas las veces que trabajemos.

Abre Visual Studio code y arrastra la carpeta del repo para abrirlo en VSCode. Una vez esté abierto verás en la parte izquierda, dentro del repo el archivo readme que se creó al momento de crear el repositorio. Esto dará confirmación a que hicimos todo correctamente!

### Modificar repositorio local

Como paso siguiente debemos modificar algo para poder ver cómo se actualiza el repositorio local. En la parte izquierda arriba del nombre del repositorio verás un ícono con un «+», haz click y crea un nuevo archivo (file).

Dale un nombre sin problema y luego en el editor de código, añade otro texto adicional.

### Subir repositorio

Por último, debemos subir esta actualización a GitHub. Para esto en el menú superior de visual Studio, haz click en filee > save. Esto guardará los cambios que hicimos dentro de nuestro pc. Ahora, en el mismo menú haz click en terminal > new terminal.

Una vez abierta la terminal desde VSCode, vamos a escribir los siguientes comandos y oprimimos enter luego de escribir cada uno:.

```
git status
```
esto nos permitirá ver el estado del repositorio. Debe salir el nombre del archivo que creamos en rojo. Lo cual indica que se hizo un cambio que aún no se ha subido GitHub.

```
git add nombredelarchivo
```

A continuación, reemplaza nombredelarchivo por el nombre que aparece en rojo. Te recomiendo autocompletar siempre los nombres con LA TECLA TAB. Si por ejemplo, el archivo se llama «mi archivo», son dos palabras en el nombre, escribe: mi y oprime inmediatamente TAB. Esto autocompletará el nombre para evitar errores.

Si deseas confirmar que se subió correctamente, puedes volver a escribir git status y ahora debes ver el nombre del archivo en verde.

```
git commit -m 'comentariodelrepo'
```

Este comando nos permitirá darle una etiqueta o comentario a la actualización que acabamos de hacer en el repositorio. Reemplaza comentariodelrepo con un comentario cualquiera como: mi primer archivo creado.

```
git push
```
Este es el paso final, nos permitirá subir el archivo a GitHub. Al oprimir enter saldrá un aviso para autorizar a vscode junto con GitHub de subir la actualización:

* En la ventana emergente: The extension GitHub wants to sign in using GitHub, haz click en «allow».
* Esto te llevará a GitHub. Haz click en «continuar».
* Vuelve a VSCode y haz click en Open.

Aquí verás que se añade un código como respuesta a la terminal. Ahora para confirmar que la actualización fue correcta, puedes ir a tu cuenta de GitHub desde el navegador que desees y en el repositorio debes ver una carpeta adicional junto con el comentario que asignaste.

Listo! hemos terminado completamente.

[Click para ver el Video](https://www.youtube.com/watch?v=tH15EPkRc3w)



-----

# Incluyendo CSS a nuestro proyecto - Clase 02

#### Objetivos de la clase:
- Comprender la sintaxis de CSS.
- Incluir CSS en nuestro Proyecto.
- Conocer el uso de medidas, colores, fuentes y fondos en CSS.

---

### Glosario

**Listas:** HTML permite agrupar elementos que tienen más significado de forma conjunta. Aunque cada palabra por separado tiene sentido, de forma conjunta constituyen el menú de navegación de la página, por lo que su significado conjunto es mayor que por separado. Esto se denomina listas.

**Tablas:** Son un conjunto de celdas organizadas, dentro del cual es posible alojar distintos contenidos. Sirven para representar información tabulada, en filas y columnas.

**Formularios:** Son etiquetas donde el usuario ingresará o seleccionará valores, que serán enviados a un archivo encargado de procesar la información.

**Enlaces:** También conocidos como links o anchors, se utilizan para relacionar partes del mismo documento. Por defecto, se visualizan azules y subrayados.

---

### Mapa de Conceptos

- Atributos
- Bases de CSS
- Propiedades
- Class
- Reglas sintácticas
- Sintaxis de CSS
- Padres e hijos
- ¿Qué es CSS?
- ID

---

### Temario

1. Primeros pasos con HTML
2. Incluyendo CSS a nuestro proyecto
3. CSS + Box Modeling

---

### Bases de CSS

**CSS (Cascading Style Sheets):** Es un lenguaje web para aplicar formato visual (color, tamaño, separación y ubicación) al HTML. Permite cambiar por completo el aspecto de cualquier etiqueta HTML.

---

### Sintaxis de CSS

```css
selector {
   propiedad1: valor;
   propiedad2: valor;
}

h1 {
   color: red;
}
```

**Reglas sintácticas:**
1. Cada declaración CSS está formada por un juego de pares propiedad:valor.
2. No se ve afectado por el espacio en blanco. Las propiedades se pueden escribir de corrido o una debajo de la otra.
3. Siempre que la propiedad represente un número, el valor debe indicar en qué unidad se expresa.

---

### Padres e Hijos

Cuando tienes una etiqueta "dentro" de otra, aplicas el concepto de padres e hijos. Esto permite agregar atributos específicos a “hijos” sin alterar los del “padre”. 

```html
<section>
    <article> 
        <h2>Título</h2>
        <p>Lorem ipsum dolor sit amet...</p>
    </article>
</section>
```

---

### Insertar CSS en el HTML

**Forma externa:**
```html
<link rel="stylesheet" href="archivo.css" />
```

**Forma interna:**
```html
<style>
    /* comentario de CSS dentro de esta etiqueta va el código CSS */
</style>
```

**Forma inline (no recomendable):**
```html
<h2 style="color: red;">H2 con formato CSS</h2>
```

---

### Class

**Desde CSS:**
```css
.bordesRedondeados {
  /* código CSS */
}
```

**En HTML:**
```html
<img src="" class="bordesRedondeados" />
```

Puedes aplicar más de una clase a cada etiqueta separada por un espacio:
```html
<img src="" class="bordesRedondeados imgChica"/>
```

---

### Atributo ID

**Desde CSS:**
```css
#productos {
  /* código CSS */
}
```

**En HTML:**
```html
<section id="productos"></section>
```

### Class vs ID

- **ID:** Nombrar secciones, divisiones de código (único por documento).
- **Class:** Especificar diseño aparte del código (puede repetirse).

```html
<section id="prod">
  <article class="rojo"></article>
  <article class="rojo"></article>
</section>
```

---

### Herencia y Cascada

**Herencia:** Los elementos hijos heredan propiedades del elemento padre, a menos que tengan estilos específicos aplicados.

```css
div {
   color: red;
}

<div>
   <p>Este párrafo quedará en rojo por herencia</p>
</div>
```

**Cascada:** El navegador lee de arriba hacia abajo. La última declaración prevalece.

```css
p {
   color: red;
}

p {
   color: green;
}
```

### Precedencia de Declaraciones

1. **ID:** Pisan cualquier otra regla.
2. **Class:** Sobreescriben las reglas de etiqueta pero no las de ID.
3. **Etiquetas:** Tienen la menor precedencia.

```css
ID > Class > Etiquetas
```

---

### Estilos Inline

Los estilos inline sobrescriben cualquier estilo de las páginas externas de CSS y tienen la mayor especificidad.

```html
<p style="color: red">Párrafo rojo</p>
```

---

### Importancia de los Selectores

- Estilo aplicado a la Etiqueta.
- Estilo aplicado a la Class.
- Estilo aplicado al ID.
- Estilo aplicado Inline.

### !important

La declaración `!important` corta la precedencia. Se escribe después del valor de la propiedad CSS que se quiere convertir en la más importante. Se recomienda no abusar de esta práctica.

```css
color: red !important;
```

### Reset CSS

Los reset CSS unifican estilos entre diferentes navegadores.

```css
* {
   margin: 0;
   padding: 0;
}
```

### Primeras Propiedades

**Propiedad: color**
Mediante esta propiedad se puede agregar color a los textos del sitio.

Valores comunes:
- Nombre del color (ej: red).
- Hexadecimal (ej: #ffffff).
- RGB (ej: rgb(50, 212, 227)).

### Estilos de Texto

**FONT-STYLE:**

```css
.normal {
   font-style: normal;
}

.italica {
   font-style: italic;
}
```

**FONT-WEIGHT:**

```css
.normal {
   font-weight: normal;
}

.negrita {
   font-weight: bold;
}
```

---


