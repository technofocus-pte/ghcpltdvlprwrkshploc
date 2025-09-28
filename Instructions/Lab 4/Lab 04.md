**實驗 04：查看拉取請求並解決合併衝突**

目的：

想像一下，您是開發團隊的一員，負責一個有多個貢獻者的項目。隨著更改的進行，審查這些更改並確保每個人的工作順利集成至關重要。您需要通過管理拉取請求和解決合併衝突來有效協作，以維護項目的完整性並避免中斷。

在這個動手實驗室中，你將重點介紹 GitHub 上協作的兩個關鍵方面:

- 創建拉取請求：選擇適當的分支，提供標題和描述，然後提交拉取請求以提出更改建議。

- 審查拉取請求：檢查拉取請求中提出的更改，確保它們符合項目標準並準備好進行集成。

- 解決合併衝突：練習解決不同分支中的更改影響文件的相同部分時出現的衝突，確保順利集成和協作。

練習 \#1：從模板創建存儲庫並創建拉取請求

拉取請求將向其他人顯示分支中的更改。此拉取請求將保留您剛剛在分支上所做的更改，並建議將它們應用於主分支。

1.  登錄到你的 GitHub 帳戶。

2.  瀏覽到以下鏈接：https://github.com/skills/review-pull-requests

在本練習中，你將使用公共模板“**skills-review-pull-requests**”創建存儲庫。

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image1.jpeg)

3.  選擇“**Create a new repository**”菜單下的“**Use this template**”。  

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image2.jpeg)

4.  輸入以下詳細信息，然後選擇 **Create Repository**。

    1.  存儲庫名稱: **skills-review-pull-requests**

    2.  存儲庫類型: **Public**

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image3.jpeg)

5.  在主導航頁上，選擇“**Pull requests** ”選項卡。

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image4.jpeg)

6.  在下一頁上，選擇“**New pull request**”。

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image5.jpeg)

7.  在“**Compare changes”**頁上:

    1.  在 **base**： 下拉列表中，選擇
        **main**（默認情況下處於選中狀態）

    2.  在 **compare**： 下拉列表中，選擇 **update-game**，

通常需要等待幾秒鐘並刷新頁面才能查看分支。

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image6.jpeg)

![A screenshot of a phone AI-generated content may be
incorrect.](./media/image7.jpeg)

8.  在**compare:**下拉列表中選擇 **update-game** 後，將打開“**Comparing
    changes**”窗口。單擊**Create pull request**。

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image8.jpeg)

9.  在“**Open a pull request”頁上，**輸入以下內容:

    1.  為拉取請求**添加標題**：更新遊戲結束消息

    2.  為您的拉取請求**添加描述**：更新遊戲結束消息，以便人們知道如何玩

10. 單擊 **Create pull request**。 

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image9.jpeg)

11. 等待大約 20 秒，然後刷新此頁面。GitHub Actions 將自動更新到下一步。

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image10.jpeg)

練習 \#2：更新拉取請求並解決合併衝突

1.  瀏覽到以下鏈接：https://github.com/skills/resolve-merge-conflicts

在本練習中，你將使用公共模板“**skills-resolve-merge-conflicts**”創建存儲庫。

![A screenshot of a web page AI-generated content may be
incorrect.](./media/image11.jpeg)

2.  選擇“**Use this template** ”菜單下的“**Create a new repository** ”。

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image12.jpeg)

3.  輸入以下詳細信息，然後選擇**Create Repository**。

    - 存儲庫名稱: **skills-resolve-merge-conflicts**

    - 存儲庫類型: **Public**

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image13.jpeg)

4.  創建存儲庫後，選擇主導航欄上的“**Pull request** ”選項卡。

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image14.jpeg)

5.  單擊“**New pull request** ”按鈕。

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image15.jpeg)

6.  通過選擇以下選項創建拉取請求:

    - **my-resume** 作為 head 分支，並將

    - **main** 作為比較分支。

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image16.jpeg)

![A screenshot of a chat AI-generated content may be
incorrect.](./media/image17.jpeg)

7.  單擊**“Create pull request”**按鈕

8.  在“**Open a pull
    request** ”頁上，輸入標題為“解決合併衝突”，然後單擊“**Create pull
    request**”。

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image18.jpeg)

9.  等待 20 秒，讓 GitHub Actions
    自動更新，頁面顯示衝突的詳細信息（如果有）。

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image19.jpeg)

10. 單擊 **Resolve conflicts** 以繼續。 

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image20.jpeg)

11. 查看衝突並解決它們。

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image21.jpeg)

12. 在本練習中，讓我們刪除行項目衝突，然後單擊** Mark as resolved**
    按鈕。

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image22.jpeg)

13. 單擊**“Commit merge ”**按鈕並選中提醒消息框。

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image23.jpeg)

14. 點擊 **I understand, continue updating main。**
    您將看到最終檢查結果\*\*。

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image24.jpeg)

**總結：**

現在，你已經完成了衝突的拉取請求的創建和審查以及解決衝突，這是在 GitHub
上進行有效團隊合作和項目管理的基本技能。
