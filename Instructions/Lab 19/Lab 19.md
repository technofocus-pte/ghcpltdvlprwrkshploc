**Lab 19 - Creare un'API REST utilizzando Quarkus con l'aiuto di GitHub
CopilotGoal**

L'obiettivo di questo laboratorio è imparare a usare GitHub Copilot,
utilizzando un'attività che consiste nella creazione di un'API REST
utilizzando https://quarkus.io/.

Abbiamo creato un progetto Quarkus con alcuni file già creati, puoi
trovare il progetto nella cartella **exercisefiles/quarkus**.

Iniziamo a fare il copiloting!!

**Attività 1 - Creare il codice per gestire una semplice richiesta GET**

Passare al file 'DemoResource.java' e iniziare a scrivere il codice per
gestire una semplice richiesta GET.

1.  In questo primo passaggio, abbiamo fornito un commento che descrive
    il codice che devi generare. Basta premere invio e attendere un paio
    di secondi.

![Immagine rotta](./media/image1.png)

2.  Copilot genererà il codice per te. Se non sei soddisfatto del
    codice, premi Ctrl + Enter e ti suggeriranno più opzioni di codice.

![Uno screenshot di un computer Descrizione generata
automaticamente](./media/image2.png)

3.  . Se non sei soddisfatto del codice generato, puoi premere
    nuovamente invio e Copilot genererà un nuovo codice

![Uno screenshot di un computer Descrizione generata
automaticamente](./media/image3.png)

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image4.png)

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image5.png)

