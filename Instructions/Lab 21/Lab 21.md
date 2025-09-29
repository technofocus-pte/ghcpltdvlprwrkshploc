**Lab 21 - Creare un Minimal WebAPI usando .NET e un'immagine Docker
corrispondente con GitHub Copilot**

**Obiettivo:**

L'obiettivo è creare un Minimal WebAPI utilizzando .NET 7.0 e
un'immagine Docker corrispondente con l'aiuto di GitHub Copilot. In
questo caso, utilizziamo GitHub Copilot il più possibile.

Prova cose diverse e vedere cosa può fare GitHub Copilot per voi, come
generare un Dockerfile o una classe, aggiungere commenti, ecc.

Prima di eseguire questo laboratorio, installiamo i pacchetti software
necessari e configuriamo l'ambiente

Esercizio 0: Installazione e configurazione dell'ambiente

È necessario scaricare e installare i seguenti pacchetti software per
configurare l'ambiente per l'esecuzione di questo lab.

• dotnet-sdk-8.0

1.  Aprire il browser Edge.

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image1.jpeg)

2.  Nel campo URL del browser copiare e incollare il collegamento per
    scaricare il pacchetto software nella macchina virtuale del lab.

dotnet-sdk-8.0 ◊
https://dotnet.microsoft.com/en-us/download/dotnet/thank-you/sdk-8.0.401-windows-x64-installer

**Nota:** Per impostazione predefinita, i pacchetti verranno salvati
nella cartella **downloads**.

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image2.jpeg)

3.  Installare .NET SDK Passare alla cartella **Downloads**
    (**C:\Users\Admin\Downloads**) e fare doppio clic su
    **dotnet-sdk-8.0.401** e seguire il processo di installazione.

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image3.jpeg)

**Esercizio 1: Configurare il progetto in VS Code**

1.  Aprire **Visual Studio Code** dal menu **Start**.

![Uno screenshot di un computer Descrizione generata
automaticamente](./media/image4.png)

2.  Selezionare **File -\> Open Folder…**

![Uno screenshot di un computer Descrizione generata
automaticamente](./media/image5.png)

3.  Selezionare la cartella **CopilotHackathon** da **C:\Labfiles** e
    fare clic su **Select Folder**.

![Immagine rotta](./media/image6.png)

4.  Cliccare su **Yes, I trust the authors**.

![Uno screenshot di un computer Descrizione generata
automaticamente](./media/image7.png)

**Esercizio 2: Introduzione**

**Nota:** Il codice generato da Copilot potrebbe differire in caso di
esecuzioni diverse. Nei passaggi in cui è coinvolta la generazione del
codice di seguito, abbiamo fornito il **Reference code**. Si prega di
utilizzarlo per verificare la correttezza del codice generato da Copilot
o per risolvere eventuali errori.

1.  Aprire **Program.cs** da **dotnet** -\> **MinimalAPI.**

![Immagine rotta](./media/image8.png)

2.  All'interno di **MinimalAPI\Program.cs** dopo la riga **// ADD NEW
    ENDPOINTS HERE** (riga numero 19), digitare // Hello World Get
    endpoint e premere **Enter.** Il Copilot suggerirà il codice in
    grigio.

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image9.png)

3.  Una volta ottenuto il codice generato da Copilot, puoi
    **accettarlo** o **scartarlo**. Per accettare, fare clic sul
    pulsante **Ctrl** e la barra delle opzioni apparirà sopra il testo
    grigio. Un'altra opzione è semplicemente premere il tasto **Tab**.

**Codice di riferimento :** app.MapGet("/", () =\> "Hello World!");

![Immagine rotta](./media/image10.png)

4.  Il codice sarà ora simile al seguente. **Salvare** il file.

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image11.png)

5.  Fare clic con il pulsante destro del mouse sulla cartella **dotnet**
    e selezionare **Open in Integrated Terminal**.

![Uno screenshot di un computer Descrizione generata
automaticamente](./media/image12.png)

6.  Dal terminale, eseguire il comando seguente.

dotnet test

![Uno screenshot dello schermo di un computer Descrizione generata
automaticamente](./media/image13.png)

**Esercizio 3: Creazione di nuove funzionalità**

1.  Accanto all'endpoint Hello World, aggiungere **DaysBetweenDates.**

2.  Premere **Ctrl+I** per aprire il Copilot in linea.

3.  Inserire il testo sottostante e premere il pulsante **Send**.

4.  /DaysBetweenDates:

5.  Calcolare i giorni tra due date

Ricevere tramite la stringa di query due parametri date1 e date2 e
calcolare i giorni tra queste due date.

![Uno screenshot di un computer Descrizione generata
automaticamente](./media/image14.png)

6.  Il Copilot ora genera **il codice** e lo inserisce nel file
    **Program.cs**. Una volta terminato, vedrai due opzioni per
    **accettare** o **scartare**. **Accept** il codice.

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image15.png)

