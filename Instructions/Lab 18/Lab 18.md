**實驗室 18 - 在 GitHub Copilot 的幫助下使用 Spring Boot 生成 REST API**

**目標**

本實驗室的目標是學習如何使用 GitHub Copilot，使用包括使用 Spring Boot
生成 REST API 的練習。

我們已經創建了一個 Spring Boot
項目，其中已經創建了一些文件，您可以在文件夾
**C：\CopilotHackathon\exercisefiles\springboot 中找到該項目**。

在執行本練習之前，讓我們先安裝必要的軟件包並設置環境。

任務 0：安裝和設置環境

您需要下載並安裝以下軟件包來設置環境以執行本練習。

a\. Microsoft JDK 17

b\. apache maven

1.  打開 Edge 瀏覽器。

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image1.jpeg)

2.  在瀏覽器 URL 字段中，複製粘貼鏈接以將軟件包下載到實驗室 VM。

a\. Microsoft JDK 17
◊ https://aka.ms/download-jdk/microsoft-jdk-17.0.12-windows-x64.msi

b\. apache maven
◊https://dlcdn.apache.org/maven/maven-3/3.9.9/binaries/apache-maven-3.9.9-bin.zip

**注意：**重複相同的步驟以下載所有其他軟件包。默認情況下，包將保存在下載文件夾中。

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image2.jpeg)

a. **安裝 Microsoft JDK 17**

1.  在 **Downloads** (**C:\Users\Admin\Downloads**)
    文件夾中，雙擊“**Microsoft JDK**”

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image3.jpeg)

2.  單擊 **Next**。 

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image4.jpeg)

3.  接受 EULA 並單擊 **Next**。

![A screenshot of a software agreement AI-generated content may be
incorrect.](./media/image5.jpeg)

4.  選擇“**Install just for you (Admin)**”，然後單擊“**Next**”。 

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image6.jpeg)

5.  在 **Custom setup** 屏幕中，您現在將 **set the JAVA_HOME
    variable**。單擊向下箭頭並選擇 **Entire feature will be installed on
    local hard drive**。

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image7.jpeg)

6.  單擊 **Next**。 

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image8.jpeg)

7.  單擊 **Install**。 

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image9.jpeg)

**b. Install apache- maven**

8.  導航到 **Downloads** (**C:\Users\Admin\Downloads**) 文件夾

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image10.jpeg)

9.  右鍵單擊 **apache-maven-3.9.9-bin.zip** 文件夾，然後選擇 **Extract
    All**。

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image11.jpeg)

10. 在“**Select a destination**”頁面中，輸入目標為
    **C：\Users\Admin\Downloads，**然後單擊“**Extract**”。

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image12.jpeg)

11. 提取的文件將如屏幕截圖所示。

**注意：**如果您看到任何其他名稱，請確保該文件夾已重命名為
**apache-maven-3.9.9**。

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image13.jpeg)

**設置環境變量**

12. 單擊 **Windows logo** 並選擇 **Settings**

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image14.jpeg)

13. 在 **Windows settings** 頁面中搜索編輯系統，然後選擇 **Edit System
    Environment variable**。

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image15.jpeg)

14. 單擊“**Environment Variable** ”按鈕。 

![A screenshot of a computer program AI-generated content may be
incorrect.](./media/image16.jpeg)

15. 單擊“**User variable for Admin**”部分的“**New** ”。 

![A screenshot of a computer program AI-generated content may be
incorrect.](./media/image17.jpeg)

16. 現在，您將為 Maven 設置環境和路徑變量。

在“**User variable for Admin**”部分下選擇“**New**”。 

![A screenshot of a computer program AI-generated content may be
incorrect.](./media/image18.jpeg)

17. 在“**New User Variable** ”窗口中，輸入以下內容，然後單擊“**OK**”

Variable name: MAVEN_HOME

Variable value: C:\Users\Admin\Downloads\apache-maven-3.9.9

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image19.jpeg)

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image20.jpeg)

