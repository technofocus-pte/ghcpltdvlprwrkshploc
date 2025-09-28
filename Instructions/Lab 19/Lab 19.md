**Laboratorio 19 - Cree una API REST usando Quarkus con la ayuda de
GitHub Copilot**

El objetivo de este laboratorio es aprender a usar GitHub Copilot
mediante tareas que consisten en construir una API REST usando
https://quarkus.io/.

Se creó un proyecto de Quarkus con algunos archivos ya preparados; puede
encontrarlo en la carpeta **exercisefiles/quarkus**.

¡Comencemos a copilotar!

**Tarea 1 - Crear el código para manejar una solicitud GET simple**

Vaya al archivo 'DemoResource.java' y comience a escribir el código para
manejar una solicitud GET simple.

1.  En este primer paso, se proporciona un comentario que describe el
    código que debe generar. Solo presione Enter y espere un par de
    segundos.

![BrokenImage](./media/image1.png)

2.  Copilot generará el código por usted. Si no está conforme con el
    código, presione Ctrl + Enter y se le mostrarán múltiples opciones
    de código.

![A screenshot of a computer Description automatically
generated](./media/image2.png)

3.  Si no está conforme con el código generado, puede presionar Enter
    nuevamente y Copilot generará un nuevo código.

![A screenshot of a computer Description automatically
generated](./media/image3.png)

![A screenshot of a computer program Description automatically
generated](./media/image4.png)

![A screenshot of a computer program Description automatically
generated](./media/image5.png)

4.  Vaya a **test/java/com/Microsoft/hackthon/quarkus/** y haga clic en
    **DemoResourceTest.java**. Ya existe una prueba unitaria
    implementada para esta tarea.

![A screenshot of a computer Description automatically
generated](./media/image6.png)

5.  Haga clic en **Terminal -\> New Terminal.**

![BrokenImage](./media/image7.png)

6.  Seleccione **Gitbash**.

![BrokenImage](./media/image8.png)

7.  Ejecute el comando: cd exercisefiles/quarkus/copilot-demo/ 

![A screen shot of a computer program Description automatically
generated](./media/image9.png)

8.  Puede ejecutarlo usando el comando mvn test antes y después para
    validar que el código generado por Copilot sea correcto.

![A screenshot of a computer program Description automatically
generated](./media/image10.png)

![A screen shot of a computer Description automatically
generated](./media/image11.png)

![A screenshot of a computer program Description automatically
generated](./media/image12.png)

9.  Después de cada tarea, si lo desea, puede empaquetar y ejecutar su
    aplicación para probarla.

Package: mvn package

![A screenshot of a computer program Description automatically
generated](./media/image13.png)

![A screenshot of a computer program Description automatically
generated](./media/image14.png)

10. Ejecutar: mvn quarkus:dev

![A screenshot of a computer program Description automatically
generated](./media/image15.png)

![A screenshot of a computer program Description automatically
generated](./media/image16.png)

11. Seleccione la opción de dividir el terminal, ingrese el comando en
    el segundo terminal y ejecútelo.

curl -v http://localhost:8080/hello?key=world

curl http://localhost:8080/hello

curl http://localhost:8080/hello?key=world

![A screenshot of a computer screen Description automatically
generated](./media/image17.png)

![BrokenImage](./media/image18.png)

**Tarea 2: Comparación de fechas**

Cree una nueva operación bajo /diffdates que calcule la diferencia entre
dos fechas.  
La operación debe recibir dos fechas como parámetros en el formato
dd-MM-yyyy y devolver la diferencia en días.

1.  Escriba el siguiente comentario // New operation under /diffdates
    that calculates the difference between two dates. The operation
    should receive two dates as parameter in format dd-MM-yyyy and
    return the difference in days. y presione Enter.

**Nota:** El comentario se encuentra en el
archivo **DemoResource.java**. **C:\CopiolHackathon\exercisefiles\\
quarkus\\ copilot-demo\src\main\\
java\com\microsoft\hackathon\quarkus\DemoResource.java**

![A screen shot of a computer program Description automatically
generated](./media/image19.png)

2.  Presione la tecla Tab y luego nuevamente Tab para aceptar el código.

![A screen shot of a computer program Description automatically
generated](./media/image20.png)

3.  Abra el archivo DemoResourceTest.java, cree una prueba unitaria que
    valide la operación. Agregue //Create a unit test to validate
    /diffdates that calculates the difference between two dates y luego
    presione Enter.

![A screenshot of a computer program Description automatically
generated](./media/image21.png)

4.  Presione la tecla Tab para aceptar el código. También puede usar el
    siguiente código.

5.  package com.microsoft.hackathon.quarkus;

6.  

7.  import jakarta.ws.rs.GET;

8.  import jakarta.ws.rs.Path;

9.  import jakarta.ws.rs.Produces;

10. import jakarta.ws.rs.QueryParam;

11. import jakarta.ws.rs.client.Client;

12. import jakarta.ws.rs.client.ClientBuilder;

13. import jakarta.ws.rs.client.WebTarget;

14. import jakarta.ws.rs.core.MediaType;

15. import jakarta.ws.rs.core.Response;

16. 

17. import java.io.File;

18. import java.io.FileInputStream;

19. import java.io.IOException;

20. import java.io.InputStream;

21. import java.net.URL;

22. import java.nio.file.Files;

23. import java.nio.file.Paths;

24. import java.text.SimpleDateFormat;

25. import java.util.ArrayList;

26. import java.util.Date;

27. import java.util.List;

28. import java.util.Objects;

29. 

30. import com.fasterxml.jackson.databind.JsonNode;

31. import com.fasterxml.jackson.databind.ObjectMapper;

32. import com.fasterxml.jackson.databind.node.ObjectNode;

33. 

34. import io.quarkus.fs.util.ZipUtils;

35. 

36. 

37. 

38. 

39. 

40. /\*

41. \* The Demo resource should be mapped to the root path.

42. \*

43. \* Create a GET operation to return the value of a key passed as
    query parameter in the request.

44. \*

45. \* If the key is not passed, return "key not passed".

46. \* If the key is passed, return "hello \<key\>".

47. \*

48. \*/

