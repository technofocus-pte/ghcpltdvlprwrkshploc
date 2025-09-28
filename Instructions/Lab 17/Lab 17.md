**實驗 17：在 GitHub 存儲庫中啟用機密掃描並提交令牌**

假設您是一名軟件開發人員，正在處理一個具有共享 GitHub
存儲庫的團隊項目。為了確保您的代碼保持安全且不會意外洩漏，您決定實施機密掃描---該功能有助於識別可能無意中提交到存儲庫的敏感信息，例如
API 令牌或密碼。

目的：

在這個動手實驗室中，你將：

1.  啟用 Secret Scanning：在 GitHub 存儲庫上配置 secret scanning
    以自動檢測和標記敏感信息。

2.  提交令牌：有意向存儲庫添加令牌或其他敏感信息，以測試秘密掃描功能的有效性。

練習 \#1：創建 GitHub repository 並啟用機密掃描

任務 \#1：使用模板創建存儲庫

1.  登錄到你的 GitHub 帳戶。

2.  瀏覽到以下鏈接：https://github.com/skills/introduction-to-secret-scanning

在本練習中，您將使用公共模板“**skills-introduction-to-secret-scanning**”創建存儲庫。

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image1.jpeg)

3.  選擇“**Use this template** ”菜單下的“**Create a new
    repository**”。  

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image2.jpeg)

4.  輸入以下詳細信息，然後選擇 **Create Repository**。

    1.  存儲庫名稱：**skills-introduction-to-secret-scanning**

&nbsp;

1.  存儲庫類型：**Public**

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image3.jpeg)

任務 \#2：啟用機密掃描

1.  在新創建的存儲庫的登錄頁上，從 頂部導航欄中選擇“**Settings**”。

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image4.jpeg)

2.  在邊欄的“**Security**”部分中，選擇“**Code security and analysis**”。

**注意**：您需要向下滾動才能看到“**Security”**菜單

![A screenshot of a browser window AI-generated content may be
incorrect.](./media/image5.jpeg)

3.  向下滾動到頁面底部，然後單擊 **Enable** 進行機密掃描。

**注意：**如果看到**“Disable ”**按鈕，則表示已為存儲庫啟用了 secret
scanning。

![A white background with black text AI-generated content may be
incorrect.](./media/image6.jpeg)

如果尚未啟用，您將看到“**Enable”**按鈕，如下所示：

![A screenshot of a computer error AI-generated content may be
incorrect.](./media/image7.jpeg)

**注意：** 啟用 secret scanning
後，將向與帳戶關聯的郵件標識發送有關存儲庫中憑證的電子郵件通知。此技能存儲庫中的令牌處於非活動狀態。對環境沒有風險。

現在，在此存儲庫中啟用了 secret
scanning，讓我們提交一個新令牌以查看它是如何工作的。

練習 \#2：提交令牌

在本練習中，您將向存儲庫提交 AWS 密鑰和訪問
ID。這是一個非活動令牌，不能用於登錄 AWS。

1.  在主導航欄的左上窗格中，單擊**“Code**”選項卡，然後選擇**credentials.yml**文件。

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image8.jpeg)

2.  單擊右側的 Edit 按鈕。

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image9.jpeg)

3.  複製以下文本並將其粘貼到 **credentials.yml**
    文件編輯窗格中的現有代碼下方 。

4.  default:

5.  aws_access_key_id: AKIAQYLPMN5HNM4OZ56B

6.  aws_secret_access_key: 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

7.  output: json

region: us-east-2

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image10.jpeg)

8.  單擊右上角的“**Commit changes** ”按鈕，然後在“**Commit
    Changes** ”窗口中再次單擊“**Commit Changes** ”。

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image11.jpeg)

**注意：**提交更改後，你將在與 GitHub 帳戶關聯的郵箱中收到警報。

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image12.jpeg)

總結：

現在，您已經對如何啟用和測試機密掃描以保護您的代碼和數據有了實際的瞭解。

