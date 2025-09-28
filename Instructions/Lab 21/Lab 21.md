**Laboratoire 21 - Création d'une WebAPI minimale à l'aide de .NET et
d'une image Docker correspondante avec GitHub Copilot**

**Objectif:**

L'objectif est de créer une WebAPI minimale à l'aide de .NET 7.0 et
d'une image Docker correspondante à l'aide de GitHub Copilot. Ici, nous
utilisons GitHub Copilot autant que possible.

Essayez différentes choses et voyez ce que GitHub Copilot peut faire
pour vous, comme générer un Dockerfile ou une classe, ajouter des
commentaires, etc.

Avant d'exécuter cet atelier, nous allons d'abord installer les packages
logiciels nécessaires et configurer l'environnement

Exercice 0 : Installation et configuration de l'environnement

Vous devez télécharger et installer les packages logiciels suivants pour
configurer l'environnement afin d'exécuter cet atelier.

• dotnet-sdk-8.0

1.  Ouvrez le navigateur Edge.

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image1.jpeg)

2.  Dans le champ URL du navigateur, copiez-collez le lien pour
    télécharger le progiciel sur la machine virtuelle de votre
    laboratoire.

dotnet-sdk-8.0 ◊
https://dotnet.microsoft.com/en-us/download/dotnet/thank-you/sdk-8.0.401-windows-x64-installer

**Remarque :** Par défaut, les packages sont enregistrés dans le dossier
**des téléchargements (downloads)**.

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image2.jpeg)

3.  Installez le SDK .NET Allez dans le dossier **Downloads
    (C:\Users\Admin\Downloads)** et double-cliquez sur
    **dotnet-sdk-8.0.401** et suivez le processus d'installation.

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image3.jpeg)

**Exercice 1 : Configurer le projet dans VS Code**

1.  Ouvrez **Visual Studio Code** à partir du menu **Start**.

![Une capture d'écran d'un ordinateur Description générée
automatiquement](./media/image4.png)

2.  Sélectionnez **File -\> Open Folder…**

![Une capture d'écran d'un ordinateur Description générée
automatiquement](./media/image5.png)

3.  Sélectionnez le dossier **CopilotHackathon** dans C** :\Labfiles**
    et cliquez sur **Select Folder**.

![BrokenImage](./media/image6.png)

4.  Cliquez sur **Yes, I trust the authors**.

![Une capture d'écran d'un ordinateur Description générée
automatiquement](./media/image7.png)

**Exercice 2 : Introduction**

**Remarque :** Le code généré par Copilot peut différer selon les
exécutions. Dans les étapes où la génération de code est impliquée
ci-dessous, nous avons donné le **code de référence**. Veuillez
l'utiliser pour vérifier l'exactitude du code généré par Copilot ou pour
résoudre les erreurs le cas échéant.

1.  Ouvrez **Program.cs** à partir de **dotnet** -\> **MinimalAPI.**

![BrokenImage](./media/image8.png)

2.  Dans **MinimalAPI\Program.cs** après la ligne **ADD NEW ENDPOINTS
    HERE**(Ligne numéro 19), tapez // Hello World Get endpoint et
    appuyez sur **Entrée.** Le Copilot vous proposera le code en gris.

![Une capture d'écran d'un programme d'ordinateur Description générée
automatiquement](./media/image9.png)

3.  Une fois que vous avez obtenu le code généré par Copilot, vous
    pouvez **l'**accepter ou le **supprimer**. Pour accepter, cliquez
    sur le bouton Ctrl et la barre d'options apparaîtra sur le texte
    gris. Une autre option consiste simplement à appuyer sur la touche
    **Tab**.

**Code de référence :** app.MapGet("/", () =\> "Hello World!");

![BrokenImage](./media/image10.png)

4.  Le code ressemblera maintenant à ceci. **Save** le fichier.

![Une capture d'écran d'un programme d'ordinateur Description générée
automatiquement](./media/image11.png)

5.  Faites un clic droit sur le **dossier dotnet** et sélectionnez
    **Open in Integrated Terminal**

![Une capture d'écran d'un ordinateur Description générée
automatiquement](./media/image12.png)

6.  Depuis le terminal, exécutez la commande ci-dessous.

Test dotnet

![Une capture d'écran d'un écran d'ordinateur Description générée
automatiquement](./media/image13.png)

**Exercice 3 : Construire de nouvelles fonctionnalités**

