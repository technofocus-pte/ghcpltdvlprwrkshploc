# **Lab 20 – Aktivieren von GitHub Copilot mit Nodejs**

**Ziel:**

Dieses Lab soll das Demo-Projekt zum Ausführen von Labs zur Bewertung
der Copilot-Rentabilität verstehen.

Bevor wir dieses Lab ausführen, installieren wir zunächst die
erforderlichen Softwarepakete und richten die Umgebung ein.

**Aufgabe 0: Installieren und Einrichten der Umgebung**

Sie müssen die folgenden Softwarepakete herunterladen und installieren,
um die Umgebung zum Ausführen dieses Labs einzurichten.

1.  Node.js

2.  mocha

&nbsp;

1.  Öffnen Sie den Edge-Browser.

> ![Ein Screenshot eines Computers Beschreibung wird automatisch
> generiert](./media/image1.png)

2.  Kopieren Sie in das URL-Feld des Browsers den Link und fügen Sie ihn
    ein, um die Softwarepakete auf Ihre Lab-VM herunterzuladen.

&nbsp;

1.  Node.js und mvn 🡪
    <https://nodejs.org/dist/v20.16.0/node-v20.16.0-x64.msi>

2.  mocha (kein Download erforderlich)

> **Hinweis**: Standardmäßig werden die Pakete im **Downloads**-Ordner
> gespeichert.
>
> ![Ein Screenshot eines Computers Beschreibung wird automatisch
> generiert](./media/image2.png)

1.  **Installieren Sie Node.js und mvn**

&nbsp;

1.  Wechseln Sie zum Ordner **Downloads**
    (**C:\Users\Admin\Downloads**), und doppelklicken Sie auf
    **node-v20.16.0-x64.msi.**

> ![Ein Screenshot eines Computers Beschreibung wird automatisch
> generiert](./media/image3.png)

2.  Klicken Sie im Fenster "Node.js Setup-Wizard" auf **Next**.

> ![Ein Screenshot eines Computers Beschreibung wird automatisch
> generiert](./media/image4.png)

3.  Akzeptieren Sie **EULA** und klicken Sie auf **Next**.

> ![Ein Screenshot eines Software-Lizenzvertrags Beschreibung wird
> automatisch generiert](./media/image5.png)

4.  Behalten Sie den Standardzielordner bei, und klicken Sie dann auf
    **Next**.

> ![Ein Screenshot eines Computers Beschreibung wird automatisch
> generiert](./media/image6.png)

5.  Klicken Sie auf **Add to the PATH** und dann auf **Next**.

> ![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
> generiert](./media/image7.png)

6.  Aktivieren Sie im Fenster **Tools for native Modules** das
    **Kontrollkästchen** und klicken Sie auf **Next**.

> ![Ein Screenshot eines Computers Beschreibung wird automatisch
> generiert](./media/image8.png)

7.  Klicken Sie auf **Install**.

> ![Ein Screenshot eines Computers Beschreibung wird automatisch
> generiert](./media/image9.png)
>
> Hinweis: Wenn das Popup-Fenster **"User Access Control**" angezeigt
> wird, klicken Sie bitte auf **Yes**, um fortzufahren**.**

8.  Klicken Sie auf **Finish** , wenn Sie fertig sind.

> ![Ein Screenshot eines Computers Beschreibung wird automatisch
> generiert](./media/image10.png)

9.  Das **Cmd**-Terminal wird geöffnet. Drücken Sie eine beliebige
    Taste, um fortzufahren.

> ![Ein Screenshot eines Computers Beschreibung wird automatisch
> generiert](./media/image11.png)
>
> Hinweis: Nach dem Drücken einer Taste kann es zu einer Verzögerung
> kommen. Bitte warten Sie einige Zeit, um mit der Installation
> fortzufahren.

10. Klicken Sie auf **Yes**, um im UAC-Fenster fortzufahren.

> ![Ein Screenshot eines Computerfehlers Beschreibung wird automatisch
> generiert](./media/image12.png)

11. **Windows Powershell** wird geöffnet und zeigt Installationsdetails
    an.

> ![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
> generiert](./media/image13.png)

