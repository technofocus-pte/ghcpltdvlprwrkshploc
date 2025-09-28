# **Lab 20 - Activer GitHub Copilot à l'aide de Nodejs**

**Objectif :**

Cet atelier a pour but d'aider à comprendre le projet de démonstration
pour l'exécution des laboratoires d'évaluation de la viabilité de
Copilot.

Avant d'exécuter cet atelier, nous allons d'abord installer les packages
logiciels nécessaires et configurer l'environnement.

**Tâche 0 : Installation et configuration de l'environnement**

Vous devez télécharger et installer les packages logiciels suivants pour
configurer l'environnement afin d'exécuter cet atelier.

1.  Node.js

2.  mocha

&nbsp;

1.  Ouvrez le navigateur Edge.

> ![Une capture d'écran d'un ordinateur Description générée
> automatiquement](./media/image1.png)

2.  Dans le champ URL du navigateur, copiez-collez le lien pour
    télécharger les packages logiciels sur la machine virtuelle de votre
    laboratoire.

&nbsp;

1.  Node.js and mvn 🡪
    <https://nodejs.org/dist/v20.16.0/node-v20.16.0-x64.msi>

2.  mocha (aucun téléchargement n'est requis)

> **Remarque** : Par défaut, les packages sont enregistrés dans le
> dossier **des téléchargements (downloads)**.
>
> ![Une capture d'écran d'un ordinateur Description générée
> automatiquement](./media/image2.png)

1.  **Installer Node.js et mvn**

&nbsp;

1.  Accédez au dossier **Downloads (C:\Users\Admin\Downloads)** et
    double-cliquez sur **node-v20.16.0-x64.msi.**

> ![Une capture d'écran d'un ordinateur Description générée
> automatiquement](./media/image3.png)

2.  Dans la fenêtre “Node.js setup wizard”, cliquez sur **Next**.

> ![Une capture d'écran d'un ordinateur Description générée
> automatiquement](./media/image4.png)

3.  Acceptez **EULA** et cliquez sur **Next**.

> ![Une capture d'écran d'un contrat de licence de logiciel Description
> générée automatiquement](./media/image5.png)

4.  Conservez le dossier de destination par défaut, puis cliquez sur
    **Next**.

> ![Une capture d'écran d'un ordinateur Description générée
> automatiquement](./media/image6.png)

5.  Cliquez sur **Add to the PATH**, puis sur **Next**.

> ![Une capture d'écran d'un programme informatique Description générée
> automatiquement](./media/image7.png)

6.  Dans la fenêtre **Tools for native Modules**, cochez la **case** et
    cliquez sur Next.

> ![Une capture d'écran d'un ordinateur Description générée
> automatiquement](./media/image8.png)

7.  Cliquez sur **Install**.

> ![Une capture d'écran d'un ordinateur Description générée
> automatiquement](./media/image9.png)
>
> Remarque : Si la fenêtre contextuelle **User Access Control**
> s'affiche, cliquez sur **Yes** pour continuer**.**

8.  Cliquez sur **Finish** une fois que vous avez terminé.

> ![Une capture d'écran d'un ordinateur Description générée
> automatiquement](./media/image10.png)

9.  Le terminal **Cmd** s'ouvre. Appuyez sur n'importe quelle touche
    pour continuer.

> ![Une capture d'écran d'un ordinateur Description générée
> automatiquement](./media/image11.png)
>
> Remarque : Vous pouvez voir un décalage après avoir appuyé sur une
> touche. Veuillez patienter un certain temps avant de procéder à
> l'installation.

10. Cliquez sur **Yes** pour continuer dans la fenêtre UAC.

> ![Une capture d'écran d'une erreur informatique Description générée
> automatiquement](./media/image12.png)

11. **Windows Powershell** s'ouvre et affiche les détails de
    l'installation.

> ![Une capture d'écran d'un programme informatique Description générée
> automatiquement](./media/image13.png)

12. Une fois l'installation terminée, tapez **Entrée** pour quitter
    PowerShell.

> ![Un écran d'ordinateur avec du texte dessus Description générée
> automatiquement](./media/image14.png)

2.  **Installer mocha**

&nbsp;

1.  Ouvrez l'invite de commande

> ![Une capture d'écran d'un ordinateur Description générée
> automatiquement](./media/image15.png)

2.  Exécutez d'abord la commande suivante.

> +++npm install --global mocha+++
>
> ![Une capture d'écran d'un ordinateur Description générée
> automatiquement](./media/image16.png)
>
> ![Une capture d'écran d'un écran d'ordinateur Description générée
> automatiquement](./media/image17.png)

3.  Exécutez ensuite la commande suivante

> +++npm install axios+++
>
> ![Une capture d'écran d'un écran d'ordinateur Description générée
> automatiquement](./media/image18.png)
>
> ![Une capture d'écran d'un ordinateur Description générée
> automatiquement](./media/image19.png)
>
> Vous avez maintenant terminé l'installation de **mocha.** Fermez le
> terminal pour procéder à l'installation d'autres packages.

## **Exercice 1 : Introduction**

1.  À partir de Visual Studio, ouvrez **nodeserver.js** à partir du nœud
    exercisefiles -\>.

![Une capture d'écran d'un ordinateur Description générée
automatiquement](./media/image20.png)

2.  Nous devons commencer à coder pour le nœud. Serveur JS qui exposera
    un appel de méthode “get” qui renverra la valeur de la clé passée
    dans la chaîne de requête. Utilisons le Copilot pour nous aider dans
    ce domaine.

3.  Appuyez sur **Ctrl+I** et collez les commandes ci-dessous pour que
    le Copilot génère le code et appuie sur **Send**.

**// write a nodejs server that will expose a method call "get" that
will return the value of the key passed in the query string**

**// example: http://localhost:3000/get?key=hello**

**// if the key is not passed, return "key not passed"**

**// if the key is passed, return "hello" + key**

**// if the url has other methods, return "method not supported"**

**// when server is listening, log "server is listening on port
3000"**![Une capture d'écran d'un ordinateur Description générée
automatiquement](./media/image21.png)

