**Laboratório 10: Use o GitHub Actions para publicar seu projeto em uma
imagem Docker**

Objetivos:

Imagine que você está desenvolvendo um projeto de software que deseja
criar pacotes e distribuir como uma imagem Docker. Para otimizar o
processo de implementação e garantir que sua imagem Docker seja
publicada de forma consistente no GitHub Packages, você decide usar o
GitHub Actions para automação. Isso permitirá que você configure um
fluxo de trabalho que automatiza a publicação de sua imagem Docker
sempre que alterações forem feitas, garantindo que seu projeto esteja
sempre atualizado e disponível para implementação.

Neste laboratório prático, você irá:

- Configurar um arquivo de fluxo de trabalho do GitHub Actions que
  automatiza o processo de criação e publicação da sua imagem Docker.

- Configurar o fluxo de trabalho para criar sua imagem Docker e enviá-la
  para o GitHub Packages, garantindo que a imagem seja publicada
  corretamente.

- Criar uma solicitação pull para visualizar todas as alterações feitas.

Exercício nº 1: criar um novo repositório a partir de um modelo público

1.  Navegue até o seguinte
    link: https://github.com/skills/publish-packages

Neste laboratório, você criará o repositório usando um modelo público
"**skills-publish-packages**".

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image1.jpeg)

2.  Selecione **Create a new repository** no menu **Use this template**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image2.jpeg)

3.  Insira os seguintes detalhes e selecione **Create Repository**.

    - Repository name: **skills-publish-packages**

    - Repository type: **Public**

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image3.jpeg)

Exercício 2: Criar um arquivo de fluxo de trabalho e configurar o fluxo
de trabalho

1.  Clique no botão **Code** na barra de navegação principal do
    repositório que você acabou de criar.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image4.jpeg)

2.  No menu suspenso do **main** branch, selecione o branch **cd**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image5.jpeg)

3.  Na página seguinte, navegue até a pasta **.github/workflows/**,
    selecione **Add file** e clique em **Create new file**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image6.jpeg)

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image7.jpeg)

4.  No campo **Name your file**, insira publish.yml

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image8.jpeg)

5.  Adicione o seguinte código ao arquivo **publish.yml**:

6.  name: Publish to Docker

7.  on:

8.  push:

9.  branches:

10. \- main

11. permissions:

12. packages: write

13. contents: read

14. jobs:

15. publish:

16. runs-on: ubuntu-latest

17. steps:

18. \- name: Checkout

19. uses: actions/checkout@v4

20. \# Add your test steps here if needed...

21. \- name: Docker meta

22. id: meta

23. uses: docker/metadata-action@v5

24. with:

25. images: ghcr.io/YOURNAME/publish-packages/game

26. tags: type=sha

27. \- name: Login to GHCR

28. uses: docker/login-action@v3

29. with:

30. registry: ghcr.io

31. username: ${{ github.repository_owner }}

32. password: ${{ secrets.GITHUB_TOKEN }}

33. \- name: Build container

34. uses: docker/build-push-action@v5

35. with:

36. context: .

37. push: true

tags: ${{ steps.meta.outputs.tags }}

38. Substitua YOURNAME pelo seu nome de usuário.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image9.jpeg)

39. Certifique-se de que o nome da imagem seja exclusivo e clique em
    **Commit changes.**

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image10.jpeg)

40. Clique novamente em **Commit changes** para confirmar.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image11.jpeg)

41. Agora, crie uma solicitação de pull para visualizar todas as
    alterações feitas no exercício acima.

42. Clique na guia **Pull Requests** na barra de navegação.

43. Clique em **New pull request**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image12.jpeg)

44. Na página **Comparing changes**, defina **base:** main e
    **compare:** cd, depois clique em **Create pull request.**

![A screenshot of a chat AI-generated content may be
incorrect.](./media/image13.jpeg)

45. Na página **Add a title**, clique em **Create pull request.**

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image14.jpeg)

46. Aguarde cerca de 20 segundos para que as actions sejam executadas e
    revise os resultados.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image15.jpeg)

Resumo:

Você agora adquiriu experiência prática no uso do GitHub Actions para
automatizar a publicação de imagens Docker, aprimorando sua capacidade
de agilizar processos de implementação e manter distribuições de projeto
sempre atualizadas.
