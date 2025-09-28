**Lab 18 - Erstellen einer REST-API mit Spring Boot mit Hilfe von GitHub
Copilot**

**Ziel**

Das Ziel dieses Labs ist es, die Verwendung von GitHub Copilot anhand
einer Übung zu erlernen, die darin besteht, eine REST-API mit Spring
Boot zu erstellen.

Wir haben ein Spring Boot Projekt mit einigen bereits erstellten Dateien
erstellt, Sie finden das Projekt im Ordner
**C:\CopilotHackathon\exercisefiles\springboot**.

Bevor wir dieses Lab ausführen, installieren wir zunächst die
erforderlichen Softwarepakete und richten die Umgebung ein.

Aufgabe 0: Installieren und Einrichten der Umgebung

Sie müssen die folgenden Softwarepakete herunterladen und installieren,
um die Umgebung zum Ausführen dieses Labs einzurichten.

a\. Microsoft JDK 17

b\. Apache Maven

1.  Öffnen Sie den Edge-Browser.

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image1.jpeg)

2.  Kopieren Sie in das URL-Feld des Browsers den Link und fügen Sie ihn
    ein, um die Softwarepakete auf Ihre Lab-VM herunterzuladen.

a\. Microsoft JDK 17 ◊
https://aka.ms/download-jdk/microsoft-jdk-17.0.12-windows-x64.msi

B. Apache Maven
◊https://dlcdn.apache.org/maven/maven-3/3.9.9/binaries/apache-maven-3.9.9-bin.zip

**Hinweis:** Wiederholen Sie die gleichen Schritte, um auch alle anderen
Pakete herunterzuladen. Standardmäßig werden die Pakete im
Download-Ordner gespeichert.

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image2.jpeg)

a\. **Installieren von Microsoft JDK 17**

1.  Doppelklicken Sie im Ordner **Downloads**
    (**C:\Users\Admin\Downloads**) auf **Microsoft JDK**

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image3.jpeg)

2.  Klicken Sie auf **Next**.

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image4.jpeg)

3.  Akzeptieren Sie die EULA und klicken Sie auf **Next**.

![Ein Screenshot eines Softwarevertrags KI-generierte Inhalte können
falsch sein.](./media/image5.jpeg)

4.  Wählen Sie **Install just for you (Admin)** aus und klicken Sie auf
    **Next**.

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image6.jpeg)

5.  Im Bildschirm **Custom setup** **legen Sie** nun **die Variable
    JAVA_HOME fest**. Klicken Sie auf den Pfeil nach unten, und wählen
    Sie **Entire feature will be installed on local hard drive** aus.

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image7.jpeg)

6.  Klicken Sie auf **Next**.

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image8.jpeg)

7.  Klicken Sie auf **Install**.

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image9.jpeg)

**b. Installieren Sie apache-maven**

8.  Navigieren Sie zum Ordner **Downloads**
    (**C:\Users\Admin\Downloads**)

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image10.jpeg)

9.  Klicken Sie mit der rechten Maustaste auf
    **apache-maven-3.9.9-bin.zip**-Ordner und wählen Sie **Extract
    All**.

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image11.jpeg)

10. Geben Sie auf der Seite " **Select a destination** " das Ziel als
    **C:\Users\Admin\Downloads** ein und klicken Sie auf **Extract**.

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image12.jpeg)

11. Die extrahierten Dateien sehen so aus, wie im Screenshot gezeigt.

**Hinweis:** Stellen Sie sicher, dass der Ordner in
**apache-maven-3.9.9** umbenannt wird, wenn Sie einen anderen Namen
sehen.

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image13.jpeg)

**Einrichten von Umgebungsvariablen**

12. Klicken Sie auf das **Windows-Logo** und wählen Sie **Settings**

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image14.jpeg)

13. Suchen Sie auf der Seite **Windows-Settings** nach “Edit system” ,
    und wählen Sie **Edit System Environment Variable** aus.

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image15.jpeg)

14. Klicken Sie auf die Schaltfläche **Environment Variable**.

![Ein Screenshot eines Computerprogramms KI-generierte Inhalte können
falsch sein.](./media/image16.jpeg)

15. Klicken Sie unter den Abschnitt **User variable for Admin** auf
    **New**.

![Ein Screenshot eines Computerprogramms KI-generierte Inhalte können
falsch sein.](./media/image17.jpeg)

16. Sie richten nun die Umgebungs- und Pfadvariablen für Maven ein.

Wählen Sie **New** unter den Abschnitt **User variable for Admin** aus.