49. 

50. @Path("/")

51. public class DemoResource {

52. @GET

53. @Path("/hello")

54. @Produces(MediaType.TEXT_PLAIN)

55. public String hello(@QueryParam("key") String key) {

56. if (key == null) {

57. return "key not passed";

58. } else {

59. return "hello " + key;

60. }

61. }

62. // New operation under /diffdates that calculates the difference
    between two dates. The operation should receive two dates as
    parameter in format dd-MM-yyyy and return the difference in days.

63. @GET

64. @Path("/diffdates")

65. @Produces(MediaType.TEXT_PLAIN)

66. public String diffdates(@QueryParam("date1") String date1,
    @QueryParam("date2") String date2) {

67. Objects.requireNonNull(date1, "date1 must not be null");

68. Objects.requireNonNull(date2, "date2 must not be null");

69. try {

70. SimpleDateFormat dateFormat = new SimpleDateFormat("dd-MM-yyyy");

71. Date date1Obj = dateFormat.parse(date1);

72. Date date2Obj = dateFormat.parse(date2);

73. long diffMillis = Math.abs(date1Obj.getTime() - date2Obj.getTime());

74. long diffDays = diffMillis / (24 \* 60 \* 60 \* 1000);

75. return String.valueOf(diffDays);

76. } catch (Exception e) {

77. return "invalid date format";

78. }

}

![A screenshot of a computer program Description automatically
generated](./media/image22.png)

79. Abra la terminal y ejecute el comando mvn test.

![A screen shot of a computer Description automatically
generated](./media/image23.png)

![A screenshot of a computer program Description automatically
generated](./media/image24.png)

80. Empaquete la solución ejecutando el comando mvn package.

![A screenshot of a computer program Description automatically
generated](./media/image25.png)

![A screenshot of a computer program Description automatically
generated](./media/image26.png)

81. Ejecute: mvn quarkus:dev or mvn compile quarkus:dev

![A screenshot of a computer program Description automatically
generated](./media/image27.png)

82. Divida la terminal y ejecute curl -v http://localhost:8080/diffdates

**Tarea 3: Validar el formato de un teléfono español**

Valide el formato de un número de teléfono español (prefijo +34, seguido
de 9 dígitos que comiencen con 6, 7 o 9). La operación debe recibir un
número de teléfono como parámetro y devolver true si el formato es
correcto o false en caso contrario.

1.  Escriba el comentario //Validate the format of a spanish phone
    number (+34 prefix, then 9 digits, starting with 6, 7 or 9). The
    operation should receive a phone number as parameter and return true
    if the format is correct, false otherwise y presione Enter. Presione
    Tab para aceptar el código sugerido por Copilot.

![A screen shot of a computer program Description automatically
generated](./media/image28.png)

2.  Escriba el comentario // write unit test to Validate the format of a
    spanish phone number (+34 prefix, then 9 digits, starting with 6, 7
    or 9). The operation should receive a phone number as parameter and
    return true if the format is correct, false otherwise y presione
    Enter. Presione Tab para aceptar las pruebas unitarias sugeridas por
    Copilot.

![A screen shot of a computer program Description automatically
generated](./media/image29.png)

3.  Abra la terminal y ejecute el comando mvn test.

![A screen shot of a computer Description automatically
generated](./media/image30.png)

![A screenshot of a computer program Description automatically
generated](./media/image31.png)

4.  Ejecute mvn package

![A screenshot of a computer program Description automatically
generated](./media/image32.png)

![A screenshot of a computer program Description automatically
generated](./media/image33.png)

5.  Ejecute mvn quarkus:dev

![A screenshot of a computer screen Description automatically
generated](./media/image34.png)

6.  Seleccione la opción de dividir la terminal y ejecute el comando en
    una de las terminales

curl -v http://localhost:8080/validatephone?phone=+34866666666

curl -v http://localhost:8080/validatephone?phone=+34666666667

curl -v http://localhost:8080/validatephone?phone=+34666666666

![A screenshot of a computer program Description automatically
generated](./media/image35.png)

**Tarea 4: Validar el formato de un DNI español**

Valide el formato de un DNI español (8 dígitos y 1 letra). La operación
debe recibir un DNI como parámetro y devolver true si el formato es
correcto o false en caso contrario.

1.  Escriba el comentario // Validate the format of a spanish DNI (8
    digits and 1 letter). The operation should receive a DNI as
    parameter and return true if the format is correct, false otherwise.
    y presione Enter. Presione Tab para aceptar el código sugerido por
    Copilot.

