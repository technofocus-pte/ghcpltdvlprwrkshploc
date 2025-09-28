**實驗 08：創建 GitHub Action 並在工作流中使用它**

目的：

想像一下，您是一個開發團隊的一員，該團隊希望通過自動化重複性任務來簡化您的軟件開發流程。為了提高效率，您決定利用
GitHub Actions，它允許您直接在 GitHub
存儲庫中自動執行測試、部署和代碼審查等任務。通過設置 GitHub Action
並將其集成到您的工作流程中，您可以確保自動執行基本任務，從而節省時間並減少手動工作。

在這個動手實驗室中，你將：

- 在 .github/workflows
  目錄中設置工作流文件，定義內容並指定觸發工作流的事件。

- 練習將工作流文件添加並提交到存儲庫，以將 GitHub Actions
  集成到開發過程中。

練習 \#1：從公共模板創建新存儲庫

1.  瀏覽到以下鏈接： https://github.com/skills/hello-github-actions

在本練習中，你將使用公共模板“**skills-hello-github-actions**”創建存儲庫。

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image1.jpeg)

2.  選擇“**Use this template**”菜單下的“**Create a new repository**”。  

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image1.jpeg)

3.  輸入以下詳細信息，然後選擇 **Create Repository**。

    1.  存儲庫名稱：**skills-hello-github-actions**

&nbsp;

1.  存儲庫類型： **Public**

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image2.jpeg)

練習 \#2：創建工作流文件

1.  在新創建的存儲庫的登陸頁上，導航到“**Pull requests** ”選項卡。

![A screenshot of a web page AI-generated content may be
incorrect.](./media/image3.jpeg)

2.  在下一頁上，單擊“**New pull request** ”按鈕。

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image4.jpeg)

3.  在“**Compare changes** ”頁上，選擇“**base： main**”和“**compare：
    welcome-workflow**”，然後單擊“**Create pull request**”。

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image5.jpeg)

4.  在“**Open a pull request** ”頁上，單擊“**Create pull request**”。

![A screenshot of a email request AI-generated content may be
incorrect.](./media/image6.jpeg)

5.  導航到“**Code**”選項卡。 

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image7.jpeg)

6.  在下一頁上，從 **main branch dropdown** 中，單擊
    **welcome-workflow** 分支。

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image8.jpeg)

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image9.jpeg)

7.  將主分支更改為 **welcome-workflow** 後，導航到 **.github/workflows**
    文件夾，然後選擇“**Add file** ”，然後單擊“**Create new file**”。

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image10.jpeg)

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image11.jpeg)

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image12.jpeg)

8.  在文件創建頁面上，輸入文件名welcome.yml

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image13.jpeg)

9.  在編輯器頁面上，將以下內容添加到welcome.yml文件：並單擊“**Commit
    changes**”。

10. name: Post welcome comment

11. on:

12. pull_request:

13. types: \[opened\]

14. permissions:

pull-requests: write

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image14.jpeg)

15. 在“**Commit changes** ”頁上，單擊“**commit changes**”。

16. 等待 20 秒讓作運行，然後刷新此作，作將自動關閉此步驟。

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image15.jpeg)

總結：

您現在已經獲得了設置和管理 GitHub Actions
的實踐經驗，提高了自動化和優化軟件開發工作流程的能力。