![Ein Screenshot eines Computerprogramms KI-generierte Inhalte können
falsch sein.](./media/image18.jpeg)

17. Geben Sie im Fenster **New User Variable** Folgendes ein und klicken
    Sie auf **OK**

Name der Variablen: MAVEN_HOME

Variablenwert: C:\Users\Admin\Downloads\apache-maven-3.9.9

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image19.jpeg)

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image20.jpeg)

18. Wählen Sie nun **Path** und klicken Sie auf **Edit**

![Ein Screenshot eines Computerprogramms KI-generierte Inhalte können
falsch sein.](./media/image21.jpeg)

19. Klicken Sie im Fenster **Edit environment variable** auf **New**.

![Ein Screenshot eines Computerprogramms KI-generierte Inhalte können
falsch sein.](./media/image22.jpeg)

20. Geben Sie in das leere Feld %MAVEN_HOME%\bin ein und klicken Sie auf
    **OK**.

![Ein Screenshot eines Computerprogramms KI-generierte Inhalte können
falsch sein.](./media/image23.jpeg)

![Ein Screenshot eines Computerprogramms KI-generierte Inhalte können
falsch sein.](./media/image24.jpeg)

21. Klicken Sie auf **OK**, um die Einrichtung der Benutzerumgebungs-
    und Pfadvariablen für Maven abzuschließen.

![Ein Screenshot eines Computerprogramms KI-generierte Inhalte können
falsch sein.](./media/image25.jpeg)

22. Sie richten nun die **Systemvariablen** für Maven ein. Wählen Sie
    **New** im Abschnitt **System variables** aus.

![Ein Screenshot eines Computerprogramms KI-generierte Inhalte können
falsch sein.](./media/image26.jpeg)

23. Geben Sie im Fenster “New System Variable” Folgendes ein und klicken
    Sie auf **OK**

Name der Variablen: MAVEN_HOME

Variablenwert: C:\Users\Admin\Downloads\apache-maven-3.9.9

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image27.jpeg)

Aufgabe 1: Erstellen des Codes zum Verarbeiten einer einfachen
GET-Anforderung

Wechseln Sie zur Datei 'DemoController.java' und beginnen Sie mit dem
Schreiben des Codes für die Verarbeitung einer einfachen
GET-Anforderung. In dieser ersten Übung haben wir einen Kommentar
bereitgestellt, der den Code beschreibt, den Sie generieren müssen.
Drücken Sie einfach die Eingabetaste und warten Sie ein paar Sekunden,
Copilot generiert den Code für Sie.

Für diese Übung ist bereits ein Komponententest implementiert, den Sie
mit dem Befehl “mvn test” vorher und nachher ausführen können, um zu
überprüfen, ob der von Copilot generierte Code korrekt ist.

Erstellen Sie dann einen neuen Komponententest für den Fall, in dem kein
Schlüssel in der Anforderung angegeben wird.

Nach jeder Übung können Sie Ihre Anwendung verpacken und ausführen, um
sie zu testen.

Package: mvn package

Run: mvn spring-boot:run

Test: curl -v http://localhost:8080/hello?key=world

1.  Öffnen Sie den Datei-Explorer, erweitern Sie Local Disk (C:) und
    erweitern Sie den Ordner **CopilotHackathon-\>exercisefiles \>
    Springboot \> copilot-demo \>
    src\>main\>java\>com\>Microsoft\>hackathon\>copilotdemo\>controller,**
    um die Datei **“DemoController.java”** anzuzeigen.

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image28.jpeg)

Doppelklicken Sie auf **DemoController.java**-Datei. In dieser ersten
Übung wird nur ein Kommentar bereitgestellt, der den Code beschreibt,
den Sie generieren müssen.

![Ein Screenshot eines Computers Beschreibung wird automatisch
generiert](./media/image29.png)

2.  Nehmen Sie den Cursor am Ende des Kommentars (Zeile 12), drücken Sie
    einfach die Eingabetaste und warten Sie ein paar Sekunden,
    **Copilot** generiert den Code für Sie. Drücken Sie auf die
    Registerkarte, bis Sie den vollständigen Code erhalten.

Sie können auch “Ctrl + Enter” drücken, um Codeoptionen auszuwählen.

![Ein Screenshot eines Computers Beschreibung wird automatisch
generiert](./media/image30.png)

![Ein Screenshot eines Computers Beschreibung wird automatisch
generiert](./media/image31.png)

3.  Expandieren Sie den **Test**-Ordner und klicken Sie auf
    **CopilotDemoApplicationTests.java.** Der Unit-Test liegt bereits
    vor.

