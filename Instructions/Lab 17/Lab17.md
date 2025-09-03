**实验 17：在 GitHub 存储库中启用机密扫描并提交令牌**

假设您是一名软件开发人员，正在处理一个具有共享 GitHub
存储库的团队项目。为了确保您的代码保持安全且不会意外泄漏，您决定实施机密扫描---该功能有助于识别可能无意中提交到存储库的敏感信息，例如
API 令牌或密码。

目的：

在这个动手实验室中，你将：

1.  启用 Secret Scanning：在 GitHub 存储库上配置 secret scanning
    以自动检测和标记敏感信息。

2.  提交令牌：有意向存储库添加令牌或其他敏感信息，以测试秘密扫描功能的有效性。

练习 \#1：创建 GitHub repository 并启用机密扫描

任务 \#1：使用模板创建存储库

1.  登录到你的 GitHub 帐户。

2.  浏览到以下链接：https://github.com/skills/introduction-to-secret-scanning

在本练习中，您将使用公共模板“**skills-introduction-to-secret-scanning**”创建存储库。

![](./media/image1.jpeg)

3.  选择“**Use this template** ”菜单下的“**Create a new
    repository**”。  

![](./media/image2.jpeg)

4.  输入以下详细信息，然后选择 **Create Repository**。

    1.  存储库名称：**skills-introduction-to-secret-scanning**

<!-- -->

1.  存储库类型：**Public**

![](./media/image3.jpeg)

任务 \#2：启用机密扫描

1.  在新创建的存储库的登录页上，从 顶部导航栏中选择“**Settings**”。

![](./media/image4.jpeg)

2.  在边栏的“**Security**”部分中，选择“**Code security and analysis**”。

**注意**：您需要向下滚动才能看到“**Security”**菜单

![](./media/image5.jpeg)

3.  向下滚动到页面底部，然后单击 **Enable** 进行机密扫描。

**注意：**如果看到**“Disable ”**按钮，则表示已为存储库启用了 secret
scanning。

![](./media/image6.jpeg)

如果尚未启用，您将看到“**Enable”**按钮，如下所示：

![](./media/image7.jpeg)

**注意：** 启用 secret scanning
后，将向与帐户关联的邮件标识发送有关存储库中凭证的电子邮件通知。此技能存储库中的令牌处于非活动状态。对环境没有风险。

现在，在此存储库中启用了 secret
scanning，让我们提交一个新令牌以查看它是如何工作的。

练习 \#2：提交令牌

在本练习中，您将向存储库提交 AWS 密钥和访问
ID。这是一个非活动令牌，不能用于登录 AWS。

1.  在主导航栏的左上窗格中，单击**“Code**”选项卡，然后选择**credentials.yml**文件。

![](./media/image8.jpeg)

2.  单击右侧的 Edit 按钮。

![](./media/image9.jpeg)

3.  复制以下文本并将其粘贴到 **credentials.yml**
    文件编辑窗格中的现有代码下方 。

4.  default:

5.  aws_access_key_id: AKIAQYLPMN5HNM4OZ56B

6.  aws_secret_access_key: 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

7.  output: json

region: us-east-2

![](./media/image10.jpeg)

8.  单击右上角的“**Commit changes** ”按钮，然后在“**Commit
    Changes** ”窗口中再次单击“**Commit Changes** ”。

![](./media/image11.jpeg)

**注意：**提交更改后，你将在与 GitHub 帐户关联的邮箱中收到警报。

![](./media/image12.jpeg)

总结：

现在，您已经对如何启用和测试机密扫描以保护您的代码和数据有了实际的了解。

