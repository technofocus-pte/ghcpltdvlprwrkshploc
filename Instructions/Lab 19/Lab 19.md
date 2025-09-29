**ラボ 19 - GitHub CopilotGoal の助けを借りて Quarkus を使用して REST
API を構築する**

このラボの目的は、https://quarkus.io/ を使用して REST API
を構築するタスクを使用して、GitHub Copilot
の使用方法を学習することです。

いくつかのファイルがすでに作成されたQuarkusプロジェクトを作成しましたが、プロジェクトは**exercisefiles/quarkus**フォルダにあります。

コパイロットを始めましょう!!

**タスク1 - 単純なGETリクエストを処理するコードを作成する**

「DemoResource.java」ファイルに移動し、単純な GET
リクエストを処理するコードの記述を開始します。

1.  この最初のステップでは、生成する必要があるコードを説明するコメントを提供しました。Enter
    キーを押して数秒待ちます。

![壊れた画像](./media/image1.png)

2.  Copilot がコードを生成します。コードに満足できない場合は、Ctrl +
    Enterを押すと、複数のコードオプションが提案されます。

![コンピューターのスクリーンショット説明が自動的に生成されます](./media/image2.png)

3.  生成されたコードに満足できない場合は、もう一度 Enter
    キーを押すと、Copilot が新しいコードを生成します

![コンピューターのスクリーンショット説明が自動的に生成されます](./media/image3.png)

![コンピュータプログラムのスクリーンショット説明が自動的に生成されます](./media/image4.png)

![コンピュータプログラムのスクリーンショット説明が自動的に生成されます](./media/image5.png)

