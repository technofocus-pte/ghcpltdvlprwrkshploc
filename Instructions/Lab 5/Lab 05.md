**實驗 05：使用基於 GitHub 發佈的工作流管理軟件版本**

目的：

想像一下，您是軟件開發團隊的一員，從事一個需要定期更新和發佈的項目。為了有效地管理您的軟件，您決定使用
GitHub
實現基於發佈的工作流。此工作流程可幫助您有效地處理版本控制和管理軟件迭代，確保跟蹤每個版本，並以受控方式解決問題。

在這個動手實驗室中，您將

- 創建存儲庫：設置名為 skills-release-based-workflow
  的存儲庫，作為基於發佈的工作流的基礎。

- 實施版本控制：探索版本控制的概念以及跟蹤軟件迭代的重要性。

- 創建測試版：按照步驟為當前代碼庫創建測試版，包括在 GitHub
  上標記和發佈。

- 模擬真實場景：向代碼庫引入錯誤，模擬在發佈工作流程中識別和解決問題的常見場景。

練習 \#1：設置新的存儲庫（作為基於發佈的工作流的基礎)

1.  登錄到你的 GitHub 帳戶。

2.  瀏覽到以下鏈接：https://github.com/skills/release-based-workflow

在本練習中，你將使用公共模板“**skills-release-based-workflow**”創建存儲庫。

![](./media/image1.jpeg)

3.  選擇“**Use this template** ”菜單下的“**Create a new repository** ”。

![](./media/image2.jpeg)

4.  輸入以下詳細信息，然後選擇**Create Repository**。

    1.  存儲庫名稱: **skills-release-based-workflow**

    2.  存儲庫類型: **Public**

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image3.jpeg)

練習 \#2：為當前代碼庫創建版本

在本練習中，我們將在 GitHub 上為此存儲庫創建一個版本。

- GitHub Releases 指向特定的提交。

- 版本可以包括 Markdown 文件和附加二進制文件中的發行說明。

注意：在將基於版本的工作流用於較大的版本之前，讓我們先創建一個標記和一個版本。

1.  創建存儲庫後（在練習 \#1
    中），導航到頁面右側邊欄上的“**Releases**”，然後單擊“**Create a new
    release**”。 

![](./media/image4.jpeg)

提示：要訪問此頁面，請單擊 存儲庫頂部的代碼選項卡。然後，在
右側邊欄中找到“**Releases**”部分。

1.  在“**Releases/Tags**”頁面上，輸入以下內容:

    - 將 **Target** 保持為主目標

    - 在“ **Choose a Tag**”字段中，指定一個數字。

在這種情況下，請使用 v0.9 並選擇 **Create new tag v0.9 on publish**

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image5.jpeg)

1.  為版本指定一個標題，例如“第一個測試版”版本

**注意：**您也可以為版本提供簡短說明。

![](./media/image6.jpeg)

2.  向下滾動頁面以選中 **Set as a pre-release**
    旁邊的複選框，因為它代表測試版，然後單擊 **Publish** **release**。

![A screenshot of a phone AI-generated content may be
incorrect.](./media/image7.jpeg)

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image8.jpeg)

練習 \#3：引入 bug（稍後修復）

為了為以後奠定基礎，現在讓我們添加一個
bug，我們將在以後的步驟中作為發佈工作流的一部分修復該
bug。已經在存儲庫中為你創建了一個分支“update-text-colors”（在練習 \#1
中創建），所以讓我們創建一個拉取請求並將其與此分支合併。

1.  在主導航欄上，單擊**“Pull requests”**選項卡。

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image9.jpeg)

2.  在下一頁上，單擊“**New pull request**”。

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image10.jpeg)

3.  在“**Compare changes**”頁上，選擇以下內容，然後單擊“**Create pull
    request**”， 

    1.  base: **release-v1.0** 和

    2.  compare: **update-text-colors**.

![](./media/image11.jpeg)

4.  在“**Open a pull request**”頁上，輸入以下內容，然後單擊“**Create
    pull request**”。

    1.  添加標題：將拉取請求標題設置為“更新的遊戲文本樣式”

    2.  添加描述：## Description：將遊戲文本顏色更新為綠色

![](./media/image12.jpeg)

5.  在“**Updated game text style \#1** ”頁上，單擊“**Merge pull
    request**”，然後單擊“**Confirm**”頁。

![](./media/image13.jpeg)

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image14.jpeg)

6.  在下一頁上，單擊刪除分支按鈕 **Delete branch** 新創建。

![](./media/image15.jpeg)

7.  等待大約 20 秒，讓 GitHub Actions 自動更新頁面。

![](./media/image16.jpeg)

**總結：**

您現在已經獲得了建立和管理基於發佈的工作流程的實踐經驗，增強了跟蹤版本、處理發佈和有效解決錯誤的能力。
