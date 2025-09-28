**Laboratorio 09: Crear flujos de trabajo para usar integración continua
(CI) en sus proyectos**

Objetivos:

Imagine que usted está trabajando en un proyecto de software donde
mantener altos estándares de calidad es crucial. Para garantizar que su
código se mantenga robusto y libre de errores, decide implementar
Integración Continua (CI) utilizando GitHub Actions. La CI ayuda a
automatizar el proceso de ejecución de pruebas y verificación de la
calidad del código cada vez que se realizan cambios en la base de
código. Al crear workflows de CI, se pueden ejecutar automáticamente
linters para archivos Markdown, correr pruebas y recibir
retroalimentación inmediata sobre la calidad del código, asegurando que
su proyecto cumpla de manera consistente con los estándares de calidad.

En este laboratorio práctico, usted:

- Creará un flujo de trabajo de pruebas: Configurará un workflow de
  GitHub Actions diseñado específicamente para realizar linting de
  archivos Markdown y comprobar problemas de formato.

- Configurará y actualizará el workflow: Configurará el archivo del
  workflow para definir los jobs y steps necesarios para el linting
  automatizado y lo actualizará según sea necesario para mejorar su
  funcionalidad.

- Creará una Pull Request: Integrará los cambios creando una pull
  request, lo que permitirá probar el workflow de CI y observar cómo
  automatiza las verificaciones de calidad.

- Analizará los resultados del workflow de CI para comprender cómo se
  reportan los problemas y cómo se garantiza la calidad del código.

Ejercicio \#1: Crear un nuevo repositorio desde una plantilla pública

1.  Vaya al siguiente
    enlace: https://github.com/skills/test-with-actions

En este laboratorio creará el repositorio usando una plantilla pública
"**skills-test-with-actions**".

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image1.jpeg)

2.  Seleccione **Create a new repository** en el menú **Use this
    template**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image2.jpeg)

3.  Ingrese los siguientes detalles y seleccione **Create Repository**.

    - Repository name: **skills-test-with-actions**

    - Repository type: **Public**

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image3.jpeg)

Ejercicio \#2: Agregar un flujo de trabajo de prueba

1.  Navegue a la pestaña Actions en el repositorio creado anteriormente.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image4.jpeg)

2.  Debajo de Actions en la barra lateral izquierda, seleccione **New
    workflow**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image5.jpeg)

3.  En la página **Choose a workflow**, navegue hasta "**Simple
    workflow**" y haga clic en **Configure**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image6.jpeg)

4.  En la siguiente página, cambie el nombre de su flujo de trabajo a
    ci.yml y actualice el flujo de trabajo eliminando los dos últimos
    pasos.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image7.jpeg)

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image8.jpeg)

5.  Agregue el siguiente código al final del flujo de trabajo y haga
    clic en **Commit changes** en la parte superior derecha.

6.  \- name: Run markdown lint

7.  run: |

8.  npm install remark-cli remark-preset-lint-consistent

npx remark . --use remark-preset-lint-consistent

**Nota:** Por favor asegúrese de que el fragmento de código agregado al
workflow esté correctamente indentado

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image9.jpeg)

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image10.jpeg)

9.  En la ventana **Commit changes**, seleccione **Create a new branch
    for this commit and start a pull request**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image11.jpeg)

10. Una vez seleccionado **Create a new branch for this commit and start
    a pull request**, la ventana **Commit changes** cambia a **Propose
    changes**. Ahora haga clic en **Propose changes**.

![A screenshot of a computer screen AI-generated content may be
incorrect.](./media/image12.jpeg)

11. En la página siguiente de **Open a pull request**, haga clic en
    **Create pull request.**

![A screenshot of a email AI-generated content may be
incorrect.](./media/image13.jpeg)

12. Espere 20 segundos y luego actualice esta página para analizar los
    resultados.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image14.jpeg)

Resumen:

Ahora ha adquirido experiencia práctica con las prácticas de CI
utilizando GitHub Actions, lo que mejora su capacidad para automatizar y
mantener altos estándares de calidad en sus proyectos de software.
