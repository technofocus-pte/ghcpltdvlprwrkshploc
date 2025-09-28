**Lab 21: Erstellen einer minimalen WebAPI mit .NET und einem
entsprechenden Docker-Image mit GitHub Copilot**

**Objektiv:**

Ziel ist es, mit Hilfe von GitHub Copilot eine Minimal WebAPI unter
Verwendung von .NET 7.0 und einem entsprechenden Docker-Image zu
erstellen. Hier verwenden wir so viel wie möglich GitHub Copilot.

Probieren Sie verschiedene Dinge aus und sehen Sie, was GitHub Copilot
für Sie tun kann, z. B. das Generieren einer Dockerfile oder einer
Klasse, das Hinzufügen von Kommentaren usw.

Bevor wir dieses Lab ausführen, installieren wir zunächst die
erforderlichen Softwarepakete und richten die Umgebung ein

Übung 0: Installieren und Einrichten der Umgebung

Sie müssen die folgenden Softwarepakete herunterladen und installieren,
um die Umgebung zum Ausführen dieses Labs einzurichten.

• dotnet-sdk-8.0

1.  Öffnen Sie den Edge-Browser.

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image1.jpeg)

2.  Kopieren Sie in das URL-Feld des Browsers den Link zum Herunterladen
    des Softwarepakets auf Ihre Lab-VM und fügen Sie ihn ein.

dotnet-sdk-8.0 ◊
https://dotnet.microsoft.com/en-us/download/dotnet/thank-you/sdk-8.0.401-windows-x64-installer

**Hinweis:** Standardmäßig werden die Pakete im **Downloads**-Ordner
gespeichert.

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image2.jpeg)

3.  Installieren von .NET SDK Wechseln Sie zum Ordner **Downloads**
    (**C:\Users\Admin\Downloads**), doppelklicken Sie auf
    **dotnet-sdk-8.0.401,** und führen Sie den Installationsvorgang aus.

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image3.jpeg)

**Übung 1: Einrichten des Projekts in VS Code**

1.  Öffnen Sie **Visual Studio Code** über das **Start** Menü.

![Ein Screenshot eines Computers Beschreibung wird automatisch
generiert](./media/image4.png)

2.  Wählen Sie **File** -\> **Open Folder...** aus

![Ein Screenshot eines Computers Beschreibung wird automatisch
generiert](./media/image5.png)

3.  Wählen Sie den **CopilotHackathon**-Ordner aus **C:\Labfiles** aus
    und klicken Sie auf **Select Folder**.

![Defektes Bild](./media/image6.png)

4.  Klicken Sie auf **Yes, I trust the authors**.

![Ein Screenshot eines Computers Beschreibung wird automatisch
generiert](./media/image7.png)

**Übung 2: Einführung**

**Hinweis:** Der von Copilot generierte Code kann bei verschiedenen
Ausführungen unterschiedlich sein. In den Schritten, in denen es um die
Codegenerierung geht, haben wir den **Referenzcode** angegeben. Bitte
verwenden Sie dies, um die Richtigkeit des von Copilot generierten Codes
zu überprüfen oder um eventuelle Fehler zu beheben.

1.  Öffnen Sie **Program.cs** von **dotnet** -\> **MinimalAPI.**

![Defektes Bild](./media/image8.png)

2.  Geben Sie in **MinimalAPI\Program.cs** nach der Zeile **// ADD NEW
    ENDPOINTS HERE**(Zeilennummer 19) // Hello World Get endpoint ein
    und drücken Sie die **Enter**-Taste. Der Copilot schlägt den Code in
    Grau vor.

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image9.png)

3.  Sobald Sie den von Copilot generierten Code erhalten haben, können
    Sie ihn **akzeptieren** oder **verwerfen**. Um zu akzeptieren,
    klicken Sie auf die **Ctrl-**Schaltfläche und die Optionsleiste wird
    über dem grauen Text angezeigt. Eine andere Möglichkeit besteht
    darin, einfach die **Tab**-Taste zu drücken.

**Referenzcode :** app.MapGet("/", () =\> "Hello World!");

![Defektes Bild](./media/image10.png)

4.  Der Code sieht nun wie folgt aus. **Speichern Sie** die Datei.

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image11.png)

5.  Klicken Sie mit der rechten Maustaste auf den Ordner **dotnet**, und
    wählen Sie **Open in Integrated Terminal** aus.

