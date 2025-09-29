# **Lab 20 - Attivare GitHub Copilot utilizzando Nodejs**

**Obiettivo:**

Questo lab ha lo scopo di aiutare a comprendere il progetto demo per
l'esecuzione di lab per valutare la fattibilità di Copilot.

Prima di eseguire questo laboratorio, installiamo i pacchetti software
necessari e configuriamo l'ambiente.

**Attività 0: Installazione e configurazione dell'ambiente**

È necessario scaricare e installare i seguenti pacchetti software per
configurare l'ambiente per eseguire questo lab.

1.  Node.js

2.  mocha

&nbsp;

1.  Aprire il browser Edge.

> ![Uno screenshot di un computer Descrizione generata
> automaticamente](./media/image1.png)

2.  Nel campo URL del browser copiare e incollare il collegamento per
    scaricare i pacchetti software nella macchina virtuale del lab.

&nbsp;

1.  Node.js e mvn 🡪
    <https://nodejs.org/dist/v20.16.0/node-v20.16.0-x64.msi>

2.  mocha (non è richiesto il download)

> **Nota**: Per impostazione predefinita, i pacchetti verranno salvati
> nella cartella **downloads**.
>
> ![Uno screenshot di un computer Descrizione generata
> automaticamente](./media/image2.png)

1.  **Installare Node.js e mvn**

&nbsp;

1.  Andare alla cartella **Downloads** (**C:\Users\Admin\Downloads**) e
    fare doppio clic su **node-v20.16.0-x64.msi.**

> ![Uno screenshot di un computer Descrizione generata
> automaticamente](./media/image3.png)

2.  Nella finestra "Node.js setup wizard", fare clic su **Next**.

> ![Uno screenshot di un computer Descrizione generata
> automaticamente](./media/image4.png)

3.  Accettare **EULA** e fare clic su **Next**.

> ![Uno screenshot di un contratto di licenza software Descrizione
> generata automaticamente](./media/image5.png)

4.  Mantenere la cartella di destinazione predefinita, quindi fare clic
    su **Next**.

> ![Uno screenshot di un computer Descrizione generata
> automaticamente](./media/image6.png)

5.  Fare clic su **Add to the PATH** e quindi fare clic su **Next**.

> ![Uno screenshot di un programma per computer Descrizione generata
> automaticamente](./media/image7.png)

6.  Nella finestra **Tools for native Modules**, selezionare **check
    box** e fare clic su **Next**.

> ![Uno screenshot di un computer Descrizione generata
> automaticamente](./media/image8.png)

7.  Fare clic su **Install**.

> ![Uno screenshot di un computer Descrizione generata
> automaticamente](./media/image9.png)
>
> Nota: Se viene visualizzato **User Access Control**, fare clic su
> **Yes** per continuare**.**

8.  Fare clic su **Finish** una volta terminato.

> ![Uno screenshot di un computer Descrizione generata
> automaticamente](./media/image10.png)

9.  Si apre il terminale **Cmd**. Premere un tasto qualsiasi per
    continuare.

> ![Uno screenshot di un computer Descrizione generata
> automaticamente](./media/image11.png)
>
> NOTA: Potresti vedere un ritardo dopo aver premuto un tasto. Attendere
> un po' di tempo per procedere con l'installazione.

10. Fare clic su **Yes** per continuare nella finestra UAC.

> ![Uno screenshot di un errore del computer Descrizione generata
> automaticamente](./media/image12.png)

11. Verrà aperto **Windows Powershell** con i dettagli
    dell'installazione.

> ![Uno screenshot di un programma per computer Descrizione generata
> automaticamente](./media/image13.png)

12. Una volta completata l'installazione, digitare **Enter** per uscire
    da PowerShell.

> ![Schermo di un computer con del testo Descrizione generata
> automaticamente](./media/image14.png)

2.  **Installare mocha**

&nbsp;

1.  Aprire il command prompt

> ![Uno screenshot di un computer Descrizione generata
> automaticamente](./media/image15.png)

2.  Per prima cosa eseguire il seguente comando.

> +++npm install --global mocha+++
>
> ![Uno screenshot di un computer Descrizione generata
> automaticamente](./media/image16.png)
>
> ![Uno screenshot dello schermo di un computer Descrizione generata
> automaticamente](./media/image17.png)

3.  Eseguire quindi il comando seguente

> +++npm install axios+++
>
> ![Uno screenshot dello schermo di un computer Descrizione generata
> automaticamente](./media/image18.png)
>
> ![Uno screenshot di un computer Descrizione generata
> automaticamente](./media/image19.png)
>
> Ora hai finito di installare **mocha.** Chiudere il terminale per
> procedere con l'installazione di altri pacchetti.

