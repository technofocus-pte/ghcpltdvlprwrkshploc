**Lab 19 - Erstellen einer REST-API mit Quarkus mit Hilfe von GitHub
CopilotGoal**

Das Ziel dieses Labs besteht darin, die Verwendung von GitHub Copilot
anhand einer Aufgabe zu erlernen, die darin besteht, eine REST-API
mithilfe von https://quarkus.io/ zu erstellen.

Wir haben ein Quarkus-Projekt erstellt, bei dem bereits einige Dateien
erstellt wurden, Sie finden das Projekt im Ordner
**exercisefiles/quarkus**.

Beginnen wir mit dem Copiloting!!

**Aufgabe 1: Erstellen des Codes zum Verarbeiten einer einfachen
GET-Anforderung**

Wechseln Sie zur Datei "DemoResource.java" und beginnen Sie mit dem
Schreiben des Codes für die Verarbeitung einer einfachen
GET-Anforderung.

1.  In diesem ersten Schritt haben wir einen Kommentar bereitgestellt,
    der den Code beschreibt, den Sie generieren müssen. Drücken Sie
    einfach die Eingabetaste und warten Sie ein paar Sekunden.

![Defektes Bild](./media/image1.png)

2.  Copilot generiert den Code für Sie. Wenn Sie mit dem Code nicht
    zufrieden sind, drücken Sie Ctrl +Enter und es werden mehrere
    Codeoptionen vorgeschlagen.

![Ein Screenshot eines Computers Beschreibung wird automatisch
generiert](./media/image2.png)

3.  . Wenn Sie mit dem generierten Code nicht zufrieden sind, können Sie
    erneut die Eingabetaste drücken und Copilot generiert einen neuen
    Code

![Ein Screenshot eines Computers Beschreibung wird automatisch
generiert](./media/image3.png)

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image4.png)

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image5.png)

