**實驗 19 - 在 GitHub CopilotGoal 的幫助下使用 Quarkus 構建 REST API**

本實驗室的目標是學習如何使用 GitHub Copilot，使用包括使用
https://quarkus.io/ 生成 REST API 的任務。

我們已經創建了一個 Quarkus
項目，其中已經創建了一些文件，您可以在**文件夾 exercisefiles/quarkus**
中找到該項目。

讓我們開始副駕駛!!

**任務 1 - 創建代碼以處理簡單的 GET 請求**

移動到“DemoResource.java”文件並開始編寫代碼來處理簡單的 GET 請求。

1.  在第一步中，我們提供了一個注釋來描述您需要生成的代碼。只需按 Enter
    並等待幾秒鐘。

![BrokenImage](./media/image1.png)

2.  Copilot 將為您生成代碼。如果您對代碼不滿意，請按 Ctrl
    +Enter，它會建議多個代碼選項。

![A screenshot of a computer Description automatically
generated](./media/image2.png)

3.  .如果您對生成的代碼不滿意，可以再次按 Enter 鍵，Copilot
    將生成一個新代碼

![A screenshot of a computer Description automatically
generated](./media/image3.png)

![A screenshot of a computer program Description automatically
generated](./media/image4.png)

![A screenshot of a computer program Description automatically
generated](./media/image5.png)

4.  轉到 **test/java/com/Microsoft/hackthon/quarkus/** 並單擊
    **DemoResourceTest.java**。已經為此任務實現了單元測試。

![A screenshot of a computer Description automatically
generated](./media/image6.png)

5.  單擊 **Terminal -\> New Terminal**。

![BrokenImage](./media/image7.png)

6.  選擇 **Gitbash**。

![BrokenImage](./media/image8.png)

7.  運行 cd exercisefiles/quarkus/copilot-demo/ 命令。

![A screen shot of a computer program Description automatically
generated](./media/image9.png)

8.  您可以使用命令 mvn test before and after 運行它，以驗證 Copilot
    生成的代碼是否正確。

![A screenshot of a computer program Description automatically
generated](./media/image10.png)

![A screen shot of a computer Description automatically
generated](./media/image11.png)

![A screenshot of a computer program Description automatically
generated](./media/image12.png)

9.  完成每項任務後，請隨意打包並運行您的應用程序以對其進行測試。

Package: mvn package

![A screenshot of a computer program Description automatically
generated](./media/image13.png)

![A screenshot of a computer program Description automatically
generated](./media/image14.png)

10. 運行：mvn quarkus：dev

![A screenshot of a computer program Description automatically
generated](./media/image15.png)

![A screenshot of a computer program Description automatically
generated](./media/image16.png)

11. 單擊拆分終端並在第二個終端中輸入命令並運行

curl -v http://localhost:8080/hello?key=world

curl http://localhost:8080/hello

curl http://localhost:8080/hello?key=world

![A screenshot of a computer screen Description automatically
generated](./media/image17.png)

![BrokenImage](./media/image18.png)

**任務 2 ： 日期比較**

/diffdates 下的新作，用於計算兩個日期之間的差異。該作應以 dd-MM-yyyy
格式接收兩個日期作為參數，並返回以天為單位的差異。

1.  鍵入以下注釋 // 在 /diffdates 下計算兩個日期之間差異的新作。該作應以
    dd-MM-yyyy 格式接收兩個日期作為參數，並返回以天為單位的差異。並按
    Enter 鍵

**注意：**注釋位於**DemoResource.java**文件中。
**C：\CopiolHackathon\exercisefiles\\ quarkus\\ copilot-demo\src\main\\
java\com\microsoft\hackathon\quarkus\DemoResource.java**

![A screen shot of a computer program Description automatically
generated](./media/image19.png)

2.  按 Tab 鍵，然後再次按 Tab 鍵接受代碼。

![A screen shot of a computer program Description automatically
generated](./media/image20.png)

3.  打開DemoResourceTest.java文件，創建驗證作的單元測試。添加
    //創建單元測試以驗證計算兩個日期之間差異的 /diffdates，然後按
    Enter。

![A screenshot of a computer program Description automatically
generated](./media/image21.png)

4.  按 Tab 接受代碼。您也可以使用以下代碼。

5.  package com.microsoft.hackathon.quarkus;

6.  

7.  import jakarta.ws.rs.GET;

8.  import jakarta.ws.rs.Path;

9.  import jakarta.ws.rs.Produces;

10. import jakarta.ws.rs.QueryParam;

11. import jakarta.ws.rs.client.Client;

12. import jakarta.ws.rs.client.ClientBuilder;

13. import jakarta.ws.rs.client.WebTarget;

14. import jakarta.ws.rs.core.MediaType;

15. import jakarta.ws.rs.core.Response;

16. 

17. import java.io.File;

18. import java.io.FileInputStream;

19. import java.io.IOException;

20. import java.io.InputStream;

21. import java.net.URL;

22. import java.nio.file.Files;

23. import java.nio.file.Paths;

24. import java.text.SimpleDateFormat;

25. import java.util.ArrayList;

26. import java.util.Date;

27. import java.util.List;

28. import java.util.Objects;

29. 

30. import com.fasterxml.jackson.databind.JsonNode;

31. import com.fasterxml.jackson.databind.ObjectMapper;

32. import com.fasterxml.jackson.databind.node.ObjectNode;

33. 

34. import io.quarkus.fs.util.ZipUtils;

35. 

36. 

37. 

38. 

39. 

40. /\*

41. \* The Demo resource should be mapped to the root path.

42. \*

43. \* Create a GET operation to return the value of a key passed as
    query parameter in the request.

44. \*

45. \* If the key is not passed, return "key not passed".

46. \* If the key is passed, return "hello \<key\>".

47. \*

48. \*/

