**Laboratorio 07: Programación con GitHub Codespaces y Visual Studio
Code**

Objetivo:

Imagine que es un desarrollador que trabaja en un proyecto que requiere
un entorno de desarrollo alojado en la nube para facilitar la
colaboración y optimizar su flujo de trabajo. Para mejorar su
productividad y administrar de manera más eficaz la configuración de su
entorno de desarrollo, decide usar GitHub Codespaces con Visual Studio
Code. Esta configuración le permite crear y personalizar entornos de
desarrollo directamente en la nube, lo que facilita la colaboración con
su equipo y la administración eficiente de las configuraciones del
proyecto.

En este laboratorio práctico, usted aprenderá a:

- Iniciar un Codespace: Cree y ejecute un GitHub Codespace utilizando
  plantillas predefinidas.

- Personalizar configuraciones: Personalice las configuraciones de su
  proyecto dentro del codespace para adaptarlas a sus necesidades de
  desarrollo.

- Administrar Codespaces: Administre y navegue sus codespaces de manera
  eficiente, asegurando un proceso de desarrollo fluido y organizado.

- Enviar código al repositorio: Practique cómo enviar sus cambios de
  código desde el codespace al repositorio de GitHub, reforzando su
  capacidad de integrar el trabajo de desarrollo con el control de
  versiones.

Ejercicio \#1: Configurar un nuevo repositorio e iniciar un GitHub
Codespace

1.  Inicie sesión en su cuenta de GitHub.

2.  Vaya al siguiente
    enlace: https://github.com/skills/code-with-codespaces

En este laboratorio usted creará el repositorio utilizando una plantilla
pública "**skills-code-with-codespaces**".

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image1.jpeg)

3.  Seleccione **Create a new repository** en el menú **Use this
    template**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image2.jpeg)

4.  Ingrese los siguientes detalles y seleccione **Create Repository**.

    - Repository name: **skills-code-with-codespaces**

    - Repository type: **Public**

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image3.jpeg)

5.  Una vez que el repositorio sea creado, haga clic en el botón
    **Code**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image4.jpeg)

6.  Seleccione la pestaña **Codespaces** en la ventana emergente y luego
    haga clic en el botón **Create codespace on main**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image5.jpeg)

**Nota:** El codespace se abrirá en una nueva pestaña del explorador.

7.  El explorador mostrará un editor web de VS Code y un terminal deberá
    estar presente como se muestra a continuación.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image6.jpeg)

8.  Espere 2 minutos para que el codespace (una máquina virtual) se
    inicie.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image7.jpeg)

9.  Navegue de regreso al repositorio **skills-code-with-codespaces** y
    haga clic en el botón **Code**

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image8.jpeg)

**Nota:** Si el codespace recién creado no se carga, actualice la
página.

10. Haga clic en el icono de tres puntos (…) en el codespace
    activo\*\*.\*\*

**Nota**: El nombre del codespace puede variar en su caso

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image9.jpeg)

11. Seleccione **Open in Visual Studio Code** en el menú emergente.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image10.jpeg)

12. Un mensaje emergente solicitará confirmación para abrir el codespace
    en la aplicación Visual Studio Code. Seleccione **Open Visual Studio
    Code** para abrir el codespace.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image11.jpeg)

13. Se le pedirá instalar la extensión de GitHub Codespaces, haga clic
    en **Install extension and open URI**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image12.jpeg)

14. Una vez instalada, verá una ventana emergente solicitando permisos
    adicionales. **Haga clic en Authorize** **Visual Studio code**

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image13.jpeg)

15. Confirme el acceso ingresando la contraseña de su cuenta de GitHub.

![A screenshot of a login form AI-generated content may be
incorrect.](./media/image14.jpeg)

**Nota:** Si aparece la ventana emergente Allow Windows Firewall
permissions, seleccione Allow para continuar.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image15.jpeg)

Ejercicio \#2: Enviar código a su repositorio desde el codespace

1.  Desde dentro del codespace, en la ventana del explorador de VS Code,
    seleccione el archivo index.html.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image16.jpeg)

2.  Reemplace el encabezado h1 con lo siguiente:

\<h1\>Hello from the codespace!\</h1\>

3.  Guarde el archivo.

**Nota:** El archivo debería guardarse automáticamente.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image17.jpeg)

4.  Ingrese el siguiente mensaje de confirmación en la terminal de VS
    Code para hacer commit del cambio:

git commit -a -m "Adding hello from the codespace!"

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image18.jpeg)

5.  En la terminal de VS Code, ejecute el siguiente comando para enviar
    los cambios a su repositorio:

git push

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image19.jpeg)

6.  ¡El nuevo código desde VS Code ha sido enviado a su repositorio!

7.  Cambie de nuevo a la página principal de su repositorio y revise el
    archivo index.html para verificar que el nuevo código fue enviado a
    su repositorio.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image20.jpeg)

8.  Espere aproximadamente 20 segundos y luego actualice la página;
    GitHub Actions se actualizará automáticamente al siguiente paso.

Resumen:

Ahora ha utilizado GitHub Codespaces y Visual Studio Code para

- Crear y lanzar un Codespace de GitHub usando plantillas predefinidas.

- Enviar código al repositorio: practicó cómo enviar sus cambios de
  código desde el Codespace al repositorio de GitHub, reforzando su
  capacidad de integrar el trabajo de desarrollo con el control de
  versiones.
