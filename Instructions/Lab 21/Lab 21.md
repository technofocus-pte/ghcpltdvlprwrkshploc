**Laboratorio 21 - Crear una WebAPI mínima con .NET y una imagen Docker
correspondiente usando GitHub Copilot**

**Objetivo:**

El objetivo es crear una WebAPI mínima usando .NET 7.0 y una imagen
Docker correspondiente con la ayuda de GitHub Copilot. En este
ejercicio, usaremos GitHub Copilot tanto como sea posible.

Pruebe diferentes cosas y vea lo que GitHub Copilot puede hacer por
usted, como generar un Dockerfile o una clase, agregar comentarios, etc.

Antes de ejecutar este laboratorio, primero instalemos los paquetes de
software necesarios y configuremos el entorno.

Ejercicio 0: Instalación y configuración del entorno

Debe descargar e instalar los siguientes paquetes de software para
configurar el entorno y ejecutar este laboratorio.

• dotnet-sdk-8.0

1.  Abra el navegador Edge.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image1.jpeg)

2.  En el campo de URL del navegador, copie y pegue el enlace para
    descargar el paquete de software en su máquina virtual de
    laboratorio.

dotnet-sdk-8.0
◊ https://dotnet.microsoft.com/en-us/download/dotnet/thank-you/sdk-8.0.401-windows-x64-installer

**Nota:** De forma predeterminada, los paquetes se guardarán en la
carpeta de **downloads**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image2.jpeg)

3.  Instale el SDK de .NET  
    Vaya a la carpeta de **Downloads (C:\Users\Admin\Downloads)** y haga
    doble clic en **dotnet-sdk-8.0.401**. Luego, siga el proceso de
    instalación.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image3.jpeg)

**Ejercicio 1: Configurar el proyecto en VS Code**

1.  Abra **Visual Studio Code** desde el menú **Start**.

![A screenshot of a computer Description automatically
generated](./media/image4.png)

2.  Seleccione **File** -\> **Open Folder…**

![A screenshot of a computer Description automatically
generated](./media/image5.png)

3.  Seleccione la carpeta **CopilotHackathon** desde **C:\Labfiles** y
    haga clic en **Select Folder**.

![BrokenImage](./media/image6.png)

4.  Haga clic en **Yes, I trust the authors**.

![A screenshot of a computer Description automatically
generated](./media/image7.png)

**Ejercicio 2: Introducción**

**Nota:** El código generado por Copilot puede variar en cada ejecución.
En los pasos que implican generación de código a continuación, se ha
proporcionado el **código de referencia**. Utilícelo para verificar que
el código generado por Copilot sea correcto o para resolver errores, en
caso de que los haya.

1.  Abra **Program.cs** desde **dotnet** -\> **MinimalAPI**.

![BrokenImage](./media/image8.png)

2.  Dentro de **MinimalAPI\Program.cs** después de la línea **// ADD NEW
    ENDPOINTS HERE** (línea número 19), escriba // Hello World Get
    endpoint y presione **Enter.** Copilot sugerirá el código en gris.

![A screenshot of a computer program Description automatically
generated](./media/image9.png)

3.  Una vez que obtenga el código generado por Copilot, puede
    **aceptarlo** o **descartarlo**. Para aceptarlo, haga clic en el
    botón **Ctrl** y aparecerá una barra de opciones sobre el texto en
    gris. Otra opción es simplemente presionar la tecla **Tab**.

**Código de referencia:** app.MapGet("/", () =\> "Hello World!");

![BrokenImage](./media/image10.png)

4.  El código ahora se verá así. **Guarde** el archivo.

![A screenshot of a computer program Description automatically
generated](./media/image11.png)

5.  Haga clic derecho en la carpeta **dotnet** y seleccione **Open in
    Integrated Terminal**.

![A screenshot of a computer Description automatically
generated](./media/image12.png)

6.  Desde la terminal, ejecute el siguiente comando.

dotnet test

![A screenshot of a computer screen Description automatically
generated](./media/image13.png)

**Ejercicio 3: Crear nuevas funcionalidades**

1.  Al lado del endpoint Hello World, agregue **DaysBetweenDates.**

2.  Presione **Ctrl+I** para abrir la función Copilot inline.

3.  Ingrese el siguiente texto y haga clic en el botón **Send**.

4.  /DaysBetweenDates:

5.  calcular los días entre dos fechas

Reciba mediante *query string* dos parámetros date1 y date2, y calcule
los días entre esas dos fechas.

