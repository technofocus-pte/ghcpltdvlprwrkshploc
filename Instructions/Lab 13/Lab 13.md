**實驗 13：編寫 GitHub JavaScript Action
並自動執行工作流特有的自定義任務**

目標：

想像一下，您的任務是創建一個自定義 GitHub
Action，以自動執行工作流程中的特定任務。首先，您需要設置一個開發環境來編寫和測試您的
JavaScript Action。這涉及初始化一個新的 JavaScript
項目、配置項目結構以及安裝必要的依賴項。通過執行本練習中的步驟，您將為開發
GitHub Action 奠定堅實的基礎，從而允許您構建適合項目需求的自動化。

在這個動手實驗室中，你將：

- 克隆存儲庫：將提供的存儲庫克隆到本地計算機以開始開發過程。

- 導航到項目文件夾：移動到克隆的存儲庫文件夾，您將在其中設置作。

- 創建作文件夾：在存儲庫中專門為您的作文件設置一個新文件夾。

- 初始化 npm 項目：在作文件夾中初始化一個新的 npm
  項目，以管理依賴關係和配置。

- 安裝依賴項：使用 npm 安裝開發 GitHub JavaScript作所需的必要依賴項。

- 準備作開發：配置您的項目環境以開始編寫和測試您的自定義 GitHub
  JavaScript Action。

練習：1 創建新存儲庫

1.  瀏覽到以下鏈接：https://github.com/skills/write-javascript-actions

在本實驗中，您將使用公共模板 **skills-write-javascript-actions**
創建存儲庫

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image1.jpeg)

2.  選擇“**Use this template**”菜單下的“**Create a new repository** ”。 

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image2.jpeg)

3.  輸入以下詳細信息，然後選擇 **Create Repository**。

    1.  存儲庫名稱：**skills-write-javascript-actions**

&nbsp;

1.  存儲庫類型: **Public**

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image3.jpeg)

練習 \#2：初始化新的 JavaScript 項目

在本地安裝必要的工具後，請按照以下步驟開始創建您的第一個作。

1.  在 **write-javascript-actions** 存儲庫的登錄頁面上，單擊
    **Code**（綠色的）按鈕，然後複製 **Local** 選項卡下的 HTTPS URL。 

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image4.jpeg)

2.  現在打開**Command prompt** 並將您的技能存儲庫克隆到本地計算機：

git clone \<this repository URL\>.git

![A screenshot of a computer program AI-generated content may be
incorrect.](./media/image5.jpeg)

**注意：**通常它會克隆到以下路徑“**C：\Users\Admin\skills-write-javascript-actions**”

3.  導航到您剛剛克隆的文件夾：

cd C:\Users\Admin\skills-write-javascript-actions

![A screenshot of a computer program AI-generated content may be
incorrect.](./media/image6.jpeg)

4.  我們將使用名為 main 的分支。

git switch main

![A screenshot of a computer program AI-generated content may be
incorrect.](./media/image7.jpeg)

5.  為我們的作文件創建一個新文件夾:

mkdir -p .github\actions\joke-action

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image8.jpeg)

6.  導航到您剛剛創建的 joke-action 文件夾:

cd .github/actions/joke-action

![A screenshot of a computer program AI-generated content may be
incorrect.](./media/image9.jpeg)

7.  初始化新項目:

npm init -y

![A screenshot of a computer program AI-generated content may be
incorrect.](./media/image10.jpeg)

8.  使用 GitHub ToolKit （https://github.com/actions/toolkit） 中的 npm
    安裝 request、request-promise 和 \\actions/core 依賴項：

Npm install -save request request-promise @actions/core

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image11.jpeg)

9.  提交這些新添加的文件，我們將在後面的步驟中消除上傳node_modules的需要:

git add . && git commit -m "add project dependencies"

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image12.jpeg)

**注意：**如果系統提示輸入用戶電子郵件和用戶名，請輸入以下命令並替換詳細信息。

![A screen shot of a computer AI-generated content may be
incorrect.](./media/image13.jpeg)

git config --global user.email "your_email@example.com"

git config --global user.name "Your Name"

**注意**：替換為您的詳細信息。

10. 將更改推送到存儲庫：輸入以下命令並登錄

git push

![A computer screen with white text AI-generated content may be
incorrect.](./media/image14.jpeg)

**注意：**當提示授權時，登錄 GitHub 帳戶並繼續該過程。

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image15.jpeg)

![A screenshot of a login form AI-generated content may be
incorrect.](./media/image16.jpeg)

![A screenshot of a computer error AI-generated content may be
incorrect.](./media/image17.jpeg)

11. 等待大約 20 秒，讓 GitHub Actions 自動刷新頁面以進行進一步處理。

總結：

您現在已經建立了一個強大的開發環境來創建和管理 GitHub JavaScript
Action，為自動化和增強工作流程奠定了基礎。
