**Laboratório 19 - Crie uma REST API usando Quarkus com a ajuda do
GitHub Copilot**

O objetivo deste laboratório é aprender a usar o GitHub Copilot, usando
uma tarefa que consiste em criar uma REST API usando
https://quarkus.io/.

Criamos um projeto Quarkus com alguns arquivos já criados. Você pode
encontrar o projeto na pasta **exercisefiles/quarkus**.

Vamos começar a copilotar!!!

**Tarefa 1 - Criar o código para lidar com uma solicitação GET simples**

Vá para o arquivo ‘DemoResource.java’ e comece a escrever o código para
lidar com uma solicitação GET simples.

1.  Nesta primeira etapa, fornecemos um comentário que descreve o código
    que você precisa gerar. Basta pressionar Enter e aguardar alguns
    segundos.

![BrokenImage](./media/image1.png)

2.  O Copilot irá gerar o código para você. Se você não estiver
    satisfeito com o código, pressione Ctrl + Enter e ele irá sugerir
    várias opções de código.

![A screenshot of a computer Description automatically
generated](./media/image2.png)

3.  Se você não estiver satisfeito com o código gerado, pressione Enter
    novamente e o Copilot irá gerar um novo código.

![A screenshot of a computer Description automatically
generated](./media/image3.png)

![A screenshot of a computer program Description automatically
generated](./media/image4.png)

![A screenshot of a computer program Description automatically
generated](./media/image5.png)