![Ein Screenshot eines Computerbildschirms Beschreibung wird automatisch
generiert](./media/image32.png)

4.  Sie können versuchen, den Code auszuführen, ohne pom xml zu
    aktualisieren, und Copilot nach einer Lösung fragen, um das Produkt
    zu untersuchen.

5.  Öffnen Sie **Pom.xml** fügen Sie das folgende Plugin hinzu und
    speichern Sie die Datei

6.  \<plugin\>

7.  \<groupId\>org.apache.maven.plugins\</groupId\>

8.  \<artifactId\>maven-compiler-plugin\</artifactId\>

9.  \<version\>3.8.1\</version\>

10. \<configuration\>

11. \<source\>17\</source\>

12. \<target\>17\</target\>

13. \</configuration\>

> \</plugin\>

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image33.png)

14. Klicken Sie in der Symbolleiste auf **Terminal -\> New Terminal**.

![Defektes Bild](./media/image34.png)

15. Wählen Sie **Gitbash** aus und führen Sie den folgenden Befehl aus.

cd exercisefiles/springboot/copilot-demo/

![Defektes Bild](./media/image35.png)

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image36.png)

16. Führen Sie den Befehl “mvn clean install -DskipTests” aus

![Ein Screenshot eines Computerprogramms Beschreibung automatisch
generiert](./media/image37.png)

![Ein Screenshot eines Computers Beschreibung wird automatisch
generiert](./media/image38.png)

17. Führen Sie mvn test aus. Wenn Ihr Build mit einem Fehler
    fehlschlägt.

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image39.png)

18. Klicken Sie auf das **Copilot**-Symbol in der rechten unteren Ecke
    und wählen Sie **Github Copilot Chat** aus.

![Defektes Bild](./media/image40.png)

19. Bitten Sie den Github Copilot-Chat, eine Korrektur für Ihren Fehler
    bereitzustellen.

![Ein Screenshot eines Computerbildschirms Beschreibung wird automatisch
generiert](./media/image41.png)

20. Schauen Sie sich den Copilot-Chat an, in dem das Problem und der
    entsprechende Fix erklärt werden. Wenn Sie sich mit der Lösung immer
    noch nicht im Klaren sind, stellen Sie weiterhin Ihre Zweifel und
    Copilot wird Ihnen antworten. Lesen und verstehen Sie den Fehler und
    die zu implementierende Lösung.

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image42.png)

21. Stellen Sie Copilot die /hello-Methode zur Verfügung, und sehen wir
    uns an, was sie vorschlagen wird.

![Defektes Bild](./media/image43.png)

22. Kehren Sie zum **CopilotDemoApplicationTests.java** Bewegen Sie den
    Cursor am Ende des Tests (Zeile 24) und drücken Sie die
    Eingabe-Taste. Copilot generiert einen weiteren Test für Sie.
    Drücken Sie die Tabulator-Taste, um sie zu übernehmen.

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image44.png)

23. Geben Sie die /hello-Methode aus dem Test für Copilot an, und prüfen
    Sie, was sie vorschlagen wird.

![Ein Screenshot eines Computers Beschreibung wird automatisch
generiert](./media/image45.png)

24. Führen Sie den mvn-Test erneut aus. Ihr Code kann wie folgt
    aussehen. Sie können auch Ihren eigenen Code schreiben und Copilot
    bitten, ihn zu validieren.

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

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image46.png)

35. Führen Sie den Befehl mvn package aus

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image47.png)

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image48.png)

36. Führen Sie mvn spring-boot:run aus.

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image49.png)

37. Klicken Sie auf “Split the Terminal” und geben Sie curl -v
    http://localhost:8080/hello?key=world im 2. Terminal ein. Sie können
    Ihren Copilot auch bitten, den curl-Befehl bereitzustellen, um Ihren
    Code zu testen.

![Defektes Bild](./media/image50.png)

38. Klicken Sie auf “Split the Terminal” und geben Sie curl -v
    http://localhost:8080/hello im 2. Terminal ein

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image51.png)

39. Drücken Sie Ctrl +C, um den ausgeführten Dienst zu beenden.

Aufgabe 2 : Vergleich der Termine

Neuer Vorgang unter /diffdates, der die Differenz zwischen zwei
Datumsangaben berechnet. Die Operation sollte zwei Datumsangaben als
Parameter im Format dd-MM-yyyy erhalten und die Differenz in Tagen
zurückgeben.

Erstellen Sie außerdem einen Komponententest, der den Vorgang überprüft.