4.  Le Copilot génère le code et l'affiche. Cliquez sur **Accept** pour
    l'accepter.

![Une capture d'écran d'un programme informatique Description générée
automatiquement](./media/image22.png)

5.  Faites un clic droit sur le dossier du **nœud** et sélectionnez
    **Open in Integrated Terminal**.

![Une capture d'écran d'un ordinateur Description générée
automatiquement](./media/image23.png)

6.  Une fois le terminal ouvert, exécutez la commande ci-dessous à
    partir de celui-ci.

!!**mocha test.js**!!

7.  Vous devriez obtenir un résultat comme **1 Passing** comme dans la
    capture d'écran ci-dessous.

![Un écran d'ordinateur avec du texte blanc Description générée
automatiquement](./media/image24.png)

8.  Il s'agit du test unitaire de la méthode dans le nodeserver.js et il
    a réussi.

9.  Nous continuerons à ajouter différentes méthodes au serveur à l'aide
    du Copilot.

## **Exercice 2 : Créer de nouvelles fonctionnalités**

L'exercice consiste à construire un serveur web à l'aide de Nodejs qui
répond à la demande de diverses fonctionnalités.

1.  Ajoutez la demande de fonctionnalité **DaysBetweenDates** à laquelle
    le serveur doit répondre.

2.  Appuyez sur **Enter** après la fin de la condition **if** –
    **pathname == '/get'**.

**Remarque :** Reportez-vous à l'accolade en surbrillance rouge où vous
devez appuyer sur Enter

![](./media/image25.png)

3.  Appuyez sur **Ctrl+I** pour ouvrir la fonction en ligne du Copilot,
    entrez ce qui suit et cliquez sur **Send**.

> **/DaysBetweenDates :**
>
> **Calculer les jours entre deux dates**
>
> **Recevez par la chaîne de requête 2 les paramètres Date1 et Date 2,
> et calculez les jours entre ces deux dates.**

**Code de référence :**

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

4.  Copilot génère le code. Cliquez sur **Accept** pour accepter le
    code. Notez que le code généré est un bloc **else if** où dans la
    requête se trouve **DaysBetweenDates**.

![](./media/image27.png)

5.  Cliquez sur **Entrée** après le bloc **DaysBetweenDates**.

6.  Entrez le bloc de commentaires ci-dessous et appuyez sur **Entrée**.

**/\***

**/Validatephonenumber:**

**Receive by querystring a parameter called phoneNumber**

**validate phoneNumber with proper Spanish format, for example
34666666666**

**if phoneNumber is valid return "valid"**

**if phoneNumber is not valid return "invalid"**