18. 現在選擇 **Path** 並單擊 **Edit** 

![A screenshot of a computer program AI-generated content may be
incorrect.](./media/image21.jpeg)

19. 在“**Edit environment variable**”窗口中，單擊“**New**”。

![A screenshot of a computer program AI-generated content may be
incorrect.](./media/image22.jpeg)

20. 在空白字段中，輸入以下 %MAVEN_HOME%\bin，然後單擊 **OK**。

![A screenshot of a computer program AI-generated content may be
incorrect.](./media/image23.jpeg)

![A screenshot of a computer program AI-generated content may be
incorrect.](./media/image24.jpeg)

21. 單擊“**Ok**”以完成 Maven 的用戶環境和路徑變量的設置。

![A screenshot of a computer program AI-generated content may be
incorrect.](./media/image25.jpeg)

22. 現在，您將為 Maven 設置 **System variables** 。在 **System
    variables**  部分下選擇**New**。

![A screenshot of a computer program AI-generated content may be
incorrect.](./media/image26.jpeg)

23. 在“New System Variable”窗口中，輸入以下內容，然後單擊“**OK**”

Variable name: MAVEN_HOME

Variable value: C:\Users\Admin\Downloads\apache-maven-3.9.9

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image27.jpeg)

任務 1 ：創建代碼以處理簡單的 GET 請求

移動到“DemoController.java”文件並開始編寫代碼來處理簡單的 GET
請求。在第一個練習中，我們提供了一個注釋，描述了您需要生成的代碼。只需按
Enter 並等待幾秒鐘，Copilot 就會為您生成代碼。

本練習已經實現了單元測試，可以在之前和之後使用命令 mvn test
運行它，以驗證 Copilot 生成的代碼是否正確。

然後，在請求中未提供密鑰時，為案例創建新的單元測試。

每次練習結束後，請隨意打包並運行您的應用程序以對其進行測試。

Package: mvn package

Run: mvn spring-boot:run

Test: curl -v http://localhost:8080/hello?key=world

1.  打開文件資源管理器，展開 Local Disk (C:)，然後展開
    **CopilotHackathon-\>exercisefiles \> Springboot \> copilot-demo \>
    src\>main\>java\>com\>Microsoft\>hackathon\>copilotdemo\>controller** 文件夾，查看
    **'DemoController.java** 文件。

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image28.jpeg)

雙擊 **DemoController.java**
文件。在第一個練習中，僅提供了描述需要生成的代碼的注釋。

![A screenshot of a computer Description automatically
generated](./media/image29.png)

2.  將光標放在評論末尾（第 12 行），只需按 Enter
    鍵並等待幾秒鐘，**Copilot**
    就會為您生成代碼。按選項卡，直到它為您提供完整的代碼。

您也可以按 Ctrl + Enter 選擇代碼選項。

![A screenshot of a computer Description automatically
generated](./media/image30.png)

![A screenshot of a computer Description automatically
generated](./media/image31.png)

3.  展開**test **文件夾並單擊 **CopilotDemoApplicationTests.java。**
    單元測試已經提供給你。

![A screenshot of a computer screen Description automatically
generated](./media/image32.png)

4.  您可以嘗試在不更新 pom xml 的情況下運行代碼，並向 Coiplot
    尋求解決方案來探索該產品。

5.  打開**Pom.xml**添加以下插件並保存文件

6.  \<plugin\>

7.  \<groupId\>org.apache.maven.plugins\</groupId\>

8.  \<artifactId\>maven-compiler-plugin\</artifactId\>

9.  \<version\>3.8.1\</version\>

10. \<configuration\>

11. \<source\>17\</source\>

12. \<target\>17\</target\>

13. \</configuration\>

\</plugin\>

![A screenshot of a computer program Description automatically
generated](./media/image33.png)

14. 單擊工具欄中的 **Terminal -\> New Terminal** 。

![BrokenImage](./media/image34.png)

