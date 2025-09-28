**Laboratoire 18 - Création d'une API REST à l'aide de Spring Boot à
l'aide de GitHub Copilot**

**But**

L'objectif de cet atelier est d'apprendre à utiliser GitHub Copilot, à
l'aide d'un exercice qui consiste à créer une API REST à l'aide de
Spring Boot.

Nous avons créé un projet Spring Boot avec certains fichiers déjà créés,
vous pouvez trouver le projet dans le dossier
**C :\CopilotHackathon\exercisefiles\springboot**.

Avant d'exécuter cet atelier, nous allons d'abord installer les packages
logiciels nécessaires et configurer l'environnement.

Tâche 0 : Installation et configuration de l'environnement

Vous devez télécharger et installer les packages logiciels suivants pour
configurer l'environnement afin d'exécuter cet atelier.

un. Microsoft JDK 17

B. Apache Maven

1.  Ouvrez le navigateur Edge.

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image1.jpeg)

2.  Dans le champ URL du navigateur, copiez-collez le lien pour
    télécharger les packages logiciels sur la machine virtuelle de votre
    laboratoire.

a\. Microsoft JDK 17 ◊
https://aka.ms/download-jdk/microsoft-jdk-17.0.12-windows-x64.msi

b\. apache Maven
◊https://dlcdn.apache.org/maven/maven-3/3.9.9/binaries/apache-maven-3.9.9-bin.zip

**Remarque :** Répétez les mêmes étapes pour télécharger également tous
les autres packages. Par défaut, les packages seront enregistrés dans le
dossier des téléchargements.

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image2.jpeg)

un. **Installer Microsoft JDK 17**

1.  Dans le dossier **Downloads** (**C :\Users\Admin\Downloads**) et
    double-cliquez sur **Microsoft JDK**

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image3.jpeg)

2.  Cliquez sur **Next**.

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image4.jpeg)

3.  Acceptez EULA et cliquez sur **Next**.

![Une capture d'écran d'un contrat logiciel Le contenu généré par l'IA
peut être incorrect.](./media/image5.jpeg)

4.  Sélectionnez **Install just for you (Admin)** et cliquez sur
    **Next**.

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image6.jpeg)

5.  Dans l' écran de **Custom setup**, vous allez maintenant **set the
    JAVA_HOME variable**. Cliquez sur la flèche vers le bas et
    sélectionnez **Entire feature will be installed on local hard
    drive**.

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image7.jpeg)

6.  Cliquez sur **Next**.

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image8.jpeg)

7.  Cliquez sur **Install**.

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image9.jpeg)

**b. Installer apache-maven**

8.  Accédez au dossier **Downloads (C:\Users\Admin\Downloads)**

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image10.jpeg)

9.  Faites un clic droit sur **apache-maven-3.9.9-bin.zip** dossier et
    sélectionnez **Extract All**.

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image11.jpeg)

10. Dans la page "**Select a destination**", entrez la destination
    C** :\Users\Admin\Downloads** et cliquez sur **Extract**.

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image12.jpeg)

11. Les fichiers extraits seront comme indiqué dans la capture d'écran.

**Remarque :** Assurez-vous que le dossier est renommé
**apache-maven-3.9.9**, si vous voyez un autre nom.

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image13.jpeg)

**Configuration des variables d'environnement**

12. Cliquez sur **Windows logo** et sélectionnez **Settings**

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image14.jpeg)

13. Recherchez Modifier le système dans la page **Windows settings** et
    sélectionnez **Edit System Environment variable**.

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image15.jpeg)

14. Cliquez sur le bouton **Environment Variable**.