12. Geben Sie nach Abschluss der Installation **Enter**-Taste ein, um
    PowerShell zu beenden.

> ![Ein Computerbildschirm mit Text darauf Beschreibung wird automatisch
> generiert](./media/image14.png)

2.  **Mocha installieren**

&nbsp;

1.  Öffnen Sie die Eingabeaufforderung

> ![Ein Screenshot eines Computers Beschreibung wird automatisch
> generiert](./media/image15.png)

2.  Führen Sie zuerst den folgenden Befehl aus.

> +++npm install --global mocha+++
>
> ![Ein Screenshot eines Computers Beschreibung wird automatisch
> generiert](./media/image16.png)
>
> ![Ein Screenshot eines Computerbildschirms Beschreibung wird
> automatisch generiert](./media/image17.png)

3.  Führen Sie als Nächstes den folgenden Befehl aus

> +++npm install axios+++
>
> ![Ein Screenshot eines Computerbildschirms Beschreibung wird
> automatisch generiert](./media/image18.png)
>
> ![Ein Screenshot eines Computers Beschreibung wird automatisch
> generiert](./media/image19.png)
>
> Jetzt haben Sie die Installation von **mocha** abgeschlossen.
> Schließen Sie das Terminal, um mit der Installation anderer Pakete
> fortzufahren.

## **Übung 1: Einführung**

1.  Öffnen Sie in Visual Studio **nodeserver.js** über den Knoten
    exercisefiles -\>.

![Ein Screenshot eines Computers Beschreibung wird automatisch
generiert](./media/image20.png)

2.  Wir müssen mit der Codierung für den **Node.js-Server** beginnen,
    der einen Methodenaufruf "get" verfügbar macht, der den Wert des
    Schlüssels zurückgibt, der in der Abfragezeichenfolge übergeben
    wird. Lassen Sie uns den Copilot nutzen, um uns dabei zu helfen.

3.  Drücken Sie **Ctrl+I**, fügen Sie die folgenden Befehle ein, damit
    der Copilot den Code generieren kann, und klicken Sie auf **Send**.

**// write a nodejs server that will expose a method call "get" that
will return the value of the key passed in the query string**

**// example: http://localhost:3000/get?key=hello**

**// if the key is not passed, return "key not passed"**

**// if the key is passed, return "hello" + key**

**// if the url has other methods, return "method not supported"**

**// when server is listening, log "server is listening on port 3000"**

![Ein Screenshot eines Computers Beschreibung wird automatisch
generiert](./media/image21.png)

4.  Der Copilot generiert den Code und zeigt ihn an. Klicken Sie auf
    **Accept**, um es zu akzeptieren.

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image22.png)

5.  Klicken Sie mit der rechten Maustaste auf den **node**-Ordner und
    wählen Sie **Open in Integrated Terminal**.

![Ein Screenshot eines Computers Beschreibung wird automatisch
generiert](./media/image23.png)

6.  Sobald das Terminal geöffnet ist, führen Sie den folgenden Befehl
    aus.

!!**mocha test.js**!!

7.  Sie sollten ein Ergebnis wie **1 Passing** erhalten , wie im
    Screenshot unten.

![Ein Computerbildschirm mit weißem Text Beschreibung wird automatisch
generiert](./media/image24.png)

8.  Dies ist der Komponententest für die Methode im nodeserver.js und
    sie hat bestanden.

9.  Wir werden dem Server weiterhin verschiedene Methoden hinzufügen,
    die den Copilot verwenden.

## **Übung 2: Erstellen neuer Funktionalitäten**

Die Übung besteht darin, einen Webserver mit Nodejs zu erstellen, der
die Anforderung verschiedener Funktionen bedient.

1.  Fügen Sie die **DaysBetweenDates**-Funktionsanforderung hinzu, an
    der der Server teilnehmen muss.

2.  Drücken Sie die **Enter-**Taste, nachdem die **if**-Bedingung –
    **pathname == ‘/get’** beendet ist.

**Hinweis:** Beachten Sie die rot hervorgehobene geschweifte Klammer, an
der Sie die **Enter**-Taste drücken müssen.

![](./media/image25.png)

