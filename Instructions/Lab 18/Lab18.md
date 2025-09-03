**实验室 18 - 在 GitHub Copilot 的帮助下使用 Spring Boot 生成 REST API**

**目标**

本实验室的目标是学习如何使用 GitHub Copilot，使用包括使用 Spring Boot
生成 REST API 的练习。

我们已经创建了一个 Spring Boot
项目，其中已经创建了一些文件，您可以在文件夹
**C：\CopilotHackathon\exercisefiles\springboot 中找到该项目**。

在执行本练习之前，让我们先安装必要的软件包并设置环境。

任务 0：安装和设置环境

您需要下载并安装以下软件包来设置环境以执行本练习。

a\. Microsoft JDK 17

b\. apache maven

1.  打开 Edge 浏览器。

![](./media/image1.jpeg)

2.  在浏览器 URL 字段中，复制粘贴链接以将软件包下载到实验室 VM。

a. Microsoft JDK 17
◊ https://aka.ms/download-jdk/microsoft-jdk-17.0.12-windows-x64.msi

b. apache maven
◊https://dlcdn.apache.org/maven/maven-3/3.9.9/binaries/apache-maven-3.9.9-bin.zip

**注意：**重复相同的步骤以下载所有其他软件包。默认情况下，包将保存在下载文件夹中。

![](./media/image2.jpeg)

a. **安装 Microsoft JDK 17**

1.  在 **Downloads** (**C:\Users\Admin\Downloads**)
    文件夹中，双击“**Microsoft JDK**”

![](./media/image3.jpeg)

2.  单击 **Next**。 

![](./media/image4.jpeg)

3.  接受 EULA 并单击 **Next**。

![](./media/image5.jpeg)

4.  选择“**Install just for you (Admin)**”，然后单击“**Next**”。 

![](./media/image6.jpeg)

5.  在 **Custom setup** 屏幕中，您现在将 **set the JAVA_HOME
    variable**。单击向下箭头并选择 **Entire feature will be installed on
    local hard drive**。

![](./media/image7.jpeg)

6.  单击 **Next**。 

![](./media/image8.jpeg)

7.  单击 **Install**。 

![](./media/image9.jpeg)

**b. Install apache- maven**

8.  导航到 **Downloads** (**C:\Users\Admin\Downloads**) 文件夹

![](./media/image10.jpeg)

9.  右键单击 **apache-maven-3.9.9-bin.zip** 文件夹，然后选择 **Extract
    All**。

![](./media/image11.jpeg)

10. 在“**Select a destination**”页面中，输入目标为
    **C：\Users\Admin\Downloads，**然后单击“**Extract**”。

![](./media/image12.jpeg)

11. 提取的文件将如屏幕截图所示。

**注意：**如果您看到任何其他名称，请确保该文件夹已重命名为
**apache-maven-3.9.9**。

![](./media/image13.jpeg)

**设置环境变量**

12. 单击 **Windows logo** 并选择 **Settings**

![](./media/image14.jpeg)

13. 在 **Windows settings** 页面中搜索编辑系统，然后选择 **Edit System
    Environment variable**。

![](./media/image15.jpeg)

14. 单击“**Environment Variable** ”按钮。 

![](./media/image16.jpeg)

15. 单击“**User variable for Admin**”部分的“**New** ”。 

![](./media/image17.jpeg)

16. 现在，您将为 Maven 设置环境和路径变量。

在“**User variable for Admin**”部分下选择“**New**”。 

![](./media/image18.jpeg)

17. 在“**New User Variable** ”窗口中，输入以下内容，然后单击“**OK**”

Variable name: MAVEN_HOME

Variable value: C:\Users\Admin\Downloads\apache-maven-3.9.9

![](./media/image19.jpeg)

![](./media/image20.jpeg)

18. 现在选择 **Path** 并单击 **Edit** 

![](./media/image21.jpeg)

19. 在“**Edit environment variable**”窗口中，单击“**New**”。

![](./media/image22.jpeg)

20. 在空白字段中，输入以下 %MAVEN_HOME%\bin，然后单击 **OK**。

![](./media/image23.jpeg)

![](./media/image24.jpeg)

