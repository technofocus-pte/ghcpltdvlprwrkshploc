
# **實驗室 20 - 使用 Nodejs 激活 GitHub Copilot**

**客觀的：**

本實驗室旨在幫助瞭解用於運行實驗室以評估 Copilot 可行性的演示項目。

在執行本練習之前，讓我們先安裝必要的軟件包並設置環境。

**任務 0：安裝和設置環境**

您需要下載並安裝以下軟件包來設置環境以執行本練習。

1.  Node.js

2.  mocha

&nbsp;

1.  打開 Edge 瀏覽器。

> ![A screenshot of a computer Description automatically
> generated](./media/image1.png)

2.  在瀏覽器 URL 字段中，複製粘貼鏈接以將軟件包下載到實驗室 VM。

&nbsp;

1.  Node.js和 MVN 🡪
    <https://nodejs.org/dist/v20.16.0/node-v20.16.0-x64.msi>

> b.mocha （無需下載）
>
> **注意**：默認情況下，包將保存在**downloads**文件夾中。
>
> ![A screenshot of a computer Description automatically
> generated](./media/image2.png)

1.  **安裝Node.js和 mvn**

&nbsp;

1.  轉到 **Downloads**（**C：\Users\Admin\Downloads**）
    文件夾，然後雙擊node-v20.16.0-x64.msi **。**

> ![A screenshot of a computer Description automatically
> generated](./media/image3.png)

2.  在“Node.js setup wizard”窗口中，單擊 **Next**。

> ![A screenshot of a computer Description automatically
> generated](./media/image4.png)

3.  接受 EULA 並單擊 **Next**。

> ![A screenshot of a software license agreement Description
> automatically generated](./media/image5.png)

4.  保留默認目標文件夾，然後單擊“**Next**”。

> ![A screenshot of a computer Description automatically
> generated](./media/image6.png)

5.  單擊“**Add to the PATH**”，然後單擊“**Next**”。

> ![A screenshot of a computer program Description automatically
> generated](./media/image7.png)

6.  在“**Tools for native
    Modules**”窗口中，選中該**複選框**並單擊“Next”。

> ![A screenshot of a computer Description automatically
> generated](./media/image8.png)

7.  單擊 **Install**。

> ![A screenshot of a computer Description automatically
> generated](./media/image9.png)
>
> 注意：如果您看到 **User Access Control** 彈出窗口，請單擊 **Yes**
> 繼續。

8.  完成後點擊 **Finish**。

> ![A screenshot of a computer Description automatically
> generated](./media/image10.png)

9.  **Cmd** 終端打開。按任意鍵繼續..

> ![A screenshot of a computer Description automatically
> generated](./media/image11.png)
>
> 注意：按下某個鍵後，您可能會看到延遲。請等待一段時間以繼續安裝。

10. 單擊“**Yes**”在 UAC 窗口中繼續。

> ![A screenshot of a computer error Description automatically
> generated](./media/image12.png)

11. **Windows Powershell** 打開，顯示安裝詳細信息。

> ![A screenshot of a computer program Description automatically
> generated](./media/image13.png)

12. 安裝完成後，鍵入 **Enter** 退出 PowerShell。

> ![A computer screen with text on it Description automatically
> generated](./media/image14.png)

2.  **安裝 mocha**

&nbsp;

1.  打開命令提示符

> ![A screenshot of a computer Description automatically
> generated](./media/image15.png)

2.  首先運行以下命令。

> +++npm install --global mocha+++
>
> ![A screenshot of a computer Description automatically
> generated](./media/image16.png)
>
> ![A screenshot of a computer screen Description automatically
> generated](./media/image17.png)

3.  接下來運行以下命令

> +++npm install axios+++
>
> ![A screenshot of a computer screen Description automatically
> generated](./media/image18.png)
>
> ![A screenshot of a computer Description automatically
> generated](./media/image19.png)
>
> 現在您已經完成了**mocha** 的安裝。關閉終端以繼續安裝其他軟件包。

## **練習 1：簡介**

1.  在 Visual Studio 中， 從 exercisefiles -\>
    節點打開**nodeserver.js**。

![A screenshot of a computer Description automatically
generated](./media/image20.png)

2.  我們需要開始為節點編碼。js
    服務器，該服務器將公開一個方法調用“get”，該調用將返回查詢字符串中傳遞的鍵的值。讓我們使用
    Copilot 來幫助我們解決這個問題。

3.  按 **Ctrl+I** 並粘貼以下命令，讓 Copilot 生成代碼並點擊 **Send**。

**// write a nodejs server that will expose a method call "get" that
will return the value of the key passed in the query string**

**// example: http://localhost:3000/get?key=hello**

**// if the key is not passed, return "key not passed"**

**// if the key is passed, return "hello" + key**

**// if the url has other methods, return "method not supported"**

**// when server is listening, log "server is listening on port 3000"**

![A screenshot of a computer Description automatically
generated](./media/image21.png)