3.  Drücken Sie **Ctrl+I** , um die Copilot-Inline-Funktion zu öffnen,
    geben Sie Folgendes ein und klicken Sie auf **Send**.

> **/DaysBetweenDates:**
>
> **Calculate days between two dates**
>
> **receive by query string 2 parameters date1 and date 2, and calculate
> the days between those two dates.**

**Referenz-Code:**

if (req.url.startsWith('/DaysBetweenDates')) {

//calculate days between two dates

//get dates from querystring

var queryData = url.parse(req.url, true).query;

var date1 = queryData.date1;

var date2 = queryData.date2;

//convert dates to milliseconds

var date1_ms = Date.parse(date1);

var date2_ms = Date.parse(date2);

//calculate difference in milliseconds

var difference_ms = date2_ms - date1_ms;

//convert to days and return

res.end(Math.round(difference_ms / 86400000) + " days");

}

![](./media/image26.png)

4.  Copilot generiert den Code. Klicken Sie auf **Accept**, um den Code
    zu akzeptieren. Beachten Sie, dass es sich bei dem generierten Code
    um einen **else if**-Block handelt, wobei in der Anforderung
    **DaysBetweenDays** angegeben ist.

![](./media/image27.png)

5.  Klicken Sie auf **Enter** nach dem **DaysBetweenDates**-Block.

6.  Geben Sie den untenstehenden Kommentarblock ein und drücken Sie die
    **Enter**-Taste.

**/\***

**/Validatephonenumber:**

**Receive by querystring a parameter called phoneNumber**

**validate phoneNumber with proper Spanish format, for example
34666666666**

**if phoneNumber is valid return "valid"**

**if phoneNumber is not valid return "invalid"**

**\*/**

**Referenz-Code:**

else if (req.url.startsWith('/Validatephonenumber')) {

//get phoneNumber var from querystring

var queryData = url.parse(req.url, true).query;

var phoneNumber = queryData.phoneNumber;

//validate phoneNumber with Spanish format

var regex = /^(\\34|0034|34)?\[ -\]\*(6|7)\[ -\]\*(\[0-9\]\[
-\]\*){8}$/;

//if phoneNumber is valid return "valid"

if (regex.test(phoneNumber)) {

res.end("valid");

}

//if phoneNumber is not valid return "invalid"

else {

res.end("invalid");

}

}

![Ein Screenshot eines Computers Beschreibung wird automatisch
generiert](./media/image28.png)

7.  Der Copilot generiert den Code. Klicken Sie auf **Accept**, um den
    Code zu akzeptieren.

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image29.png)

8.  Klicken Sie nach dem Block **Validatephonenumber** auf die
    **Enter**-Taste, um den nächsten Codeblock hinzuzufügen.

9.  Kopieren Sie den folgenden Text und fügen Sie ihn in die js-Datei
    ein.

> **/\***
>
> **/ValidateSpanishDNI:**

**Receive by querystring a parameter called dni**

> **calculate DNI letter**
>
> **if DNI is valid return "valid"**
>
> **if DNI is not valid return "invalid"**
>
> **\*/**
>
> **Referenz-Code:**
>
> else if (req.url.startsWith('/ValidateSpanishDNI')) {
>
> var queryData = url.parse(req.url, true).query;
>
> var dni = queryData.dni;
>
> // calculate DNI letter
>
> var dniLetter = dni.charAt(dni.length - 1);
>
> var dniNumber = dni.substring(0, dni.length - 1);
>
> var dniLetterCalc = "TRWAGMYFPDXBNJZSQVHLCKE".charAt(dniNumber % 23);
>
> //if DNI is valid return "valid"
>
> if (dniLetter == dniLetterCalc) {
>
> res.end("valid");
>
> }
>
> //if DNI is not valid return "invalid"
>
> else {
>
> res.end("invalid");
>
> }
>
> }
>
> ![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
> generiert](./media/image30.png)

10. Sobald der obige Inhalt eingefügt ist, generiert der Copilot den
    Code, der direkt unter dem Kommentar angezeigt wird. Klicken Sie auf
    **Accept**, um den Code zu akzeptieren.

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image31.png)

11. Öffnen Sie den Copilot-Chat im linken Navigationsbereich.

![Ein schwarzes rechteckiges Objekt mit weißen Symbolen Beschreibung
wird automatisch generiert](./media/image32.png)

12. Fügen Sie den folgenden Inhalt in den Chat ein und klicken Sie auf
    die Schaltfläche **Send**.

> **/ReturnColorCode:**
>
> **Receive by querystring a parameter called color**
>
> **read colors.json file and return the rgba field**
>
> **get color var from querystring**
>
> **iterate for each color in colors.json to find the color**
>
> **return the code.hex field**
>
> **Referenz-Code:**