21. 单击“**Ok**”以完成 Maven 的用户环境和路径变量的设置。

![](./media/image25.jpeg)

22. 现在，您将为 Maven 设置 **System variables** 。在 **System
    variables**  部分下选择**New**。

![](./media/image26.jpeg)

23. 在“New System Variable”窗口中，输入以下内容，然后单击“**OK**”

Variable name: MAVEN_HOME

Variable value: C:\Users\Admin\Downloads\apache-maven-3.9.9

![](./media/image27.jpeg)

任务 1 ：创建代码以处理简单的 GET 请求

移动到“DemoController.java”文件并开始编写代码来处理简单的 GET
请求。在第一个练习中，我们提供了一个注释，描述了您需要生成的代码。只需按
Enter 并等待几秒钟，Copilot 就会为您生成代码。

本练习已经实现了单元测试，可以在之前和之后使用命令 mvn test
运行它，以验证 Copilot 生成的代码是否正确。

然后，在请求中未提供密钥时，为案例创建新的单元测试。

每次练习结束后，请随意打包并运行您的应用程序以对其进行测试。

Package: mvn package

Run: mvn spring-boot:run

Test: curl -v http://localhost:8080/hello?key=world

1.  打开文件资源管理器，展开 Local Disk (C:)，然后展开
    **CopilotHackathon-\>exercisefiles \> Springboot \> copilot-demo \>
    src\>main\>java\>com\>Microsoft\>hackathon\>copilotdemo\>controller** 文件夹，查看
    **'DemoController.java** 文件。

![](./media/image28.jpeg)

双击 **DemoController.java**
文件。在第一个练习中，仅提供了描述需要生成的代码的注释。

![](./media/image29.jpeg)

2.  将光标放在评论末尾（第 12 行），只需按 Enter
    键并等待几秒钟，**Copilot**
    就会为您生成代码。按选项卡，直到它为您提供完整的代码。

您也可以按 Ctrl + Enter 选择代码选项。

![](./media/image30.jpeg)

![](./media/image31.jpeg)

3.  展开**test **文件夹并单击 **CopilotDemoApplicationTests.java。**
    单元测试已经提供给你。

![](./media/image32.jpeg)

4.  您可以尝试在不更新 pom xml 的情况下运行代码，并向 Coiplot
    寻求解决方案来探索该产品。

5.  打开**Pom.xml**添加以下插件并保存文件

6.  \<plugin\>

7.  \<groupId\>org.apache.maven.plugins\</groupId\>

8.  \<artifactId\>maven-compiler-plugin\</artifactId\>

9.  \<version\>3.8.1\</version\>

10. \<configuration\>

11. \<source\>17\</source\>

12. \<target\>17\</target\>

13. \</configuration\>

\</plugin\>

![](./media/image33.jpeg)

14. 单击工具栏中的 **Terminal -\> New Terminal** 。

![](./media/image34.jpeg)

15. 选择 **Gitbash** 并运行以下命令。

cd exercisefiles/springboot/copilot-demo/

![](./media/image35.jpeg)

![](./media/image36.jpeg)

16. 运行 mvn clean install -DskipTests 命令

![](./media/image37.jpeg)

![](./media/image38.jpeg)

17. 运行 mvn test 。如果您的构建失败并出现错误。

![](./media/image39.jpeg)

18. 单击 右下角的 **Copilot** 图标，然后选择 **Github Copilot Chat**。

![](./media/image40.jpeg)

19. 要求 Github Copilot 聊天为您的错误提供修复。

![](./media/image41.jpeg)

20. 查看解释问题和相应修复的 Copilot
    聊天。如果您仍然不清楚修复方法，请继续提出您的疑问，Copilot
    会回答您。阅读并理解错误和要实施的解决方案。

![](./media/image42.jpeg)

21. 向 Copilot 提供 /hello 方法，让我们看看它会提出什么建议。

![](./media/image43.jpeg)

22. 返回CopilotDemoApplicationTests.java 在测试结束时（第 24
    行）将光标移开，然后按 Enter。Copilot
    会为你生成另一个测试。按选项卡接受它。

![](./media/image44.jpeg)

23. 向 Copilot 提供 /hello 测试方法，看看它会提出什么建议。

