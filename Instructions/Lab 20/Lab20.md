# **实验室 20 - 使用 Nodejs 激活 GitHub Copilot**

**客观的：**

本实验室旨在帮助了解用于运行实验室以评估 Copilot 可行性的演示项目。

在执行本练习之前，让我们先安装必要的软件包并设置环境。

**任务 0：安装和设置环境**

您需要下载并安装以下软件包来设置环境以执行本练习。

1.  Node.js

2.  mocha

<!-- -->

1.  打开 Edge 浏览器。

> ![](./media/image1.png)

2.  在浏览器 URL 字段中，复制粘贴链接以将软件包下载到实验室 VM。

<!-- -->

1.  Node.js和 MVN 🡪
    <https://nodejs.org/dist/v20.16.0/node-v20.16.0-x64.msi>

> b.mocha （无需下载）
>
> **注意**：默认情况下，包将保存在**downloads**文件夹中。
>
> ![](./media/image2.png)

1.  **安装Node.js和 mvn**

<!-- -->

1.  转到 **Downloads**（**C：\Users\Admin\Downloads**）
    文件夹，然后双击node-v20.16.0-x64.msi **。**

> ![](./media/image3.png)

2.  在“Node.js setup wizard”窗口中，单击 **Next**。

> ![](./media/image4.png)

3.  接受 EULA 并单击 **Next**。

> ![](./media/image5.png)

4.  保留默认目标文件夹，然后单击“**Next**”。

> ![](./media/image6.png)

5.  单击“**Add to the PATH**”，然后单击“**Next**”。

> ![](./media/image7.png)

6.  在“**Tools for native
    Modules**”窗口中，选中该**复选框**并单击“Next”。

> ![](./media/image8.png)

7.  单击 **Install**。

> ![](./media/image9.png)
>
> 注意：如果您看到 **User Access Control** 弹出窗口，请单击 **Yes**
> 继续。

8.  完成后点击 **Finish**。

> ![](./media/image10.png)

9.  **Cmd** 终端打开。按任意键继续..

> ![](./media/image11.png)
>
> 注意：按下某个键后，您可能会看到延迟。请等待一段时间以继续安装。

10. 单击“**Yes**”在 UAC 窗口中继续。

> ![](./media/image12.png)

11. **Windows Powershell** 打开，显示安装详细信息。

> ![](./media/image13.png)

12. 安装完成后，键入 **Enter** 退出 PowerShell。

> ![](./media/image14.png)

2.  **安装 mocha**

<!-- -->

1.  打开命令提示符

> ![](./media/image15.png)

2.  首先运行以下命令。

> +++npm install --global mocha+++
>
> ![](./media/image16.png)
>
> ![](./media/image17.png)

3.  接下来运行以下命令

> +++npm install axios+++
>
> ![](./media/image18.png)
>
> ![](./media/image19.png)
>
> 现在您已经完成了**mocha** 的安装。关闭终端以继续安装其他软件包。

## **练习 1：简介**

1.  在 Visual Studio 中， 从 exercisefiles -\>
    节点打开**nodeserver.js**。

![](./media/image20.png)

2.  我们需要开始为节点编码。js
    服务器，该服务器将公开一个方法调用“get”，该调用将返回查询字符串中传递的键的值。让我们使用
    Copilot 来帮助我们解决这个问题。

3.  按 **Ctrl+I** 并粘贴以下命令，让 Copilot 生成代码并点击 **Send**。

**// write a nodejs server that will expose a method call "get" that
will return the value of the key passed in the query string**

**// example: http://localhost:3000/get?key=hello**

**// if the key is not passed, return "key not passed"**

**// if the key is passed, return "hello" + key**

**// if the url has other methods, return "method not supported"**

**// when server is listening, log "server is listening on port 3000"**

![](./media/image21.png)

4.  Copilot 生成代码并显示。单击 **“Accept”** 以接受它。

![](./media/image22.png)

5.  右键单 **node** 点文件夹，然后选择在集成终端中打开。

![](./media/image23.png)

6.  打开终端后，从中执行以下命令。

!!**mocha test.js**!!

7.  您应该得到的结果为 **1 Passing**，如下面的屏幕截图所示。

![](./media/image24.png)

8.  这是nodeserver.js中方法的单元测试，它已通过。

9.  我们将继续使用 Copilot 向服务器添加不同的方法。

## **练习 2：构建新功能**

该练习包括使用 Nodejs 构建一个 Web
服务器，该服务器可满足各种功能的请求。

1.  添加 服务器必须参与的 **DaysBetweenDates** 功能请求。

2.  在 **if** 条件 **– pathname == '/get'** 结束后按 **Enter**。

**请注意：** 请参阅红色突出显示的大括号，您需要按 **Enter** 键

