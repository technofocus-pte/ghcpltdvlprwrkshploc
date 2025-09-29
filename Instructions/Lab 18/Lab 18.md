**Laboratório 18 - Crie uma REST API usando Spring Boot com a ajuda do
GitHub Copilot**

**Objetivo**

O objetivo deste laboratório é aprender a usar o GitHub Copilot, usando
um exercício que consiste em criar uma REST API usando Spring Boot.

Criamos um projeto Spring Boot com alguns arquivos já criados. Você pode
encontrar o projeto na pasta
**C:\CopilotHackathon\exercisefiles\springboot**.

Antes de executar este laboratório, vamos primeiro instalar os pacotes
de software necessários e configurar o ambiente.

Tarefa 0: Instalar e configurar o ambiente

Você precisa baixar e instalar os seguintes pacotes de software para
configurar o ambiente para executar este laboratório.

a\. Microsoft JDK 17

b\. apache maven

1.  Abra o navegador Edge.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image1.jpeg)

2.  No campo URL do navegador, copie e cole o link para baixar os
    pacotes de software para a VM do seu laboratório.

a\. Microsoft JDK 17
◊ https://aka.ms/download-jdk/microsoft-jdk-17.0.12-windows-x64.msi

b\. apache maven
◊https://dlcdn.apache.org/maven/maven-3/3.9.9/binaries/apache-maven-3.9.9-bin.zip

**Observação:** repita os mesmos passos para baixar todos os outros
pacotes também. Por padrão, os pacotes serão salvos na pasta de
downloads.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image2.jpeg)

a. **Install Microsoft JDK 17**

1.  Na pasta **Downloads** (**C:\Users\Admin\Downloads**), clique duas
    vezes em **Microsoft JDK**

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image3.jpeg)

2.  Clique **Next**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image4.jpeg)

3.  Aceite o EULA e clique em **Next**.

![A screenshot of a software agreement AI-generated content may be
incorrect.](./media/image5.jpeg)

4.  Selecione **Install just for you (Admin)** e clique em **Next**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image6.jpeg)

5.  Na tela **Custom setup**, você agora **set the JAVA_HOME variable**.
    Clique na seta para baixo e selecione **Entire feature will be
    installed on local hard drive**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image7.jpeg)

6.  Clique em **Next**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image8.jpeg)

7.  Clique em **Install**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image9.jpeg)

**b. Install apache- maven**

8.  Navegue até a pasta **Downloads** (**C:\Users\Admin\Downloads**)

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image10.jpeg)

9.  Clique com o botão direito do mouse na pasta
    **apache-maven-3.9.9-bin.zip** e selecione **Extract All**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image11.jpeg)

10. Na página “ **Select a destination**”, insira o destino
    como **C:\Users\Admin\Downloads** e clique em **Extract**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image12.jpeg)

11. Os arquivos extraídos serão exibidos conforme mostrado na captura de
    tela.

**Observação:** certifique-se de que a pasta seja renomeada
como **apache-maven-3.9.9**, caso você observe qualquer outro nome.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image13.jpeg)

**Configurar variáveis ambientais**

12. Clique no **logotipo do Windows** e selecione **Settings**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image14.jpeg)

13. Na página **Settings** **do Windows**, pesquise por **Edit system**
    e selecione **Edit System Environment variable**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image15.jpeg)

14. Clique no botão **Environment Variable**.

![A screenshot of a computer program AI-generated content may be
incorrect.](./media/image16.jpeg)

15. Clique em **New** na seção **User variable for Admin**.

![A screenshot of a computer program AI-generated content may be
incorrect.](./media/image17.jpeg)

16. Agora você irá configurar as variáveis de ambiente e de caminho para
    o Maven.

**Selecione** **New** na seção **User variable for Admin**.

![A screenshot of a computer program AI-generated content may be
incorrect.](./media/image18.jpeg)

17. Na janela **New User Variable**, insira o seguinte e clique em
    **OK**

Variable name: MAVEN_HOME

Variable value: C:\Users\Admin\Downloads\apache-maven-3.9.9

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image19.jpeg)

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image20.jpeg)

18. Agora selecione **Path** e clique em **Edit**.

![A screenshot of a computer program AI-generated content may be
incorrect.](./media/image21.jpeg)