![A screenshot of a computer Description automatically
generated](./media/image14.png)

6.  Copilot ahora genera el código y lo ingresa en el archivo
    **Program.cs**. Una vez hecho esto, verá dos opciones: **Accept** o
    **Discard**. Acepte el código hacienda clic en **Accept**.

![A screenshot of a computer program Description automatically
generated](./media/image15.png)

7.  Una vez aceptado, seleccione el código generado y presione
    **Ctrl+I.** Ingrese, Convert this code into a single line y
    presione **Enter**. Haga clic en Accept una vez que el código se
    haya convertido en una sola línea.

**Referencia
code** - app.MapGet("/DaysBetweenDates", (DateTime date1, DateTime date2) =\> (date2 - date1).Days.ToString());

![A screen shot of a computer Description automatically
generated](./media/image16.png)

8.  Ingrese las siguientes instrucciones (comentadas) y presione
    **Enter**.

Haga clic en Accept para aceptar el código generado por Copilot.

/\*

/validatephonenumber:

receive by querystring a parameter called phoneNumber

validate phoneNumber with Spanish format, for example +34666777888

if phoneNumber is valid return true

\*/

**Código de referencia:**

app.MapGet("/validatephonenumber", (string phonenumber) =\> Regex.IsMatch(phonenumber, @"^(\\\[0-9\]{9})$").ToString());

![A screenshot of a computer program Description automatically
generated](./media/image17.png)

9.  Agregue el texto a continuación usando la función Copilot inline en
    el archivo Program.cs y presione **Enter**.

10. /validatespanishdni:

11. receive by querystring a parameter called dni

12. calculate DNI letter

13. if DNI is valid return "valid"

if DNI is not valid return "invalid"

En este caso, es posible que desee ver varias soluciones de Copilot para
elegir la que mejor se adapte a la forma de calcular la letra. Para ver
las primeras 10 sugerencias de Copilot, presione Ctrl + Enter.

Acepte el código generado por GitHub.

**Código de referencia:**

app.MapGet("/validatespanishdni", (string dni) =\> {

var valid = false;

if (dni.Length == 9 && int.TryParse(dni.Substring(0, 8), out int
number))

{

var letters = "TRWAGMYFPDXBNJZSQVHLCKE";

var letter = letters\[number % 23\];

valid = dni.EndsWith(letter.ToString());

}

return valid ? "valid" : "invalid";

});

![A screenshot of a computer program Description automatically
generated](./media/image18.png)

14. Seleccione **Chat** desde el panel izquierdo.

![A screenshot of a computer Description automatically
generated](./media/image19.png)

15. Ingrese el siguiente texto y haga clic en **Enter**.

16. /returncolorcode:

receive by querystring a parameter called color read colors.json file
and return the rgba field get color var from querystring iterate for
each color in colors.json to find the color return the code.hex field

![A black screen with white text Description automatically
generated](./media/image20.png)

17. Verifique que Copilot proporcione pasos detallados y luego genere el
    código.  
    Coloque el cursor en el archivo **Program.cs**, después del bloque
    de código **validatespanishdni**.  
    Haga clic en el icono **Insert at cursor** para pegar el código en
    el archivo.

**Código de referencia:**

app.MapGet("/color", (string color) =\>

{

var colors =
JsonSerializer.Deserialize\<Color\[\]\>(File.ReadAllText("colors.json"));

return colors.First(c =\> c.Name == color).Code.HEX;

});

![A screenshot of a computer program Description automatically
generated](./media/image21.png)

![A screenshot of a computer program Description automatically
generated](./media/image22.png)

18. Asegúrese de que no haya errores en el código generado. Si existe
    algún error, utilice el reference code como referencia para corregir
    el código.

19. En este caso, hay un error, **Color does not contain definition for
    code**.

![A screenshot of a computer program Description automatically
generated](./media/image23.png)

20. El código generado se actualiza como se muestra a continuación para
    corregir los errores.

![A screen shot of a computer Description automatically
generated](./media/image24.png)

21. Ingrese el texto que aparece a continuación y presione Enter, luego
    revise y acepte el código generado por Copilot.

22. /\*

23. /tellmeajoke:

24. Make a call to the joke api and return a random joke

\*/

**Código de referencia:**

app.MapGet("/tellmeajoke", async () =\> {

var client = new HttpClient();

var response = await
client.GetAsync("https://official-joke-api.appspot.com/jokes/random");

var joke = await response.Content.ReadAsStringAsync();

return joke;

});