else if (req.url.startsWith('/ReturnColorCode')) {

//read colors.json file and return the rgba field

var colors = fs.readFileSync('colors.json', 'utf-8');

var colorsObj = JSON.parse(colors);

//get color var from querystring

var queryData = url.parse(req.url, true).query;

var color = queryData.color;

var colorFound = "not found";

//for each color in colors.json

for (var i = 1; i \< colorsObj.length; i++) {

//if color is found return the color code

if (colorsObj\[i\].color == color) {

colorFound = colorsObj\[i\].code.hex;

}

}

res.end(colorFound);

}

**Hinweis:** Copilot verwendet standardmäßig die geöffnete Datei als
Kontext, um den Vorschlag zu generieren.

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image33.png)

13. Halten Sie den Cursor nach dem **ValidateSpanishDNI**-Block und
    klicken Sie im Chat auf das Symbol “Insert at cursor”. Dadurch wird
    der von Copilot generierte Code aus dem Chat in die js-Datei des
    Servers an der genannten Stelle **kopiert**.

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image34.png)

14. Überprüfen Sie, ob Fehler vorhanden sind. In diesem generierten Code
    gibt es einen Fehler, da sich zwischen den else if-Blöcken eine
    konstante Deklaration befindet.

![Ein Screenshot eines Computers Beschreibung wird automatisch
generiert](./media/image35.png)

15. Drücken Sie **Ctrl+I**, um den Copilot Inline zu öffnen, geben Sie
    !!**/fix**!! und klicken Sie auf die Schaltfläche **Send**.

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image36.png)

16. Copilot generiert eine Lösung, wenn es eine finden kann. Akzeptieren
    oder verwerfen Sie die Lösung, je nachdem, wie genau die Lösung ist.

![Ein Screenshot eines Computers Beschreibung wird automatisch
generiert](./media/image37.png)

17. Hier verschieben wir die konstante Deklaration in den else if-Block
    von returncolors, um den Fehler zu beheben.

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image38.png)

**Wichtig:** Der Code und die Auflösung können für Sie unterschiedlich
sein, je nachdem, welche der Copilot generiert.

18. Drücken Sie nach dem hinzugefügten Block **Ctrl+I,** um die
    Copilot-Inline-Funktion zu öffnen, fügen Sie den folgenden Inhalt
    ein und klicken Sie auf **Send**.

**/TellMeAJoke:**

**Make a call to the joke api and return a random joke using axios
(<https://official-joke-api.appspot.com/random_joke>)**

Referenz-Code:

else if (req.url.startsWith('/TellMeAJoke')) {

//make a call to the joke api and return a random joke using axios

const axios = require('axios');

axios.get('https://official-joke-api.appspot.com/random_joke')

.then(function (response) {

// handle success

res.end(response.data.setup + " " + response.data.punchline);

}

)

.catch(function (error) {

// handle error

console.log(error);

})

.then(function () {

// always executed

});

}

![Ein Screenshot eines Computers Beschreibung wird automatisch
generiert](./media/image39.png)

19. Klicken Sie auf **Accept**, um den von Copilot generierten Code zu
    akzeptieren.

![Ein Screenshot eines Computers Beschreibung wird automatisch
generiert](./media/image40.png)

20. Drücken Sie nach dem generierten Codeblock **Ctrl+I**, geben Sie den
    folgenden Text ein und klicken Sie auf die Schaltfläche **Send**.

**/MoviesByDirector:**

**Receive by querystring a parameter called director**

**Make a call to the movie api and return a list of movies of that
director using axios**

**Return the full list of movies**

**Referenz-Code:**

//method that gets the name of a director and retrieves from an api the
list of movies of that director

else if (req.url.startsWith('/MoviesByDirector')) {

//get a director name from querystring

var queryData = url.parse(req.url, true).query;

var director = queryData.director;

//make a call to the movie api omdbapi.com and return a list of movies
of that director using axios

const axios = require('axios');

axios.get('http://www.omdbapi.com/?apikey=XXXXXXX&s=' + director)

.then(function (response) {

//return the full list of movies

var movies = "";

for (var i = 0; i \< response.data.Search.length; i++) {

movies = movies + response.data.Search\[i\].Title + ", ";

}

res.end(movies);

}

)

.catch(function (error) {

// handle error

console.log(error);

}

)

.then(function () {

// always executed

}

);

}

![Ein Screenshot eines Computers Beschreibung wird automatisch
generiert](./media/image41.png)

21. Klicken Sie auf **Accept**, um den Code zu akzeptieren.

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image42.png)