1.  À côté du point de terminaison Hello World, ajoutez
    **DaysBetweenDates.**

2.  Appuyez sur **Ctrl+I** pour ouvrir le Copilot en ligne.

3.  Entrez le texte ci-dessous et cliquez sur le bouton **Send.**

4.  /DaysBetweenDates :

5.  Calculer les jours entre deux dates

Recevez par chaîne de requête deux paramètres date1 et date2, et
calculez les jours entre ces deux dates.

![Une capture d'écran d'un ordinateur Description générée
automatiquement](./media/image14.png)

6.  Le Copilot génère maintenant du **code** et l'entre dans le fichier
    **Program.cs**. Une fois cela fait, vous verrez deux options pour
    **Accept** ou **Discard**. **Accept** le code.

![Une capture d'écran d'un programme d'ordinateur Description générée
automatiquement](./media/image15.png)

7.  Une fois accepté, sélectionnez le code généré et appuyez sur
    **Ctrl+I.** Entrez, convertissez ce code en une seule ligne et
    appuyez sur **Entrée**. Cliquez sur Accepter une fois le code
    converti en une seule ligne.

**Code de référence** - app.MapGet("/DaysBetweenDates", (DateTime date1,
DateTime date2) =\> (date2 - date1).Days.ToString());

![Une capture d'écran d'un ordinateur Description générée
automatiquement](./media/image16.png)

8.  Entrez les déclarations ci-dessous (commentées) et cliquez sur
    **Entrer**.

Cliquez sur Accepter pour accepter le code généré par le Copilot.

/\*

/validatephonenumber:

receive by querystring a parameter called phoneNumber

validate phoneNumber with Spanish format, for example +34666777888

if phoneNumber is valid return true

\*/

**Code de référence :**

app.MapGet("/validatephonenumber", (string phonenumber) =\>
Regex.IsMatch(phonenumber, @"^(\\\[0-9\]{9})$").ToString());![Une
capture d'écran d'un programme d'ordinateur Description générée
automatiquement](./media/image17.png)

9.  Ajoutez le texte ci-dessous comme dans la fonction en ligne du
    Copilot, dans le fichier Program.cs et appuyez sur **Entrée**.

10. /validatespanishdni:

11. receive by querystring a parameter called dni

12. calculate DNI letter

13. if DNI is valid return "valid"

if DNI is not valid return "invalid"

Dans ce cas, vous voudrez peut-être voir plusieurs solutions de Copilot
pour choisir celle qui correspond le mieux à la façon de calculer la
lettre. Pour voir les 10 premières suggestions de Copilot, appuyez sur
ctrl + entrée.

Acceptez le code généré par GitHub.

**Code de référence :**

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

![Une capture d'écran d'un programme d'ordinateur Description générée
automatiquement](./media/image18.png)

14. Sélectionnez **Chat** dans le volet gauche.

![Une capture d'écran d'un ordinateur Description générée
automatiquement](./media/image19.png)

15. Entrez le texte ci-dessous et cliquez sur **Entrée**.

16. /returncolorcode :

Recevoir par querystring un paramètre appelé color read colors.json
fichier et retourner le champ rgba obtenir la variable de couleur de
querystring Itérer pour chaque coleur dans colors.json pour trouver la
couleur retourner le champ code.hex

![Un écran noir avec du texte blanc Description générée
automatiquement](./media/image20.png)

17. Veillez à ce que le Copilot donne une étape détaillée puis le code
    généré. Placez le curseur dans le fichier Program.cs, après le code
    **validatespanishdni**. Cliquez sur l'icône **Insert at cursor**
    pour coller le code dans le fichier.

**Code de référence :**

app.MapGet("/color", (string color) =\>

{

var colors =
JsonSerializer.Deserialize\<Color\[\]\>(File.ReadAllText("colors.json"));

return colors.First(c =\> c.Name == color).Code.HEX;

});

![Une capture d'écran d'un programme d'ordinateur Description générée
automatiquement](./media/image21.png)

![Une capture d'écran d'un programme d'ordinateur Description générée
automatiquement](./media/image22.png)

18. Assurez-vous qu'il n'y a pas d'erreurs dans le code généré. S'il y a
    erreur, conservez le code de référence comme référence et
    corrigez-le.

19. Dans ce cas, il y a une erreur, **Color does not contain definition
    for code**.

![Une capture d'écran d'un programme d'ordinateur Description générée
automatiquement](./media/image23.png)

