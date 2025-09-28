**Laboratorio 14: Proteja la cadena de suministro de su repositorio**

Objetivos:

Imagine que usted es responsable de mantener la seguridad de un proyecto
de software que depende de diversas dependencias de terceros. Para
garantizar la integridad y la seguridad de la cadena de suministro de su
proyecto, configure un control eficaz de dichas dependencias. Esto
implica identificar posibles vulnerabilidades en ellas y aplicar los
parches necesarios para proteger el proyecto. En este laboratorio, usted
aprenderá a utilizar la característica Dependency graph de GitHub para
supervisar y revisar las dependencias, asegurándose de que el proyecto
permanezca seguro y actualizado.

En este laboratorio práctico, usted:

- Habilitará Dependency Graph: Habilite y verifique la característica
  Dependency Graph en la configuración de su repositorio para visualizar
  las dependencias de su proyecto.

- Agregará una nueva dependencia: Agregue una nueva dependencia a su
  proyecto y asegúrese de que esté integrada correctamente.

- Revisará Dependency Graph: Utilice Dependency Graph para revisar y
  confirmar que la nueva dependencia se refleje y supervise de manera
  adecuada.

Ejercicio 01: Crear un nuevo repositorio

1.  Vaya al siguiente
    enlace: https://github.com/skills/secure-repository-supply-chain

En este laboratorio usted creará el repositorio utilizando una plantilla
pública **skills-secure-repository-supply-chain**

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image1.jpeg)

2.  Seleccione **Create a new repository** en el menú **Use this
    template**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image2.jpeg)

3.  Ingrese los siguientes detalles y seleccione **Create Repository**.

    - Repository name: **skills-secure-repository-supply-chain**

    - Repository type: **Public**

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image3.jpeg)

Ejercicio 02: Verifique que Dependency graph esté habilitado

1.  En la página principal del repositorio recién creado, navegue a la
    pestaña **Settings**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image4.jpeg)

2.  En la página **Settings**, seleccione **Code security and
    analysis** que se encuentra disponible debajo de **Security.**

![A screenshot of a general login AI-generated content may be
incorrect.](./media/image5.jpeg)

3.  Verifique o habilite Dependency graph. (Si el repositorio es
    privado, habilítelo aquí. Si el repositorio es público, estará
    habilitado de manera predeterminada)

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image6.jpeg)

Ejercicio 03: Agregar una nueva dependencia y ver su gráfico de
dependencias

1.  Navegue a la pestaña **Code** y localice la
    carpeta **code/src/AttendeeSite**.

**Note:** Puede navegar a la carpeta o utilizar la búsqueda **Go to
file** con code/src/AttendeeSite

![A screenshot of a web page AI-generated content may be
incorrect.](./media/image7.jpeg)

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image8.jpeg)

2.  Abra el archivo **package-lock.json**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image9.jpeg)

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image10.jpeg)

3.  Inserte el siguiente fragmento de código entre la línea n.º 14 y la
    línea n.º 15

4.  "follow-redirects": {

5.  "version": "1.14.1",

6.  "resolved":

7.  "https://registry.npmjs.org/follow-redirects/-/follow-redirects-1.14.1.tgz",

8.  "integrity":

9.  "sha512-HWqDgT7ZEkqRzBvc2s64vSZ/hfOceEol3ac/7tKwzuvEyWx3/4UegXh5oBOIotkGsObyk3xznnSRVADBgWSQVg=="

},

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image11.jpeg)

**Nota:** Por favor asegúrese de que el fragmento de código agregado
esté correctamente indentado, tal como se muestra en la captura de
pantalla

10. En la parte superior derecha, seleccione **Commit changes**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image12.jpeg)

11. En la barra de navegación principal haga clic en **Insights tab**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image13.jpeg)

12. En el panel de navegación lateral haga clic en **Dependency graph**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image14.jpeg)

13. Revise todas las nuevas dependencias en el Dependencies hub.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image15.jpeg)

14. Busque follow-redirects y revise la nueva dependencia que acaba de
    agregar.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image16.jpeg)

Resumen:

Ahora ha adquirido conocimientos valiosos sobre la gestión de las
dependencias de su proyecto y la protección de la cadena de suministro
de su repositorio, lo que le permitirá abordar y mitigar de manera
proactiva los riesgos de seguridad.
