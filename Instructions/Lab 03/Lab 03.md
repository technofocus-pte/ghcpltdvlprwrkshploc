**Laboratorio 03: Cree su portafolio en línea con GitHub Pages y
Jekyll**

Objetivo:

Imagine que es un desarrollador de software en crecimiento en una
startup tecnológica, con entusiasmo por mostrar sus proyectos,
habilidades y experiencias mediante un portafolio en línea. Desea contar
con una plataforma profesional para exhibir su trabajo, por lo que
decide crear un sitio web o blog personal utilizando GitHub Pages. Esta
plataforma le permite aprovechar repositorios de GitHub para publicar y
mantener su sitio web de forma sencilla.

En este laboratorio práctico, usted:

- Creará un repositorio de GitHub: Configurará un nuevo repositorio que
  servirá como base para su sitio personal.

- Habilitará GitHub Pages: Configurará GitHub Pages para hospedar su
  sitio web directamente desde su repositorio.

- Implementará su primer sitio con Jekyll: Utilizará Jekyll, un popular
  generador de sitios estáticos, para crear e implementar un sitio web
  profesional con un esfuerzo mínimo.

Ejercicio n.º 1: Crear un repositorio a partir de una plantilla

1.  Inicie sesión en su cuenta de GitHub.

2.  Vaya al siguiente enlace: https://github.com/skills/github-pages

En este laboratorio, creará el repositorio utilizando una plantilla
pública - "**skills-github-pages**".

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image1.jpeg)

3.  Seleccione **Create a new repository** en el menú **Use this
    template**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image2.jpeg)

4.  Ingrese los siguientes detalles y seleccione **Create Repository**.

    - Repository name: **skills-github-pages**

    - Repository type: **Public**

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image3.jpeg)

Ejercicio n.º 2: Habilitar GitHub Pages

1.  Una vez creado el repositorio, vaya a la página principal. En el
    panel de navegación principal, seleccione el icono **Settings**.

![A screenshot of a web page AI-generated content may be
incorrect.](./media/image4.jpeg)

2.  En la página **Settings**, desplácese hacia abajo hasta **Code and
    automation** y seleccione **Pages.**

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image5.jpeg)

3.  En la página **GitHub Pages**, asegúrese de que en el menú
    desplegable **Source** esté seleccionada la opción **Deploy from a
    branch**, y luego seleccione **main** en el menú desplegable
    **Branch**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image6.jpeg)

4.  Haga clic en el botón **Save** para continuar.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image7.jpeg)

5.  La fuente de GitHub Pages se guardará. Espere aproximadamente un
    minuto y luego actualice esta página. GitHub Actions actualizará
    automáticamente al siguiente paso.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image8.jpeg)

6.  Su sitio ahora está activo.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image9.jpeg)

7.  Haga clic en el botón **Visit Site** para ver su sitio. Ha activado
    GitHub Pages.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image10.jpeg)

Ejercicio n.º 3: Implementar su sitio con Jekyll

Trabajará en la rama **my-pages** para que este sitio luzca excelente.
En este laboratorio usaremos un tema listo para blogs, "minima".

Jekyll utiliza un archivo titulado **\_config.yml** para almacenar la
configuración de su sitio, su tema y contenido reutilizable, como el
título del sitio y su usuario de GitHub.

1.  Seleccione la pestaña **Code** de su repositorio.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image11.jpeg)

2.  Expanda la rama **main** y seleccione **my-pages**.

![A screenshot of a web page AI-generated content may be
incorrect.](./media/image12.jpeg)

En la rama **my-pages**, busque el archivo \_**config.yml**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image13.jpeg)

3.  Abra el editor de archivos en la esquina superior derecha.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image14.jpeg)

4.  Agregue un tema: establezca el valor en **minima** para que aparezca
    en el archivo \_config.yml como se muestra a continuación:

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image15.jpeg)

5.  Haga clic en el botón **Commit changes** para guardar los cambios.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image16.jpeg)

**Nota:** Espere aproximadamente un minuto y luego actualice esta
página. GitHub Actions se actualizará automáticamente al siguiente paso.

6.  Para comprobar el sitio actualizado, seleccione el botón **Visit
    site** que se encuentra debajo de **GitHub Pages**.

![A screenshot of a web page AI-generated content may be
incorrect.](./media/image17.jpeg)

7.  El tema seleccionado se ha aplicado. Puede continuar modificando
    otras variables de configuración como title:, author: y description:
    para personalizar aún más su sitio.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image18.jpeg)

Resumen:

Ahora ha creado un sitio web con GitHub Pages y ha aplicado un tema.
Puede aprovechar esta experiencia para crear un sitio web en vivo que
pueda actualizar de forma continua y en el que pueda mostrar su
trayectoria en el desarrollo de software, lo que facilitará que
empleadores, colaboradores y la comunidad tecnológica conozcan su
trabajo y habilidades.
