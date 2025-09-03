**实验室 10：使用 GitHub Actions 将项目发布到 Docker 映像**

目标：

想象一下，您正在开发一个软件项目，想要将其打包并分发为 Docker
映像。为了简化部署过程并确保 Docker 映像一致地发布到 GitHub
Packages，您决定使用 GitHub Actions
进行自动化。这将允许您设置一个工作流程，在进行更改时自动发布 Docker
映像，确保您的项目始终是最新的并可用于部署。

在这个动手实验室中，您将:

- 设置 GitHub Actions 工作流文件，以自动执行生成和发布 Docker
  映像的过程。

- 配置工作流以构建 Docker 镜像并将其推送到 GitHub
  Packages，确保正确发布镜像。

- 创建拉取请求以查看所做的所有更改。

练习 \#1：从公共模板创建新存储库

1.  浏览到以下链接：https://github.com/skills/publish-packages

在本实验中，你将使用公共模板“**skills-publish-packages**”创建存储库。

![](./media/image1.jpeg)

2.  选择“**Use this template**”菜单下的“**Create a new repository** ”。 

![](./media/image2.jpeg)

3.  输入以下详细信息，然后选择 **Create Repository**。

    - 存储库名称：**skills-publish-packages**

    <!-- -->

    - 存储库类型：**Public**

![](./media/image3.jpeg)

练习 2：创建工作流文件并配置工作流

1.  单击刚刚创建的存储库中主导航栏上的**Code** 按钮。

![](./media/image4.jpeg)

2.  在**main**分支下拉列表中，选择 **cd** 分支。

![](./media/image5.jpeg)

3.  在下一页上，导航到 **.github/workflows/** 文件夹，然后选择“**Add
    file** ”，然后单击“**Create new file**”。

![](./media/image6.jpeg)

![](./media/image7.jpeg)

4.  在**Name your file** ”字段中，输入publish.yml

![](./media/image8.jpeg)

5.  将以下代码添加到 **publish.yml** 文件中。

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

31. username: \${{ github.repository_owner }}

32. password: \${{ secrets.GITHUB_TOKEN }}

33. \- name: Build container

34. uses: docker/build-push-action@v5

35. with:

36. context: .

37. push: true

tags: \${{ steps.meta.outputs.tags }}

38. 将 YOURNAME 替换为您的用户名。

![](./media/image9.jpeg)

39. 确保镜像名称是唯一的，单击“**Commit changes**”。

![](./media/image10.jpeg)

40. 再次单击“**Commit changes** ”。

![](./media/image11.jpeg)

41. 现在创建一个拉取请求，以查看在上述练习中所做的所有更改。

42. 单击导航栏上的 **Pull Requests** 选项卡。

43. 单击“**New pull request**”。 

![](./media/image12.jpeg)

44. 在“**Comparing changes** ”页上，设置 **base**： main 和
    **compare**：cd，然后单击“**Create pull request**”。

![](./media/image13.jpeg)

45. 在“**Add a title** ”页上，单击“**Create pull request**”。

![](./media/image14.jpeg)

46. 等待 20 秒，让作运行并查看结果。

![](./media/image15.jpeg)

总结：

您现在已经获得了使用 GitHub Actions 自动发布 Docker
映像的实践经验，从而增强了简化部署流程和维护最新项目分发的能力。