![](./media/image25.png)

3.  按 **Ctrl+I** 打开 Copilot 内联功能，输入以下内容并单击 **Send**。

> **/DaysBetweenDates:**
>
> **Calculate days between two dates**
>
> **receive by query string 2 parameters date1 and date 2, and calculate
> the days between those two dates.**

**Reference Code:**

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

4.  Copilot 生成代码。点击 **Accept**
    接受代码。请注意，生成的代码是请求中的 **else if** 块，其中是
    **DaysBetweenDates**。

![](./media/image27.png)

5.  单击 **DaysBetweenDates** 块后的 **Enter**。

6.  输入下面的评论块并按 **Enter**。

**/\***

**/Validatephonenumber:**

**Receive by querystring a parameter called phoneNumber**

**validate phoneNumber with proper Spanish format, for example
34666666666**

**if phoneNumber is valid return "valid"**

**if phoneNumber is not valid return "invalid"**

**\*/**

**Reference Code:**

else if (req.url.startsWith('/Validatephonenumber')) {

//get phoneNumber var from querystring

var queryData = url.parse(req.url, true).query;

var phoneNumber = queryData.phoneNumber;

//validate phoneNumber with Spanish format

var regex = /^(\\34\|0034\|34)?\[ -\]\*(6\|7)\[ -\]\*(\[0-9\]\[
-\]\*){8}\$/;

//if phoneNumber is valid return "valid"

if (regex.test(phoneNumber)) {

res.end("valid");

}

//if phoneNumber is not valid return "invalid"

else {

res.end("invalid");

}

}

![](./media/image28.png)

7.  Copilot 生成代码。单击 **“Accept”** 以接受代码。

![](./media/image29.png)

8.  单击 **Validatephonenumber** 块后的 **Enter** 以添加下一个代码块。

9.  将以下文本复制并粘贴到 js 文件中。

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
> **Reference Code:**
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
> ![](./media/image30.png)

10. 粘贴上述内容后，Copilot 会生成代码，该代码显示在评论下方。点击
    **Accept** 接受代码。

![](./media/image31.png)

11. 从左侧导航窗格打开 Copilot 聊天。

![](./media/image32.png)

12. 将以下内容粘贴到聊天中，然后单击“**Send”**按钮。

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
> **Reference code:**

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

> **注意：** 默认情况下，Copilot 将使用打开的文件作为上下文来生成建议。

![](./media/image33.png)

13. 将光标保留在 **ValidateSpanishDNI**
    块之后，然后单击聊天中的“插入光标处”图标。这**会将** Copilot
    生成的代码从聊天复制到上述位置的服务器 js 文件。

![](./media/image34.png)

14. 检查是否有错误。在此生成的代码中，存在错误，因为 else if
    块之间有一个常量声明。

![](./media/image35.png)

15. 按 **Ctrl+I** 打开 Copilot Inline，输入 !!**/fix**!!
    并单击“**Send**”按钮

![](./media/image36.png)

16. 如果可以找到解决方案，Copilot
    会生成解决方案。根据解决方案的准确性接受或放弃解决方案。

![](./media/image37.png)

17. 在这里，我们将常量声明移动到 returncolors 的 else if
    块中以解决错误。

![](./media/image38.png)

**重要提示：** 根据 Copilot
生成的代码和解决方案，代码和解决方案可能有所不同。

18. 添加块后，按 **Ctrl+I** 打开 Copilot 内联功能，粘贴以下内容并单击
    **Send**。

**/TellMeAJoke:**

