**Laboratório 08: Crie uma ação do GitHub e use-a em um fluxo de
trabalho**

Objetivo:

Imagine que você faz parte de uma equipe de desenvolvimento que deseja
otimizar seu processo de desenvolvimento de software automatizando
tarefas repetitivas. Para melhorar a eficiência, você decide aproveitar
o GitHub Actions, que permite automatizar tarefas como testes,
implementação e revisões de código diretamente no seu repositório
GitHub. Ao configurar um GitHub Action e integrá-lo ao seu fluxo de
trabalho, você pode garantir que tarefas essenciais sejam realizadas
automaticamente, economizando tempo e reduzindo o esforço manual.

Neste laboratório prático, você irá:

- Configurar um arquivo de fluxo de trabalho no diretório
  .github/workflows, definindo o conteúdo e especificando os eventos que
  acionam o fluxo de trabalho.

- Praticar a inclusão e confirmar arquivos de fluxo de trabalho ao seu
  repositório para integrar o GitHub Actions ao seu processo de
  desenvolvimento.

Exercício nº 1: Criar um novo repositório a partir de um modelo público

1.  Navegue até o seguinte
    link: https://github.com/skills/hello-github-actions

Neste laboratório, você criará o repositório usando um modelo público
"**skills-hello-github-actions**".

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image1.jpeg)

2.  Selecione **Create a new repository** no menu **Use this template**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image1.jpeg)

3.  Insira os seguintes detalhes e selecione **Create Repository**.

    - Repository name: **skills-hello-github-actions**

    - Repository type: **Public**

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image2.jpeg)

Exercício nº 2: Criar um arquivo de fluxo de trabalho

1.  Na página inicial do repositório recém-criado, navegue até a guia
    **Pull requests**.

![A screenshot of a web page AI-generated content may be
incorrect.](./media/image3.jpeg)

2.  Na página seguinte, clique no botão **New pull request**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image4.jpeg)

3.  Na página **Compare changes**, selecione **base:** **main** e
    **compare: welcome-workflow** e clique em **Create pull request.**

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image5.jpeg)

4.  Na página **Open a pull request**, clique em **Create pull
    request**.

![A screenshot of a email request AI-generated content may be
incorrect.](./media/image6.jpeg)

5.  Navegue até a guia **Code**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image7.jpeg)

6.  Na página seguinte, **no menu suspenso main branch**, clique no
    branch **welcome-workflow**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image8.jpeg)

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image9.jpeg)

7.  Após alterar o branch principal para **welcome-workflow**, navegue
    até a pasta **.github/workflows**, selecione **Add file** e clique
    em **Create new file**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image10.jpeg)

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image11.jpeg)

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image12.jpeg)

8.  Na página de criação do arquivo, insira o nome do arquivo como
    welcome.yml.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image13.jpeg)

9.  No editor, adicione o seguinte conteúdo ao arquivo welcome.yml e
    clique em **Commit changes**:

10. name: Post welcome comment

11. on:

12. pull_request:

13. types: \[opened\]

14. permissions:

pull-requests: write

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image14.jpeg)

15. Na página **Commit changes**, clique em **Commit changes.**

16. Aguarde cerca de 20 segundos para que as actions sejam executadas e,
    em seguida, atualize a página — uma ação encerrará automaticamente
    esta etapa.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image15.jpeg)

**Resumo:**

Agora você adquiriu experiência prática na configuração e gerenciamento
do GitHub Actions, melhorando sua capacidade de automatizar e otimizar
fluxos de trabalho de desenvolvimento de software.