20. Le code généré est mis à jour comme ci-dessous pour résoudre les
    erreurs.

![Une capture d'écran d'un ordinateur Description générée
automatiquement](./media/image24.png)

21. Entrez le texte ci-dessous et appuyez sur Entrée, puis vérifiez et
    acceptez le code généré par Copilot.

22. /\*

23. /tellmeajoke :

24. Effectuez un appel à l'API joke et renvoyez une blague aléatoire

\*/

**Code de référence :**

app.MapGet("/tellmeajoke", async () =\> {

var client = new HttpClient();

var response = await
client.GetAsync("https://official-joke-api.appspot.com/jokes/random");

var joke = await response.Content.ReadAsStringAsync();

return joke;

});

![Une capture d'écran d'un programme d'ordinateur Description générée
automatiquement](./media/image25.png)

REMARQUE : il s'agit d'un exemple où vous devrez peut-être utiliser vos
propres connaissances et votre jugement pour valider que Copilot suit
les meilleures pratiques. Ce n'est pas parce que Copilot imite ce que
font de nombreux développeurs que c'est toujours la bonne façon. Vous
devrez peut-être être très précis dans votre invite pour informer
Copilot des meilleures pratiques. Astuce : Faites attention à
HttpClient.

25. Copilot peut vous aider à apprendre de nouveaux cadres.

Entrez le texte ci-dessous dans Copilot en ligne et appuyez sur
**Entrée**.

/parseurl :

Récupère un paramètre de querystring appelé someurl

Analysez l'URL et renvoyez le protocole, l'hôte, le port, le chemin, la
chaîne de requête et le hachage

Retourner l'hôte analysé

**Code de référence :**

appli. MapGet(« /parseurl », (chaîne someurl) =\> {

var uri = new Uri(someurl);

var host = uri.Host;

var protocol = uri.Scheme;

var port = uri.Port;

var path = uri.AbsolutePath;

var query = uri.Query;

var hash = uri.Fragment;

return host;

});

![Une capture d'écran d'un ordinateur Description générée
automatiquement](./media/image26.png)

26. Copilot peut également aider avec ce type de commandes localement.
    Cette fonctionnalité est appelée Copilot dans l'interface de ligne
    de commande. Vous pouvez en savoir plus sur cette fonctionnalité
    ici.

Ouvrez Copilot Inline, entrez le texte ci-dessous et appuyez sur
**Entrée**.

/listfiles :

Obtenir le répertoire actuel

Récupérer la liste des fichiers dans le répertoire courant

Retourner la liste des fichiers

**Code de référence :**

app.MapGet("/listfiles", () =\> {

var currentDirectory = Directory.GetCurrentDirectory();

var files = Directory.GetFiles(currentDirectory);

return files;

});

![Une capture d'écran d'un programme d'ordinateur Description générée
automatiquement](./media/image27.png)

27. Entrez le texte ci-dessous dans le copilote en ligne et appuyez sur
    **Entrée**.

28. /calculatememoryconsumption :

Renvoie la consommation de mémoire du processus en Go, arrondie à 2
décimales

**Code de référence :**

// Calculate memory consumption endpoint

app.MapGet("/calculatememoryconsumption", () =\>

{

var process = System.Diagnostics.Process.GetCurrentProcess();

var memoryUsage = process.WorkingSet64 / (1024.0 \* 1024 \* 1024); //
Convert to GB

return Math.Round(memoryUsage, 2);

});

![Une capture d'écran d'un programme d'ordinateur Description générée
automatiquement](./media/image28.png)

29. Entrez le texte ci-dessous dans Copilot en ligne et appuyez sur
    **Entrée**.

30. /randomPays européen :

31. Faire un tableau des pays européens et de ses codes iso

32. Retourner un pays aléatoire à partir du tableau

Retourner le pays et son code iso

**Code de référence :**

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

![Une capture d'écran d'un programme d'ordinateur Description générée
automatiquement](./media/image29.png)

**Exercice 4 : Documenter le code**

1.  Ouvrez la fenêtre de discussion.

![Une capture d'écran d'un ordinateur Description générée
automatiquement](./media/image19.png)

2.  Tapez Documentez **le fichier Program.cs** et sélectionnez **Send**.

GitHubCopiot génère une brève **documentation** du fichier
**Program.cs**.

![Une capture d'écran d'un programme d'ordinateur Description générée
automatiquement](./media/image30.png)

