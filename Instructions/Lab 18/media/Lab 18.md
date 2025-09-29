**Lab 18 - Creare un'API REST utilizzando Spring Boot con l'aiuto di
GitHub Copilot**

**Traguardo**

L'obiettivo di questo lab è imparare a usare GitHub Copilot, usando un
esercizio che consiste nella creazione di un'API REST usando Spring
Boot.

Abbiamo creato un progetto Spring Boot con alcuni file già creati, puoi
trovare il progetto nella cartella
**C:\CopilotHackathon\exercisefiles\springboot**.

Prima di eseguire questo laboratorio, installiamo i pacchetti software
necessari e configuriamo l'ambiente.

Attività 0: Installazione e configurazione dell'ambiente

È necessario scaricare e installare i seguenti pacchetti software per
configurare l'ambiente per eseguire questo lab.

a\. Microsoft JDK 17

b\. apache maven

1.  Aprire il browser Edge.

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image1.jpeg)

2.  Nel campo URL del browser copiare e incollare il collegamento per
    scaricare i pacchetti software nella macchina virtuale del lab.

A. Microsoft JDK 17 ◊
https://aka.ms/download-jdk/microsoft-jdk-17.0.12-windows-x64.msi

B. Apache Maven
◊https://dlcdn.apache.org/maven/maven-3/3.9.9/binaries/apache-maven-3.9.9-bin.zip

**Nota:** Ripetere gli stessi passaggi per scaricare anche tutti gli
altri pacchetti. Per impostazione predefinita, i pacchetti verranno
salvati nella cartella dei download.

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image2.jpeg)

a\. **Installazione di Microsoft JDK 17**

1.  Nella cartella **Download** (**C:\Users\Admin\Downloads**) e fare
    doppio clic su **Microsoft JDK**

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image3.jpeg)

2.  Fare clic su **Next**.

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image4.jpeg)

3.  Accettare l'EULA e fare clic su **Next**.

![Uno screenshot di un contratto software I contenuti generati
dall'intelligenza artificiale potrebbero non essere
corretti.](./media/image5.jpeg)

4.  Selezionare **Install just for you (Admin) **e fare clic su
    **Next**.

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image6.jpeg)

5.  Nella schermata **Custom setup**, ora imposterai **set the JAVA_HOME
    variable**. Fare clic sulla freccia giù e selezionare **Entire
    feature will be installed on local hard drive**.

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image7.jpeg)

6.  Fare clic su **Next**.

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image8.jpeg)

7.  Fare clic su **Install**.

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image9.jpeg)

**b. Installare apache-maven**

8.  Passare alla cartella **Downloads** (**C:\Users\Admin\Downloads**)

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image10.jpeg)

9.  Fare clic con **apache-maven-3.9.9-bin.zip** destro sulla cartella e
    selezionare **Extract All**.

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image11.jpeg)

10. Nella pagina "**Select a destination**", inserire la destinazione
    come **C:\Users\Admin\Downloads** e fare clic su **Extract**.

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image12.jpeg)

11. I file estratti saranno come mostrato nello screenshot.

**Nota:** Assicurati che la cartella sia rinominata come
**apache-maven-3.9.9**, se vedi un altro nome.

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image13.jpeg)

**Impostazione delle variabili ambientali**

12. Fare clic sul logo di **Windows** e selezionare **Settings**

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image14.jpeg)

13. Cercare **Edit system** nella pagina **Windows settings **e
    selezionare **Edit System Environment variable**.

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image15.jpeg)

14. Fare clic sul pulsante **Environment Variable**.

![Uno screenshot di un programma per computer I contenuti generati
dall'intelligenza artificiale potrebbero non essere
corretti.](./media/image16.jpeg)

15. Fare clic su **New **nella sezione **User variable for Admin**.

![Uno screenshot di un programma per computer I contenuti generati
dall'intelligenza artificiale potrebbero non essere
corretti.](./media/image17.jpeg)

16. A questo punto verranno configurate le variabili di ambiente e di
    percorso per Maven.

Selezionare **New **nella sezione **User variable for Admin**.

![Uno screenshot di un programma per computer I contenuti generati
dall'intelligenza artificiale potrebbero non essere
corretti.](./media/image18.jpeg)

