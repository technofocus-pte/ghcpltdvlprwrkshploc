**Laboratorio 12: Creación de flujos de trabajo de implementación usando
GitHub Actions y Microsoft Azure**

Objetivo:

Imagine que administra un proyecto de software con requisitos de
implementación complejos que abarcan múltiples entornos, incluidos
ensayo (*staging*) y producción. Para optimizar su proceso de
implementación y garantizar la consistencia, decide automatizarlo con
GitHub Actions y Microsoft Azure. Al configurar flujos de
implementación, puede definir desencadenantes basados en etiquetas
aplicadas a las *pull requests*, los cuales se encargarán de
aprovisionar entornos, implementar en *staging* y desaprovisionar
entornos de forma automática. Este enfoque ayuda a mantener la
eficiencia y reduce la intervención manual en el pipeline de
implementación.

En este laboratorio práctico, usted:

- Configurará flujos de trabajo para crear y configurar automáticamente
  entornos utilizando recursos de Azure cuando se aplique una etiqueta
  específica a una pull request.

- Configurará tareas de implementación dentro de los flujos de trabajo
  para implementar automáticamente su proyecto en un entorno de staging
  al recibir la etiqueta correspondiente.

Ejercicio 1: Crear un nuevo repositorio

1.  Vaya al siguiente enlace: https://github.com/skills/deploy-to-azure

En este laboratorio, usted creará el repositorio utilizando una
plantilla pública **skills-deploy-to-azure**

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image1.jpeg)

2.  Seleccione **Create a new repository** en el menú **Use this
    template**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image2.jpeg)

3.  Ingrese los siguientes detalles y seleccione **Create Repository**.

    - Repository name: **skills-deploy-to-azure**

    - Repository type: **Public**

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image3.jpeg)

Ejercicio 2: Configurar los permisos de GITHUB_TOKEN

Al inicio de cada ejecución del flujo de trabajo, GitHub crea
automáticamente un secreto único llamado GITHUB_TOKEN para usar en su
flujo de trabajo. Es necesario asegurarse de que este token tenga los
permisos requeridos.

1.  En la página principal del repositorio recién creado, vaya a
    **Settings** \> **Actions** \> **General**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image4.jpeg)

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image5.jpeg)

2.  Desplácese hacia abajo hasta **Workflow permissions**, habilite
    **Read and write permissions** y haga clic en **Save**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image6.jpeg)

**Nota:** Esto es necesario para que el flujo de trabajo pueda cargar la
imagen en el registro de contenedores.

Ejercicio 3: Configurar un desencadenante basado en etiquetas

1.  En la barra de navegación, vaya a la pestaña **Actions**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image7.jpeg)

2.  En la página **Actions**, haga clic en **New workflow** en el panel
    de navegación del lado izquierdo.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image8.jpeg)

3.  En la página **Choose a workflow**, busque \\**simple workflow**\\ y
    haga clic en **Configure**

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image9.jpeg)

4.  Nombre su flujo de trabajo deploy-staging.yml

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image10.jpeg)

5.  En la página del editor, edite el contenido del archivo y elimine
    todos los triggers y jobs. El archivo resultante deberá quedar como
    se muestra a continuación.

6.  name: Stage the app

7.  on:

8.  pull_request:

9.  types: \[labeled\]

10. jobs:

11. build:

12. runs-on: ubuntu-latest

if: contains(github.event.pull_request.labels.\*.name, 'stage')

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image11.jpeg)

**Nota:** Por favor asegúrese de que el fragmento de código agregado
esté correctamente indentado, tal como se muestra en la captura de
pantalla

13. Haga clic en el botón **Commit changes** en la parte superior
    derecha de la página.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image12.jpeg)

14. En la ventana **Commit Changes**, seleccione **Create a new branch
    for this commit and start a pull request.**

**Nota:** La ventana **Commit changes** cambia a **Propose Changes**.

Asigne el nombre **staging-workflow** a la **nueva rama** y haga clic en
**Propose changes**.

![A screenshot of a chat AI-generated content may be
incorrect.](./media/image13.jpeg)

15. En la siguiente página de **Open a pull request**, haga clic en
    **Create pull request**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image14.jpeg)

16. Espere 20 segundos para que las acciones se ejecuten y luego revise
    los resultados.

Resumen:

Ahora ha adquirido experiencia práctica en la automatización de flujos
de trabajo de implementación con GitHub Actions, lo que mejora tanto la
eficiencia como la confiabilidad de su proceso de implementación.