![Une capture d'écran d'un programme informatique Le contenu généré par
l'IA peut être incorrect.](./media/image16.jpeg)

15. Cliquez sur **New** sous la section **User variable for Admin**.

![Une capture d'écran d'un programme informatique Le contenu généré par
l'IA peut être incorrect.](./media/image17.jpeg)

16. Vous allez maintenant configurer les variables d'environnement et de
    chemin d'accès pour Maven.

Sélectionnez **New** sous la section **User variable for Admin**.

![Une capture d'écran d'un programme informatique Le contenu généré par
l'IA peut être incorrect.](./media/image18.jpeg)

17. Dans la fenêtre **New User Variable**, entrez ce qui suit et cliquez
    sur **OK**

Variable name: MAVEN_HOME

Variable value: C:\Users\Admin\Downloads\apache-maven-3.9.9

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image19.jpeg)

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image20.jpeg)

18. Sélectionnez maintenant **Path** d'accès et cliquez sur **Edit**

![Une capture d'écran d'un programme informatique Le contenu généré par
l'IA peut être incorrect.](./media/image21.jpeg)

19. Dans la fenêtre **Edit environment variable**, cliquez sur **New**.

![Une capture d'écran d'un programme informatique Le contenu généré par
l'IA peut être incorrect.](./media/image22.jpeg)

20. Dans le champ vide, entrez le %MAVEN_HOME %\bin suivant et cliquez
    sur **OK.**

![Une capture d'écran d'un programme informatique Le contenu généré par
l'IA peut être incorrect.](./media/image23.jpeg)

![Une capture d'écran d'un programme informatique Le contenu généré par
l'IA peut être incorrect.](./media/image24.jpeg)

21. Cliquez sur **OK** pour terminer la configuration de l'environnement
    utilisateur et des variables de chemin d'accès pour Maven.

![Une capture d'écran d'un programme informatique Le contenu généré par
l'IA peut être incorrect.](./media/image25.jpeg)

22. Vous allez maintenant configurer les **variables système** **(System
    variables)** pour Maven. Sélectionnez **New** dans la section
    **System variables**.

![Une capture d'écran d'un programme informatique Le contenu généré par
l'IA peut être incorrect.](./media/image26.jpeg)

23. Dans la fenêtre Nouvelle variable système, entrez ce qui suit et
    cliquez sur **OK**

Variable name: MAVEN_HOME

Variable value: C:\Users\Admin\Downloads\apache-maven-3.9.9

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image27.jpeg)

Tâche 1 : Créer le code pour gérer une simple requête GET

Passez au fichier 'DemoController.java' et commencez à écrire le code
pour gérer une simple requête GET. Dans ce premier exercice, nous avons
fourni un commentaire qui décrit le code que vous devez générer. Appuyez
simplement sur Entrée et attendez quelques secondes, Copilot générera le
code pour vous.

Il existe déjà un test unitaire implémenté pour cet exercice, vous
pouvez l'exécuter à l'aide de la commande mvn test avant et après pour
valider que le code généré par Copilot est correct.

Ensuite, créez un nouveau test unitaire pour le cas où aucune clé n'est
fournie dans la demande.

Après chaque exercice, n'hésitez pas à empaqueter et à exécuter votre
application pour la tester.

Package: mvn package

Run: mvn spring-boot:run

Test: curl -v http://localhost:8080/hello?key=world

1.  Ouvrez l'Explorateur de fichiers, développez Local Disk (C :) et
    développez le dossier **CopilotHackathon-\>exercisefiles \>
    Springboot \> copilot-demo \>
    src\>main\>java\>com\>Microsoft\>hackathon\>copilotdemo\>controller**
    pour afficher le fichier **DemoController.java**.

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image28.jpeg)

Double-cliquez **DemoController.java** fichier. Dans ce premier
exercice, seul un commentaire décrivant le code que vous devez générer
est fourni.

![Une capture d'écran d'un ordinateur Description générée
automatiquement](./media/image29.png)

2.  Prenez le curseur à la fin du commentaire (ligne 12), appuyez
    simplement sur Entrée et attendez quelques secondes, **Copilot**
    générera le code pour vous. Appuyez sur l'onglet jusqu'à ce qu'il
    vous donne le code complet.

Vous pouvez également appuyer sur Ctrl + Entrée pour choisir les options
de code.

![Une capture d'écran d'un ordinateur Description générée
automatiquement](./media/image30.png)

![Une capture d'écran d'un ordinateur Description générée
automatiquement](./media/image31.png)

3.  Développez le dossier **test** et cliquez sur
    **CopilotDemoApplicationTests.java.** Le test unitaire vous est déjà
    remis.

![Une capture d'écran d'un écran d'ordinateur Description générée
automatiquement](./media/image32.png)

4.  Vous pouvez essayer d'exécuter le code sans mettre à jour pom xml et
    demander à Coiplot une solution pour explorer le produit.

5.  Ouvrez **Pom.xml** ajoutez le plugin ci-dessous et enregistrez le
    fichier

6.  \<plugin\>

7.  \<groupId\>org.apache.maven.plugins\</groupId\>

8.  \<artifactId\>maven-compiler-plugin\</artifactId\>

9.  \<version\>3.8.1\</version\>

10. \<configuration\>

11. \<source\>17\</source\>

12. \<target\>17\</target\>

13. \</configuration\>

\</plugin\>

![Une capture d'écran d'un programme d'ordinateur Description générée
automatiquement](./media/image33.png)

14. Cliquez sur **Terminal -\> New Terminal** dans la barre d'outils.

![BrokenImage](./media/image34.png)

15. Sélectionnez **Gitbash** et exécutez la commande ci-dessous.

cd
exercisefiles/springboot/copilot-demo/![BrokenImage](./media/image35.png)

![Une capture d'écran d'un programme d'ordinateur Description générée
automatiquement](./media/image36.png)

16. Exécutez la commande mvn clean install -DskipTests

![Capture d'écran d'un programme d'ordinateur Description générée
automatiquement](./media/image37.png)

![Une capture d'écran d'un ordinateur Description générée
automatiquement](./media/image38.png)

17. Exécutez le test mvn . Si votre build échoue avec une erreur.

![Une capture d'écran d'un programme d'ordinateur Description générée
automatiquement](./media/image39.png)

18. Cliquez sur l'icône **Copilot** dans le coin inférieur droit et
    sélectionnez **Github Copilot Chat**.

![BrokenImage](./media/image40.png)

19. Demandez au chat Github Copilot de vous fournir un correctif pour
    votre erreur.

![Une capture d'écran d'un écran d'ordinateur Description générée
automatiquement](./media/image41.png)

20. Regardez le chat Copilot expliquant le problème et la solution
    correspondante. Si vous n'êtes toujours pas clair avec le correctif,
    continuez à poser vos doutes et Copilot vous répondra . Lisez et
    comprenez l'erreur et la solution à mettre en œuvre.

![Une capture d'écran d'un programme d'ordinateur Description générée
automatiquement](./media/image42.png)

21. Fournissez la méthode /hello à Copilot et voyons ce qu'elle va
    suggérer.

![BrokenImage](./media/image43.png)

22. Retournez à **CopilotDemoApplicationTests.java** Prenez le curseur à
    la fin du test (ligne 24) et appuyez sur Entrée. Copilot génère un
    autre test pour vous. Appuyez sur l'onglet pour l'accepter.

![Une capture d'écran d'un programme d'ordinateur Description générée
automatiquement](./media/image44.png)

23. Fournissez la méthode /hello du test au Copilot et voyez ce qu'elle
    suggère.

![Une capture d'écran d'un ordinateur Description générée
automatiquement](./media/image45.png)

24. Réexécutez le test mvn Votre code peut ressembler à ce qui suit.
    Vous pouvez également écrire votre propre code et demander à Copilot
    de le valider.

25. @RestController

26. public class DemoController {

27. @GetMapping("/hello")

28. public String hello(@RequestParam(name = "key", required = false)
    String key) {

29. if (clé == null) {

30. retour « clé non transmise » ;

31. }

32. retour « Bonjour » + touche ;

33. }

34. 

}

![Une capture d'écran d'un programme d'ordinateur Description générée
automatiquement](./media/image46.png)

35. Exécuter la commande mvn package

![Une capture d'écran d'un programme d'ordinateur Description générée
automatiquement](./media/image47.png)

![Une capture d'écran d'un programme d'ordinateur Description générée
automatiquement](./media/image48.png)

36. Exécuter mvn spring-boot :run

![Une capture d'écran d'un programme d'ordinateur Description générée
automatiquement](./media/image49.png)

37. Cliquez sur diviser le terminal et entrez curl -v
    http://localhost:8080/hello?key=world dans le 2ème terminal . Vous
    pouvez également demander à votre Copilot de fournir la commande
    curl pour tester votre code.

![BrokenImage](./media/image50.png)

38. Cliquez sur diviser le terminal et entrez curl -v
    http://localhost:8080/hello dans le 2ème terminal

![Une capture d'écran d'un programme d'ordinateur Description générée
automatiquement](./media/image51.png)

39. Appuyez sur Ctrl + C pour arrêter l'exécution du service.

Tâche 2 : Comparaison des dates

Nouvelle opération sous /diffdates qui calcule la différence entre deux
dates. L'opération doit recevoir deux dates en paramètre au format
jj-MM-aaaa et renvoyer la différence en jours.

En outre, créez un test unitaire qui valide l'opération.

Désormais, vous devrez créer les tests unitaires pour chaque nouvelle
opération. N'était-ce pas facile avec Copilot ?

1.  Allez dans **DemoController.java** et entrez l'invite //create a New
    operation sous /diffdates qui calcule la différence entre deux
    dates. L'opération doit recevoir deux dates en paramètre au format
    jj-MM-aaaa et renvoyer la différence en jours et appuyer sur Entrée.
    Attendez un certain temps et une fois que Copilot prédit le code,
    appuyez sur la touche pour accepter le code.

![BrokenImage](./media/image52.png)

2.  Vous pouvez également utiliser le code ci-dessous.

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

> }![Une capture d'écran d'un programme d'ordinateur Description générée
> automatiquement](./media/image53.png)

14. Désormais, vous devrez créer les tests unitaires pour chaque
    nouvelle opération. Utilisez Copilot pour créer.

15. Ouvrez **CopilotDemoApplicationTests.java** sous le dossier **de
    test** et entrez l'invite // create unit test to /diffdates qui
    calcule la différence entre deux dates. L'opération doit recevoir
    deux dates en paramètre au format jj-MM-aaaa et renvoyer la
    différence en jours. puis appuyez sur Entrée. Attendez une seconde
    pour que le copilote prédit le code et appuyez sur la touche de
    tabulation pour accepter le code prédit.

16. Vous pouvez entrer et appuyer sur la touche de tabulation pour créer
    plusieurs tests unitaires

![Capture d'écran d'ordinateur d'un programme Description générée
automatiquement](./media/image54.png)

![Une capture d'écran d'un programme d'ordinateur Description générée
automatiquement](./media/image55.png)

17. Prenez l'aide du chat Copilot pour les problèmes à résoudre ou pour
    expliquer le unittest et mettre à jour le code si nécessaire en
    fonction des entrées Copilot.

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

![Une capture d'écran d'un programme d'ordinateur Description générée
automatiquement](./media/image56.png)

35. Ouvrez **Terminal -\>Gitbash** et exécutez les commandes ci-dessous

cd "exercisefiles\springboot\copilot-demo"

mvn test ![BrokenImage](./media/image57.png)

36. Si vous voyez des erreurs de compilation, copiez le message d'erreur
    et demandez le correctif à Copilot.

![BrokenImage](./media/image58.png)

37. Copilot vous propose d'importer des packages avec du code. Ajoutez
    la commande à votre code et exécutez mvn test

![Une capture d'écran d'un programme d'ordinateur Description générée
automatiquement](./media/image59.png)

![Une capture d'écran d'un programme d'ordinateur Description générée
automatiquement](./media/image60.png)

![Une capture d'écran d'un programme d'ordinateur Description générée
automatiquement](./media/image61.png)

38. Exécuter le paquet mvn (mvn package)

![Une capture d'écran d'un programme d'ordinateur Description générée
automatiquement](./media/image62.png)

![Une capture d'écran d'un programme d'ordinateur Description générée
automatiquement](./media/image63.png)

39. Exécutez le test mvn -Dtest=CopilotDemoApplicationTests#diffdates
    test

![Une capture d'écran d'un programme d'ordinateur Description générée
automatiquement](./media/image64.png)

40. Exécuter mvn spring-boot :run

![Capture d'écran d'un programme d'ordinateur Description générée
automatiquement](./media/image65.png)

41. Cliquez sur Split terminal et exécutez curl -v
    http://localhost:8080/diffdates?date1=01-01-2021&date2=01-02-2021

Une erreur s'affiche. Prenez l'aide de Copilot et résolvez le petit
problème.

![Une capture d'écran d'un écran d'ordinateur Description générée
automatiquement](./media/image66.png)

42. En tant que Copilot Chat pour vous aider avec la commande de boucle
    . Copiez simplement le message d'erreur en le collant dans le chat.
    Copilot vous donne la commande modifiée avec une explication

![Une capture d'écran d'un programme d'ordinateur Description générée
automatiquement](./media/image67.png)

Tâche 3 : Valider le format d'un téléphone espagnol

Validez le format d'un numéro de téléphone espagnol (+34 préfixes, puis
9 chiffres, commençant par 6, 7 ou 9) (// Validate the format of a
spanish phone number (+34 prefix, then 9 digits, starting with 6, 7 or
9)). L'opération doit recevoir un numéro de téléphone en paramètre et
retourner true si le format est correct, false dans le cas contraire.

1.  Ouvrez DemoController.Java et entrez l'invite // Validate the format
    of a spanish phone number (+34 prefix, then 9 digits, starting with
    6, 7 or 9). L'opération doit recevoir un numéro de téléphone en
    paramètre et retourner true si le format est correct, false dans le
    cas contraire. . Appuyez sur la touche pour accepter le code.

![Capture d'écran d'un programme d'ordinateur Description générée
automatiquement](./media/image68.png)

2.  Vous pouvez également utiliser le code ci-dessous.

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

11. Passez à **CopilotDemoApplicationTests.java**. Pour écrire un test
    unitaire pour tester la fonction ci-dessus, ajoutez //Write unit
    test to validate the format of a spanish phone number (+34 prefix,
    then 9 digits, starting with 6, 7 or 9). L'opération doit recevoir
    un numéro de téléphone en paramètre et retourner true si le format
    est correct, false sinon Appuyez sur Entrée. Appuyez sur l'onglet
    pour accepter le code.

![Capture d'écran d'ordinateur d'un programme Description générée
automatiquement](./media/image69.png)

12. Vous pouvez également utiliser les tests unitaires ci-dessous ou
    écrire vos propres tests unitaires.

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

42. Ouvrez **Terminal -\>Gitbash** et exécutez les commandes ci-dessous.

cd exercisefiles/springboot/copilot-demo/

mvn test

![Une capture d'écran d'un programme d'ordinateur Description générée
automatiquement](./media/image70.png)

43. Exécuter mvn package

![Une capture d'écran d'un programme d'ordinateur Description générée
automatiquement](./media/image71.png)

44. Exécuter mvn spring-boot:run

![Une capture d'écran d'un programme d'ordinateur Description générée
automatiquement](./media/image72.png)

45. Divisez le terminal et exécutez les commandes curl ci-dessous pour
    valider les numéros de téléphone.

curl -v http://localhost:8080/validatephone?phone=+34866666666

curl -v http://localhost:8080/validatephone?phone=+34666666667

curl -v http://localhost:8080/validatephone?phone=+34666666666![Une
capture d'écran d'un écran d'ordinateur Description générée
automatiquement](./media/image73.png)

Tâche 4 : Valider le format d'un DNI espagnol

Validez le format d'une carte d'identité espagnole (8 chiffres et 1
lettre). L'opération doit recevoir un DNI en paramètre et retourner true
si le format est correct, false dans le cas contraire.

1.  Ouvrez DemoController.Java et entrez l'invite // Validez le format
    d'un DNI espagnol (8 chiffres et 1 lettre). L'opération doit
    recevoir un DNI en paramètre et retourner true si le format est
    correct, false dans le cas contraire. . Appuyez sur l'onglet pour
    accepter le code.

![Capture d'écran d'un programme d'ordinateur Description générée
automatiquement](./media/image74.png)

2.  Vous pouvez également utiliser le code ci-dessous

3.  Validez le format d'une carte d'identité espagnole (8 chiffres et 1
    lettre). L'opération doit recevoir un DNI en paramètre et retourner
    true si le format est correct, false dans le cas contraire.

4.  @GetMapping(« /validatedni »)

5.  public booléen validatedni(@RequestParam(name = « dni », required =
    false) Chaîne dni) {

6.  if (days == null || days.isEmpty()) {

7.  return false ;

8.  }

9.  String regex = "^\\d{8}\[A-Z\]$";

10. retour dni.matches(regex) ;

}

11. Passez à **CopilotDemoApplicationTests.java**. Pour écrire un test
    unitaire pour tester la fonction ci-dessus, ajoutez //Write test
    unitaire pour valider le format d'un DNI espagnol (8 chiffres et 1
    lettre). L'opération doit recevoir un DNI en paramètre et retourner
    true si le format est correct, false sinon Appuyez sur Entrée.
    Appuyez sur la tabulation pour accepter le code.

![Une capture d'écran d'un programme d'ordinateur Description générée
automatiquement](./media/image75.png)

12. Vous pouvez également utiliser le test unitaire ci-dessous ou écrire
    vos propres tests unitaires.

@Test

void validatedniNoDni() throws Exception {

mockMvc.perform(MockMvcRequestBuilders.get("/validatedni"))

.andExpect(MockMvcResultMatchers.status().isOk())

.andExpect(MockMvcResultMatchers.content().string("false"));

}

Open Terminal -\> Gitbash and run the below commands.

cd exercisefiles/springboot/copilot-demo/

mvn test

![Une capture d'écran d'un programme d'ordinateur Description générée
automatiquement](./media/image76.png)

![Une capture d'écran d'un programme d'ordinateur Description générée
automatiquement](./media/image77.png)

13. Exécuter mvn package ![Une capture d'écran d'un programme
    d'ordinateur Description générée
    automatiquement](./media/image78.png)

![Une capture d'écran d'un programme d'ordinateur Description générée
automatiquement](./media/image79.png)

14. Exécuter mvn spring-boot :run

![Une capture d'écran d'un programme d'ordinateur Description générée
automatiquement](./media/image80.png)

15. Divisez le terminal et exécutez curl -v
    http://localhost:8080/validatedni?dni=12345678C in \>the 2ndterminal

![Une capture d'écran d'un programme d'ordinateur Description générée
automatiquement](./media/image81.png)

Tâche 5 : Du nom de la couleur au code hexadécimal

Sur la base du fichier colors.json existant sous les ressources, étant
donné le nom de la couleur comme paramètre de chemin, renvoie le code
hexadécimal. Si la couleur n'est pas trouvée, retournez 404

Astuce : utilisez TDD. Commencez par créer le test unitaire, puis
implémentez le code.

1.  Ouvrez DemoController.Java et entrez l'invite // Based on existing
    colors.json file under resources, given the name of the color as
    path parameter, return the hexadecimal code. Si la couleur n'est pas
    trouvée, retournez 404 . Appuyez sur l'onglet pour accepter le code.

![Capture d'écran d'un programme d'ordinateur Description générée
automatiquement](./media/image82.png)

2.  Vous pouvez également utiliser le code ci-dessous ou écrire votre
    code.

3.  Sur la base du fichier colors.json existant sous les ressources,
    étant donné le nom de la couleur comme paramètre de chemin, renvoie
    le code hexadécimal. Si la couleur n'est pas trouvée, retournez 404

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

17. Passez à **CopilotDemoApplicationTests.java**. Pour écrire un test
    unitaire afin de tester la fonction ci-dessus, ajoutez //test for
    /color/{color} endpoint. Appuyez sur Entrée. Appuyez sur la touche
    de tabulation pour accepter le code.

![Une capture d'écran d'un programme d'ordinateur Description générée
automatiquement](./media/image83.png)

18. Vous pouvez écrire vos tests unitaires. Vous pouvez toujours
    vérifier auprès de Copilot s'il y a du code/correctif/test unitaire

19. Ouvrez **Terminal -\> Gitbash** et exécutez les commandes
    ci-dessous. Vous pouvez voir des erreurs de compilation.

cd exercisefiles/springboot/copilot-demo/

mvn test

![Une capture d'écran d'un programme d'ordinateur Description générée
automatiquement](./media/image84.png)

20. Appuyez sur **Ctrl + Alt + I** pour ouvrir **Github Copilot Chat**.
    Copiez le message d'erreur et collez-le dans la fenêtre de
    discussion. Copilot suggère avec la solution.

![Une capture d'écran d'un programme d'ordinateur Description générée
automatiquement](./media/image85.png)

21. Copilot vous suggère d'importer les paquets manquants avec la
    fonction d'importation. Copiez-le et ajoutez-le à votre code.
    Appuyez sur Entrée et Copilot vous suggère d'ajouter les packages
    manquants. Appuyez sur l'onglet et acceptez-les pour les ajouter au
    code.

![Une capture d'écran d'un programme d'ordinateur Description générée
automatiquement](./media/image86.png)

![Une capture d'écran d'un ordinateur Description générée
automatiquement](./media/image87.png)

22. Ouvrez **Terminal -\> Gitbash** et exécutez à nouveau les commandes
    ci-dessous.

cd exercisefiles/springboot/copilot-demo/

mvn test

![Une capture d'écran d'un programme d'ordinateur Description générée
automatiquement](./media/image88.png)

![Une capture d'écran d'un programme d'ordinateur Description générée
automatiquement](./media/image89.png)

23. Exécuter le package mvn (mvn package) Pour empaqueter votre
    application.

![Une capture d'écran d'un programme d'ordinateur Description générée
automatiquement](./media/image90.png)

![Une capture d'écran d'un programme d'ordinateur Description générée
automatiquement](./media/image91.png)

24. Exécutez mvn spring-boot:run Pour tester

![Une capture d'écran d'un programme d'ordinateur Description générée
automatiquement](./media/image92.png)

25. Vous pouvez demander à votre copilote de vous aider avec la commande
    curl pour tester votre fonction.

![BrokenImage](./media/image93.png)

26. Cliquez sur **Split terminal** et exécutez la commande curl pour
    tester votre application.( Mettre à jour le port)

![BrokenImage](./media/image94.png)

27. Testez avec les couleurs répertoriées dans **colors.json** fichier

![Une capture d'écran d'un programme d'ordinateur Description générée
automatiquement](./media/image95.png)

28. Testez la couleur qui n'est pas répertoriée dans **colors.json** et
    voyez les résultats

![Capture d'écran d'ordinateur d'un programme Description générée
automatiquement](./media/image96.png)

Tâche 6 : Créateur de blagues

Créez une opération qui appelle l'API
https://api.chucknorris.io/jokes/random et renvoie la blague.

1.  Ouvrez DemoController.Java et entrez l'invite // new operation that
    call the API https://api.chucknorris.io/jokes/random and return the
    joke . Appuyez sur l'onglet pour accepter le code.

![Une capture d'écran d'un programme d'ordinateur Description générée
automatiquement](./media/image97.png)

![Capture d'écran d'ordinateur d'un programme Description générée
automatiquement](./media/image98.png)

2.  Vous pouvez également utiliser le code ci-dessous.

3.  nouvelle opération qui appelle l'API
    https://api.chucknorris.io/jokes/random et retourne la blague

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

![Capture d'écran d'ordinateur d'un programme Description générée
automatiquement](./media/image99.png)

18. Passez à **CopilotDemoApplicationTests.java**. Pour écrire un test
    unitaire pour tester la fonction ci-dessus, ajoutez // Create un
    test unitaire pour une nouvelle opération qui appelle l'API
    https://api.chucknorris.io/jokes/random et renvoie la blague Appuyez
    sur Entrée. Appuyez sur la touche de tabulation pour accepter le
    code.

![Une capture d'écran d'un programme d'ordinateur Description générée
automatiquement](./media/image100.png)

19. Vous pouvez également ajouter ci-dessous un test unitaire ou écrire
    vos propres tests unitaires.

20. @Test

21. void joke() throws Exception{

22. mockMvc.perform(MockMvcRequestBuilders.get("/joke"))

23. .andExpect(MockMvcResultMatchers.status().isOk())

24. // check that content is a string

25. .andExpect(MockMvcResultMatchers.content().string(Matchers.any(String.class)));

}

![Une capture d'écran d'un programme d'ordinateur Description générée
automatiquement](./media/image101.png)

26. Ouvrez Terminal -\> Gitbahs et exécutez les commandes ci-dessous.

cd exercisefiles/springboot/copilot-demo/

mvn test

![Une capture d'écran d'un programme d'ordinateur Description générée
automatiquement](./media/image101.png)

![Une capture d'écran d'un ordinateur Description générée
automatiquement](./media/image102.png)

27. Packagez votre application. Exécuter mvn package

![Une capture d'écran d'un programme d'ordinateur Description générée
automatiquement](./media/image103.png)

![Une capture d'écran d'un programme d'ordinateur Description générée
automatiquement](./media/image104.png)

28. Exécuter mvn spring-boot :run

![Une capture d'écran d'un programme d'ordinateur Description générée
automatiquement](./media/image105.png)

![BrokenImage](./media/image106.png)

29. Cliquez sur Split terminal et exécutez la commande pour : curl -v
    http://localhost:8080/joke in 2ndterminal

![Une capture d'écran d'un écran d'ordinateur Description générée
automatiquement](./media/image107.png)

Tâche 7 : Analyse d'URL

Étant donné une URL comme paramètre de requête, analysez-la et renvoyez
les paramètres de protocole, d'hôte, de port, de chemin et de requête.
La réponse doit être au format Json.

1.  Ouvrez **DemoController.Java** et entrez l'invite //écrivez un code
    pour Given a url as query parameter, parse it and return the
    protocol, host, port, path and query parameters. La réponse doit
    être au format Json . Appuyez sur l'onglet pour accepter le code.

![BrokenImage](./media/image108.png)

2.  Vous pouvez également utiliser le code ci-dessous.

3.  // Given a url as query parameter, parse it and return the protocol,
    host, port, path and query parameters. La réponse doit être au
    format Json.

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

![Capture d'écran d'ordinateur d'un programme Description générée
automatiquement](./media/image109.png)

16. Passez à **CopilotDemoApplicationTests.java**. Pour écrire un test
    unitaire pour tester la fonction ci-dessus, ajoutez // Create a unit
    test for new operation that call the API
    https://api.chucknorris.io/jokes/random and return the joke. Appuyez
    sur Entrée. Appuyez sur la touche de tabulation pour accepter le
    code.

![Une capture d'écran d'un programme d'ordinateur Description générée
automatiquement](./media/image110.png)

17. Vous pouvez également ajouter des tests unitaires ci-dessous ou
    écrire vos propres tests unitaires.

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

![Une capture d'écran d'un programme d'ordinateur Description générée
automatiquement](./media/image111.png)

33. Ouvrez **Terminal -\> Gitbash** et exécutez les commandes
    ci-dessous.

cd exercisefiles/springboot/copilot-demo/

mvn test

![Une capture d'écran d'un programme d'ordinateur Description générée
automatiquement](./media/image112.png)

![Une capture d'écran d'un programme d'ordinateur Description générée
automatiquement](./media/image113.png)

34. Exécuter mvn package Pour empaqueter votre application.

![Une capture d'écran d'un programme d'ordinateur Description générée
automatiquement](./media/image114.png)

35. Exécuter mvn spring-boot:run

![Une capture d'écran d'un programme d'ordinateur Description générée
automatiquement](./media/image115.png)

![BrokenImage](./media/image116.png)

36. Divisez le terminal et testez votre application : curl -v
    http://localhost:8080/parseurl?url=https://www.google.com/search?q=chuck+norris

![Une capture d'écran d'un écran d'ordinateur Description générée
automatiquement](./media/image117.png)

Tâche 8 : Comptage de mots

Étant donné le chemin d'accès d'un fichier et comptez le nombre
d'occurrences d'un mot fourni. Le chemin d'accès et le mot doivent être
des paramètres de requête. La réponse doit être au format Json.

1.  Ouvrez **DemoController.Java** et entrez l'invite //écrivez un code
    pour Given the path of a file and count the number of occurrences of
    a provided word. The path and the word should be query parameters.
    Le chemin d'accès et le mot doivent être des paramètres de requête.
    La réponse doit être au format Json . Appuyez sur l'onglet pour
    accepter le code.

![BrokenImage](./media/image118.png)

2.  Passez à **CopilotDemoApplicationTests.java**. Pour écrire un test
    unitaire pour tester la fonction ci-dessus, ajoutez // Étant donné
    le chemin d'un fichier et comptez le nombre d'occurrences d'un mot
    fourni. Le chemin d'accès et le mot doivent être des paramètres de
    requête. La réponse doit être au format Json. Appuyez sur Entrée.
    Appuyez sur l'onglet pour accepter le code.

![BrokenImage](./media/image119.png)

3.  Ouvrez Terminal -\> Gitbash et exécutez les commandes ci-dessous.

cd exercisefiles/springboot/copilot-demo/

mvn test![BrokenImage](./media/image120.png)

![BrokenImage](./media/image121.png)

4.  Exécutez mvn package pour empaqueter votre application/

![BrokenImage](./media/image122.png)

5.  Exécuter mvn spring-boot :run

![BrokenImage](./media/image123.png)

6.  Cliquez sur Split terminal et exécutez la commande curl pour tester
    votre application.

curl http://localhost:8080/countword?path=src/test/resources/test.txt

![BrokenImage](./media/image124.png)

Tâche 9 : Conteneuriser l'application

Utilisez le fichier Dockerfile fourni pour créer une image Docker de
l'application. Il y a quelques commentaires dans le Dockerfile qui vous
aideront à terminer l'exercice.

Afin de construire, d'exécuter et de tester l'image docker, vous pouvez
également utiliser Copilot pour générer les commandes.

Par exemple, créez un fichier DOCKER.md dans lequel vous pouvez stocker
les commandes pour générer, exécuter et tester l'image Docker. Vous
remarquerez que Copilot vous aidera également à documenter votre projet
et vos commandes.

Exemples d'étapes à documenter : Créer l'image du conteneur, Exécuter le
conteneur, Tester le conteneur.

1.  Double-cliquez sur Docker depuis Dekstop et connectez-vous avec
    votre compte.

2.  Ouvrez le fichier Docker ou le code Visual studio, ajoutez-y le code
    ci-dessous et enregistrez le fichier.

3.  \# Créer une image d'application java basée sur openjdk 17 et
    l'exécuter sur le port 8080

4.  FROM openjdk :17-jdk-alpine

5.  EXPOSE 8080

6.  COPY cible/\*.jar app.jar

ENTRYPOINT \["java","-jar","/app.jar"\]

![BrokenImage](./media/image125.png)

7.  Appuyez sur **Ctrl + Alt + I** pour ouvrir la fenêtre de discussion
    **GitHub Copilot**. Demandez à Copilot ci-dessous. Copilot fournit
    des étapes pour conteneuriser l'application.

comment créer, exécuter et tester l'image Docker avec le Dockerfile
fourni pour créer une image Docker de l'application

![BrokenImage](./media/image126.png)

8.  Suivez la 1ère étape - Créez l'image Docker. Ouvrez \*\*Terminal -\>
    Gitbash\*\* et exécutez la commande pour créer l'image Docker.

cd exercisefiles/springboot/copilot-demo/

docker build -t mon-application .

![BrokenImage](./media/image127.png)

![BrokenImage](./media/image128.png)

![Une capture d'écran d'un ordinateur Description générée
automatiquement](./media/image129.png)

9.  Une fois l'image créée, vous pouvez l'exécuter à l'aide de la
    commande docker run.

docker run -p 8080:8080 my-application

![Une capture d'écran d'un programme d'ordinateur Description générée
automatiquement](./media/image130.png)

10. Une fois que le conteneur Docker est en cours d'exécution, vous
    pouvez le tester en envoyant des requêtes à votre application.

curl \<http://localhost:8080/hello?key=world

![BrokenImage](./media/image131.png)