**\*/**

**Code de référence :**

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

![Une capture d'écran d'un ordinateur Description générée
automatiquement](./media/image28.png)

7.  Le Copilot génère le code. Cliquez sur **Accept** pour accepter le
    code.

![Une capture d'écran d'un programme informatique Description générée
automatiquement](./media/image29.png)

8.  Cliquez sur **Entrée** après le bloc **Validatephonenumber** pour
    ajouter le bloc de code suivant.

9.  Copiez et collez le texte ci-dessous dans le fichier js.

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
> **Code de référence :**
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
> ![Capture d'écran d'un programme informatique Description générée
> automatiquement](./media/image30.png)

10. Une fois le contenu ci-dessus collé, le Copilot génère le code qui
    s'affiche juste en dessous du commentaire. Cliquez sur **Accept**
    pour accepter le code.

![Une capture d'écran d'un programme informatique Description générée
automatiquement](./media/image31.png)

11. Ouvrez le chat Copilot à partir du volet de navigation de gauche.

![Un objet rectangulaire noir avec des symboles blancs Description
générée automatiquement](./media/image32.png)

12. Collez le contenu ci-dessous dans le chat et cliquez sur le **bouton
    Envoyer**.

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
> **Code de référence :**

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

> **Remarque :** Copilot utilisera par défaut le fichier ouvert comme
> contexte afin de générer la suggestion.

![Une capture d'écran d'un programme informatique Description générée
automatiquement](./media/image33.png)

13. Maintenez le curseur après le bloc **ValidateSpanishDNI** et cliquez
    sur l'icône Insérer dans le curseur dans le chat. Cela **copie** le
    code généré par Copilot du chat vers le fichier js du serveur à
    l'emplacement mentionné.

![Une capture d'écran d'un programme informatique Description générée
automatiquement](./media/image34.png)

14. Vérifiez s'il y a des erreurs. Dans ce code généré, il y a une
    erreur puisqu'il y a une déclaration constante entre les blocs else
    if.

![Une capture d'écran d'un ordinateur Description générée
automatiquement](./media/image35.png)

15. Appuyez sur **Ctrl+I** pour ouvrir le Copilot Inline, tapez
    !!**/fix !!** et cliquez sur le bouton **Send.**

![Une capture d'écran d'un programme informatique Description générée
automatiquement](./media/image36.png)

16. Copilot génère une solution s'il peut en trouver une. Acceptez ou
    supprimez la solution en fonction de sa précision.

![Une capture d'écran d'un ordinateur Description générée
automatiquement](./media/image37.png)

17. Ici, nous déplaçons la déclaration constante à l'intérieur du bloc
    else if de returncolors pour résoudre l'erreur.

![Capture d'écran d'un programme informatique Description générée
automatiquement](./media/image38.png)

**Important :** Le code et la résolution peuvent être différents pour
vous en fonction de celui généré par le Copilot.

18. Après le bloc ajouté, appuyez sur **Ctrl+I** pour ouvrir la fonction
    en ligne Copilot, collez le contenu ci-dessous et cliquez sur
    **Send**.

**/TellMeAJoke:**

