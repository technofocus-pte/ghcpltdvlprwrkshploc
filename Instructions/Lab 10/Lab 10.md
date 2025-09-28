**Laboratorio 10: Utilizar GitHub Actions para publicar su proyecto en
una imagen de Docker**

Objetivos:

Imagine que está desarrollando un proyecto de software que desea
empaquetar y distribuir como una imagen de Docker. Para optimizar el
proceso de implementación y asegurarse de que su imagen de Docker se
publique de manera constante en GitHub Packages, decide utilizar GitHub
Actions para la automatización. Esto le permitirá configurar un flujo de
trabajo que automatice la publicación de su imagen de Docker cada vez
que se realicen cambios, garantizando que su proyecto esté siempre
actualizado y disponible para su implementación.

En este laboratorio práctico, usted:

- Configurará un archivo de flujo de trabajo de GitHub Actions que
  automatizará el proceso de compilación y publicación de su imagen de
  Docker.

- Configurará el flujo de trabajo para compilar su imagen de Docker y
  enviarla a GitHub Packages, asegurándose de que la imagen se publique
  correctamente.

- Creará una pull request para visualizar todos los cambios realizados.

Ejercicio \#1: Crear un nuevo repositorio a partir de una plantilla
pública

1.  Vaya al siguiente
    enlance: https://github.com/skills/publish-packages

En este laboratorio creará el repositorio utilizando una plantilla
pública "**skills-publish-packages**".

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image1.jpeg)

2.  Seleccione **Create a new repository** en el menú **Use this
    template**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image2.jpeg)

3.  Ingrese los siguientes detalles y seleccione **Create Repository**.

    - Repository name: **skills-publish-packages**

    - Repository type: **Public**

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image3.jpeg)

Ejercicio 2: Crear un archivo de flujo de trabajo y configurar el flujo
de trabajo

1.  Haga clic en el botón **Code** en la barra de navegación principal
    del repositorio que acaba de crear.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image4.jpeg)

2.  En el menú desplegable de la rama principal (**main**), seleccione
    la rama **cd**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image5.jpeg)

3.  En la siguiente página, navegue a la carpeta **.github/workflows/**,
    luego seleccione **Add file** y haga clic en **Create new file**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image6.jpeg)

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image7.jpeg)

4.  En el campo **Name your file**, ingrese publish.yml

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image8.jpeg)

5.  Agregue el siguiente código al archivo **publish.yml**.

6.  name: Publish to Docker

7.  on:

8.  push:

9.  branches:

10. \- main

11. permissions:

12. packages: write

13. contents: read

14. jobs:

15. publish:

16. runs-on: ubuntu-latest

17. steps:

18. \- name: Checkout

19. uses: actions/checkout@v4

20. \# Add your test steps here if needed...

21. \- name: Docker meta

22. id: meta

23. uses: docker/metadata-action@v5

24. with:

25. images: ghcr.io/YOURNAME/publish-packages/game

26. tags: type=sha

27. \- name: Login to GHCR

28. uses: docker/login-action@v3

29. with:

30. registry: ghcr.io

31. username: ${{ github.repository_owner }}

32. password: ${{ secrets.GITHUB_TOKEN }}

33. \- name: Build container

34. uses: docker/build-push-action@v5

35. with:

36. context: .

37. push: true

tags: ${{ steps.meta.outputs.tags }}

38. Reemplace YOURNAME con su nombre de usuario.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image9.jpeg)

39. Asegúrese de que el nombre de la imagen sea único y haga clic en
    **Commit changes.**

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image10.jpeg)

40. Haga clic en **Commit changes** una vez más.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image11.jpeg)

41. Ahora cree una pull request para visualizar todos los cambios que
    realizó en el ejercicio anterior.

42. Haga clic en la pestaña **Pull Requests** en la barra de navegación.

43. Haga clic en **New pull request**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image12.jpeg)

44. En la página **Comparing changes**, establezca **base**: main
    y **compare**:cd y luego haga clic en **Create pull request.**

![A screenshot of a chat AI-generated content may be
incorrect.](./media/image13.jpeg)

45. En la página **Add a title**, haga clic en **Create pull request.**

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image14.jpeg)

46. Espere 20 segundos a que se ejecuten las actions y revise los
    resultados.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image15.jpeg)

Resumen:

Ahora ha adquirido experiencia práctica en el uso de GitHub Actions para
automatizar la publicación de imágenes de Docker, mejorando su capacidad
para agilizar los procesos de implementación y mantener distribuciones
de proyectos actualizadas.