4.  Gehen Sie zu **test/java/com/Microsoft/hackthon/quarkus/** und
    klicken Sie auf **DemoResourceTest.java**. Für diese Aufgabe ist
    bereits ein Komponententest implementiert.

![Ein Screenshot eines Computers Beschreibung wird automatisch
generiert](./media/image6.png)

5.  Klicken Sie auf **Terminal -\> New Terminal.**

![Defektes Bild](./media/image7.png)

6.  Wählen Sie **Gitbash** aus.

![Defektes Bild](./media/image8.png)

7.  Führen Sie den Befehl cd exercisefiles/quarkus/copilot-demo/ aus.

![Ein Screenshot eines Computerprogramms Beschreibung automatisch
generiert](./media/image9.png)

8.  Sie können es mit dem Befehl “mvn test” ausführen, um zu prüfen, ob
    der von Copilot generierte Code korrekt ist – sowohl vorher als auch
    nachher.

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image10.png)

![Ein Screenshot eines Computers Beschreibung wird automatisch
generiert](./media/image11.png)

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image12.png)

9.  Nach jeder Aufgabe können Sie Ihre Anwendung verpacken und
    ausführen, um sie zu testen.

Package: mvn package

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image13.png)

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image14.png)

10. Ausführen: mvn quarkus:dev

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image15.png)

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image16.png)

11. Klicken Sie auf “Split terminal” und geben Sie den Befehl in das 2.
    Terminal ein und führen Sie

> curl -v http://localhost:8080/hello?key=world

curl http://localhost:8080/hello

curl http://localhost:8080/hello?key=world

![Ein Screenshot eines Computerbildschirms Beschreibung wird automatisch
generiert](./media/image17.png)

![Defektes Bild](./media/image18.png)

**Aufgabe 2 : Vergleich der Termine**

Neuer Vorgang unter /diffdates, der die Differenz zwischen zwei
Datumsangaben berechnet. Die Operation sollte zwei Datumsangaben als
Parameter im Format dd-MM-yyyy erhalten und die Differenz in Tagen
zurückgeben.

1.  Geben Sie unter /diffdates den folgenden Kommentar // Neuer Vorgang
    ein, der die Differenz zwischen zwei Datumsangaben berechnet. Die
    Operation sollte zwei Datumsangaben als Parameter im Format
    dd-MM-yyyy erhalten und die Differenz in Tagen zurückgeben. und
    drücken Sie die Eingabetaste

**Hinweis:** Der Kommentar befindet sich in der Datei
**DemoResource.java**. **C:\CopiolHackathon\exercisefiles\\ quarkus\\
copilot-demo\src\main\\
java\com\microsoft\hackathon\quarkus\DemoResource.java**

![Ein Screenshot eines Computerprogramms Beschreibung automatisch
generiert](./media/image19.png)

2.  Drücken Sie die Tabulatortaste und erneut die Tabulatortaste, um den
    Code zu übernehmen.

![Ein Screenshot eines Computerprogramms Beschreibung automatisch
generiert](./media/image20.png)

3.  Öffnen Sie DemoResourceTest.java-Datei, und erstellen Sie einen
    Komponententest, der den Vorgang überprüft. Fügen Sie // Create a
    unit test to validate /diffdates that calculates the difference
    between two dates und drücken Sie dann die Eingabe-Taste.

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image21.png)

4.  Drücken Sie die Tabulatortaste, um den Code zu übernehmen. Sie
    können auch den folgenden Code verwenden.

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

}![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image22.png)

79. Öffnen Sie das Terminal und führen Sie den Befehl “mvn test” aus.

![Ein Screenshot eines Computers Beschreibung wird automatisch
generiert](./media/image23.png)

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image24.png)

80. Packen Sie die Lösung, indem Sie den Befehl “mvn package” ausführen

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image25.png)

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image26.png)

81. Führen Sie mvn quarkus:dev oder mvn compile quarkus:dev aus.

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image27.png)

82. Split Terminal und Ausführen von curl -v
    http://localhost:8080/diffdates

**Aufgabe 3: Überprüfen des Formats eines spanischen Telefons**

Überprüfen Sie das Format einer spanischen Telefonnummer (+34 Präfix,
dann 9 Ziffern, beginnend mit 6, 7 oder 9). Der Vorgang sollte eine
Telefonnummer als Parameter erhalten und true zurückgeben, wenn das
Format korrekt ist, andernfalls false.

1.  Geben Sie // Validate the format of a spanish phone number (+34
    prefix, then 9 digits, starting with 6, 7 or 9). Die Operation
    sollte eine Telefonnummer als Parameter erhalten und true
    zurückgeben, wenn das Format korrekt ist, andernfalls false und
    drücken Sie die Eingabetaste. Drücken Sie die Tabulatortaste, um den
    Coilot-Vorschlagscode zu akzeptieren.

![Ein Screenshot eines Computerprogramms Beschreibung automatisch
generiert](./media/image28.png)

2.  Geben Sie // write unit test to Validate the format of a spanish
    phone number (+34 prefix, then 9 digits, starting with 6, 7 or 9).
    Der Vorgang sollte eine Telefonnummer als Parameter erhalten und
    true zurückgeben, wenn das Format korrekt ist, andernfalls false und
    drücken Sie die Eingabetaste. Drücken Sie die Tabulatortaste, um die
    von copilot vorgeschlagenen Komponententests zu akzeptieren

![Ein Screenshot eines Computerprogramms Beschreibung automatisch
generiert](./media/image29.png)

3.  Öffnen Sie das Terminal und führen Sie mvn test aus.

![Ein Screenshot eines Computers Beschreibung wird automatisch
generiert](./media/image30.png)

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image31.png)

4.  Führen Sie “mvn package” aus

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image32.png)

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image33.png)

5.  Führen Sie mvn quarkus:dev aus.

![Ein Screenshot eines Computerbildschirms Beschreibung wird automatisch
generiert](./media/image34.png)

6.  Klicken Sie auf “Split terminal” und führen Sie es in einem der
    Terminals aus -

curl -v http://localhost:8080/validatephone?phone=+34866666666

curl -v http://localhost:8080/validatephone?phone=+34666666667

curl -v http://localhost:8080/validatephone?phone=+34666666666

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image35.png)

**Aufgabe 4: Überprüfen des Formats eines spanischen DNI**

Überprüfen Sie das Format eines spanischen DNI (8 Ziffern und 1
Buchstabe). Der Vorgang sollte einen DNI als Parameter erhalten und true
zurückgeben, wenn das Format korrekt ist, andernfalls false.

1.  Geben Sie // Validate the format of a spanish DNI (8 digits and 1
    letter).Der Vorgang sollte einen DNI als Parameter erhalten und true
    zurückgeben, wenn das Format korrekt ist, andernfalls false. und
    drücken Sie die Eingabetaste. Drücken Sie die Tabulatortaste, um den
    Copilot-Vorschlagscode zu übernehmen.

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image36.png)

2.  Wechseln Sie zu **CopilotDemoApplicationTests.java**. Um einen
    Komponententest zum Testen der obigen Funktion zu schreiben, fügen
    Sie // Write unit test to Validate the format of a spanish DNI (8
    digits and 1 letter). Der Vorgang sollte einen DNI als Parameter
    erhalten und true zurückgeben, wenn das Format korrekt ist,
    andernfalls false. Drücken Sie die Eingabetaste. Drücken Sie die
    Tabulatortaste, um den Code zu übernehmen.

![Ein Screenshot eines Computerprogramms Beschreibung automatisch
generiert](./media/image37.png)

3.  Öffnen Sie das Terminal und führen Sie den mvn test aus

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image38.png)

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image39.png)

4.  Führen Sie mvn package aus

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image40.png)

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image41.png)

5.  Ausführen: mvn quarkus:dev

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image42.png)

6.  Test: curl -v http://localhost:8080/hello/validatedni?dni=12345678A

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image43.png)

**Aufgabe 5: Vom Farbnamen zum Hexadezimalcode**

Basierend auf der vorhandenen colors.json Datei unter Resources wird der
hexadezimale Code zurückgegeben, wenn der Name der Farbe als
Pfadparameter angegeben wird. Wenn die Farbe nicht gefunden wird, geben
Sie 404 zurück

Tipp: Verwenden Sie TDD. Beginnen Sie mit dem Erstellen des
Komponententests, und implementieren Sie dann den Code.

1.  Geben Sie // Based on the existing colors.json file under resources,
    given the name of the color as path parameter, return the
    hexadecimal code. Wenn die Farbe nicht gefunden wird, geben Sie 404
    zurück. und drücken Sie die Eingabetaste. Drücken Sie die
    Tabulatortaste, um den Copilot-Vorschlagscode zu übernehmen.

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image44.png)

2.  Wechseln Sie zu **CopilotDemoApplicationTests.java**. Um einen
    Komponententest zu schreiben, um die obige Funktion zu testen, fügen
    Sie // Write unit test to Based on the existing colors.json file
    under resources, given the name of the color as path parameter,
    return the hexadecimal code. Wenn die Farbe nicht gefunden wird,
    geben Sie 404 zurück. Drücken Sie die Eingabetaste. Drücken Sie die
    Tabulatortaste, um den Code zu übernehmen.

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image45.png)

3.  Führen Sie mvn test aus

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image46.png)

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image47.png)

4.  Führen Sie mvn package aus

![Ein Screenshot eines Computers Beschreibung wird automatisch
generiert](./media/image48.png)

5.  Ausführen: mvn quarkus:dev

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image49.png)

6.  Test: curl -v http://localhost:8080/hello/color?color=red

![Defektes Bild](./media/image50.png)

**Aufgabe 6 : Witze-Ersteller**

Erstellen Sie einen neuen Vorgang, der die
API-https://api.chucknorris.io/jokes/random aufruft und den Witz
zurückgibt.

1.  Geben Sie // Create a new operation that call the API
    https://api.chucknorris.io/jokes/random and return the joke und
    drücken Sie die Eingabetaste. Drücken Sie die Tabulatortaste, um den
    Copilot-Vorschlagscode zu übernehmen.

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image51.png)

2.  Drücken Sie die Tabulatortaste, um den Code zu akzeptieren

![Ein Screenshot eines Computerprogramms Beschreibung automatisch
generiert](./media/image52.png)

3.  Wechseln Sie zu **CopilotDemoApplicationTests.java**. Um einen
    Komponententest zum Testen der obigen Funktion zu schreiben, fügen
    Sie // Create a new operation that call the API
    \[\<u\>https://api.chucknorris.io/jokes/random\</u\>\](https://api.chucknorris.io/jokes/random)
    and return the joke. Drücken Sie die Eingabetaste. Drücken Sie die
    Tabulatortaste, um den Code zu übernehmen.

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image53.png)

4.  Drücken Sie die Tabulatortaste, um den Code zu übernehmen.

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image54.png)

5.  Klicken Sie auf Terminal -\> New Terminal -\> Gitbash und führen Sie
    die folgenden Befehle aus

cd exercisefiles/quarkus/copilot-demo/

mvn test

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image55.png)

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image56.png)

6.  Führen Sie mvn package aus, um Ihre Anwendung zu verpacken.

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image57.png)

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image58.png)

7.  Ausführen: mvn quarkus:dev

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image59.png)

8.  Test: curl -v http://localhost:8080/hello/joke

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image60.png)

**Aufgabe 7: URL-Parsing**

Wenn Sie eine URL als Abfrageparameter angeben, analysieren Sie sie und
geben Sie die Parameter Protokoll, Host, Port, Pfad und Abfrage zurück.
Die Antwort sollte im JSON-Format vorliegen.

1.  Geben Sie // Given a url as query parameter, parse it and return the
    protocol, host, port, path and query parameters. Die Antwort sollte
    im JSON-Format vorliegen. und drücken Sie die Eingabetaste. Drücken
    Sie die Tabulatortaste, um den Copilot-Vorschlagscode zu übernehmen.

![Ein Screenshot eines Computerprogramms Beschreibung automatisch
generiert](./media/image61.png)

![Ein Screenshot eines Computerprogramms Beschreibung automatisch
generiert](./media/image62.png)

2.  Wechseln Sie zu **CopilotDemoApplicationTests.java**. Um einen
    Komponententest zum Testen der obigen Funktion zu schreiben, fügen
    Sie // Write unit test for Given a url as query parameter, parse it
    and return the protocol, host, port, path and query parameters. Die
    Antwort sollte im JSON-Format vorliegen. Drücken Sie die
    Eingabetaste. Drücken Sie die Tabulatortaste, um den Code zu
    übernehmen.

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image63.png)

3.  Führen Sie mvn test aus

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image64.png)

![Ein Screenshot eines Computers Beschreibung wird automatisch
generiert](./media/image65.png)

4.  Führen Sie mvn package aus, um Ihre Anwendung zu verpacken.

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image66.png)

5.  Führen Sie mvn quarkus:dev aus.

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image67.png)

6.  Klicken Sie auf “split terminal” und führen Sie curl -v
    http://localhost:8080/hello/parseurl?url=https://www.google.com/search?q=quarkus

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image68.png)

**Aufgabe 9 : Zählen von Wörtern**

Gibt den Pfad einer Datei an und zählt die Anzahl der Vorkommen eines
bereitgestellten Wortes. Der Pfad und das Wort sollten Abfrageparameter
sein. Die Antwort sollte im JSON-Format vorliegen.

1.  Geben Sie // Given the path of a file and count the number of
    occurrence of a provided word. The path and the word should be query
    parameters. Die Antwort sollte im JSON-Format vorliegen. und drücken
    Sie die Eingabetaste. Drücken Sie die Tabulatortaste, um den
    Copilot-Vorschlagscode zu übernehmen.

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image69.png)

2.  Wechseln Sie zu **CopilotDemoApplicationTests.java**. Um einen
    Komponententest zu schreiben, um die obige Funktion zu testen, fügen
    Sie ///Write unit test to Given the path of a file and count the
    number of occurrence of a provided word. Der Pfad und das Wort
    sollten Abfrageparameter sein. Die Antwort sollte im JSON-Format
    vorliegen. Drücken Sie die Eingabetaste. Drücken Sie die
    Tabulatortaste, um den Code zu übernehmen.

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image70.png)

3.  Öffnen Sie das **Terminal** und führen Sie den mvn test aus

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image71.png)

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image72.png)

4.  Führen Sie mvn package aus, um Ihre Anwendung zu verpacken.

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image73.png)

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image74.png)

5.  Ausführen: mvn quarkus:dev

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image75.png)

6.  Test: curl
    \<http://localhost:8080/hello/countword?path=/tmp/test.txt&word=hello

Sie können GitHub Copilot nach dem curl-Befehl für Ihr Projekt fragen.

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image76.png)

**Aufgabe 10: Containerisieren der Anwendung**

Verwenden Sie die bereitgestellte Dockerfile, um ein Docker-Image der
Anwendung zu erstellen. In diesem Fall wird der vollständige Inhalt
bereitgestellt, aber zum Erstellen, Ausführen und Testen des
Docker-Images verwenden Sie auch Copilot, um die Befehle zu generieren.

Ich habe eine DOCKER.md Datei erstellt, in der wir die Schritte zum
Erstellen der Anwendung (nativ), zum Erstellen des Container-Images, zum
Ausführen des Containers und zum Testen des Containers dokumentieren.

1.  Drücken Sie in Visual Studio Code **Ctrl +Shit + X** Suchen Sie nach
    **Docker** und installieren Sie es.

![Ein Screenshot eines Computers Beschreibung wird automatisch
generiert](./media/image77.png)

2.  Doppelklicken Sie auf **Desktop Docker** und melden Sie sich mit
    Ihrem Docker-Konto an.

![Defektes Bild](./media/image78.png)

3.  Drücken Sie **Ctrl +Alt+I**, um den **Github Copilot-Chat** zu
    öffnen. Fragen Sie Ihren Copilot, wie das Containerimage erstellt,
    der Container ausgeführt und der Container mit der bereitgestellten
    Dockerfile getestet wird

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image79.png)

4.  Befolgen Sie die Anweisungen von Copilot.Erstellen Sie die
    Anwendung: Führen Sie den folgenden Befehl in Ihrem Terminal aus:

./mvnw package -Pnative -Dquarkus.native.container-build=true

![Ein Screenshot eines Computers Beschreibung wird automatisch
generiert](./media/image77.png)

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image80.png)

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image81.png)

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image82.png)

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image83.png)

5.  **Erstellen Sie das Docker-Image:** Angenommen, Ihre Docker-Datei
    heißt **Dockerfile.native-micro**, können Sie den folgenden Befehl
    verwenden:

docker build -f Dockerfile.native-micro -t my-app .

![Ein Computer-Screenshot eines Programms Beschreibung wird automatisch
generiert](./media/image84.png)

6.  Dieser Befehl weist Docker an, ein Image mit der Dockerfile mit dem
    Namen "Dockerfile.native-micro" im aktuellen Verzeichnis ('.' am
    Ende des Befehls) zu erstellen und das resultierende Image mit dem
    Namen "my-app" zu markieren.

7.  Führen Sie das Docker-Image aus: Nachdem das Image erstellt wurde,
    können Sie es mit dem Befehl "docker run" ausführen:

docker run -p 8080:8080 my-app

![Defektes Bild](./media/image85.png)

Dieser Befehl weist Docker an, einen Container aus dem Image "my-app"
auszuführen und den Port 8080 im Container auf den Port 8080 des
Host-Systems zu mappen.

1.  **Testen Sie die Anwendung**: Um zu testen, ob Ihre Anwendung
    ordnungsgemäß ausgeführt wird, können Sie eine Anfrage an
    http://localhost:8080 in Ihrem Browser senden oder ein Tool wie curl
    verwenden:

curl http://localhost:8080

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image86.png)

Dieser Befehl sendet eine GET-Anforderung an die Anwendung und gibt die
Antwort aus. Wenn Ihre Anwendung ordnungsgemäß ausgeführt wird, sollte
die erwartete Antwort angezeigt werden.

Bitte beachten Sie, dass diese Befehle in Ihrem Terminal und nicht in
Ihrem Java-Anwendungscode ausgeführt werden sollten.