![](./media/image45.jpeg)

24. 重新运行 mvn 测试您的代码如下所示。您还可以编写自己的代码并要求
    Copilot 进行验证。

25. @RestController

26. public class DemoController {

27. @GetMapping("/hello")

28. public String hello(@RequestParam(name = "key", required = false)
    String key) {

29. if (key == null) {

30. return "key not passed";

31. }

32. return "hello " + key;

33. }

34. 

}

![](./media/image46.jpeg)

35. 运行 mvn package 命令

![](./media/image47.jpeg)

![](./media/image48.jpeg)

36. 运行 mvn spring-boot：run

![](./media/image49.jpeg)

37. 单击拆分 terminal 并在第二个终端中输入 curl -v
    http://localhost:8080/hello?key=world 。还可以要求 Copilot 提供 curl
    命令来测试代码。

![](./media/image50.jpeg)

38. 单击拆分终端并在第二个终端中输入 curl -v http://localhost:8080/hello

![](./media/image51.jpeg)

39. 按 Ctrl +C 停止正在运行的服务。

任务 2 ： 日期比较

/diffdates 下的新作，用于计算两个日期之间的差异。该作应以 dd-MM-yyyy
格式接收两个日期作为参数，并返回以天为单位的差异。

此外，创建验证作的单元测试。

从现在开始，您必须为每个新作创建单元测试。使用 Copilot 不是很容易吗？

1.  转到 **DemoController.java** 并输入提示 //在 /diffdates
    下创建计算两个日期之间差异的新作。该作应接收两个日期作为格式为
    dd-MM-yyyy 的参数，并返回以天为单位的差异，然后按
    Enter。等待一段时间，一旦助手预测代码，然后按选项卡接受代码。

![](./media/image52.jpeg)

2.  您也可以使用以下代码。

3.  @GetMapping("/diffdates")

4.  public String diffdates(@RequestParam(name = "date1", required =
    false) String date1, @RequestParam(name = "date2", required = false)
    String date2) throws ParseException {

5.  if (date1 == null \|\| date2 == null) {

6.  return "date not passed";

7.  }

8.  SimpleDateFormat sdf = new SimpleDateFormat("dd-MM-yyyy");

9.  Date date1Obj = sdf.parse(date1);

10. Date date2Obj = sdf.parse(date2);

11. long diffInMillies = Math.abs(date2Obj.getTime() -
    date1Obj.getTime());

12. long diff = TimeUnit.DAYS.convert(diffInMillies,
    TimeUnit.MILLISECONDS);

13. return "difference in days: " + diff;

}

![](./media/image53.jpeg)

14. From now on, you will have to create the unit tests for every new
    operation. Use Copilot to create.

15. Open **CopilotDemoApplicationTests.java** under the **test** folder
    and enter the prompt // create unit test to /diffdates that
    calculates the difference between two dates. The operation should
    receive two dates as parameter in format dd-MM-yyyy and return the
    difference in days. then press Enter. Wait for a sec to copilot to
    predict the code and press tab to accept the predicted code.

16. You can enter and press tab to create multiple unit tests

![](./media/image54.jpeg)

![](./media/image55.jpeg)

17. 获取 Copilot 聊天帮助以解决要修复的问题，或根据需要根据 Copilot
    输入解释单元测试和更新代码。

18. @Test

