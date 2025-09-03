**实验室 07：使用 GitHub Codespaces 和 Visual Studio Code 进行编码**

目的：

想象一下，您是一名开发人员，正在从事一个需要云托管开发环境来促进协作和简化工作流程的项目。为了提高工作效率并更有效地管理开发设置，你决定将
GitHub Codespaces 与 Visual Studio Code
配合使用。此设置允许您直接在云中创建和自定义开发环境，从而更轻松地与团队协作并有效管理项目配置。

在这个动手实验室中，您将:

- 启动 Codespace：使用预定义的模板创建和启动 GitHub Codespace。

- 自定义配置：在 codespace 中自定义项目配置以满足您的开发需求。

- 管理代码空间：有效管理和导航您的代码空间，确保开发过程顺利且有组织。

- 将代码推送到存储库：练习将代码更改从 codespace 推送到 GitHub
  存储库，从而增强将开发工作与版本控制集成的能力。

练习 \#1：设置新存储库并启动 GitHub Codespace

1.  登录到你的 GitHub 帐户。

2.  浏览到以下链接：https://github.com/skills/code-with-codespaces

在本实验室中，你将使用公共模板“**skills-code-with-codespaces**”创建存储库。

![](./media/image1.jpeg)

3.  选择“**Use this template** ”菜单下的“**Create a new
    repository**”。  

![](./media/image2.jpeg)

4.  输入以下详细信息，然后选择 **Create Repository**。

    1.  存储库名称：**skills-code-with-codespaces**

<!-- -->

1.  存储库类型：**Public**

![](./media/image3.jpeg)

2.  创建存储库后，单击 **Code** 按钮。

![](./media/image4.jpeg)

3.  在弹出窗口中选择“**Codespaces**”选项卡，然后单击“**the Create
    codespace on main** ”按钮。

![](./media/image5.jpeg)

**注意：**codespace 将在新的浏览器选项卡中打开。

4.  浏览器将显示一个基于 Web 的 VS Code
    编辑器，并且应该存在一个终端，如下所示。

![](./media/image6.jpeg)

5.  等待 2 分钟，让 codespace（虚拟机）自行启动。

![](./media/image7.jpeg)

6.  导航回 skills-code-with-codespaces 存储库，然后单击“**Code**”按钮 

![](./media/image8.jpeg)

**注意：**如果未加载新创建的 codespace，请刷新页面。

7.  单击省略号 **...** 在活动 codespace 中\*\*.\*\*

**注意**：codespace 名称可能因你的情况而异

![](./media/image9.jpeg)

8.  在弹出菜单中选择“**Open in Visual Studio Code** ”。 

![](./media/image10.jpeg)

9.  弹出窗口将要求确认是否在 VS code 应用程序中打开
    codespace。选择“**Open Visual Studio Code** ”以打开 codespace。

![](./media/image11.jpeg)

10. 系统将提示你安装 GitHub Codespaces 的扩展，单击 **Install extension
    and open URI**。

![](./media/image12.jpeg)

11. 安装后，您将看到一个弹出窗口，要求提供其他权限。 **点击
    Authorize** **Visual Studio code**

![](./media/image13.jpeg)

12. 通过输入您的 GitHub 帐户密码来确认访问。

![](./media/image14.jpeg)

**注意：**如果您看到“Allow Windows Firewall
permissions”弹出窗口，请允许继续。

![](./media/image15.jpeg)

练习 \#2：将代码从 codespace 推送到存储库

1.  在 VS Code 资源管理器窗口的 codespace 中，选择index.html文件。

![](./media/image16.jpeg)

2.  将 h1 标头替换为以下内容:

\<h1\>Hello from the codespace!\</h1\>

3.  保存文件。

**注意：**文件应自动保存。

![](./media/image17.jpeg)

4.  使用 VS Code 终端通过输入以下提交消息来提交文件更改:

git commit -a -m "Adding hello from the codespace!"

![](./media/image18.jpeg)

5.  将更改推送回存储库。在 VS Code 终端中，输入:

git push

![](./media/image19.jpeg)

6.  VS 的新代码已推送到您的存储库！

7.  切换回存储库的主页并查看index.html以验证新代码是否已推送到存储库。

![](./media/image20.jpeg)

8.  等待大约 20 秒，然后刷新此 GitHub Actions 将自动更新到下一步。

总结：

现在，你已使用 GitHub Codespaces 和 Visual Studio Code 来

- 使用预定义的模板创建和启动 GitHub Codespace。

- 将代码推送到存储库：练习将代码更改从 codespace 推送到 GitHub
  存储库，从而增强将开发工作与版本控制集成的能力。

