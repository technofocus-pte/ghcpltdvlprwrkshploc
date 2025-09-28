**實驗室 10：使用 GitHub Actions 將項目發佈到 Docker 映像**

目標：

想像一下，您正在開發一個軟件項目，想要將其打包並分發為 Docker
映像。為了簡化部署過程並確保 Docker 映像一致地發佈到 GitHub
Packages，您決定使用 GitHub Actions
進行自動化。這將允許您設置一個工作流程，在進行更改時自動發佈 Docker
映像，確保您的項目始終是最新的並可用於部署。

在這個動手實驗室中，您將:

- 設置 GitHub Actions 工作流文件，以自動執行生成和發佈 Docker
  映像的過程。

- 配置工作流以構建 Docker 鏡像並將其推送到 GitHub
  Packages，確保正確發佈鏡像。

- 創建拉取請求以查看所做的所有更改。

練習 \#1：從公共模板創建新存儲庫

1.  瀏覽到以下鏈接：https://github.com/skills/publish-packages

在本實驗中，你將使用公共模板“**skills-publish-packages**”創建存儲庫。

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image1.jpeg)

2.  選擇“**Use this template**”菜單下的“**Create a new repository** ”。 

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image2.jpeg)

3.  輸入以下詳細信息，然後選擇 **Create Repository**。

    - 存儲庫名稱：**skills-publish-packages**

    &nbsp;

    - 存儲庫類型：**Public**

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image3.jpeg)

練習 2：創建工作流文件並配置工作流

1.  單擊剛剛創建的存儲庫中主導航欄上的**Code** 按鈕。

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image4.jpeg)

2.  在**main**分支下拉列表中，選擇 **cd** 分支。

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image5.jpeg)

3.  在下一頁上，導航到 **.github/workflows/** 文件夾，然後選擇“**Add
    file** ”，然後單擊“**Create new file**”。

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image6.jpeg)

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image7.jpeg)

4.  在**Name your file** ”字段中，輸入publish.yml

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image8.jpeg)

5.  將以下代碼添加到 **publish.yml** 文件中。

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

tags: ${{ steps.meta.outputs.tags }}

38. 將 YOURNAME 替換為您的用戶名。

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image9.jpeg)

39. 確保鏡像名稱是唯一的，單擊“**Commit changes**”。

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image10.jpeg)

40. 再次單擊“**Commit changes** ”。

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image11.jpeg)

41. 現在創建一個拉取請求，以查看在上述練習中所做的所有更改。

42. 單擊導航欄上的 **Pull Requests** 選項卡。

43. 單擊“**New pull request**”。 

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image12.jpeg)

44. 在“**Comparing changes** ”頁上，設置 **base**： main 和
    **compare**：cd，然後單擊“**Create pull request**”。

![A screenshot of a chat AI-generated content may be
incorrect.](./media/image13.jpeg)

45. 在“**Add a title** ”頁上，單擊“**Create pull request**”。

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image14.jpeg)

46. 等待 20 秒，讓作運行並查看結果。

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image15.jpeg)

總結：

您現在已經獲得了使用 GitHub Actions 自動發佈 Docker
映像的實踐經驗，從而增強了簡化部署流程和維護最新項目分發的能力。
