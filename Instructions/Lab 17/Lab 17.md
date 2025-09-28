**Laboratorio 17: Habilitar Secret scanning en un repositorio de GitHub
y realizar un commit de un token**

Imagine que es un desarrollador de software que trabaja en un proyecto
en equipo con un repositorio compartido en GitHub. Para garantizar que
su código permanezca seguro y libre de filtraciones accidentales, decida
implementar Secret scanning, una característica que ayuda a identificar
información confidencial, como tokens de API o contraseñas, que podrían
incorporarse al repositorio de forma inadvertida mediante un commit.

Objetivo:

En este laboratorio práctico, realizará lo siguiente:

1.  Habilitará Secret scanning: Configurará Secret scanning en su
    repositorio de GitHub para detectar y marcar automáticamente
    información confidencial.

2.  Realizará un commit de un token: Agregará intencionalmente un token
    u otra información confidencial al repositorio para probar la
    efectividad de la función Secret scanning.

Ejercicio \#1:Crear un repositorio de GitHub y habilitar Secret scanning

Tarea \#1: Cree un repositorio usando una plantilla

1.  Inicie sesión en su cuenta de GitHub.

2.  Vaya al siguiente
    enlace: https://github.com/skills/introduction-to-secret-scanning

En este laboratorio, cree el repositorio usando una plantilla pública
"**skills-introduction-to-secret-scanning**".

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image1.jpeg)

3.  Seleccione **Create a new repository** debajo del menú **Use this
    template**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image2.jpeg)

4.  Ingrese los siguientes detalles y seleccione **Create Repository**.

    - Repository name: **skills-introduction-to-secret-scanning**

    - Repository type: **Public**

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image3.jpeg)

Tarea \#2: Habilite secret scanning

1.  En la página principal del repositorio recién creado, seleccione
    **Settings** en la barra de navegación superior.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image4.jpeg)

2.  En la sección **Security** en la barra lateral, seleccione **Code
    security and analysis**.

**Nota**: Desplácese hacia abajo para ver el menú **Security**.

![A screenshot of a browser window AI-generated content may be
incorrect.](./media/image5.jpeg)

3.  Desplácese hasta la parte inferior de la página y seleccione
    **Enable** en Secret scanning

**Nota:** Si ve el botón **Disable**, significa que secret scanning ya
está habilitado para el repositorio.

![A white background with black text AI-generated content may be
incorrect.](./media/image6.jpeg)

Si aún no está habilitado, verá el botón **Enable** como se muestra a
continuación:

![A screenshot of a computer error AI-generated content may be
incorrect.](./media/image7.jpeg)

**Nota:** Cuando secret scanning está habilitado, se envía una
notificación por correo electrónico sobre credenciales en el repositorio
al correo asociado a la cuenta. Los tokens en este repositorio de Skills
están inactivos. No existe riesgo para el entorno.

Ahora que secret scanning está habilitado en este repositorio, realice
un commit de un nuevo token para comprobar cómo funciona.

Ejercicio \#2: Realice un commit de un token

En este ejercicio, realizará un commit de una clave de AWS y un ID de
acceso en el repositorio. Este es un token inactivo que no se puede usar
para iniciar sesión en AWS.

1.  En el panel superior izquierdo de la barra de navegación principal,
    seleccione la pestaña **Code** y seleccione el archivo
    **credentials.yml**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image8.jpeg)

2.  Seleccione el botón Edit a la derecha.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image9.jpeg)

3.  Copie el texto siguiente y péguelo debajo de el código existente en
    el panel de edición del archivo **credentials.yml**.

4.  default:

5.  aws_access_key_id: AKIAQYLPMN5HNM4OZ56B

6.  aws_secret_access_key: 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

7.  output: json

region: us-east-2

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image10.jpeg)

8.  Haga clic en el botón **Commit changes** en la esquina superior
    derecha y haga clic en **Commit Changes** nuevamente en la ventana
    **Commit Changes**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image11.jpeg)

**Nota:** Después de realizar el commit de los cambios, recibirá una
alerta en el buzón de correo asociado a su cuenta de GitHub.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image12.jpeg)

Resumen:

Ahora ha adquirido una comprensión práctica de cómo habilitar y probar
secret scanning para proteger su código y sus datos.
