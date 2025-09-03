**实验 04：查看拉取请求并解决合并冲突**

目的：

想象一下，您是开发团队的一员，负责一个有多个贡献者的项目。随着更改的进行，审查这些更改并确保每个人的工作顺利集成至关重要。您需要通过管理拉取请求和解决合并冲突来有效协作，以维护项目的完整性并避免中断。

在这个动手实验室中，你将重点介绍 GitHub 上协作的两个关键方面:

- 创建拉取请求：选择适当的分支，提供标题和描述，然后提交拉取请求以提出更改建议。

- 审查拉取请求：检查拉取请求中提出的更改，确保它们符合项目标准并准备好进行集成。

- 解决合并冲突：练习解决不同分支中的更改影响文件的相同部分时出现的冲突，确保顺利集成和协作。

练习 \#1：从模板创建存储库并创建拉取请求

拉取请求将向其他人显示分支中的更改。此拉取请求将保留您刚刚在分支上所做的更改，并建议将它们应用于主分支。

1.  登录到你的 GitHub 帐户。

2.  浏览到以下链接：https://github.com/skills/review-pull-requests

在本练习中，你将使用公共模板“**skills-review-pull-requests**”创建存储库。

![](./media/image1.jpeg)

3.  选择“**Create a new repository**”菜单下的“**Use this template**”。  

![](./media/image2.jpeg)

4.  输入以下详细信息，然后选择 **Create Repository**。

    1.  存储库名称: **skills-review-pull-requests**

    2.  存储库类型: **Public**

![](./media/image3.jpeg)

5.  在主导航页上，选择“**Pull requests** ”选项卡。

![](./media/image4.jpeg)

6.  在下一页上，选择“**New pull request**”。

![](./media/image5.jpeg)

7.  在“**Compare changes”**页上:

    1.  在 **base**： 下拉列表中，选择
        **main**（默认情况下处于选中状态）

    2.  在 **compare**： 下拉列表中，选择 **update-game**，

通常需要等待几秒钟并刷新页面才能查看分支。

![](./media/image6.jpeg)

![](./media/image7.jpeg)

8.  在**compare:**下拉列表中选择 **update-game** 后，将打开“**Comparing
    changes**”窗口。单击**Create pull request**。

![](./media/image8.jpeg)

9.  在“**Open a pull request”页上，**输入以下内容:

    1.  为拉取请求**添加标题**：更新游戏结束消息

    2.  为您的拉取请求**添加描述**：更新游戏结束消息，以便人们知道如何玩

10. 单击 **Create pull request**。 

![](./media/image9.jpeg)

11. 等待大约 20 秒，然后刷新此页面。GitHub Actions 将自动更新到下一步。

![](./media/image10.jpeg)

练习 \#2：更新拉取请求并解决合并冲突

1.  浏览到以下链接：https://github.com/skills/resolve-merge-conflicts

在本练习中，你将使用公共模板“**skills-resolve-merge-conflicts**”创建存储库。

![](./media/image11.jpeg)

2.  选择“**Use this template** ”菜单下的“**Create a new repository** ”。

![](./media/image12.jpeg)

3.  输入以下详细信息，然后选择**Create Repository**。

    - 存储库名称: **skills-resolve-merge-conflicts**

    - 存储库类型: **Public**

![](./media/image13.jpeg)

4.  创建存储库后，选择主导航栏上的“**Pull request** ”选项卡。

![](./media/image14.jpeg)

5.  单击“**New pull request** ”按钮。

![](./media/image15.jpeg)

6.  通过选择以下选项创建拉取请求:

    - **my-resume** 作为 head 分支，并将

    - **main** 作为比较分支。

![](./media/image16.jpeg)

![](./media/image17.jpeg)

7.  单击**“Create pull request”**按钮

8.  在“**Open a pull
    request** ”页上，输入标题为“解决合并冲突”，然后单击“**Create pull
    request**”。

![](./media/image18.jpeg)

9.  等待 20 秒，让 GitHub Actions
    自动更新，页面显示冲突的详细信息（如果有）。

![](./media/image19.jpeg)

10. 单击 **Resolve conflicts** 以继续。 

![](./media/image20.jpeg)

11. 查看冲突并解决它们。

![](./media/image21.jpeg)

12. 在本练习中，让我们删除行项目冲突，然后单击** Mark as resolved**
    按钮。

![](./media/image22.jpeg)

13. 单击**“Commit merge ”**按钮并选中提醒消息框。

![](./media/image23.jpeg)

14. 点击 **I understand, continue updating main。**
    您将看到最终检查结果\*\*。

![](./media/image24.jpeg)

**总结：**

现在，你已经完成了冲突的拉取请求的创建和审查以及解决冲突，这是在 GitHub
上进行有效团队合作和项目管理的基本技能。

