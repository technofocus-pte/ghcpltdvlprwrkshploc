# **Laboratório 20 - Ative o GitHub Copilot usando Nodejs**

**Objetivo:**

Este laboratório tem como objetivo ajudar a compreender o projeto de
demonstração para a execução de laboratórios para avaliar a viabilidade
do Copilot.

Antes de executar este laboratório, vamos primeiro instalar os pacotes
de software necessários e configurar o ambiente.

**Tarefa 0: Instalar e configurar o ambiente**

Você precisa baixar e instalar os seguintes pacotes de software para
configurar o ambiente para executar este laboratório.

1.  Node.js

2.  mocha

&nbsp;

1.  Abra o navegador Edge.

> ![A screenshot of a computer Description automatically
> generated](./media/image1.png)

2.  No campo URL do navegador, copie e cole o link para baixar os
    pacotes de software para a VM do seu laboratório.

&nbsp;

1.  Node.js and mvn 🡪
    <https://nodejs.org/dist/v20.16.0/node-v20.16.0-x64.msi>

2.  mocha (não é necessário fazer download)

> **Observação:** por padrão, os pacotes serão salvos na pasta de
> **downloads.**
>
> ![A screenshot of a computer Description automatically
> generated](./media/image2.png)

1.  **Install Node.js and mvn**

&nbsp;

1.  Vá até a pasta **Downloads (C:\Users\Admin\Downloads)** e dê um
    duplo clique em **node-v20.16.0-x64.msi.**

> ![A screenshot of a computer Description automatically
> generated](./media/image3.png)

2.  Na janela “Node.js setup wizard” clique em **Next**.

> ![A screenshot of a computer Description automatically
> generated](./media/image4.png)

3.  Aceite o **EULA** e clique em **Next**.

> ![A screenshot of a software license agreement Description
> automatically generated](./media/image5.png)

4.  Mantenha a pasta de destino padrão e clique em **Next**.

> ![A screenshot of a computer Description automatically
> generated](./media/image6.png)

5.  Clique em **Add to the PATH** e depois clique em **Next**.

> ![A screenshot of a computer program Description automatically
> generated](./media/image7.png)

6.  Na janela **Tools for native Modules**, marque a **caixa de
    seleção** e clique em Next.

> ![A screenshot of a computer Description automatically
> generated](./media/image8.png)

7.  Clique em **Install**.

> ![A screenshot of a computer Description automatically
> generated](./media/image9.png)
>
> **Observação:** Se aparecer o pop-up do **User Access Control**,
> clique em **Yes** para continuar**.**

8.  Clique em **Finish** quando concluir.

> ![A screenshot of a computer Description automatically
> generated](./media/image10.png)

9.  O terminal **Cmd** será aberto. Pressione qualquer tecla para
    continuar.

> ![A screenshot of a computer Description automatically
> generated](./media/image11.png)
>
> Observação: Você pode notar um atraso após pressionar uma tecla.
> Aguarde alguns instantes para que a instalação prossiga.

10. Clique em **Yes** para continuar na janela do UAC.

> ![A screenshot of a computer error Description automatically
> generated](./media/image12.png)

11. O **Windows PowerShell** será aberto exibindo os detalhes da
    instalação.

> ![A screenshot of a computer program Description automatically
> generated](./media/image13.png)

12. Quando a instalação for concluída, pressione **Enter** para sair do
    PowerShell.

> ![A computer screen with text on it Description automatically
> generated](./media/image14.png)

2.  **Install mocha**

&nbsp;

1.  Open the command prompt

> ![A screenshot of a computer Description automatically
> generated](./media/image15.png)

2.  Primeiro, execute o seguinte comando.

> +++npm install --global mocha+++
>
> ![A screenshot of a computer Description automatically
> generated](./media/image16.png)
>
> ![A screenshot of a computer screen Description automatically
> generated](./media/image17.png)

3.  Em seguida, execute o seguinte comando

> +++npm install axios+++
>
> ![A screenshot of a computer screen Description automatically
> generated](./media/image18.png)
>
> ![A screenshot of a computer Description automatically
> generated](./media/image19.png)
>
> Agora você concluiu a instalação do **mocha**. Feche o terminal para
> prosseguir com a instalação de outros pacotes.

## **Exercício 1: Introdução**

1.  No Visual Studio, abra o arquivo **nodeserver.js** em exercisefiles
    -\> node.

![A screenshot of a computer Description automatically
generated](./media/image20.png)

