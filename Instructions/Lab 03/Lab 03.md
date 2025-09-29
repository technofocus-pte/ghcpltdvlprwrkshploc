**Laboratório 03: Crie seu Portfólio Online com GitHub Pages e Jekyll**

Objetivo:

Imagine que você é um desenvolvedor de software iniciante em uma startup
de tecnologia, ansioso para apresentar seus projetos, habilidades e
experiências por meio de um portfólio online. Você deseja uma plataforma
profissional para exibir seu trabalho, então decide criar um site
pessoal ou blog usando o GitHub Pages. Essa plataforma permite que você
aproveite os repositórios do GitHub para publicar e manter seu site de
forma simples.

Neste laboratório prático, você irá:

- Criar um Repositório GitHub: configurar um novo repositório que
  servirá como a base do seu site pessoal.

- Habilitar o GitHub Pages: configurar o GitHub Pages para hospedar seu
  site diretamente do seu repositório.

- Publicar seu Primeiro Site Usando o Jekyll: utilizar o Jekyll, um
  gerador de sites estáticos popular, para criar e publicar um site com
  aparência profissional de forma simples.

Exercício nº 1: Criar um repositório a partir de um modelo

1.  Acesse sua conta do GitHub.

2.  Navegue até o link: https://github.com/skills/github-pages

Neste laboratório, você criará o repositório usando um modelo público
"**skills-github-pages**".

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image1.jpeg)

3.  Selecione **Create a new repository** no menu **Use this template**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image2.jpeg)

4.  Insira os seguintes detalhes e selecione **Create Repository**.

    - Repository name: **skills-github-pages**

    - Repository type: **Public**

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image3.jpeg)

Exercício nº 2: Ativar o GitHub Pages

1.  Depois que o repositório for criado, vá para a página inicial. No
    painel de navegação principal, clique no ícone **Settings**.

![A screenshot of a web page AI-generated content may be
incorrect.](./media/image4.jpeg)

2.  Na página de configurações, role até Code and automation e clique em
    **Pages**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image5.jpeg)

3.  Na página do GitHub Pages, verifique se “**Deploy from a branch”**
    está selecionado no menu suspenso **Source** e, em seguida,
    selecione **main** no menu suspenso **Branch**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image6.jpeg)

4.  Clique no botão **Save** para continuar.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image7.jpeg)

5.  A fonte do GitHub Pages será salva. Aguarde cerca de um minuto e
    depois atualize a página. O GitHub Actions atualizará
    automaticamente para a próxima etapa.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image8.jpeg)

6.  Seu site agora está ativo.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image9.jpeg)

7.  Clique no botão Visit Site para visualizar seu site. O GitHub Pages
    foi ativado.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image10.jpeg)

Exercício nº 3: Publicar seu site usando Jekyll

Você trabalhará em um branch chamado **my-pages** para deixar o site com
boa aparência. Neste laboratório, usaremos um tema pronto para blog
chamado "minima".

O Jekyll utiliza um arquivo chamado **\_config.yml** para armazenar as
configurações do site, o tema e conteúdos reutilizáveis, como o título
do site e o nome de usuário do GitHub.

1.  Selecione a guia **Code** do seu repositório

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image11.jpeg)

2.  Expanda o branch **main** e selecione **my-pages**.

![A screenshot of a web page AI-generated content may be
incorrect.](./media/image12.jpeg)

No branch **my-pages**, navegue até o arquivo **\_config.yml**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image13.jpeg)

3.  Abra o editor de arquivos no canto superior direito.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image14.jpeg)

4.  Adicione o tema configurando para **minima**, de modo que apareça no
    arquivo \_config.yml como no exemplo abaixo:

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image15.jpeg)

5.  Clique no botão **Commit Changes** para salvar as alterações.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image16.jpeg)

**Observação:** Aguarde cerca de um minuto e depois atualize a página. O
GitHub Actions atualizará automaticamente para a próxima etapa.

6.  Para verificar o site atualizado, clique no botão **Visit site** na
    seção do GitHub Pages.

![A screenshot of a web page AI-generated content may be
incorrect.](./media/image17.jpeg)

7.  O tema selecionado será aplicado. Você pode continuar modificando
    outras variáveis de configuração, como title:, author: e
    description:, para personalizar ainda mais seu site.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image18.jpeg)

Resumo:

Agora você criou um site com o GitHub Pages e aplicou um tema. Essa
experiência pode ser utilizada para criar um site ativo que você poderá
atualizar continuamente, apresentando sua trajetória no desenvolvimento
de software e facilitando para empregadores, colaboradores e para a
comunidade de tecnologia conhecerem seu trabalho e suas habilidades.