4.  **test/java/com/Microsoft/hackthon/quarkus/**に移動し、**DemoResourceTest.java**をクリックします。このタスクには既に単体テストが実装されています。

![コンピューターのスクリーンショット説明が自動的に生成されます](./media/image6.png)

5.  「**Terminal -\> New Terminal**」をクリックします。

![壊れた画像](./media/image7.png)

6.  **「Gitbash」**を選択します。

![壊れた画像](./media/image8.png)

7.  cd exercisefiles/quarkus/copilot-demo/ コマンドを実行します。

![コンピュータプログラムのスクリーンショット説明が自動生成される](./media/image9.png)

8.  コマンド mvn test 前後を使用して実行し、Copilot
    によって生成されたコードが正しいことを検証できます。

![コンピュータプログラムのスクリーンショット説明が自動的に生成されます](./media/image10.png)

![コンピューターのスクリーンショット説明が自動的に生成されます](./media/image11.png)

![コンピュータプログラムのスクリーンショット説明が自動的に生成されます](./media/image12.png)

9.  すべてのタスクの後、アプリケーションをパッケージ化して実行し、テストしてください。

Package: mvn package
![コンピュータプログラムのスクリーンショット説明が自動的に生成されます](./media/image13.png)

![コンピュータプログラムのスクリーンショット説明が自動的に生成されます](./media/image14.png)

10. 実行: mvn quarkus:dev

![コンピュータプログラムのスクリーンショット説明が自動的に生成されます](./media/image15.png)

![コンピュータプログラムのスクリーンショット説明が自動的に生成されます](./media/image16.png)

11. 「ターミナルの分割」をクリックし、2番目のターミナルにコマンドを入力して実行します

curl -v http://localhost:8080/hello?key=world

curl <http://localhost:8080/hello>

curl <http://localhost:8080/hello?key=world>

![コンピューター画面のスクリーンショット説明が自動的に生成されます](./media/image17.png)

![壊れた画像](./media/image18.png)

**タスク 2 : 日付の比較**

2 つの日付の差を計算する /diffdates の下の新しい操作。操作は、dd-MM-yyyy
形式のパラメーターとして 2
つの日付を受け取り、日数単位の差を返す必要があります。

1.  次のコメントを入力します // 2 つの日付の差を計算する // /diffdates
    の新しい操作。操作は、dd-MM-yyyy 形式のパラメーターとして 2
    つの日付を受け取り、日数単位の差を返す必要があります。をクリックし、Enter
    キーを押します。

**注:** コメントは**DemoResource.java**ファイルにあります。
**C:\CopiolHackathon\exercisefiles\\ quarkus\\ copilot-demo\src\main\\
java\com\microsoft\hackathon\quarkus\DemoResource.java**

![コンピュータプログラムのスクリーンショット説明が自動生成される](./media/image19.png)

2.  Tab キーを押し、もう一度 Tab キーを押してコードを受け入れます。

![コンピュータプログラムのスクリーンショット説明が自動生成される](./media/image20.png)

3.  ファイルDemoResourceTest.java開き、操作を検証する単体テストを作成します。追加
    //2 つの日付の差を計算する /diffdates
    を検証する単体テストを作成し、Enter キーを押します。

![コンピュータプログラムのスクリーンショット説明が自動的に生成されます](./media/image21.png)

4.  Tab
    キーを押してコードを受け入れます。以下のコードを使用することもできます。

5.  パッケージ com.microsoft.hackathon.quarkus;

6.  

7.  jakarta.ws.rs.GETをインポートします。

8.  jakarta.ws.rs.Path をインポートします。

9.  import jakarta.ws.rs.Produces;

10. jakarta.ws.rs.QueryParamをインポートします。

11. jakarta.ws.rs.client.Clientをインポートします。

12. jakarta.ws.rs.client.ClientBuilderをインポートします。

13. jakarta.ws.rs.client.WebTargetをインポートします。

14. jakarta.ws.rs.core.MediaTypeをインポートします。

15. jakarta.ws.rs.core.Responseをインポートします。

16. 

17. java.io.Fileをインポートします。

18. java.io.FileInputStreamをインポートします。

19. java.io.IOExceptionをインポートします。

20. java.io.InputStreamをインポートします。

21. java.net.URLをインポートします。

22. java.nio.file.Filesをインポートします。

23. java.nio.file.Pathsをインポートします。

24. java.text.SimpleDateFormatをインポートします。

25. java.util.ArrayListをインポートします。

26. java.util.Dateをインポートします。

27. java.util.Listをインポートします。

28. java.util.Objectsをインポートします。

29. 

30. com.fasterxml.jackson.databind.JsonNode をインポートします。

31. com.fasterxml.jackson.databind.ObjectMapperをインポートします。

32. com.fasterxml.jackson.databind.node.ObjectNodeをインポートします。

33. 

34. io.quarkus.fs.util.ZipUtilsをインポートします。

35. 

36. 

37. 

38. 

39. 

40. /\*

41. \* デモリソースはルートパスにマッピングする必要があります。

42. \*

43. \* リクエストでクエリパラメータとして渡されたキーの値を返す GET
    操作を作成します。

44. \*

45. ※キーが渡されない場合は、「キーが渡されませんでした」を返します。

46. ※キーが渡された場合は、「hello \<key\>」を返します。

47. \*

48. \*/

49. 

50. @Path("/")