Von nun an müssen Sie die Komponententests für jeden neuen Vorgang
erstellen. War es nicht einfach mit Copilot?

1.  Wechseln Sie zu **DemoController.java,** und geben Sie unter
    /diffdates die Prompt //create a New operation ein, die die
    Differenz zwischen zwei Datumsangaben berechnet. Der Vorgang sollte
    zwei Datumsangaben als Parameter im Format dd-MM-yyyy erhalten und
    die Differenz in Tagen zurückgeben und die Eingabetaste drücken.
    Warten Sie einige Zeit, und sobald der Copilot den Code vorhergesagt
    hat, drücken Sie die Tabulatortaste, um den Code zu akzeptieren.

![Defektes Bild](./media/image52.png)

2.  Sie können auch den folgenden Code verwenden.

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

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image53.png)

14. Von nun an müssen Sie die Komponententests für jeden neuen Vorgang
    erstellen. Verwenden Sie Copilot zum Erstellen.

15. Öffnen Sie **CopilotDemoApplicationTests.java** unter dem
    **test**-Ordner, und geben Sie die Prompt // create unit test to
    /diffdates ein, die die Differenz zwischen zwei Datumsangaben
    berechnet. Die Operation sollte zwei Datumsangaben als Parameter im
    Format dd-MM-yyyy erhalten und die Differenz in Tagen
    zurückgeben. Drücken Sie dann die Eingabetaste. Warten Sie, bis der
    Copilot den Code vorhergesagt hat, und drücken Sie die
    Tabulator-Taste, um den vorhergesagten Code zu akzeptieren.

16. Sie können die Tabulator-Taste eingeben und drücken, um mehrere
    Komponententests zu erstellen

![Ein Computer-Screenshot eines Programms Beschreibung wird automatisch
generiert](./media/image54.png)

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image55.png)

17. Nehmen Sie die Copilot-Chat-Hilfe in Anspruch, um Probleme zu
    beheben oder den Unittest zu erklären und den Code zu aktualisieren,
    falls dies auf der Grundlage von Copilot-Eingaben erforderlich ist.

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

}![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image56.png)

35. Öffnen Sie **Terminal -\>Gitbash** und führen Sie die folgenden
    Befehle aus

cd "exercisefiles\springboot\copilot-demo"

mvn test ![Defektes Bild](./media/image57.png)

36. Wenn Kompilierungsfehler angezeigt werden, kopieren Sie die
    Fehlermeldung und bitten Sie Copilot um die Lösung.

![Defektes Bild](./media/image58.png)

37. Copilot schlägt vor, Pakete mit Code zu importieren. Fügen Sie den
    Befehl zu Ihrem Code hinzu, und führen Sie mvn test aus

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image59.png)

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image60.png)

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image61.png)

38. Führen Sie das mvn-Package aus

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image62.png)

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image63.png)

39. Führen Sie den Test mvn -Dtest=CopilotDemoApplicationTests#diffdates
    test aus.

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image64.png)

40. Führen Sie mvn spring-boot:run aus.

![Ein Screenshot eines Computerprogramms Beschreibung automatisch
generiert](./media/image65.png)

41. Klicken Sie auf “Split terminal” und führen Sie curl -v
    <http://localhost:8080/diffdates?date1=01-01-2021&date2=01-02-2021>
    aus

Es wird ein Fehler angezeigt. Nehmen Sie die Hilfe von Copilot in
Anspruch und beheben Sie das kleine Problem.

![Ein Screenshot eines Computerbildschirms Beschreibung wird automatisch
generiert](./media/image66.png)

42. Als Copilot Chat, um Ihnen mit dem Curl-Befehl zu helfen. Kopieren
    Sie einfach die Fehlermeldung als Einfügen in den Chat. Copilot gibt
    Ihnen den modifizierten Befehl mit Erklärung

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image67.png)

Aufgabe 3: Überprüfen des Formats eines spanischen Telefons

Überprüfen Sie das Format einer spanischen Telefonnummer (+34 Präfix,
dann 9 Ziffern, beginnend mit 6, 7 oder 9). Der Vorgang sollte eine
Telefonnummer als Parameter erhalten und “true” zurückgeben, wenn das
Format korrekt ist, andernfalls “false”.

1.  Öffnen Sie DemoController.Java und geben Sie die Prompt // Validate
    the format of a spanish phone number (+34 prefix, then 9 digits,
    starting with 6, 7 or 9). Der Vorgang sollte eine Telefonnummer als
    Parameter erhalten und “true” zurückgeben, wenn das Format korrekt
    ist, andernfalls “false”. Drücken Sie die Tabulator-Taste, um den
    Code zu übernehmen.

