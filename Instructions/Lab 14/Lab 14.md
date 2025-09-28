**實驗室 14：保護存儲庫的供應鏈**

目標：

想像一下，您負責維護依賴於各種第三方依賴項的軟件項目的安全性。為了確保項目供應鏈的完整性和安全性，有效瞭解和管理這些依賴關係至關重要。這涉及識別依賴項中的潛在漏洞並應用必要的補丁來保護您的項目。在本實驗中，您將學習如何使用
GitHub
的依賴關係圖功能來監控和查看依賴關係，確保您的項目保持安全和最新。

在這個動手實驗室中，你將：

- 啟用依賴關係圖：在存儲庫設置中啟用並驗證依賴關係圖功能，以可視化項目的依賴關係。

- 添加新的依賴項：向您的項目添加新的依賴項並確保其正確集成。

- 查看依賴關係圖：使用依賴關係圖查看並確認新依賴關係是否正確反映和監控。

練習 01：創建新存儲庫

1.  瀏覽到以下鏈接：https://github.com/skills/secure-repository-supply-chain

在本練習中，您將使用公共模板創建存儲庫
**skills-secure-repository-supply-chain**

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image1.jpeg)

2.  選擇“**Use this template** ”菜單下的“**Create a new
    repository**”。  

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image2.jpeg)

3.  輸入以下詳細信息，然後選擇 **Create Repository**。

    1.  存儲庫名稱：**skills-secure-repository-supply-chain**

&nbsp;

1.  存儲庫類型：**Public**

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image3.jpeg)

練習 02：驗證是否啟用了依賴關係圖

1.  在新創建的存儲庫的登錄頁上，導航到“**Settings”**選項卡。

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image4.jpeg)

2.  在“**Settings**”頁上，選擇“**Security**”下可用的 **Code security and
    analysis** 。 

![A screenshot of a general login AI-generated content may be
incorrect.](./media/image5.jpeg)

3.  驗證/啟用依賴關係圖。（如果存儲庫是私有的，您將在此處啟用它。如果存儲庫是公共的，則默認情況下將啟用它）

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image6.jpeg)

練習 03：添加新的依賴項並查看依賴關係圖

1.  導航到“**Code**”選項卡並找到 **code/src/AttendeeSite** 文件夾。

**注意：**您可以瀏覽到該文件夾或使用 **Go to file** 搜索
code/src/AttendeeSite

![A screenshot of a web page AI-generated content may be
incorrect.](./media/image7.jpeg)

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image8.jpeg)

2.  打開**package-lock.json**文件。

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image9.jpeg)

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image10.jpeg)

3.  在第 \# 14 行和第 \#15 行之間插入以下代碼片段

4.  "follow-redirects": {

5.  "version": "1.14.1",

6.  "resolved":

7.  "https://registry.npmjs.org/follow-redirects/-/follow-redirects-1.14.1.tgz",

8.  "integrity":

9.  "sha512-HWqDgT7ZEkqRzBvc2s64vSZ/hfOceEol3ac/7tKwzuvEyWx3/4UegXh5oBOIotkGsObyk3xznnSRVADBgWSQVg=="

},

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image11.jpeg)

**注意：**請確保添加的代碼片段已正確縮進，如屏幕截圖所示

10. 點擊右上角的 **Commit changes**。

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image12.jpeg)

11. 在主導航欄上，單擊“** Insights”選項卡**。

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image13.jpeg)

12. 在左側導航窗格中，單擊“**Dependency graph**”。

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image14.jpeg)

13. 查看依賴項中心上的所有新依賴項。

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image15.jpeg)

14. 搜索 follow-redirects 並查看您剛剛添加的新依賴項。

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image16.jpeg)

總結：

您現在已經獲得了有關管理項目依賴項和保護存儲庫供應鏈的寶貴見解，從而使您能夠主動解決和減輕安全風險。