4.  Copilot 生成代碼並顯示。單擊 **“Accept”** 以接受它。

![A screenshot of a computer program Description automatically
generated](./media/image22.png)

5.  右鍵單 **node** 點文件夾，然後選擇在集成終端中打開。

![A screenshot of a computer Description automatically
generated](./media/image23.png)

6.  打開終端後，從中執行以下命令。

!!**mocha test.js**!!

7.  您應該得到的結果為 **1 Passing**，如下面的屏幕截圖所示。

![A computer screen with white text Description automatically
generated](./media/image24.png)

8.  這是nodeserver.js中方法的單元測試，它已通過。

9.  我們將繼續使用 Copilot 向服務器添加不同的方法。

## **練習 2：構建新功能**

該練習包括使用 Nodejs 構建一個 Web
服務器，該服務器可滿足各種功能的請求。

1.  添加 服務器必須參與的 **DaysBetweenDates** 功能請求。

2.  在 **if** 條件 **– pathname == '/get'** 結束後按 **Enter**。

**請注意：** 請參閱紅色突出顯示的大括號，您需要按 **Enter** 鍵

![](./media/image25.png)

3.  按 **Ctrl+I** 打開 Copilot 內聯功能，輸入以下內容並單擊 **Send**。

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

4.  Copilot 生成代碼。點擊 **Accept**
    接受代碼。請注意，生成的代碼是請求中的 **else if** 塊，其中是
    **DaysBetweenDates**。

![](./media/image27.png)

5.  單擊 **DaysBetweenDates** 塊後的 **Enter**。

6.  輸入下面的評論塊並按 **Enter**。

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

7.  Copilot 生成代碼。單擊 **“Accept”** 以接受代碼。

![A screenshot of a computer program Description automatically
generated](./media/image29.png)

8.  單擊 **Validatephonenumber** 塊後的 **Enter** 以添加下一個代碼塊。

9.  將以下文本複製並粘貼到 js 文件中。

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
> ![A screen shot of a computer program Description automatically
> generated](./media/image30.png)

10. 粘貼上述內容後，Copilot 會生成代碼，該代碼顯示在評論下方。點擊
    **Accept** 接受代碼。

![A screenshot of a computer program Description automatically
generated](./media/image31.png)

11. 從左側導航窗格打開 Copilot 聊天。

![A black rectangular object with white symbols Description
automatically generated](./media/image32.png)

12. 將以下內容粘貼到聊天中，然後單擊“**Send”**按鈕。

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

> **注意：** 默認情況下，Copilot 將使用打開的文件作為上下文來生成建議。

![A screenshot of a computer program Description automatically
generated](./media/image33.png)

13. 將光標保留在 **ValidateSpanishDNI**
    塊之後，然後單擊聊天中的“插入光標處”圖標。這**會將** Copilot
    生成的代碼從聊天複製到上述位置的服務器 js 文件。

![A screenshot of a computer program Description automatically
generated](./media/image34.png)

14. 檢查是否有錯誤。在此生成的代碼中，存在錯誤，因為 else if
    塊之間有一個常量聲明。

![A screen shot of a computer Description automatically
generated](./media/image35.png)

15. 按 **Ctrl+I** 打開 Copilot Inline，輸入 !!**/fix**!!
    並單擊“**Send**”按鈕

![A screenshot of a computer program Description automatically
generated](./media/image36.png)

16. 如果可以找到解決方案，Copilot
    會生成解決方案。根據解決方案的準確性接受或放棄解決方案。

![A screenshot of a computer Description automatically
generated](./media/image37.png)

17. 在這裡，我們將常量聲明移動到 returncolors 的 else if
    塊中以解決錯誤。

![A screen shot of a computer program Description automatically
generated](./media/image38.png)

**重要提示：** 根據 Copilot
生成的代碼和解決方案，代碼和解決方案可能有所不同。

18. 添加塊後，按 **Ctrl+I** 打開 Copilot 內聯功能，粘貼以下內容並單擊
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

![A screenshot of a computer Description automatically
generated](./media/image39.png)

19. 單擊 **“Accept”** 以接受 Copilot 生成的代碼。

![A screenshot of a computer Description automatically
generated](./media/image40.png)

20. 生成代碼塊後，按 **Ctrl+I**，輸入以下文本，然後單擊 **Send** 按鈕。

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

![A screenshot of a computer Description automatically
generated](./media/image41.png)

21. 點擊 **Accept** 接受代碼。

![A screenshot of a computer program Description automatically
generated](./media/image42.png)

22. 生成代碼塊後，按 **Ctrl+I**，輸入以下文本，然後單擊 **Send** 按鈕。

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

![A screenshot of a computer Description automatically
generated](./media/image43.png)

23. 點擊 **Accept** 接受代碼。

![A screenshot of a computer program Description automatically
generated](./media/image44.png)