17. Nella finestra **New User Variable**, immettere quanto segue e fare
    clic su **OK**

Variable name: MAVEN_HOME

Variable value: C:\Users\Admin\Downloads\apache-maven-3.9.9

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image19.jpeg)

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image20.jpeg)

18. Ora selezionare **Path **e fare clic su **Edit**

![Uno screenshot di un programma per computer I contenuti generati
dall'intelligenza artificiale potrebbero non essere
corretti.](./media/image21.jpeg)

19. Nella finestra **Edit environment variable **fare clic su **New**.

![Uno screenshot di un programma per computer I contenuti generati
dall'intelligenza artificiale potrebbero non essere
corretti.](./media/image22.jpeg)

20. Nel campo vuoto, inserire il seguente %MAVEN_HOME%\bin e fare clic
    su **OK**.

![Uno screenshot di un programma per computer I contenuti generati
dall'intelligenza artificiale potrebbero non essere
corretti.](./media/image23.jpeg)

![Uno screenshot di un programma per computer I contenuti generati
dall'intelligenza artificiale potrebbero non essere
corretti.](./media/image24.jpeg)

21. Fare clic su **OK** per completare la configurazione dell'ambiente
    utente e delle variabili di percorso per Maven.

![Uno screenshot di un programma per computer I contenuti generati
dall'intelligenza artificiale potrebbero non essere
corretti.](./media/image25.jpeg)

22. A questo punto imposterai le **System variables **per Maven.
    Selezionare **New **nella sezione **System variables**.

![Uno screenshot di un programma per computer I contenuti generati
dall'intelligenza artificiale potrebbero non essere
corretti.](./media/image26.jpeg)

23. Nella finestra **New System Variable**, immettere quanto segue e
    fare clic su **OK**

Variable name: MAVEN_HOME

Variable value: C:\Users\Admin\Downloads\apache-maven-3.9.9

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image27.jpeg)

Attività 1 : Creare il codice per gestire una semplice richiesta GET

Passa al file 'DemoController.java' e inizia a scrivere il codice per
gestire una semplice richiesta GET. In questo primo esercizio, abbiamo
fornito un commento che descrive il codice che devi generare. Basta
premere invio e attendere un paio di secondi, Copilot genererà il codice
per te.

Esiste già un test unitario implementato per questo esercizio, è
possibile eseguirlo utilizzando il comando mvn test prima e dopo per
convalidare che il codice generato da Copilot sia corretto.

Creare quindi un nuovo unit test per il caso in cui non viene fornita
alcuna chiave nella richiesta.

Dopo ogni esercizio, sentiti libero di creare un pacchetto ed eseguire
la vostra applicazione per testarla.

Package: mvn package

Run: mvn spring-boot:run

Test: curl -v <http://localhost:8080/hello?key=world>

1.  Aprire File Explorer, espandere Local Disk (C:) ed espandere i file
    **CopilotHackathon-\>exercisefiles \> Springboot \> copilot-demo \>
    src\>main\>java\>com\>Microsoft\>hackathon\>copilotdemo\>controller** per
    visualizzare il file **'DemoController.java**.

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image28.jpeg)

Fare doppio clic **DemoController.java** file. In questo primo
esercizio, viene fornito solo un commento che descrive il codice che è
necessario generare.

![Uno screenshot di un computer Descrizione generata
automaticamente](./media/image29.png)

2.  Prendere il cursore alla fine del commento (riga 12) basta premere
    invio e attendere un paio di secondi, **Copilot** genererà il codice
    per voi. Premere la scheda finché non vi dà il codice completo.

Puoi anche premere Ctrl + Enter per scegliere le opzioni del codice.

![Uno screenshot di un computer Descrizione generata
automaticamente](./media/image30.png)

![Uno screenshot di un computer Descrizione generata
automaticamente](./media/image31.png)

3.  Espandere la cartella del **test** e fare clic su
    **CopilotDemoApplicationTests.java.** Il test unitario vi è già
    stato dato.

![Uno screenshot dello schermo di un computer Descrizione generata
automaticamente](./media/image32.png)

4.  Puoi provare a eseguire il codice senza aggiornare pom xml e
    chiedere a Coiplot una soluzione per esplorare il prodotto.