22. Drücken Sie nach dem generierten Codeblock **Ctrl+I**, geben Sie den
    folgenden Text ein und klicken Sie auf die Schaltfläche **Send**.

**/ParseUrl:**

**Retrieves a parameter from querystring called someurl**

**Parse the url and return the protocol, host, port, path, querystring
and hash**

**Return the parsed host**

**Referenz-Code:**

> //If url equals to ParseUrl
>
> else if (req.url.startsWith('/ParseUrl')) {
>
> //retrieves a parameter from querystring called someurl
>
> var queryData = url.parse(req.url, true).query;
>
> var someUrl = queryData.someurl;
>
> //parse the url and return the protocol, host, port, path, querystring
> and hash
>
> var urlObj = new URL(someUrl);
>
> var protocol = urlObj.protocol;
>
> var host = urlObj.host;
>
> var port = urlObj.port;
>
> var path = urlObj.pathname;
>
> var querystring = urlObj.search;
>
> var hash = urlObj.hash;
>
> //return the parsed host
>
> res.end("host: " + host);
>
> }

![Ein Screenshot eines Computers Beschreibung wird automatisch
generiert](./media/image43.png)

23. Klicken Sie auf **Accept**, um den Code zu akzeptieren.

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image44.png)

24. Drücken Sie nach dem generierten Codeblock **Ctrl+I**, geben Sie den
    folgenden Text ein und klicken Sie auf die Schaltfläche **Send**.

**/GetFullTextFile:**

