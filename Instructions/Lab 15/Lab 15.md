**實驗室 15：啟用 CodeQL 以保護源代碼**

目的：

想像一下，您是一名軟件開發人員，正在為公司處理一個關鍵項目，其中確保應用程序的安全是重中之重。隨著人們對網絡威脅和數據洩露的擔憂日益增加，必須確保您的代碼不存在漏洞和不安全的編碼實踐。在此動手實驗室中，你將啟用
GitHub Code Scanning 以自動查看源代碼是否存在潛在的安全問題。

在此動手實驗室中，你將啟用 GitHub Code Scanning
以自動查看源代碼是否存在潛在的安全問題。

練習 \#1：從公共模板創建新存儲庫

1.  登錄到你的 GitHub 帳戶。

2.  瀏覽到以下鏈接：https://github.com/skills/introduction-to-codeql

在本實驗室中，你將使用公共模板“**skills-introduction-to-codeql**”創建存儲庫。

![](./media/image1.jpeg)

3.  選擇“**Use this template** ”菜單下的“**Create a new repository** ”。

![](./media/image2.jpeg)

4.  輸入以下詳細信息，然後選擇**Create Repository**。

    1.  存儲庫名稱：**skills-introduction-to-codeql**

&nbsp;

1.  存儲庫類型：**Public**

![](./media/image3.jpeg)

練習 \#2：使用 CodeQL 啟用代碼掃描

1.  在新創建的存儲庫的登錄頁上，導航到“**Settings”**選項卡。

![](./media/image4.jpeg)

2.  在左側邊欄的“**Security**”部分下，選擇“**Code security and
    analysis**”。 

![](./media/image5.jpeg)

3.  向下滾動到標題為“Code
    scanning”的部分，單擊“**Set-up** ”下拉菜單，然後選擇“**Default**”。

![](./media/image6.jpeg)

4.  選擇以下選項，然後單擊**“Enable CodeQL”**

    1.  要分析的語言：這些是 CodeQL
        將掃描的語言。在這種情況下，我們將使用 Python 進行掃描。

    2.  查詢套件：CodeQL
        查詢打包在稱為“套件”的捆綁包中。此部分允許您選擇要使用的查詢套件。在本練習中，我們將此集保留為默認值。

    3.  事件：本部分告知 CodeQL
        何時掃描。在這種情況下，它設置為掃描對主分支的任何拉取請求。

![](./media/image7.jpeg)

5.  等待大約 20 秒，然後刷新此頁面以繼續。

![](./media/image8.jpeg)

總結：

現在，你已啟用 GitHub Code Scanning
來自動查看源代碼是否存在潛在的安全問題。
