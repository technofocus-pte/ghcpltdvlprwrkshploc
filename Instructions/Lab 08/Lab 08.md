**Laboratorio 08: Crear una GitHub Action y usarla en un flujo de
trabajo**

Objetivo:

Imagine que forma parte de un equipo de desarrollo que desea simplificar
su proceso de desarrollo de software automatizando tareas repetitivas.
Para mejorar la eficiencia, decide aprovechar GitHub Actions, que
permite automatizar tareas como pruebas, implementación y revisiones de
código directamente dentro de su repositorio de GitHub. Al configurar
una GitHub Action e integrarla en su flujo de trabajo, puede garantizar
que las tareas esenciales se ejecuten automáticamente, ahorrando tiempo
y reduciendo el esfuerzo manual.

En este laboratorio práctico, usted:

- Configurará un archivo de flujo de trabajo en el directorio
  .github/workflows, definirá el contenido y especificará los eventos
  que activan el flujo de trabajo.

- Practicará agregar y confirmar archivos de flujo de trabajo en su
  repositorio para integrar GitHub Actions en su proceso de desarrollo.

Ejercicio \#1: Crear un nuevo repositorio a partir de una plantilla
pública

1.  Navegue al siguiente
    enlace: https://github.com/skills/hello-github-actions

En este laboratorio creará el repositorio utilizando una plantilla
pública "**skills-hello-github-actions**".

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image1.jpeg)

2.  Seleccione **Create a new repository** en el menú **Use this
    template**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image1.jpeg)

3.  Ingrese los siguientes detalles y seleccione **Create Repository**.

    - Repository name: **skills-hello-github-actions**

    - Repository type: **Public**

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image2.jpeg)

Ejercicio \#2: Crear un archivo de flujo de trabajo

1.  En la página principal del repositorio recién creado, navegue a la
    pestaña **Pull requests**.

![A screenshot of a web page AI-generated content may be
incorrect.](./media/image3.jpeg)

2.  En la página siguiente, seleccione el botón **New pull request**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image4.jpeg)

3.  En la página **Compare changes**, seleccione **base: main** y
    **compare: welcome-workflow** y haga clic en **Create pull
    request.**

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image5.jpeg)

4.  En la página **Open a pull request**, haga clic en **Create pull
    request**.

![A screenshot of a email request AI-generated content may be
incorrect.](./media/image6.jpeg)

5.  Navegue a la pestaña **Code**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image7.jpeg)

6.  En la página siguiente, en el **menú desplegable de la rama main**,
    haga clic en la rama **welcome-workflow**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image8.jpeg)

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image9.jpeg)

7.  Una vez que la rama main se haya cambiado a **welcome-workflow**,
    navegue a la carpeta **.github/workflows**, luego seleccione **Add
    file** y haga clic en **Create new file**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image10.jpeg)

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image11.jpeg)

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image12.jpeg)

8.  En la página de creación del archivo, escriba el nombre del archivo
    como welcome.yml

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image13.jpeg)

9.  En la página del editor, agregue el siguiente contenido al archivo
    welcome.yml: y haga clic en **Commit changes.**

10. name: Post welcome comment

11. on:

12. pull_request:

13. types: \[opened\]

14. permissions:

pull-requests: write

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image14.jpeg)

15. En la página **Commit changes**, haga clic en **Commit changes**.

16. Espere 20 segundos para que las actions se ejecuten, luego actualice
    la página y una action cerrará automáticamente este paso.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image15.jpeg)

Resumen:

Ahora ha adquirido experiencia práctica en la configuración y
administración de GitHub Actions, mejorando su capacidad para
automatizar y optimizar los flujos de trabajo de desarrollo de software.
