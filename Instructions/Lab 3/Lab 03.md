**實驗室 03：使用 GitHub Pages 和 Jekyll 創建在線作品集**

目的：

想像一下，您是一家科技初創公司的一名嶄露頭角的軟件開發人員，渴望通過在線作品集展示您的項目、技能和經驗。您需要一個專業的平臺來展示您的作品，因此您決定使用
GitHub Pages 創建一個個人網站或博客。該平臺允許您利用 GitHub
存儲庫輕鬆發佈和維護您的網站。

在這個動手實驗室中，您將:

- 創建 GitHub 存儲庫：設置一個新存儲庫，作為您個人站點的基礎。

- 啟用 GitHub Pages：將 GitHub Pages 配置為直接從存儲庫託管您的網站。

&nbsp;

- 使用 Jekyll 部署您的第一個站點：利用流行的靜態站點生成器
  Jekyll，以最小的努力構建和部署具有專業外觀的網站.

練習 \#1：從模板創建存儲庫

1.  登錄到你的 GitHub 帳戶。

2.  瀏覽到以下鏈接: https://github.com/skills/github-pages

在本練習中，你將使用公共模板“**skills-github-pages**”創建存儲庫。

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image1.jpeg)

3.  選擇“**Use this template**”菜單下的“**Create a new repository**”。  

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image2.jpeg)

4.  輸入以下詳細信息，然後選擇 **Create Repository**。

    1.  存儲庫名稱: **skills-github-pages**

    2.  存儲庫類型: **Public**

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image3.jpeg)

練習 \#2：啟用 GitHub 頁面

1.  創建存儲庫後，導航到主頁。在主導航窗格中，單擊“**Settings**”圖標。 

![A screenshot of a web page AI-generated content may be
incorrect.](./media/image4.jpeg)

2.  在設置頁面中，向下滾動到代碼和自動化，然後單擊 **Pages**。

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image5.jpeg)

3.  在 GitHub 頁面上，確保從“**Source**”下拉菜單中選擇“**Deploy from a
    branch**”，然後從“**Branch**”下拉菜單中選擇“**main**”。

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image6.jpeg)

4.  點擊 **Save**  按鈕繼續。

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image7.jpeg)

5.  將保存 GitHub Pages 源代碼。等待大約一分鐘，然後刷新此頁面。GitHub
    Actions 將自動更新到下一步。

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image8.jpeg)

6.  您的網站現已上線。

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image9.jpeg)

7.  單擊訪問站點按鈕以查看您的站點。你打開了 GitHub 頁面。

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image10.jpeg)

練習 \#3：使用 Jekyll 部署您的站點

您將在分支 my-pages
中工作，以使這個網站看起來很棒。在本實驗中，我們將使用博客就緒主題。“minima”。

Jekyll 使用名為 **\_config.yml**
的文件來存儲您的網站、主題和可重用內容（如網站標題和 GitHub
句柄）的設置。

1.  選擇存儲庫的**“Code**”選項卡

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image11.jpeg)

2.  展開**main **分支並選擇 **my-pages**。

![A screenshot of a web page AI-generated content may be
incorrect.](./media/image12.jpeg)

在 **my-pages** 分支中，**\_config.yml**瀏覽到文件

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image13.jpeg)

3.  打開右上角的文件編輯器。

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image14.jpeg)

4.  添加主題：設置為 **minima**，使其在**\_config.yml**文件中顯示如下：

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image15.jpeg)

5.  單擊**“Commit Changes”**按鈕以保存更改。

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image16.jpeg)

**注意：**等待大約一分鐘，然後刷新此頁面。GitHub Actions
將自動更新到下一步。

6.  要檢查更新的網站，請單擊 GitHub 頁面下的 **Visit site** 按鈕。

![A screenshot of a web page AI-generated content may be
incorrect.](./media/image17.jpeg)

7.  將應用所選主題。您可以繼續修改其他配置變量，例如 title：、author：
    和 description：，以進一步自定義您的網站

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image18.jpeg)

總結：

您現在已經創建了一個包含 GitHub
頁面的網站並應用了主題。您可以利用此經驗創建一個實時網站，您可以在其中不斷更新和展示您的軟件開發之旅，使雇主、合作者和技術社區更容易看到您的工作和技能。
