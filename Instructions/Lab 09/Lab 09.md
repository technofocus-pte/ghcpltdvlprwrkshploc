**Laboratório 09: Crie fluxos de trabalho para usar a Continuous
Integration (CI) em seus projetos**

Objetivos:

Imagine que você está trabalhando em um projeto de software em que é
fundamental manter padrões de alta qualidade. Para garantir que seu
código permaneça robusto e livre de erros, você decide implementar a
Continuous Integration (CI) usando o GitHub Actions. A CI ajuda a
automatizar o processo de execução de testes e verificação da qualidade
do código sempre que são feitas alterações na base de código. Ao criar
fluxos de trabalho de CI, você pode automaticamente verificar arquivos
Markdown, executar testes e receber feedback imediato sobre a qualidade
do código, garantindo que seu projeto atenda aos padrões de qualidade de
forma consistente.

Neste laboratório prático, você irá:

- Criar um fluxo de trabalho de teste: configurar um fluxo de trabalho
  do GitHub Actions projetado especificamente para verificar arquivos
  Markdown e verificar problemas de formatação.

- Configurar e atualizar o fluxo de trabalho: praticar a configuração do
  arquivo de fluxo de trabalho para definir as tarefas e etapas
  necessárias para a verificação automatizada e atualizá-lo conforme
  necessário para aprimorar sua funcionalidade.

- Criar uma solicitação pull: integrar as alterações criando uma
  solicitação pull, permitindo que você teste o fluxo de trabalho de CI
  e observe como ele automatiza as verificações de qualidade.

- Analisar os resultados do fluxo de trabalho de CI para entender como
  ele relata problemas e garante a qualidade do código.

Exercício nº 1: Criar um novo repositório a partir de um modelo público

1.  Navegue até o seguinte
    link: https://github.com/skills/test-with-actions

Neste laboratório, você criará o repositório usando um modelo público
"**skills-test-with-actions**".

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image1.jpeg)

2.  Selecione **Create a new repository** no menu **Use this template**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image2.jpeg)

3.  Insira os seguintes detalhes e selecione **Create Repository**:

    - Repository name: **skills-test-with-actions**

    - Repository type: **Public**

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image3.jpeg)

Exercício nº 2: Adicionar um fluxo de trabalho de teste

1.  No repositório criado anteriormente, navegue até a guia Actions.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image4.jpeg)

2.  No menu lateral esquerdo, em Actions, selecione **New workflow**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image5.jpeg)

3.  Na página **Choose a workflow**, localize “**Simple workflow”** e
    clique em **Configure**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image6.jpeg)

4.  Na página seguinte, renomeie o fluxo de trabalho para ci.yml e
    remova as duas últimas etapas do arquivo.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image7.jpeg)

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image8.jpeg)

5.  Adicione o seguinte código ao final do fluxo de trabalho e clique em
    **Commit changes** no canto superior direito:

6.  \- name: Run markdown lint

7.  run: |

8.  npm install remark-cli remark-preset-lint-consistent

npx remark . --use remark-preset-lint-consistent

**Observação:** certifique-se de que o trecho de código adicionado
esteja devidamente indentado.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image9.jpeg)

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image10.jpeg)

9.  Na janela **Commit changes**, selecione **Create a new branch for
    this commit and start a pull request**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image11.jpeg)

10. Quando a opção **Create a new branch for this commit and start a
    pull request** for selecionada, a janela **Commit changes** mudará
    para **Propose changes**. Agora, clique em **Propose changes**.

![A screenshot of a computer screen AI-generated content may be
incorrect.](./media/image12.jpeg)

11. Na página seguinte, **Open a pull request**, clique em **Create pull
    request.**

![A screenshot of a email AI-generated content may be
incorrect.](./media/image13.jpeg)

12. Aguarde cerca de 20 segundos e, em seguida, atualize esta página
    para analisar os resultados.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image14.jpeg)

Resumo:

Você agora adquiriu experiência prática com práticas de CI usando o
GitHub Actions, aprimorando sua capacidade de automatizar e manter altos
padrões de qualidade em seus projetos de software.