15. 選擇 **Gitbash** 並運行以下命令。

cd exercisefiles/springboot/copilot-demo/

![BrokenImage](./media/image35.png)

![A screenshot of a computer program Description automatically
generated](./media/image36.png)

16. 運行 mvn clean install -DskipTests 命令

![A screen shot of a computer program Description automatically
generated](./media/image37.png)

![A screenshot of a computer Description automatically
generated](./media/image38.png)

17. 運行 mvn test 。如果您的構建失敗並出現錯誤。

![A screenshot of a computer program Description automatically
generated](./media/image39.png)

18. 單擊 右下角的 **Copilot** 圖標，然後選擇 **Github Copilot Chat**。

![BrokenImage](./media/image40.png)

19. 要求 Github Copilot 聊天為您的錯誤提供修復。

![A screenshot of a computer screen Description automatically
generated](./media/image41.png)

20. 查看解釋問題和相應修復的 Copilot
    聊天。如果您仍然不清楚修復方法，請繼續提出您的疑問，Copilot
    會回答您。閱讀並理解錯誤和要實施的解決方案。

![A screenshot of a computer program Description automatically
generated](./media/image42.png)

21. 向 Copilot 提供 /hello 方法，讓我們看看它會提出什麼建議。

![BrokenImage](./media/image43.png)

22. 返回CopilotDemoApplicationTests.java 在測試結束時（第 24
    行）將光標移開，然後按 Enter。Copilot
    會為你生成另一個測試。按選項卡接受它。

![A screenshot of a computer program Description automatically
generated](./media/image44.png)

23. 向 Copilot 提供 /hello 測試方法，看看它會提出什麼建議。

![A screenshot of a computer Description automatically
generated](./media/image45.png)

24. 重新運行 mvn 測試您的代碼如下所示。您還可以編寫自己的代碼並要求
    Copilot 進行驗證。

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

![A screenshot of a computer program Description automatically
generated](./media/image46.png)

35. 運行 mvn package 命令

![A screenshot of a computer program Description automatically
generated](./media/image47.png)

![A screenshot of a computer program Description automatically
generated](./media/image48.png)

36. 運行 mvn spring-boot：run

![A screenshot of a computer program Description automatically
generated](./media/image49.png)

37. 單擊拆分 terminal 並在第二個終端中輸入 curl -v
    http://localhost:8080/hello?key=world 。還可以要求 Copilot 提供 curl
    命令來測試代碼。

![BrokenImage](./media/image50.png)

38. 單擊拆分終端並在第二個終端中輸入 curl -v http://localhost:8080/hello

![A screenshot of a computer program Description automatically
generated](./media/image51.png)

39. 按 Ctrl +C 停止正在運行的服務。

任務 2 ： 日期比較

/diffdates 下的新作，用於計算兩個日期之間的差異。該作應以 dd-MM-yyyy
格式接收兩個日期作為參數，並返回以天為單位的差異。

此外，創建驗證作的單元測試。

從現在開始，您必須為每個新作創建單元測試。使用 Copilot 不是很容易嗎？

1.  轉到 **DemoController.java** 並輸入提示 //在 /diffdates
    下創建計算兩個日期之間差異的新作。該作應接收兩個日期作為格式為
    dd-MM-yyyy 的參數，並返回以天為單位的差異，然後按
    Enter。等待一段時間，一旦助手預測代碼，然後按選項卡接受代碼。

![BrokenImage](./media/image52.png)

2.  您也可以使用以下代碼。

3.  @GetMapping("/diffdates")