**Make a call to the joke api and return a random joke using axios
(<https://official-joke-api.appspot.com/random_joke>)**

Code de référence :

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

![Une capture d'écran d'un ordinateur Description générée
automatiquement](./media/image39.png)

19. Cliquez sur **Accept** pour accepter le code généré par Copilot.

![Une capture d'écran d'un ordinateur Description générée
automatiquement](./media/image40.png)

20. Après le bloc de code généré, appuyez sur **Ctrl+I**, entrez le
    texte ci-dessous et cliquez sur le bouton **Send.**

**/MoviesByDirector:**

**Receive by querystring a parameter called director**

**Make a call to the movie api and return a list of movies of that
director using axios**

**Return the full list of movies**

**Code de référence :**

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

![Une capture d'écran d'un ordinateur Description générée
automatiquement](./media/image41.png)

21. Cliquez sur **Accept** pour accepter le code.

![Une capture d'écran d'un programme informatique Description générée
automatiquement](./media/image42.png)

22. Après le bloc de code généré, appuyez sur **Ctrl+I**, entrez le
    texte ci-dessous et cliquez sur le bouton **Send.**

**/ParseUrl:**

**Retrieves a parameter from querystring called someurl**

**Parse the url and return the protocol, host, port, path, querystring
and hash**

**Return the parsed host**

**Code de référence :**

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

![Une capture d'écran d'un ordinateur Description générée
automatiquement](./media/image43.png)

23. Cliquez sur **Accept** pour accepter le code.

![Une capture d'écran d'un programme informatique Description générée
automatiquement](./media/image44.png)

24. Après le bloc de code généré, appuyez sur **Ctrl+I**, entrez le
    texte ci-dessous et cliquez sur le bouton **Send.**

**/GetFullTextFile:**

**Read \`sample.txt\`\` and return lines that contains the word
"Fusce"**

**Code de référence :**

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

**REMARQUE :** Soyez prudent avec cette implémentation, car elle lit
normalement tout le contenu du fichier avant de l'analyser, de sorte que
l'utilisation de la mémoire est élevée et peut échouer lorsque les
fichiers sont trop volumineux.

![Une capture d'écran d'un ordinateur Description générée
automatiquement](./media/image45.png)

25. Cliquez sur **Accept** pour accepter le code.

![Une capture d'écran d'un programme informatique Description générée
automatiquement](./media/image46.png)

26. Après le bloc de code généré, appuyez sur **Ctrl+I**, entrez le
    texte ci-dessous et cliquez sur le bouton **Send.**

**/GetLineByLinefromtTextFile:**

**Read sample.txt line by line**

**Create a promise to read the file line by line, and return a list of
lines that contains the word "Fusce"**

**Return the list of lines**

**Code de référence :**

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

![Une capture d'écran d'une vidéo Description générée
automatiquement](./media/image47.png)

27. Cliquez sur **Accept** pour accepter le code.

![Une capture d'écran d'un programme informatique Description générée
automatiquement](./media/image48.png)

28. Après le bloc de code généré, appuyez sur **Ctrl+I**, entrez le
    texte ci-dessous et cliquez sur le bouton **Send.**

**/CalculateMemoryConsumption:**

**Return the memory consumption of the process in GB, rounded to 2
decimals**

**Code de référence :**

else if (req.url.startsWith('/CalculateMemoryConsumption')) {

//return the memory consumption of the process in GB, rounded to 2
decimals

var memory = process.memoryUsage().heapUsed / 1024 / 1024;

res.end(memory.toFixed(2) + " GB");

}

![Une capture d'écran d'un ordinateur Description générée
automatiquement](./media/image49.png)

29. Cliquez sur **Accept** pour accepter le code.

![Une capture d'écran d'un programme informatique Description générée
automatiquement](./media/image50.png)

30. Après le bloc de code généré, appuyez sur **Ctrl+I**, entrez le
    texte ci-dessous et cliquez sur le bouton **Send.**

**/RandomEuropeanCountry:**

**Make an array of european countries and its iso codes**

**Return a random country from the array**

**Return the country and its iso code**

**Code de référence :**

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

![Une capture d'écran d'un programme informatique Description générée
automatiquement](./media/image51.png)

31. Cliquez sur **Accept** pour accepter le code.

![Une capture d'écran d'un programme informatique Description générée
automatiquement](./media/image52.png)

## **Exercice 3 : Documenter le code**

Documenter le code est toujours une tâche ennuyeuse et pénible.
Cependant, nous pouvons utiliser Copilot pour le documenter pour nous.
Dans le chat, demandez à Copilot de documenter le fichier nodeserver.js.

1.  **Sélectionnez tout** dans le fichier **nodeserver.js**.

2.  Depuis le chat Copilot, entrez !!**Documentez le fichier
    nodeserver.js** !! et cliquez sur Envoyer.

3.  Le Copilot génère une documentation détaillée du dossier.

![Une capture d'écran d'un ordinateur Description générée
automatiquement](./media/image53.png)

## **Exercice 4 : Construire des tests**

Nous allons créer des tests automatisés pour vérifier que la
fonctionnalité des points de terminaison précédents est correctement
implémentée. Les tests doivent être regroupés dans le fichier test.js.

Vous pouvez utiliser Copilot pour exécuter les tests. Il existe une
commande /tests que vous pouvez exécuter directement à partir de Copilot
Chat ou en sélectionnant le morceau de code pour lequel vous souhaitez
créer des tests et en utilisant la fonctionnalité en ligne de Copilot.

1.  Ouvrez le fichier test.js.

2.  Cliquez sur **Entrée** après le bloc **it** existant .

3.  Entrez le texte ci-dessous et cliquez sur **Entrée**.

**//add test to test DaysBetweenDates**![Une capture d'écran d'un
ordinateur Description générée automatiquement](./media/image54.png)

4.  Cela génère le bloc de test unitaire pour **DaysBetweenDates**.
    Cliquez sur **Accept** pour accepter le code.

![Une capture d'écran d'un ordinateur Description générée
automatiquement](./media/image55.png)

5.  Depuis le terminal, exécutez la commande ci-dessous !!**mocha
    test.js**!!![Un écran d'ordinateur avec du texte blanc Description
    générée automatiquement](./media/image56.png)

6.  Entrez le texte ci-dessous **//add test to check
    validatephoneNumber** et cliquez sur **Entrer**.

![Une capture d'écran d'un ordinateur Description générée
automatiquement](./media/image57.png)

7.  Cliquez sur **Accept** pour accepter le code généré par Copilot.

![Une capture d'écran d'un ordinateur Description générée
automatiquement](./media/image58.png)

8.  Depuis le terminal, exécutez la commande, !!**mocha test.js**!!.
    Vérifiez que le numéro de téléphone de validation est passé.

![Une capture d'écran d'un ordinateur Description générée
automatiquement](./media/image59.png)

9.  Entrez le texte ci-dessous et appuyez sur **Entrée**.

!!**//write test to validate validateSpanishDNI**!!

![Capture d'écran d'un programme informatique Description générée
automatiquement](./media/image60.png)

10. Acceptez le texte généré par Copilot.

11. Depuis le terminal, exécutez !!**mocha test.js**!! et vérifiez que
    le ValidateSpanishDNI a réussi.

![Une capture d'écran d'un programme informatique Description générée
automatiquement](./media/image61.png)

**Code de référence :**

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

test d'écriture pour valider le DNI espagnol

it('devrait renvoyer « valide » si le DNI espagnol 12345678A n'est pas
valide', (done) =\> {

http.get('http ://localhost :3000/ValidateSpanishDNI ?dni=12345678A',
(res) =\> {

let data = '' ;

res.on('données', (morceau) =\> {

données += morceau ;

});

res.on('fin', () =\> {

assert.equal(données, 'invalide') ;

done() ;

});

});

});

test d'écriture pour returnColorCode

it('devrait renvoyer « rouge » si la couleur est rouge', (fait) =\> {

http.get('http ://localhost :3000/ReturnColorCode ?color=red', (res) =\>
{

let data = '' ;

res.on('données', (morceau) =\> {

données += morceau ;

});

res.on('fin', () =\> {

assert.equal(données, '#FF0000') ;

done() ;

});

});

});

write test pour daysBetweenDates

it('devrait renvoyer « 1 » si les dates sont 2020-01-01 et 2020-01-02',
(fait) =\> {

http.get('http ://localhost :3000/DaysBetweenDates ?date1=2020-01-01&date2=2020-01-02',
(res) =\> {

let data = '' ;

res.on('données', (morceau) =\> {

données += morceau ;

});

res.on('fin', () =\> {

assert.equal(données, '1 jours') ;

done() ;

});

});

});

});

## **Exercice 5 : Création d'un fichier Dockerfile**

1.  Ouvrez le **dockerfile** à partir du dossier **node**.

![Une capture d'écran d'un ordinateur Description générée
automatiquement](./media/image62.png)

2.  Le fichier comprendra des commentaires sur la façon dont il doit
    être rempli.

3.  Appuyez sur **Ctrl+I** et tapez !!**/corriger**!. Cliquez sur l'
    icône **Send**.

4.  Le Copilot générera le contenu du fichier Docker. Cliquez sur
    **Accept**.

![Une capture d'écran d'un programme informatique Description générée
automatiquement](./media/image63.png)

5.  Depuis le terminal, exécutez la commande ci-dessous

!!**docker build -t mynodeapp .**!!

Il s'agit de créer l'image et de la marquer comme mynodeapp.

![Une capture d'écran d'un ordinateur Description générée
automatiquement](./media/image64.png)

6.  Exécutez docker sur le port **4000** à l'aide de la commande
    ci-dessous.

!!**docker run -p 4000:3000 -d mynodeapp** !!

![](./media/image65.png)

7.  Ouvrez le démon Docker pour voir que l'application a été
    conteneurisée et qu'elle s'exécute dans celui-ci.

![Une capture d'écran d'un ordinateur Description générée
automatiquement](./media/image66.png)

**Résumé:**

Dans cet atelier, nous avons appris à utiliser le Copilot dans un projet
de nœud