## **Esercizio 1: Introduzione**

1.  Da Visual Studio, aprire **nodeserver.js** dal exercisefiles -\>
    node.

![Uno screenshot di un computer Descrizione generata
automaticamente](./media/image20.png)

2.  Dobbiamo iniziare a codificare per il node..js che esporrà una
    chiamata al metodo "get" che restituirà il valore della chiave
    passata nella stringa di query. Usiamo il Copilot per aiutarci in
    questo.

3.  Premere **Ctrl+I** e incollare i comandi seguenti per consentire al
    Copilot di generare il codice e premere **Send**.

**// write a nodejs server that will expose a method call "get" that
will return the value of the key passed in the query string**

**// example: http://localhost:3000/get?key=hello**

**// if the key is not passed, return "key not passed"**

**// if the key is passed, return "hello" + key**

**// if the url has other methods, return "method not supported"**

**// when server is listening, log "server is listening on port 3000"**

![Uno screenshot di un computer Descrizione generata
automaticamente](./media/image21.png)

4.  Il Copilot genera il codice e lo visualizza. Cliccare su **Accept**
    per accettarlo.

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image22.png)

5.  Fare clic con il pulsante destro del mouse sulla cartella del
    **node** e selezionare **Open in Integrated Terminal**.

![Uno screenshot di un computer Descrizione generata
automaticamente](./media/image23.png)

6.  Una volta aperto il terminale, eseguire il comando seguente da esso.

!!**mocha test.js**!!

7.  Dovresti ottenere un risultato come **1 Passing** come nello
    screenshot qui sotto.

![Schermo di un computer con testo bianco Descrizione generata
automaticamente](./media/image24.png)

8.  Questo è il test unitario per il metodo in nodeserver.js ed è stato
    superato.

9.  Continueremo ad aggiungere diversi metodi al server utilizzando il
    Copilot.

## **Esercizio 2: Creazione di nuove funzionalità**

L'esercizio consiste nella creazione di un server web utilizzando Nodejs
che serve la richiesta di varie funzionalità.

1.  Aggiungere la richiesta di funzionalità **DaysBetweenDates** a cui
    il server deve partecipare.

2.  Premere **Enter** dopo la fine della condizione **if** – **pathname
    == '/get'**.

**Nota:** fare riferimento al tutore nell'evidenziazione rossa in cui è
necessario premere **Enter**

![](./media/image25.png)

3.  Premere **Ctrl+I** per aprire la funzione in linea di Copilot,
    immettere quanto segue e fare clic su **Send**.

> **/DaysBetweenDates:**
>
> **Calculate days between two dates**
>
> **receive by query string 2 parameters date1 and date 2, and calculate
> the days between those two dates.**

**Codice di riferimento:**

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

4.  Copilot genera il codice. Cliccare su **Accept** per accettare il
    codice. Si noti che il codice generato è un blocco **else if** in
    cui nella richiesta è **DaysBetweenDates**.

![](./media/image27.png)

5.  Fare clic su **Enter** dopo il blocco **DaysBetweenDates**.

6.  Inserire il blocco dei commenti qui sotto e premere **Enter**.

**/\***

**/Validatephonenumber:**

**Receive by querystring a parameter called phoneNumber**

**validate phoneNumber with proper Spanish format, for example
34666666666**

**if phoneNumber is valid return "valid"**

**if phoneNumber is not valid return "invalid"**

**\*/**

**Codice di riferimento:**

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

![Uno screenshot di un computer Descrizione generata
automaticamente](./media/image28.png)

7.  Il Copilot genera il codice. Fare clic su **Accept** per accettare
    il codice.

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image29.png)

8.  Fare clic su **Enter** dopo il blocco **Validatephonenumber** per
    aggiungere il blocco di codice successivo.

9.  Copiare e incollare il testo seguente nel file js.

> **/\***
>
> **/ValidateSpanishDNI:**
>
> **Receive by querystring a parameter called dni**
>
> **calculate DNI letter**
>
> **if DNI is valid return "valid"**
>
> **if DNI is not valid return "invalid"**
>
> **\*/**
>
> **Codice di riferimento:**
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
> ![Schermata di un programma per computer Descrizione generata
> automaticamente](./media/image30.png)

10. Una volta incollato il contenuto di cui sopra, il Copilot genera il
    codice che viene visualizzato appena sotto il commento. Cliccare su
    **Accept** per accettare il codice.

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image31.png)

11. Aprire la chat di Copilot dal riquadro di navigazione a sinistra.

![Un oggetto rettangolare nero con simboli bianchi Descrizione generata
automaticamente](./media/image32.png)

12. Incollare il contenuto sottostante nella chat e fare clic sul
    pulsante **Send**.

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
> **Codice di riferimento:**

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

**Nota:** Copilot utilizzerà per impostazione predefinita il file aperto
come contesto per generare il suggerimento.

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image33.png)

13. Tenere il cursore dopo il blocco **ValidateSpanishDNI** e fare clic
    sull'icona **Insert** al cursore nella chat. In questo modo il
    codice generato da Copilot viene **copiato** dalla chat nel file js
    del server nella posizione indicata**.**

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image34.png)

14. Verificare la presenza di eventuali errori. In questo codice
    generato si verifica un errore poiché è presente una dichiarazione
    costante tra i blocchi else if.

![Schermata di un computer Descrizione generata
automaticamente](./media/image35.png)

15. Premere **Ctrl+I** per aprire il Copilot Inline, digitare
    !!**/fix**!! e fare clic sul pulsante **Send**.

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image36.png)