4.  andare su **test/java/com/Microsoft/hackthon/quarkus/** e fare clic
    su **DemoResourceTest.java**. Esiste già un test unitario
    implementato per questa attività.

![Uno screenshot di un computer Descrizione generata
automaticamente](./media/image6.png)

5.  Fare clic su **Terminal -\> New Terminal.**

![Immagine rotta](./media/image7.png)

6.  Selezionare **Gitbash**.

![Immagine rotta](./media/image8.png)

7.  Eseguire il comando cd exercisefiles/quarkus/copilot-demo/.

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image9.png)

8.  È possibile eseguirlo utilizzando il comando mvn test prima e dopo
    per verificare che il codice generato da Copilot sia corretto.

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image10.png)

![Una schermata di un computer Descrizione generata
automaticamente](./media/image11.png)

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image12.png)

9.  Dopo ogni attività, sentiti libero di creare un pacchetto ed
    eseguire la vostra applicazione per testarla.

Package: mvn package

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image13.png)

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image14.png)

10. Run: mvn quarkus:dev

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image15.png)

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image16.png)

11. Fare clic su Split terminal e immettere il comando nel 2° terminale
    ed eseguire

curl -v http://localhost:8080/hello?key=world

curl http://localhost:8080/hello

curl http://localhost:8080/hello?key=world

![Uno screenshot dello schermo di un computer Descrizione generata
automaticamente](./media/image17.png)

![Immagine rotta](./media/image18.png)

**Attività 2 : Confronto delle date**

Nuova operazione in /diffdates che calcola la differenza tra due date.
L'operazione deve ricevere due date come parametro nel formato
gg-MM-aaaa e restituire la differenza in giorni.

1.  Digitare il seguente commento // Nuova operazione in /diffdates che
    calcola la differenza tra due date. L'operazione deve ricevere due
    date come parametro nel formato gg-MM-aaaa e restituire la
    differenza in giorni. e premere Enter

**Nota:** Il commento si trova nel file **DemoResource.java**.
**C:\CopiolHackathon\exercisefiles\\ quarkus\\ copilot-demo\src\main\\
java\com\microsoft\hackathon\quarkus\DemoResource.java**

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image19.png)

2.  Premere TAB e di nuovo TAB per accettare il codice.

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image20.png)

3.  Aprire DemoResourceTest.java file, creare uno unit test che
    convalida l'operazione. Aggiungere //Creare uno unit test per
    convalidare /diffdates che calcola la differenza tra due date,
    quindi premere Invio.

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image21.png)

4.  Premere Tab per accettare il codice. Puoi anche utilizzare il codice
    qui sotto.

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

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image22.png)

79. Aprire il terminale ed eseguire il comando mvn test.

![Una schermata di un computer Descrizione generata
automaticamente](./media/image23.png)

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image24.png)

80. Creare il pacchetto della soluzione eseguendo il comando mvn package

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image25.png)

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image26.png)

81. Run: mvn quarkus:dev or mvn compile quarkus:dev

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image27.png)

82. Dividere il terminale ed eseguire curl -v
    http://localhost:8080/diffdates

**Attività 3 : Convalidare il formato di un telefono spagnolo**

Convalida il formato di un numero di telefono spagnolo (+34 prefisso,
poi 9 cifre, iniziando con 6, 7 o 9). L'operazione deve ricevere un
numero di telefono come parametro e restituire true se il formato è
corretto, false in caso contrario.

1.  Digitare //Convalidar il formato di un numero di telefono spagnolo
    (+34 prefisso, poi 9 cifre, iniziando con 6, 7 o 9). L'operazione
    dovrebbe ricevere un numero di telefono come parametro e restituire
    true se il formato è corretto, false altrimenti e premere Invio.
    Premere Tab per accettare il codice di suggerimento Coilot.

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image28.png)

2.  Digitare // scrivere unit test per convalidare il formato di un
    numero di telefono spagnolo (+34 prefisso, poi 9 cifre, iniziando
    con 6, 7 o 9). L'operazione dovrebbe ricevere un numero di telefono
    come parametro e restituire true se il formato è corretto, false
    altrimenti e premere Enter. Premere Tab per accettare i test unitari
    suggeriti da copilot

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image29.png)

3.  Aprire il terminale ed eseguire il test mvn.

![Una schermata di un computer Descrizione generata
automaticamente](./media/image30.png)

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image31.png)

4.  Run mvn package

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image32.png)

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image33.png)

5.  Run mvn quarkus:dev

![Uno screenshot dello schermo di un computer Descrizione generata
automaticamente](./media/image34.png)

6.  Fare clic su Split Terminal ed eseguire in uno dei terminali -

curl -v http://localhost:8080/validatephone?phone=+34866666666

curl -v http://localhost:8080/validatephone?phone=+34666666667

curl -v http://localhost:8080/validatephone?phone=+34666666666

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image35.png)

**Attività 4 : Convalidare il formato di un DNI spagnolo**

Convalidare il formato di un DNI spagnolo (8 cifre e 1 lettera).
L'operazione deve ricevere un DNI come parametro e restituire true se il
formato è corretto, false in caso contrario.

1.  Digitare // Convalidare il formato di un DNI spagnolo (8 cifre e 1
    lettera). L'operazione deve ricevere un DNI come parametro e
    restituire true se il formato è corretto, false in caso contrario e
    premere Invio. Premere Tab per accettare il codice suggerito da
    Copilot.

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image36.png)

2.  Passare a **CopilotDemoApplicationTests.java**. Per scrivere un test
    unitario per testare la funzione precedente, aggiungere //Scrivere
    test unitario per convalidare il formato di un DNI spagnolo (8 cifre
    e 1 lettera). L'operazione deve ricevere un DNI come parametro e
    restituire true se il formato è corretto, false in caso
    contrario. Premere Enter. Premere Tab per accettare il codice.

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image37.png)

3.  Aprire il terminale ed eseguire il test mvn

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image38.png)

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image39.png)

4.  Run mvn package

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image40.png)

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image41.png)

5.  Run: mvn quarkus:dev

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image42.png)

6.  Test: curl -v http://localhost:8080/hello/validatedni?dni=12345678A

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image43.png)

**Attività 5: Dal nome del colore al codice esadecimale**

In base al file colors.json esistente in resources, dato il nome del
colore come parametro di percorso, restituire il codice esadecimale. Se
il colore non viene trovato, restituire 404

Suggerimento: Utilizzare TDD. Iniziare creando lo unit test e quindi
implementare il codice.

1.  Digitare // In base al file colors.json esistente in risorse, dato
    il nome del colore come parametro di percorso, restituisci il codice
    esadecimale. Se il colore non viene trovato, restituire 404. e
    premere Enter. Premere Tab per accettare il codice suggerito da
    Copilot.

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image44.png)

2.  Passa a **CopilotDemoApplicationTests.java**. Per scrivere uno unit
    test per testare la funzione precedente, aggiungere //Write unit
    test a In base al file colors.json esistente in risorse, dato il
    nome del colore come parametro path, restituire il codice
    esadecimale. Se il colore non viene trovato, restituire 404. Premere
    Enter. Premere Tab per accettare il codice.

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image45.png)

3.  Run mvn test

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image46.png)

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image47.png)

4.  Run mvn package

![Uno screenshot di un computer Descrizione generata
automaticamente](./media/image48.png)

5.  Run: mvn quarkus:dev

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image49.png)

6.  Test: curl -v http://localhost:8080/hello/color?color=red

![Immagine rotta](./media/image50.png)

**Compito 6 : Jokes creator**

Creare una nuova operazione che chiami l'API
https://api.chucknorris.io/jokes/random e restituisca lo scherzo.

1.  Digitare // Creare una nuova operazione che chiami l'API
    https://api.chucknorris.io/jokes/random e restituisca lo scherzo. e
    premere Invio. Premere Tab per accettare il codice suggerito da
    Copilot.

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image51.png)

2.  Premere Tab per accettare il codice

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image52.png)

3.  Passare a **CopilotDemoApplicationTests.java**. Per scrivere uno
    unit test per testare la funzione precedente, aggiungere //Creare
    una nuova operazione che chiama l'API
    \[\<u\>https://api.chucknorris.io/jokes/random\</u\>\](https://api.chucknorris.io/jokes/random)
    e restituire lo scherzo. Premere Enter. Premere la scheda per
    accettare il codice.

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image53.png)

4.  Premere Tab per accettare il codice.

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image54.png)

5.  Fare clic su Terminal -\> New Terminal -\> Gitbash ed eseguire i
    comandi seguenti

cd exercisefiles/quarkus/copilot-demo/

mvn test

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image55.png)

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image56.png)

6.  Eseguire il pacchetto mvn per creare il pacchetto dell'applicazione.

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image57.png)

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image58.png)

7.  Run: mvn quarkus:dev

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image59.png)

8.  Test: curl -v http://localhost:8080/hello/joke

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image60.png)

**Attività 7 : Analisi degli URL**

Dato un url come parametro di query, analizzarlo e restituire il
protocollo, l'host, la porta, il percorso e i parametri di query. La
risposta deve essere in formato Json.

1.  Digitare //Dato un url come parametro di query, analizzalo e
    restituisci il protocollo, l'host, la porta, il percorso e i
    parametri di query. La risposta deve essere in formato Json. e
    premere Invio. Premere Tab per accettare il codice suggerito da
    Copilot.

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image61.png)

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image62.png)

2.  Passare a **CopilotDemoApplicationTests.java**. Per scrivere un test
    unitario per testare la funzione precedente, aggiungere //Write unit
    test per Dato un URL come parametro di query, analizzarlo e
    restituire i parametri di protocollo, host, porta, percorso e query.
    La risposta deve essere in formato Json. Premere Enter. Premere la
    scheda per accettare il codice.

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image63.png)

3.  Run mvn test

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image64.png)

![Uno screenshot di un computer Descrizione generata
automaticamente](./media/image65.png)

4.  Eseguire il pacchetto mvn per creare il pacchetto dell'applicazione.

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image66.png)

5.  Run mvn quarkus:dev

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image67.png)

6.  Fare clic su split terminal ed eseguire curl -v
    http://localhost:8080/hello/parseurl?url=https://www.google.com/search?q=quarkus

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image68.png)

**Attività 9: Conteggio delle parole**

Dato il percorso di un file e contare il numero di occorrenze di una
parola fornita. Il percorso e la parola devono essere parametri di
query. La risposta deve essere in formato Json.

1.  Digitare //Dato il percorso di un file e conta il numero di
    occorrenze di una parola fornita. Il percorso e la parola devono
    essere parametri di query. La risposta deve essere in formato
    Json. e premere Invio. Premere Tab per accettare il codice suggerito
    da Copilot.

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image69.png)

2.  Passa a **CopilotDemoApplicationTests.java**. Per scrivere un test
    unitario per testare la funzione precedente, aggiungere //Scrivi
    test unitario a Dato il percorso di un file e contare il numero di
    occorrenze di una parola fornita. Il percorso e la parola devono
    essere parametri di query. La risposta deve essere in formato
    Json. Premere Enter. Premere la scheda per accettare il codice.

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image70.png)

3.  Aprire **Terminal **ed eseguire il test mvn

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image71.png)

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image72.png)

4.  Eseguire il pacchetto mvn per creare il pacchetto dell'applicazione.

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image73.png)

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image74.png)

5.  Run: mvn quarkus:dev

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image75.png)

6.  Test: curl \<http://localhost:8080/hello/countword?path=/tmp/test.txt&word=hello

Puoi chiedere a GitHub copilot il comando curl per il vostro progetto.

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image76.png)

**Attività 10: Containerizzare l'applicazione**

Usare il Dockerfile fornito per creare un'immagine docker
dell'applicazione. In questo caso, viene fornito il contenuto completo,
ma per creare, eseguire e testare l'immagine docker, utilizzerai anche
Copilot per generare i comandi.

Ho creato un file DOCKER.md dove documenteremo i passaggi per costruire
l'applicazione (nativa), costruire l'immagine del container, eseguire il
container e testare il container.

1.  Nel codice di Visual Studio, premere **Ctrl +Shit + X** Cercare
    **Docker** e installarlo.

![Uno screenshot di un computer Descrizione generata
automaticamente](./media/image77.png)

2.  Fare doppio clic su **Desktop Docker** e accedere con il vostro
    account Docker.

![Immagine rotta](./media/image78.png)

3.  Premere **Ctrl + Alt + I** per aprire **Github Copilot chat**.
    Chiedere al Copilot come creare l'immagine del container, eseguire
    il container e testare il container con il Dockerfile fornito

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image79.png)

4.  Seguire le istruzioni di Copilot. Costruire l'applicazione: Eseguire
    il seguente comando nel vostro terminale:

./mvnw package -Pnative -Dquarkus.native.container-build=true

![Uno screenshot di un computer Descrizione generata
automaticamente](./media/image77.png)

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image80.png)

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image81.png)

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image82.png)

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image83.png)

5.  **Compilare l'immagine Docker:** Supponendo che il Dockerfile sia
    denominato **Dockerfile.native-micro**, è possibile utilizzare il
    comando seguente:

docker build -f Dockerfile.native-micro -t my-app .

![Una schermata del computer di un programma Descrizione generata
automaticamente](./media/image84.png)

6.  Questo comando indica a Docker di creare un'immagine utilizzando il
    Dockerfile denominato 'Dockerfile.native-micro' nella directory
    corrente ('.' alla fine del comando) e di contrassegnare l'immagine
    risultante con il nome 'my-app'.

7.  Eseguire l'immagine Docker: dopo aver creato l'immagine, è possibile
    eseguirla con il comando 'docker run':

docker run -p 8080:8080 my-app

![Immagine rotta](./media/image85.png)

Questo comando indica a Docker di eseguire un container dall'immagine
'my-app' e di mappare la porta 8080 nel container alla porta 8080 nel
computer host.

1.  **Testare l'applicazione**: Infine, per verificare se la vostra
    applicazione funziona correttamente, puoi inviare una richiesta a
    http://localhost:8080 nel vostro browser o utilizzando uno strumento
    come curl:

curl http://localhost:8080

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image86.png)

Questo comando invia una richiesta GET all'applicazione e stampa la
risposta. Se l'applicazione viene eseguita correttamente, dovrebbe
essere visualizzata la risposta prevista.

Tenere presente che questi comandi devono essere eseguiti nel vostro
terminale, non all'interno del codice dell'applicazione Java.