![A screenshot of a computer program Description automatically
generated](./media/image25.png)

NOTA: Este es un ejemplo donde puede que necesite usar su propio
conocimiento y criterio para validar que Copilot siga las prácticas
recomendadas. El hecho de que Copilot imite lo que hacen muchos
desarrolladores no siempre significa que sea la manera correcta. Puede
que necesite ser más específico en su instrucción para hacerle saber a
Copilot cuáles son las prácticas recomendadas. Sugerencia: Preste
atención a HttpClient.

25. Copilot puede ayudarle a aprender nuevos frameworks.

Escriba el siguiente texto en Copilot Inline y presione **Enter**.

/parseurl:

Retrieves a parameter from querystring called someurl

Parse the url and return the protocol, host, port, path, querystring and
hash

Return the parsed host

**Código de referencia:**

app.MapGet("/parseurl", (string someurl) =\> {

var uri = new Uri(someurl);

var host = uri.Host;

var protocol = uri.Scheme;

var port = uri.Port;

var path = uri.AbsolutePath;

var query = uri.Query;

var hash = uri.Fragment;

return host;

});

![A screen shot of a computer Description automatically
generated](./media/image26.png)

26. Copilot también puede ayudar con este tipo de comandos de forma
    local. La funcionalidad se llama Copilot in the CLI. Puede obtener
    más información sobre esta función aquí.

Abra Copilot Inline, ingrese el siguiente texto y presione **Enter**.

/listfiles:

Get the current directory

Get the list of files in the current directory

Return the list of files

**Código de referencia:**

app.MapGet("/listfiles", () =\> {

var currentDirectory = Directory.GetCurrentDirectory();

var files = Directory.GetFiles(currentDirectory);

return files;

});

![A screenshot of a computer program Description automatically
generated](./media/image27.png)

27. Ingrese el siguiente texto en Copilot Inline y presione **Enter**.

28. /calculatememoryconsumption:

Devuelve el consumo de memoria del proceso en GB, redondeado a 2
decimales

**Código de referencia:**

// Calculate memory consumption endpoint

app.MapGet("/calculatememoryconsumption", () =\>

{

var process = System.Diagnostics.Process.GetCurrentProcess();

var memoryUsage = process.WorkingSet64 / (1024.0 \* 1024 \* 1024); //
Convert to GB

return Math.Round(memoryUsage, 2);

});

![A screenshot of a computer program Description automatically
generated](./media/image28.png)

29. Ingrese el siguiente texto en Copilot inline y presione **Enter**.

30. /randomeuropeancountry:

31. Make an array of european countries and its iso codes

32. Return a random country from the array

Return the country and its iso code

**Código de referencia:**

// Random European Country endpoint

app.MapGet("/randomeuropeancountry", () =\>

{

var europeanCountries = new Dictionary\<string, string\>

{

{ "Albania", "AL" },

{ "Andorra", "AD" },

{ "Austria", "AT" },

{ "Belarus", "BY" },

{ "Belgium", "BE" },

{ "Bosnia and Herzegovina", "BA" },

{ "Bulgaria", "BG" },

{ "Croatia", "HR" },

{ "Cyprus", "CY" },

{ "Czech Republic", "CZ" },

{ "Denmark", "DK" },

{ "Estonia", "EE" },

{ "Finland", "FI" },

{ "France", "FR" },

{ "Germany", "DE" },

{ "Greece", "GR" },

{ "Hungary", "HU" },

{ "Iceland", "IS" },

{ "Ireland", "IE" },

{ "Italy", "IT" },

{ "Kosovo", "XK" },

{ "Latvia", "LV" },

{ "Liechtenstein", "LI" },

{ "Lithuania", "LT" },

{ "Luxembourg", "LU" },

{ "Malta", "MT" },

{ "Moldova", "MD" },

{ "Monaco", "MC" },

{ "Montenegro", "ME" },

{ "Netherlands", "NL" },

{ "North Macedonia", "MK" },

{ "Norway", "NO" },

{ "Poland", "PL" },

{ "Portugal", "PT" },

{ "Romania", "RO" },

{ "Russia", "RU" },

{ "San Marino", "SM" },

{ "Serbia", "RS" },

{ "Slovakia", "SK" },

{ "Slovenia", "SI" },

{ "Spain", "ES" },

{ "Sweden", "SE" },

{ "Switzerland", "CH" },

{ "Ukraine", "UA" },

{ "United Kingdom", "GB" },

{ "Vatican City", "VA" }

};

var random = new Random();

var index = random.Next(europeanCountries.Count);

var country = europeanCountries.ElementAt(index);

return $"{country.Key} ({country.Value})";

});

