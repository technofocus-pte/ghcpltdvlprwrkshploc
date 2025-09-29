**Laboratório 07: Codificação com GitHub Codespaces e Visual Studio
Code**

Objetivo:

Imagine que você é um desenvolvedor trabalhando em um projeto que requer
um ambiente de desenvolvimento hospedado na nuvem para facilitar a
colaboração e otimizar seu fluxo de trabalho. Para aumentar sua
produtividade e gerenciar sua configuração de desenvolvimento de forma
mais eficaz, você decide usar o GitHub Codespaces com o Visual Studio
Code. Essa configuração permite criar e personalizar ambientes de
desenvolvimento diretamente na nuvem, facilitando a colaboração com sua
equipe e o gerenciamento eficiente das configurações do projeto.

Neste laboratório prático, você irá:

- Iniciar um Codespace: criar e iniciar um GitHub Codespace usando
  modelos predefinidos.

- Personalizar configurações: personalizar as configurações do seu
  projeto dentro do codespace para atender às suas necessidades de
  desenvolvimento.

- Gerenciar Codespaces: gerencie e navegue com eficiência pelos seus
  codespaces, garantindo um processo de desenvolvimento tranquilo e
  organizado.

- Enviar código para o repositório: pratique enviar suas alterações de
  código do codespace para o repositório GitHub, reforçando sua
  capacidade de integrar o trabalho de desenvolvimento com o controle de
  versão.

Exercício nº 1: configurar um novo repositório e iniciar um GitHub
Codespace

1.  Faça login na sua conta GitHub.

2.  Navegue até o seguinte
    link: https://github.com/skills/code-with-codespaces

Neste laboratório, você criará o repositório usando um modelo público
"**skills-code-with-codespaces**".

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image1.jpeg)

3.  Selecione **Create a new repository** no menu **Use this template**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image2.jpeg)

4.  Insira os seguintes detalhes e selecione **Create Repository**.

    - Repository name: **skills-code-with-codespaces**

    - Repository type: **Public**

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image3.jpeg)

5.  Após criar o repositório, clique no botão **Code**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image4.jpeg)

6.  Na janela pop-up, selecione a guia **Codespaces** e clique no botão
    **Create codespace on main**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image5.jpeg)

**Observação:** o codespace será aberto em uma nova guia do
navegador**.**

7.  O navegador exibirá um editor baseado na web do VS Code e um
    terminal deverá estar presente, conforme mostrado no exemplo.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image6.jpeg)

8.  Aguarde cerca de 2 minutos para que o codespace (uma máquina
    virtual) seja inicializado.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image7.jpeg)

9.  Volte para o repositório **skills-code-with-codespaces** e clique no
    botão **Code**

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image8.jpeg)

**Observação:** se o codespace recém-criado não carregar, atualize a
página.

10. Clique no ícone de reticências (…) no codespace ativo \*\*.\*\*

**Observação:** o nome do codespace pode ser diferente no seu caso

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image9.jpeg)

11. No menu pop-up, selecione **Open in Visual Studio Code**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image10.jpeg)

12. Será exibido um pop-up pedindo confirmação para abrir o codespace no
    aplicativo VS Code. Selecione **Open Visual Studio Code** para abrir
    o codespace.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image11.jpeg)

13. Você será solicitado a instalar a extensão GitHub Codespaces. Clique
    em **Install extension and open URI**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image12.jpeg)

14. Após a instalação, aparecerá um pop-up solicitando permissões
    adicionais. Clique em **Authorize Visual Studio Code.**

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image13.jpeg)

15. Confirme o acesso digitando a senha da sua conta GitHub.

![A screenshot of a login form AI-generated content may be
incorrect.](./media/image14.jpeg)

**Observação:** se aparecer o pop-up solicitando permissão no Windows
Firewall, permita para continuar.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image15.jpeg)

Exercício nº 2: Enviar código do codespace para o repositório

1.  Dentro do codespace, na janela do explorador do VS Code, selecione o
    arquivo index.html.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image16.jpeg)

2.  Substitua o cabeçalho h1 pelo seguinte:

\<h1\>Hello from the codespace!\</h1\>

3.  Salve o arquivo.

**Observação:** o arquivo deve ser salvo automaticamente.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image17.jpeg)

4.  Use o terminal do VS Code para confirmar a alteração do arquivo,
    inserindo a seguinte mensagem de confirmação:

git commit -a -m "Adding hello from the codespace!"

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image18.jpeg)

5.  Envie as alterações de volta para o seu repositório. No terminal do
    VS Code, digite:

git push

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image19.jpeg)

6.  O novo código do VS Code foi enviado para o seu repositório!

7.  Volte para a página inicial do seu repositório e abra o arquivo
    index.html para verificar se o novo código foi enviado com sucesso.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image20.jpeg)

8.  Aguarde cerca de 20 segundos e atualize esta página. O GitHub
    Actions será atualizado automaticamente para a próxima etapa.

Resumo:

Você já utilizou o GitHub Codespaces e o Visual Studio Code para

- Criar e iniciar um GitHub Codespace utilizando modelos predefinidos.

- Enviar código para o repositório: pratique enviar suas alterações de
  código do codespace para o repositório GitHub, reforçando sua
  capacidade de integrar o trabalho de desenvolvimento com o controle de
  versão.
