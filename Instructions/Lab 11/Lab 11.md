**Laboratorio 11: Hacer reutilizable un workflow y usar una estrategia
de matriz para ejecutar múltiples versiones de Node.js**

Objetivo:

Imagine que está administrando múltiples repositorios dentro de un
proyecto que comparten flujos de trabajo comunes para tareas como
compilación, pruebas e implementación. Para evitar redundancia y
mantener la consistencia en todos los repositorios, usted decide
implementar flujos de trabajo reutilizables con GitHub Actions. Al
aprovechar el desencadenante workflow_call, puede centralizar la
configuración de sus workflows, asegurando que los cambios se realicen
en un solo lugar y se apliquen automáticamente en todos los repositorios
relevantes. Además, utilizará estrategias de matriz (matrix strategies)
para probar sus flujos de trabajo con múltiples versiones de Node.js,
mejorando la compatibilidad y la escalabilidad de sus proyectos.

En este laboratorio práctico, usted:

- Usará el desencadenante workflow_call para que los workflows sean
  reutilizables en varios repositorios, reduciendo la redundancia en la
  configuración.

- Navegará a su repositorio, actualizará el archivo de workflow para
  incluir el desencadenante workflow_call y confirmará los cambios.

- Creará una pull request para comparar los cambios y las excepciones.

Ejercicio \#1: Crear un nuevo repositorio.

1.  Vaya al siguiente
    enlace: https://github.com/skills/reusable-workflows

En este laboratorio, usted creará el repositorio utilizando una
plantilla pública "**skills-reusable-workflows**".

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image1.jpeg)

2.  Seleccione **Create a new repository** en el menú **Use this
    template**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image2.jpeg)

3.  Ingrese los siguientes detalles y seleccione **Create Repository**.

    - Repository name: **skills-reusable-workflows**

    - Repository type: **Public**

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image3.jpeg)

Ejercicio \#2: Agregar un desencadenante workflow_call a un flujo de
trabajo

1.  En la página principal del repositorio recién creado, navegue a la
    pestaña **Code**\*\*.\*\*

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image4.jpeg)

2.  En el menú desplegable de la rama main, seleccione la rama
    **reusable-workflow**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image5.jpeg)

3.  Después de cambiar la rama, navegue a la carpeta
    **.github/workflows/** y seleccione el archivo
    **reusable-workflow\\yml**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image6.jpeg)

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image7.jpeg)

4.  En el editor del archivo **reusable-workflow\\yml**, seleccione
    **Edit in place**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image8.jpeg)

5.  Reemplace el desencadenante **workflow_dispatch** con el
    desencadenante del evento **workflow_call** y seleccione **Commit
    changes**.

**Nota**: Reemplace el bloque de código desde la **Línea \#3** hasta la
**Línea \#8** con el siguiente

on:

workflow_call:

inputs:

node:

required: true

type: string

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image9.jpeg)

6.  En la ventana **Commit changes**, seleccione **Commit changes**.

![A screenshot of a screenshot of a new branch AI-generated content may
be incorrect.](./media/image10.jpeg)

Ejercicio \#3: Crear una pull request para ver los cambios realizados en
el ejercicio anterior

1.  Seleccione la pestaña **Pull requests**, y luego haga clic en **New
    pull request**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image11.jpeg)

2.  En la página **Comparing changes**, configure **base: main** y
    **compare: reusable-workflow.**

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image12.jpeg)

3.  En la página **Open a pull request**, haga clic en **Create pull
    request.**

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image13.jpeg)

4.  Espere 20 segundos para que las actions se ejecuten y luego revise
    los resultados.

Resumen:

Ahora usted ha adquirido experiencia práctica en la creación de
workflows eficientes y reutilizables, así como en su optimización para
diversos entornos utilizando GitHub Actions.