![Ein Screenshot eines Computers Beschreibung wird automatisch
generiert](./media/image12.png)

6.  Führen Sie im Terminal den folgenden Befehl aus.

dotnet test

![Ein Screenshot eines Computerbildschirms Beschreibung wird automatisch
generiert](./media/image13.png)

**Übung 3: Erstellen neuer Funktionalitäten**

1.  Fügen Sie neben dem Endpunkt Hello World **DaysBetweenDates** hinzu.

2.  Drücken Sie **Ctrl+I**, um Copilot inline zu öffnen.

3.  Geben Sie den folgenden Text ein und klicken Sie auf die
    Schaltfläche **Send**.

4.  /DaysBetweenDates:

5.  Berechnen Sie die Tage zwischen zwei Daten

Empfangen Sie per Abfragezeichenfolge die beiden Parameter date1 und
date2, und berechnen Sie die Tage zwischen diesen beiden Daten.

![Ein Screenshot eines Computers Beschreibung wird automatisch
generiert](./media/image14.png)

6.  Der Copilot generiert nun **Code** und trägt ihn in die
    **Program.cs**-Datei ein. Sobald Sie fertig sind, sehen Sie zwei
    Optionen zum **Accept** oder **Discard**. **Akzeptieren Sie** den
    Code.

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image15.png)

7.  Wählen Sie nach der Annahme den generierten Code aus, und drücken
    Sie **Ctrl+I.** Geben Sie ein, konvertieren Sie diesen Code in eine
    einzelne Zeile und drücken Sie die **Enter**-Taste. Klicken Sie auf
    **Accept**, sobald der Code in eine einzelne Zeile umgewandelt
    wurde.

**Referenzcode** -
app.MapGet("/DaysBetweenDates", (DateTime date1, DateTime date2) =\> (date2 - date1).Days.ToString());

![Ein Screenshot eines Computers Beschreibung wird automatisch
generiert](./media/image16.png)

8.  Geben Sie die folgenden Anweisungen ein (kommentiert) und klicken
    Sie auf **Enter**.

Klicken Sie auf Accept, um den vom Copilot generierten Code zu
akzeptieren.

/\*

/validatephonenumber:

receive by querystring a parameter called phoneNumber

validate phoneNumber with Spanish format, for example +34666777888

if phoneNumber is valid return true

\*/

**Referenz-Code:**

app.MapGet("/validatephonenumber", (string phonenumber) =\> Regex.IsMatch(phonenumber, @"^(\\\[0-9\]{9})$").ToString());

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image17.png)

9.  Fügen Sie den folgenden Text wie in der Copilot-Inline-Funktion in
    die Program.cs-Datei ein und drücken Sie die **Enter**-Taste.

10. /validatespanishdni:

11. receive by querystring a parameter called dni

12. calculate DNI letter

13. if DNI is valid return "valid"

if DNI is not valid return "invalid"

In diesem Fall können Sie mehrere Lösungen von Copilot sehen, um
diejenige auszuwählen, die am besten zur Berechnung des Buchstabens
passt. Um die ersten 10 Vorschläge von Copilot zu sehen, drücken Sie
Ctrl + Enter.

Akzeptieren Sie den von GitHub generierten Code.

**Referenz-Code:**

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

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image18.png)

14. Wählen Sie im linken Fensterbereich **Chat** aus.

![Ein Screenshot eines Computers Beschreibung wird automatisch
generiert](./media/image19.png)

15. Geben Sie den folgenden Text ein und klicken Sie auf die
    **Enter**-Taste.

16. /returncolorcode:

receive by querystring a parameter called color read colors.json file
and return the rgba field get color var from querystring iterate for
each color in colors.json to find the color return the code.hex field

![Ein schwarzer Bildschirm mit weißem Text Beschreibung wird automatisch
generiert](./media/image20.png)

17. Achten Sie darauf, dass der Copilot detaillierte Schritte und dann
    den generierten **Code** angibt. Platzieren Sie den Cursor in der
    Program.cs Datei nach dem Code **validatespanishdni**. Klicken Sie
    auf das **Symbol “Insert at cursor”**, um den Code in die Datei
    einzufügen.

**Referenz-Code:**

