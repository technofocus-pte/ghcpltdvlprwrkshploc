**Laboratório 12: Criando fluxos de trabalho de implementação usando
GitHub Actions e Microsoft Azure**

Objetivos:

Imagine que você está gerenciando um projeto de software com requisitos
complexos de implementação que envolvem vários ambientes, incluindo
preparação e produção. Para otimizar seu processo de implementação e
garantir a consistência, você decide automatizá-lo usando GitHub Actions
e Microsoft Azure. Ao configurar fluxos de trabalho de implementação,
você pode definir acionadores com base em rótulos aplicados a
solicitações pull, que irão lidar com a ativação de ambientes, a
implementação em staging e a desativação de ambientes automaticamente.
Essa abordagem ajuda a manter a eficiência e reduz a intervenção manual
no pipeline de implementação.

Neste laboratório prático, você irá:

- Configurar fluxos de trabalho para criar e configurar ambientes
  automaticamente usando recursos do Azure quando um rótulo específico
  for aplicado a uma solicitação pull.

- Configurar tarefas de implementação nos fluxos de trabalho para
  implantar automaticamente seu projeto em um ambiente de teste ao
  receber o rótulo apropriado.

Exercício 1: Criar um novo repositório

1.  Navegue até o seguinte
    link: https://github.com/skills/deploy-to-azure

Neste laboratório, você criará o repositório usando um modelo
público **skills-deploy-to-azure**

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image1.jpeg)

2.  Selecione **Create a new repository** no menu **Use this template**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image2.jpeg)

3.  Insira os seguintes detalhes e selecione **Create Repository**.

    - Repository name: **skills-deploy-to-azure**

    - Repository type: **Public**

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image3.jpeg)

Exercício nº 2: Configurar permissões do GITHUB_TOKEN

No início de cada execução do fluxo de trabalho, o GitHub cria
automaticamente um segredo GITHUB_TOKEN exclusivo para usar no seu fluxo
de trabalho. Precisamos garantir que esse token tenha as permissões
necessárias.

1.  Na página inicial do repositório recém-criado, vá para
    **Settings** \> **Actions** \> **General**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image4.jpeg)

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image5.jpeg)

2.  Role até **Workflow permissions**, habilite **Read and write
    permissions** e clique em **Save**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image6.jpeg)

**Observação:** isso é necessário para que o fluxo de trabalho carregue
a imagem no registro de contêineres.

Exercício 3: Configurar um acionador com base em rótulos

1.  Na barra de navegação, vá até a guia **Actions**

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image7.jpeg)

2.  Na página **Actions**, clique em **New workflow** no painel de
    navegação à esquerda.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image8.jpeg)

3.  Na página **Choose a workflow**, procure por **\\simple workflow\\**
    e clique em **Configure**. ![A screenshot of a computer AI-generated
    content may be incorrect.](./media/image9.jpeg)

4.  Nomeie seu fluxo de trabalho como deploy-staging.yml

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image10.jpeg)

5.  Na página Edit, edite o conteúdo do arquivo e remova todos os
    acionadores e tarefas. O arquivo resultante terá a aparência
    mostrada abaixo.

6.  name: Stage the app

7.  on:

8.  pull_request:

9.  types: \[labeled\]

10. jobs:

11. build:

12. runs-on: ubuntu-latest

if: contains(github.event.pull_request.labels.\*.name, 'stage')

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image11.jpeg)

**Observação:** certifique-se de que o trecho de código adicionado
esteja devidamente indentado, conforme mostrado na captura de tela.

13. Clique no botão **Commit changes** no canto superior direito da
    página.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image12.jpeg)

14. Na janela **Commit changes**, selecione **Create a new branch for
    this commit and start a pull request.**

**Observação:** a janela **Commit changes** muda para **Propose
changes**.

Nomeie o **new branch** como **staging-workflow** e clique em **Propose
changes**.

![A screenshot of a chat AI-generated content may be
incorrect.](./media/image13.jpeg)

15. Na página seguinte, **Open a pull request**, clique em **Create pull
    request**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image14.jpeg)

16. Aguarde cerca de 20 segundos para que as ações sejam executadas e
    revise os resultados.

Resumo:

Agora você adquiriu experiência prática na automação de fluxos de
trabalho de implantação usando o GitHub Actions, aumentando a eficiência
e a confiabilidade do seu processo de implementação.