24. 生成代碼塊後，按 **Ctrl+I**，輸入以下文本，然後單擊 **Send** 按鈕。

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
小心此實現，因為它通常會在分析文件之前讀取文件的全部內容，因此內存使用率很高，並且當文件太大時可能會失敗。

![A screenshot of a computer Description automatically
generated](./media/image45.png)

25. 點擊 **Accept** 接受代碼。

![A screenshot of a computer program Description automatically
generated](./media/image46.png)

26. 生成代碼塊後，按 **Ctrl+I**，輸入以下文本，然後單擊 **Send** 按鈕。

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

![A screenshot of a video Description automatically
generated](./media/image47.png)

27. 點擊 **Accept** 接受代碼。

![A screenshot of a computer program Description automatically
generated](./media/image48.png)

28. 生成代碼塊後，按 **Ctrl+I**，輸入以下文本，然後單擊 **Send** 按鈕。

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

![A screenshot of a computer Description automatically
generated](./media/image49.png)

29. 點擊 **Accept** 接受代碼。

![A screenshot of a computer program Description automatically
generated](./media/image50.png)

30. 生成代碼塊後，按 **Ctrl+I**，輸入以下文本，然後單擊 **Send**按鈕。

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

![A screenshot of a computer program Description automatically
generated](./media/image51.png)

31. 點擊 **Accept** 接受代碼。

![A screenshot of a computer program Description automatically
generated](./media/image52.png)

## **練習 3：記錄代碼**

記錄代碼始終是一項枯燥而痛苦的任務。但是，我們可以使用 Copilot
為我們記錄它。在聊天中，要求 Copilot 記錄nodeserver.js文件。

1.  選擇**nodeserver.js**文件中的**所有內容。**

2.  在 Copilot 聊天中，輸入 !!**document the nodeserver.js
    file**!!，然後單擊發送。

3.  Copilot 生成文件的詳細文檔。

![A screenshot of a computer Description automatically
generated](./media/image53.png)

## **練習 4：構建測試**

我們將創建自動化測試來檢查先前端點的功能是否正確實現。測試應一起放在test.js文件中。

您可以利用 Copilot 運行測試。有一個 /tests 命令，您可以直接從 Copilot
Chat 運行，也可以通過選擇要為其創建測試的代碼片段並使用 Copilot
內聯功能來運行該命令。

1.  打開test.js文件。

2.  單擊 現有 **it** 塊後的 **Enter**。

3.  輸入以下文本，然後單擊 **Enter**。

**//add test to test DaysBetweenDates**

![A screen shot of a computer Description automatically
generated](./media/image54.png)

4.  這將生成 **DaysBetweenDates** 的單元測試塊。點擊 **Accept**
    接受代碼。

![A screenshot of a computer Description automatically
generated](./media/image55.png)

5.  在終端上，執行以下命令!!**mocha test.js**!!

![A computer screen with white text Description automatically
generated](./media/image56.png)

6.  輸入以下文本 **//add test to check validatephoneNumber**，然後單擊
    **Enter**。

![A screen shot of a computer Description automatically
generated](./media/image57.png)

7.  單擊 **“Accept”** 以接受 Copilot 生成的代碼。

![A screenshot of a computer Description automatically
generated](./media/image58.png)

8.  在終端上，執行命令!!**mocha test.js**!!.檢查驗證電話號碼是否已通過。

![A screenshot of a computer Description automatically
generated](./media/image59.png)

9.  輸入以下文本並按 **Enter**。

!!**//write test to validate validateSpanishDNI**!!

![A screen shot of a computer program Description automatically
generated](./media/image60.png)

10. 接受 Copilot 生成的文本。

11. 從終端，執行!!**mocha test.js**!!並檢查 ValidateSpanishDNI
    是否已通過。

![A screenshot of a computer program Description automatically
generated](./media/image61.png)

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

## **練習 5：創建 Dockerfile**

1.  從 **node** 文件夾中打開 **dockerfile**。

![A screenshot of a computer Description automatically
generated](./media/image62.png)

2.  該文件將包含有關如何填充它的注釋。

3.  按 **Ctrl+I** 並鍵入 !!**/fix**!!.單擊 **Send** 圖標。

4.  Copilot 將生成 Docker 文件內容。單擊 **“Accept”**。

![A screenshot of a computer program Description automatically
generated](./media/image63.png)

5.  在終端中，執行以下命令

!!**docker build -t mynodeapp .**!!

這是為了構建映像並將其標記為 mynodeapp。

![A screenshot of a computer Description automatically
generated](./media/image64.png)

6.  使用以下命令在端口 **4000** 中運行 docker。

!!**docker run -p 4000:3000 -d mynodeapp**!!

![](./media/image65.png)

7.  打開 Docker 守護程序以查看應用程序是否已容器化並在其中運行。

![A screenshot of a computer Description automatically
generated](./media/image66.png)

**總結：**

在本實驗室中，我們學習了如何在節點項目中使用 Copilot
