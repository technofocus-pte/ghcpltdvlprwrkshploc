**실습 19 - GitHub Copilot을 통해 Quarkus를 사용하여 REST API를
빌드하기**

**목표**

이 랩의 목표는 https://quarkus.io/ 를 사용하여 REST API를 빌드하는
작업을 사용하여 GitHub Copilot을 사용하는 방법을 알아보는 것입니다.

일부 파일이 이미 생성된 Quarkus 프로젝트를 생성했으므로
**exercisefiles/quarkus** 폴더에서 프로젝트를 찾을 수 있습니다.

Copiloting 시작해 보겠습니다!!!

**작업 1 - 간단한 GET 요청을 처리하는 코드 생성하기**

'DemoResource.java' 파일로 이동하여 간단한 GET 요청을 처리하는 코드
작성을 시작하세요.

1.  이 첫 번째 단계에서는 생성해야 하는 코드를 설명하는 주석을
    제공했습니다. Enter 키를 누르고 몇 초만 기다리세요.

![](./media/image1.png)

2.  Copilot이 코드를 생성합니다. 코드가 마음에 들지 않으면 Ctrl +
    Enter를 누르면 여러 코드 옵션이 제안됩니다.

![](./media/image2.png)

3.  생성된 코드가 마음에 들지 않으면 Enter 키를 다시 누르면 Copilot이 새
    코드를 생성합니다

![](./media/image3.png)

![](./media/image4.png)

![](./media/image5.png)