![Ein Screenshot eines Computerprogramms Beschreibung automatisch
generiert](./media/image68.png)

2.  Sie können auch den folgenden Code verwenden.

3.  // Validate the format of a spanish phone number (+34 prefix, then 9
    digits, starting with 6, 7 or 9). Der Vorgang sollte eine
    Telefonnummer als Parameter erhalten und “true” zurückgeben, wenn
    das Format korrekt ist, andernfalls “false”.

4.  @GetMapping("/validatephone")

5.  public boolean validatephone(@RequestParam(name = "phone", required
    = false) String phone) {

6.  if (phone == null || phone.isEmpty()) {

7.  return false;

8.  }

9.  String regex = "^\\+34\[679\]\\d{8}$";

10. return phone.matches(regex);

}

11. Wechseln Sie zu **CopilotDemoApplicationTests.java**. Um einen
    Komponententest zum Testen der obigen Funktion zu schreiben, fügen
    Sie ////Write unit test to validate the format of a spanish phone
    number (+34 prefix, then 9 digits, starting with 6, 7 or 9). Der
    Vorgang sollte eine Telefonnummer als Parameter erhalten und “true”
    zurückgeben, wenn das Format korrekt ist, andernfalls “false”.
    Drücken Sie die Tabulatortaste, um den Code zu übernehmen.

![Ein Computer-Screenshot eines Programms Beschreibung wird automatisch
generiert](./media/image69.png)

12. Sie können auch die folgenden Komponententests verwenden oder eigene
    Komponententests schreiben.

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

42. Öffnen Sie **Terminal -\>Gitbash** und führen Sie die folgenden
    Befehle aus.

cd exercisefiles/springboot/copilot-demo/

mvn test

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image70.png)

43. Führen Sie das mvn-Package aus

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image71.png)

44. Führen Sie mvn spring-boot:run aus.

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image72.png)

45. Teilen Sie das Terminal und führen Sie die folgenden curl-Befehle
    aus, um die Telefonnummern zu validieren.

curl -v http://localhost:8080/validatephone?phone=+34866666666

curl -v http://localhost:8080/validatephone?phone=+34666666667

curl -v http://localhost:8080/validatephone?phone=+34666666666

![Ein Screenshot eines Computerbildschirms Beschreibung wird automatisch
generiert](./media/image73.png)

Aufgabe 4: Überprüfen des Formats eines spanischen DNI

Überprüfen Sie das Format eines spanischen DNI (8 Ziffern und 1
Buchstabe). Der Vorgang sollte einen DNI als Parameter erhalten und
“true” zurückgeben, wenn das Format korrekt ist, andernfalls “false”.

1.  Öffnen Sie DemoController.Java und geben Sie die Prompt // Validate
    the format of a spanish DNI (8 digits and 1 letter) ein. Der Vorgang
    sollte einen DNI als Parameter erhalten und “true” zurückgeben, wenn
    das Format korrekt ist, andernfalls “false”. Drücken Sie die
    Tabulatortaste, um den Code zu übernehmen.

![Ein Screenshot eines Computerprogramms Beschreibung automatisch
generiert](./media/image74.png)

2.  Sie können auch den folgenden Code verwenden

3.  // Validate the format of a spanish DNI (8 digits and 1 letter). Der
    Vorgang sollte einen DNI als Parameter erhalten und “true”
    zurückgeben, wenn das Format korrekt ist, andernfalls “false”.

4.  @GetMapping("/validatedni")

5.  public boolean validatedni(@RequestParam(name = "dni", required =
    false) String dni) {

6.  if (dni == null || dni.isEmpty()) {

7.  return false;

8.  }

9.  String regex = "^\\d{8}\[A-Z\]$";

10. return dni.matches(regex);

}

11. Wechseln Sie zu **CopilotDemoApplicationTests.java**. Um einen
    Komponententest zum Testen der obigen Funktion zu schreiben, fügen
    Sie ///Write unit test to Validate the format of a spanish DNI (8
    digits and 1 letter). Der Vorgang sollte einen DNI als Parameter
    erhalten und “true” zurückgeben, wenn das Format korrekt ist,
    andernfalls “false”. Drücken Sie die Tabulatortaste, um den Code zu
    übernehmen.

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image75.png)

12. Sie können auch den folgenden Komponententest verwenden, oder Sie
    können Ihre eigenen Komponententests schreiben.