19. Na janela **Edit environment variable**, clique em **New**.

![A screenshot of a computer program AI-generated content may be
incorrect.](./media/image22.jpeg)

20. No campo vazio, insira %MAVEN_HOME%\bin e clique em **OK**.

![A screenshot of a computer program AI-generated content may be
incorrect.](./media/image23.jpeg)

![A screenshot of a computer program AI-generated content may be
incorrect.](./media/image24.jpeg)

21. Clique em **OK** para concluir a configuração das variáveis de
    ambiente e de caminho do usuário para o Maven.

![A screenshot of a computer program AI-generated content may be
incorrect.](./media/image25.jpeg)

22. Agora você irá configurar as **System variables** para o Maven.
    Selecione **New** na seção **System variables**.

![A screenshot of a computer program AI-generated content may be
incorrect.](./media/image26.jpeg)

23. Na janela New System Variable, insira o seguinte e clique em **OK**

Variable name: MAVEN_HOME

Variable value: C:\Users\Admin\Downloads\apache-maven-3.9.9

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image27.jpeg)

Tarefa 1: Criar o código para lidar com uma requisição GET simples

Mova para o arquivo 'DemoController.java' e comece a escrever o código
para lidar com uma requisição GET simples. Neste primeiro exercício, já
fornecemos um comentário que descreve o código que você precisa gerar.
Basta pressionar Enter e aguardar alguns segundos; o Copilot irá gerar o
código para você.

Já existe um teste de unidade implementado para este exercício. Você
pode executá-lo usando o comando: mvn test antes e depois, para validar
que o código gerado pelo Copilot está correto.

Em seguida, crie um novo teste de unidade para o caso em que nenhuma
chave seja fornecida na requisição.

Após cada exercício, sinta-se à vontade para criar um pacote e executar
seu aplicativo para testá-lo.

Pacote: mvn package

Execute: mvn spring-boot:run

Teste: curl -v http://localhost:8080/hello?key=world

1.  Abra o File Explorer, expanda Local Disk (C:) e navegue
    até **CopilotHackathon-\>exercisefiles \> Springboot \> copilot-demo
    \>
    src\>main\>java\>com\>Microsoft\>hackathon\>copilotdemo\>controller** para
    visualizar o arquivo **'DemoController.java**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image28.jpeg)

Clique duas vezes no arquivo **DemoController.java**. Neste primeiro
exercício, é fornecido apenas um comentário que descreve o código que
você precisa gerar.

![A screenshot of a computer Description automatically
generated](./media/image29.png)

2.  Leve o cursor até o final do comentário (linha 12), pressione Enter
    e aguarde alguns segundos; o **Copilot** irá gerar o código para
    você. Pressione a tecla Tab até que seja exibido o código completo.

Você também pode pressionar Ctrl + Enter para escolher opções de código.

![A screenshot of a computer Description automatically
generated](./media/image30.png)

![A screenshot of a computer Description automatically
generated](./media/image31.png)

3.  Expanda a pasta **test** e clique em
    **CopilotDemoApplicationTests.java**. O teste de unidade já está
    fornecido para você.

![A screenshot of a computer screen Description automatically
generated](./media/image32.png)

4.  Você pode tentar executar o código sem atualizar o arquivo pom.xml e
    pedir ao Copilot uma solução para explorar o produto.

5.  Abra o arquivo **pom.xml**, adicione o plugin abaixo e salve o
    arquivo.

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

14. Clique em **Terminal -\> New Terminal** na barra de ferramentas.

![BrokenImage](./media/image34.png)

15. Selecione **Git Bash** e execute o comando abaixo.

cd exercisefiles/springboot/copilot-demo/

![BrokenImage](./media/image35.png)

![A screenshot of a computer program Description automatically
generated](./media/image36.png)

16. Execute o comando mvn clean install -DskipTests 

![A screenshot of a computer Description automatically
generated](./media/image37.png)

17. Execute mvn test. Se a sua compilação falhar com erro.

![A screenshot of a computer program Description automatically
generated](./media/image38.png)

18. Clique no ícone **Copilot** no canto inferior direito e selecione
    **Github Copilot Chat.**

![BrokenImage](./media/image39.png)

19. Peça ao chat do Github Copilot para fornecer uma correção para o seu
    erro.