![A screenshot of a computer program Description automatically
generated](./media/image36.png)

2.  Cambie a **CopilotDemoApplicationTests.java**. Para escribir una
    prueba unitaria que valide la función anterior, agregue el
    comentario //Write unit test to Validate the format of a spanish DNI
    (8 digits and 1 letter). The operation should receive a DNI as
    parameter and return true if the format is correct, false otherwise.
    y presione Enter. Presione la tecla Tab para aceptar el código.

![A screen shot of a computer program Description automatically
generated](./media/image37.png)

3.  Abra la terminal y ejecute el comando mvn test

![A screenshot of a computer program Description automatically
generated](./media/image38.png)

![A screenshot of a computer program Description automatically
generated](./media/image39.png)

4.  Ejecute mvn package

![A screenshot of a computer program Description automatically
generated](./media/image40.png)

![A screenshot of a computer program Description automatically
generated](./media/image41.png)

5.  Ejecute: mvn quarkus:dev

![A screenshot of a computer program Description automatically
generated](./media/image42.png)

6.  Ejecute: curl -v
    http://localhost:8080/hello/validatedni?dni=12345678A

![A screenshot of a computer program Description automatically
generated](./media/image43.png)

**Tarea 5: De nombre de color a código hexadecimal**

Con base en el archivo existente colors.json dentro de la carpeta
resources, dado el nombre de un color como parámetro de ruta, devuelva
el código hexadecimal. Si el color no se encuentra, devuelva 404.

Pista: Use TDD. Comience creando la prueba unitaria y luego implemente
el código.

1.  Escriba el comentario // Based on the existing colors.json file
    under resources, given the name of the color as path parameter,
    return the hexadecimal code. If the color is not found, return 404.
    y presione Enter. Presione Tab para aceptar el código sugerido por
    Copilot.

![A screenshot of a computer program Description automatically
generated](./media/image44.png)

2.  Cambie a **CopilotDemoApplicationTests.java**. Para escribir una
    prueba unitaria que valide la función anterior, agregue el
    comentario //Write unit test to Based on the existing colors.json
    file under resources, given the name of the color as path parameter,
    return the hexadecimal code. If the color is not found, return 404.
    y presione Enter. Presione la tecla Tab para aceptar el código.

![A screenshot of a computer program Description automatically
generated](./media/image45.png)

3.  Ejecute mvn test

![A screenshot of a computer program Description automatically
generated](./media/image46.png)

![A screenshot of a computer program Description automatically
generated](./media/image47.png)

4.  Ejecute mvn package