51. パブリッククラス DemoResource {

52. @GET

53. @Path("/こんにちは")

54. @Produces(MediaType.TEXT_PLAIN)

55. public 文字列 hello(@QueryParam("key") 文字列キー) {

56. if (キー== null) {

57. return "キーが渡されませんでした"

58. } そうでなければ {

59. return "こんにちは " + キー;

60. }

61. }

62. 2 つの日付の差を計算する /diffdates
    の下の新しい操作。操作は、dd-MM-yyyy 形式のパラメーターとして 2
    つの日付を受け取り、日数単位の差を返す必要があります。

63. @GET

64. @Path("/diffdates")

65. @Produces(MediaType.TEXT_PLAIN)

66. public String diffdates(@QueryParam("date1") String date1,
    @QueryParam("date2") String date2) {

67. Objects.requireNonNull(date1, "date1はnullであってはなりません");

68. Objects.requireNonNull(date2, "date2はnullであってはなりません");

69. {を試す

70. SimpleDateFormat dateFormat = 新しい SimpleDateFormat("dd-MM-yyyy");

71. 日付 date1Obj = dateFormat.parse(date1);

72. 日付 date2Obj = dateFormat.parse(date2);

73. 長い差分Millis = Math.abs(date1Obj.getTime() - date2Obj.getTime());

74. 長い diffDays = diffMillis / (24 \* 60 \* 60 \* 1000);

75. String.valueOf(diffDays)を返します。

76. } catch (例外 e) {

77. 「無効な日付形式」を返します。

78. }

> }

![コンピュータプログラムのスクリーンショット説明が自動的に生成されます](./media/image22.png)

79. ターミナルを開き、mvn testコマンドを実行します。

![コンピューターのスクリーンショット説明が自動的に生成されます](./media/image23.png)

![コンピュータプログラムのスクリーンショット説明が自動的に生成されます](./media/image24.png)

80. コマンドmvn packageを実行してソリューションをパッケージ化します

![コンピュータプログラムのスクリーンショット説明が自動的に生成されます](./media/image25.png)

![コンピュータプログラムのスクリーンショット説明が自動的に生成されます](./media/image26.png)

81. 実行: mvn quarkus:dev または mvn compile quarkus:dev

![コンピュータプログラムのスクリーンショット説明が自動的に生成されます](./media/image27.png)

82. ターミナルを分割して curl -v http://localhost:8080/diffdates
    を実行します。

**タスク 3 : スペイン語の電話の形式を検証する**

スペインの電話番号の形式(+34プレフィックス、次に9桁、6、7、または9で始まる)を検証します。操作はパラメータとして電話番号を受け取り、形式が正しい場合はtrueを返し、それ以外の場合はfalseを返す必要があります。

1.  入力
    //スペインの電話番号の形式を検証します(+34プレフィックス、次に9桁、6、7、または9から始まります)。操作はパラメータとして電話番号を受け取り、形式が正しい場合はtrueを返し、それ以外の場合はfalseを返してEnterキーを押す必要があります。Tabキーを押して、Coilotの提案コードを受け入れます。

![コンピュータプログラムのスクリーンショット説明が自動生成される](./media/image28.png)

2.  スペイン語の電話番号の形式を検証する // 単体テストを書き込みます
    (+34 プレフィックス、次に 9 桁、6、7、または 9
    から始まります)。操作はパラメーターとして電話番号を受け取り、形式が正しい場合は
    true を返し、それ以外の場合は false を返し、Enter
    キーを押します。Tab
    キーを押して、コパイロットによって提案された単体テストを受け入れます

![コンピュータプログラムのスクリーンショット説明が自動生成される](./media/image29.png)

3.  ターミナルを開き、mvn testを実行します。

![コンピューターのスクリーンショット説明が自動的に生成されます](./media/image30.png)

![コンピュータプログラムのスクリーンショット説明が自動的に生成されます](./media/image31.png)

4.  mvn パッケージを実行します

![コンピュータプログラムのスクリーンショット説明が自動的に生成されます](./media/image32.png)

![コンピュータプログラムのスクリーンショット説明が自動的に生成されます](./media/image33.png)

5.  mvn quarkus:devを実行します。

![コンピューター画面のスクリーンショット説明が自動的に生成されます](./media/image34.png)

6.  「ターミナルの分割」をクリックし、ターミナルの1つで実行します。

curl -v http://localhost:8080/validatephone?phone=+34866666666

curl -v http://localhost:8080/validatephone?phone=+34666666667

curl -v http://localhost:8080/validatephone?phone=+34666666666

![コンピュータプログラムのスクリーンショット説明が自動的に生成されます](./media/image35.png)

**タスク 4 : スペイン語の DNI の形式の検証**

スペイン語のDNI(8桁と1文字)の形式を検証します。操作はパラメータとしてDNIを受け取り、フォーマットが正しい場合はtrueを返し、それ以外の場合はfalseを返す必要があります。

1.  タイプ // スペイン語の DNI の形式 (8 桁と 1 文字)
    を検証します。操作はパラメータとしてDNIを受け取り、フォーマットが正しい場合はtrueを返し、それ以外の場合はfalseを返す必要があります。Enter
    キーを押します。Tab キーを押して、Copilot
    の提案コードを受け入れます。

![コンピュータプログラムのスクリーンショット説明が自動的に生成されます](./media/image36.png)

2.  **CopilotDemoApplicationTests.java**に切り替えます。上記の関数をテストする単体テストを記述するには、スペイン語のDNI(8桁と1文字)の形式を検証するために//単体テストを記述します。操作はパラメータとしてDNIを受け取り、フォーマットが正しい場合はtrueを返し、それ以外の場合はfalseを返す必要があります。Enter
    キーを押します。タブを押してコードを受け入れます。

![コンピュータプログラムのスクリーンショット説明が自動生成される](./media/image37.png)

3.  **ターミナル**を開き、mvn testを実行します

![コンピュータプログラムのスクリーンショット説明が自動的に生成されます](./media/image38.png)

![コンピュータプログラムのスクリーンショット説明が自動的に生成されます](./media/image39.png)

4.  mvn パッケージを実行する

![コンピュータプログラムのスクリーンショット説明が自動的に生成されます](./media/image40.png)

![コンピュータプログラムのスクリーンショット説明が自動的に生成されます](./media/image41.png)

5.  実行: mvn quarkus:dev

![コンピュータプログラムのスクリーンショット説明が自動的に生成されます](./media/image42.png)

6.  テスト: curl -v
    http://localhost:8080/hello/validatedni?dni=12345678A

![コンピュータプログラムのスクリーンショット説明が自動的に生成されます](./media/image43.png)

**タスク 5: 色名から 16 進数コードへ**

リソースの下の既存のcolors.jsonファイルに基づいて、パスパラメータとして色の名前を指定して、16進数コードを返します。色が見つからない場合は、404
を返します

ヒント: TDD を使用します。まず単体テストを作成し、コードを実装します。

1.  タイプ //
    リソースの下の既存のcolors.jsonファイルに基づいて、パスパラメータとして色の名前を指定して、16進数コードを返します。色が見つからない場合は、404
    を返します。Enter キーを押します。Tab キーを押して、Copilot
    の提案コードを受け入れます。

![コンピュータプログラムのスクリーンショット説明が自動的に生成されます](./media/image44.png)

2.  **CopilotDemoApplicationTests.java.**に切り替えます。上記の関数をテストする単体テストを記述するには、
    //Write unit test を resources
    の下にある既存のcolors.jsonファイルに基づいて、path
    パラメータとして色の名前を指定して、16
    進数コードを返します。色が見つからない場合は、404 を返します。Enter
    キーを押します。タブを押してコードを受け入れます。

![コンピュータプログラムのスクリーンショット説明が自動的に生成されます](./media/image45.png)

3.  mvn テストを実行する

![コンピュータプログラムのスクリーンショット説明が自動的に生成されます](./media/image46.png)

![コンピュータプログラムのスクリーンショット説明が自動的に生成されます](./media/image47.png)

4.  mvn パッケージを実行する

![コンピューターのスクリーンショット説明が自動的に生成されます](./media/image48.png)

5.  実行: mvn quarkus:dev

![コンピュータプログラムのスクリーンショット説明が自動的に生成されます](./media/image49.png)

6.  テスト: curl -v http://localhost:8080/hello/color?color=red

![壊れた画像](./media/image50.png)

**タスク6 : ジョーク作成者**

API https://api.chucknorris.io/jokes/random
を呼び出してジョークを返す新しい操作を作成します。

1.  入力 // API https://api.chucknorris.io/jokes/random
    を呼び出してジョークを返す新しい操作を作成します。Enter
    キーを押します。Tab キーを押して、Copilot
    の提案コードを受け入れます。

![コンピュータプログラムのスクリーンショット説明が自動的に生成されます](./media/image51.png)

2.  Tab キーを押してコードを受け入れます

![コンピュータプログラムのスクリーンショット説明が自動生成される](./media/image52.png)

3.  **CopilotDemoApplicationTests.java**.に切り替えます。上記の関数をテストする単体テストを作成するには、API
    「\<u\>https://api.chucknorris.io/jokes/random\</u\>」(https://api.chucknorris.io/jokes/random)
    を呼び出してジョークを返す新しい操作を作成します。Enter
    キーを押します。タブを押してコードを受け入れます。

![コンピュータプログラムのスクリーンショット説明が自動的に生成されます](./media/image53.png)

4.  Tab キーを押してコードを受け入れます。

![コンピュータプログラムのスクリーンショット説明が自動的に生成されます](./media/image54.png)

5.  Terminal -\> New Terminal -\>
    Gitbashをクリックし、以下のコマンドを実行します

cd exercisefiles/quarkus/copilot-demo/

mvn test

![コンピュータプログラムのスクリーンショット説明が自動的に生成されます](./media/image55.png)

![コンピュータプログラムのスクリーンショット説明が自動的に生成されます](./media/image56.png)

6.  mvn packageを実行して、アプリケーションをパッケージ化します。

![コンピュータプログラムのスクリーンショット説明が自動的に生成されます](./media/image57.png)

![コンピュータプログラムのスクリーンショット説明が自動的に生成されます](./media/image58.png)

7.  実行: mvn quarkus:dev

![コンピュータプログラムのスクリーンショット説明が自動的に生成されます](./media/image59.png)

8.  テスト: curl -v http://localhost:8080/hello/joke

![コンピュータプログラムのスクリーンショット説明が自動的に生成されます](./media/image60.png)

**タスク7 : URL解析**

クエリパラメータとして url
を指定すると、それを解析し、プロトコル、ホスト、ポート、パス、およびクエリパラメータを返します。応答は
Json 形式である必要があります。

1.  //クエリパラメータとしてURLを指定し、それを解析し、プロトコル、ホスト、ポート、パス、クエリパラメータを返します。応答は
    Json 形式である必要があります。Enter キーを押します。Tab
    キーを押して、Copilot の提案コードを受け入れます。

![コンピュータプログラムのスクリーンショット説明が自動生成される](./media/image61.png)

![コンピュータプログラムのスクリーンショット説明が自動生成される](./media/image62.png)

2.  **CopilotDemoApplicationTests.java**に切り替えます。上記の関数をテストするための単体テストを作成するには、
    //Write unit test for Given a url as query parameter
    を追加し、それを解析して、protocol、host、port、path、およびqueryパラメータを返します。応答は
    Json 形式である必要があります。Enter
    キーを押します。タブを押してコードを受け入れます。

![コンピュータプログラムのスクリーンショット説明が自動的に生成されます](./media/image63.png)

3.  mvn テストを実行します

![コンピュータプログラムのスクリーンショット説明が自動的に生成されます](./media/image64.png)

![コンピューターのスクリーンショット説明が自動的に生成されます](./media/image65.png)

4.  mvn package を実行して、アプリケーションをパッケージ化します。

![コンピュータプログラムのスクリーンショット説明が自動的に生成されます](./media/image66.png)

5.  mvn quarkus:dev を実行します。

![コンピュータプログラムのスクリーンショット説明が自動的に生成されます](./media/image67.png)

6.  split terminalをクリックし、curl -v
    http://localhost:8080/hello/parseurl?url=https://www.google.com/search?q=quarkus
    を実行します。

![コンピュータプログラムのスクリーンショット説明が自動的に生成されます](./media/image68.png)

**タスク 9 : 単語数カウント**

ファイルのパスが与えられ、指定された単語の出現回数をカウントします。パスと単語はクエリ
パラメーターである必要があります。応答は Json 形式である必要があります。

1.  //ファイルのパスを指定して入力し、指定された単語の出現回数をカウントします。パスと単語はクエリ
    パラメーターである必要があります。応答は Json
    形式である必要があります。Enter キーを押します。Tab
    キーを押して、Copilot の提案コードを受け入れます。

![コンピュータプログラムのスクリーンショット説明が自動的に生成されます](./media/image69.png)

2.  **CopilotDemoApplicationTests.java**に切り替えます。上記の関数をテストするための単体テストを記述するには、
    //Write unit test を Given the path of a file
    に追加し、指定された単語の出現回数をカウントします。パスと単語はクエリ
    パラメーターである必要があります。応答は Json
    形式である必要があります。Enter
    キーを押します。タブを押してコードを受け入れます。

![コンピュータプログラムのスクリーンショット説明が自動的に生成されます](./media/image70.png)

3.  **ターミナル**を開き 、mvn testを実行します

![コンピュータプログラムのスクリーンショット説明が自動的に生成されます](./media/image71.png)

![コンピュータプログラムのスクリーンショット説明が自動的に生成されます](./media/image72.png)

4.  mvn package を実行して、アプリケーションをパッケージ化します。

![コンピュータプログラムのスクリーンショット説明が自動的に生成されます](./media/image73.png)

![コンピュータプログラムのスクリーンショット説明が自動的に生成されます](./media/image74.png)

5.  実行: mvn quarkus:dev

![コンピュータプログラムのスクリーンショット説明が自動的に生成されます](./media/image75.png)

6.  テスト:カール\<http://localhost:8080/hello/countword?path=/tmp/test.txt&word=hello

GitHub copilot にプロジェクトの curl コマンドを依頼できます。

![コンピュータプログラムのスクリーンショット説明が自動的に生成されます](./media/image76.png)

**タスク10 : アプリケーションのコンテナ化**

提供されている Dockerfile を使用して、アプリケーションの Docker
イメージを作成します。この場合、完全なコンテンツが提供されますが、Docker
イメージをビルド、実行、テストするには、Copilot
を使用してコマンドも生成します。

アプリケーション(ネイティブ)のビルド、コンテナイメージのビルド、コンテナの実行、コンテナのテストの手順を文書化する
DOCKER.md ファイルを作成しました。

1.  Visual Studio Code で、**Ctrl + Shit + X** を押して **Docker**
    を検索してインストールします。

![コンピューターのスクリーンショット説明が自動的に生成されます](./media/image77.png)

2.  **Desktop Docker**ダブルクリックし、Dockerアカウントで歌います。

![壊れた画像](./media/image78.png)

3.  **Ctrl + Alt + I** を押して、**Github Copilot
    chat**を開きます。コンテナー
    イメージをビルドし、コンテナーを実行し、提供された
    Dockerfileを使用してコンテナーをテストする方法を Copilot に尋ねます

![コンピュータプログラムのスクリーンショット説明が自動的に生成されます](./media/image79.png)

4.  Copilot
    の指示に従います。アプリケーションを構築します。ターミナルで次のコマンドを実行します。

> ./mvnw package -Pnative -Dquarkus.native.container-build=true

![コンピューターのスクリーンショット説明が自動的に生成されます](./media/image77.png)

![コンピュータプログラムのスクリーンショット説明が自動的に生成されます](./media/image80.png)

![コンピュータプログラムのスクリーンショット説明が自動的に生成されます](./media/image81.png)

![コンピュータプログラムのスクリーンショット説明が自動的に生成されます](./media/image82.png)

![コンピュータプログラムのスクリーンショット説明が自動的に生成されます](./media/image83.png)

5.  **Docker イメージをビルドする:** Dockerfile の名前が
    **Dockerfile.native-micro**であると仮定すると、次のコマンドを使用できます。

> docker build -f Dockerfile.native-micro -t my-app

![プログラムのコンピューターのスクリーンショット説明が自動的に生成される](./media/image84.png)

6.  このコマンドは、現在のディレクトリ (コマンドの末尾にある '.') にある
    'Dockerfile.native-micro' という名前の Dockerfile
    を使用してイメージをビルドし、結果のイメージに 'my-app'
    という名前を付けるようにDocker に指示します。

7.  Docker イメージを実行する: イメージがビルドされたら、'docker run'
    コマンドを使用して実行できます:

docker run -p 8080:8080 my-app

![壊れた画像](./media/image85.png)

このコマンドは、'my-app'
イメージからコンテナーを実行し、コンテナー内のポート 8080 をホスト
マシンのポート 8080 にマップするように Docker に指示します。

1.  **アプリケーションをテストする**:
    最後に、アプリケーションが正しく実行されているかどうかをテストするには、ブラウザーでリクエストを送信するか、curl
    などのツールを使用して http://localhost:8080 に送信します:

> curl http://localhost:8080

![コンピュータプログラムのスクリーンショット説明が自動的に生成されます](./media/image86.png)

このコマンドは、GET
要求をアプリケーションに送信し、応答を出力します。アプリケーションが正しく実行されている場合は、予期される応答が表示されます。

これらのコマンドは、Javaアプリケーションコード内ではなく、ターミナルで実行する必要があることに注意してください。