4.  **test/java/com/Microsoft/hackthon/quarkus/**로 이동하고 
    **DemoResourceTest.java**를 클릭하세요. 이 작업에 대해 구현된 단위
    테스트가 이미 있습니다.

![](./media/image6.png)

5.  **Terminal -\> New Terminal**을 클릭하세요.

![](./media/image7.png)

6.  **Gitbash**를 선택하세요.

![](./media/image8.png)

7.  cd exercisefiles/quarkus/copilot-demo/ 명령을 실행하세요.

![](./media/image9.png)

8.  Copilot에서 생성된 코드가 올바른지 확인하기 위해 mvn test 전후에
    명령을 사용하여 실행할 수 있습니다.

![](./media/image10.png)

![](./media/image11.png)

![](./media/image12.png)

9.  모든 작업이 끝나면 애플리케이션을 자유롭게 패키징하고 실행하여
    테스트하세요.

Package: mvn package

![](./media/image13.png)

![](./media/image14.png)

10. mvn quarkus:dev을 실행하세요

![](./media/image15.png)

![](./media/image16.png)

11. 터미널 분할을 클릭하고 2nd터미널에 명령을 입력하고 실행하세요

curl -v http://localhost:8080/hello?key=world

curl http://localhost:8080/hello

curl http://localhost:8080/hello?key=world

![](./media/image17.png)

![](./media/image18.png)

**작업 2: 날짜 비교**

두 날짜 간의 차이를 계산하는 /diffdates 아래의 새 작업입니다. 작업은
dd-MM-yyyy 형식의 매개 변수로 두 개의 날짜를 수신하고 차이를 일 단위로
반환해야 합니다.

1.  다음 주석을 입력하세요 // /diffdates 아래에 두 날짜 간의 차이를
    계산하는 새 작업. 작업은 dd-MM-yyyy 형식의 매개 변수로 두 개의
    날짜를 수신하고 일 단위의 차이를 반환하고 Enter 키를 누르세요.

**참고:** 멘트는**DemoResource.java** 파일에
있습니다. **C:\CopiolHackathon\exercisefiles\\ quarkus\\
copilot-demo\src\main\\
java\com\microsoft\hackathon\quarkus\DemoResource.java**

![](./media/image19.png)

2.  Tab 키를 누른 후 다시 Tab 키를 눌러 코드를 수락하세요.

![](./media/image20.png)

3.  DemoResourceTest.java 파일을 열고 작업의 유효성을 검사하는 단위
    테스트를 생성하세요. 추가 //단위 테스트를 만들어 유효성을
    검사하세요/diffdates 두 날짜 간의 차이를 계산한 다음 Enter 키를
    누르세요.

![](./media/image21.png)

4.  Tab 키를 눌러 코드를 수락하세요. 아래 코드를 사용할 수도 있습니다.

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

![](./media/image22.png)

79. Terminal을 열고 mvn 테스트 명령을 실행하세요.

![](./media/image23.png)

![](./media/image24.png)

80. mvn package 명령을 실행하여 솔루션을 패키징하세요.

![](./media/image25.png)

![](./media/image26.png)

81. mvn quarkus:dev or mvn compile quarkus:dev를 실행하세요

![](./media/image27.png)

82. 터미널을 분할하고 curl -v http://localhost:8080/diffdates 실행하세요

**작업 3: 스페인어 전화의 형식 확인하기**

스페인어 전화번호의 형식 (+34 접두사, 9자리, 6, 7 또는 9로 시작)의
유효성을 검사하세요. 작업은 전화 번호를 매개 변수로 수신하고 형식이
올바르면 true를 반환하고 그렇지 않으면 false를 반환해야 합니다.

1.  //Validate the format of a spanish phone number (+34 prefix, then 9
    digits, starting with 6, 7 or 9)를 입력하세요. 작업은 전화 번호를
    매개변수로 수신하고 형식이 올바르면 true를 반환하고 그렇지 않으면
    false를 반환하고 Enter 키를 누르세요. Tab 키를 눌러 Coilot 제안
    코드를 수락하세요.

![](./media/image28.png)

2.  // write unit test to Validate the format of a spanish phone number
    (+34 prefix, then 9 digits, starting with 6, 7 or 9)를 입력하세요.
    작업은 전화 번호를 매개 변수로 수신하고 형식이 올바르면 true를
    반환하고 그렇지 않으면 false를 반환하고 Enter 키를 누르세요. Tab
    키를 눌러 Copilot에서 제안한 단위 테스트를 수락하세요.

![](./media/image29.png)

3.  터미널을 열고 mvn test를 실행하세요.

![](./media/image30.png)

![](./media/image31.png)

4.  mvn 패키지를 실행하세요

![](./media/image32.png)

![](./media/image33.png)

5.  mvn quarkus:dev를 실행하세요

![](./media/image34.png)

6.  터미널 분할을 클릭하고 터미널 중 하나에서 실행하세요 -

curl -v http://localhost:8080/validatephone?phone=+34866666666

curl -v http://localhost:8080/validatephone?phone=+34666666667

curl -v http://localhost:8080/validatephone?phone=+34666666666

![](./media/image35.png)

**작업 4 : 스페인어 DNI의 형식 유효성 검사**

스페인어 DNI(8자리 1자)의 형식을 확인하세요. 작업은 DNI를 매개 변수로
수신하고 형식이 올바르면 true를 반환하고 그렇지 않으면 false를 반환해야
합니다.

1.  // Validate the format of a spanish DNI (8 digits and 1 letter)를
    입력하세요. 작업은 DNI를 매개 변수로 수신하고 형식이 올바른 경우
    true를 반환하고 그렇지 않으면 false를 반환해야 합니다. Enter 키를
    누르세요. Tab 키를 눌러 Copilot 제안 코드를 수락하세요.

![](./media/image36.png)

2.  **CopilotDemoApplicationTests.java**로 전환하세요. 위의 함수를
    테스트하기 위한 단위 테스트를 작성하려면, //Write unit test to
    Validate the format of a spanish DNI (8 digits and 1 letter)를
    추가하세요. 작업은 DNI를 매개 변수로 수신하고 형식이 올바른 경우
    true를 반환하고 그렇지 않으면 false를 반환해야 합니다. Enter 키를
    누르세요. 탭을 눌러 코드를 수락하세요.

![](./media/image37.png)

3.  터미널을 열고 mvn test 실행하세요

![](./media/image38.png)

![](./media/image39.png)

4.  mvn 패키지를 실행하세요

![](./media/image40.png)

![](./media/image41.png)

5.  mvn quarkus:dev를 실행하세요

![](./media/image42.png)

6.  Test: curl -v
    <http://localhost:8080/hello/validatedni?dni=12345678A>

![](./media/image43.png)

**작업 5: 색상 이름에서 16진수 코드까지**

리소스 아래의 기존 colors.json 파일을 기반으로 경로 매개 변수로 색상의
이름이 주어지면 16진수 코드를 반환하세요. 색상을 찾을 수 없으면 404를
반환하세요.

힌트: TDD를 사용하세요. 단위 테스트를 생성한 후 코드를 구현하여
시작하세요.

1.  // Based on the existing colors.json file under resources, given the
    name of the color as path parameter, return the hexadecimal code를
    입력하세요. 색상을 찾을 수 없으면 404를 반환하세요. Enter 키를
    누르세요. Tab 키를 눌러 Copilot 제안 코드를 수락하세요.

![](./media/image44.png)

2.  **CopilotDemoApplicationTests.java**로 전환하새요. 위의 함수를
    테스트하기 위한 단위 테스트를 작성하려면, //Write unit test to Based
    on the existing colors.json file under resources, given the name of
    the color as path parameter, return the hexadecimal code를
    추가하세요. 색상을 찾을 수 없으면 404를 반환하세요. Enter 키를
    누르세요. 탭을 눌러 코드를 수락하세요.

![](./media/image45.png)

3.  mvn test를 실행하세요

![](./media/image46.png)

![](./media/image47.png)

4.  mvn package를 실행하세요

![](./media/image48.png)

5.  mvn quarkus:dev를 실행하세요

![](./media/image49.png)

6.  Test: curl -v http://localhost:8080/hello/color?color=red

![](./media/image50.png)

**작업 6 : Jokes creator**

API https://api.chucknorris.io/jokes/random 를 호출하고 농담을 반환하는
새 작업을 생성하세요.

1.  // Create a new operation that call the API
    https://api.chucknorris.io/jokes/random and return the joke를
    입력하세요. Enter를 입력하세요. Tab 키를 눌러 Copilot 제안 코드를
    수락하세요.

![](./media/image51.png)

2.  Tab 키를 눌러 코드를 수락하세요.

![](./media/image52.png)

3.  **CopilotDemoApplicationTests.java**로 전환하세요. 위의 함수를
    테스트하기 위한 단위 테스트를 작성하려면, add //Create a new
    operation that call the API
    \[\<u\>[https://api.chucknorris.io/jokes/random\</u\>\](https://api.chucknorris.io/jokes/random)](https://api.chucknorris.io/jokes/random%3c/u%3e%5d(https://api.chucknorris.io/jokes/random))를
    추가하고 농담을 돌려주세요. Enter를 입력하세요. 탭을 눌러 코드를
    수락하세요.

![](./media/image53.png)

4.  Tab 키를 눌러 코드를 수락하세요.

![](./media/image54.png)

5.  Terminal -\> New Terminal -\> Gitbash를 클릭하고 다음 명령을
    실행하세요

cd exercisefiles/quarkus/copilot-demo/

mvn test

![](./media/image55.png)

![](./media/image56.png)

6.  mvn 패키지를 실행하여 애플리케이션 패키징하세요.

![](./media/image57.png)

![](./media/image58.png)

7.  mvn quarkus:dev를 실행하세요

![](./media/image59.png)

8.  Test: curl -v http://localhost:8080/hello/joke

![](./media/image60.png)

**작업 7 : URL parsing**

쿼리 매개 변수로 URL이 주어지면 구문 분석하고 프로토콜, 호스트, 포트,
경로 및 쿼리 매개 변수를 반환합니다. 응답은 Json 형식이어야 합니다.

1.  //Given a url as query parameter, parse it and return the protocol,
    host, port, path and query parameters를 입력하세요. 응답은 Json
    형식이어야 합니다. Enter 키를 누르세요. Tab 키를 눌러 Copilot 제안
    코드를 수락하세요.

![](./media/image61.png)

![](./media/image62.png)

2.  **CopilotDemoApplicationTests.java**로 전환합니다. 위의 함수를
    테스트하기 위한 단위 테스트를 작성하려면, //Write unit test for
    Given a url as query parameter, parse it and return the protocol,
    host, port, path and query parameters를 추가하세요. 응답은 Json
    형식이어야 합니다. Enter 키를 누르세요. 탭을 눌러 코드를 수락하세요.

![](./media/image63.png)

3.  mvn test를 실행하세요

![](./media/image64.png)

![](./media/image65.png)

4.  mvn 패키지를 실행하여 애플리케이션 패키징하세요.

![](./media/image66.png)

5.  mvn quarkus:dev를 실행하세요

![](./media/image67.png)

6.  split 터미널을 클릭하고 curl -v
    http://localhost:8080/hello/parseurl?url=https://www.google.com/search?q=quarkus
    실행하세요.

![](./media/image68.png)

**작업 9: 단어 계산**

파일의 경로가 주어지고 제공된 단어의 발생 횟수를 계산합니다. 경로와
단어는 쿼리 매개 변수여야 합니다. 응답은 Json 형식이어야 합니다.

1.  //Given the path of a file and count the number of occurrence of a
    provided word를 입력하세요. 경로와 단어는 쿼리 매개 변수여야 합니다.
    응답은 Json 형식이어야 합니다. Enter 키를 누르세요. Tab 키를 눌러
    Copilot 제안 코드를 수락하세요.

![](./media/image69.png)

2.  CopilotDemoApplicationTests.java로 전환합니다. 위의 함수를
    테스트하기 위한 단위 테스트를 작성하려면, //Write unit test to Given
    the path of a file and count the number of occurrence of a provided
    word를 추가하세요. 경로와 단어는 쿼리 매개 변수여야 합니다. 응답은
    Json 형식이어야 합니다. Enter 키를 누르세요. 탭을 눌러 코드를
    수락하세요.

![](./media/image70.png)

3.  **Terminal**을 열고 mvn test를 실행하세요

![](./media/image71.png)

![](./media/image72.png)

4.  mvn 패키지를 실행하여 애플리케이션 패키징하세요.

![](./media/image73.png)

![](./media/image74.png)

5.  mvn quarkus:dev를 실행하세요

![](./media/image75.png)

6.  Test: curl \<http://localhost:8080/hello/countword?path=/tmp/test.txt&word=hello

프로젝트에 대한 curl 명령에 대해 GitHub copilot에 요청할 수 있습니다.

![](./media/image76.png)

**작업10 : 애플리케이션 컨테이너화**

제공된 Dockerfile을 사용하여 애플리케이션의 Docker 이미지를 생성합니다.
이 경우 전체 콘텐츠가 제공되지만 Docker 이미지를 빌드, 실행 및
테스트하려면 Copilot도 사용하여 명령을 생성합니다.

응용 프로그램 (네이티브)을 빌드하고, 컨테이너 이미지를 빌드하고,
컨테이너를 실행하고, 컨테이너를 테스트하는 단계를 문서화하는 DOCKER.md
파일을 생성했습니다.

1.  Visual Studio 코드에서 **Ctrl + Shit + X**를 눌러 **Docker**를
    검색하여 설치하세요.

![](./media/image77.png)

2.  **Desktop Docker**를 두 번 클릭하고 Docker 계정으로 로그인하세요.

![](./media/image78.png)

3.  **Ctrl + Alt + I**를 눌러 **Github Copilot chat**을 여세요.
    Copilot에게 컨테이너 이미지를 빌드하고, 컨테이너를 실행하고, 제공된
    Dockerfile을 사용하여 컨테이너를 테스트하는 방법을 물어보세요

![](./media/image79.png)

4.  Copilot의 지시를 따르세요. 애플리케이션을 빌드하세요. 터미널에서
    다음 명령을 실행하세요:

./mvnw package -Pnative -Dquarkus.native.container-build=true

![](./media/image77.png)

![](./media/image80.png)

![](./media/image81.png)

![](./media/image82.png)

![](./media/image83.png)

5.  **Build the Docker image:** Dockerfile의 이름이
    **Dockerfile.native-micro**라고 가정하면 다음 명령을 사용할 수
    있습니다.:

docker build -f Dockerfile.native-micro -t my-app .

![](./media/image84.png)

6.  이 명령은 Docker에 현재 디렉터리(명령 끝에 있는 '.')에 있는
    'Dockerfile.native-micro'라는 Dockerfile을 사용하여 이미지를
    빌드하고 결과 이미지에 'my-app'이라는 이름으로 태그를 지정하도록
    지시하세요.

7.  Run the Docker image: 이미지가 빌드된 후 'docker run' 명령으로
    실행할 수 있습니다.:

docker run -p 8080:8080 my-app

![](./media/image85.png)

이 명령은 Docker에 'my-app' 이미지에서 컨테이너를 실행하고 컨테이너의
포트 8080을 호스트 컴퓨터의 포트 8080에 매핑하도록 지시합니다.

1.  **Test the application**: 마지막으로 애플리케이션이 올바르게
    실행되고 있는지 테스트하기 위해 브라우저에서 또는 curl과 같은 도구를
    사용하여 http://localhost:8080 에 요청을 보낼 수 있습니다:

curl http://localhost:8080

![](./media/image86.png)

이 명령은 애플리케이션에 GET 요청을 보내고 응답을 인쇄합니다.
애플리케이션이 올바르게 실행되고 있으면 예상 응답이 표시되어야 합니다.

이러한 명령은 Java 애플리케이션 코드가 아닌 터미널에서 실행해야 합니다.