13. @Test

14. void validatedniNoDni() throws Exception {

15. mockMvc.perform(MockMvcRequestBuilders.get("/validatedni"))

16. .andExpect(MockMvcResultMatchers.status().isOk())

17. .andExpect(MockMvcResultMatchers.content().string("false"));

}

18. Öffnen Sie Terminal -\> Gitbash und führen Sie die folgenden Befehle
    aus.

cd exercisefiles/springboot/copilot-demo/

mvn test

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image76.png)

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image77.png)

19. Führen Sie das mvn-Paket aus

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image78.png)

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image79.png)

20. Führen Sie mvn spring-boot:run aus.

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image80.png)

21. Teilen Sie das Terminal und führen Sie curl -v
    http://localhost:8080/validatedni?dni=12345678C im zweiten Terminal
    aus.

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image81.png)

Aufgabe 5 : Vom Farbnamen zum Hexadezimalcode

Geben Sie basierend auf der vorhandenen colors.json Datei unter
Resources den Namen der Farbe als Pfadparameter zurück und geben Sie den
Hexadezimalcode zurück. Wenn die Farbe nicht gefunden wird, geben Sie
404 zurück

Tipp: Verwenden Sie TDD. Beginnen Sie mit dem Erstellen des
Komponententests, und implementieren Sie dann den Code.

1.  Öffnen Sie DemoController.Java und geben Sie die Prompt // Based on
    existing colors.json file under resources, given the name of the
    color as path parameter, return the hexadecimal code. If the color
    is not found, return 404.Press the tab to accept the code.

> ![Ein Screenshot eines Computerprogramms Beschreibung automatisch
> generiert](./media/image82.png)

2.  Sie können auch den folgenden Code verwenden oder Ihren Code
    schreiben.

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

17. Wechseln Sie zu **CopilotDemoApplicationTests.java**. Um einen
    Komponententest zum Testen der obigen Funktion zu schreiben, fügen
    Sie //test für den Endpunkt /color/{color} hinzu. Drücken Sie die
    Eingabe-Taste. Drücken Sie die Tab-Taste, um den Code zu
    akzeptieren.

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image83.png)

18. Sie können Ihre Komponententests schreiben. Sie können sich
    jederzeit bei Copilot nach Code/Fix/Unit-Test erkundigen.

19. Öffnen Sie **Terminal -\> Gitbash** und führen Sie die folgenden
    Befehle aus. Sie können Kompilierungsfehler sehen.

cd exercisefiles/springboot/copilot-demo/

mvn test

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image84.png)

20. Drücken Sie **Ctrl +Alt+ I**, um **Github Copilot Chat** zu öffnen.
    Kopieren Sie die Fehlermeldung und fügen Sie sie in das Chat-Fenster
    ein. Copilot schlägt mit der Lösung vor.

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image85.png)

21. Copilot schlägt vor, fehlende Pakete mit der Importfunktion zu
    importieren. Kopieren Sie es, und fügen Sie es Ihrem Code hinzu.
    Drücken Sie die Eingabetaste und Copilot schlägt vor, fehlende
    Pakete hinzuzufügen. Drücken Sie die Tabulatortaste, und akzeptieren
    Sie sie, um sie dem Code hinzuzufügen.

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image86.png)

![Ein Screenshot eines Computers Beschreibung wird automatisch
generiert](./media/image87.png)

22. Öffnen Sie **Terminal -\> Gitbash** und führen Sie die folgenden
    Befehle erneut aus.

cd exercisefiles/springboot/copilot-demo/

mvn test

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image88.png)

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image89.png)

23. Führen Sie “mvn package” aus, um Ihre Anwendung zu verpacken.

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image90.png)

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image91.png)

24. Führen Sie mvn spring-boot:run zum Testen aus

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image92.png)

25. Sie können Ihren Copilot bitten, Ihnen mit dem curl-Befehl zu
    helfen, um Ihre Funktion zu testen.

![Defektes Bild](./media/image93.png)

26. Klicken Sie auf **Split terminal** und führen Sie den Befehl curl
    aus, um Ihre Anwendung zu testen. (Aktualisieren Sie den Port)

![Defektes Bild](./media/image94.png)

27. Testen Sie mit Farben, die in **colors.json**-Datei aufgeführt sind

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image95.png)

28. Testen Sie die Farbe, die nicht in **colors.json** aufgeführt ist,
    und sehen Sie sich die Ergebnisse an

![Ein Computer-Screenshot eines Programms Beschreibung wird automatisch
generiert](./media/image96.png)