![A screenshot of a computer program Description automatically
generated](./media/image29.png)

**Ejercicio 4: Documentar el código**

1.  Abra la ventana de chat.

![A screenshot of a computer Description automatically
generated](./media/image19.png)

2.  Escriba, **Document the Program.cs file** y seleccione **Send**.

GitHub Copilot genera una **documentación** breve del archivo
**Program.cs**.

![A screenshot of a computer program Description automatically
generated](./media/image30.png)

**Ejercicio 5: Crear pruebas (tests)**

1.  Abra el archivo **Program.cs**.

2.  Seleccione el endpoint **DaysBetweenDates**, presione **Ctrl+I**
    para abrir la función inline de Copilot.

En la función inline de Copilot, escriba **/tests** y haga clic en el
botón **Send**.

![A screenshot of a computer program Description automatically
generated](./media/image31.png)

3.  Copie la prueba generada.

![A screenshot of a computer program Description automatically
generated](./media/image32.png)

4.  Abra el archivo IntegrationTests.cs desde MinimalAPI.Tests.

![A screenshot of a computer Description automatically
generated](./media/image33.png)

5.  Pegue el código en el archivo .cs después del bloque de prueba de
    Hello World. Resuelva cualquier problema que pueda surgir.

6.  Abra el chat de Copilot desde el panel izquierdo.

![A screenshot of a computer Description automatically
generated](./media/image19.png)

7.  Escriba /tests, el comando para crear pruebas unitarias, y presione
    **Enter**. Copilot generará un archivo de prueba. Copie su
    contenido.

![A screenshot of a computer Description automatically
generated](./media/image34.png)

![A screenshot of a computer program Description automatically
generated](./media/image35.png)

8.  Abra **IntegrationTests.cs** desde **MinimalAPI.Tests**.

![A screenshot of a computer Description automatically
generated](./media/image33.png)

9.  Reemplace el contenido del archivo con el código generado por
    Copilot y guarde los cambios.

**Importante:** Verifique si hay errores y corríjalos usando el comando
/fix o de forma manual. Utilice el código de referencia a continuación
para solucionar problemas.

10. Si no se generaron pruebas para todos los endpoints, desde el chat
    especifique el nombre del endpoint y pídale a Copilot que genere la
    prueba como se muestra a continuación. Actualice los nombres de los
    endpoints según los que se hayan agregado o los que falten en su
    prueba.

generate test units for moviesbydirector, parseurl, listfiles,
calculatememoryconsumption and randomeuropeancountry

**Código de referencia:**

using System;

using System.Net.Http;

using System.Threading.Tasks;

using Microsoft.AspNetCore.Mvc.Testing;

using Xunit;

public class EndpointTests :
IClassFixture\<WebApplicationFactory\<Program\>\>

