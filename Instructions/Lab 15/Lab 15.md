**Laboratório 15: Habilite o CodeQL para proteger seu código-fonte**

Objetivo:

Imagine que você é um desenvolvedor de software trabalhando em um
projeto crítico para sua empresa, onde garantir a segurança do seu
aplicativo é uma prioridade. Com as crescentes preocupações com ameaças
cibernéticas e violações de dados, é essencial garantir que seu código
esteja livre de vulnerabilidades e práticas de codificação inseguras.
Neste laboratório prático, você habilitará o GitHub Code Scanning para
revisar automaticamente seu código-fonte em busca de possíveis problemas
de segurança.

Neste laboratório prático, você habilitará o GitHub Code Scanning para
revisar automaticamente seu código-fonte em busca de possíveis problemas
de segurança.

Exercício nº 1: criar um novo repositório a partir de um modelo público.

1.  Faça login na sua conta do GitHub.

2.  Navegue até o seguinte
    link: https://github.com/skills/introduction-to-codeql

Neste laboratório, você criará o repositório usando um modelo público
"**skills-introduction-to-codeql**".

![](./media/image1.jpeg)

3.  Selecione **Create a new repository** no menu **Use this template**.

![](./media/image2.jpeg)

4.  Insira os seguintes detalhes e selecione **Create Repository**.

    - Repository name:**skills-introduction-to-codeql**

    - Repository type: **Public**

![](./media/image3.jpeg)

Exercício nº 2: Habilitar a verificação de código com o CodeQL

1.  Na página inicial do repositório recém-criado, navegue até a guia
    **Settings**.

![](./media/image4.jpeg)

2.  Na seção **Security** na barra lateral à esquerda, selecione **Code
    security and analysis**.

![](./media/image5.jpeg)

3.  Role para baixo até a seção intitulada Code scanning, clique no menu
    suspenso **Set-up** e escolha **Default**.

![](./media/image6.jpeg)

4.  Selecione as seguintes opções e clique em **Enable CodeQL:**

    - Languages à serem analisadas: estas são as linguagens que serão
      verificadas pelo CodeQL. Neste caso, faremos a verificação em
      Python.

    - Query suites: as consultas do CodeQL são agrupadas em pacotes
      chamados “conjuntos”. Esta seção permite que você escolha qual
      conjunto de consultas usar. Deixaremos esta configuração como
      Padrão para este exercício.

    - Events: esta seção informa ao CodeQL quando fazer a varredura.
      Neste caso, está configurado para fazer a varredura em qualquer
      solicitação pull para o branch principal.

![](./media/image7.jpeg)

5.  Aguarde cerca de 20 segundos e depois atualize esta página para
    prosseguir.

![](./media/image8.jpeg)

Resumo:

Agora você ativou o GitHub Code Scanning para revisar automaticamente o
seu código-fonte em busca de possíveis problemas de segurança.