Aufgabe 6 : Witze-Ersteller

Erstellen Sie einen neuen Vorgang, der die
API-https://api.chucknorris.io/jokes/random aufruft und den Witz
zurückgibt.

1.  Öffnen Sie DemoController.Java und geben Sie die Prompt // new
    operation that call the API https://api.chucknorris.io/jokes/random
    and return the joke .Press the tab to accept the code.

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image97.png)

![Ein Computer-Screenshot eines Programms Beschreibung wird automatisch
generiert](./media/image98.png)

2.  Sie können auch den folgenden Code verwenden.

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

![Ein Computer-Screenshot eines Programms Beschreibung wird automatisch
generiert](./media/image99.png)

18. Wechseln Sie zu **CopilotDemoApplicationTests.java**. Um einen
    Komponententest zum Testen der obigen Funktion zu schreiben, fügen
    Sie // Create a unit test for new operation that call the API
    https://api.chucknorris.io/jokes/random and return the joke Press
    Enter. Press the tab to accept the code.

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image100.png)

19. Sie können auch den folgenden Komponententest hinzufügen oder eigene
    Komponententests schreiben.

20. @Test

21. void joke() throws Exception{

22. mockMvc.perform(MockMvcRequestBuilders.get("/joke"))

23. .andExpect(MockMvcResultMatchers.status().isOk())

24. // check that content is a string

25. .andExpect(MockMvcResultMatchers.content().string(Matchers.any(String.class)));

}

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image101.png)

26. Öffnen Sie Terminal -\> Gitbahs und führen Sie die folgenden Befehle
    aus.

cd exercisefiles/springboot/copilot-demo/

mvn test

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image101.png)

![Ein Screenshot eines Computers Beschreibung wird automatisch
generiert](./media/image102.png)

27. Packen Sie Ihre Anwendung. Führen Sie mvn package aus

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image103.png)

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image104.png)

28. Führen Sie mvn spring-boot:run aus.

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image105.png)

![Defektes Bild](./media/image106.png)

29. Klicken Sie auf “Split terminal” und führen Sie den Befehl aus: curl
    -v http://localhost:8080/joke im zweiten Terminal

![Ein Screenshot eines Computerbildschirms Beschreibung wird automatisch
generiert](./media/image107.png)

Aufgabe 7: URL-Parsing

Wenn Sie eine URL als Abfrageparameter angeben, analysieren Sie sie und
geben Sie die Parameter Protokoll, Host, Port, Pfad und Abfrage zurück.
Die Antwort sollte im JSON-Format vorliegen.

1.  Öffnen Sie **DemoController.Java** und geben Sie die Prompt // write
    a code for Given a url as query parameter, parse it and return the
    protocol, host, port, path and query parameters. The response should
    be in Json format.Press the tab to accept the code.

![Defektes Bild](./media/image108.png)

2.  Sie können auch den folgenden Code verwenden.

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

> }

![Ein Computer-Screenshot eines Programms Beschreibung wird automatisch
generiert](./media/image109.png)

16. Wechseln Sie zu **CopilotDemoApplicationTests.java**. Um einen
    Komponententest zum Testen der obigen Funktion zu schreiben, fügen
    Sie // Create a unit test for new operation that call the API
    https://api.chucknorris.io/jokes/random and return the joke Press
    Enter. Press the tab to accept the code.

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image110.png)

17. Sie können auch die folgenden Komponententests hinzufügen oder
    eigene Komponententests schreiben.

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

> }

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image111.png)

33. Öffnen Sie **Terminal -\> Gitbash** und führen Sie die folgenden
    Befehle aus.

cd exercisefiles/springboot/copilot-demo/

mvn test

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image112.png)

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image113.png)

34. Führen Sie mvn package aus, um Ihre Anwendung zu verpacken.

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image114.png)

35. Führen Sie mvn spring-boot:run aus.

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image115.png)

![Defektes Bild](./media/image116.png)

36. Teilen Sie das Terminal und testen Sie Ihre Anwendung: curl -v
    http://localhost:8080/parseurl?url=https://www.google.com/search?q=chuck+norris

![Ein Screenshot eines Computerbildschirms Beschreibung wird automatisch
generiert](./media/image117.png)

Aufgabe 8 : Zählen von Wörtern

Gibt den Pfad einer Datei an und zählt die Anzahl der Vorkommen eines
bereitgestellten Wortes. Der Pfad und das Wort sollten Abfrageparameter
sein. Die Antwort sollte im JSON-Format vorliegen.