5.  Aprire **Pom.xml** aggiungere il plug-in sottostante e salva il file

6.  \<plugin\>

7.  \<groupId\>org.apache.maven.plugins\</groupId\>

8.  \<artifactId\>maven-compiler-plugin\</artifactId\>

9.  \<version\>3.8.1\</version\>

10. \<configuration\>

11. \<source\>17\</source\>

12. \<target\>17\</target\>

13. \</configuration\>

\</plugin\>

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image33.png)

14. Fare clic su **Terminal -\> New Terminal **dalla barra degli
    strumenti.

![Immagine rotta](./media/image34.png)

15. Selezionare **Gitbash** ed eseguire il comando seguente.

cd exercisefiles/springboot/copilot-demo/

![Immagine rotta](./media/image35.png)

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image36.png)

16. Eseguire il comando mvn clean install -DskipTests

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image37.png)

![Uno screenshot di un computer Descrizione generata
automaticamente](./media/image38.png)

17. Eseguire mvn test se la compilazione non riesce con errore.

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image39.png)

18. Fare clic sull'icona **Copilot** nell'angolo in basso a destra e
    selezionare **Github Copilot Chat**.

![Immagine rotta](./media/image40.png)

19. Chiedere alla chat di Github Copilot di fornire una correzione per
    il vostro errore.

![Uno screenshot dello schermo di un computer Descrizione generata
automaticamente](./media/image41.png)

20. Guardare la chat di Copilot che spiega il problema e la correzione
    corrispondente. Se non vi è ancora chiara la correzione, continua a
    porre i vostri dubbi e Copilot vi risponderà. Leggere e comprendere
    l'errore e la soluzione da implementare.

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image42.png)

21. Fornire il metodo /hello a Copilot e vediamo cosa suggerirà.

![Immagine rotta](./media/image43.png)

22. Tornare al **CopilotDemoApplicationTests.java** Prendere il cursore
    alla fine del test (riga 24) e premere Enter. Copilot genera un
    altro test per voi. Premere la scheda per accettarlo.

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image44.png)

23. Fornire il metodo /hello dal test a Copilot e vedere cosa suggerirà.

![Uno screenshot di un computer Descrizione generata
automaticamente](./media/image45.png)

24. Eseguire nuovamente il test mvn Il vostro codice può essere simile
    al seguente. Puoi anche scrivere il vostro codice e chiedere a
    Copilot di convalidare.

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

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image46.png)

35. Eseguire il comando mvn package

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image47.png)

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image48.png)

36. Run mvn spring-boot:run

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image49.png)

37. Fare clic su dividi il terminale e inserire curl -v
    http://localhost:8080/hello?key=world nel 2 ° terminale . Puoi anche
    chiedere al vostro Copilot di fornire il comando curl per testare il
    vostro codice.

![Immagine rotta](./media/image50.png)

38. Fare clic su dividi il terminale e inserire curl -v
    http://localhost:8080/hello nel 2° terminale

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image51.png)

39. Premere CTRL + C per arrestare il servizio in esecuzione.

Attività 2 : Confronto delle date

Nuova operazione in /diffdates che calcola la differenza tra due date.
L'operazione deve ricevere due date come parametro nel formato
gg-MM-aaaa e restituire la differenza in giorni.

Inoltre, creare uno unit test che convalidi l'operazione.

D'ora in poi, sarà necessario creare gli unit test per ogni nuova
operazione. Non è stato facile con Copilot?

1.  Andare su **DemoController.java** e inserire il prompt //create una
    nuova operazione in /diffdates che calcola la differenza tra due
    date. L'operazione dovrebbe ricevere due date come parametro nel
    formato gg-MM-aaaa e restituire la differenza in giorni e premere
    Invio. Attendere un po' di tempo e una volta che il copilot prevede
    il codice, premere la scheda per accettare il codice.

![Immagine rotta](./media/image52.png)

2.  Puoi anche utilizzare il codice qui sotto.

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

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image53.png)

14. D'ora in poi, sarà necessario creare gli unit test per ogni nuova
    operazione. Usa Copilot per creare.