4.  public String diffdates(@RequestParam(name = "date1", required =
    false) String date1, @RequestParam(name = "date2", required = false)
    String date2) throws ParseException {

5.  if (date1 == null || date2 == null) {

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

![A screenshot of a computer program Description automatically
generated](./media/image53.png)

14. From now on, you will have to create the unit tests for every new
    operation. Use Copilot to create.

15. Open **CopilotDemoApplicationTests.java** under the **test** folder
    and enter the prompt // create unit test to /diffdates that
    calculates the difference between two dates. The operation should
    receive two dates as parameter in format dd-MM-yyyy and return the
    difference in days. then press Enter. Wait for a sec to copilot to
    predict the code and press tab to accept the predicted code.

16. You can enter and press tab to create multiple unit tests

![A computer screen shot of a program Description automatically
generated](./media/image54.png)

![A screenshot of a computer program Description automatically
generated](./media/image55.png)

17. 獲取 Copilot 聊天幫助以解決要修復的問題，或根據需要根據 Copilot
    輸入解釋單元測試和更新代碼。

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

![A screenshot of a computer program Description automatically
generated](./media/image56.png)

35. 打開 **Terminal -\>Gitbash** 並運行以下命令 

cd "exercisefiles\springboot\copilot-demo"

mvn test

![BrokenImage](./media/image57.png)

36. 如果看到編譯錯誤，請複製錯誤消息並要求 Copilot 進行修復。

![BrokenImage](./media/image58.png)

37. Copolit 建議您導入帶有代碼的包。將命令添加到代碼中並運行 mvn test

![A screenshot of a computer program Description automatically
generated](./media/image59.png)

![A screenshot of a computer program Description automatically
generated](./media/image60.png)

![A screenshot of a computer program Description automatically
generated](./media/image61.png)

38. 運行 mvn 包

![A screenshot of a computer program Description automatically
generated](./media/image62.png)

![A screenshot of a computer program Description automatically
generated](./media/image63.png)

39. 運行測試 mvn -Dtest=CopilotDemoApplicationTests#diffdates 測試

![A screenshot of a computer program Description automatically
generated](./media/image64.png)

30. 運行 mvn spring-boot：run

![A screen shot of a computer program Description automatically
generated](./media/image65.png)

31. 單擊拆分終端並運行 curl -v
    http://localhost:8080/diffdates?date1=01-01-2021&date2=01-02-2021

您將看到一個錯誤。獲取 Copilot 幫助並解決小問題。

![A screenshot of a computer screen Description automatically
generated](./media/image66.png)

32. 作為 Copilot Chat 幫助您使用 curl
    命令。只需將錯誤消息複製為粘貼到聊天中即可。Copilot
    為您提供修改後的命令和解釋

![A screenshot of a computer program Description automatically
generated](./media/image67.png)

任務 3：驗證西班牙語電話的格式

驗證西班牙語電話號碼的格式（+34 前綴，然後是 9 位數字，從 6、7 或 9
開始）。該作應接收電話號碼作為參數，如果格式正確，則返回 true，否則返回
false。

1.  打開 DemoController.Java 並輸入提示 //
    驗證西班牙語電話號碼的格式（+34 前綴，然後是 9 位數字，從 6、7 或 9
    開始）。該作應接收電話號碼作為參數，如果格式正確，則返回
    true，否則返回 false。.按 Tab 接受代碼。

![A screen shot of a computer program Description automatically
generated](./media/image68.png)

2.  您也可以使用下面的代碼。

3.  // Validate the format of a spanish phone number (+34 prefix, then 9
    digits, starting with 6, 7 or 9). The operation should receive a
    phone number as parameter and return true if the format is correct,
    false otherwise.

4.  @GetMapping("/validatephone")

5.  public boolean validatephone(@RequestParam(name = "phone", required
    = false) String phone) {

6.  if (phone == null || phone.isEmpty()) {

7.  return false;

8.  }

9.  String regex = "^\\+34\[679\]\\d{8}$";

10. return phone.matches(regex);

}

11. 切換到
    **CopilotDemoApplicationTests.java**。要編寫單元測試來測試上述功能，請添加
    //編寫單元測試以驗證西班牙語電話號碼的格式（+34 前綴，然後是 9
    位數字，從 6、7 或 9
    開始）。該作應接收一個電話號碼作為參數，如果格式正確，則返回
    true，否則返回 false，否則按 Enter。按 選項卡接受代碼。

![A computer screen shot of a program Description automatically
generated](./media/image69.png)

12. 您還可以使用以下單元測試，也可以編寫自己的單元測試。

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

42. 打開 **Terminal -\>Gitbash** 並運行以下命令。 

cd exercisefiles/springboot/copilot-demo/

mvn test

![A screenshot of a computer program Description automatically
generated](./media/image70.png)

45. 運行 mvn 包

![A screenshot of a computer program Description automatically
generated](./media/image71.png)

46. 運行 mvn spring-boot：run

![A screenshot of a computer program Description automatically
generated](./media/image72.png)

47. 拆分終端並運行以下 curl 命令來驗證電話號碼。

curl -v http://localhost:8080/validatephone?phone=+34866666666

curl -v http://localhost:8080/validatephone?phone=+34666666667

curl -v http://localhost:8080/validatephone?phone=+34666666666

![A screenshot of a computer screen Description automatically
generated](./media/image73.png)

任務 4：驗證西班牙語 DNI 的格式

驗證西班牙語 DNI 的格式（8 位數字和 1 個字母）。該作應接收 DNI
作為參數，如果格式正確，則返回 true，否則返回 false。

1.  打開 DemoController.Java 並輸入提示符 // 驗證西班牙語 DNI 的格式（8
    位數字和 1 個字母）。該作應接收 DNI 作為參數，如果格式正確，則返回
    true，否則返回 false。.按選項卡接受代碼。

![A screen shot of a computer program Description automatically
generated](./media/image74.png)

2.  您也可以使用以下代碼

3.  // Validate the format of a spanish DNI (8 digits and 1 letter). The
    operation should receive a DNI as parameter and return true if the
    format is correct, false otherwise.

4.  @GetMapping("/validatedni")

5.  public boolean validatedni(@RequestParam(name = "dni", required =
    false) String dni) {

6.  if (dni == null || dni.isEmpty()) {

7.  return false;

8.  }

9.  String regex = "^\\d{8}\[A-Z\]$";

10. return dni.matches(regex);

}

11. 切換到
    **CopilotDemoApplicationTests.java**。要編寫單元測試來測試上述函數，請添加
    //編寫單元測試以驗證西班牙語 DNI 的格式（8 位數字和 1
    個字母）。該作應接收 DNI 作為參數，如果格式正確，則返回
    true，否則返回 false，否則按 Enter。按 選項卡接受代碼。

![A screenshot of a computer program Description automatically
generated](./media/image75.png)

12. 您也可以使用以下單元測試，也可以編寫自己的單元測試。

13. @Test

14. void validatedniNoDni() throws Exception {

15. mockMvc.perform(MockMvcRequestBuilders.get("/validatedni"))

16. .andExpect(MockMvcResultMatchers.status().isOk())

17. .andExpect(MockMvcResultMatchers.content().string("false"));

}

18. 打開 Terminal -\> Gitbash 並運行以下命令。

cd exercisefiles/springboot/copilot-demo/

mvn test

![A screenshot of a computer program Description automatically
generated](./media/image76.png)

![A screenshot of a computer program Description automatically
generated](./media/image77.png)

19. 運行 mvn 包

![A screenshot of a computer program Description automatically
generated](./media/image78.png)

![A screenshot of a computer program Description automatically
generated](./media/image79.png)

20. 運行 mvn spring-boot：run

![A screenshot of a computer program Description automatically
generated](./media/image80.png)

21. 拆分終端並運行 curl -v
    http://localhost:8080/validatedni?dni=12345678C in \>the
    2^(nd)terminal

![A screenshot of a computer program Description automatically
generated](./media/image81.png)

任務 5 ： 從顏色名稱到十六進制代碼

根據資源下的現有colors.json文件，給定顏色作為路徑參數的名稱，返回十六進制代碼。如果未找到顏色，則返回
404

提示：使用 TDD。首先創建單元測試，然後實現代碼。

1.  打開 DemoController.Java 並輸入提示 //
    根據資源下的現有colors.json文件，給定顏色作為路徑參數的名稱，返回十六進制代碼。如果未找到顏色，則返回
    404 。按選項卡接受代碼。

![A screen shot of a computer program Description automatically
generated](./media/image82.png)

2.  您也可以使用以下代碼，也可以編寫代碼。

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

17. 切換到
    **CopilotDemoApplicationTests.java**。要編寫單元測試來測試上述函數，請添加
    //test for /color/{color} endpoint 按 Enter。按 tab 接受代碼。

![A screenshot of a computer program Description automatically
generated](./media/image83.png)

18. 您可以編寫單元測試。您可以隨時與 Copilot 檢查任何 code/fix /unit
    測試

19. 打開 **Terminal -\> Gitbash** 並運行以下命令。你可以看到編譯錯誤。

cd exercisefiles/springboot/copilot-demo/

mvn test

![A screenshot of a computer program Description automatically
generated](./media/image84.png)

20. 按 **Ctrl +Alt+ I** 打開 **Github Copilot
    Chat**。複製錯誤消息並粘貼到聊天窗口中。Copilot 建議解決方案。

![A screenshot of a computer program Description automatically
generated](./media/image85.png)

21. Copilot
    建議使用導入函數導入丟失的包。複製它並將其添加到您的代碼中。按 Enter
    鍵，Copilot 會建議您添加缺少的包。按選項卡並接受它們以添加到代碼中。

![A screenshot of a computer program Description automatically
generated](./media/image86.png)

![A screenshot of a computer Description automatically
generated](./media/image87.png)

22. 打開 **Terminal -\> Gitbash** 並再次運行以下命令。 

cd exercisefiles/springboot/copilot-demo/

mvn test

![A screenshot of a computer program Description automatically
generated](./media/image88.png)

![A screenshot of a computer program Description automatically
generated](./media/image89.png)

23. 運行 mvn package 打包您的應用程序。

![A screenshot of a computer program Description automatically
generated](./media/image90.png)

![A screenshot of a computer program Description automatically
generated](./media/image91.png)

24. 運行 mvn spring-boot：run 進行測試

![A screenshot of a computer program Description automatically
generated](./media/image92.png)

25. 您可以要求助手幫助使用 curl 命令來測試您的功能。

![BrokenImage](./media/image93.png)

26. 單擊**Split terminal** 並運行 curl
    命令來測試您的應用程序。（更新端口）

![BrokenImage](./media/image94.png)

27. 使用 **colors.json** 文件中列出的顏色進行測試

![A screenshot of a computer program Description automatically
generated](./media/image95.png)

28. 測試**colors.json**中未列出的顏色並查看結果

![A computer screen shot of a program Description automatically
generated](./media/image96.png)

任務 6 ： 笑話創作者

創建一個調用 API https://api.chucknorris.io/jokes/random
並返回笑話的新作。

1.  打開 DemoController.Java 並輸入調用 API
    https://api.chucknorris.io/jokes/random 並返回 joke 的提示詞 //
    new作。按選項卡接受代碼。

![A screenshot of a computer program Description automatically
generated](./media/image97.png)

![A computer screen shot of a program Description automatically
generated](./media/image98.png)

2.  您也可以使用下面的代碼。

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

![A computer screen shot of a program Description automatically
generated](./media/image99.png)

18. 切換到
    **CopilotDemoApplicationTests.java**。要編寫單元測試來測試上述函數，請添加
    // 為調用 API https://api.chucknorris.io/jokes/random
    並返回笑話的新作創建單元測試按 Enter 鍵。按 tab 接受代碼。

![A screenshot of a computer program Description automatically
generated](./media/image100.png)

19. 您也可以在下面添加單元測試，也可以編寫自己的單元測試。

20. @Test

21. void joke() throws Exception{

22. mockMvc.perform(MockMvcRequestBuilders.get("/joke"))

23. .andExpect(MockMvcResultMatchers.status().isOk())

24. // check that content is a string

25. .andExpect(MockMvcResultMatchers.content().string(Matchers.any(String.class)));

}

![A screenshot of a computer program Description automatically
generated](./media/image101.png)

26. 打開 Terminal -\> Gitbahs 並運行以下命令。

cd exercisefiles/springboot/copilot-demo/

mvn test

![A screenshot of a computer program Description automatically
generated](./media/image101.png)

![A screenshot of a computer Description automatically
generated](./media/image102.png)

27. 打包您的應用程序。運行 mvn 包

![A screenshot of a computer program Description automatically
generated](./media/image103.png)

![A screenshot of a computer program Description automatically
generated](./media/image104.png)

28. 運行 mvn spring-boot：run

![A screenshot of a computer program Description automatically
generated](./media/image105.png)

![BrokenImage](./media/image106.png)

29. 單擊拆分終端並運行命令：curl -v http://localhost:8080/joke
    在第二個終端中

![A screenshot of a computer screen Description automatically
generated](./media/image107.png)

任務 7：URL 解析

給定一個 url
作為查詢參數，解析它並返回協議、主機、端口、路徑和查詢參數。響應應採用
Json 格式。

1.  打開 **DemoController.Java** 並輸入提示 //給定一個 url
    作為查詢參數編寫代碼，解析它並返回協議、主機、端口、路徑和查詢參數。響應應採用
    Json 格式。按選項卡接受代碼。

![BrokenImage](./media/image108.png)

2.  您也可以使用以下代碼。

3.  // Given a url as query parameter, parse it and return the protocol,
    host, port, path and query parameters. The response should be in
    Json format.

4.  @GetMapping("/parseurl")

5.  public String parseurl(@RequestParam(name = "url", required = false)
    String url) throws MalformedURLException {

6.  if (url == null || url.isEmpty()) {

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

![A computer screen shot of a program Description automatically
generated](./media/image109.png)

16. 切換到
    **CopilotDemoApplicationTests.java**。要編寫單元測試來測試上述函數，請添加
    // 為調用 API https://api.chucknorris.io/jokes/random
    並返回笑話的新作創建單元測試按 Enter 鍵。按 tab 接受代碼。

![A screenshot of a computer program Description automatically
generated](./media/image110.png)

17. 您還可以添加以下單元測試或編寫自己的單元測試。

18. @Test

19. void parseUrl() throws Exception{

20. mockMvc.perform(MockMvcRequestBuilders.get("/parseurl?url=https://learn.microsoft.com/en-us/azure/aks/concepts-clusters-workloads?source=recommendations"))

21. .andExpect(MockMvcResultMatchers.status().isOk())

22. // validate json fields

23. .andExpect(MockMvcResultMatchers.jsonPath("$.protocol").value("https"))

24. .andExpect(MockMvcResultMatchers.jsonPath("$.host").value("learn.microsoft.com"))

25. .andExpect(MockMvcResultMatchers.jsonPath("$.path").value("/en-us/azure/aks/concepts-clusters-workloads"))

26. .andExpect(MockMvcResultMatchers.jsonPath("$.query").value("source=recommendations"));

27. }

28. @Test

29. void parseUrlNoUrl() throws Exception{

30. mockMvc.perform(MockMvcRequestBuilders.get("/parseurl"))

31. .andExpect(MockMvcResultMatchers.status().isOk())

32. .andExpect(MockMvcResultMatchers.content().string("url not
    passed"));

}

![A screenshot of a computer program Description automatically
generated](./media/image111.png)

33. 打開 **Terminal -\> Gitbash** 並運行以下命令。 

cd exercisefiles/springboot/copilot-demo/

mvn test

![A screenshot of a computer program Description automatically
generated](./media/image112.png)

![A screenshot of a computer program Description automatically
generated](./media/image113.png)

34. 運行 mvn package 打包您的應用程序。

![A screenshot of a computer program Description automatically
generated](./media/image114.png)

35. 運行 mvn spring-boot：run

![A screenshot of a computer program Description automatically
generated](./media/image115.png)

![BrokenImage](./media/image116.png)

36. 拆分終端並測試您的應用程序：curl -v
    http://localhost:8080/parseurl?url=https://www.google.com/search?q=chuck+norris

![A screenshot of a computer screen Description automatically
generated](./media/image117.png)

任務 8 ： 字數統計

給定文件的路徑並計算所提供單詞的出現次數。路徑和單詞應該是查詢參數。響應應採用
Json 格式。

1.  打開 **DemoController.Java** 並輸入提示
    //給定文件路徑的代碼並計算所提供單詞的出現次數。路徑和單詞應該是查詢參數。響應應採用
    Json 格式。按選項卡接受代碼。

![BrokenImage](./media/image118.png)

2.  切換到
    **CopilotDemoApplicationTests.java**。要編寫單元測試來測試上述函數，請添加
    //
    給定文件的路徑並計算所提供單詞的出現次數。路徑和單詞應該是查詢參數。響應應採用
    Json 格式。按 Enter 鍵。按 選項卡接受代碼。

![BrokenImage](./media/image119.png)

3.  打開 **Terminal -\> Gitbash**並運行以下命令。

cd exercisefiles/springboot/copilot-demo/

mvn test

![BrokenImage](./media/image120.png)

![BrokenImage](./media/image121.png)

4.  運行 mvn package 打包您的應用程序/

![BrokenImage](./media/image122.png)

5.  運行 mvn spring-boot：run

![BrokenImage](./media/image123.png)

6.  單擊拆分終端並運行 curl 命令來測試您的應用程序。

curl http://localhost:8080/countword?path=src/test/resources/test.txt

![BrokenImage](./media/image124.png)

任務 9：容器化應用程序

使用提供的 Dockerfile 創建應用程序的 Docker 映像。Dockerfile
中有一些注釋可以幫助您完成練習。

為了生成、運行和測試 docker 映像，您也可以使用 Copilot 生成命令。

例如，創建一個 DOCKER.md 文件，您可以在其中存儲用於構建、運行和測試
docker 映像的命令。您會注意到 Copilot 還將幫助您記錄您的項目和命令。

要記錄的步驟示例：生成容器映像、運行容器、測試容器。

1.  雙擊 Dekstop 中的 Docker 並使用您的帳戶登錄。

2.  打開 Docker 文件 om Visual Studio
    代碼，向其中添加以下代碼並保存文件。

3.  \# 基於openjdk 17構建java應用鏡像，在8080端口上運行

4.  FROM openjdk:17-jdk-alpine

5.  EXPOSE 8080

6.  COPY target/\*.jar app.jar

ENTRYPOINT \["java","-jar","/app.jar"\]

![BrokenImage](./media/image125.png)

7.  按 **Ctrl +Alt +I** 打開 **GitHub Copilot** 聊天窗口。詢問 Copilot
    以下提示。Copilot 提供了容器化應用程序的步驟。

如何使用提供的 Dockerfile 構建、運行和測試 docker 映像，以創建應用程序的
docker 映像

![BrokenImage](./media/image126.png)

8.  按照第一步 - 構建 Docker 鏡像。打開 \*\*Terminal -\> Gitbash\*\*
    並運行命令來構建 Docker 鏡像。

cd exercisefiles/springboot/copilot-demo/

docker build -t my-application .

![BrokenImage](./media/image127.png)

![BrokenImage](./media/image128.png)

![A screenshot of a computer Description automatically
generated](./media/image129.png)

9.  構建鏡像後，您可以使用 docker run 命令運行它。

docker run -p 8080:8080 my-application

![A screenshot of a computer program Description automatically
generated](./media/image130.png)

10. Docker 容器運行後，您可以通過向應用程序發送請求來對其進行測試。

curl \<http://localhost:8080/hello?key=world

![BrokenImage](./media/image131.png)