1.  Öffnen Sie **DemoController.Java** und geben Sie die Prompt //write
    a code for Given the path of a file and count the number of
    occurrence of a provided word ein. Der Pfad und das Wort sollten
    Abfrageparameter sein. Die Antwort sollte im Json-Format vorliegen.
    Drücken Sie die Tabulatortaste, um den Code zu übernehmen.

![Defektes Bild](./media/image118.png)

2.  Wechseln Sie zu **CopilotDemoApplicationTests.java**. Um einen
    Komponententest zum Testen der obigen Funktion zu schreiben, fügen
    Sie // Given the path of a file and count the number of occurrences
    of a provided word. Der Pfad und das Wort sollten Abfrageparameter
    sein. Die Antwort sollte im JSON-Format vorliegen. Drücken Sie die
    Eingabetaste. Drücken Sie die Tabulatortaste, um den Code zu
    übernehmen.

![Defektes Bild](./media/image119.png)

3.  Öffnen Sie Terminal -\> Gitbash und führen Sie die folgenden Befehle
    aus.

cd exercisefiles/springboot/copilot-demo/

mvn test

![Defektes Bild](./media/image120.png)

![Defektes Bild](./media/image121.png)

4.  Führen Sie mvn-package aus, um Ihre Anwendung zu verpacken/

![Defektes Bild](./media/image122.png)

5.  Führen Sie mvn spring-boot:run aus.

![Defektes Bild](./media/image123.png)

6.  Klicken Sie auf “Split terminal” und führen Sie den Befehl curl aus,
    um Ihre Anwendung zu testen.

curl http://localhost:8080/countword?path=src/test/resources/test.txt

![Defektes Bild](./media/image124.png)

Aufgabe 9: Containerisieren der Anwendung

Verwenden Sie die bereitgestellte Dockerfile, um ein Docker-Image der
Anwendung zu erstellen. Es gibt einige Kommentare in der Docker-Datei,
die Ihnen helfen, die Übung abzuschließen.

Um das Docker-Image zu erstellen, auszuführen und zu testen, können Sie
auch Copilot verwenden, um die Befehle zu generieren.

Erstellen Sie beispielsweise eine DOCKER.md-Datei, in der Sie die
Befehle zum Erstellen, Ausführen und Testen des Docker-Images speichern
können. Sie werden feststellen, dass Copilot Ihnen auch dabei hilft, Ihr
Projekt und Ihre Befehle zu dokumentieren.

Beispiele für zu dokumentierende Schritte: Erstellen des
Containerimages, Ausführen des Containers, Testen des Containers.

1.  Doppelklicken Sie auf Docker von Dekstop und melden Sie sich mit
    Ihrem Konto an.

2.  Öffnen Sie die Docker-Datei om Visual Studio Code, fügen Sie den
    folgenden Code hinzu und speichern Sie die Datei.

3.  \# Build a java application image based on openjdk 17 and run it on
    port 8080

4.  FROM openjdk:17-jdk-alpine

5.  EXPOSÉ 8080

6.  COPY target/\*.jar app.jar

ENTRYPOINT \["java","-jar","/app.jar"\]

![Defektes Bild](./media/image125.png)

7.  Drücken Sie **Ctrl +Alt +I**, um das **GitHub Copilot**-Chatfenster
    zu öffnen. Fragen Sie Copilot an die untenstehende Prompt. Copilot
    stellt Schritte zum Containerisieren der Anwendung bereit.

Erstellen, Ausführen und Testen des Docker-Images mit der
bereitgestellten Docker-Datei, um ein Docker-Image der Anwendung zu
erstellen

![Defektes Bild](./media/image126.png)

8.  Befolgen Sie den 1. Schritt – Erstellen Sie das Docker-Image. Öffnen
    Sie \*\*Terminal -\> Gitbash\*\* und führen Sie den Befehl aus, um
    das Docker-Image zu erstellen.

cd exercisefiles/springboot/copilot-demo/

docker build -t my-application.

![Defektes Bild](./media/image127.png)

![Defektes Bild](./media/image128.png)

![Ein Screenshot eines Computers Beschreibung wird automatisch
generiert](./media/image129.png)

9.  Nachdem das Image erstellt wurde, können Sie es mit dem Befehl
    docker run ausführen.

docker run -p 8080:8080 my-application

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image130.png)

10. Sobald der Docker-Container ausgeführt wird, können Sie ihn testen,
    indem Sie Anforderungen an Ihre Anwendung senden.

curl \<http://localhost:8080/hello?key=world

![Defektes Bild](./media/image131.png)