2.  Precisamos começar a codificação para o servidor node.js que irá
    expor um método chamado "get", que retornará o valor da chave
    passada na string de consulta. Vamos usar o Copilot para nos ajudar
    com isso.

3.  Pressione **Ctrl+I**, cole os comandos abaixo para que o Copilot
    gere o código e clique em **Send**.

**// write a nodejs server that will expose a method call "get" that
will return the value of the key passed in the query string**

**// example: http://localhost:3000/get?key=hello**

**// if the key is not passed, return "key not passed"**

**// if the key is passed, return "hello" + key**

**// if the url has other methods, return "method not supported"**

**// when server is listening, log "server is listening on port 3000"**

![A screenshot of a computer Description automatically
generated](./media/image21.png)

4.  O Copilot gera o código e o exibe. Clique em **Accept** para
    aceitá-lo.

![A screenshot of a computer program Description automatically
generated](./media/image22.png)

5.  Clique com o botão direito na pasta **node** e selecione **Open in
    Integrated Terminal**.

![A screenshot of a computer Description automatically
generated](./media/image23.png)

6.  Quando o terminal for aberto, execute o comando abaixo nele.

!!**mocha test.js**!!

7.  Você deverá obter um resultado como **1 Passing**, conforme mostrado
    na captura de tela abaixo.

![A computer screen with white text Description automatically
generated](./media/image24.png)

8.  Este é o teste de unidade para o método no nodeserver.js e foi
    aprovado.

9.  Agora continuaremos adicionando diferentes métodos ao servidor
    usando o Copilot.

## **Exercício 2: Criando novas funcionalidades**

O exercício consiste em criar um servidor web usando Nodejs que atenda
às solicitações de várias funcionalidades.

1.  Adicione a solicitação da funcionalidade **DaysBetweenDates** que o
    servidor deve atender.

2.  Pressione **Enter** após o fim da condição **if** – **pathname**
    **== ‘/get’**.

**Observação**: Consulte a chave em destaque em vermelho onde você
precisa pressionar **Enter**.

![](./media/image25.png)

3.  Pressione **Ctrl+I** para abrir o recurso Copilot inline, digite o
    seguinte e clique em **Send**.

> **/DaysBetweenDates:**
>
> **Calculate days between two dates**
>
> **receive by query string 2 parameters date1 and date 2, and calculate
> the days between those two dates.**

**Código de referência:**

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

4.  O Copilot gera o código. Clique em **Accept** para aceitar o código.
    Observe que o código gerado é um bloco **else if**, onde a
    requisição é **DaysBetweenDates**.

![](./media/image27.png)

5.  Clique em **Enter** após o bloco **DaysBetweenDates**.

6.  Digite o bloco de comentário abaixo e pressione **Enter**.

**/\***

**/Validatephonenumber:**

**Receive by querystring a parameter called phoneNumber**

**validate phoneNumber with proper Spanish format, for example
34666666666**

**if phoneNumber is valid return "valid"**

**if phoneNumber is not valid return "invalid"**

**\*/**

**Código de referência:**

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

![A screenshot of a computer Description automatically
generated](./media/image28.png)

7.  O Copilot gera o código. Clique em **Accept** para aceitar o código.

![A screenshot of a computer program Description automatically
generated](./media/image29.png)

8.  **Click Enter** após o bloco **Validatephonenumber** para adicionar
    o próximo bloco de código.

9.  Copie e cole o texto abaixo no arquivo .js.

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
> **Código de referência:**
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
> ![A screen shot of a computer program Description automatically
> generated](./media/image30.png)

10. Depois que o conteúdo acima for colado, o Copilot gera o código que
    será exibido logo abaixo do comentário. Clique em **Accept** para
    aceitar o código.

![A screenshot of a computer program Description automatically
generated](./media/image31.png)

11. Abra o chat do Copilot no painel de navegação à esquerda.

![A black rectangular object with white symbols Description
automatically generated](./media/image32.png)

12. Cole o conteúdo abaixo no chat e clique no botão **Send**.

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
> **Código de referência:**

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

> **Observação:** O Copilot utilizará por padrão o arquivo aberto como
> contexto para gerar a sugestão.

![A screenshot of a computer program Description automatically
generated](./media/image33.png)

13. Mantenha o cursor após o bloco **ValidateSpanishDNI** e clique no
    ícone ícone Inserir no cursor no chat. Isso **copia** o código
    gerado pelo Copilot do chat para o arquivo server.js no local
    mencionado.

![A screenshot of a computer program Description automatically
generated](./media/image34.png)

14. Verifique se há erros. Neste código gerado, há um erro, pois há uma
    declaração constante entre os blocos else if.

![A screen shot of a computer Description automatically
generated](./media/image35.png)

15. Pressione **Ctrl+I** para abrir o Copilot Inline, digite
    !!**/fix**!! e clique no botão **Send**.

