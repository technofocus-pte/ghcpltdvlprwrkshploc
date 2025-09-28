**Laboratorio 04: Revisar solicitudes de incorporación de cambios y
resolver conflictos de combinación**

Objetivo:

Imagine que forma parte de un equipo de desarrollo que trabaja en un
proyecto con múltiples colaboradores. A medida que se realizan cambios,
es crucial revisarlos y asegurarse de que el trabajo de todos se integre
sin problemas. Debe colaborar de manera efectiva gestionando pull
requests y resolviendo conflictos de combinación para mantener la
integridad del proyecto y evitar interrupciones.

En este laboratorio práctico, se enfocará en dos aspectos clave de la
colaboración en GitHub:

- Crear una solicitud de extracción (Pull Request): Seleccione las ramas
  correspondientes, proporcione un título y una descripción, y envíe la
  solicitud de extracción para proponer cambios.

- Revisar solicitudes de extracción (Pull Requests): Examine los cambios
  propuestos en las solicitudes de extracción, asegurándose de que
  cumplan con los estándares del proyecto y estén listos para su
  integración.

- Resolver conflictos de combinación (Merge Conflicts): Practique la
  resolución de conflictos que surgen cuando los cambios en diferentes
  ramas afectan las mismas partes de un archivo, garantizando una
  integración y colaboración fluidas.

Ejercicio n.º 1: Crear un repositorio a partir de una plantilla y crear
una Pull Request

La pull request mostrará los cambios en su rama a otras personas. Esta
pull request mantendrá los cambios que acaba de realizar en su rama y
propondrá aplicarlos a la rama principal.

1.  Inicie sesión en su cuenta de GitHub.

2.  Navegue al siguiente
    enlace: https://github.com/skills/review-pull-requests

En este laboratorio, creará el repositorio utilizando una plantilla
pública "**skills-review-pull-requests**".

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image1.jpeg)

3.  Seleccione **Create a new repository** en el menú **Use this
    template**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image2.jpeg)

4.  Ingrese los siguientes detalles y seleccione **Create Repository**.

    - Repository name: **skills-review-pull-requests**

    - Repository type: **Public**

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image3.jpeg)

5.  En la página principal de navegación, seleccione la pestaña **Pull
    requests**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image4.jpeg)

6.  En la página siguiente, seleccione **New pull request.**

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image5.jpeg)

7.  En la página **Compare changes**:

    - En la lista desplegable **base:**, seleccione **main** (de forma
      predeterminada, esta opción ya está seleccionada)

    - En la lista desplegable **compare:**, seleccione **update-game**,

Por lo general, es necesario esperar unos segundos y actualizar la
página para visualizar las ramas.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image6.jpeg)

![A screenshot of a phone AI-generated content may be
incorrect.](./media/image7.jpeg)

8.  Una vez que seleccione **update-game** en el menú desplegable
    **compare:**, se abrirá la ventana **Comparing changes**. Haga clic
    en el botón **Create pull request**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image8.jpeg)

9.  En la página **Open a pull request**, ingrese lo siguiente:

    - **Agregue un título** para su pull request: Update the game over
      message

    - **Agregue una descripción** para su pull request: Update the game
      over message so people know how to play again.

10. Haga clic en **Create pull request**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image9.jpeg)

11. Espere aproximadamente 20 segundos y luego actualice esta página.
    GitHub Actions se actualizará automáticamente al siguiente paso.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image10.jpeg)

Ejercicio n.º 2: Actualizar una solicitud de incorporación de cambios
(Pull Request) y resolver conflictos de combinación (Merge Conflicts)

1.  Navegue al siguiente
    enlace: https://github.com/skills/resolve-merge-conflicts

En este laboratorio, creará el repositorio utilizando una plantilla
pública "**skills-resolve-merge-conflicts**".

![A screenshot of a web page AI-generated content may be
incorrect.](./media/image11.jpeg)

2.  Seleccione la opción **Create a new repository** en el menú **Use
    this template**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image12.jpeg)

3.  Ingrese los siguientes detalles y seleccione **Create Repository**.

    - Repository name: **skills-resolve-merge-conflicts**

    - Repository type: **Public**

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image13.jpeg)

4.  Una vez que el repositorio se haya creado, seleccione la pestaña
    **Pull requests** en la barra de navegación principal.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image14.jpeg)

5.  Haga clic en el botón **New pull request**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image15.jpeg)

6.  Cree una pull request seleccionando lo siguiente:

    - **my-resume** como la rama principal (head branch) y

    - **main** como la rama de comparación (compare branch).

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image16.jpeg)

![A screenshot of a chat AI-generated content may be
incorrect.](./media/image17.jpeg)

7.  Haga clic en el botón **Create pull request** 

8.  En la página **Open a pull request**, ingrese el título **Resolving
    merge conflicts** y haga clic en el botón **Create pull request.**

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image18.jpeg)

9.  Espere 20 segundos mientras GitHub Actions se actualiza
    automáticamente y la página muestra los detalles de los conflictos,
    si los hay.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image19.jpeg)

10. Haga clic en **Resolve conflicts** para continuar.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image20.jpeg)

11. Revise los conflictos y resuélvalos.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image21.jpeg)

12. En este ejercicio, elimine la línea en conflicto y haga clic en el
    botón **Mark as resolved**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image22.jpeg)

13. Haga clic en el botón **Commit merge** y verifique el mensaje de
    confirmación que aparece en pantalla.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image23.jpeg)

14. Haga clic en **I understand, continue updating main**. Verá los
    resultados finales de la verificación\*\*.\*\*

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image24.jpeg)

**Resumen:**

Ahora ha completado la creación y revisión de pull requests para
detectar conflictos y resolverlos, habilidades esenciales para un
trabajo en equipo efectivo y una gestión de proyectos exitosa en GitHub.