16. Copilot genera una soluzione se riesce a trovarne una. Accettare o
    scartare la soluzione in base all'accuratezza della soluzione.

![Uno screenshot di un computer Descrizione generata
automaticamente](./media/image37.png)

17. Qui, stiamo spostando la dichiarazione costante all'interno del
    blocco else if di returncolors per risolvere l'errore.

![Schermata di un programma per computer Descrizione generata
automaticamente](./media/image38.png)

**Importante:** Il codice e la risoluzione potrebbero essere diversi in
base a quella generata dal Copilot.

18. Dopo aver aggiunto il blocco, premere **Ctrl+I** per aprire la
    funzione in linea di Copilot, incollare il contenuto sottostante e
    fare clic su **Send**.

**/TellMeAJoke:**

**Make a call to the joke api and return a random joke using axios
(<https://official-joke-api.appspot.com/random_joke>)**

Codice di riferimento:

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

![Uno screenshot di un computer Descrizione generata
automaticamente](./media/image39.png)

19. Fare clic su **Accept** per accettare il codice generato da Copilot.

![Uno screenshot di un computer Descrizione generata
automaticamente](./media/image40.png)

20. Dopo il blocco di codice generato, premere **Ctrl+I**, inserire il
    testo sottostante e fare clic sul pulsante **Send**.

**/MoviesByDirector:**

**Receive by querystring a parameter called director**

**Make a call to the movie api and return a list of movies of that
director using axios**

**Return the full list of movies**

**Codice di riferimento:**

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

![Uno screenshot di un computer Descrizione generata
automaticamente](./media/image41.png)

21. Cliccare su **Accept** per accettare il codice.

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image42.png)

22. Dopo il blocco di codice generato, premere **Ctrl+I**, inserire il
    testo sottostante e fare clic sul pulsante **Send**.

**/ParseUrl:**

**Retrieves a parameter from querystring called someurl**

**Parse the url and return the protocol, host, port, path, querystring
and hash**

**Return the parsed host**

**Codice di riferimento:**

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

![Uno screenshot di un computer Descrizione generata
automaticamente](./media/image43.png)

23. Cliccare su **Accept** per accettare il codice.

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image44.png)

24. Dopo il blocco di codice generato, premere **Ctrl+I**, inserire il
    testo sottostante e fare clic sul pulsante **Send**.

**/GetFullTextFile:**