4.  Vá para **test/java/com/Microsoft/hackthon/quarkus/** e clique em
    **DemoResourceTest.java**. Já existe um teste de unidade
    implementado para esta tarefa.

![A screenshot of a computer Description automatically
generated](./media/image6.png)

5.  Clique em **Terminal -\> New Terminal.**

![BrokenImage](./media/image7.png)

6.  Selecione **Gitbash**.

![BrokenImage](./media/image8.png)

7.  Execute o comando cd exercisefiles/quarkus/copilot-demo/

![A screen shot of a computer program Description automatically
generated](./media/image9.png)

8.  Você pode executá-lo usando o comando mvn test antes e depois para
    validar se o código gerado pelo Copilot está correto.

![A screenshot of a computer program Description automatically
generated](./media/image10.png)

![A screen shot of a computer Description automatically
generated](./media/image11.png)

![A screenshot of a computer program Description automatically
generated](./media/image12.png)

9.  Após cada tarefa, sinta-se à vontade para criar o pacote e executar
    sua aplicação para testá-la.

Package: mvn package

![A screenshot of a computer program Description automatically
generated](./media/image13.png)

![A screenshot of a computer program Description automatically
generated](./media/image14.png)

10. Execute: mvn quarkus:dev

![A screenshot of a computer program Description automatically
generated](./media/image15.png)

![A screenshot of a computer program Description automatically
generated](./media/image16.png)

11. Clique em Separar terminal, insira o comando no segundo terminal e
    execute.

curl -v http://localhost:8080/hello?key=world

curl http://localhost:8080/hello

curl http://localhost:8080/hello?key=world

![A screenshot of a computer screen Description automatically
generated](./media/image17.png)

![BrokenImage](./media/image18.png)

**Tarefa 2: Comparação de datas**

Nova operação chamada /diffdates que calcula a diferença entre duas
datas. A operação deve receber duas datas como parâmetro no formato
dd-MM-aaaa e retornar a diferença em dias.

1.  Type the following comment // New operation under /diffdates that
    calculates the difference between two dates. The operation should
    receive two dates as parameter in format dd-MM-yyyy and return the
    difference in days. Pressione Enter

**Observação:** O comentário está no arquivo
**DemoResource.java**. **C:\CopiolHackathon\exercisefiles\\ quarkus\\
copilot-demo\src\main\\
java\com\microsoft\hackathon\quarkus\DemoResource.java**

![A screen shot of a computer program Description automatically
generated](./media/image19.png)

2.  Pressione a tecla Tab, e em seguida pressione Tab novamente para
    aceitar o código.

![A screen shot of a computer program Description automatically
generated](./media/image20.png)

3.  Abra o arquivo DemoResourceTest.java, crie um teste de unidade que
    valide a operação. Adicione //Create a unit test to validate
    /diffdates that calculates the difference between two dates e depois
    pressione Enter.

![A screenshot of a computer program Description automatically
generated](./media/image21.png)

4.  Pressione a tecla Tab para aceitar o código. Você também pode usar o
    código abaixo:

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

![A screenshot of a computer program Description automatically
generated](./media/image22.png)

79. Abra o terminal e execute o commando: mvn test.

![A screen shot of a computer Description automatically
generated](./media/image23.png)

![A screenshot of a computer program Description automatically
generated](./media/image24.png)

80. Gere o pacote de solução executando o comando: mvn package

![A screenshot of a computer program Description automatically
generated](./media/image25.png)

![A screenshot of a computer program Description automatically
generated](./media/image26.png)

81. Execute: mvn quarkus:dev ou mvn compile quarkus:dev

![A screenshot of a computer program Description automatically
generated](./media/image27.png)

82. Separe o Terminal e execute o comando: curl -v
    http://localhost:8080/diffdates

**Tarefa 3: Validar o formato de um telefone espanhol**

Valide o formato de um número de telefone espanhol (prefixo +34, depois
9 dígitos iniciando com 6, 7 ou 9). A operação deve receber um número de
telefone como parâmetro e retornar true se o formato estiver correto;
caso contrário, false.

1.  Digite //Validate o formato de um número de telefone espanhol (+34
    prefix, then 9 digits, starting with 6, 7 or 9). The operation
    should receive a phone number as parameter and return true if the
    format is correct, false otherwise and press Enter. Pressione tab
    para aceitar o código sugerido pelo Coilot.

![A screen shot of a computer program Description automatically
generated](./media/image28.png)

2.  Digite // write unit test para validar o formato de um número de
    telefone espanhol ( +34 prefix, then 9 digits, starting with 6, 7 or
    9). The operation should receive a phone number as parameter and
    return true if the format is correct, false otherwise and press
    Enter. Pressione tab para aceitar os testes unitários sugeridos pelo
    Copilot.

![A screen shot of a computer program Description automatically
generated](./media/image29.png)

3.  Abra o terminal e execute: mvn test.

![A screen shot of a computer Description automatically
generated](./media/image30.png)

![A screenshot of a computer program Description automatically
generated](./media/image31.png)

4.  Execute: mvn package

![A screenshot of a computer program Description automatically
generated](./media/image32.png)

![A screenshot of a computer program Description automatically
generated](./media/image33.png)

5.  Execute mvn quarkus:dev

![A screenshot of a computer screen Description automatically
generated](./media/image34.png)

6.  Clique em separar terminal e execute em um dos terminais -

curl -v http://localhost:8080/validatephone?phone=+34866666666

curl -v http://localhost:8080/validatephone?phone=+34666666667

curl -v http://localhost:8080/validatephone?phone=+34666666666

![A screenshot of a computer program Description automatically
generated](./media/image35.png)

**Tarefa 4: Validar o formato de um DNI espanhol**

Valide o formato de um DNI espanhol (8 dígitos e 1 letra). A operação
deve receber um DNI como parâmetro e retornar true se o formato estiver
correto, false caso contrário.

1.  Digite // Validate the format of a spanish DNI (8 digits and 1
    letter). The operation should receive a DNI as parameter and return
    true if the format is correct, false otherwise and press Enter.
    Pressione tab para aceitar o código sugerido pelo Copilot.

![A screenshot of a computer program Description automatically
generated](./media/image36.png)

2.  Alterne para CopilotDemoApplicationTests.java. Para escrever um
    teste de unidade para testar a função acima, adicione // Write unit
    test to Validate the format of a spanish DNI (8 digits and 1
    letter). The operation should receive a DNI as parameter and return
    true if the format is correct, false otherwise. Pressione Enter.
    Pressione a tecla Tab para aceitar o código.

![A screen shot of a computer program Description automatically
generated](./media/image37.png)

3.  Abra o terminal e execute: mvn test

![A screenshot of a computer program Description automatically
generated](./media/image38.png)

![A screenshot of a computer program Description automatically
generated](./media/image39.png)

4.  Execute: mvn package

![A screenshot of a computer program Description automatically
generated](./media/image40.png)

![A screenshot of a computer program Description automatically
generated](./media/image41.png)

5.  Execute: mvn quarkus:dev

![A screenshot of a computer program Description automatically
generated](./media/image42.png)

6.  Teste: curl -v http://localhost:8080/hello/validatedni?dni=12345678A

![A screenshot of a computer program Description automatically
generated](./media/image43.png)

**Tarefa 5: Do nome da cor ao código hexadecimal**

Com base no arquivo colors.json existente em recursos, dado o nome da
cor como parâmetro de caminho, retorne o código hexadecimal. Se a cor
não for encontrada, retorne 404

Dica: use TDD. Comece criando o teste de unidade e, em seguida,
implemente o código.

1.  Digite // Based on the existing colors.json file under resources,
    given the name of the color as path parameter, return the
    hexadecimal code. If the color is not found, return 404 and press
    Enter. Pressione tab para aceitar o código sugerido pelo Copilot.

![A screenshot of a computer program Description automatically
generated](./media/image44.png)

2.  Alterne para **CopilotDemoApplicationTests.java.** Para escrever um
    teste de unidade para testar a função acima, adicione //Write unit
    test to based on the existing colors.json file under resources,
    given the name of the color as path parameter, return the
    hexadecimal code. If the color is not found, return 404. Pressione
    Enter. Pressione a tecla Tab para aceitar o código.

![A screenshot of a computer program Description automatically
generated](./media/image45.png)

3.  Execute: mvn test

![A screenshot of a computer program Description automatically
generated](./media/image46.png)

![A screenshot of a computer program Description automatically
generated](./media/image47.png)

4.  Execute: mvn package

![A screenshot of a computer Description automatically
generated](./media/image48.png)

5.  Execute: mvn quarkus:dev

![A screenshot of a computer program Description automatically
generated](./media/image49.png)

6.  Teste: curl -v http://localhost:8080/hello/color?color=red

![BrokenImage](./media/image50.png)

**Tarefa 6: Criador de piadas**

Crie uma nova operação que chame a API
https://api.chucknorris.io/jokes/random and return the joke.

1.  Digite // Create a new operation that call the API
    https://api.chucknorris.io/jokes/random and return the joke and
    press Enter. Pressione tab para aceitar o código sugerido pelo
    Copilot.

![A screenshot of a computer program Description automatically
generated](./media/image51.png)

2.  Pressione a tecla Tab para aceitar o código.

![A screen shot of a computer program Description automatically
generated](./media/image52.png)

3.  Alterne para **CopilotDemoApplicationTests.java**. Para escrever um
    teste de unidade para testar a função acima, adicione //Create a new
    operation that call the API
    \[\<u\>https://api.chucknorris.io/jokes/random\</u\>\](https://api.chucknorris.io/jokes/random)
    and return the joke. Pressione Enter. Pressione a tecla Tab para
    aceitar o código.

![A screenshot of a computer program Description automatically
generated](./media/image53.png)

4.  Pressione a tecla Tab para aceitar o código.

![A screenshot of a computer program Description automatically
generated](./media/image54.png)

5.  Clique em Terminal -\> New Terminal -\> Gitbash e execute os
    comandos abaixo

cd exercisefiles/quarkus/copilot-demo/

mvn test

![A screenshot of a computer program Description automatically
generated](./media/image55.png)

![A screenshot of a computer program Description automatically
generated](./media/image56.png)

6.  Execute: mvn package para gerar o pacote de sua aplicação.

![A screenshot of a computer program Description automatically
generated](./media/image57.png)

![A screenshot of a computer program Description automatically
generated](./media/image58.png)

7.  Execute: mvn quarkus:dev

![A screenshot of a computer program Description automatically
generated](./media/image59.png)

8.  Teste: curl -v http://localhost:8080/hello/joke

![A screenshot of a computer program Description automatically
generated](./media/image60.png)

**Tarefa 7: Análise de URL**

Dado uma URL como parâmetro de consulta, faça a análise e retorne o
protocolo, host, porta, caminho e parâmetros de consulta. A resposta
deve estar no formato JSON.

1.  Digite //Given a url as query parameter, parse it and return the
    protocol, host, port, path and query parameters. The response should
    be in Json format and press Enter. Pressione tab para aceitar o
    código sugerido pelo Copilot.

![A screen shot of a computer program Description automatically
generated](./media/image61.png)

![A screen shot of a computer program Description automatically
generated](./media/image62.png)

2.  Alterne para **CopilotDemoApplicationTests.java.** Para escrever um
    teste de unidade para testar a função acima, adicione //Write unit
    test for Given a url as query parameter, parse it and return the
    protocol, host, port, path and query parameters. The response should
    be in Json format. Pressione Enter. Pressione a tecla Tab para
    aceitar o código.

![A screenshot of a computer program Description automatically
generated](./media/image63.png)

3.  Execute: mvn test

![A screenshot of a computer program Description automatically
generated](./media/image64.png)

![A screenshot of a computer Description automatically
generated](./media/image65.png)

4.  Execute: mvn package para gerar o pacote da sua aplicação.

![A screenshot of a computer program Description automatically
generated](./media/image66.png)

5.  Execute: mvn quarkus:dev

![A screenshot of a computer program Description automatically
generated](./media/image67.png)

6.  Clique em separar terminal e execute o comando curl -v
    http://localhost:8080/hello/parseurl?url=https://www.google.com/search?q=quarkus

![A screenshot of a computer program Description automatically
generated](./media/image68.png)

**Tarefa 9: Contagem de palavras**

Dado o caminho de um arquivo, conte o número de ocorrências de uma
palavra fornecida. O caminho e a palavra devem ser parâmetros de
consulta. A resposta deve estar em formato JSON.

1.  Digite //Given the path of a file and count the number of occurrence
    of a provided word. The path and the word should be query
    parameters. The response should be in Json format and press Enter.
    Pressione tab para aceitar o código sugerido pelo Copilot.

![A screenshot of a computer program Description automatically
generated](./media/image69.png)

2.  Alterne para **CopilotDemoApplicationTests.java.** Para escrever um
    teste de unidade para testar a função acima, adicione //Write unit
    test to Given the path of a file and count the number of occurrence
    of a provided word. The path and the word should be query
    parameters. The response should be in Json format. Pressione Enter.
    Pressione a tecla Tab para aceitar o código.

![A screenshot of a computer program Description automatically
generated](./media/image70.png)

3.  Abra o **terminal** e execute: mvn test

![A screenshot of a computer program Description automatically
generated](./media/image71.png)

![A screenshot of a computer program Description automatically
generated](./media/image72.png)

4.  Execute: mvn package para gerar o pacote da sua aplicação.

![A screenshot of a computer program Description automatically
generated](./media/image73.png)

![A screenshot of a computer program Description automatically
generated](./media/image74.png)

5.  Execute: mvn quarkus:dev

![A screenshot of a computer program Description automatically
generated](./media/image75.png)

6.  Teste: curl \<http://localhost:8080/hello/countword?path=/tmp/test.txt&word=hello

Você pode pedir ao GitHub Copilot o comando curl para o seu projeto.

![A screenshot of a computer program Description automatically
generated](./media/image76.png)

**Tarefa 10: Containerizar a aplicação**

Use o Dockerfile fornecido para criar uma imagem Docker da aplicação.
Neste caso, o conteúdo completo já é fornecido, mas para compilar,
executar e testar a imagem Docker, você também usará o Copilot para
gerar os comandos.

Criei um arquivo DOCKER.md onde documentaremos as etapas para
desenvolver o aplicativo (nativo), compilar a imagem do contêiner,
executar o contêiner e testar o contêiner.

1.  No Visual Studio Code, pressione **Ctrl + Shift + X**. Procure por
    **Docker** e instale-o.

![A screenshot of a computer Description automatically
generated](./media/image77.png)

2.  Clique duas vezes em **Desktop Docker** e faça login com a sua conta
    Docker.

![BrokenImage](./media/image78.png)

3.  Pressione **Ctrl + Alt + I** para abrir o **GitHub Copilot Chat**.
    Pergunte ao seu Copilot como criar a imagem do contêiner, executar o
    contêiner e testar o contêiner usando o Dockerfile fornecido.

![A screenshot of a computer program Description automatically
generated](./media/image79.png)

4.  Siga as instruções do Copilot. Crie o aplicativo: execute o seguinte
    comando em seu terminal: 

> /mvnw package -Pnative -Dquarkus.native.container-build=true 
>
> ![A screenshot of a computer Description automatically
> generated](./media/image80.png)
>
> ![A screenshot of a computer program Description automatically
> generated](./media/image81.png)
>
> ![A screenshot of a computer program Description automatically
> generated](./media/image82.png)
>
> ![A screenshot of a computer program Description automatically
> generated](./media/image83.png)
>
> ![A screenshot of a computer program Description automatically
> generated](./media/image84.png)

5.  **Build the Docker image**: Supondo que seu arquivo Dockerfile
    esteja nomeado como **Dockerfile.native-micro**, você pode usar o
    seguinte comando: 

> docker build -f Dockerfile.native-micro -t my-app. 
>
> ![A computer screen shot of a program Description automatically
> generated](./media/image85.png)
>
> 6\. Este comando instrui o Docker a criar uma imagem usando o
> Dockerfile chamado \`Dockerfile.native-micro\` no diretório atual
> (\`.\` no final do comando) e a rotular a imagem resultante com o nome
> \`my-app\`.
>
> 7\. Execute a imagem do Docker: após a imagem ser criada, você pode
> executá-la com o comando \`docker run\`:
>
> docker run -p 8080:8080 my-app 

![BrokenImage](./media/image86.png)

Este comando instrui o Docker a executar um contêiner a partir da imagem
\`my-app\` e a mapear a porta 8080 no contêiner para a porta 8080 na
máquina host.

1.  **Teste o aplicativo:** Por fim, para testar se o seu aplicativo
    está funcionando corretamente, você pode enviar uma solicitação para
    http://localhost:8080 no navegador ou usar uma ferramenta como o
    curl:

curl http://localhost:8080

![A screenshot of a computer program Description automatically
generated](./media/image87.png)

Este comando envia uma requisição GET para a sua aplicação e imprime a
resposta. Se a sua aplicação estiver em execução corretamente, você
deverá ver a resposta esperada.

Observe que esses comandos devem ser executados no terminal, não no
código do aplicativo Java.
