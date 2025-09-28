**Laboratorio 15: Habilitar CodeQL para proteger su código fuente**

Objetivo:

Imagine que es un desarrollador de software que trabaja en un proyecto
crítico para su empresa, donde garantizar la seguridad de la aplicación
es la máxima prioridad. Con las crecientes preocupaciones sobre
ciberamenazas y filtraciones de datos, es fundamental asegurarse de que
el código esté libre de vulnerabilidades y prácticas de codificación
inseguras.

En este laboratorio práctico, habilitará GitHub Code Scanning para
revisar automáticamente el código fuente en busca de posibles problemas
de seguridad.

Ejercicio \#1: Crear un nuevo repositorio a partir de una plantilla
pública

1.  Inicie sesión en su cuenta de GitHub.

2.  Navegue al siguiente
    enlace: https://github.com/skills/introduction-to-codeql

En este laboratorio, usted creará el repositorio utilizando una
plantilla pública "**skills-introduction-to-codeql**".

![](./media/image1.jpeg)

3.  Seleccione **Create a new repository** en el menú **Use this
    template**.

![](./media/image2.jpeg)

4.  Ingrese los siguientes detalles y seleccione **Create Repository**.

    - Repository name:**skills-introduction-to-codeql**

    - Repository type: **Public**

![](./media/image3.jpeg)

Ejercicio \#2: Habilitar el análisis de código con CodeQL

1.  En la página principal del repositorio recién creado, navegue a la
    pestaña **Settings**.

![](./media/image4.jpeg)

2.  En la barra lateral izquierda, debajo de la sección **Security**,
    seleccione **Code security and analysis**.

![](./media/image5.jpeg)

3.  Desplácese hacia abajo hasta la sección titulada **Code scanning**,
    haga clic en el menú desplegable **Set up** y seleccione
    **Default**.

![](./media/image6.jpeg)

4.  Seleccione las siguientes opciones y haga clic en **Enable CodeQL**

    - Languages to analyze: Estos son los lenguajes que serán analizados
      por CodeQL. En este caso, se analizará Python.

    - Query suites: Las consultas de CodeQL se agrupan en paquetes
      llamados suites. Esta sección le permite elegir qué suite de
      consultas usar. Para este ejercicio, déjela en Default.

    - Events: Esta sección indica a CodeQL cuándo realizar el análisis.
      En este caso, está configurado para analizar en cualquier pull
      request hacia la rama main.

![](./media/image7.jpeg)

5.  Espere aproximadamente 20 segundos y luego actualice esta página
    para continuar.

![](./media/image8.jpeg)

Resumen:

Ahora ha habilitado GitHub Code Scanning para revisar automáticamente su
código fuente en busca de posibles problemas de seguridad.