15. Aprire **CopilotDemoApplicationTests.java** nella cartella del
    **test** e immettere il prompt // create unit test in /diffdates che
    calcola la differenza tra due date. L'operazione deve ricevere due
    date come parametro nel formato gg-MM-aaaa e restituire la
    differenza in giorni. quindi premere Invio. Attendere un secondo per
    consentire al copilota di prevedere il codice e premere TAB per
    accettare il codice previsto.

16. È possibile accedere e premere TAB per creare più unit test

![Una schermata del computer di un programma Descrizione generata
automaticamente](./media/image54.png)

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image55.png)

17. Chiedere aiuto alla chat di Copilot per problemi da risolvere o per
    spiegare il test unitario e aggiornare il codice, se necessario, in
    base agli input di Copilot.

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

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image56.png)

35. Aprire **Terminal -\>Gitbash **ed eseguire i comandi seguenti

cd "exercisefiles\springboot\copilot-demo"

mvn test

![Immagine rotta](./media/image57.png)

36. Se vengono visualizzati errori di compilazione, copiare il messaggio
    di errore e chiedere a Copilot la correzione.

![Immagine rotta](./media/image58.png)

37. Copolit suggerisce di importare pacchetti con codice. Aggiungere il
    comando al vostro codice ed eseguire il test mvn

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image59.png)

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image60.png)

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image61.png)

38. Run mvn package

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image62.png)

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image63.png)

39. Eseguire il test mvn -Dtest=CopilotDemoApplicationTests#diffdates
    test

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image64.png)

40. Run mvn spring-boot:run

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image65.png)

41. Fare clic su Dividi terminale ed eseguire curl -v
    http://localhost:8080/diffdates?date1=01-01-2021&date2=01-02-2021

Vedrai un errore. Chiedere aiuto a Copilot e risolvere il piccolo
problema.

![Uno screenshot dello schermo di un computer Descrizione generata
automaticamente](./media/image66.png)

42. Come Copilot Chat per aiutarti con il comando curl. Basta copiare il
    messaggio di errore come incollarlo nella chat. Copilot vi dà il
    comando modificato con la spiegazione

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image67.png)

Attività 3 : Convalidare il formato di un telefono spagnolo

Convalidare il formato di un numero di telefono spagnolo (+34 prefisso,
poi 9 cifre, iniziando con 6, 7 o 9). L'operazione deve ricevere un
numero di telefono come parametro e restituire true se il formato è
corretto, false in caso contrario.

1.  Aprire DemoController.Java e inserire il prompt // Convalida il
    formato di un numero di telefono spagnolo (+34 prefisso, poi 9
    cifre, iniziando con 6, 7 o 9). L'operazione deve ricevere un numero
    di telefono come parametro e restituire true se il formato è
    corretto, false in caso contrario. . Premere TAB per accettare il
    codice.

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image68.png)

2.  Puoi anche utilizzare il codice sottostante.

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

11. Passare a **CopilotDemoApplicationTests.java**. Per scrivere un test
    unitario per testare la funzione precedente, aggiungere //Scrivere
    test unitario per convalidare il formato di un numero di telefono
    spagnolo (+34 prefisso, quindi 9 cifre, iniziando con 6, 7 o 9).
    L'operazione dovrebbe ricevere un numero di telefono come parametro
    e restituire true se il formato è corretto, false altrimenti premere
    **Enter**. Premere la scheda per accettare il codice.

![Una schermata del computer di un programma Descrizione generata
automaticamente](./media/image69.png)

12. È inoltre possibile utilizzare gli unit test riportati di seguito
    oppure scrivere unit test personalizzati.

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

42. Aprire **Terminal -\>Gitbash** ed eseguire i comandi seguenti.

cd exercisefiles/springboot/copilot-demo/

mvn test

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image70.png)

43. Run mvn package

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image71.png)

44. Run mvn spring-boot:run

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image72.png)

45. Dividere il terminale ed eseguire i seguenti comandi curl per
    convalidare i numeri di telefono.

curl -v http://localhost:8080/validatephone?phone=+34866666666

curl -v http://localhost:8080/validatephone?phone=+34666666667

curl -v http://localhost:8080/validatephone?phone=+34666666666

![Uno screenshot dello schermo di un computer Descrizione generata
automaticamente](./media/image73.png)

Attività 4 : Convalidare il formato di un DNI spagnolo