![A screenshot of a computer Description automatically
generated](./media/image48.png)

5.  Ejecute: mvn quarkus:dev

![A screenshot of a computer program Description automatically
generated](./media/image49.png)

6.  Ejecute: curl -v http://localhost:8080/hello/color?color=red

![BrokenImage](./media/image50.png)

**Tarea 6: Creador de chistes**

Cree una nueva operación que llame a la API
https://api.chucknorris.io/jokes/random y devuelva el chiste.

1.  Escriba el comentario // Create a new operation that call the API
    https://api.chucknorris.io/jokes/random and return the joke. y
    presione Enter. Presione la tecla Tab para aceptar el código
    sugerido por Copilot.

![A screenshot of a computer program Description automatically
generated](./media/image51.png)

2.  Presione la tecla Tab para aceptar el código

![A screen shot of a computer program Description automatically
generated](./media/image52.png)

3.  Cambie a **CopilotDemoApplicationTests.java**. Para escribir una
    prueba unitaria que valide la función anterior, agregue el
    comentario //Create a new operation that call the API
    https://api.chucknorris.io/jokes/random and return the joke. y
    presione Enter. Presione la tecla Tab para aceptar el código.

![A screenshot of a computer program Description automatically
generated](./media/image53.png)

4.  Presione la tecla Tab para aceptar el código.

![A screenshot of a computer program Description automatically
generated](./media/image54.png)

5.  Haga clic en Terminal -\> New Terminal -\> Gitbash y ejecute los
    siguientes comandos

cd exercisefiles/quarkus/copilot-demo/

mvn test

![A screenshot of a computer program Description automatically
generated](./media/image55.png)

![A screenshot of a computer program Description automatically
generated](./media/image56.png)

6.  Ejecute el comando mvn package para empaquetar su aplicación.

![A screenshot of a computer program Description automatically
generated](./media/image57.png)

![A screenshot of a computer program Description automatically
generated](./media/image58.png)

7.  Ejecute: mvn quarkus:dev

![A screenshot of a computer program Description automatically
generated](./media/image59.png)

8.  Ejecute: curl -v http://localhost:8080/hello/joke

![A screenshot of a computer program Description automatically
generated](./media/image60.png)

**Tarea 7: Análisis de URL**

Dada una url como parámetro de consulta, analícela y devuelva el
protocolo, host, puerto, ruta y parámetros de consulta. La respuesta
debe estar en formato Json.

1.  Escriba el comentario //Given a url as query parameter, parse it and
    return the protocol, host, port, path and query parameters. The
    response should be in Json format. y presione Enter. Presione Tab
    para aceptar el código sugerido por Copilot.

![A screen shot of a computer program Description automatically
generated](./media/image61.png)

![A screen shot of a computer program Description automatically
generated](./media/image62.png)

2.  Cambie a **CopilotDemoApplicationTests.java**. Para escribir una
    prueba unitaria que valide la función anterior, agregue el
    comentario //Write unit test for Given a url as query parameter,
    parse it and return the protocol, host, port, path and query
    parameters. The response should be in Json format. y presione Enter.
    Presione la tecla Tab para aceptar el código.

![A screenshot of a computer program Description automatically
generated](./media/image63.png)

3.  Ejecute mvn test

![A screenshot of a computer program Description automatically
generated](./media/image64.png)

![A screenshot of a computer Description automatically
generated](./media/image65.png)

4.  Ejecute el comando mvn package para empaquetar su aplicación.

![A screenshot of a computer program Description automatically
generated](./media/image66.png)

5.  Ejecute mvn quarkus:dev

![A screenshot of a computer program Description automatically
generated](./media/image67.png)

6.  Haga clic en split terminal y ejecute curl -v
    http://localhost:8080/hello/parseurl?url=https://www.google.com/search?q=quarkus

![A screenshot of a computer program Description automatically
generated](./media/image68.png)

**Tarea 9: Conteo de palabras**

Dado el path de un archivo, cuente el número de ocurrencias de una
palabra proporcionada. El path y la palabra deben recibirse como
parámetros de consulta. La respuesta debe devolverse en formato Json.

1.  Escriba el comentario //Given the path of a file and count the
    number of occurrence of a provided word. The path and the word
    should be query parameters. The response should be in Json format. y
    presione Enter. Presione Tab para aceptar el código sugerido por
    Copilot.

![A screenshot of a computer program Description automatically
generated](./media/image69.png)

