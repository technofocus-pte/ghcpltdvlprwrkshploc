**Laboratório 13: Escreva uma GitHub JavaScript Action e automatize
tarefas personalizadas exclusivas para o seu fluxo de trabalho.**

Objetivos:

Imagine que você recebeu a tarefa de criar uma GitHub Action
personalizada para automatizar tarefas específicas dentro do seu fluxo
de trabalho. Para começar, é necessário configurar um ambiente de
desenvolvimento para escrever e testar sua JavaScript Action. Isso
envolve inicializar um novo projeto JavaScript, configurar a estrutura
do projeto e instalar as dependências necessárias.

Seguindo os passos deste laboratório, você criará uma base sólida para
desenvolver sua GitHub Action, permitindo criar automações adaptadas às
necessidades do seu projeto.

Neste laboratório prático, você irá:

- Clonar o repositório: clone o repositório fornecido para sua máquina
  local para iniciar seu processo de desenvolvimento.

- Navegar até a pasta do projeto: vá para a pasta do repositório
  clonado, onde você configurará sua ação.

- Criar a pasta de ação: configure uma nova pasta dentro do repositório
  especificamente para seus arquivos de ação.

- Inicializar o projeto npm: inicialize um novo projeto npm na pasta de
  ação para gerenciar dependências e configuração.

- Instalar dependências: use o npm para instalar as dependências
  necessárias para desenvolver sua ação JavaScript do GitHub.

- Preparar-se para o desenvolvimento da ação: configure o ambiente do
  seu projeto para começar a escrever e testar sua ação GitHub
  JavaScript personalizada.

Exercício: 1 Criar um novo repositório

1.  Navegue até o
    link: https://github.com/skills/write-javascript-actions

Neste laboratório, você criará o repositório usando o modelo público
**skills-write-javascript-actions**

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image1.jpeg)

2.  Selecione **Create a new repository** no menu **Use this template**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image2.jpeg)

3.  Insira os seguintes detalhes e selecione **Create Repository**:

    - Repository name: **skills-write-javascript-actions**

    - Repository type: **Public**

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image3.jpeg)

Exercício nº 2: Inicializar um novo projeto JavaScript

Depois de instalar as ferramentas necessárias localmente, siga estas
etapas para começar a criar sua primeira ação.

1.  Na página inicial do repositório **write-javascript-actions**,
    clique no botão **Code** (o botão de cor verde) e copie o URL HTTPS
    na guia **Local**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image4.jpeg)

2.  Agora abra o **Command prompt**  e clone seu repositório de
    habilidades para a máquina local:

git clone \<this repository URL\>.git

![A screenshot of a computer program AI-generated content may be
incorrect.](./media/image5.jpeg)

**Observação:** Geralmente ele é clonado no caminho
"**C:\Users\Admin\skills-write-javascript-actions**"

3.  Navegue até a pasta clonada:

cd C:\Users\Admin\skills-write-javascript-actions

![A screenshot of a computer program AI-generated content may be
incorrect.](./media/image6.jpeg)

4.  Vamos usar o branch chamado main:

git switch main

![A screenshot of a computer program AI-generated content may be
incorrect.](./media/image7.jpeg)

5.  Crie uma nova pasta para nossos arquivos de ações:

mkdir -p .github\actions\joke-action

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image8.jpeg)

6.  Navegue até a pasta joke-action que você acabou de criar:

cd .github/actions/joke-action

![A screenshot of a computer program AI-generated content may be
incorrect.](./media/image9.jpeg)

7.  Inicialize um novo projeto:

npm init -y

![A screenshot of a computer program AI-generated content may be
incorrect.](./media/image10.jpeg)

8.  Instale as dependências request, request-promise e \\actions/core
    usando o npm a partir do GitHub ToolKit
    (https://github.com/actions/toolkit):

Npm install -save request request-promise @actions/core

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image11.jpeg)

9.  Confirme os arquivos recém-adicionados. Removeremos a necessidade de
    carregar node_modules em uma etapa posterior:

git add . && git commit -m "add project dependencies"

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image12.jpeg)

**Observação:** Se for solicitado para informar o e-mail e o nome de
usuário, insira os comandos abaixo substituindo pelos seus dados:

![A screen shot of a computer AI-generated content may be
incorrect.](./media/image13.jpeg)

git config --global user.email "your_email@example.com"

git config --global user.name "Your Name"

**Observação**: Substitua pelos seus dados.

10. Envie suas alterações para o repositório: digite o comando abaixo e
    faça login

git push

![A computer screen with white text AI-generated content may be
incorrect.](./media/image14.jpeg)

**Observação:** quando solicitado a autorizar, faça login na conta do
GitHub e continue o processo.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image15.jpeg)

![A screenshot of a login form AI-generated content may be
incorrect.](./media/image16.jpeg)

![A screenshot of a computer error AI-generated content may be
incorrect.](./media/image17.jpeg)

11. Aguarde cerca de 20 segundos enquanto o GitHub Actions atualiza
    automaticamente a página para processamento adicional.

Resumo:

Você estabeleceu um ambiente de desenvolvimento robusto para criar e
gerenciar seu GitHub JavaScript Action, preparando o terreno para
automatizar e aprimorar seus fluxos de trabalho.
