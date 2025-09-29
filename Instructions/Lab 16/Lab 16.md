客観的:

あなたが開発チームの一員で、API
キーやデータベース資格情報などの機密情報が誤って Git
リポジトリにコミットされたプロジェクトに取り組んでいると想像してください。偶発的なコミットは、Git
で削除するのが難しい場合があります。

このラボでは、次のことを行います。

- 誤ってコミットされた機密データを含むリポジトリのクローンを作成します。

- 機密データを含むファイルをクローンされたリポジトリから削除/削除し、削除をコミットします。

- 変更を GitHub にプッシュする: 更新されたリポジトリを GitHub
  にアップロードして、変更を反映します。

### **演習 \#1: 偶発的なコミット履歴 (機密データ) を使用してリポジトリを作成する**

1.  GitHub アカウントにサインインします。

2.  次のリンクを参照します:
    <https://github.com/skills/change-commit-history>

> このラボでは、パブリックテンプレート「**skills-change-commit-history**」を使用してリポジトリを作成します。
>
> ![](./media/image1.png)

3.  「**このテンプレートを使用する」**メニューの「**新しいリポジトリの作成**」
    を選択します。

> ![コンピューターのスクリーンショット
> 説明が自動生成される](./media/image2.png)

4.  次の詳細を入力し、「**Create Repository」**を選択します。

- リポジトリ名: **skills-change-commit-history**

- リポジトリの種類: **Public**

![](./media/image3.png)

### **演習 \# 2: 機密データを含むファイル (プロジェクト ルート ディレクトリの .env) を削除/削除する**

1.  複製されたリポジトリのランディングページで、**Code\>Local\>HTTPS**
    に移動し、URL をコピーします。

![](./media/image4.png)

2.  Windows Powershellを開き、次のコマンドを入力します。

**git clone \<your-repository-url\>**

**注**: 手順 1 でコピーした URL に置き換えます。

> ![](./media/image5.png)

3.  リポジトリディレクトリに切り替えて、次のコマンドを入力します。

**+++cd “C:\Users\Admin\skills-change-commit-history”+++**

**注**: リポジトリ名に置き換えます

> ![](./media/image6.png)

4.  次のコマンドを実行して、ルートディレクトリから「.envを削除」します

**+++git rm .env**+++

> ![コンピューター画面のスクリーンショット
> 説明が自動生成される](./media/image7.png)

5.  .env ファイルの削除をコミットします

**+++git commit -m "remove .env file”+++**

> ![コンピューターのスクリーンショット
> 説明が自動生成される](./media/image8.png)
>
> **ヒント**:Git履歴から.envファイルを完全に削除し、新しいコミットハッシュで合計履歴を書き換える方法は?
>
> 次のコマンドを使用して、次の操作を行います：

- Git履歴から.envファイルを完全に削除し、全履歴を書き換える

> **git filter-branch --force --index-filter 'git rm --cached
> --ignore-unmatch.env' --prune-empty --tag-name-filter cat -- --all**

- 削除を GitHub にプッシュします

> **git push origin --force –all**

6.  削除を GitHub にプッシュします：

**git push**

> ![コンピューター プログラムのスクリーン ショット
> 説明が自動生成される](./media/image9.png)

**概要**：

これで、Git
リポジトリのクリーンアップが完了し、機密コンテンツがリポジトリの履歴に公開されないようにしました。