Convalidare il formato di un DNI spagnolo (8 cifre e 1 lettera).
L'operazione deve ricevere un DNI come parametro e restituire true se il
formato è corretto, false in caso contrario.

1.  Aprire DemoController.Java e inserire il prompt // Convalida il
    formato di un DNI spagnolo (8 cifre e 1 lettera). L'operazione deve
    ricevere un DNI come parametro e restituire true se il formato è
    corretto, false in caso contrario. . Premere la scheda per accettare
    il codice.

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image74.png)

2.  Puoi anche utilizzare il codice sottostante

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

11. Passare a **CopilotDemoApplicationTests.java**. Per scrivere un test
    unitario per testare la funzione precedente, aggiungere //Scrivere
    test unitario per convalidare il formato di un DNI spagnolo (8 cifre
    e 1 lettera). L'operazione dovrebbe ricevere un DNI come parametro e
    restituire true se il formato è corretto, false altrimenti premere
    **Enter**. Premere il tasto tab per accettare il codice.

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image75.png)

12. È inoltre possibile utilizzare lo unit test riportato di seguito
    oppure scrivere unit test personalizzati.

13. @Test

14. void validatedniNoDni() throws Exception {

15. mockMvc.perform(MockMvcRequestBuilders.get("/validatedni"))

16. .andExpect(MockMvcResultMatchers.status().isOk())

17. .andExpect(MockMvcResultMatchers.content().string("false"));

}

18. Open Terminal -\> Gitbash and run the below commands.

cd exercisefiles/springboot/copilot-demo/

mvn test

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image76.png)

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image77.png)

19. Run mvn package

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image78.png)

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image79.png)

20. Run mvn spring-boot:run

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image80.png)

21. Dividere il terminale ed eseguire curl -v
    http://localhost:8080/validatedni?dni=12345678C in \>the
    2^(nd)terminal

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image81.png)

Attività 5 : Dal nome del colore al codice esadecimale

In base al file colors.json esistente in risorse, dato il nome del
colore come parametro di percorso, restituisce il codice esadecimale. Se
il colore non viene trovato, restituire 404

Suggerimento: Utilizzare TDD. Iniziare creando lo unit test e quindi
implementare il codice.

1.  Aprire DemoController.Java e inserire il prompt // In base al file
    colors.json esistente in risorse, dato il nome del colore come
    parametro di percorso, restituisci il codice esadecimale. Se il
    colore non viene trovato, restituire 404 . Premere la scheda Tab per
    accettare il codice.

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image82.png)

2.  Puoi anche utilizzare il codice sottostante oppure puoi scrivere il
    vostro codice.

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

17. Passare a **CopilotDemoApplicationTests.java**. Per scrivere uno
    unit test per testare la funzione precedente, aggiungere //test per
    /color/{color} endpoint Premere Invio. Premere la scheda per
    accettare il codice.

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image83.png)

18. È possibile scrivere gli unit test. Puoi sempre verificare con
    Copilot la presenza di qualsiasi codice/correzione/test unitario

19. Aprire **Terminal -\> Gitbash **ed eseguire i comandi seguenti. Puoi
    vedere gli errori di compilazione.

cd exercisefiles/springboot/copilot-demo/

mvn test

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image84.png)

20. Premere **Ctrl + Alt + I** per aprire **Github Copilot Chat**.
    Copiare il messaggio di errore e incollalo nella finestra della
    chat. Copilot suggerisce la soluzione.

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image85.png)

21. Copilot suggerisce di importare i pacchetti mancanti con la funzione
    di importazione. Copialo e aggiungilo al vostro codice. Premere
    Enter e Copilot ti suggerisce di aggiungere i pacchetti mancanti.
    Premere la scheda e accettali per aggiungerli al codice.

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image86.png)

![Uno screenshot di un computer Descrizione generata
automaticamente](./media/image87.png)

22. Aprire **Terminal -\> Gitbash** ed eseguire nuovamente i comandi
    seguenti.

cd exercisefiles/springboot/copilot-demo/

mvn test

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image88.png)

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image89.png)

23. Eseguire pacchetto mvn Per creare un pacchetto dell'applicazione.

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image90.png)

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image91.png)

24. Run mvn spring-boot:run To test

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image92.png)

25. Puoi chiedere al vostro copilot di aiutarvi con il comando curl per
    testare la vostra funzione.

