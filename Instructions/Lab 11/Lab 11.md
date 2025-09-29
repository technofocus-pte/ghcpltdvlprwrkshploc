**Laboratório 11: Tornando um fluxo de trabalho reutilizável e usando
uma estratégia de matriz para executar várias versões do nó**

Objetivos:

Imagine que você está gerenciando vários repositórios dentro de um
projeto que compartilham fluxos de trabalho comuns para tarefas como
criar, testar e implementar. Para evitar redundância e manter a
consistência entre esses repositórios, você decide implementar fluxos de
trabalho reutilizáveis usando o GitHub Actions. Ao utilizar o acionador
workflow_call, você pode centralizar suas configurações de fluxo de
trabalho, garantindo que as alterações sejam feitas em um único lugar e
aplicadas automaticamente em todos os repositórios relevantes. Além
disso, você aproveitará as estratégias de matriz para testar seus fluxos
de trabalho com várias versões do Node.js, melhorando a compatibilidade
e a escalabilidade.

Neste laboratório prático, você irá:

- Usar o acionador workflow_call para tornar seus fluxos de trabalho
  reutilizáveis em vários repositórios, reduzindo a redundância de
  configuração.

- Navegar até seu repositório, atualizar o arquivo de fluxo de trabalho
  para incluir o acionador workflow_call e confirmar as alterações.

- Criar uma solicitação pull para comparar as alterações e as exceções.

Exercício nº 1: criar um novo repositório.

1.  Navegue até o seguinte
    link: https://github.com/skills/reusable-workflows

Neste laboratório, você criará o repositório usando um modelo público
"**skills-reusable-workflows**".

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image1.jpeg)

2.  Selecione **Create a new repository** no menu **Use this template**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image2.jpeg)

3.  Insira os seguintes detalhes e selecione **Create Repository**.

    - Repository name: **skills-reusable-workflows**

    - Repository type: **Public**

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image3.jpeg)

Exercício nº 2: Adicionar um acionador workflow_call a um fluxo de
trabalho

1.  Na página inicial do repositório recém-criado, navegue até a guia
    **Code** \*\*.\*\*

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image4.jpeg)

2.  No menu suspenso do branch principal, selecione o branch
    **reusable-workflow**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image5.jpeg)

3.  Após mudar o branch, navegue até a pasta **.github/workflows/** e
    selecione o arquivo **reusable-workflow.yml**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image6.jpeg)

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image7.jpeg)

4.  No editor do arquivo **reusable-workflow.yml**, selecione **Edit in
    place**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image8.jpeg)

5.  Substitua o acionador de evento **workflow_dispatch** pelo acionador
    de evento **workflow_call** e clique em **Commit changes**.

**Observação:** Substitua o bloco de código da **Linha 3** à **Linha 8**
pelo seguinte**:**

on:

workflow_call:

inputs:

node:

required: true

type: string

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image9.jpeg)

6.  Na janela **Commit changes**, clique em **Commit changes.**

![A screenshot of a screenshot of a new branch AI-generated content may
be incorrect.](./media/image10.jpeg)

Exercício nº 3: Criar um solicitação pull para visualizar as alterações
feitas no exercício anterior

1.  Selecione a guia **Pull requests** e clique em **New pull request**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image11.jpeg)

2.  Na página **Comparing changes,** defina **base** como **main** e
    **compare** como **reusable-workflow.**

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image12.jpeg)

3.  Na página **Open a pull request**, clique em **Create pull
    request.**

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image13.jpeg)

4.  Aguarde cerca de 20 segundos para que as actions sejam executadas e
    revise os resultados.

Resumo:

Agora você adquiriu experiência prática na criação de fluxos de trabalho
eficientes e reutilizáveis e na otimização deles para vários ambientes
usando o GitHub Actions.