![A screenshot of a computer program Description automatically
generated](./media/image36.png)

16. O Copilot gera uma solução se conseguir encontrar uma. Aceite ou
    descarte a solução com base em quão precisa ela for.

![A screenshot of a computer Description automatically
generated](./media/image37.png)

17. Aqui, estamos movendo a declaração da constante para dentro do bloco
    else if de returncolors para resolver o erro.

![A screen shot of a computer program Description automatically
generated](./media/image38.png)

**Importante:** O código e a resolução podem ser diferentes para você,
dependendo do que o Copilot gera.

18. Após o bloco adicionado, pressione **Ctrl+I** para abrir o recurso
    Copilot inline, cole o conteúdo abaixo e clique em **Send**.

**/TellMeAJoke:**

**Make a call to the joke api and return a random joke using axios
(<https://official-joke-api.appspot.com/random_joke>)**

Código de referência:

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

![A screenshot of a computer Description automatically
generated](./media/image39.png)

19. Clique em **Accept** para aceitar o código gerado pelo Copilot.

![A screenshot of a computer Description automatically
generated](./media/image40.png)

20. Após o bloco de código gerado, pressione **Ctrl+I**, digite o texto
    abaixo e clique no botão **Send**.

**/MoviesByDirector:**

**Receive by querystring a parameter called director**

**Make a call to the movie api and return a list of movies of that
director using axios**

**Return the full list of movies**

**Código de referência:**

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

![A screenshot of a computer Description automatically
generated](./media/image41.png)

21. Clique em **Accept** para aceitar o código.

![A screenshot of a computer program Description automatically
generated](./media/image42.png)

22. Após o bloco de código gerado, pressione **Ctrl+I**, digite o texto
    abaixo e clique no botão **Send**.

**/ParseUrl:**

**Retrieves a parameter from querystring called someurl**

**Parse the url and return the protocol, host, port, path, querystring
and hash**

**Return the parsed host**

**Código de referência:**

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

![A screenshot of a computer Description automatically
generated](./media/image43.png)

23. Clique em **Accept** para aceitar o código.

![A screenshot of a computer program Description automatically
generated](./media/image44.png)

24. Após o bloco de código gerado, pressione **Ctrl+I**, digite o texto
    abaixo e clique no botão **Send**.

**/GetFullTextFile:**

**Read \`sample.txt\`\` and return lines that contains the word
"Fusce"**

**Código de referência:**

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

**OBSERVAÇÃO:** Tenha cuidado com essa implementação, pois ela
normalmente lê todo o conteúdo do arquivo antes de analisá-lo. Isso faz
com que o uso de memória seja alto e pode falhar quando os arquivos
forem muito grandes.

![A screenshot of a computer Description automatically
generated](./media/image45.png)

25. Clique em **Accept** para aceitar o código.

![A screenshot of a computer program Description automatically
generated](./media/image46.png)

26. Após o bloco de código gerado, pressione **Ctrl+I**, digite o texto
    abaixo e clique no botão **Send**.

**/GetLineByLinefromtTextFile:**

**Read sample.txt line by line**

**Create a promise to read the file line by line, and return a list of
lines that contains the word "Fusce"**

**Return the list of lines**

**Código de referência:**

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

![A screenshot of a video Description automatically
generated](./media/image47.png)

27. Clique em **Accept** para aceitar o código.

![A screenshot of a computer program Description automatically
generated](./media/image48.png)

28. Após o bloco de código gerado, pressione **Ctrl+I**, digite o texto
    abaixo e clique no botão **Send**.

**/CalculateMemoryConsumption:**

**Return the memory consumption of the process in GB, rounded to 2
decimals**

**Código de referência:**

else if (req.url.startsWith('/CalculateMemoryConsumption')) {

//return the memory consumption of the process in GB, rounded to 2
decimals

var memory = process.memoryUsage().heapUsed / 1024 / 1024;

res.end(memory.toFixed(2) + " GB");

}

![A screenshot of a computer Description automatically
generated](./media/image49.png)

29. Clique em **Accept** para aceitar o código.

![A screenshot of a computer program Description automatically
generated](./media/image50.png)

30. Após o bloco de código gerado, pressione **Ctrl+I**, digite o texto
    abaixo e clique no botão **Send**.

**/RandomEuropeanCountry:**

**Make an array of european countries and its iso codes**

**Return a random country from the array**

**Return the country and its iso code**

**Código de referência:**

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

![A screenshot of a computer program Description automatically
generated](./media/image51.png)

31. Clique em **Accept** para aceitar o código.

![A screenshot of a computer program Description automatically
generated](./media/image52.png)

## **Exercício 3: Documentar o código**

Documentar código geralmente é uma tarefa chata e trabalhosa. No
entanto, podemos usar o Copilot para documentar automaticamente o
arquivo nodeserver.js.

1.  **Selecione todo** o conteúdo do arquivo **nodeserver.js**.

2.  No Copilot Chat, digite !!**document the nodeserver.js file**!! e
    clique em **Send**.

3.  O Copilot irá gerar uma documentação detalhada para o arquivo.

![A screenshot of a computer Description automatically
generated](./media/image53.png)

## **Exercício 4: Criando testes**

Nós vamos criar testes automatizados para verificar se a funcionalidade
dos endpoints anteriores foi implementada corretamente. Os testes devem
estar juntos no arquivo test.js.

Você pode aproveitar o Copilot para executar os testes. Existe um
comando /tests que você pode executar diretamente a partir do Copilot
Chat ou selecionando o trecho de código para o qual deseja criar testes
e usando o recurso Copilot inline.

1.  Abra o arquivo test.js.

2.  Clique em **Enter** após o bloco **it** existente.

3.  Digite o texto abaixo e clique em **Enter**.

**//add test to test DaysBetweenDates**

![A screen shot of a computer Description automatically
generated](./media/image54.png)

4.  Isso gera o bloco de teste unitário para **DaysBetweenDates**.
    Clique em **Accept** para aceitar o código.

![A screenshot of a computer Description automatically
generated](./media/image55.png)

5.  No terminal, execute o comando abaixo !!**mocha test.js**!!

![A computer screen with white text Description automatically
generated](./media/image56.png)

6.  Digite o texto abaixo **//add test to check validatephoneNumber** e
    clique em **Enter**.

![A screen shot of a computer Description automatically
generated](./media/image57.png)

7.  Clique em **Accept** para aceitar o código gerado pelo Copilot.

![A screenshot of a computer Description automatically
generated](./media/image58.png)

8.  No terminal, execute o comando, !!**mocha test.js**!!. Verifique se
    a validação do número de telefone foi aprovada.

![A screenshot of a computer Description automatically
generated](./media/image59.png)

9.  Digite o texto abaixo e pressione **Enter**.

!!**//write test to validate validateSpanishDNI**!!

![A screen shot of a computer program Description automatically
generated](./media/image60.png)

10. Aceite o texto gerado pelo Copilot.

11. No terminal, execute !!**mocha test.js**!! e verifique se o
    ValidateSpanishDNI foi aprovado.

![A screenshot of a computer program Description automatically
generated](./media/image61.png)

**Código de referência:**

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

## **Exercício 5: Criar um Dockerfile**

1.  Abra o **dockerfile** da pasta **node**.

![A screenshot of a computer Description automatically
generated](./media/image62.png)

2.  O arquivo consistirá em comentários sobre como ele deve ser
    preenchido.

3.  Pressione **Ctrl+I** e digite !!**/fix**!!. Clique no ícone
    **Send**.

4.  O Copilot irá gerar o conteúdo do Docker file. Clique em **Accept**.

![A screenshot of a computer program Description automatically
generated](./media/image63.png)

5.  A partir do terminal, execute o comando abaixo:

!!**docker build -t mynodeapp .**!!

Isto serve para criar a imagem e marcá-la como mynodeapp.

![A screenshot of a computer Description automatically
generated](./media/image64.png)

6.  Execute o docker na porta **4000** usando o comando abaixo:

!!**docker run -p 4000:3000 -d mynodeapp**!!

![](./media/image65.png)

7.  Abra o Docker daemon para verificar que a aplicação foi
    conteinerizada e está em execução nele.

![A screenshot of a computer Description automatically
generated](./media/image66.png)

**Resumo:**

Neste laboratório, aprendemos como usar o Copilot em um projeto baseado
em nós.