![A screenshot of a computer screen Description automatically
generated](./media/image40.png)

20. Consulte o chat do Copilot explicando o problema e a correção
    correspondente. Se ainda não estiver claro com a correção, continue
    perguntando suas dúvidas e o Copilot responderá. Leia e entenda o
    erro e a solução a ser implementada.

![A screenshot of a computer program Description automatically
generated](./media/image41.png)

21. Forneça o método //hello ao Copilot e vamos ver o que ele irá
    sugerir.

![BrokenImage](./media/image42.png)

22. Volte para **CopilotDemoApplicationTests.java.** Coloque o cursor no
    final do teste (linha 24) e pressione Enter. O Copilot gera outro
    teste para você. Pressione a tecla Tab para aceitá-lo.

![A screenshot of a computer program Description automatically
generated](./media/image43.png)

23. Forneça o método /hello do teste para o Copilot e veja o que ele irá
    sugerir.

![A screenshot of a computer Description automatically
generated](./media/image44.png)

24. Execute novamente o comando mvn test Seu código pode se parecer com
    o exemplo abaixo. Você também pode escrever o seu próprio código e
    pedir ao Copilot para validar.

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
generated](./media/image45.png)

35. Execute o comando mvn package

![A screenshot of a computer program Description automatically
generated](./media/image46.png)

![A screenshot of a computer program Description automatically
generated](./media/image47.png)

36. Execute: mvn spring-boot:run

![A screenshot of a computer program Description automatically
generated](./media/image48.png)

37. Clique em separar terminal e digite o comando abaixo no segundo
    terminal: curl -v <http://localhost:8080/hello?key=world>. Você
    também pode pedir ao Copilot para fornecer o comando curl para
    testar o seu código.

![BrokenImage](./media/image49.png)

38. Clique em separar terminal e digite o comando abaixo no segundo
    terminal: curl -v http://localhost:8080/hello 

![A screenshot of a computer program Description automatically
generated](./media/image50.png)

39. Pressione Ctrl + C para suspender o serviço em execução.

Tarefa 2: Comparação de datas

Nova operação em / diffdates that calculates the difference between two
dates. A operação deve receber duas datas como parâmetro no formato
dd-MM-aaaa e retornar a diferença em dias.

Além disso, crie um teste de unidade que valide a operação.

A partir de agora, você terá que criar os testes de unidade para cada
nova operação. Não foi fácil com o Copilot?

1.  Vá para **DemoController.java** e digite o prompt //create a New
    operation under /diffdates that calculates the difference between
    two dates. The operation should receive two dates as parameter in
    format dd-MM-yyyy and return the difference in days and press Enter.
    Aguarde um pouco e, quando o copilot previr o código, pressione a
    tecla Tab para aceitar o código.

![BrokenImage](./media/image51.png)

2.  Você também pode usar o código abaixo.

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
generated](./media/image52.png)

14. From now on, you will have to create the unit tests for every new
    operation. Use Copilot to create.

15. Abra o **CopilotDemoApplicationTests.java** na pasta **test** folder
    e digite o prompt // create unit test to /diffdates that calculates
    the difference between two dates. The operation should receive two
    dates as parameter in format dd-MM-yyyy and return the difference in
    days. then press Enter. Aguarde um segundo para que o Copilot
    preveja o código e pressione Tab para aceitar o código previsto.

16. Você pode inserir e pressionar Tab para criar vários testes
    unitários.

![A computer screen shot of a program Description automatically
generated](./media/image53.png)

![A screenshot of a computer program Description automatically
generated](./media/image54.png)

17. Use a ajuda do chat do Copilot para resolver problemas ou explicar o
    teste de unidade e atualize o código, se necessário, com base nas
    informações fornecidas pelo Copilot.

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
generated](./media/image55.png)

35. Abra o **Terminal -\> Gitbash** e execute os comandos abaixo

cd "exercisefiles\springboot\copilot-demo"

mvn test

![BrokenImage](./media/image56.png)

36. Se você encontrar erros de compilação, copie a mensagem de erro e
    peça ao Copilot para corrigi-los.

![BrokenImage](./media/image57.png)

37. O Copilot sugere que você importe pacotes com código. Adicione o
    comando ao seu código e execute o teste mvn.

