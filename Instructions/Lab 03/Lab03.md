**实验室 03：使用 GitHub Pages 和 Jekyll 创建在线作品集**

目的：

想象一下，您是一家科技初创公司的一名崭露头角的软件开发人员，渴望通过在线作品集展示您的项目、技能和经验。您需要一个专业的平台来展示您的作品，因此您决定使用
GitHub Pages 创建一个个人网站或博客。该平台允许您利用 GitHub
存储库轻松发布和维护您的网站。

在这个动手实验室中，您将:

- 创建 GitHub 存储库：设置一个新存储库，作为您个人站点的基础。

- 启用 GitHub Pages：将 GitHub Pages 配置为直接从存储库托管您的网站。

<!-- -->

- 使用 Jekyll 部署您的第一个站点：利用流行的静态站点生成器
  Jekyll，以最小的努力构建和部署具有专业外观的网站.

练习 \#1：从模板创建存储库

1.  登录到你的 GitHub 帐户。

2.  浏览到以下链接: https://github.com/skills/github-pages

在本练习中，你将使用公共模板“**skills-github-pages**”创建存储库。

![](./media/image1.jpeg)

3.  选择“**Use this template**”菜单下的“**Create a new repository**”。  

![](./media/image2.jpeg)

4.  输入以下详细信息，然后选择 **Create Repository**。

    1.  存储库名称: **skills-github-pages**

    2.  存储库类型: **Public**

![](./media/image3.jpeg)

练习 \#2：启用 GitHub 页面

1.  创建存储库后，导航到主页。在主导航窗格中，单击“**Settings**”图标。 

![](./media/image4.jpeg)

2.  在设置页面中，向下滚动到代码和自动化，然后单击 **Pages**。

![](./media/image5.jpeg)

3.  在 GitHub 页面上，确保从“**Source**”下拉菜单中选择“**Deploy from a
    branch**”，然后从“**Branch**”下拉菜单中选择“**main**”。

![](./media/image6.jpeg)

4.  点击 **Save**  按钮继续。

![](./media/image7.jpeg)

5.  将保存 GitHub Pages 源代码。等待大约一分钟，然后刷新此页面。GitHub
    Actions 将自动更新到下一步。

![](./media/image8.jpeg)

6.  您的网站现已上线。

![](./media/image9.jpeg)

7.  单击访问站点按钮以查看您的站点。你打开了 GitHub 页面。

![](./media/image10.jpeg)

练习 \#3：使用 Jekyll 部署您的站点

您将在分支 my-pages
中工作，以使这个网站看起来很棒。在本实验中，我们将使用博客就绪主题。“minima”。

Jekyll 使用名为 **\_config.yml**
的文件来存储您的网站、主题和可重用内容（如网站标题和 GitHub
句柄）的设置。

1.  选择存储库的**“Code**”选项卡

![](./media/image11.jpeg)

2.  展开**main **分支并选择 **my-pages**。

![](./media/image12.jpeg)

在 **my-pages** 分支中，**\_config.yml**浏览到文件

![](./media/image13.jpeg)

3.  打开右上角的文件编辑器。

![](./media/image14.jpeg)

4.  添加主题：设置为 **minima**，使其在**\_config.yml**文件中显示如下：

![](./media/image15.jpeg)

5.  单击**“Commit Changes”**按钮以保存更改。

![](./media/image16.jpeg)

**注意：**等待大约一分钟，然后刷新此页面。GitHub Actions
将自动更新到下一步。

6.  要检查更新的网站，请单击 GitHub 页面下的 **Visit site** 按钮。

![](./media/image17.jpeg)

7.  将应用所选主题。您可以继续修改其他配置变量，例如 title：、author：
    和 description：，以进一步自定义您的网站

![](./media/image18.jpeg)

总结：

您现在已经创建了一个包含 GitHub
页面的网站并应用了主题。您可以利用此经验创建一个实时网站，您可以在其中不断更新和展示您的软件开发之旅，使雇主、合作者和技术社区更容易看到您的工作和技能。