19. void diffdates() throws Exception {

20. mockMvc.perform(MockMvcRequestBuilders.get("/diffdates?date1=01-01-2021&date2=01-02-2021"))

21. .andExpect(MockMvcResultMatchers.status().isOk())

22. .andExpect(MockMvcResultMatchers.content().string("difference in
    days: 31"));

23. }

24. @Test

25. void diffdatesNoDate1() throws Exception {

26. mockMvc.perform(MockMvcRequestBuilders.get("/diffdates?date2=01-02-2021"))

27. .andExpect(MockMvcResultMatchers.status().isOk())

28. .andExpect(MockMvcResultMatchers.content().string("date not
    passed"));

29. }

30. @Test

31. void diffdatesNoDate2() throws Exception {

32. mockMvc.perform(MockMvcRequestBuilders.get("/diffdates?date1=01-01-2021"))

33. .andExpect(MockMvcResultMatchers.status().isOk())

34. .andExpect(MockMvcResultMatchers.content().string("date not
    passed"));

}

![](./media/image56.jpeg)

35. 打开 **Terminal -\>Gitbash** 并运行以下命令 

cd "exercisefiles\springboot\copilot-demo"

mvn test

![](./media/image57.jpeg)

36. 如果看到编译错误，请复制错误消息并要求 Copilot 进行修复。

![](./media/image58.jpeg)

37. Copolit 建议您导入带有代码的包。将命令添加到代码中并运行 mvn test

![](./media/image59.jpeg)

![](./media/image60.jpeg)

![](./media/image61.jpeg)

38. 运行 mvn 包

![](./media/image62.jpeg)

![](./media/image63.jpeg)

39. 运行测试 mvn -Dtest=CopilotDemoApplicationTests#diffdates 测试

![](./media/image64.jpeg)

30. 运行 mvn spring-boot：run

![](./media/image65.jpeg)

31. 单击拆分终端并运行 curl -v
    http://localhost:8080/diffdates?date1=01-01-2021&date2=01-02-2021

您将看到一个错误。获取 Copilot 帮助并解决小问题。

![](./media/image66.jpeg)

32. 作为 Copilot Chat 帮助您使用 curl
    命令。只需将错误消息复制为粘贴到聊天中即可。Copilot
    为您提供修改后的命令和解释

![](./media/image67.jpeg)

任务 3：验证西班牙语电话的格式

验证西班牙语电话号码的格式（+34 前缀，然后是 9 位数字，从 6、7 或 9
开始）。该作应接收电话号码作为参数，如果格式正确，则返回 true，否则返回
false。

1.  打开 DemoController.Java 并输入提示 //
    验证西班牙语电话号码的格式（+34 前缀，然后是 9 位数字，从 6、7 或 9
    开始）。该作应接收电话号码作为参数，如果格式正确，则返回
    true，否则返回 false。.按 Tab 接受代码。

![](./media/image68.jpeg)

2.  您也可以使用下面的代码。

3.  // Validate the format of a spanish phone number (+34 prefix, then 9
    digits, starting with 6, 7 or 9). The operation should receive a
    phone number as parameter and return true if the format is correct,
    false otherwise.

4.  @GetMapping("/validatephone")

5.  public boolean validatephone(@RequestParam(name = "phone", required
    = false) String phone) {

6.  if (phone == null \|\| phone.isEmpty()) {

7.  return false;

8.  }

9.  String regex = "^\\+34\[679\]\\d{8}\$";

10. return phone.matches(regex);

}

11. 切换到
    **CopilotDemoApplicationTests.java**。要编写单元测试来测试上述功能，请添加
    //编写单元测试以验证西班牙语电话号码的格式（+34 前缀，然后是 9
    位数字，从 6、7 或 9
    开始）。该作应接收一个电话号码作为参数，如果格式正确，则返回
    true，否则返回 false，否则按 Enter。按 选项卡接受代码。

![](./media/image69.jpeg)

12. 您还可以使用以下单元测试，也可以编写自己的单元测试。

13. @Test

14. void validatephone() throws Exception {

15. mockMvc.perform(MockMvcRequestBuilders.get("/validatephone?phone=+34666666666"))

16. .andExpect(MockMvcResultMatchers.status().isOk())

17. .andExpect(MockMvcResultMatchers.content().string("true"));

18. mockMvc.perform(MockMvcRequestBuilders.get("/validatephone?phone=+34766666666"))

19. .andExpect(MockMvcResultMatchers.status().isOk())

20. .andExpect(MockMvcResultMatchers.content().string("true"));

21. mockMvc.perform(MockMvcRequestBuilders.get("/validatephone?phone=+34966666666"))

22. .andExpect(MockMvcResultMatchers.status().isOk())

23. .andExpect(MockMvcResultMatchers.content().string("true"));

24. mockMvc.perform(MockMvcRequestBuilders.get("/validatephone?phone=+3466666666"))

25. .andExpect(MockMvcResultMatchers.status().isOk())

26. .andExpect(MockMvcResultMatchers.content().string("false"));

27. mockMvc.perform(MockMvcRequestBuilders.get("/validatephone?phone=+346666666666"))

28. .andExpect(MockMvcResultMatchers.status().isOk())

29. .andExpect(MockMvcResultMatchers.content().string("false"));

30. mockMvc.perform(MockMvcRequestBuilders.get("/validatephone?phone=+3466666666a"))

31. .andExpect(MockMvcResultMatchers.status().isOk())

32. .andExpect(MockMvcResultMatchers.content().string("false"));

33. mockMvc.perform(MockMvcRequestBuilders.get("/validatephone?phone=+34866666666"))

34. .andExpect(MockMvcResultMatchers.status().isOk())

35. .andExpect(MockMvcResultMatchers.content().string("false"));

36. }

37. @Test

38. void validatephoneNoPhone() throws Exception {

39. mockMvc.perform(MockMvcRequestBuilders.get("/validatephone"))

40. .andExpect(MockMvcResultMatchers.status().isOk())

41. .andExpect(MockMvcResultMatchers.content().string("false"));

}

42. 打开 **Terminal -\>Gitbash** 并运行以下命令。 

cd exercisefiles/springboot/copilot-demo/

mvn test

![](./media/image70.jpeg)

45. 运行 mvn 包

![](./media/image71.jpeg)

46. 运行 mvn spring-boot：run

![](./media/image72.jpeg)

47. 拆分终端并运行以下 curl 命令来验证电话号码。

curl -v http://localhost:8080/validatephone?phone=+34866666666

curl -v http://localhost:8080/validatephone?phone=+34666666667

curl -v http://localhost:8080/validatephone?phone=+34666666666

![](./media/image73.jpeg)

任务 4：验证西班牙语 DNI 的格式

验证西班牙语 DNI 的格式（8 位数字和 1 个字母）。该作应接收 DNI
作为参数，如果格式正确，则返回 true，否则返回 false。

1.  打开 DemoController.Java 并输入提示符 // 验证西班牙语 DNI 的格式（8
    位数字和 1 个字母）。该作应接收 DNI 作为参数，如果格式正确，则返回
    true，否则返回 false。.按选项卡接受代码。

![](./media/image74.jpeg)

2.  您也可以使用以下代码

3.  // Validate the format of a spanish DNI (8 digits and 1 letter). The
    operation should receive a DNI as parameter and return true if the
    format is correct, false otherwise.

4.  @GetMapping("/validatedni")

5.  public boolean validatedni(@RequestParam(name = "dni", required =
    false) String dni) {

6.  if (dni == null \|\| dni.isEmpty()) {

7.  return false;

8.  }

9.  String regex = "^\\d{8}\[A-Z\]\$";

10. return dni.matches(regex);

}

11. 切换到
    **CopilotDemoApplicationTests.java**。要编写单元测试来测试上述函数，请添加
    //编写单元测试以验证西班牙语 DNI 的格式（8 位数字和 1
    个字母）。该作应接收 DNI 作为参数，如果格式正确，则返回
    true，否则返回 false，否则按 Enter。按 选项卡接受代码。

![](./media/image75.jpeg)

12. 您也可以使用以下单元测试，也可以编写自己的单元测试。

13. @Test

14. void validatedniNoDni() throws Exception {

15. mockMvc.perform(MockMvcRequestBuilders.get("/validatedni"))

16. .andExpect(MockMvcResultMatchers.status().isOk())

17. .andExpect(MockMvcResultMatchers.content().string("false"));

}

18. 打开 Terminal -\> Gitbash 并运行以下命令。

cd exercisefiles/springboot/copilot-demo/

mvn test

![](./media/image76.jpeg)

![](./media/image77.jpeg)

19. 运行 mvn 包

![](./media/image78.jpeg)

![](./media/image79.jpeg)

20. 运行 mvn spring-boot：run

![](./media/image80.jpeg)

21. 拆分终端并运行 curl -v
    http://localhost:8080/validatedni?dni=12345678C in \>the
    2<sup>nd</sup>terminal

![](./media/image81.jpeg)

任务 5 ： 从颜色名称到十六进制代码

根据资源下的现有colors.json文件，给定颜色作为路径参数的名称，返回十六进制代码。如果未找到颜色，则返回
404

提示：使用 TDD。首先创建单元测试，然后实现代码。

1.  打开 DemoController.Java 并输入提示 //
    根据资源下的现有colors.json文件，给定颜色作为路径参数的名称，返回十六进制代码。如果未找到颜色，则返回
    404 。按选项卡接受代码。

![](./media/image82.jpeg)

2.  您也可以使用以下代码，也可以编写代码。

3.  //Based on existing colors.json file under resources, given the name
    of the color as path parameter, return the hexadecimal code. If the
    color is not found, return 404

4.  @GetMapping("/color/{name}")

5.  public ResponseEntity\<String\> color(@PathVariable("name") String
    name) throws IOException {

6.  InputStream inputStream =
    getClass().getClassLoader().getResourceAsStream("colors.json");

7.  ObjectMapper objectMapper = new ObjectMapper();

8.  // create JsonNode from mapper

9.  JsonNode rootNode = objectMapper.readTree(inputStream);

10. for (JsonNode color : rootNode) {

11. // if color name is found, return the hex code

12. if (color.get("color").asText().equals(name)) {

13. return new
    ResponseEntity\<String\>(color.get("code").get("hex").asText(),
    HttpStatus.OK);

14. }

15. }

16. return new ResponseEntity\<String\>("Color not found",
    HttpStatus.NOT_FOUND);

}

17. 切换到
    **CopilotDemoApplicationTests.java**。要编写单元测试来测试上述函数，请添加
    //test for /color/{color} endpoint 按 Enter。按 tab 接受代码。

![](./media/image83.jpeg)

18. 您可以编写单元测试。您可以随时与 Copilot 检查任何 code/fix /unit
    测试

19. 打开 **Terminal -\> Gitbash** 并运行以下命令。你可以看到编译错误。

cd exercisefiles/springboot/copilot-demo/

mvn test

![](./media/image84.jpeg)

20. 按 **Ctrl +Alt+ I** 打开 **Github Copilot
    Chat**。复制错误消息并粘贴到聊天窗口中。Copilot 建议解决方案。

![](./media/image85.jpeg)

21. Copilot
    建议使用导入函数导入丢失的包。复制它并将其添加到您的代码中。按 Enter
    键，Copilot 会建议您添加缺少的包。按选项卡并接受它们以添加到代码中。

![](./media/image86.jpeg)

![](./media/image87.jpeg)

22. 打开 **Terminal -\> Gitbash** 并再次运行以下命令。 

cd exercisefiles/springboot/copilot-demo/

mvn test

![](./media/image88.jpeg)

![](./media/image89.jpeg)

23. 运行 mvn package 打包您的应用程序。

![](./media/image90.jpeg)

![](./media/image91.jpeg)

24. 运行 mvn spring-boot：run 进行测试

![](./media/image92.jpeg)

25. 您可以要求助手帮助使用 curl 命令来测试您的功能。

![](./media/image93.jpeg)

26. 单击**Split terminal** 并运行 curl
    命令来测试您的应用程序。（更新端口）

![](./media/image94.jpeg)

27. 使用 **colors.json** 文件中列出的颜色进行测试

![](./media/image95.jpeg)

28. 测试**colors.json**中未列出的颜色并查看结果

![](./media/image96.jpeg)

任务 6 ： 笑话创作者

创建一个调用 API https://api.chucknorris.io/jokes/random
并返回笑话的新作。

1.  打开 DemoController.Java 并输入调用 API
    https://api.chucknorris.io/jokes/random 并返回 joke 的提示词 //
    new作。按选项卡接受代码。

![](./media/image97.jpeg)

![](./media/image98.jpeg)

2.  您也可以使用下面的代码。

3.  // new operation that call the API
    https://api.chucknorris.io/jokes/random and return the joke

4.  @GetMapping("/joke")

5.  public String getJoke() {

6.  RestTemplate restTemplate = new RestTemplate();

7.  String url = "https://api.chucknorris.io/jokes/random";

8.  ResponseEntity\<String\> response = restTemplate.getForEntity(url,
    String.class);

9.  // parse response to get the value

10. ObjectMapper objectMapper = new ObjectMapper();

11. JsonNode rootNode;

12. try {

13. rootNode = objectMapper.readTree(response.getBody());

14. return rootNode.get("value").asText();

15. } catch (IOException e) {

16. return new String("Error getting joke");

17. }

}

![](./media/image99.jpeg)

18. 切换到
    **CopilotDemoApplicationTests.java**。要编写单元测试来测试上述函数，请添加
    // 为调用 API https://api.chucknorris.io/jokes/random
    并返回笑话的新作创建单元测试按 Enter 键。按 tab 接受代码。

![](./media/image100.jpeg)

19. 您也可以在下面添加单元测试，也可以编写自己的单元测试。

20. @Test

21. void joke() throws Exception{

22. mockMvc.perform(MockMvcRequestBuilders.get("/joke"))

23. .andExpect(MockMvcResultMatchers.status().isOk())

24. // check that content is a string

25. .andExpect(MockMvcResultMatchers.content().string(Matchers.any(String.class)));

}

![](./media/image101.jpeg)

26. 打开 Terminal -\> Gitbahs 并运行以下命令。

cd exercisefiles/springboot/copilot-demo/

mvn test

![](./media/image101.jpeg)

![](./media/image102.jpeg)

27. 打包您的应用程序。运行 mvn 包

![](./media/image103.jpeg)

![](./media/image104.jpeg)

28. 运行 mvn spring-boot：run

![](./media/image105.jpeg)

![](./media/image106.jpeg)

29. 单击拆分终端并运行命令：curl -v http://localhost:8080/joke
    在第二个终端中

![](./media/image107.jpeg)

任务 7：URL 解析

给定一个 url
作为查询参数，解析它并返回协议、主机、端口、路径和查询参数。响应应采用
Json 格式。

1.  打开 **DemoController.Java** 并输入提示 //给定一个 url
    作为查询参数编写代码，解析它并返回协议、主机、端口、路径和查询参数。响应应采用
    Json 格式。按选项卡接受代码。

![](./media/image108.jpeg)

2.  您也可以使用以下代码。

3.  // Given a url as query parameter, parse it and return the protocol,
    host, port, path and query parameters. The response should be in
    Json format.

4.  @GetMapping("/parseurl")

5.  public String parseurl(@RequestParam(name = "url", required = false)
    String url) throws MalformedURLException {

6.  if (url == null \|\| url.isEmpty()) {

7.  return "url not passed";

8.  }

9.  URL urlObj = new URL(url);

10. String protocol = urlObj.getProtocol();

11. String host = urlObj.getHost();

12. int port = urlObj.getPort();

13. String path = urlObj.getPath();

14. String query = urlObj.getQuery();

15. return "{ \\protocol\\: \\" + protocol + "\\, \\host\\: \\" + host +
    "\\, \\port\\: \\" + port + "\\, \\path\\: \\" + path + "\\,
    \\query\\: \\" + query + "\\ }";

}

![](./media/image109.jpeg)

16. 切换到
    **CopilotDemoApplicationTests.java**。要编写单元测试来测试上述函数，请添加
    // 为调用 API https://api.chucknorris.io/jokes/random
    并返回笑话的新作创建单元测试按 Enter 键。按 tab 接受代码。

![](./media/image110.jpeg)

17. 您还可以添加以下单元测试或编写自己的单元测试。

18. @Test

19. void parseUrl() throws Exception{

20. mockMvc.perform(MockMvcRequestBuilders.get("/parseurl?url=https://learn.microsoft.com/en-us/azure/aks/concepts-clusters-workloads?source=recommendations"))

21. .andExpect(MockMvcResultMatchers.status().isOk())

22. // validate json fields

23. .andExpect(MockMvcResultMatchers.jsonPath("\$.protocol").value("https"))

24. .andExpect(MockMvcResultMatchers.jsonPath("\$.host").value("learn.microsoft.com"))

25. .andExpect(MockMvcResultMatchers.jsonPath("\$.path").value("/en-us/azure/aks/concepts-clusters-workloads"))

26. .andExpect(MockMvcResultMatchers.jsonPath("\$.query").value("source=recommendations"));

27. }

28. @Test

29. void parseUrlNoUrl() throws Exception{

30. mockMvc.perform(MockMvcRequestBuilders.get("/parseurl"))

31. .andExpect(MockMvcResultMatchers.status().isOk())

32. .andExpect(MockMvcResultMatchers.content().string("url not
    passed"));

}

![](./media/image111.jpeg)

33. 打开 **Terminal -\> Gitbash** 并运行以下命令。 

cd exercisefiles/springboot/copilot-demo/

mvn test

![](./media/image112.jpeg)

![](./media/image113.jpeg)

34. 运行 mvn package 打包您的应用程序。

![](./media/image114.jpeg)

35. 运行 mvn spring-boot：run

![](./media/image115.jpeg)

![](./media/image116.jpeg)

36. 拆分终端并测试您的应用程序：curl -v
    http://localhost:8080/parseurl?url=https://www.google.com/search?q=chuck+norris

![](./media/image117.jpeg)

任务 8 ： 字数统计

给定文件的路径并计算所提供单词的出现次数。路径和单词应该是查询参数。响应应采用
Json 格式。

1.  打开 **DemoController.Java** 并输入提示
    //给定文件路径的代码并计算所提供单词的出现次数。路径和单词应该是查询参数。响应应采用
    Json 格式。按选项卡接受代码。

![](./media/image118.jpeg)

2.  切换到
    **CopilotDemoApplicationTests.java**。要编写单元测试来测试上述函数，请添加
    //
    给定文件的路径并计算所提供单词的出现次数。路径和单词应该是查询参数。响应应采用
    Json 格式。按 Enter 键。按 选项卡接受代码。

![](./media/image119.jpeg)

3.  打开 **Terminal -\> Gitbash**并运行以下命令。

cd exercisefiles/springboot/copilot-demo/

mvn test

![](./media/image120.jpeg)

![](./media/image121.jpeg)

4.  运行 mvn package 打包您的应用程序/

![](./media/image122.jpeg)

5.  运行 mvn spring-boot：run

![](./media/image123.jpeg)

6.  单击拆分终端并运行 curl 命令来测试您的应用程序。

curl http://localhost:8080/countword?path=src/test/resources/test.txt

![](./media/image124.jpeg)

任务 9：容器化应用程序

使用提供的 Dockerfile 创建应用程序的 Docker 映像。Dockerfile
中有一些注释可以帮助您完成练习。

为了生成、运行和测试 docker 映像，您也可以使用 Copilot 生成命令。

例如，创建一个 DOCKER.md 文件，您可以在其中存储用于构建、运行和测试
docker 映像的命令。您会注意到 Copilot 还将帮助您记录您的项目和命令。

要记录的步骤示例：生成容器映像、运行容器、测试容器。

1.  双击 Dekstop 中的 Docker 并使用您的帐户登录。

2.  打开 Docker 文件 om Visual Studio
    代码，向其中添加以下代码并保存文件。

3.  \# 基于openjdk 17构建java应用镜像，在8080端口上运行

4.  FROM openjdk:17-jdk-alpine

5.  EXPOSE 8080

6.  COPY target/\*.jar app.jar

ENTRYPOINT \["java","-jar","/app.jar"\]

![](./media/image125.jpeg)

7.  按 **Ctrl +Alt +I** 打开 **GitHub Copilot** 聊天窗口。询问 Copilot
    以下提示。Copilot 提供了容器化应用程序的步骤。

如何使用提供的 Dockerfile 构建、运行和测试 docker 映像，以创建应用程序的
docker 映像

![](./media/image126.jpeg)

8.  按照第一步 - 构建 Docker 镜像。打开 \*\*Terminal -\> Gitbash\*\*
    并运行命令来构建 Docker 镜像。

cd exercisefiles/springboot/copilot-demo/

docker build -t my-application .

![](./media/image127.jpeg)

![](./media/image128.jpeg)

![](./media/image129.jpeg)

9.  构建镜像后，您可以使用 docker run 命令运行它。

docker run -p 8080:8080 my-application

![](./media/image130.jpeg)

10. Docker 容器运行后，您可以通过向应用程序发送请求来对其进行测试。

curl \<http://localhost:8080/hello?key=world

![](./media/image131.jpeg)