{

private readonly WebApplicationFactory\<Program\> \_factory;

private readonly HttpClient \_client;

public EndpointTests(WebApplicationFactory\<Program\> factory)

{

\_factory = factory;

\_client = \_factory.CreateClient();

}

\[Fact\]

public async Task Get_HelloWorld_ReturnsHelloWorld()

{

var response = await \_client.GetAsync("/");

response.EnsureSuccessStatusCode();

var stringResponse = await response.Content.ReadAsStringAsync();

Assert.Equal("Hello World!", stringResponse);

}

\[Fact\]

public async Task Get_ValidatePhoneNumber_ReturnsInvalid()

{

var response = await
\_client.GetAsync("/validatephonenumber?phonenumber=123456789");

response.EnsureSuccessStatusCode();

var stringResponse = await response.Content.ReadAsStringAsync();

Assert.Equal("False", stringResponse);

}

\[Fact\]

public async Task Get_ValidateSpanishDni_ReturnsValid()

{

var response = await
\_client.GetAsync("/validatespanishdni?dni=12345678Z");

response.EnsureSuccessStatusCode();

var stringResponse = await response.Content.ReadAsStringAsync();

Assert.Equal("valid", stringResponse);

}

\[Fact\]

public async Task Get_Color_ReturnsHexCode()

{

var response = await \_client.GetAsync("/color?color=red");

response.EnsureSuccessStatusCode();

var stringResponse = await response.Content.ReadAsStringAsync();

Assert.Equal("#FF0000", stringResponse); // assuming red color returns
\#FF0000

}

\[Fact\]

public async Task Get_TellMeAJoke_ReturnsJoke()

{

var response = await \_client.GetAsync("/tellmeajoke");

response.EnsureSuccessStatusCode();

var stringResponse = await response.Content.ReadAsStringAsync();

Assert.NotNull(stringResponse); // assuming the joke API always returns
a joke

}

\[Fact\]

public async Task Get_ParseUrl_ReturnsHost()

{

var response = await
\_client.GetAsync("/parseurl?someurl=https://www.example.com");

response.EnsureSuccessStatusCode();

var stringResponse = await response.Content.ReadAsStringAsync();

Assert.Equal("www.example.com", stringResponse);

}

\[Fact\]

public async Task Get_ListFiles_ReturnsFiles()

{

var response = await \_client.GetAsync("/listfiles");

response.EnsureSuccessStatusCode();

var stringResponse = await response.Content.ReadAsStringAsync();

Assert.NotNull(stringResponse); // assuming the API always returns a
list of files

}

\[Fact\]

public async Task Get_CalculateMemoryConsumption_ReturnsMemoryUsage()

{

var response = await \_client.GetAsync("/calculatememoryconsumption");

response.EnsureSuccessStatusCode();

var stringResponse = await response.Content.ReadAsStringAsync();

Assert.NotNull(stringResponse); // assuming the API always returns a
memory usage

}

\[Fact\]

public async Task Get_RandomEuropeanCountry_ReturnsCountry()

{

var response = await \_client.GetAsync("/randomeuropeancountry");

response.EnsureSuccessStatusCode();

var stringResponse = await response.Content.ReadAsStringAsync();

Assert.NotNull(stringResponse); // assuming the API always returns a
country

}

// Add similar tests for the other endpoints

}

![A screen shot of a computer program Description automatically
generated](./media/image36.png)

11. Desde la terminal, ejecute el comando, **dotnet test**

12. Si la prueba se aprueba, debería ver una salida similar a la que se
    muestra en la captura de pantalla a continuación.

![BrokenImage](./media/image37.png)

13. Puede agregar más pruebas si es necesario.

**Ejercicio 6: Crear un Dockerfile**

1.  Haga clic derecho en la carpeta **dotnet** y seleccione **New
    file**, luego asígnele el nombre **Dockerfile**.

![BrokenImage](./media/image38.png)

2.  Nombre el archive como **Dockerfile**.

![A screenshot of a computer Description automatically
generated](./media/image39.png)

3.  En el archivo recién creado, presione **Ctrl+I**, escriba el
    siguiente texto y presione **Enter**.

**Generate content for Dockerfile for .NET 8 Project Name - MinimalAPI**

![A screenshot of a computer Description automatically
generated](./media/image40.png)

4.  Acepte el código generado.

![A screenshot of a computer program Description automatically
generated](./media/image41.png)

5.  Guarde el archivo. Desde la terminal, ejecute el siguiente comando.

docker build -t dotnetapp .

Utilice el código de referencia para resolver errores, si los hay.

**Código de referencia:**

\# Use the official .NET SDK image as the base image

FROM mcr.microsoft.com/dotnet/sdk:8.0 AS build

\# Set the working directory in the container

WORKDIR /app

\# Copy the project file(s) to the container

COPY \*.csproj ./

\# Copy the remaining source code to the container

COPY . ./

\# Build the application

RUN dotnet build -c Release

\# Publish the application

RUN dotnet publish -c Release --no-build -o out

\# Use the official .NET runtime image as the base image for the final
stage

FROM mcr.microsoft.com/dotnet/runtime:8.0 AS runtime

\# Set the working directory in the container

WORKDIR /app

\# Copy the published output from the build stage to the final stage

COPY --from=build /app/out ./

\# Set the entry point for the container

ENTRYPOINT \["dotnet", "MinimalAPI.dll"\]

![BrokenImage](./media/image42.png)

6.  Ejecute el siguiente comando para ejecutar la aplicación en el
    puerto 8080

docker run -d -p 8080:80 --name dotnetapp dotnetapp

![BrokenImage](./media/image43.png)

7.  Ahora, tenemos la aplicación de .NET ejecutándose en Docker.

![A screenshot of a computer Description automatically
generated](./media/image44.png)