**Exercice 5 : Construire des tests**

1.  Ouvrez **Program.cs** fichier.

2.  Sélectionnez le point de terminaison **DaysBetweenDates**, appuyez
    sur **Ctrl+I** pour ouvrir le Copilot en ligne.

Dans le Copilot en ligne, tapez **/tests** et cliquez sur le bouton
**Send.**

![Une capture d'écran d'un programme d'ordinateur Description générée
automatiquement](./media/image31.png)

3.  Copiez le test généré.

![Une capture d'écran d'un programme d'ordinateur Description générée
automatiquement](./media/image32.png)

4.  Ouvrez le IntegrationTests.cs à partir du fichier MinimalAPI.Tests.

![Une capture d'écran d'un ordinateur Description générée
automatiquement](./media/image33.png)

5.  Collez-le dans le fichier cs après le bloc de test du Hello World.
    Résolvez tous les problèmes qui pourraient survenir.

6.  Ouvrez le chat Copilot à partir du volet de gauche.

![Une capture d'écran d'un ordinateur Description générée
automatiquement](./media/image19.png)

7.  Tapez /tests, la commande pour créer des unités de test et appuyez
    sur **Entrée**. Le Copilot génère un fichier de test. Copiez son
    contenu.

![Une capture d'écran d'un ordinateur Description générée
automatiquement](./media/image34.png)

![Une capture d'écran d'un programme d'ordinateur Description générée
automatiquement](./media/image35.png)

8.  Ouvrez **IntegrationTests.cs** à partir du **MinimalAPI.Tests**.

![Une capture d'écran d'un ordinateur Description générée
automatiquement](./media/image33.png)

9.  Remplacez le contenu du fichier par le code généré par Copilot et
    enregistrez-le.

**Important :** Vérifiez s'il y a des erreurs et corrigez-les à l'aide
de la commande /fix ou manuellement. Utilisez le code de référence
ci-dessous pour résoudre le problème.

10. Si les tests ne sont pas générés pour tous les points de
    terminaison, à partir du chat, spécifiez le nom du point de
    terminaison et demandez au Copilot de générer le test comme
    ci-dessous. Mettez à jour les noms de point de terminaison en
    fonction de ceux qui sont mis à jour et de ceux qui sont manquants
    dans votre test.

generate test units for moviesbydirector, parseurl, listfiles,
calculatememoryconsumption and randomeuropeancountry

**Code de référence :**

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

} ![Capture d'écran d'un programme d'ordinateur Description générée
automatiquement](./media/image36.png)

11. Depuis le terminal, exécutez la commande **dotnet test**

12. Si le test réussit, vous devriez voir une sortie similaire à celle
    de la capture d'écran ci-dessous.

![BrokenImage](./media/image37.png)

13. Vous pouvez ajouter d'autres tests si nécessaire.

**Exercice 6 : Création d'un fichier Dockerfile**

1.  Faites un clic droit sur le dossier **dotnet** et sélectionnez **New
    File** et nommez le fichier **Dockerfile**.

![BrokenImage](./media/image38.png)

2.  Nommez le fichier **Dockerfile**.

![Une capture d'écran d'un ordinateur Description générée
automatiquement](./media/image39.png)

3.  Dans le fichier nouvellement créé, appuyez sur **Ctrl+I**, tapez le
    texte ci-dessous et appuyez sur **Entrée**.

**Générer du contenu pour Dockerfile pour .NET 8 Nom du projet -
MinimalAPI**

![Une capture d'écran d'un ordinateur Description générée
automatiquement](./media/image40.png)

4.  Acceptez le code généré.

![Une capture d'écran d'un programme d'ordinateur Description générée
automatiquement](./media/image41.png)

5.  Enregistrez le fichier. À partir du terminal, exécutez la commande
    ci-dessous.

docker build -t dotnetapp .

Utilisez le code de référence pour résoudre les erreurs le cas échéant.

**Code de référence :**

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

ENTRYPOINT \["dotnet",
"MinimalAPI.dll"\]![BrokenImage](./media/image42.png)

6.  Exécutez la commande ci-dessous pour exécuter l'application sur le
    port 8080

docker run -d -p 8080:80 --name dotnetapp dotnetapp

![BrokenImage](./media/image43.png)

7.  Maintenant, nous avons l'application dotnet qui s'exécute dans le
    docker.

![Une capture d'écran d'un ordinateur Description générée
automatiquement](./media/image44.png)