![Immagine rotta](./media/image93.png)

26. Fare clic su **Split terminal** ed eseguire il comando curl per
    testare l'applicazione. (Aggiornare la port)

![Immagine rotta](./media/image94.png)

27. Testare con i colori elencati nel file **colors.json**

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image95.png)

28. Provare il colore che non è elencato in **colors.json** e guardare i
    risultati

![Una schermata del computer di un programma Descrizione generata
automaticamente](./media/image96.png)

Attività 6 : Jokes creator

Creare una nuova operazione che chiami l'API
https://api.chucknorris.io/jokes/random e restituisca il Joke.

1.  Aprire DemoController.Java e inserire il prompt // nuova operazione
    che chiama l'API https://api.chucknorris.io/jokes/random e
    restituisce il Joke. Premere la scheda per accettare il codice.

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image97.png)

![Una schermata del computer di un programma Descrizione generata
automaticamente](./media/image98.png)

2.  Puoi anche utilizzare il codice sottostante.

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

![Una schermata del computer di un programma Descrizione generata
automaticamente](./media/image99.png)

18. Passare a **CopilotDemoApplicationTests.java**. Per scrivere uno
    unit test per testare la funzione precedente, aggiungere // Creare
    uno unit test per una nuova operazione che chiama l'API
    https://api.chucknorris.io/jokes/random e restituisce lo scherzo
    Premere Enter. Premere la scheda per accettare il codice.

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image100.png)

19. È inoltre possibile aggiungere il test unitario sottostante oppure è
    possibile scrivere i propri test unitari.

20. @Test

21. void joke() throws Exception{

22. mockMvc.perform(MockMvcRequestBuilders.get("/joke"))

23. .andExpect(MockMvcResultMatchers.status().isOk())

24. // check that content is a string

25. .andExpect(MockMvcResultMatchers.content().string(Matchers.any(String.class)));

}

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image101.png)

26. Aprire Terminal -\> Gitbahs ed eseguire i comandi seguenti .

cd exercisefiles/springboot/copilot-demo/

mvn test

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image101.png)

![Uno screenshot di un computer Descrizione generata
automaticamente](./media/image102.png)

27. Creare il pacchetto dell'applicazione. Eseguire pacchetto mvn

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image103.png)

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image104.png)

28. Run mvn spring-boot:run

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image105.png)

![Immagine rotta](./media/image106.png)

29. Fare clic su Split terminal ed eseguire il comando per: curl -v
    http://localhost:8080/joke nel 2° terminale

![Uno screenshot dello schermo di un computer Descrizione generata
automaticamente](./media/image107.png)

Attività 7 : Analisi degli URL

Dato un url come parametro di query, analizzarlo e restituire il
protocollo, l'host, la porta, il percorso e i parametri di query. La
risposta deve essere in formato Json.

1.  Aprire **DemoController.Java** e inserire il prompt //scrivi un
    codice per Given a url as query parameter, analizzalo e restituisci
    i parametri di protocollo, host, porta, percorso e query. La
    risposta dovrebbe essere in formato Json. Premere la scheda per
    accettare il codice.

![Immagine rotta](./media/image108.png)

2.  Puoi anche utilizzare il codice qui sotto.

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

![Una schermata del computer di un programma Descrizione generata
automaticamente](./media/image109.png)

16. Passa a **CopilotDemoApplicationTests.java**. Per scrivere uno unit
    test per testare la funzione precedente, aggiungere // Creare uno
    unit test per una nuova operazione che chiama l'API
    https://api.chucknorris.io/jokes/random e restituisce lo scherzo
    Premere Enter. Premere la scheda per accettare il codice.

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image110.png)

17. È inoltre possibile aggiungere unit test sottostanti o scrivere unit
    test personalizzati.

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

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image111.png)

33. Aprire **Terminal -\> Gitbash** ed eseguire i comandi seguenti.

cd exercisefiles/springboot/copilot-demo/

mvn test

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image112.png)

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image113.png)

34. Eseguire pacchetto mvn Per creare un pacchetto dell'applicazione.

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image114.png)

35. Run mvn spring-boot:run

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image115.png)

![Immagine rotta](./media/image116.png)