![A screenshot of a computer program Description automatically
generated](./media/image58.png)

![A screenshot of a computer program Description automatically
generated](./media/image59.png)

![A screenshot of a computer program Description automatically
generated](./media/image60.png)

38. Execute: mvn package

![A screenshot of a computer program Description automatically
generated](./media/image61.png)

![A screenshot of a computer program Description automatically
generated](./media/image62.png)

39. Execute o teste mvn -Dtest=CopilotDemoApplicationTests#diffdates
    test

![A screenshot of a computer program Description automatically
generated](./media/image63.png)

40. Execute mvn spring-boot:run

![A screen shot of a computer program Description automatically
generated](./media/image64.png)

41. Clique em separar terminal e execute curl -v
    http://localhost:8080/diffdates?date1=01-01-2021&date2=01-02-2021

Você verá um erro. Peça ajuda ao Copilot e corrija o pequeno problema.

![A screenshot of a computer screen Description automatically
generated](./media/image65.png)

42. Peça ao Copilot Chat ajuda com o comando curl. Basta copiar a
    mensagem de erro e colar no chat. O Copilot fornecerá o comando
    modificado com a explicação.

![A screenshot of a computer program Description automatically
generated](./media/image66.png)

Tarefa 3: Validar o formato de um telefone espanhol

Valide o formato de um número de telefone espanhol (prefixo +34, seguido
de 9 dígitos iniciando com 6, 7 ou 9). A operação deve receber um número
de telefone como parâmetro e retornar true se o formato estiver correto;
caso contrário, false.

1.  Abra DemoController.Java e digite o prompt // Validate o formato de
    um número de telefone espanhol (+34 prefix, then 9 digits, starting
    with 6, 7 or 9). The operation should receive a phone number as
    parameter and return true if the format is correct, false otherwise.
    Pressione tab para aceitar o código.

![A screen shot of a computer program Description automatically
generated](./media/image67.png)

2.  Você também pode usar o código abaixo.

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

11. Alterne para **CopilotDemoApplicationTests.java.** Para escrever um
    teste de unidade para testar a função acima, adicione //Write unit
    test to validate the format of a spanish phone number (+34 prefix,
    then 9 digits, starting with 6, 7 or 9). The operation should
    receive a phone number as parameter and return true if the format is
    correct, false otherwise. Pressione Enter. Pressione a tecla Tab
    para aceitar o código.

![A computer screen shot of a program Description automatically
generated](./media/image68.png)

12. Você também pode usar os testes de unidade abaixo ou escrever seus
    próprios testes de unidade.

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

42. Abra o **Terminal -\>Gitbash** e execute os comandos abaixo.

cd exercisefiles/springboot/copilot-demo/

mvn test

![A screenshot of a computer program Description automatically
generated](./media/image69.png)

43. Execute: mvn package

![A screenshot of a computer program Description automatically
generated](./media/image70.png)

44. Execute: mvn spring-boot:run

![A screenshot of a computer program Description automatically
generated](./media/image71.png)

45. Separe o terminal e execute os comandos curl abaixo para validar os
    números de telefone.

curl -v http://localhost:8080/validatephone?phone=+34866666666

curl -v http://localhost:8080/validatephone?phone=+34666666667

curl -v http://localhost:8080/validatephone?phone=+34666666666

![A screenshot of a computer screen Description automatically
generated](./media/image72.png)

Tarefa 4: Validar o formato de um DNI espanhol

Valide o formato de um DNI espanhol (8 dígitos e 1 letra). A operação
deve receber um DNI como parâmetro e retornar true se o formato estiver
correto, false caso contrário.

1.  Abra o DemoController.Java e digite o prompt // Validate the format
    of a spanish DNI (8 digits and 1 letter). The operation should
    receive a DNI as parameter and return true if the format is correct,
    false otherwise. Pressione tab para aceitar o código.

![A screen shot of a computer program Description automatically
generated](./media/image73.png)

2.  Você também pode usar o código abaixo

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

11. Alterne para **CopilotDemoApplicationTests.java**. Para escrever um
    teste de unidade para testar a função acima, adicione // Write unit
    test to Validate the format of a spanish DNI (8 digits and 1
    letter). The operation should receive a DNI as parameter and return
    true if the format is correct, false otherwise. Pressione Enter.
    Pressione a tecla Tab para aceitar o código.