2.  Cambie a **CopilotDemoApplicationTests.java**. Para escribir una
    prueba unitaria que valide la función anterior, agregue el
    comentario //Write unit test to Given the path of a file and count
    the number of occurrence of a provided word. The path and the word
    should be query parameters. The response should be in Json format. y
    presione Enter. Presione la tecla Tab para aceptar el código.

![A screenshot of a computer program Description automatically
generated](./media/image70.png)

3.  Abra la **Terminal** y ejecute mvn test

![A screenshot of a computer program Description automatically
generated](./media/image71.png)

![A screenshot of a computer program Description automatically
generated](./media/image72.png)

4.  Ejecute el comando mvn package para empaquetar su aplicación.

![A screenshot of a computer program Description automatically
generated](./media/image73.png)

![A screenshot of a computer program Description automatically
generated](./media/image74.png)

5.  Ejecute: mvn quarkus:dev

![A screenshot of a computer program Description automatically
generated](./media/image75.png)

6.  Probar: curl \<http://localhost:8080/hello/countword?path=/tmp/test.txt&word=hello

You can ask GitHub copilot for curl command for your project.

![A screenshot of a computer program Description automatically
generated](./media/image76.png)

**Tarea 10: Contenerizar la aplicación**

Use el Dockerfile proporcionado para crear una imagen Docker de la
aplicación. En este caso, ya se le proporciona el contenido completo,
pero para compilar, ejecutar y probar la imagen Docker también usará
Copilot para generar los comandos.

He creado un archivo DOCKER.md donde documentaremos los pasos para
compilar la aplicación (nativa), compilar la imagen del contenedor,
ejecutar el contenedor y probar el contenedor.

1.  En Visual Studio Code, presione **Ctrl + Shift + X**, busque
    **Docker** e instálelo.

![A screenshot of a computer Description automatically
generated](./media/image77.png)

2.  Haga doble clic en **Docker Desktop** e inicie sesión con su cuenta
    de Docker.

![BrokenImage](./media/image78.png)

3.  Presione **Ctrl + Alt + I** para abrir el **chat de GitHub
    Copilot**. Pregunte a Copilot cómo compilar la imagen del
    contenedor, ejecutar el contenedor y probar el contenedor con el
    Dockerfile proporcionado.

![A screenshot of a computer program Description automatically
generated](./media/image79.png)

4.  Siga las instrucciones de Copilot. Compile la aplicación ejecutando
    el siguiente comando en la terminal:

./mvnw package -Pnative -Dquarkus.native.container-build=true

![A screenshot of a computer Description automatically
generated](./media/image77.png)

![A screenshot of a computer program Description automatically
generated](./media/image80.png)

![A screenshot of a computer program Description automatically
generated](./media/image81.png)

![A screenshot of a computer program Description automatically
generated](./media/image82.png)

![A screenshot of a computer program Description automatically
generated](./media/image83.png)

5.  **Build the Docker image:** Assuming your Dockerfile is
    named **Dockerfile.native-micro**, you can use the following
    command:

docker build -f Dockerfile.native-micro -t my-app .

![A computer screen shot of a program Description automatically
generated](./media/image84.png)

6.  Este comando le indica a Docker que construya una imagen usando el
    archivo \`Dockerfile.native-micro\` en el directorio actual (\`.\`
    al final del comando), y que etiquete la imagen resultante con el
    nombre \`my-app\`.

7.  Ejecute la imagen de Docker: una vez que la imagen esté compilada,
    puede ejecutarla con el comando \`docker run\`:

docker run -p 8080:8080 my-app

![BrokenImage](./media/image85.png)

Este comando le indica a Docker que ejecute un contenedor a partir de la
imagen \`my-app\`, y que mapee el puerto 8080 dentro del contenedor al
puerto 8080 en la máquina host.

1.  **Pruebe la aplicación**: Finalmente, para verificar que su
    aplicación se esté ejecutando correctamente, puede enviar una
    solicitud a http://localhost:8080 en su navegador o usando una
    herramienta como curl:

curl http://localhost:8080

![A screenshot of a computer program Description automatically
generated](./media/image86.png)

Este comando envía una solicitud GET a su aplicación y muestra la
respuesta.  
Si su aplicación se está ejecutando correctamente, debería ver la
respuesta esperada.

Tenga en cuenta que estos comandos deben ejecutarse en su terminal, no
dentro del código de su aplicación Java.
