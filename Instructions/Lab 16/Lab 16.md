Laboratório 16: Remover o histórico de envios de um repositório Git

Objetivo:

Imagine que você faz parte de uma equipe de desenvolvimento trabalhando
em um projeto em que informações confidenciais, como chaves API ou
credenciais de banco de dados, foram acidentalmente enviadas para o seu
repositório Git. Envios acidentais podem ser difíceis de remover com o
Git.

Neste laboratório, você irá:

- Clonar o repositório com dados confidenciais enviados acidentalmente.

- Remover/excluir o arquivo que contém dados confidenciais do
  repositório clonado e enviar as alterações.

- Enviar as alterações para o GitHub: carregar o repositório atualizado
  no GitHub para refletir as alterações.

### Exercício nº 1: Criar o repositório com o histórico de envios acidentais (dados confidenciais)

1.  Acesse sua conta do GitHub.

2.  Navegue até o link:
    <https://github.com/skills/change-commit-history>

> Neste laboratório, você criará o repositório usando um modelo público
> “**skills-change-commit-history**”.
>
> ![](./media/image1.png)

3.  Selecione **Create a new repository** no menu **Use this template**.

> ![A screenshot of a computer Description automatically
> generated](./media/image2.png)

4.  Insira os seguintes detalhes e selecione **Create Repository**.

- Repository name: **skills-change-commit-history**

- Repository type: **Public**

![](./media/image3.png)

### Exercício nº 2: Remover/excluir o arquivo (.env no diretório raiz do projeto) que contém dados confidenciais.

1.  Na página inicial do repositório clonado, navegue até **Code \>
    Local \> HTTPS** e copie a URL.

![](./media/image4.png)

2.  Abra o Windows PowerShell e insira o seguinte comando:

**git clone \<your-repository-url\>**

**Observação:** substitua pelo URL copiado no passo 1.

> ![](./media/image5.png)

3.  Mude para o diretório do seu repositório, insira o seguinte comando:

**+++cd “C:\Users\Admin\skills-change-commit-history”+++**

**Observação:** substitua pelo nome do repositório

> ![](./media/image6.png)

4.  Execute o seguinte comando para excluir o arquivo .env do diretório
    raiz:

**+++git rm .env**+++

> ![A screenshot of a computer screen Description automatically
> generated](./media/image7.png)

5.  Confirme a remoção do arquivo .env.

**+++git commit -m "remove .env file”+++**

> ![A screen shot of a computer Description automatically
> generated](./media/image8.png)
>
> **Dica**: Como remover completamente o arquivo .env do histórico do
> Git e reescrever todo o histórico com novos hashes de commit?
>
> Use os seguintes comandos:

- Remova completamente o .env do histórico do Git e reescreva todo o
  histórico:

> **git filter-branch --force --index-filter 'git rm --cached
> --ignore-unmatch.env' --prune-empty --tag-name-filter cat -- --all**

- Envie a remoção para o GitHub:

> **git push origin --force –all**

6.  Envie a remoção para o GitHub:

**git push**

> ![A screen shot of a computer program Description automatically
> generated](./media/image9.png)

Resumo:

Agora você concluiu a limpeza do seu repositório Git, garantindo que
nenhum conteúdo confidencial seja exposto no histórico do repositório.