49. 

50. @Path("/")

51. public class DemoResource {

52. @GET

53. @Path("/hello")

54. @Produces(MediaType.TEXT_PLAIN)

55. public String hello(@QueryParam("key") String key) {

56. if (key == null) {

57. return "key not passed";

58. } else {

59. return "hello " + key;

60. }

61. }

62. // New operation under /diffdates that calculates the difference
    between two dates. The operation should receive two dates as
    parameter in format dd-MM-yyyy and return the difference in days.

63. @GET

64. @Path("/diffdates")

65. @Produces(MediaType.TEXT_PLAIN)

66. public String diffdates(@QueryParam("date1") String date1,
    @QueryParam("date2") String date2) {

67. Objects.requireNonNull(date1, "date1 must not be null");

68. Objects.requireNonNull(date2, "date2 must not be null");

69. try {

70. SimpleDateFormat dateFormat = new SimpleDateFormat("dd-MM-yyyy");

71. Date date1Obj = dateFormat.parse(date1);

72. Date date2Obj = dateFormat.parse(date2);

73. long diffMillis = Math.abs(date1Obj.getTime() - date2Obj.getTime());

74. long diffDays = diffMillis / (24 \* 60 \* 60 \* 1000);

75. return String.valueOf(diffDays);

76. } catch (Exception e) {

77. return "invalid date format";

78. }

}

![A screenshot of a computer program Description automatically
generated](./media/image22.png)

79. 打開終端並運行 mvn test 命令。

![A screen shot of a computer Description automatically
generated](./media/image23.png)

![A screenshot of a computer program Description automatically
generated](./media/image24.png)

80. 通過運行命令 mvn package 打包解決方案

![A screenshot of a computer program Description automatically
generated](./media/image25.png)

![A screenshot of a computer program Description automatically
generated](./media/image26.png)

81. 運行： mvn quarkus：dev 或 mvn compile quarkus：dev

![A screenshot of a computer program Description automatically
generated](./media/image27.png)

82. 拆分終端並運行 curl -v http://localhost:8080/diffdates

**任務 3：驗證西班牙語電話的格式**

驗證西班牙語電話號碼的格式（+34 前綴，然後是 9 位數字，從 6、7 或 9
開始）。該作應接收電話號碼作為參數，如果格式正確，則返回 true，否則返回
false。

1.  輸入 //驗證西班牙語電話號碼的格式（+34 前綴，然後是 9 位數字，從
    6、7 或 9
    開始）。該作應接收一個電話號碼作為參數，如果格式正確，則返回
    true，否則返回 false，然後按 Enter。按 Tab 接受 Coilot 建議代碼。

![A screen shot of a computer program Description automatically
generated](./media/image28.png)

2.  鍵入 // 編寫單元測試以驗證西班牙語電話號碼的格式（+34 前綴，然後是 9
    位數字，從 6、7 或 9
    開始）。該作應接收電話號碼作為參數，如果格式正確，則返回
    true，否則返回 false，然後按 Enter。按 Tab 接受助手建議的單元測試

![A screen shot of a computer program Description automatically
generated](./media/image29.png)

3.  打開終端並運行 mvn test。

![A screen shot of a computer Description automatically
generated](./media/image30.png)

![A screenshot of a computer program Description automatically
generated](./media/image31.png)

4.  運行 mvn 包

![A screenshot of a computer program Description automatically
generated](./media/image32.png)

![A screenshot of a computer program Description automatically
generated](./media/image33.png)

5.  運行 mvn quarkus：dev

![A screenshot of a computer screen Description automatically
generated](./media/image34.png)

6.  單擊拆分終端並在其中一個終端中運行 -

curl -v http://localhost:8080/validatephone?phone=+34866666666

curl -v http://localhost:8080/validatephone?phone=+34666666667

curl -v http://localhost:8080/validatephone?phone=+34666666666

![A screenshot of a computer program Description automatically
generated](./media/image35.png)

**任務 4：驗證西班牙語 DNI 的格式**

驗證西班牙語 DNI 的格式（8 位數字和 1 個字母）。該作應接收 DNI
作為參數，如果格式正確，則返回 true，否則返回 false。

1.  輸入 // 驗證西班牙語 DNI 的格式（8 位數字和 1 個字母）。該作應接收
    DNI 作為參數，如果格式正確，則返回 true，否則返回 false。並按
    Enter。按 Tab 接受 Copilot 建議代碼。

![A screenshot of a computer program Description automatically
generated](./media/image36.png)

2.  切換到
    **CopilotDemoApplicationTests.java**。要編寫單元測試來測試上述函數，請添加
    //編寫單元測試以驗證西班牙語 DNI 的格式（8 位數字和 1
    個字母）。該作應接收 DNI 作為參數，如果格式正確，則返回
    true，否則返回 false。按 Enter 鍵。按 選項卡接受代碼。

![A screen shot of a computer program Description automatically
generated](./media/image37.png)

3.  打開終端並運行 mvn test

![A screenshot of a computer program Description automatically
generated](./media/image38.png)

![A screenshot of a computer program Description automatically
generated](./media/image39.png)

4.  運行 mvn 包

![A screenshot of a computer program Description automatically
generated](./media/image40.png)

![A screenshot of a computer program Description automatically
generated](./media/image41.png)

5.  運行：mvn quarkus：dev

![A screenshot of a computer program Description automatically
generated](./media/image42.png)

6.  測試：curl -v http://localhost:8080/hello/validatedni?dni=12345678A

![A screenshot of a computer program Description automatically
generated](./media/image43.png)

**任務 5：從顏色名稱到十六進制代碼**

根據資源下現有的colors.json文件，給定顏色作為路徑參數的名稱，返回十六進制代碼。如果未找到顏色，則返回
404

提示：使用 TDD。首先創建單元測試，然後實現代碼。

1.  鍵入 //
    根據資源下的現有colors.json文件，給定顏色名稱作為路徑參數，返回十六進制代碼。如果未找到顏色，則返回
    404。並按 Enter。按 Tab 接受 Copilot 建議代碼。

![A screenshot of a computer program Description automatically
generated](./media/image44.png)

2.  切換到
    **CopilotDemoApplicationTests.java**。要編寫單元測試來測試上述函數，請添加
    //Write unit test to Based on the existing colors.json file under
    resources， given color as path
    參數的名稱，返回十六進制代碼。如果未找到顏色，則返回 404。按 Enter
    鍵。按 選項卡接受代碼。

![A screenshot of a computer program Description automatically
generated](./media/image45.png)

3.  運行 mvn 測試

![A screenshot of a computer program Description automatically
generated](./media/image46.png)

![A screenshot of a computer program Description automatically
generated](./media/image47.png)

4.  運行 mvn 包

![A screenshot of a computer Description automatically
generated](./media/image48.png)

5.  運行：mvn quarkus：dev

![A screenshot of a computer program Description automatically
generated](./media/image49.png)

6.  測試：curl -v http://localhost:8080/hello/color?color=red

![BrokenImage](./media/image50.png)

**任務 6 ： 笑話創作者**

創建一個調用 API https://api.chucknorris.io/jokes/random
並返回笑話的新作。

1.  鍵入 // 創建一個調用 API https://api.chucknorris.io/jokes/random
    並返回笑話的新作。並按 Enter。按 Tab 接受 Copilot 建議代碼。

![A screenshot of a computer program Description automatically
generated](./media/image51.png)

2.  按 Tab 接受代碼

![A screen shot of a computer program Description automatically
generated](./media/image52.png)

3.  切換到
    **CopilotDemoApplicationTests.java**。要編寫單元測試來測試上述函數，請添加
    //創建一個調用 API
    \[\<u\>https://api.chucknorris.io/jokes/random\</u\>\]（https://api.chucknorris.io/jokes/random）
    並返回笑話的新作。按 Enter 鍵。按 選項卡接受代碼。

![A screenshot of a computer program Description automatically
generated](./media/image53.png)

4.  按 Tab 接受代碼。

![A screenshot of a computer program Description automatically
generated](./media/image54.png)

5.  單擊 Terminal -\> New Terminal -\> Gitbash 並運行以下命令

cd exercisefiles/quarkus/copilot-demo/

mvn test

![A screenshot of a computer program Description automatically
generated](./media/image55.png)

![A screenshot of a computer program Description automatically
generated](./media/image56.png)

6.  運行 mvn package 以打包您的應用程序。

![A screenshot of a computer program Description automatically
generated](./media/image57.png)

![A screenshot of a computer program Description automatically
generated](./media/image58.png)

7.  運行：mvn quarkus：dev

![A screenshot of a computer program Description automatically
generated](./media/image59.png)

8.  測試：curl -v http://localhost:8080/hello/joke

![A screenshot of a computer program Description automatically
generated](./media/image60.png)

**任務 7：URL 解析**

給定一個 url
作為查詢參數，解析它並返回協議、主機、端口、路徑和查詢參數。響應應採用
Json 格式。

1.  鍵入 //給定一個 url
    作為查詢參數，解析它並返回協議、主機、端口、路徑和查詢參數。響應應採用
    Json 格式。並按 Enter。按 Tab 接受 Copilot 建議代碼。

![A screen shot of a computer program Description automatically
generated](./media/image61.png)

![A screen shot of a computer program Description automatically
generated](./media/image62.png)

2.  切換到
    **CopilotDemoApplicationTests.java**。要編寫單元測試來測試上述函數，請添加
    //給定 url
    作為查詢參數編寫單元測試，對其進行解析並返回協議、主機、端口、路徑和查詢參數。響應應採用
    Json 格式。按 Enter 鍵。按 選項卡接受代碼。

![A screenshot of a computer program Description automatically
generated](./media/image63.png)

3.  運行 mvn 測試

![A screenshot of a computer program Description automatically
generated](./media/image64.png)

![A screenshot of a computer Description automatically
generated](./media/image65.png)

4.  運行 mvn package 以打包您的應用程序。

![A screenshot of a computer program Description automatically
generated](./media/image66.png)

5.  運行 mvn quarkus：dev

![A screenshot of a computer program Description automatically
generated](./media/image67.png)

6.  單擊拆分終端並運行 curl -v
    http://localhost:8080/hello/parseurl?url=https://www.google.com/search?q=quarkus

![A screenshot of a computer program Description automatically
generated](./media/image68.png)

**任務 9 ： 字數統計**

給定文件的路徑並計算所提供單詞的出現次數。路徑和單詞應該是查詢參數。響應應採用
Json 格式。

1.  鍵入
    //給定文件的路徑並計算所提供單詞的出現次數。路徑和單詞應該是查詢參數。響應應採用
    Json 格式。並按 Enter。按 Tab 接受 Copilot 建議代碼。

![A screenshot of a computer program Description automatically
generated](./media/image69.png)

2.  切換到
    **CopilotDemoApplicationTests.java**。要編寫單元測試來測試上述函數，請將
    //Write unit test
    添加到給定文件的路徑並計算所提供單詞的出現次數。路徑和單詞應該是查詢參數。響應應採用
    Json 格式。按 Enter 鍵。按 選項卡接受代碼。

![A screenshot of a computer program Description automatically
generated](./media/image70.png)

3.  打開**Terminal**並運行 mvn test

![A screenshot of a computer program Description automatically
generated](./media/image71.png)

![A screenshot of a computer program Description automatically
generated](./media/image72.png)

4.  運行 mvn package 以打包您的應用程序。

![A screenshot of a computer program Description automatically
generated](./media/image73.png)

![A screenshot of a computer program Description automatically
generated](./media/image74.png)

5.  運行：mvn quarkus：dev

![A screenshot of a computer program Description automatically
generated](./media/image75.png)

6.  測試：curl \<http://localhost:8080/hello/countword?path=/tmp/test.txt&word=hello

可以向 GitHub 助手請求項目的 curl 命令。

![A screenshot of a computer program Description automatically
generated](./media/image76.png)

**任務 10：容器化應用程序**

使用提供的 Dockerfile 創建應用程序的 Docker
映像。在這種情況下，提供了完整的內容，但為了構建、運行和測試 docker
映像，您還將使用 Copilot 來生成命令。

我創建了一個 DOCKER.md
文件，我們將在其中記錄構建應用程序（本機）、構建容器映像、運行容器和測試容器的步驟。

1.  在 Visual Studio 代碼中，按 **Ctrl +Shit + X** 搜索 **Docker**
    並安裝它。

![A screenshot of a computer Description automatically
generated](./media/image77.png)

2.  雙擊**Desktop Docker**並使用您的 Docker 帳戶唱歌。

![BrokenImage](./media/image78.png)

3.  按 **Ctrl +Alt+I** 打開 **Github Copilot chat**。詢問 Copilot
    如何使用提供的 Dockerfile 生成容器映像、運行容器和測試容器

![A screenshot of a computer program Description automatically
generated](./media/image79.png)

4.  按照 Copilot 的指示。構建應用程序：在終端中運行以下命令：

./mvnw package -Pnative -Dquarkus.native.container-build=true

![A screenshot of a computer Description automatically
generated](./media/image77.png)

![A screenshot of a computer program Description automatically
generated](./media/image80.png)

![A screenshot of a computer program Description automatically
generated](./media/image81.png)

![A screenshot of a computer program Description automatically
generated](./media/image82.png)

![A screenshot of a computer program Description automatically
generated](./media/image83.png)

5.  **構建 Docker 鏡像：**假設您的 Dockerfile 名為
    **Dockerfile.native-micro**，您可以使用以下命令:

docker build -f Dockerfile.native-micro -t my-app .

![A computer screen shot of a program Description automatically
generated](./media/image84.png)

6.  此命令告訴 Docker 使用當前目錄（命令末尾的
    '.'）中名為“Dockerfile.native-micro”的 Dockerfile
    構建映像，並使用名稱“my-app”標記生成的映像。

7.  運行 Docker 鏡像：構建鏡像後，您可以使用“docker run”命令運行它：

docker run -p 8080:8080 my-app

![BrokenImage](./media/image85.png)

此命令告訴 Docker 從“my-app”映像運行容器，並將容器中的端口 8080
映射到主機上的端口 8080。

8.  **測試應用程序**：最後，要測試您的應用程序是否正常運行，您可以在瀏覽器中或使用
    curl 等工具向 http://localhost:8080 發送請求：

curl http://localhost:8080

![A screenshot of a computer program Description automatically
generated](./media/image86.png)

此命令向應用程序發送 GET
請求並打印響應。如果應用程序運行正常，則應會看到預期的響應。

請注意，這些命令應該在您的終端中運行，而不是在您的 Java
應用程序代碼中運行。
