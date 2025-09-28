**Laboratorio 05: Administrar lanzamientos de software con un flujo de
trabajo basado en versiones de GitHub**

Objetivo:

Imagine que forma parte de un equipo de desarrollo de software que
trabaja en un proyecto que requiere actualizaciones y lanzamientos
periódicos. Para gestionar su software de forma eficiente, decide
implementar un flujo de trabajo basado en versiones (release-based
workflow) usando GitHub. Este flujo de trabajo le ayuda a manejar el
control de versiones y a gestionar las iteraciones del software de
manera efectiva, asegurando que cada lanzamiento esté documentado y que
los problemas se aborden de forma controlada.

En este laboratorio práctico, usted:

- Creará un repositorio: Configurará un repositorio con el nombre
  skills-release-based-workflow que servirá como base para su flujo de
  trabajo basado en versiones.

- Implementará control de versiones: Explorará los conceptos de control
  de versions y la importancia de dar seguimiento a las iteraciones del
  software.

- Creará una versión beta: Seguirá los pasos para crear una versión beta
  de la base de código actual, incluyendo el etiquetado (*tagging*) y la
  publicación en GitHub.

- Simulará un escenario real: Introducirá un error en la base de código,
  simulando un escenario común de identificación y resolución de
  problemas dentro del flujo de trabajo de versiones.

Ejercicio \#1: Configurar un nuevo repositorio (como base para el flujo
de trabajo basado en versiones)

1.  Inicie sesión en su cuenta de GitHub.

2.  Navegue al siguiente
    enlace: https://github.com/skills/release-based-workflow

En este laboratorio, creará el repositorio utilizando una plantilla
pública "**skills-release-based-workflow**".

![](./media/image1.jpeg)

3.  Seleccione **Create a new repository** en el menú **Use this
    template**.

![](./media/image2.jpeg)

4.  Ingrese los siguientes detalles y seleccione **Create Repository**.

    - Repository name: **skills-release-based-workflow**

    - Repository type: **Public**

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image3.jpeg)

Ejercicio \#2: Crear una versión para la base de código actual

En este ejercicio, crearemos una release para este repositorio en
GitHub.

- Las GitHub Releases apuntan a un commit específico.

- Las Releases pueden incluir notas de la versión en archivos Markdown y
  binarios adjuntos.

Nota: antes de usar un flujo de trabajo basado en releases para una
release más grande, creemos una etiqueta (tag) y una release.

1.  Una vez creado el repositorio (en el Ejercicio \#1), navegue a
    **Releases** en la barra lateral derecha de la página y haga clic en
    **Create a new release.**

![](./media/image4.jpeg)

Sugerencia: Para llegar a esta página, seleccione la pestaña **Code** en
la parte superior de su repositorio. Luego, busque la sección
**Releases** en la barra lateral derecha.

1.  En la página **Releases/Tags**, escriba lo siguiente:

    - Mantenga **Target** como main

    - En el campo **Choose a Tag**, especifique un número.

En este caso, use v0.9 y seleccione **Create new tag v0.9 on publish**

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image5.jpeg)

2.  Asigne un título a la versión, como First beta release

**Nota:** También podría asignar una breve descripción a la versión.

![](./media/image6.jpeg)

3.  Desplácese hacia abajo en la página para seleccionar la casilla de
    verificación junto a **Set as a pre-release**, ya que representa una
    versión beta, y seleccione **Publish release**.

![A screenshot of a phone AI-generated content may be
incorrect.](./media/image7.jpeg)

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image8.jpeg)

Ejercicio \#3: Introducir un error (para corregir más adelante)

Para preparar el escenario para más adelante, ahora vamos a agregar un
error que corregiremos como parte del flujo de trabajo de versiones en
los siguientes pasos. Ya existe una rama llamada “update-text-colors” en
el repositorio (creado en el Ejercicio \#1), así que vamos a crear y
combinar una pull request con esta rama. ✅.

1.  En la barra de navegación principal, seleccione la pestaña **Pull
    requests**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image9.jpeg)

2.  En la página siguiente, haga clic en **New pull request**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image10.jpeg)

3.  En la página **Compare changes**, seleccione lo siguiente y haga
    clic en **Create pull request,**

    - base: **release-v1.0** y

    - compare: **update-text-colors**.

![](./media/image11.jpeg)

4.  En la página **Open a pull request**, ingrese lo siguiente y luego
    haga clic en **Create pull request**.

    - Agregue un título: Configure el título del pull request como
      **Updated game text style**

    - Agregue una descripción: ## Description: Updated game text color
      to green

![](./media/image12.jpeg)

5.  En la página **Updated game text style \#1**, haga clic en **Merge
    pull request**, y luego confirme con **Confirm page.**

![](./media/image13.jpeg)

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image14.jpeg)

6.  En la página siguiente, elimine la rama recién creada seleccionando
    el botón **Delete branch**.

![](./media/image15.jpeg)

7.  Espere aproximadamente 20 segundos mientras GitHub Actions actualiza
    automáticamente la página.

![](./media/image16.jpeg)

**Resumen:**

Ahora ha adquirido experiencia práctica en el establecimiento y la
administración de un flujo de trabajo basado en releases, lo que mejora
su capacidad para realizar un seguimiento de versiones, manejar releases
y resolver errores de manera eficiente.
