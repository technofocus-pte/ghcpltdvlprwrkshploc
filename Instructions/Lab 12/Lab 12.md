**實驗室 12：使用 GitHub Actions 和 Microsoft Azure 創建部署工作流**

目標：

想像一下，您正在管理一個具有複雜部署要求的軟件項目，該項目涉及多個環境，包括暫存和生產。為了簡化部署過程並確保一致性，您決定使用
GitHub Actions 和 Microsoft Azure
自動執行部署過程。通過配置部署工作流，可以根據應用於拉取請求的標簽設置觸發器，這些觸發器將自動處理啟動環境、部署到暫存和拆除環境。這種方法有助於保持效率並減少部署管道中的手動干預。

在這個動手實驗室中，您將:

- 將工作流配置為在將特定標簽應用於拉取請求時使用 Azure
  資源自動創建和設置環境。

- 在工作流中設置部署任務，以便在收到相應的標簽後自動將項目部署到暫存環境。

練習 1：創建新存儲庫

1.  瀏覽到以下鏈接：https://github.com/skills/deploy-to-azure

在本實驗室中，你將使用公共模板 **skills-deploy-to-azure** 創建存儲庫

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image1.jpeg)

2.  選擇“**Use this template** ”菜單下的“**Create a new repository**”。 

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image2.jpeg)

3.  輸入以下詳細信息，然後選擇**Create Repository**。

    - 存儲庫名稱：**skills-deploy-to-azure**

    &nbsp;

    - 存儲庫類型：**Public**

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image3.jpeg)

練習 2：配置GITHUB_TOKEN權限

在每次工作流運行開始時，GitHub
會自動創建一個唯一的GITHUB_TOKEN機密以在工作流中使用。我們需要確保此令牌具有所需的權限。

1.  在新創建的存儲庫的登錄頁面上，轉到**“Settings \> Actions \> General**”。

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image4.jpeg)

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image5.jpeg)

2.  向下滾動到 **Workflow permissions** 並啟用 **Read and write
    permissions** ，然後單擊 **Save**。

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image6.jpeg)

**注意：**這是工作流將映像上傳到容器註冊表所必需的。

練習 3：根據標簽配置觸發器

1.  在導航欄上，轉到“**Actions ”**選項卡

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image7.jpeg)

2.  在 **Actions** 頁面上，單擊左側導航窗格中的 **New workflow**。 

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image8.jpeg)

3.  在“**Choose a workflow**”頁上，搜索 \\**simple
    workflow**\\，然後單擊“**Configure**” 

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image9.jpeg)

4.  將工作流命名為 deploy-staging.yml

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image10.jpeg)

5.  在編輯器頁面中，編輯文件的內容並刪除所有觸發器和作業。生成的文件如下所示。

6.  name: Stage the app

7.  on:

8.  pull_request:

9.  types: \[labeled\]

10. jobs:

11. build:

12. runs-on: ubuntu-latest

if: contains(github.event.pull_request.labels.\*.name, 'stage')

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image11.jpeg)

**注意：**請確保添加的代碼片段已正確縮進，如屏幕截圖所示

13. 單擊頁面右上角的“**Commit changes** ”按鈕。 

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image12.jpeg)

14. 在“**Commit Changes**”窗口中，選擇“**Create a new branch for this
    commit and start a pull request**”。 

**注意：Commit changes**  窗口更改為“**Propose Changes**”。

將 **new branch** 命名為 **staging-workflow**，然後單擊“**Propose
changes**”。

![A screenshot of a chat AI-generated content may be
incorrect.](./media/image13.jpeg)

15. 在“**Open a pull request** ”的下一頁上，單擊“**Create pull
    request**”。

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image14.jpeg)

16. 等待 20 秒，讓作運行並查看結果。

總結：

現在，您已經獲得了使用 GitHub Actions
自動化部署工作流程的實踐經驗，從而提高了部署過程的效率和可靠性。