![A screenshot of a computer program Description automatically
generated](./media/image74.png)

12. Você também pode usar o teste de unidade abaixo ou escrever seus
    próprios testes de unidade.

13. @Test

14. void validatedniNoDni() throws Exception {

15. mockMvc.perform(MockMvcRequestBuilders.get("/validatedni"))

16. .andExpect(MockMvcResultMatchers.status().isOk())

17. .andExpect(MockMvcResultMatchers.content().string("false"));

}

18. Abra o Terminal -\> Gitbash e execute os comandos abaixo.

cd exercisefiles/springboot/copilot-demo/

mvn test

![A screenshot of a computer program Description automatically
generated](./media/image75.png)

![A screenshot of a computer program Description automatically
generated](./media/image76.png)

19. Execute: mvn package

![A screenshot of a computer program Description automatically
generated](./media/image77.png)

![A screenshot of a computer program Description automatically
generated](./media/image78.png)

20. Execute: mvn spring-boot:run

![A screenshot of a computer program Description automatically
generated](./media/image79.png)

21. Divida o terminal e execute curl -v
    http://localhost:8080/validatedni?dni=12345678C no segundo terminal.

![A screenshot of a computer program Description automatically
generated](./media/image80.png)

Tarefa 5: Do nome da cor ao código hexadecimal

Com base no arquivo colors.json existente em recursos, dado o nome da
cor como parâmetro de caminho, retorne o código hexadecimal. Se a cor
não for encontrada, retorne 404

Dica: Use TDD. Comece criando o teste de unidade e, em seguida,
implemente o código.

1.  Abra o DemoController.Java e digite o prompt // Based on existing
    colors.json file under resources, given the name of the color as
    path parameter, return the hexadecimal code. If the color is not
    found, return 404. Pressione tab para aceitar o código.

![A screen shot of a computer program Description automatically
generated](./media/image81.png)

2.  Você também pode usar o código abaixo ou escrever seu próprio
    código.

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

17. Alterne para **CopilotDemoApplicationTests.java.** Para escrever um
    teste de unidade para testar a função acima, adicione // test for
    /color/{color} endpoint Pressione Enter. Pressione a tecla Tab para
    aceitar o código.

![A screenshot of a computer program Description automatically
generated](./media/image82.png)

18. Você pode escrever seus testes de unidade. Você sempre pode
    verificar com o Copilot qualquer código/correção/teste de unidade.

19. Abra o **Terminal -\> Gitbash** e execute os comandos abaixo. Você
    poderá ver os erros de compilação.

cd exercisefiles/springboot/copilot-demo/

mvn test

![A screenshot of a computer program Description automatically
generated](./media/image83.png)

20. Pressione **Ctrl + Alt + I** para abrir o **Github Copilot Chat**.
    Copie a mensagem de erro e cole na janela de chat. O Copilot
    sugerirá a solução.

![A screenshot of a computer program Description automatically
generated](./media/image84.png)

21. O Copilot sugere que você importe os pacotes que faltam com a função
    importar. Copie-a e adicione-a ao seu código. Pressione Enter e o
    Copilot sugerirá que você adicione os pacotes que faltam. Pressione
    a tecla Tab e aceite-os para adicioná-los ao código.

![A screenshot of a computer program Description automatically
generated](./media/image85.png)

![A screenshot of a computer Description automatically
generated](./media/image86.png)

22. Abra o **Terminal -\> Gitbash** e execute os comandos abaixo
    novamente.

cd exercisefiles/springboot/copilot-demo/

mvn test

![A screenshot of a computer program Description automatically
generated](./media/image87.png)

![A screenshot of a computer program Description automatically
generated](./media/image88.png)

23. Execute: mvn package para gerar o pacote de sua aplicação.

![A screenshot of a computer program Description automatically
generated](./media/image89.png)

![A screenshot of a computer program Description automatically
generated](./media/image90.png)

24. Execute o comando mvn spring-boot:run para testar.

![A screenshot of a computer program Description automatically
generated](./media/image91.png)

25. Você pode pedir ao Copilot para ajudar com o comando curl a fim de
    testar sua função.

![BrokenImage](./media/image92.png)