**Read \`sample.txt\`\` and return lines that contains the word
"Fusce"**

**Referenz-Code:**

else if (req.url.startsWith('/GetFullTextFile')) {

//read sample.txt and return lines that contains the word "Fusce"

var text = fs.readFileSync('sample.txt', 'utf-8');

var lines = text.split("\r");

var linesFound = "";

for (var i = 1; i \< lines.length; i++) {

if (lines\[i\].includes("Fusce")) {

linesFound = linesFound + lines\[i\] + ", ";

}

}

res.end(linesFound);

}

**HINWEIS:** Seien Sie vorsichtig mit dieser Implementierung, da diese
normalerweise den gesamten Inhalt der Datei liest, bevor sie analysiert
wird, so dass die Speicherauslastung hoch ist und bei zu großen Dateien
fehlschlagen kann.

![Ein Screenshot eines Computers Beschreibung wird automatisch
generiert](./media/image45.png)

25. Klicken Sie auf **Accept**, um den Code zu akzeptieren.

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image46.png)

26. Drücken Sie nach dem generierten Codeblock **Ctrl+I**, geben Sie den
    folgenden Text ein und klicken Sie auf die Schaltfläche **Send**.

**/GetLineByLinefromtTextFile:**

**Read sample.txt line by line**

**Create a promise to read the file line by line, and return a list of
lines that contains the word "Fusce"**

**Return the list of lines**

**Referenz-Code:**

else if (req.url.startsWith('/GetLineByLinefromtTextFile')) {

//read sample.txt line by line

var lineReader = require('readline').createInterface({

input: require('fs').createReadStream('sample.txt')

});

//create a promise to read the file line by line, and return a list of
lines that contains the word "Fusce"

var promise = new Promise(function (resolve, reject) {

var lines = \[\];

lineReader.on('line', function (line) {

if (line.includes("Fusce")) {

lines.push(line);

}

});

lineReader.on('close', function () {

resolve(lines);

});

});

//return the list of lines

promise.then(function (lines) {

res.end(lines.toString());

});

}

![Ein Screenshot eines Videos Beschreibung wird automatisch
generiert](./media/image47.png)

27. Klicken Sie auf **Accept**, um den Code zu akzeptieren.

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image48.png)

28. Drücken Sie nach dem generierten Codeblock **Ctrl+I**, geben Sie den
    folgenden Text ein und klicken Sie auf die Schaltfläche **Send**.

**/CalculateMemoryConsumption:**

**Return the memory consumption of the process in GB, rounded to 2
decimals**

**Referenz-Code:**

else if (req.url.startsWith('/CalculateMemoryConsumption')) {

//return the memory consumption of the process in GB, rounded to 2
decimals

var memory = process.memoryUsage().heapUsed / 1024 / 1024;

res.end(memory.toFixed(2) + " GB");

}

![Ein Screenshot eines Computers Beschreibung wird automatisch
generiert](./media/image49.png)

29. Klicken Sie auf **Accept**, um den Code zu akzeptieren.

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image50.png)

30. Drücken Sie nach dem generierten Codeblock **Ctrl+I**, geben Sie den
    folgenden Text ein und klicken Sie auf die Schaltfläche **Send**.

**/RandomEuropeanCountry:**

**Make an array of european countries and its iso codes**

**Return a random country from the array**

**Return the country and its iso code**

**Referenz-Code:**

else if (req.url.startsWith('/RandomEuropeanCountry')) {

//make an array of european countries and its iso codes

var countries = \[

{ country: "Italy", iso: "IT" },

{ country: "France", iso: "FR" },

{ country: "Spain", iso: "ES" },

{ country: "Germany", iso: "DE" },

{ country: "United Kingdom", iso: "GB" },

{ country: "Greece", iso: "GR" },

{ country: "Portugal", iso: "PT" },

{ country: "Romania", iso: "RO" },

{ country: "Bulgaria", iso: "BG" },

{ country: "Croatia", iso: "HR" },

{ country: "Czech Republic", iso: "CZ" },

{ country: "Denmark", iso: "DK" },

{ country: "Estonia", iso: "EE" },

{ country: "Finland", iso: "FI" },

{ country: "Hungary", iso: "HU" },

{ country: "Ireland", iso: "IE" },

{ country: "Latvia", iso: "LV" },

{ country: "Lithuania", iso: "LT" },

{ country: "Luxembourg", iso: "LU" },

{ country: "Malta", iso: "MT" },

{ country: "Netherlands", iso: "NL" },

{ country: "Poland", iso: "PL" },

{ country: "Slovakia", iso: "SK" },

{ country: "Slovenia", iso: "SI" },

{ country: "Sweden", iso: "SE" },

{ country: "Belgium", iso: "BE" },

{ country: "Austria", iso: "AT" },

{ country: "Switzerland", iso: "CH" },

{ country: "Cyprus", iso: "CY" },

{ country: "Iceland", iso: "IS" },

{ country: "Norway", iso: "NO" },

{ country: "Albania", iso: "AL" },

{ country: "Andorra", iso: "AD" },

{ country: "Armenia", iso: "AM" },

{ country: "Azerbaijan", iso: "AZ" },

{ country: "Belarus", iso: "BY" },

{ country: "Bosnia and Herzegovina", iso: "BA" },

{ country: "Georgia", iso: "GE" },

{ country: "Kazakhstan", iso: "KZ" },

{ country: "Kosovo", iso: "XK" },

{ country: "Liechtenstein", iso: "LI" },

{ country: "Macedonia", iso: "MK" },

{ country: "Moldova", iso: "MD" },

{ country: "Monaco", iso: "MC" },

{ country: "Montenegro", iso: "ME" },

{ country: "Russia", iso: "RU" },

{ country: "San Marino", iso: "SM" },

{ country: "Serbia", iso: "RS" },

{ country: "Turkey", iso: "TR" },

{ country: "Ukraine", iso: "UA" },

{ country: "Vatican City", iso: "VA" }

\];

//return a random country from the array

var randomCountry = countries\[Math.floor(Math.random() \*
countries.length)\];

//return the country and its iso code

res.end(randomCountry.country + " " + randomCountry.iso);

}

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image51.png)

31. Klicken Sie auf **Accept**, um den Code zu akzeptieren.

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image52.png)

## **Übung 3: Dokumentieren des Codes**

Das Dokumentieren von Code ist immer eine langweilige und schmerzhafte
Aufgabe. Wir können es aber mit Copilot dokumentieren. Bitten Sie
Copilot im Chat, die nodeserver.js-Datei zu dokumentieren.

1.  **Wählen Sie alle** in der **nodeserver.js**-Datei **aus**.

2.  Geben Sie im Copilot-Chat !! **document the nodeserver.js file**!!
    und klicken Sie auf Send.

3.  Der Copilot erstellt eine detaillierte Dokumentation der Datei.

![Ein Screenshot eines Computers Beschreibung wird automatisch
generiert](./media/image53.png)

## **Übung 4: Erstellen von Tests**

Wir erstellen automatisierte Tests, um zu überprüfen, ob die
Funktionalität der vorherigen Endpunkte korrekt implementiert ist. Die
Tests sollten zusammen in der Datei test.js sein.

Sie können Copilot nutzen, um die Tests auszuführen. Es gibt einen
/tests-Befehl, den Sie direkt über Copilot Chat ausführen können, oder
indem Sie den Code auswählen, für den Sie Tests erstellen möchten, und
indem Sie die Copilot-Inline-Funktion verwenden.

1.  Öffnen Sie die test.js Datei.

2.  Klicken Sie auf **Enter** nach dem bestehenden **it**-Block.

3.  Geben Sie den folgenden Text ein und klicken Sie auf die
    **Enter**-Taste.

**//add test to test DaysBetweenDates**

![Ein Screenshot eines Computers Beschreibung wird automatisch
generiert](./media/image54.png)

4.  Dadurch wird der Komponententestblock für **DaysBetweenDates**
    generiert. Klicken Sie auf **Accept**, um den Code zu akzeptieren.

![Ein Screenshot eines Computers Beschreibung wird automatisch
generiert](./media/image55.png)

5.  Führen Sie vom Terminal aus den folgenden Befehl aus !!**mocha
    test.js**!!

![Ein Computerbildschirm mit weißem Text Beschreibung wird automatisch
generiert](./media/image56.png)

6.  Geben Sie den folgenden Text **//add test to check
    validatephoneNumber**, und klicken Sie auf die **Enter**-Taste.

![Ein Screenshot eines Computers Beschreibung wird automatisch
generiert](./media/image57.png)

7.  Klicken Sie auf **Accept**, um den von Copilot generierten Code zu
    akzeptieren.

![Ein Screenshot eines Computers Beschreibung wird automatisch
generiert](./media/image58.png)

8.  Führen Sie vom Terminal den Befehl !!**mocha test.js**!! aus.
    Überprüfen Sie, ob die Validierung der Telefonnummer bestanden
    wurde.

![Ein Screenshot eines Computers Beschreibung wird automatisch
generiert](./media/image59.png)

9.  Geben Sie den folgenden Text ein und drücken Sie die
    **Enter**-Taste.

!!**//write test to validate validateSpanishDNI**!!

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image60.png)

10. Akzeptieren Sie den von Copilot generierten Text.

11. Führen Sie vom Terminal !!**mocha test.js**!! aus und überprüfen
    Sie, ob der ValidateSpanishDNI bestanden wurde.

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image61.png)

**Referenz-Code:**

//write npm command line to install mocha

//npm install --global mocha

//command to run this test file

//mocha test.js

const assert = require('assert');

const http = require('http');

const server = require('./nodeserver');

describe('Node Server', () =\> {

it('should return "key not passed" if key is not passed', (done) =\> {

http

.get('http://localhost:3000/Get' , (res) =\> {

let data = '';

res.on('data', (chunk) =\> {

data += chunk;

});

res.on('end', () =\> {

assert.equal(data, 'key not passed');

done();

});

});

});

it('should return the value of the key if key is found', (done) =\> {

http.get('http://localhost:3000/Get?key=world', (res) =\> {

let data = '';

res.on('data', (chunk) =\> {

data += chunk;

});

res.on('end', () =\> {

assert.equal(data, 'hello world');

done();

});

});

});

//add test to check validatephoneNumber

it('should return "valid" if phoneNumber is valid', (done) =\> {

http.get('http://localhost:3000/Validatephonenumber?phoneNumber=34666666666',
(res) =\> {

let data = '';

res.on('data', (chunk) =\> {

data += chunk;

});

res.on('end', () =\> {

assert.equal(data, 'valid');

done();

});

});

});

//write test to validate spanish DNI

it('should return "valid" if spanish DNI 86471508H is valid', (done) =\>
{

http.get('http://localhost:3000/ValidateSpanishDNI?dni=86471508H', (res)
=\> {

let data = '';

res.on('data', (chunk) =\> {

data += chunk;

});

res.on('end', () =\> {

assert.equal(data, 'valid');

done();

});

});

});

//write test to validate spanish DNI

it('should return "valid" if spanish DNI 24153149K is valid', (done) =\>
{

http.get('http://localhost:3000/ValidateSpanishDNI?dni=24153149K', (res)
=\> {

let data = '';

res.on('data', (chunk) =\> {

data += chunk;

});

res.on('end', () =\> {

assert.equal(data, 'valid');

done();

});

});

});

//write test to validate spanish DNI

it('should return "valid" if spanish DNI 12345678A is invalid', (done)
=\> {

http.get('http://localhost:3000/ValidateSpanishDNI?dni=12345678A', (res)
=\> {

let data = '';

res.on('data', (chunk) =\> {

data += chunk;

});

res.on('end', () =\> {

assert.equal(data, 'invalid');

done();

});

});

});

//write test for returnColorCode

it('should return "red" if color is red', (done) =\> {

http.get('http://localhost:3000/ReturnColorCode?color=red', (res) =\> {

let data = '';

res.on('data', (chunk) =\> {

data += chunk;

});

res.on('end', () =\> {

assert.equal(data, '#FF0000');

done();

});

});

});

//write test for daysBetweenDates

it('should return "1" if dates are 2020-01-01 and 2020-01-02', (done)
=\> {

http.get('http://localhost:3000/DaysBetweenDates?date1=2020-01-01&date2=2020-01-02',
(res) =\> {

let data = '';

res.on('data', (chunk) =\> {

data += chunk;

});

res.on('end', () =\> {

assert.equal(data, '1 days');

done();

});

});

});

});

## **Übung 5: Erstellen einer Dockerfile**

1.  Öffnen Sie die **Dockerfile** aus dem **node**-Ordner.

![Ein Screenshot eines Computers Beschreibung wird automatisch
generiert](./media/image62.png)

2.  Die Datei besteht aus Kommentaren, wie sie gefüllt werden soll.

3.  Drücken Sie **Ctrl+I** und geben Sie !!**/fix**!! ein. Klicken Sie
    auf das Symbol **Send**.

4.  Der Copilot generiert den Inhalt der Docker-Datei. Klicken Sie auf
    **Accept**.

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image63.png)

5.  Führen Sie im Terminal den folgenden Befehl aus.

!!**docker build -t mynodeapp .**!!

Dies dient dazu, das Image zu erstellen und es als mynodeapp zu
markieren.

![Ein Screenshot eines Computers Beschreibung wird automatisch
generiert](./media/image64.png)

6.  Führen Sie das Docker an Port **4000** mit dem folgenden Befehl aus.

!!**docker run -p 4000:3000 -d mynodeapp**!!

![](./media/image65.png)

7.  Öffnen Sie den Docker-Daemon, um zu sehen, ob die Anwendung
    containerisiert wurde und darin ausgeführt wird.

![Ein Screenshot eines Computers Beschreibung wird automatisch
generiert](./media/image66.png)

**Zusammenfassung:**

In diesem Lab haben wir gelernt, wie man den Copilot in einem
Node-Projekt einsetzt

