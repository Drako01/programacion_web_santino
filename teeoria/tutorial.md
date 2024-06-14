# Tutorial Completo de Git y GitHub

<p align="center">
	<img src="https://user-images.githubusercontent.com/25181517/192108372-f71d70ac-7ae6-4c0d-8395-51d8870c2ef0.png" alt="Git" width=160/>
	<img src="https://techcrunch.com/wp-content/uploads/2010/07/github-logo.png" alt="Git" width=160/>
</p>

---

## Introducción a Git

Git es un sistema de control de versiones distribuido que permite a múltiples personas trabajar en un proyecto simultáneamente sin sobrescribir los cambios de los demás. Git almacena instantáneas de tus archivos en el tiempo, permitiendo recuperar versiones anteriores y colaborar de manera eficiente.

### Instalación

Antes de comenzar, asegúrate de tener Git instalado en tu sistema. Puedes descargarlo desde [git-scm.com](https://git-scm.com/).

Para verificar que Git está instalado, abre una terminal y escribe:

```bash
git --version
```

## Configuración Inicial

Configura tu nombre de usuario y correo electrónico, que serán usados en tus commits:

```bash
git config --global user.name "Tu Nombre"
git config --global user.email "tuemail@example.com"
```

## Creación de un Repositorio

Para empezar a usar Git, primero debes crear un repositorio:

```bash
mkdir mi_proyecto
cd mi_proyecto
git init
```

## Añadir y Commitear Archivos

Añade un archivo al repositorio y haz un commit:

```bash
echo "Hola Mundo" > archivo.txt
git add archivo.txt
git commit -m "Añadir archivo.txt con Hola Mundo"
```

## Estado del Repositorio

Para ver el estado de tu repositorio, usa:

```bash
git status
```

## Historial de Commits

Para ver el historial de commits:

```bash
git log
```

## Ramas en Git

Las ramas te permiten trabajar en diferentes partes de un proyecto de manera aislada. Para crear y cambiar a una nueva rama:

```bash
git branch nueva_rama
git checkout nueva_rama
```

Para fusionar una rama en la rama principal:

```bash
git checkout main
git merge nueva_rama
```

## Repositorios Remotos

Para trabajar con repositorios remotos como GitHub:

### Conectar a un Repositorio Remoto

Primero, crea un repositorio en GitHub y copia la URL. Luego, conecta tu repositorio local al remoto:

```bash
git remote add origin https://github.com/tu_usuario/tu_repositorio.git
```

### Enviar Cambios al Repositorio Remoto

Para enviar (push) tus cambios al repositorio remoto:

```bash
git push origin main
```

### Obtener Cambios del Repositorio Remoto

Para obtener (pull) cambios desde el repositorio remoto:

```bash
git pull origin main
```

## Trabajar con Forks y Pull Requests

### Crear un Fork

Un fork es una copia de un repositorio que te permite experimentar con cambios sin afectar el proyecto original. Puedes hacer un fork desde la interfaz de GitHub.

### Clonar un Fork

Para clonar un fork a tu máquina local:

```bash
git clone https://github.com/tu_usuario/tu_fork.git
cd tu_fork
```

### Enviar Cambios a tu Fork

Después de hacer cambios en tu fork, envíalos a GitHub:

```bash
git add .
git commit -m "Descripción de los cambios"
git push origin main
```

### Crear un Pull Request

Para proponer cambios al proyecto original, abre un pull request desde la interfaz de GitHub. Esto le permite al propietario del repositorio original revisar y aceptar tus cambios.

## Comandos Adicionales Útiles

### Ver Diferencias

Para ver las diferencias entre tu archivo modificado y el último commit:

```bash
git diff
```

### Guardar Cambios Temporalmente

Para guardar cambios no commitados temporalmente:

```bash
git stash
```

Para recuperar esos cambios:

```bash
git stash pop
```

### Resetear Cambios

Para deshacer cambios en el historial de commits:

```bash
git reset --hard HEAD~1
```

### Crear Tags

Para crear un tag en un commit específico:

```bash
git tag -a v1.0 -m "Versión 1.0"
```

Para enviar tags al repositorio remoto:

```bash
git push origin --tags
```

## Gestión de Conflictos

### Resolver Conflictos de Fusión

Al fusionar ramas, pueden ocurrir conflictos si los mismos archivos han sido modificados de maneras diferentes. Git te notificará de los conflictos, que deben ser resueltos manualmente:

1. Abre los archivos conflictivos y busca las secciones marcadas con `<<<<<<<`, `=======`, y `>>>>>>>`.
2. Edita el archivo para resolver el conflicto.
3. Añade y commitea los cambios:

```bash
git add archivo_conflictivo.txt
git commit -m "Resolver conflicto de fusión en archivo_conflictivo.txt"
```

## Rebase

### Usar Rebase para Reordenar Commits

El rebase permite cambiar la base de una rama, aplicando sus commits sobre otra base:

```bash
git checkout nueva_rama
git rebase main
```

### Rebase Interactivo

Para reordenar, editar o combinar commits:

```bash
git rebase -i HEAD~n
```

Donde `n` es el número de commits a incluir en el rebase interactivo.

## Cherry-Pick

### Aplicar Commits Específicos a Otra Rama

Para aplicar un commit específico a otra rama:

```bash
git cherry-pick <commit_hash>
```

## Stash

### Usar Stash para Guardar Cambios Temporalmente

Para guardar cambios no commitados:

```bash
git stash
```

Para recuperar esos cambios:

```bash
git stash pop
```

## Submódulos

### Añadir Submódulos

Para incluir repositorios dentro de otros repositorios:

```bash
git submodule add <URL_del_submodulo>
git submodule init
git submodule update
```

## GitHub Pages

### Configurar GitHub Pages

GitHub Pages te permite alojar una página web estática directamente desde un repositorio en GitHub:

1. Crea un repositorio llamado `<usuario>.github.io`.
2. Añade archivos HTML, CSS y JS a este repositorio.
3. En la configuración del repositorio, habilita GitHub Pages desde la rama `main` o una carpeta específica.

## SSH y Seguridad

### Configurar Claves SSH

Para configurar y usar claves SSH para autenticación con GitHub:

1. Genera una nueva clave SSH:

```bash
ssh-keygen -t rsa -b 4096 -C "tuemail@example.com"
```

2. Añade la clave SSH a tu agente SSH:

```bash
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_rsa
```

3. Añade la clave SSH a tu cuenta de GitHub desde la configuración de SSH y GPG keys.

## Blame

### Usar Blame para Ver Cambios en una Línea Específica

Para ver quién hizo cambios en una línea específica de un archivo:

```bash
git blame <archivo>
```

## Búsqueda en Commits

### Buscar en el Historial de Commits

Para buscar en el historial de commits:

```bash
git log --grep="término de búsqueda"
```

## Ejemplos Prácticos

### Clonar y Contribuir a un Proyecto Open Source

1. Encuentra un proyecto en GitHub que te interese.
2. Haz un fork del proyecto.
3. Clona el fork a tu máquina local:

```bash
git clone https://github.com/tu_usuario/proyecto_forkeado.git
cd proyecto_forkeado
```

4. Crea una nueva rama para tu contribución:

```bash
git checkout -b mi_contribucion
```

5. Realiza los cambios y haz commits:

```bash
git add .
git commit -m "Añadir nueva funcionalidad"
```

6. Envía los cambios a tu fork en GitHub:

```bash
git push origin mi_contribucion
```

7. Abre un pull request desde la interfaz de GitHub para proponer tus cambios al proyecto original.

## Recursos Adicionales

Para profundizar más en Git, puedes consultar los siguientes recursos:
- [Pro Git Book](https://git-scm.com/book/en/v2)
- [GitHub Learning Lab](https://lab.github.com/)
- [Atlassian Git Tutorials](https://www.atlassian.com/git/tutorials)


---

## [Autor: Alejandro Di Stefano](https://github.com/Drako01)