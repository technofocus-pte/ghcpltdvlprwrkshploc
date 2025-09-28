**實驗室 07：使用 GitHub Codespaces 和 Visual Studio Code 進行編碼**

目的：

想像一下，您是一名開發人員，正在從事一個需要雲託管開發環境來促進協作和簡化工作流程的項目。為了提高工作效率並更有效地管理開發設置，你決定將
GitHub Codespaces 與 Visual Studio Code
配合使用。此設置允許您直接在雲中創建和自定義開發環境，從而更輕鬆地與團隊協作並有效管理項目配置。

在這個動手實驗室中，您將:

- 啟動 Codespace：使用預定義的模板創建和啟動 GitHub Codespace。

- 自定義配置：在 codespace 中自定義項目配置以滿足您的開發需求。

- 管理代碼空間：有效管理和導航您的代碼空間，確保開發過程順利且有組織。

- 將代碼推送到存儲庫：練習將代碼更改從 codespace 推送到 GitHub
  存儲庫，從而增強將開發工作與版本控制集成的能力。

練習 \#1：設置新存儲庫並啟動 GitHub Codespace)

1.  登錄到你的 GitHub 帳戶。

2.  瀏覽到以下鏈接：https://github.com/skills/code-with-codespaces

在本實驗室中，你將使用公共模板“**skills-code-with-codespaces**”創建存儲庫。

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image1.jpeg)

3.  選擇“**Use this template** ”菜單下的“**Create a new
    repository**”。  

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image2.jpeg)

4.  輸入以下詳細信息，然後選擇 **Create Repository**。

    1.  存儲庫名稱：**skills-code-with-codespaces**

&nbsp;

1.  存儲庫類型：**Public**

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image3.jpeg)

2.  創建存儲庫後，單擊 **Code** 按鈕。

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image4.jpeg)

3.  在彈出窗口中選擇“**Codespaces**”選項卡，然後單擊“**the Create
    codespace on main** ”按鈕。

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image5.jpeg)

**注意：**codespace 將在新的瀏覽器選項卡中打開。

4.  瀏覽器將顯示一個基於 Web 的 VS Code
    編輯器，並且應該存在一個終端，如下所示。

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image6.jpeg)

5.  等待 2 分鐘，讓 codespace（虛擬機）自行啟動。

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image7.jpeg)

6.  導航回 skills-code-with-codespaces 存儲庫，然後單擊“**Code**”按鈕 

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image8.jpeg)

**注意：**如果未加載新創建的 codespace，請刷新頁面。

7.  單擊省略號 **...** 在活動 codespace 中\*\*.\*\*

**注意**：codespace 名稱可能因你的情況而異

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image9.jpeg)

8.  在彈出菜單中選擇“**Open in Visual Studio Code** ”。 

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image10.jpeg)

9.  彈出窗口將要求確認是否在 VS code 應用程序中打開
    codespace。選擇“**Open Visual Studio Code** ”以打開 codespace。

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image11.jpeg)

10. 系統將提示你安裝 GitHub Codespaces 的擴展，單擊 **Install extension
    and open URI**。

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image12.jpeg)

11. 安裝後，您將看到一個彈出窗口，要求提供其他權限。 **點擊
    Authorize** **Visual Studio code**

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image13.jpeg)

12. 通過輸入您的 GitHub 帳戶密碼來確認訪問。

![A screenshot of a login form AI-generated content may be
incorrect.](./media/image14.jpeg)

**注意：**如果您看到“Allow Windows Firewall
permissions”彈出窗口，請允許繼續。

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image15.jpeg)

練習 \#2：將代碼從 codespace 推送到存儲庫

1.  在 VS Code 資源管理器窗口的 codespace 中，選擇index.html文件。

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image16.jpeg)

2.  將 h1 標頭替換為以下內容:

\<h1\>Hello from the codespace!\</h1\>

3.  保存文件。

**注意：**文件應自動保存。

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image17.jpeg)

4.  使用 VS Code 終端通過輸入以下提交消息來提交文件更改:

git commit -a -m "Adding hello from the codespace!"

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image18.jpeg)

5.  將更改推送回存儲庫。在 VS Code 終端中，輸入:

git push

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image19.jpeg)

6.  VS 的新代碼已推送到您的存儲庫！

7.  切換回存儲庫的主頁並查看index.html以驗證新代碼是否已推送到存儲庫。

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image20.jpeg)

8.  等待大約 20 秒，然後刷新此 GitHub Actions 將自動更新到下一步。

總結：

現在，你已使用 GitHub Codespaces 和 Visual Studio Code 來

- 使用預定義的模板創建和啟動 GitHub Codespace。

- 將代碼推送到存儲庫：練習將代碼更改從 codespace 推送到 GitHub
  存儲庫，從而增強將開發工作與版本控制集成的能力。
