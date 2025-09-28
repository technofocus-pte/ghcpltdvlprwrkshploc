實驗 16：從 Git Repository 中刪除提交歷史記錄

客觀的：

想像一下，您是開發團隊的一員，從事一個項目，其中敏感信息（例如 API
密鑰或數據庫憑據）被意外提交到您的 Git repository 中。使用 Git
刪除意外提交可能很棘手。

在本練習中，您將：

- 使用意外提交的敏感數據克隆存儲庫。

- 從克隆的存儲庫中刪除/刪除包含敏感數據的文件，然後提交刪除。

- 將更改推送到 GitHub：將更新的存儲庫上傳到 GitHub 以反映更改。

### **練習 \#1：使用意外提交歷史記錄（敏感數據）創建存儲庫**

1.  登錄到你的 GitHub 帳戶。

2.  瀏覽到以下鏈接：<https://github.com/skills/change-commit-history>

> 在本實驗中，你將使用公共模板“**skills-change-commit-history**”創建存儲庫。
>
> ![](./media/image1.png)

3.  選擇“**Use this template**”菜單下的“**Create a new repository**”。

> ![A screenshot of a computer Description automatically
> generated](./media/image2.png)

4.  輸入以下詳細信息，然後選擇創建存儲庫。.

- 存儲庫名稱： **skills-change-commit-history**

- 存儲庫類型： **Public**

![](./media/image3.png)

### 練習 \# 2：刪除/刪除包含敏感數據的文件（項目根目錄中的 .env）

1.  在克隆存儲庫的登錄頁面上，導航到 **Code\>Local\>HTTPS** 並複製 URL。

![](./media/image4.png)

2.  打開 Windows Powershell 並輸入以下命令。

**git clone \<your-repository-url\>**

**注意**：替換為您在步驟 1 中複製的 URL。

> ![](./media/image5.png)

3.  切換到您的存儲庫目錄，輸入以下命令。

**+++cd “C:\Users\Admin\skills-change-commit-history”+++**

**注意**：替換為存儲庫名稱

> ![](./media/image6.png)

4.  執行以下命令從根目錄中刪除 .env，

**+++git rm .env**+++

> ![A screenshot of a computer screen Description automatically
> generated](./media/image7.png)

5.  提交刪除 .env 文件

**+++git commit -m "remove .env file”+++**

> ![A screen shot of a computer Description automatically
> generated](./media/image8.png)
>
> **提示**：如何從 Git 歷史記錄中完全刪除 .env
> 文件並使用新的提交哈希重寫總歷史記錄？
>
> 使用以下命令可以：

- 從 Git 歷史記錄中完全刪除 .env 文件並重寫總歷史記錄

> **git filter-branch --force --index-filter 'git rm --cached
> --ignore-unmatch.env' --prune-empty --tag-name-filter cat -- --all**

- 將刪除推送到 GitHub

> **git push origin --force –all**

6.  將刪除推送到 GitHub:

**git push**

> ![A screen shot of a computer program Description automatically
> generated](./media/image9.png)

總結：

現在，您已經完成了 Git
存儲庫的清理，確保敏感內容不會在存儲庫的歷史記錄中暴露。