7.  Una volta accettato, selezionare il codice generato e premere
    **Ctrl+I.** Invio, converti questo codice in una singola riga e
    premere **Enter**. Fare clic su **Accept** una volta che il codice è
    stato convertito in una singola riga.

**Codice di riferimento** -
app.MapGet("/DaysBetweenDates", (DateTime date1, DateTime date2) =\> (date2 - date1).Days.ToString());

![Una schermata di un computer Descrizione generata
automaticamente](./media/image16.png)

8.  Inserire le seguenti dichiarazioni (commentate) e fare clic su
    **Enter**.

Cliccare su **Accept** per accettare il codice generato dal Copilot.

/\*

/validatephonenumber:

receive by querystring a parameter called phoneNumber

validate phoneNumber with Spanish format, for example +34666777888

if phoneNumber is valid return true

\*/

**Codice di riferimento:**

app.MapGet("/validatephonenumber", (string phonenumber) =\> Regex.IsMatch(phonenumber, @"^(\\\[0-9\]{9})$").ToString());

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image17.png)

9.  Aggiungere il testo sottostante come nella funzione in linea di
    Copilot, nel file Program.cs e premere **Enter**.

10. /validatespanishdni:

11. receive by querystring a parameter called dni

12. calculate DNI letter

13. if DNI is valid return "valid"

if DNI is not valid return "invalid"

In questo caso, potresti voler vedere più soluzioni di Copilot per
scegliere quella che meglio si adatta al modo di calcolare la lettera.
Per vedere i primi 10 suggerimenti da Copilot premere ctrl + Enter.

Accettare il codice generato da GitHub.

**Codice di riferimento:**

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

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image18.png)

14. Selezionare **Chat** dal riquadro a sinistra.

![Uno screenshot di un computer Descrizione generata
automaticamente](./media/image19.png)

15. Inserire il testo sottostante e fare clic su **Enter**.

16. /returncolorcode:

Ricevere tramite querystring un parametro chiamato Color Read
colors.json file e restituire il campo RGBA Ottieni colore var da
queryString itera per ogni colore in colors.json per trovare il colore
restituire il campo code.hex

![Una schermata nera con testo bianco Descrizione generata
automaticamente](./media/image20.png)

17. Vedere che il Copilot fornisce un passaggio dettagliato e quindi il
    codice generato. Posizionare il cursore nel file Program.cs, dopo il
    codice **validatespanishdni**. Fare clic sull'icona **Insert at
    cursor** per incollare il codice nel file.

**Codice di riferimento:**

app.MapGet("/color", (string color) =\>

{

var colors =
JsonSerializer.Deserialize\<Color\[\]\>(File.ReadAllText("colors.json"));

return colors.First(c =\> c.Name == color).Code.HEX;

});

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image21.png)

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image22.png)

18. Assicurarsi che non vi siano errori nel codice generato. In caso di
    errore, conservare il codice di riferimento come riferimento e
    correggere il codice.

19. In questo caso, si verifica un errore, **Color does not contain
    definition for code**.

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image23.png)

20. Il codice generato viene aggiornato come di seguito per risolvere
    gli errori.

![Una schermata di un computer Descrizione generata
automaticamente](./media/image24.png)

21. Inserire il testo sottostante e premere Enter e rivedere e accettare
    il codice generato da Copilot.

22. /\*

23. /tellmeajoke:

24. Make a call to the joke api and return a random joke

\*/

**Codice di riferimento:**

app.MapGet("/tellmeajoke", async () =\> {

var client = new HttpClient();

var response = await
client.GetAsync("https://official-joke-api.appspot.com/jokes/random");

var joke = await response.Content.ReadAsStringAsync();

return joke;

});

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image25.png)

NOTA: questo è un esempio in cui potrebbe essere necessario utilizzare
le proprie conoscenze e il proprio giudizio per verificare che Copilot
segua le migliori pratiche. Solo perché Copilot imita ciò che fanno
molti sviluppatori, non significa sempre che sia il modo corretto.
Potrebbe essere necessario essere più specifici nel prompt per far
sapere a Copilot quali sono le migliori pratiche. Suggerimento: prestare
attenzione a HttpClient.

25. Copilot può aiutarti a imparare nuovi framework.

Immettere il testo seguente in Copilot in linea e premere **Enter**.

/parseurl:

Retrieves a parameter from querystring called someurl

Parse the url and return the protocol, host, port, path, querystring and
hash

Return the parsed host

**Codice di riferimento:**

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

![Una schermata di un computer Descrizione generata
automaticamente](./media/image26.png)

26. Copilot può anche aiutare con questo tipo di comandi in locale. La
    funzione è denominata Copilot nella CLI. Per ulteriori informazioni
    su questa funzione, fare clic qui.

Aprire Copilot Inline, inserire il testo sottostante e premere
**Enter**.

/listfiles:

Get the current directory

Get the list of files in the current directory

Return the list of files

**Codice di riferimento:**

