实验 16：从 Git Repository 中删除提交历史记录

客观的：

想象一下，您是开发团队的一员，从事一个项目，其中敏感信息（例如 API
密钥或数据库凭据）被意外提交到您的 Git repository 中。使用 Git
删除意外提交可能很棘手。

在本练习中，您将：

- 使用意外提交的敏感数据克隆存储库。

- 从克隆的存储库中删除/删除包含敏感数据的文件，然后提交删除。

- 将更改推送到 GitHub：将更新的存储库上传到 GitHub 以反映更改。

### **练习 #1：使用意外提交历史记录（敏感数据）创建存储库**

1.  登录到你的 GitHub 帐户。

2.  浏览到以下链接：<https://github.com/skills/change-commit-history>

> 在本实验中，你将使用公共模板“**skills-change-commit-history**”创建存储库。
>
> ![](./media/image1.png)

3.  选择“**Use this template**”菜单下的“**Create a new repository**”。

> ![](./media/image2.png)

4.  输入以下详细信息，然后选择创建存储库。.

- 存储库名称： **skills-change-commit-history**

- 存储库类型： **Public**

![](./media/image3.png)

### 练习 \# 2：删除/删除包含敏感数据的文件（项目根目录中的 .env）

1.  在克隆存储库的登录页面上，导航到 **Code\>Local\>HTTPS** 并复制 URL。

![](./media/image5.png)

2.  打开 Windows Powershell 并输入以下命令。

**git clone <span class="mark">\<your-repository-url\></span>**

**注意**：替换为您在步骤 1 中复制的 URL。

> ![](./media/image5.png)

3.  切换到您的存储库目录，输入以下命令。

**+++cd “C:\Users\Admin\skills-change-commit-history”+++**

**注意**：替换为存储库名称

> ![](./media/image6.png)

4.  执行以下命令从根目录中删除 .env，

**+++git rm .env**+++

> ![](./media/image7.png)

5.  提交删除 .env 文件

**+++git commit -m "remove .env file”+++**

> ![](./media/image8.png)
>
> **提示**：如何从 Git 历史记录中完全删除 .env
> 文件并使用新的提交哈希重写总历史记录？
>
> 使用以下命令可以：

- 从 Git 历史记录中完全删除 .env 文件并重写总历史记录

> **git filter-branch --force --index-filter 'git rm --cached
> --ignore-unmatch.env' --prune-empty --tag-name-filter cat -- --all**

- 将删除推送到 GitHub

> **git push origin --force –all**

6.  将删除推送到 GitHub:

**git push**

> ![](./media/image9.png)

总结：

现在，您已经完成了 Git
存储库的清理，确保敏感内容不会在存储库的历史记录中暴露。