app.MapGet("/color", (string color) =\>

{

var colors =
JsonSerializer.Deserialize\<Color\[\]\>(File.ReadAllText("colors.json"));

return colors.First(c =\> c.Name == color).Code.HEX;

});

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image21.png)

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image22.png)

18. Stellen Sie sicher, dass der generierte Code keine Fehler enthält.
    Wenn ein Fehler vorhanden ist, behalten Sie den Referenzcode als
    Referenz bei, und korrigieren Sie den Code.

19. In diesem Fall tritt der Fehler **Color does not contain definition
    for code auf**.

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image23.png)

20. Der generierte Code wird wie folgt aktualisiert, um die Fehler zu
    beheben.

![Ein Screenshot eines Computers Beschreibung wird automatisch
generiert](./media/image24.png)

21. Geben Sie den folgenden Text ein und drücken Sie die Eingabetaste
    und überprüfen und den von Copilot generierten Code akzeptieren.

22. /\*

23. /tellmeajoke:

24. Make a call to the joke api and return a random joke

\*/

**Referenz-Code:**

app.MapGet("/tellmeajoke", async () =\> {

var client = new HttpClient();

var response = await
client.GetAsync("https://official-joke-api.appspot.com/jokes/random");

var joke = await response.Content.ReadAsStringAsync();

return joke;

});

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image25.png)

HINWEIS: Dies ist ein Beispiel, bei dem Sie möglicherweise Ihr eigenes
Wissen und Urteilsvermögen einsetzen müssen, um zu überprüfen, ob
Copilot Best Practices befolgt. Nur weil Copilot das nachahmt, was viele
Entwickler tun, heißt das nicht immer, dass es der richtige Weg ist.
Möglicherweise müssen Sie in Ihrer Prompt besonders spezifisch sein, um
Copilot über die Best Practices zu informieren. Tipp: Achten Sie auf
HttpClient.

25. Copilot kann Ihnen helfen, neue Frameworks zu erlernen.

Geben Sie den folgenden Text in Copilot inline ein und drücken Sie die
**Enter**-Taste.

/parseurl:

Retrieves a parameter from querystring called someurl

Parse the url and return the protocol, host, port, path, querystring and
hash

Return the parsed host

**Referenz-Code:**

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

![Ein Screenshot eines Computers Beschreibung wird automatisch
generiert](./media/image26.png)

26. Copilot kann auch bei dieser Art von Befehlen vor Ort helfen. Die
    Funktion wird in der CLI als Copilot bezeichnet. Weitere
    Informationen zu dieser Funktion finden Sie hier.

Öffnen Sie Copilot Inline, geben Sie den folgenden Text ein und drücken
Sie die **Enter-**Taste.

/listfiles:

Get the current directory

Get the list of files in the current directory

Return the list of files

**Referenz-Code:**

app.MapGet("/listfiles", () =\> {

var currentDirectory = Directory.GetCurrentDirectory();

var files = Directory.GetFiles(currentDirectory);

return files;

});

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image27.png)

27. Geben Sie den folgenden Text in Inline Copilot ein und drücken Sie
    die **Enter-**Taste.

28. /calculatememoryconsumption:

Return the memory consumption of the process in GB, rounded to 2
decimals

**Referenz-Code:**

// Calculate memory consumption endpoint

app.MapGet("/calculatememoryconsumption", () =\>

{

var process = System.Diagnostics.Process.GetCurrentProcess();

var memoryUsage = process.WorkingSet64 / (1024.0 \* 1024 \* 1024); //
Convert to GB

return Math.Round(memoryUsage, 2);

});

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image28.png)

29. Geben Sie den folgenden Text in Copilot inline ein und drücken Sie
    die **Enter-**Taste.

30. /randomeuropeancountry:

31. Make an array of european countries and its iso codes

32. Return a random country from the array

Return the country and its iso code

**Referenz-Code:**

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

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image29.png)

**Übung 4: Dokumentieren des Codes**

1.  Öffnen Sie das Chat-Fenster.

![Ein Screenshot eines Computers Beschreibung wird automatisch
generiert](./media/image19.png)

2.  Geben Sie “**Document the Program.cs file**” ein, und wählen Sie
    **Send** aus.

GitHub Copiot generiert eine kurze **Dokumentation** der
**Program.cs**-Datei.

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image30.png)

**Übung 5: Erstellen von Tests**

