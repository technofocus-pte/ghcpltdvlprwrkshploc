**实验 09：创建工作流以对项目使用持续集成 （CI）**

目标：

想象一下，您正在从事一个软件项目，其中保持高质量标准至关重要。为了确保代码保持健壮且没有错误，您决定使用
GitHub Actions 实现持续集成 （CI）。CI
有助于在每次对代码库进行更改时自动执行运行测试和检查代码质量的过程。通过创建
CI 工作流程，您可以自动对 Markdown 文件进行
lint、运行测试并立即接收有关代码质量的反馈，确保您的项目始终符合其质量标准。

在这个动手实验室中，你将：

- 创建测试工作流程：设置专门设计用于 lint Markdown 文件并检查格式问题的
  GitHub Actions 工作流程。

- 配置和更新工作流程：练习配置工作流文件以定义自动 linting
  所需的作业和步骤，并根据需要进行更新以增强其功能。

- 创建拉取请求：通过创建拉取请求来集成更改，允许您测试 CI
  工作流程并观察它如何自动执行质量检查。

- 分析 CI 工作流的结果，了解它如何报告问题并确保代码质量。

练习 \#1：从公共模板创建新存储库

1.  浏览到以下链接：https://github.com/skills/test-with-actions

在本练习中，你将使用公共模板“**skills-test-with-actions**”创建存储库。

![](./media/image1.jpeg)

2.  选择“**Use this template** ”菜单下的“**Create a new repository**”。 

![](./media/image2.jpeg)

3.  输入以下详细信息，然后选择 **Create Repository**。

    1.  存储库名称：**skills-test-with-actions**

<!-- -->

1.  存储库类型: **Public**

![](./media/image3.jpeg)

练习 \#2：添加测试工作流

1.  导航到不久前创建的存储库中的作选项卡。

![](./media/image4.jpeg)

2.  在左侧边栏的“Actions”下，选择“**New workflow**”。

![](./media/image5.jpeg)

3.  在“**Choose a workflow** ”页上，导航到“**Simple
    workflow**”，然后单击“**Configure**”。

![](./media/image6.jpeg)

4.  在下一页上，将工作流重命名为
    ci.yml，并通过删除最后两个步骤来更新工作流。

![](./media/image7.jpeg)

![](./media/image8.jpeg)

5.  在工作流末尾添加以下代码，然后单击右上角的 **Commit changes** 。

6.  \- name: Run markdown lint

7.  run: \|

8.  npm install remark-cli remark-preset-lint-consistent

npx remark . --use remark-preset-lint-consistent

**注意：**请确保添加到工作流的代码片段已正确缩进

![](./media/image9.jpeg)

![](./media/image10.jpeg)

9.  在“**Commit changes** ”窗口中，选择“**Create a new branch for this
    commit and start a pull request**”。

![](./media/image11.jpeg)

10. 选择“**Create a new branch for this commit and start a pull
    request**”后，“**Commit changes** ”窗口更改为“**Propose
    Changes** ”窗口。现在点击 **Propose changes**。  

![](./media/image12.jpeg)

11. 在“**Open a pull request**”的下一页上，单击“**Create pull
    request**”。

![](./media/image13.jpeg)

12. 等待 20 秒，然后刷新此页面以分析结果。

![](./media/image14.jpeg)

总结：

您现在已经获得了使用 GitHub Actions 进行 CI
实践的实践经验，从而增强了您在软件项目中自动化和维护高质量标准的能力。

