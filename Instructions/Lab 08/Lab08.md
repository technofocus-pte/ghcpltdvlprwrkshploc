**实验 08：创建 GitHub Action 并在工作流中使用它**

目的：

想象一下，您是一个开发团队的一员，该团队希望通过自动化重复性任务来简化您的软件开发流程。为了提高效率，您决定利用
GitHub Actions，它允许您直接在 GitHub
存储库中自动执行测试、部署和代码审查等任务。通过设置 GitHub Action
并将其集成到您的工作流程中，您可以确保自动执行基本任务，从而节省时间并减少手动工作。

在这个动手实验室中，你将：

- 在 .github/workflows
  目录中设置工作流文件，定义内容并指定触发工作流的事件。

- 练习将工作流文件添加并提交到存储库，以将 GitHub Actions
  集成到开发过程中。

练习 \#1：从公共模板创建新存储库

1.  浏览到以下链接： https://github.com/skills/hello-github-actions

在本练习中，你将使用公共模板“**skills-hello-github-actions**”创建存储库。

![](./media/image1.jpeg)

2.  选择“**Use this template**”菜单下的“**Create a new repository**”。  

![](./media/image1.jpeg)

3.  输入以下详细信息，然后选择 **Create Repository**。

    1.  存储库名称：**skills-hello-github-actions**

<!-- -->

1.  存储库类型： **Public**

![](./media/image2.jpeg)

练习 \#2：创建工作流文件

1.  在新创建的存储库的登陆页上，导航到“**Pull requests** ”选项卡。

![](./media/image3.jpeg)

2.  在下一页上，单击“**New pull request** ”按钮。

![](./media/image4.jpeg)

3.  在“**Compare changes** ”页上，选择“**base： main**”和“**compare：
    welcome-workflow**”，然后单击“**Create pull request**”。

![](./media/image5.jpeg)

4.  在“**Open a pull request** ”页上，单击“**Create pull request**”。

![](./media/image6.jpeg)

5.  导航到“**Code**”选项卡。 

![](./media/image7.jpeg)

6.  在下一页上，从 **main branch dropdown** 中，单击
    **welcome-workflow** 分支。

![](./media/image8.jpeg)

![](./media/image9.jpeg)

7.  将主分支更改为 **welcome-workflow** 后，导航到 **.github/workflows**
    文件夹，然后选择“**Add file** ”，然后单击“**Create new file**”。

![](./media/image10.jpeg)

![](./media/image11.jpeg)

![](./media/image12.jpeg)

8.  在文件创建页面上，输入文件名welcome.yml

![](./media/image13.jpeg)

9.  在编辑器页面上，将以下内容添加到welcome.yml文件：并单击“**Commit
    changes**”。

10. name: Post welcome comment

11. on:

12. pull_request:

13. types: \[opened\]

14. permissions:

pull-requests: write

![](./media/image14.jpeg)

15. 在“**Commit changes** ”页上，单击“**commit changes**”。

16. 等待 20 秒让作运行，然后刷新此作，作将自动关闭此步骤。

![](./media/image15.jpeg)

总结：

您现在已经获得了设置和管理 GitHub Actions
的实践经验，提高了自动化和优化软件开发工作流程的能力。

