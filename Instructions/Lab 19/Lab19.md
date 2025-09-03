**实验 19 - 在 GitHub CopilotGoal 的帮助下使用 Quarkus 构建 REST API**

本实验室的目标是学习如何使用 GitHub Copilot，使用包括使用
https://quarkus.io/ 生成 REST API 的任务。

我们已经创建了一个 Quarkus
项目，其中已经创建了一些文件，您可以在**文件夹 exercisefiles/quarkus**
中找到该项目。

让我们开始副驾驶!!

**任务 1 - 创建代码以处理简单的 GET 请求**

移动到“DemoResource.java”文件并开始编写代码来处理简单的 GET 请求。

1.  在第一步中，我们提供了一个注释来描述您需要生成的代码。只需按 Enter
    并等待几秒钟。

![](./media/image1.jpeg)

2.  Copilot 将为您生成代码。如果您对代码不满意，请按 Ctrl
    +Enter，它会建议多个代码选项。

![](./media/image2.jpeg)

3.  .如果您对生成的代码不满意，可以再次按 Enter 键，Copilot
    将生成一个新代码

![](./media/image3.jpeg)

![](./media/image4.jpeg)

![](./media/image5.jpeg)

4.  转到 **test/java/com/Microsoft/hackthon/quarkus/** 并单击
    **DemoResourceTest.java**。已经为此任务实现了单元测试。

![](./media/image6.jpeg)

5.  单击 **Terminal -\> New Terminal**。

![](./media/image7.jpeg)

6.  选择 **Gitbash**。

![](./media/image8.jpeg)

7.  运行 cd exercisefiles/quarkus/copilot-demo/ 命令。

![](./media/image9.jpeg)

8.  您可以使用命令 mvn test before and after 运行它，以验证 Copilot
    生成的代码是否正确。

![](./media/image10.jpeg)

![](./media/image11.jpeg)

![](./media/image12.jpeg)

9.  完成每项任务后，请随意打包并运行您的应用程序以对其进行测试。

Package: mvn package

![](./media/image13.jpeg)

![](./media/image14.jpeg)

10. 运行：mvn quarkus：dev

![](./media/image15.jpeg)

![](./media/image16.jpeg)

11. 单击拆分终端并在第二个终端中输入命令并运行

curl -v http://localhost:8080/hello?key=world

curl http://localhost:8080/hello

curl http://localhost:8080/hello?key=world

![](./media/image17.jpeg)

![](./media/image18.jpeg)

**任务 2 ： 日期比较**

/diffdates 下的新作，用于计算两个日期之间的差异。该作应以 dd-MM-yyyy
格式接收两个日期作为参数，并返回以天为单位的差异。

1.  键入以下注释 // 在 /diffdates 下计算两个日期之间差异的新作。该作应以
    dd-MM-yyyy 格式接收两个日期作为参数，并返回以天为单位的差异。并按
    Enter 键

**注意：**注释位于**DemoResource.java**文件中。
**C：\CopiolHackathon\exercisefiles\\ quarkus\\ copilot-demo\src\main\\
java\com\microsoft\hackathon\quarkus\DemoResource.java**

![](./media/image19.jpeg)

2.  按 Tab 键，然后再次按 Tab 键接受代码。

![](./media/image20.jpeg)

3.  打开DemoResourceTest.java文件，创建验证作的单元测试。添加
    //创建单元测试以验证计算两个日期之间差异的 /diffdates，然后按
    Enter。

![](./media/image21.jpeg)

4.  按 Tab 接受代码。您也可以使用以下代码。

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

![](./media/image22.jpeg)

79. 打开终端并运行 mvn test 命令。

![](./media/image23.jpeg)

![](./media/image24.jpeg)

80. 通过运行命令 mvn package 打包解决方案

![](./media/image25.jpeg)

![](./media/image26.jpeg)

81. 运行： mvn quarkus：dev 或 mvn compile quarkus：dev

![](./media/image27.jpeg)

82. 拆分终端并运行 curl -v http://localhost:8080/diffdates

**任务 3：验证西班牙语电话的格式**

验证西班牙语电话号码的格式（+34 前缀，然后是 9 位数字，从 6、7 或 9
开始）。该作应接收电话号码作为参数，如果格式正确，则返回 true，否则返回
false。

1.  输入 //验证西班牙语电话号码的格式（+34 前缀，然后是 9 位数字，从
    6、7 或 9
    开始）。该作应接收一个电话号码作为参数，如果格式正确，则返回
    true，否则返回 false，然后按 Enter。按 Tab 接受 Coilot 建议代码。

![](./media/image28.jpeg)

2.  键入 // 编写单元测试以验证西班牙语电话号码的格式（+34 前缀，然后是 9
    位数字，从 6、7 或 9
    开始）。该作应接收电话号码作为参数，如果格式正确，则返回
    true，否则返回 false，然后按 Enter。按 Tab 接受助手建议的单元测试

![](./media/image29.jpeg)

3.  打开终端并运行 mvn test。

![](./media/image30.jpeg)

![](./media/image31.jpeg)

4.  运行 mvn 包

![](./media/image32.jpeg)

![](./media/image33.jpeg)

5.  运行 mvn quarkus：dev

![](./media/image34.jpeg)

6.  单击拆分终端并在其中一个终端中运行 -

curl -v http://localhost:8080/validatephone?phone=+34866666666

curl -v http://localhost:8080/validatephone?phone=+34666666667

curl -v http://localhost:8080/validatephone?phone=+34666666666

![](./media/image35.jpeg)

**任务 4：验证西班牙语 DNI 的格式**

验证西班牙语 DNI 的格式（8 位数字和 1 个字母）。该作应接收 DNI
作为参数，如果格式正确，则返回 true，否则返回 false。

1.  输入 // 验证西班牙语 DNI 的格式（8 位数字和 1 个字母）。该作应接收
    DNI 作为参数，如果格式正确，则返回 true，否则返回 false。并按
    Enter。按 Tab 接受 Copilot 建议代码。

![](./media/image36.jpeg)

2.  切换到
    **CopilotDemoApplicationTests.java**。要编写单元测试来测试上述函数，请添加
    //编写单元测试以验证西班牙语 DNI 的格式（8 位数字和 1
    个字母）。该作应接收 DNI 作为参数，如果格式正确，则返回
    true，否则返回 false。按 Enter 键。按 选项卡接受代码。

![](./media/image37.jpeg)

3.  打开终端并运行 mvn test

![](./media/image38.jpeg)

![](./media/image39.jpeg)

4.  运行 mvn 包

![](./media/image40.jpeg)

![](./media/image41.jpeg)

5.  运行：mvn quarkus：dev

![](./media/image42.jpeg)

6.  测试：curl -v http://localhost:8080/hello/validatedni?dni=12345678A

![](./media/image43.jpeg)

**任务 5：从颜色名称到十六进制代码**

根据资源下现有的colors.json文件，给定颜色作为路径参数的名称，返回十六进制代码。如果未找到颜色，则返回
404

提示：使用 TDD。首先创建单元测试，然后实现代码。

1.  键入 //
    根据资源下的现有colors.json文件，给定颜色名称作为路径参数，返回十六进制代码。如果未找到颜色，则返回
    404。并按 Enter。按 Tab 接受 Copilot 建议代码。

![](./media/image44.jpeg)

2.  切换到
    **CopilotDemoApplicationTests.java**。要编写单元测试来测试上述函数，请添加
    //Write unit test to Based on the existing colors.json file under
    resources， given color as path
    参数的名称，返回十六进制代码。如果未找到颜色，则返回 404。按 Enter
    键。按 选项卡接受代码。

![](./media/image45.jpeg)

3.  运行 mvn 测试

![](./media/image46.jpeg)

![](./media/image47.jpeg)

4.  运行 mvn 包

![](./media/image48.jpeg)

5.  运行：mvn quarkus：dev

![](./media/image49.jpeg)

6.  测试：curl -v http://localhost:8080/hello/color?color=red

![](./media/image50.jpeg)

**任务 6 ： 笑话创作者**

创建一个调用 API https://api.chucknorris.io/jokes/random
并返回笑话的新作。

1.  键入 // 创建一个调用 API https://api.chucknorris.io/jokes/random
    并返回笑话的新作。并按 Enter。按 Tab 接受 Copilot 建议代码。

![](./media/image51.jpeg)

2.  按 Tab 接受代码

![](./media/image52.jpeg)

3.  切换到
    **CopilotDemoApplicationTests.java**。要编写单元测试来测试上述函数，请添加
    //创建一个调用 API
    \[\<u\>https://api.chucknorris.io/jokes/random\</u\>\]（https://api.chucknorris.io/jokes/random）
    并返回笑话的新作。按 Enter 键。按 选项卡接受代码。

![](./media/image53.jpeg)

4.  按 Tab 接受代码。

![](./media/image54.jpeg)

5.  单击 Terminal -\> New Terminal -\> Gitbash 并运行以下命令

cd exercisefiles/quarkus/copilot-demo/

mvn test

![](./media/image55.jpeg)

![](./media/image56.jpeg)

6.  运行 mvn package 以打包您的应用程序。

![](./media/image57.jpeg)

![](./media/image58.jpeg)

7.  运行：mvn quarkus：dev

![](./media/image59.jpeg)

8.  测试：curl -v http://localhost:8080/hello/joke

![](./media/image60.jpeg)

**任务 7：URL 解析**

给定一个 url
作为查询参数，解析它并返回协议、主机、端口、路径和查询参数。响应应采用
Json 格式。

1.  键入 //给定一个 url
    作为查询参数，解析它并返回协议、主机、端口、路径和查询参数。响应应采用
    Json 格式。并按 Enter。按 Tab 接受 Copilot 建议代码。

![](./media/image61.jpeg)

![](./media/image62.jpeg)

2.  切换到
    **CopilotDemoApplicationTests.java**。要编写单元测试来测试上述函数，请添加
    //给定 url
    作为查询参数编写单元测试，对其进行解析并返回协议、主机、端口、路径和查询参数。响应应采用
    Json 格式。按 Enter 键。按 选项卡接受代码。

![](./media/image63.jpeg)

3.  运行 mvn 测试

![](./media/image64.jpeg)

![](./media/image65.jpeg)

4.  运行 mvn package 以打包您的应用程序。

![](./media/image66.jpeg)

5.  运行 mvn quarkus：dev

![](./media/image67.jpeg)

6.  单击拆分终端并运行 curl -v
    http://localhost:8080/hello/parseurl?url=https://www.google.com/search?q=quarkus

![](./media/image68.jpeg)

**任务 9 ： 字数统计**

给定文件的路径并计算所提供单词的出现次数。路径和单词应该是查询参数。响应应采用
Json 格式。

1.  键入
    //给定文件的路径并计算所提供单词的出现次数。路径和单词应该是查询参数。响应应采用
    Json 格式。并按 Enter。按 Tab 接受 Copilot 建议代码。

![](./media/image69.jpeg)

2.  切换到
    **CopilotDemoApplicationTests.java**。要编写单元测试来测试上述函数，请将
    //Write unit test
    添加到给定文件的路径并计算所提供单词的出现次数。路径和单词应该是查询参数。响应应采用
    Json 格式。按 Enter 键。按 选项卡接受代码。

![](./media/image70.jpeg)

3.  打开**Terminal**并运行 mvn test

![](./media/image71.jpeg)

![](./media/image72.jpeg)

4.  运行 mvn package 以打包您的应用程序。

![](./media/image73.jpeg)

![](./media/image74.jpeg)

5.  运行：mvn quarkus：dev

![](./media/image75.jpeg)

6.  测试：curl \<http://localhost:8080/hello/countword?path=/tmp/test.txt&word=hello

可以向 GitHub 助手请求项目的 curl 命令。

![](./media/image76.jpeg)

**任务 10：容器化应用程序**

使用提供的 Dockerfile 创建应用程序的 Docker
映像。在这种情况下，提供了完整的内容，但为了构建、运行和测试 docker
映像，您还将使用 Copilot 来生成命令。

我创建了一个 DOCKER.md
文件，我们将在其中记录构建应用程序（本机）、构建容器映像、运行容器和测试容器的步骤。

1.  在 Visual Studio 代码中，按 **Ctrl +Shit + X** 搜索 **Docker**
    并安装它。

![](./media/image77.jpeg)

2.  双击**Desktop Docker**并使用您的 Docker 帐户唱歌。

![](./media/image78.jpeg)

3.  按 **Ctrl +Alt+I** 打开 **Github Copilot chat**。询问 Copilot
    如何使用提供的 Dockerfile 生成容器映像、运行容器和测试容器

![](./media/image79.jpeg)

4.  按照 Copilot 的指示。构建应用程序：在终端中运行以下命令：

./mvnw package -Pnative -Dquarkus.native.container-build=true

![](./media/image77.jpeg)

![](./media/image80.jpeg)

![](./media/image81.jpeg)

![](./media/image82.jpeg)

![](./media/image83.jpeg)

5.  **构建 Docker 镜像：**假设您的 Dockerfile 名为
    **Dockerfile.native-micro**，您可以使用以下命令:

docker build -f Dockerfile.native-micro -t my-app .

![](./media/image84.jpeg)

6.  此命令告诉 Docker 使用当前目录（命令末尾的
    '.'）中名为“Dockerfile.native-micro”的 Dockerfile
    构建映像，并使用名称“my-app”标记生成的映像。

7.  运行 Docker 镜像：构建镜像后，您可以使用“docker run”命令运行它：

docker run -p 8080:8080 my-app

![](./media/image85.jpeg)

此命令告诉 Docker 从“my-app”映像运行容器，并将容器中的端口 8080
映射到主机上的端口 8080。

8.  **测试应用程序**：最后，要测试您的应用程序是否正常运行，您可以在浏览器中或使用
    curl 等工具向 http://localhost:8080 发送请求：

curl http://localhost:8080

![](./media/image86.jpeg)

此命令向应用程序发送 GET
请求并打印响应。如果应用程序运行正常，则应会看到预期的响应。

请注意，这些命令应该在您的终端中运行，而不是在您的 Java
应用程序代码中运行。