**Read \`sample.txt\`\` and return lines that contains the word
"Fusce"**

**Codice di riferimento:**

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

**NOTA:** Prestare attenzione a questa implementazione, poiché
normalmente legge l'intero contenuto del file prima di analizzarlo,
quindi l'utilizzo della memoria è elevato e potrebbe non riuscire quando
i file sono troppo grandi.

![Uno screenshot di un computer Descrizione generata
automaticamente](./media/image45.png)

25. Cliccare su **Accept** per accettare il codice.

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image46.png)

26. Dopo il blocco di codice generato, premere **Ctrl+I**, inserire il
    testo sottostante e fare clic sul pulsante **Send**.

**/GetLineByLinefromtTextFile:**

**Read sample.txt line by line**

**Create a promise to read the file line by line, and return a list of
lines that contains the word "Fusce"**

**Return the list of lines**

**Codice di riferimento:**

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

![Uno screenshot di un video Descrizione generata
automaticamente](./media/image47.png)

27. Cliccare su **Accept** per accettare il codice.

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image48.png)

28. Dopo il blocco di codice generato, premere **Ctrl+I**, inserire il
    testo sottostante e fare clic sul pulsante **Send**.

**/CalculateMemoryConsumption:**

**Return the memory consumption of the process in GB, rounded to 2
decimals**

**Codice di riferimento:**

else if (req.url.startsWith('/CalculateMemoryConsumption')) {

//return the memory consumption of the process in GB, rounded to 2
decimals

var memory = process.memoryUsage().heapUsed / 1024 / 1024;

res.end(memory.toFixed(2) + " GB");

}

![Uno screenshot di un computer Descrizione generata
automaticamente](./media/image49.png)

29. Cliccare su **Accept** per accettare il codice.

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image50.png)

30. Dopo il blocco di codice generato, premere **Ctrl+I**, inserire il
    testo sottostante e fare clic sul pulsante **Send**.

**/RandomEuropeanCountry:**

**Make an array of european countries and its iso codes**

**Return a random country from the array**

**Return the country and its iso code**

**Codice di riferimento:**

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

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image51.png)

31. Cliccare su **Accept** per accettare il codice.

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image52.png)

## **Esercizio 3: Documentare il codice**

Documentare il codice è sempre un compito noioso e doloroso. Tuttavia,
possiamo utilizzare Copilot per documentarlo per noi. Nella chat, chiedi
a Copilot di documentare il file nodeserver.js.

1.  **Select all** nel file **nodeserver.js**.

2.  Dalla chat di Copilot, entrare !!**document the nodeserver.js
    file**!! e fare clic su Send.

3.  Il Copilot genera una documentazione dettagliata del file.

![Uno screenshot di un computer Descrizione generata
automaticamente](./media/image53.png)

## **Esercizio 4: Building tests**

Creeremo test automatizzati per verificare che la funzionalità degli
endpoint precedenti sia implementata correttamente. I test devono essere
raggruppati nel file test.js.

È possibile utilizzare Copilot per eseguire i test. È disponibile un
comando /tests che è possibile eseguire direttamente da Copilot Chat o
selezionando la parte di codice per cui si desidera creare i test e
utilizzando la funzione in linea di Copilot.

1.  Aprire il file test.js.

2.  Fare clic su **Enter** dopo il blocco **it** esistente.

3.  Inserire il testo sottostante e fare clic su **Enter**.

**//add test to test DaysBetweenDates**

![Schermata di un computer Descrizione generata
automaticamente](./media/image54.png)

4.  In questo modo viene generato il blocco di unit test per
    **DaysBetweenDates**. Cliccare su **Accept** per accettare il
    codice.

![Uno screenshot di un computer Descrizione generata
automaticamente](./media/image55.png)

5.  Dal terminale, eseguire il comando sottostante !!**mocha test.js**!!

![Schermo di un computer con testo bianco Descrizione generata
automaticamente](./media/image56.png)

6.  Inserire il testo sottostante **//add test to check
    validatephoneNumber** e fare clic su **Enter**.

![Schermata di un computer Descrizione generata
automaticamente](./media/image57.png)

7.  Fare clic su **Accept** per accettare il codice generato da Copilot.

![Uno screenshot di un computer Descrizione generata
automaticamente](./media/image58.png)

8.  Dal terminale, eseguire il comando, !!**mocha test.js!**!.
    Verificare che il numero di telefono di convalida sia stato
    superato.

![Uno screenshot di un computer Descrizione generata
automaticamente](./media/image59.png)

9.  Inserire il testo sottostante e premere **Enter**.

!!**//write test to validate validateSpanishDNI**!!

![Schermata di un programma per computer Descrizione generata
automaticamente](./media/image60.png)

10. Accettare il testo generato da Copilot.

11. Dal terminale, eseguire !!**mocha test.js**!! e verifica che il
    ValidateSpanishDNI sia stato superato.

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image61.png)

**Codice di riferimento:**

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

## **Esercizio 5: Creare un Dockerfile**

1.  Aprire il **dockerfile** dalla cartella del **node**.

![Uno screenshot di un computer Descrizione generata
automaticamente](./media/image62.png)

2.  Il file sarà composto da commenti su come dovrebbe essere popolato.

3.  Premere **Ctrl+I** e digitare !!**/fix**!!. Fare clic sull'icona
    **Send**.

4.  Il Copilot genererà il contenuto del file Docker. Fare clic su
    **Accept**.

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image63.png)

5.  Dal terminale, eseguire il comando seguente

!!**docker build -t mynodeapp .**!!

In questo modo si crea l'immagine e la si contrassegna come mynodeapp.

![Uno screenshot di un computer Descrizione generata
automaticamente](./media/image64.png)

6.  Eseguire la finestra mobile nella porta **4000** utilizzando il
    comando seguente.

!!**docker run -p 4000:3000 -d mynodeapp**!!

![](./media/image65.png)

7.  Aprire il daemon Docker per verificare che l'applicazione sia stata
    containerizzata e in esecuzione al suo interno.

![Uno screenshot di un computer Descrizione generata
automaticamente](./media/image66.png)

**Sommario:**

In questo laboratorio, abbiamo imparato come utilizzare il Copilot in un
progetto di node
