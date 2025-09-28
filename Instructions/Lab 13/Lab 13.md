**Laboratorio 13: Escribir una GitHub JavaScript Action y automatizar
tareas personalizadas exclusivas de su flujo de trabajo**

Objetivos:

Imagine que se le asigna la tarea de crear una GitHub Action
personalizada para automatizar tareas específicas dentro de su flujo de
trabajo. Para comenzar, necesita configurar un entorno de desarrollo
para escribir y probar su JavaScript Action. Esto implica inicializar un
nuevo proyecto de JavaScript, configurar la estructura del proyecto e
instalar las dependencias necesarias. Al seguir los pasos de este
laboratorio, creará una base sólida para desarrollar su GitHub Action,
lo que le permitirá crear automatizaciones adaptadas a las necesidades
de su proyecto.

En este laboratorio práctico, usted:

- Clonará el repositorio: Clone el repositorio proporcionado en su
  equipo local para iniciar el proceso de desarrollo.

- Navegará a la carpeta del proyecto: Desplácese a la carpeta del
  repositorio clonado donde configurará su acción.

- Creará la carpeta de la Action: Configure una carpeta nueva dentro del
  repositorio específicamente para los archivos de su GitHub JavaScript
  Action.

- Inicializará el proyecto npm: Inicialice un nuevo proyecto npm en la
  carpeta de la acción para administrar dependencias y configuración.

- Instalará dependencias: Use npm para instalar las dependencias
  necesarias para desarrollar su GitHub JavaScript Action.

- Preparará el entorno para el desarrollo de la Action: Configure el
  entorno de su proyecto para empezar a escribir y probar su GitHub
  JavaScript Action.

Ejercicio 1: Crear un nuevo repositorio

1.  Vaya al siguiente
    enlace: https://github.com/skills/write-javascript-actions

En este laboratorio creará el repositorio utilizando una plantilla
pública **skills-write-javascript-actions**

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image1.jpeg)

2.  Seleccione **Create a new repository** en el menú **Use this
    template**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image2.jpeg)

3.  Ingrese los siguientes detalles y seleccione **Create Repository**.

    - Repository name: **skills-write-javascript-actions**

    - Repository type: **Public**

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image3.jpeg)

Ejercicio \#2: Inicializar un nuevo proyecto de JavaScript

Una vez que tenga instaladas las herramientas necesarias en su máquina
local, siga estos pasos para comenzar a crear su primera acción.

1.  En la página principal del repositorio **write-javascript-actions**,
    haga clic en el botón **Code** (el de color verde) y copie la URL
    HTTPS que aparece en la pestaña **Local**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image4.jpeg)

2.  Abra la ventana **Command prompt** y clone su repositorio skills en
    la máquina local:

git clone \<this repository URL\>.git

![A screenshot of a computer program AI-generated content may be
incorrect.](./media/image5.jpeg)

**Nota:** Por lo general, el repositorio se clona en la siguiente ruta
"**C:\Users\Admin\skills-write-javascript-actions**"

3.  Navegue a la carpeta que acaba de clonar:

cd C:\Users\Admin\skills-write-javascript-actions

![A screenshot of a computer program AI-generated content may be
incorrect.](./media/image6.jpeg)

4.  Estaremos usando la rama llamada main.

git switch main

![A screenshot of a computer program AI-generated content may be
incorrect.](./media/image7.jpeg)

5.  Estaremos creando una nueva carpeta para nuestros archivos de
    acciones:

mkdir -p .github\actions\joke-action

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image8.jpeg)

6.  Navegue a la carpeta joke-action que acaba de crear:

cd .github/actions/joke-action

![A screenshot of a computer program AI-generated content may be
incorrect.](./media/image9.jpeg)

7.  Inicialice un nuevo proyecto:

npm init -y

![A screenshot of a computer program AI-generated content may be
incorrect.](./media/image10.jpeg)

8.  Instale las dependencias, request, request-promise y \\actions/core
    usando npm desde el GitHub ToolKit
    (https://github.com/actions/toolkit):

Npm install -save request request-promise @actions/core

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image11.jpeg)

9.  Haga commit de esos archivos recién agregados. Más adelante
    eliminaremos la necesidad de subir la carpeta node_modules:

git add . && git commit -m "add project dependencies"

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image12.jpeg)

**Nota:** Si se le solicita ingresar el correo electrónico de usuario y
el nombre de usuario, ingrese el siguiente comando reemplazando los
detalles.

![A screen shot of a computer AI-generated content may be
incorrect.](./media/image13.jpeg)

git config --global user.email "your_email@example.com"

git config --global user.name "Your Name"

**Nota**: Reemplace con sus detalles.

10. Publique sus cambios en el repositorio: ingrese el siguiente comando
    y luego inicie sesión

git push

![A computer screen with white text AI-generated content may be
incorrect.](./media/image14.jpeg)

**Nota:** cuando se le solicite la autorización, inicie sesión en su
cuenta de GitHub y continúe con el proceso.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image15.jpeg)

![A screenshot of a login form AI-generated content may be
incorrect.](./media/image16.jpeg)

![A screenshot of a computer error AI-generated content may be
incorrect.](./media/image17.jpeg)

11. Espere aproximadamente 20 segundos mientras GitHub Actions actualiza
    automáticamente la página para continuar con el procesamiento.

Resumen:

Ahora ha establecido un entorno de desarrollo sólido para crear y
administrar su GitHub JavaScript Action, sentando las bases para
automatizar y mejorar sus flujos de trabajo.
