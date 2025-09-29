**ラボ 10: GitHub Actions を使用してプロジェクトを Docker
イメージに発行する**

目標：

Docker イメージとしてパッケージ化して配布するソフトウェア
プロジェクトを開発していると想像してください。デプロイ
プロセスを合理化し、Docker イメージが一貫して GitHub Packages
に公開されるようにするには、自動化に GitHub Actions
を使用することにしました。これにより、変更が加えられるたびに Docker
イメージの公開を自動化するワークフローを設定でき、プロジェクトが常に最新であり、デプロイに利用できるようになります。

このハンズオンラボでは、次のことを行います:

- Docker イメージのビルドと公開のプロセスを自動化する GitHub Actions
  ワークフロー ファイルを設定します。

- Docker イメージをビルドして GitHub Packages
  にプッシュするようにワークフローを構成し、イメージが正しく公開されていることを確認します。

- pull request を作成して、行ったすべての変更を表示します。

演習 \#1: パブリックテンプレートから新しいリポジトリを作成する

1.  次のリンクを参照します: https://github.com/skills/publish-packages

このラボでは、パブリックテンプレート「**skills-publish-packages**」を使用してリポジトリを作成します。

![コンピューターのスクリーンショット AI
が生成したコンテンツは間違っている可能性があります。](./media/image1.jpeg)

2.  **「このテンプレートを使用する」** メニュー の**「Create a new
    repository」**を選択します 。

![コンピューターのスクリーンショット AI
が生成したコンテンツは間違っている可能性があります。](./media/image2.jpeg)

3.  次の詳細を入力し、「**Create Repository」**を選択します。

    - リポジトリ名: **skills-publish-packages**

    - リポジトリの種類: **Public**

![コンピューターのスクリーンショット AI
が生成したコンテンツは間違っている可能性があります。](./media/image3.jpeg)

演習 2: ワークフロー ファイルを作成し、ワークフローを構成する

1.  作成したリポジトリのメインナビゲーションバーにある**「コード」**ボタンをクリックします。

![コンピューターのスクリーンショット AI
が生成したコンテンツは間違っている可能性があります。](./media/image4.jpeg)

2.  **メイン** ブランチのドロップダウンで、**cd** ブランチを選択します。

![コンピューターのスクリーンショット AI
が生成したコンテンツは間違っている可能性があります。](./media/image5.jpeg)

3.  次のページで、**.github/workflows/** フォルダーに移動し、「**Add
    file**」を選択して「**Create new file**」をクリックします。

![コンピューターのスクリーンショット AI
が生成したコンテンツは間違っている可能性があります。](./media/image6.jpeg)

![コンピューターのスクリーンショット AI
が生成したコンテンツは間違っている可能性があります。](./media/image7.jpeg)

4.  **Name your file**を付ける フィールドに、publish.yml

![コンピューターのスクリーンショット AI
が生成したコンテンツは間違っている可能性があります。](./media/image8.jpeg)

5.  Add the following code to the publish.yml file.

6.  name: Publish to Docker

7.  on:

8.  push:

9.  branches:

10. \- main

11. permissions:

12. packages: write

13. contents: read

14. jobs:

15. publish:

16. runs-on: ubuntu-latest

17. steps:

18. \- name: Checkout

19. uses: actions/checkout@v4

20. \# Add your test steps here if needed...

21. \- name: Docker meta

22. id: meta

23. uses: docker/metadata-action@v5

24. with:

25. images: ghcr.io/YOURNAME/publish-packages/game

26. tags: type=sha

27. \- name: Login to GHCR

28. uses: docker/login-action@v3

29. with:

30. registry: ghcr.io

31. username: ${{ github.repository_owner }}

32. password: ${{ secrets.GITHUB_TOKEN }}

33. \- name: Build container

34. uses: docker/build-push-action@v5

35. with:

36. context: .

37. push: true

> tags: ${{ steps.meta.outputs.tags }}

38. YOURNAME をユーザー名に置き換えます。

![コンピューターのスクリーンショット AI
が生成したコンテンツは間違っている可能性があります。](./media/image9.jpeg)

39. イメージ名が一意であることを確認し、「**Commit
    chnages」**をクリックします。

![コンピューターのスクリーンショット AI
が生成したコンテンツは間違っている可能性があります。](./media/image10.jpeg)

40. もう一度「**Commit changes**」をクリックします 。

![コンピューターのスクリーンショット AI
が生成したコンテンツは間違っている可能性があります。](./media/image11.jpeg)

41. 次に、プルリクエストを作成して、上記の演習で行ったすべての変更を表示します。

42. ナビゲーションバーの **「Pull Requests**」 タブをクリックします。

43. 「**New pull
    request**」をクリックします。![コンピューターのスクリーンショット AI
    が生成したコンテンツは間違っている可能性があります。](./media/image12.jpeg)

44. 「**変更の比較」**ページで、「**base**: main と
    **compare**:cdの設定」をクリックし、「**Create pull
    request」**をクリックします。

![チャットのスクリーンショット AI
が生成したコンテンツは間違っている可能性があります。](./media/image13.jpeg)

45. 「**タイトルの追加**」ページで、「**Create pull
    request**」をクリックします。

![コンピューターのスクリーンショット AI
が生成したコンテンツは間違っている可能性があります。](./media/image14.jpeg)

46. アクションが実行されるまで 20 秒待って、結果を確認します。

![コンピューターのスクリーンショット AI
が生成したコンテンツは間違っている可能性があります。](./media/image15.jpeg)

概要：

これで、GitHub Actions を使用して Docker
イメージの公開を自動化し、デプロイ
プロセスを合理化し、最新のプロジェクト配布を維持する能力を強化する実践的な経験を積みました。
