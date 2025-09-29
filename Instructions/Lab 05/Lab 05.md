**Laboratório 05: Gerenciar novas versões de software com um fluxo de
trabalho baseado em GitHub Releases**

Objetivo:

Imagine que você faz parte de uma equipe de desenvolvimento de software
trabalhando em um projeto que exige atualizações e novas versões
regulares. Para gerenciar seu software de forma eficiente, você decide
implementar um fluxo de trabalho baseado em novas versões usando o
GitHub. Esse fluxo de trabalho ajuda você a lidar com versionamento e
gerenciar iterações de software de forma eficaz, garantindo que cada
nova versão seja rastreada e que problemas sejam tratados de maneira
controlada.

Neste laboratório prático, você irá:

- Criar um Repositório: Configurar um repositório chamado
  skills-release-based-workflow para servir como base para o fluxo de
  trabalho baseado em novas versões.

- Implementar Versionamento: Explorar os conceitos de versionamento e a
  importância de rastrear as iterações do software.

- Criar uma versão beta: Seguir os passos para criar uma versão beta
  para o código atual, incluindo marcação e publicação no GitHub.

- Simular um Cenário Real: Introduzir um bug no código, simulando um
  cenário comum de identificar e resolver problemas dentro do fluxo de
  trabalho de novas versões.

Exercício nº 1: Criar um novo Repositório (para servir como base para o
fluxo de trabalho baseado em novas versões)

1.  Acesse sua conta do GitHub.

2.  Navegue até o seguinte
    link: https://github.com/skills/release-based-workflow

In Neste laboratório, você criará o repositório usando um modelo público
**"skills-release-based-workflow"**.

![](./media/image1.jpeg)

3.  Selecione **Create a new repository** no menu **Use this template**.

![](./media/image2.jpeg)

4.  Insira os seguintes detalhes e selecione **Create Repository**.

    - Repository name: **skills-release-based-workflow**

    - Repository type: **Public**

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image3.jpeg)

Exercício nº 2: Criar uma nova versão para a base de código atual

Neste exercício, vamos criar uma nova versão para este repositório no
GitHub.

- Os GitHub Releases apontam para um compromisso específico.

- As novas versões podem incluir notas de lançamentos em arquivos
  Markdown e binários anexados.

Observação: antes de usar um fluxo de trabalho baseado em novas versões
para um lançamento maior, vamos criar uma rótulo e uma nova versão.

1.  Após criar o repositório (no Exercício nº 1), navegue até
    **Releases** na barra lateral direita da página e clique em **Create
    a new release**.

![](./media/image4.jpeg)

Dica**:** Para acessar esta página, clique na guia **Code** no topo do
repositório e localize a seção **Releases** na barra lateral direita.

2.  Na página **Releases/Tags**, insira as seguintes informações:

    1.  1\. Mantenha o **Target** como main

    2.  No campo **Choose a Tag**, especifique um número.

Neste caso, use v0.9 e selecione **Create new tag v0.9 on publish**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image5.jpeg)

3.  Dê um título a nova versão, como First beta release

**Observação:** Você também pode incluir uma breve descrição da nova
versão.

![](./media/image6.jpeg)

4.  Role até o final da página e marque a caixa **Set as a
    pre-release**, já que esta é uma versão beta, e clique em **Publish
    release**.

![A screenshot of a phone AI-generated content may be
incorrect.](./media/image7.jpeg)

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image8.jpeg)

Exercício nº 3: Introduzir um bug (para corrigir depois)

Para preparar o cenário para os próximos passos, vamos agora adicionar
um bug que corrigiremos como parte do fluxo de trabalho de novas versões
em etapas posteriores. Um branch “update-text-colors” já foi criado no
repositório (criada no Exercício nº 1) para você, então vamos criar e
mesclar uma solicitação pull com esse branch.

1.  Na barra de navegação principal, clique na guia **Pull requests**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image9.jpeg)

2.  Na página seguinte, clique em **New pull request.**

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image10.jpeg)

3.  Na página **Compare changes**, selecione as seguintes opções e
    clique em **Create pull request,**

    - base: **release-v1.0** e

    - compare: **update-text-colors**.

![](./media/image11.jpeg)

4.  Na página **Open a pull request**, insira as seguintes informações
    e, em seguida, clique em **Create pull request.**

    - Add a title: Defina o título da solicitação pull como Updated game
      text style

    - Add a description: ## Description: Updated game text color to
      green

![](./media/image12.jpeg)

5.  Na página **Updated game text style nº 1**, clique em **Merge pull
    request** e, em seguida, em **Confirm merge.**

![](./media/image13.jpeg)

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image14.jpeg)

6.  Na página seguinte, exclua a *branch* recém-criada clicando no botão
    **Delete branch**.

![](./media/image15.jpeg)

7.  Aguarde cerca de 20 segundos enquanto o GitHub Actions atualiza a
    página automaticamente.

![](./media/image16.jpeg)

**Resumo:**

Você agora adquiriu experiência prática na criação e gerenciamento de um
fluxo de trabalho baseado em novas versões, aprimorando sua capacidade
de rastreá-las, lidar com essas versões e corrigir bugs de forma
eficiente.
