**Laboratório 17: Habilite a verificação secreta em um repositório
GitHub e confirme um token**

Imagine que você é um desenvolvedor de software trabalhando em um
projeto de equipe com um repositório GitHub compartilhado. Para garantir
que seu código permaneça seguro e livre de vazamentos acidentais, você
decide implementar a verificação secreta — um recurso que ajuda a
identificar informações confidenciais, como tokens de API ou senhas, que
podem ser inadvertidamente enviadas para o repositório.

Objetivo:

Neste laboratório prático, você irá:

1.  Ativar a verificação secreta: configurar a verificação secreta no
    seu repositório GitHub para detectar e sinalizar automaticamente
    informações confidenciais.

2.  Confirmar um token: adicionar intencionalmente um token ou outras
    informações confidenciais ao repositório para testar a eficácia do
    recurso de verificação secreta.

Exercício nº 1: Criar um repositório GitHub e ativar a verificação
secreta

Tarefa nº 1: Criar um repositório usando um modelo

1.  Acesse sua conta do GitHub.

2.  Navegue até o seguinte
    link: https://github.com/skills/introduction-to-secret-scanning

Neste laboratório, você criará o repositório usando um modelo público
"**skills-introduction-to-secret-scanning**".

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image1.jpeg)

3.  Selecionar **Create a new repository** no menu **Use this
    template**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image2.jpeg)

4.  Inserir os seguintes detalhes e selecionar **Create Repository**.

    - Repository name: **skills-introduction-to-secret-scanning**

    - Repository type: **Public**

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image3.jpeg)

Tarefa nº 2: Ativar a verificação secreta

1.  Na página inicial do repositório recém-criado, selecione
    **Settings** na barra de navegação superior.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image4.jpeg)

2.  Na seção **Security** da barra lateral, selecione **Code security
    and analysis**.

**Observação:** É necessário rolar a página para baixo para visualizar o
menu **Security.**

![A screenshot of a browser window AI-generated content may be
incorrect.](./media/image5.jpeg)

3.  Role até o final da página e clicar em **Enable** para habilitar o
    secret scanning.

**Observação:** se você visualizar o botão **Disable**, significa que o
secret scanning já está habilitado para o repositório.

![A white background with black text AI-generated content may be
incorrect.](./media/image6.jpeg)

Se ainda não estiver habilitado, você verá o botão **Enable** conforme
mostrado abaixo:

![A screenshot of a computer error AI-generated content may be
incorrect.](./media/image7.jpeg)

**Observação:** Quando o secret scanning está habilitado, uma
notificação por e-mail sobre credenciais no repositório é enviada para o
e-mail associado à conta. Os tokens neste repositório Skills estão
inativos. Não há risco para o ambiente.

Agora que o secret scanning está habilitado neste repositório, vamos
confirmar um novo token para ver como funciona.

Exercício nº 2: Enviar um token

Neste exercício, você enviará uma chave AWS e um ID de acesso ao
repositório. Este é um token inativo que não pode ser usado para fazer
login na AWS.

1.  No painel superior esquerdo da barra de navegação principal, clique
    na guia **Code** e selecione o arquivo **credentials.yml**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image8.jpeg)

2.  Clique no botão Edit à direita.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image9.jpeg)

3.  Copie o texto abaixo e cole-o abaixo do código existente no painel
    de edição do arquivo **credentials.yml**.

4.  default:

5.  aws_access_key_id: AKIAQYLPMN5HNM4OZ56B

6.  aws_secret_access_key: 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

7.  output: json

region: us-east-2

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image10.jpeg)

8.  Clique no botão **Commit changes** no canto superior direito e
    clique novamente em **Commit Changes** na janela **Commit Changes**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image11.jpeg)

**Observação:** após confirmar as alterações, você receberá um alerta na
sua caixa de correio associada à sua conta GitHub.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image12.jpeg)

Resumo:

Agora você adquiriu um conhecimento prático sobre como habilitar e
testar a verificação secreta para proteger seu código e seus dados.