36. Dividere il terminale e testare la vostra applicazione : curl -v
    http://localhost:8080/parseurl?url=https://www.google.com/search?q=chuck+norris

![Uno screenshot dello schermo di un computer Descrizione generata
automaticamente](./media/image117.png)

Attività 8 : Conteggio delle parole

Dato il percorso di un file e contare il numero di occorrenze di una
parola fornita. Il percorso e la parola devono essere parametri di
query. La risposta deve essere in formato Json.

1.  Aprire **DemoController.Java** e inserire il prompt //scrivi un
    codice per Dato il percorso di un file e conta il numero di
    occorrenze di una parola fornita. Il percorso e la parola devono
    essere parametri di query. La risposta dovrebbe essere in formato
    Json. Premere la scheda per accettare il codice.

![Immagine rotta](./media/image118.png)

2.  Passare a **CopilotDemoApplicationTests.java**. Per scrivere un test
    unitario per testare la funzione precedente, aggiungere // Dato il
    percorso di un file e contare il numero di occorrenze di una parola
    fornita. Il percorso e la parola devono essere parametri di query.
    La risposta deve essere in formato Json. Premere la scheda per
    accettare il codice.

![Immagine rotta](./media/image119.png)

3.  Aprire Terminal -\> Gitbash ed eseguire i comandi seguenti.

cd exercisefiles/springboot/copilot-demo/

mvn test

![Immagine rotta](./media/image120.png)

![Immagine rotta](./media/image121.png)

4.  Eseguire il pacchetto mvn per creare il pacchetto della vostra
    applicazione/

![Immagine rotta](./media/image122.png)

5.  Run mvn spring-boot:run

![Immagine rotta](./media/image123.png)

6.  Fare clic su Split terminal ed eseguire il comando curl per testare
    l'applicazione.

curl http://localhost:8080/countword?path=src/test/resources/test.txt

![Immagine rotta](./media/image124.png)

Attività 9 : Containerizzare l'applicazione

Usare il Dockerfile fornito per creare un'immagine docker
dell'applicazione. Ci sono alcuni commenti nel Dockerfile che vi
aiuteranno a completare l'esercizio.

Per creare, eseguire e testare l'immagine docker, è possibile utilizzare
anche Copilot per generare i comandi.

Ad esempio, creare un file DOCKER.md in cui è possibile archiviare i
comandi per creare, eseguire e testare l'immagine docker. Noterai che
Copilot vi aiuterà anche a documentare il vostro progetto e i vostri
comandi.

Esempi di passaggi da documentare: Creare l'immagine del contenitore,
Eseguire il contenitore, Testare il contenitore.

1.  Fare doppio clic su Docker da Dekstop e accedere con il vostro
    account.

2.  Aprire il file Docker om Visual Studio code, aggiungere il codice
    seguente e salva il file.

3.  \# Build a java application image based on openjdk 17 and run it on
    port 8080

4.  FROM openjdk:17-jdk-alpine

5.  EXPOSE 8080

6.  COPY target/\*.jar app.jar

ENTRYPOINT \["java","-jar","/app.jar"\]

![Immagine rotta](./media/image125.png)

7.  Premere **Ctrl + Alt + I** per aprire la finestra di **GitHub
    Copilot**. Chiedere a Copilot di seguito. Copilot fornisce i
    passaggi per containerizzare l'applicazione.

how to build, run and test the docker image with the Dockerfile provided
to create a docker image of the application

![Immagine rotta](./media/image126.png)

8.  Seguire il 1° passaggio: Creare l'immagine Docker. Aprire
    \*\*Terminal -\> Gitbash\*\* ed eseguire il comando per creare
    l'immagine Docker.

cd exercisefiles/springboot/copilot-demo/

docker build -t my-application.

![Immagine rotta](./media/image127.png)

![Immagine rotta](./media/image128.png)

![Uno screenshot di un computer Descrizione generata
automaticamente](./media/image129.png)

9.  Dopo aver creato l'immagine, è possibile eseguirla utilizzando il
    comando docker run.

docker run -p 8080:8080 my-application

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image130.png)

10. Una volta che il contenitore Docker è in esecuzione, è possibile
    testarlo inviando richieste all'applicazione.

curl \<http://localhost:8080/hello?key=world

![Immagine rotta](./media/image131.png)