**Make a call to the joke api and return a random joke using axios
(<https://official-joke-api.appspot.com/random_joke>)**

Reference code:

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

![](./media/image39.png)

19. 单击 **“Accept”** 以接受 Copilot 生成的代码。

![](./media/image40.png)

20. 生成代码块后，按 **Ctrl+I**，输入以下文本，然后单击 **Send** 按钮。

**/MoviesByDirector:**

**Receive by querystring a parameter called director**

**Make a call to the movie api and return a list of movies of that
director using axios**

**Return the full list of movies**

**Reference code:**

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

![](./media/image41.png)

21. 点击 **Accept** 接受代码。

![](./media/image42.png)

22. 生成代码块后，按 **Ctrl+I**，输入以下文本，然后单击 **Send** 按钮。

**/ParseUrl:**

**Retrieves a parameter from querystring called someurl**

**Parse the url and return the protocol, host, port, path, querystring
and hash**

**Return the parsed host**

**Reference code:**

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

![](./media/image43.png)

23. 点击 **Accept** 接受代码。

![](./media/image44.png)

24. 生成代码块后，按 **Ctrl+I**，输入以下文本，然后单击 **Send** 按钮。

**/GetFullTextFile:**

**Read \`sample.txt\`\` and return lines that contains the word
"Fusce"**

**Reference code:**

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

**注意：**
小心此实现，因为它通常会在分析文件之前读取文件的全部内容，因此内存使用率很高，并且当文件太大时可能会失败。

![](./media/image45.png)

25. 点击 **Accept** 接受代码。

![](./media/image46.png)

26. 生成代码块后，按 **Ctrl+I**，输入以下文本，然后单击 **Send** 按钮。

**/GetLineByLinefromtTextFile:**

**Read sample.txt line by line**

**Create a promise to read the file line by line, and return a list of
lines that contains the word "Fusce"**

**Return the list of lines**

**Reference code:**

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

![](./media/image47.png)

27. 点击 **Accept** 接受代码。

![](./media/image48.png)

28. 生成代码块后，按 **Ctrl+I**，输入以下文本，然后单击 **Send** 按钮。

**/CalculateMemoryConsumption:**

**Return the memory consumption of the process in GB, rounded to 2
decimals**

**Reference code:**

else if (req.url.startsWith('/CalculateMemoryConsumption')) {

//return the memory consumption of the process in GB, rounded to 2
decimals

var memory = process.memoryUsage().heapUsed / 1024 / 1024;

res.end(memory.toFixed(2) + " GB");

}

![](./media/image49.png)

29. 点击 **Accept** 接受代码。

![](./media/image50.png)

30. 生成代码块后，按 **Ctrl+I**，输入以下文本，然后单击 **Send**按钮。

**/RandomEuropeanCountry:**

**Make an array of european countries and its iso codes**

**Return a random country from the array**

**Return the country and its iso code**

**Reference code:**

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

![](./media/image51.png)

31. 点击 **Accept** 接受代码。

![](./media/image52.png)

## **练习 3：记录代码**

记录代码始终是一项枯燥而痛苦的任务。但是，我们可以使用 Copilot
为我们记录它。在聊天中，要求 Copilot 记录nodeserver.js文件。

1.  选择**nodeserver.js**文件中的**所有内容。**

2.  在 Copilot 聊天中，输入 !!**document the nodeserver.js
    file**!!，然后单击发送。

3.  Copilot 生成文件的详细文档。

![](./media/image53.png)

## **练习 4：构建测试**

我们将创建自动化测试来检查先前端点的功能是否正确实现。测试应一起放在test.js文件中。

您可以利用 Copilot 运行测试。有一个 /tests 命令，您可以直接从 Copilot
Chat 运行，也可以通过选择要为其创建测试的代码片段并使用 Copilot
内联功能来运行该命令。

1.  打开test.js文件。

2.  单击 现有 **it** 块后的 **Enter**。

3.  输入以下文本，然后单击 **Enter**。

**//add test to test DaysBetweenDates**

![](./media/image54.png)

4.  这将生成 **DaysBetweenDates** 的单元测试块。点击 **Accept**
    接受代码。

![](./media/image55.png)

5.  在终端上，执行以下命令!!**mocha test.js**!!

![](./media/image56.png)

6.  输入以下文本 **//add test to check validatephoneNumber**，然后单击
    **Enter**。

![](./media/image57.png)

7.  单击 **“Accept”** 以接受 Copilot 生成的代码。

![](./media/image58.png)

8.  在终端上，执行命令!!**mocha test.js**!!.检查验证电话号码是否已通过。

![](./media/image59.png)

9.  输入以下文本并按 **Enter**。

!!**//write test to validate validateSpanishDNI**!!

![](./media/image60.png)

10. 接受 Copilot 生成的文本。

11. 从终端，执行!!**mocha test.js**!!并检查 ValidateSpanishDNI
    是否已通过。

![](./media/image61.png)

**Reference Code:**

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

## **练习 5：创建 Dockerfile**

1.  从 **node** 文件夹中打开 **dockerfile**。

![](./media/image62.png)

2.  该文件将包含有关如何填充它的注释。

3.  按 **Ctrl+I** 并键入 !!**/fix**!!.单击 **Send** 图标。

4.  Copilot 将生成 Docker 文件内容。单击 **“Accept”**。

![](./media/image63.png)

5.  在终端中，执行以下命令

!!**docker build -t mynodeapp .**!!

这是为了构建映像并将其标记为 mynodeapp。

![](./media/image64.png)

6.  使用以下命令在端口 **4000** 中运行 docker。

!!**docker run -p 4000:3000 -d mynodeapp**!!

![](./media/image65.png)

7.  打开 Docker 守护程序以查看应用程序是否已容器化并在其中运行。

![](./media/image66.png)

**总结：**

在本实验室中，我们学习了如何在节点项目中使用 Copilot