1.  Öffnen Sie **Program.cs**-Datei.

2.  Wählen Sie den Endpunkt **DaysBetweenDates** aus, und drücken Sie
    **Ctrl+I**, um Copilot Inline zu öffnen.

Geben Sie in der Copilot-Inline-Datei **/tests** ein und klicken Sie auf
die Schaltfläche **Send**.

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image31.png)

3.  Kopieren Sie den generierten Test.

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image32.png)

4.  Öffnen Sie die IntegrationTests.cs über MinimalAPI.Tests.

![Ein Screenshot eines Computers Beschreibung wird automatisch
generiert](./media/image33.png)

5.  Fügen Sie es in die cs-Datei nach dem Testblock von Hello World ein.
    Beheben Sie alle Probleme, die auftreten könnten.

6.  Öffnen Sie den Copilot-Chat im linken Fensterbereich.

![Ein Screenshot eines Computers Beschreibung wird automatisch
generiert](./media/image19.png)

7.  Geben Sie /tests ein, den Befehl zum Erstellen von Testeinheiten,
    und drücken Sie die **Enter**-Taste. Der Copilot generiert eine
    Testdatei. Kopieren Sie den Inhalt.

![Ein Screenshot eines Computers Beschreibung wird automatisch
generiert](./media/image34.png)

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image35.png)

8.  Öffnen Sie **IntegrationTests.cs** über die **MinimalAPI.Tests**.

![Ein Screenshot eines Computers Beschreibung wird automatisch
generiert](./media/image33.png)

9.  Ersetzen Sie den Inhalt der Datei durch den von Copilot generierten
    Code und speichern Sie.

**Wichtig:** Suchen Sie nach Fehlern und beheben Sie diese mit dem
Befehl /fix oder manuell. Verwenden Sie den untenstehenden Referenzcode
zur Fehlerbehebung.

10. Wenn die Tests nicht für alle Endpunkte generiert werden, geben Sie
    im Chat den Namen des Endpunkts an und bitten Sie Copilot, den Test
    wie folgt zu generieren. Aktualisieren Sie die Endpunktnamen, je
    nachdem, welche aktualisiert wurden und welche im Test fehlen.

generate test units for moviesbydirector, parseurl, listfiles,
calculatememoryconsumption and randomeuropeancountry

**Referenz-Code:**

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

![Ein Screenshot eines Computerprogramms Beschreibung automatisch
generiert](./media/image36.png)

11. Führen Sie im Terminal den Befehl **dotnet test** aus.

12. Wenn der Test erfolgreich ist, sollte die Ausgabe ähnlich der im
    folgenden Screenshot angezeigt werden.

![Defektes Bild](./media/image37.png)

13. Sie können bei Bedarf weitere Tests hinzufügen.

**Übung 6: Erstellen einer Dockerfile**

1.  Klicken Sie mit der rechten Maustaste auf den Ordner **dotnet**,
    wählen Sie **New File** aus, und benennen Sie die Datei als
    **Dockerfile**.

![Defektes Bild](./media/image38.png)

2.  Benennen Sie die Datei als **Dockerfile**.

![Ein Screenshot eines Computers Beschreibung wird automatisch
generiert](./media/image39.png)

3.  Drücken Sie in der neu erstellten Datei **Ctrl+I**, geben Sie den
    folgenden Text ein und drücken Sie die **Enter**-Taste.

**Generieren von Inhalten für Dockerfile für .NET 8 Projektname -
MinimalAPI**

![Ein Screenshot eines Computers Beschreibung wird automatisch
generiert](./media/image40.png)

4.  Akzeptieren Sie den generierten Code.

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image41.png)

5.  Speichern Sie die Datei. Führen Sie im Terminal den folgenden Befehl
    aus.

docker build -t dotnetapp .

Verwenden Sie den Referenzcode, um ggf. Fehler zu beheben.

**Referenz-Code:**

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

![Defektes Bild](./media/image42.png)

6.  Führen Sie den folgenden Befehl aus, um die App auf Port 8080
    auszuführen

docker run -d -p 8080:80 --name dotnetapp dotnetapp

![Defektes Bild](./media/image43.png)

7.  Jetzt wird die dotnet-App im Docker ausgeführt.

![Ein Screenshot eines Computers Beschreibung wird automatisch
generiert](./media/image44.png)