26. Clique em **separar terminal** e execute o comando curl para testar
    sua aplicação (atualize a porta, se necessário)

![BrokenImage](./media/image93.png)

27. Teste com as cores listadas no arquivo **colors.json**.

![A screenshot of a computer program Description automatically
generated](./media/image94.png)

28. Teste uma cor que não esteja listada no arquivo **colors.json** e
    observe os resultados

![A computer screen shot of a program Description automatically
generated](./media/image95.png)

Tarefa 6: Criador de piadas

Crie uma nova operação que chame a API
https://api.chucknorris.io/jokes/random and return the joke.

1.  Abra DemoController.Java e digite o prompt // new operation that
    call the API https://api.chucknorris.io/jokes/random and return the
    joke. Pressione tab para aceitar o código.

![A screenshot of a computer program Description automatically
generated](./media/image96.png)

![A computer screen shot of a program Description automatically
generated](./media/image97.png)

2.  Você também pode usar o código abaixo.

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
generated](./media/image98.png)

18. Alterne para **CopilotDemoApplicationTests.java**. Para escrever um
    teste de unidade para testar a função acima, adicione // Create a
    unit test for new operation that call the API
    https://api.chucknorris.io/jokes/random and return the
    joke. Pressione Enter. Pressione a tecla Tab para aceitar o código.

![A screenshot of a computer program Description automatically
generated](./media/image99.png)

19. Você também pode adicionar o teste de unidade abaixo ou escrever
    seus próprios testes de unidade.

20. @Test

21. void joke() throws Exception{

22. mockMvc.perform(MockMvcRequestBuilders.get("/joke"))

23. .andExpect(MockMvcResultMatchers.status().isOk())

24. // check that content is a string

25. .andExpect(MockMvcResultMatchers.content().string(Matchers.any(String.class)));

}

![A screenshot of a computer program Description automatically
generated](./media/image100.png)

26. Abra o Terminal -\> Gitbahs e execute os comandos abaixo.

cd exercisefiles/springboot/copilot-demo/

mvn test

![A screenshot of a computer program Description automatically
generated](./media/image100.png)

![A screenshot of a computer Description automatically
generated](./media/image101.png)

27. Para gerar o pacote de sua aplicação. Execute: mvn package

![A screenshot of a computer program Description automatically
generated](./media/image102.png)

![A screenshot of a computer program Description automatically
generated](./media/image103.png)

28. Execute: mvn spring-boot:run

![A screenshot of a computer program Description automatically
generated](./media/image104.png)

![BrokenImage](./media/image105.png)

29. Clique em separar terminal e execute o comando: curl -v
    http://localhost:8080/joke no segundo terminal.

![A screenshot of a computer screen Description automatically
generated](./media/image106.png)

Tarefa 7: Análise de URL

Dado uma URL como parâmetro de consulta, faça a análise e retorne o
protocolo, host, porta, caminho e parâmetros de consulta. A resposta
deve estar no formato JSON.

1.  Abra o arquivo **DemoController.java** e digite o prompt //write a
    code for Given a url as query parameter, parse it and return the
    protocol, host, port, path and query parameters. The response should
    be in Json format. Pressione a tecla Tab para aceitar o código.

![BrokenImage](./media/image107.png)

2.  Você também pode usar o código abaixo.

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
generated](./media/image108.png)

16. Alterne para **CopilotDemoApplicationTests.java.** Para escrever um
    teste de unidade para testar a função acima, adicione // Create a
    unit test for new operation that call the API
    https://api.chucknorris.io/jokes/random and return the joke.
    Pressione Enter. Pressione a tecla Tab para aceitar o código.

![A screenshot of a computer program Description automatically
generated](./media/image109.png)

17. You can also add below unit tests or write your own unit tests.

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
generated](./media/image110.png)

33. Abra o **Terminal -\> Gitbash** e execute os comandos abaixo.

cd exercisefiles/springboot/copilot-demo/

mvn test

![A screenshot of a computer program Description automatically
generated](./media/image111.png)

![A screenshot of a computer program Description automatically
generated](./media/image112.png)

34. Execute: mvn package para gerar o pacote da sua aplicação.

![A screenshot of a computer program Description automatically
generated](./media/image113.png)

35. Execute: mvn spring-boot:run

