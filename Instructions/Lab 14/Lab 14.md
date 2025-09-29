**Laboratório 14: Proteja a cadeia de suprimentos do seu repositório**

Objetivos:

Imagine que você é responsável por manter a segurança de um projeto de
software que depende de várias dependências de terceiros. Para garantir
a integridade e a segurança da cadeia de suprimentos do seu projeto, é
fundamental compreender e gerenciar essas dependências de maneira
eficaz. Isso envolve identificar possíveis vulnerabilidades nas suas
dependências e aplicar os patches necessários para proteger o seu
projeto. Neste laboratório, você aprenderá a usar o recurso de gráfico
de dependências do GitHub para monitorar e revisar suas dependências,
garantindo que seu projeto permaneça seguro e atualizado.

Neste laboratório prático, você irá:

- Habilitar o Dependency Graph: habilite e verifique o recurso
  Dependency Graph nas configurações do seu repositório para visualizar
  as dependências do seu projeto.

- Adicionar uma nova dependência: adicione uma nova dependência ao seu
  projeto e certifique-se de que ela esteja integrada corretamente.

- Revisar o Dependency Graph: use o Dependency Graph para revisar e
  confirmar se a nova dependência está refletida e monitorada
  corretamente.

Exercício nº 01: criar um novo repositório

1.  Navegue até o seguinte
    link: https://github.com/skills/secure-repository-supply-chain

Neste laboratório, você criará o repositório usando um modelo
público **skills-secure-repository-supply-chain**

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image1.jpeg)

2.  Selecione **Create a new repository** no menu **Use this template**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image2.jpeg)

3.  Insira os seguintes detalhes e selecione **Create Repository**:

    - Repository name: **skills-secure-repository-supply-chain**

    - Repository type: **Public**

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image3.jpeg)

Exercício 02: Verifique se o dependency graph está habilitado

1.  Na página inicial do repositório recém-criado, navegue até a guia
    **Settings**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image4.jpeg)

2.  Na página **Settings**, selecione **Code security and analysis** em
    **Security.**

![A screenshot of a general login AI-generated content may be
incorrect.](./media/image5.jpeg)

3.  Verifique/ative o dependency graph. (Se o repositório for privado,
    você o ativará aqui. Se o repositório for público, ele será ativado
    por padrão)

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image6.jpeg)

Exercício 03: Adicione uma nova dependência e visualize seu dependency
graph.

1.  Navegue até a guia **Code** e localize a pasta
    **code/src/AttendeeSite**.

**Observação:** Você pode navegar manualmente até a pasta ou usar **Go
to file** e pesquisar code/src/AttendeeSite

![A screenshot of a web page AI-generated content may be
incorrect.](./media/image7.jpeg)

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image8.jpeg)

2.  Abra o arquivo **package-lock.json**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image9.jpeg)

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image10.jpeg)

3.  Insira o seguinte trecho de código entre a linha 14 e a linha 15:

4.  "follow-redirects": {

5.  "version": "1.14.1",

6.  "resolved":

7.  "https://registry.npmjs.org/follow-redirects/-/follow-redirects-1.14.1.tgz",

8.  "integrity":

9.  "sha512-HWqDgT7ZEkqRzBvc2s64vSZ/hfOceEol3ac/7tKwzuvEyWx3/4UegXh5oBOIotkGsObyk3xznnSRVADBgWSQVg=="

},

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image11.jpeg)

**Observação:** Certifique-se de que o trecho de código adicionado
esteja corretamente indentado, conforme mostrado na captura de tela.

10. Clique em **Commit changes** no canto superior direito.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image12.jpeg)

11. Na barra de navegação principal, clique na guia **Insights.**

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image13.jpeg)

12. No painel de navegação esquerdo, clique em **Dependency graph**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image14.jpeg)

13. Revise todas as novas dependências no Dependencies hub.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image15.jpeg)

14. Procure por redirecionamentos de acompanhamento e revise a nova
    dependência que você acabou de adicionar.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image16.jpeg)

Resumo:

Agora você obteve informações valiosas sobre como gerenciar as
dependências do seu projeto e proteger a cadeia de suprimentos do seu
repositório, permitindo que você aborde e mitigue proativamente os
riscos de segurança.