app.MapGet("/listfiles", () =\> {

var currentDirectory = Directory.GetCurrentDirectory();

var files = Directory.GetFiles(currentDirectory);

return files;

});

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image27.png)

27. Inserire il testo seguente in copilot in linea e premere **Enter**.

28. /calculatememoryconsumption:

Return the memory consumption of the process in GB, rounded to 2
decimals

**Codice di riferimento:**

// Calculate memory consumption endpoint

app.MapGet("/calculatememoryconsumption", () =\>

{

var process = System.Diagnostics.Process.GetCurrentProcess();

var memoryUsage = process.WorkingSet64 / (1024.0 \* 1024 \* 1024); //
Convert to GB

return Math.Round(memoryUsage, 2);

});

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image28.png)

29. Immettere il testo seguente in Copilot in linea e premere **Enter**.

30. /randomeuropeancountry:

31. Make an array of european countries and its iso codes

32. Return a random country from the array

Return the country and its iso code

**Codice di riferimento:**

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

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image29.png)

**Esercizio 4: Documentare il codice**

1.  Aprire la finestra della chat.

![Uno screenshot di un computer Descrizione generata
automaticamente](./media/image19.png)

2.  Digitare, **Document the Program.cs file** e selezionare **Send**.

GitHubCopiot genera una breve **documentation **del file **Program.cs**.

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image30.png)

**Esercizio 5: Building tests**

1.  Aprire **Program.cs** file.

2.  Selezionare l'endpoint **DaysBetweenDates**, premere **CTRL+I** per
    aprire il Copilot inline.

Nel Copilot in linea, digitare **/tests** e fare clic sul pulsante
**Send**.

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image31.png)

3.  Copiare il test generato.

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image32.png)

4.  Aprire il IntegrationTests.cs da MinimalAPI.Tests.

![Uno screenshot di un computer Descrizione generata
automaticamente](./media/image33.png)

5.  Incollalo nel file cs dopo il blocco di prova di Hello World.
    Risolvere eventuali problemi che potrebbero sorgere.

6.  Aprire la chat di Copilot dal riquadro di sinistra.

![Uno screenshot di un computer Descrizione generata
automaticamente](./media/image19.png)

7.  Digitare /tests, il comando per creare unità di test e premere
    **Enter**. Il Copilot genera un file di test. Copiane il contenuto.

![Uno screenshot di un computer Descrizione generata
automaticamente](./media/image34.png)

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image35.png)

8.  Aprire **IntegrationTests.cs** da **MinimalAPI.Tests**.

![Uno screenshot di un computer Descrizione generata
automaticamente](./media/image33.png)

9.  Sostituire il contenuto del file con il codice generato da Copilot e
    salva.

**Importante:** Verificare la presenza di eventuali errori e correggili
utilizzando il comando /fix o manualmente. Utilizzare il codice di
riferimento riportato di seguito per risolvere i problemi.

10. Se i test non vengono generati per tutti gli endpoint, dalla chat
    specificare il nome del punto finale e chiedere al Copilota di
    generare il test come indicato di seguito. Aggiornare i nomi degli
    endpoint in base a quali vengono aggiornati e quali mancano nel
    test.

generate test units for moviesbydirector, parseurl, listfiles,
calculatememoryconsumption and randomeuropeancountry

**Codice di riferimento:**

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

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image36.png)

11. Dal terminale, eseguire il comando, **dotnet test**

12. Se il test viene superato, dovresti vedere l'output simile a quello
    nello screenshot qui sotto.

![Immagine rotta](./media/image37.png)

13. Se necessario, è possibile aggiungere altri test.

**Esercizio 6: Creare un Dockerfile**

1.  Fare clic con il pulsante destro del mouse sulla cartella **dotnet**
    e selezionare **New File **e denominare il file come **Dockerfile**.

![Immagine rotta](./media/image38.png)

2.  Assegnare al file il nome **Dockerfile**.

![Uno screenshot di un computer Descrizione generata
automaticamente](./media/image39.png)

3.  Nel file appena creato, premere **Ctrl+I**, digitare il testo
    seguente e premere **Enter**.

**Generate content for Dockerfile for .NET 8 Project Name - MinimalAPI**

![Uno screenshot di un computer Descrizione generata
automaticamente](./media/image40.png)

4.  Accettare il codice generato.

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image41.png)

5.  Salvare il file. Dal Terminale, eseguire il comando seguente.

docker build -t dotnetapp .

Use the reference code to solve errors if any.

**Codice di riferimento:**

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

![Immagine rotta](./media/image42.png)

6.  Eseguire il comando seguente per eseguire l'app sulla porta 8080

docker run -d -p 8080:80 --name dotnetapp dotnetapp

![Immagine rotta](./media/image43.png)

7.  A questo punto, abbiamo l'app dotnet in esecuzione nella finestra
    mobile.

![Uno screenshot di un computer Descrizione generata
automaticamente](./media/image44.png)