![A screenshot of a computer program Description automatically
generated](./media/image114.png)

![BrokenImage](./media/image115.png)

36. Separe o terminal e execute o comando curl -v
    http://localhost:8080/parseurl?url=https://www.google.com/search?q=chuck+norris

![A screenshot of a computer screen Description automatically
generated](./media/image116.png)

Tarefa 8: Contagem de palavras

Dado o caminho de um arquivo, conte o número de ocorrências de uma
palavra fornecida. O caminho e a palavra devem ser parâmetros de
consulta. A resposta deve estar em formato JSON.

1.  Abra **DemoController.Java** e digite o prompt //write a code for
    Given the path of a file and count the number of occurrences of a
    provided word. The path and the word should be query parameters. The
    response should be in Json format. Pressione a tecla Tab para
    aceitar o código.

![BrokenImage](./media/image117.png)

2.  Alterne para **CopilotDemoApplicationTests.java**. Para escrever um
    teste de unidade para testar a função acima, adicione // Given the
    path of a file and count the number of occurrences of a provided
    word. The path and the word should be query parameters. The response
    should be in Json format. Pressione Enter. Pressione a tecla Tab
    para aceitar o código.

![BrokenImage](./media/image118.png)

3.  Abra o Terminal -\> Gitbash e execute os comandos abaixo.

cd exercisefiles/springboot/copilot-demo/

mvn test

![BrokenImage](./media/image119.png)

![BrokenImage](./media/image120.png)

4.  Execute: mvn package para gerar o pacote da sua aplicação/

![BrokenImage](./media/image121.png)

5.  Execute: mvn spring-boot:run

![BrokenImage](./media/image122.png)

6.  Clique em separar terminal e execute o comando curl para testar sua
    aplicação.

curl http://localhost:8080/countword?path=src/test/resources/test.txt

![BrokenImage](./media/image123.png)

Tarefa 9: Containerizar a aplicação

Use o Dockerfile fornecido para criar uma imagem Docker da aplicação.
Existem alguns comentários no Dockerfile que o ajudarão a concluir o
exercício.

Para construir, executar e testar a imagem do Docker, você também pode
usar o Copilot para gerar os comandos.

Por exemplo, crie um arquivo DOCKER.md onde você pode armazenar os
comandos para construir, executar e testar a imagem do Docker. Você
notará que o Copilot também o ajudará a documentar seu projeto e
comandos.

Exemplos de etapas a documentar: Criar a imagem do contêiner, Executar o
contêiner, Testar o contêiner.

1.  Clique duas vezes em Docker na área de trabalho e faça login com sua
    conta.

2.  Abra o arquivo Docker no Visual Studio Code, adicione o código
    abaixo a ele e salve o arquivo.

3.  \# Build a java application image based on openjdk 17 and run it on
    port 8080

4.  FROM openjdk:17-jdk-alpine

5.  EXPOSE 8080

6.  COPY target/\*.jar app.jar

ENTRYPOINT \["java","-jar","/app.jar"\]

![BrokenImage](./media/image124.png)

7.  Pressione **Ctrl + Alt + I** para abrir a janela do **GitHub
    Copilot** Chat. Pergunte ao Copilot abaixo do prompt. O Copilot
    fornece as etapas para conteinerizar o aplicativo.

como construir, executar e testar a imagem do Docker com o Dockerfile
fornecido para criar uma imagem do Docker da aplicação.

![BrokenImage](./media/image125.png)

8.  Siga o primeiro passo: crie a imagem do Docker. Abra o \*\*Terminal
    -\> Gitbash\*\* e execute o comando para criar a imagem do Docker.

cd exercisefiles/springboot/copilot-demo/

docker build -t my-application .

![BrokenImage](./media/image126.png)

![BrokenImage](./media/image127.png)

![A screenshot of a computer Description automatically
generated](./media/image128.png)

9.  Depois que a imagem estiver criada, você pode executá-la usando o
    comando docker run.

docker run -p 8080:8080 my-application

![A screenshot of a computer program Description automatically
generated](./media/image129.png)

10. Quando o contêiner Docker estiver em execução, você poderá testá-lo
    enviando solicitações para o seu aplicativo.

curl \<http://localhost:8080/hello?key=world

![BrokenImage](./media/image130.png)
