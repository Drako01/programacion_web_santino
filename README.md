# ¡Creación de una página HTML usando buenas prácticas!


## Guía para Crear una Página HTML Usando Buenas Prácticas

## Introducción

Este documento tiene como objetivo guiarte a través del proceso de creación de una página HTML básica utilizando buenas prácticas. HTML (HyperText Markup Language) es el lenguaje estándar para crear páginas web y es fundamental para cualquier desarrollador web.

## Requisitos Previos

No se requieren conocimientos previos para seguir esta guía. Sin embargo, un editor de texto (como Visual Studio Code, Sublime Text o Atom) y un navegador web (como Google Chrome, Firefox o Safari) serán necesarios.

## Estructura Básica de un Documento HTML

Cada documento HTML debe seguir una estructura básica. Aquí tienes un ejemplo de la estructura mínima de una página HTML:

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mi Primera Página HTML</title>
</head>
<body>
    <header>
        <h1>Bienvenido a Mi Página</h1>
    </header>
    <main>
        <p>Este es un párrafo de ejemplo.</p>
    </main>
    <footer>
        <p>&copy; 2024 Mi Nombre</p>
    </footer>
</body>
</html>
```

### Descripción de la Estructura

1. `<!DOCTYPE html>`: Declara el tipo de documento como HTML5.
2. `<html lang="es">`: La etiqueta `<html>` envuelve todo el contenido de la página. El atributo `lang="es"` define el idioma de la página como español.
3. `<head>`: Contiene metadatos sobre el documento, como el juego de caracteres (`charset`) y el título (`title`) que se muestra en la pestaña del navegador.
4. `<meta charset="UTF-8">`: Define la codificación de caracteres como UTF-8.
5. `<meta name="viewport" content="width=device-width, initial-scale=1.0">`: Hace que el diseño sea adaptable a diferentes tamaños de pantalla.
6. `<title>`: Define el título de la página.
7. `<body>`: Contiene el contenido visible de la página.

## Buenas Prácticas

### 1. **Uso de Etiquetas Semánticas**

Utiliza etiquetas HTML semánticas como `<header>`, `<main>`, `<footer>`, `<article>`, y `<section>`. Estas etiquetas ayudan a mejorar la accesibilidad y el SEO de tu página.

### 2. **Organización del Código**

Mantén tu código limpio y organizado. Utiliza la indentación y espacios en blanco para mejorar la legibilidad. Aquí tienes un ejemplo de una buena práctica:

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ejemplo de Buenas Prácticas</title>
</head>
<body>
    <header>
        <h1>Encabezado Principal</h1>
    </header>
    <main>
        <section>
            <h2>Sección 1</h2>
            <p>Contenido de la primera sección.</p>
        </section>
        <section>
            <h2>Sección 2</h2>
            <p>Contenido de la segunda sección.</p>
        </section>
    </main>
    <footer>
        <p>&copy; 2024 Mi Nombre</p>
    </footer>
</body>
</html>
```

### 3. **Comentarios**

Utiliza comentarios para explicar secciones de tu código. Esto es útil para ti y para otros desarrolladores que puedan trabajar en tu código en el futuro.

```html
<!-- Esto es un comentario -->
```

### 4. **Accesibilidad**

Asegúrate de que tu página sea accesible para todos los usuarios, incluyendo aquellos con discapacidades. Utiliza atributos como `alt` en las imágenes y `aria` en elementos interactivos.

```html
<img src="imagen.jpg" alt="Descripción de la imagen">
```

### 5. **SEO (Optimización para Motores de Búsqueda)**

Incluye metaetiquetas relevantes y usa etiquetas de encabezado (`<h1>`, `<h2>`, etc.) de manera apropiada para mejorar el SEO de tu página.

```html
<meta name="description" content="Descripción de mi página web">
```

## Recursos Adicionales

- [Documentación de MDN Web Docs](https://developer.mozilla.org/es/docs/Web/HTML)
- [Curso de HTML en W3Schools](https://www.w3schools.com/html/)
- [Guía de Accesibilidad Web](https://www.w3.org/WAI/tips/developing/)

## Conclusión

Siguiendo esta guía, deberías ser capaz de crear una página HTML básica que siga buenas prácticas. Continúa explorando y aprendiendo más sobre HTML y otras tecnologías web para mejorar tus habilidades como desarrollador.

---

Autor: Alejandro Daniel Di Stefano

---



