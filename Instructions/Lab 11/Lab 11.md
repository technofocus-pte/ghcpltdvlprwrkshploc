**實驗 11：使工作流可重用並使用矩陣策略運行多個版本的節點**

目標：

想像一下，您正在管理一個項目中的多個存儲庫，這些存儲庫共享構建、測試和部署等任務的通用工作流。為了避免冗餘並在這些存儲庫之間保持一致性，您決定使用
GitHub Actions
實現可重用的工作流。通過利用工作流調用觸發器，您可以集中工作流配置，確保在一個地方進行更改並自動應用於所有相關存儲庫。此外，您將利用矩陣策略來測試具有多個版本的Node.js的工作流程，從而提高兼容性和可擴展性。

在這個動手實驗室中，你將：

- 使用 workflow_call
  觸發器使您的工作流可在多個存儲庫中重用，從而減少配置冗餘。

- 導航到存儲庫，更新工作流文件以包含workflow_call觸發器，然後提交更改。

- 創建拉取請求以比較更改和異常。

練習 \#1：創建一個新存儲庫。

1.  瀏覽到以下鏈接：https://github.com/skills/reusable-workflows

在本練習中，你將使用公共模板“**skills-reusable-workflows**”創建存儲庫。

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image1.jpeg)

2.  選擇“**Use this template** ”菜單下的“**Create a new
    repository** ”。 

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image2.jpeg)

3.  輸入以下詳細信息，然後選擇 **Create Repository**。

    1.  存儲庫名稱：**skills-reusable-workflows**

&nbsp;

1.  存儲庫類型: **Public**

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image3.jpeg)

練習 \#2：將workflow_call觸發器添加到工作流

1.  在新創建的存儲庫的登錄頁上，導航到“**Code**”選項卡\*\*。

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image4.jpeg)

2.  從 main 分支下拉列表中，選擇 “**reusable-workflow**”分支。

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image5.jpeg)

3.  更改分支後，導航到 **.github/workflows/** 文件夾，然後選擇
    **reusable-workflow.yml** 文件。

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image6.jpeg)

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image7.jpeg)

4.  在 **reusable-workflow.yml** 文件編輯器上，選擇 **Edit in place**。

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image8.jpeg)

5.  將 **workflow_dispatch** 事件觸發器替換為 **workflow_call**
    事件觸發器，然後單擊“**Commit changes**”。

**注意：**將 **Line \#3** 到 **Line \# 8** 的代碼塊替換為下面的代碼塊

on:

workflow_call:

inputs:

node:

required: true

type: string

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image9.jpeg)

6.  在“**Commit changes** ”窗口中，單擊“**Commit changes**”。

![A screenshot of a screenshot of a new branch AI-generated content may
be incorrect.](./media/image10.jpeg)

練習 \#3：創建拉取請求以查看上一個練習中所做的更改

1.  選擇“**Pull requests** ”選項卡，然後單擊“**New pull request**”。 

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image11.jpeg)

2.  在“**Comparing changes page**”頁上，將 **base** 設置為 **main**，將
    **compare** 設置為 **reusable-workflow**。 

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image12.jpeg)

3.  在“**Open a pull request** ”頁上，單擊“**Create pull request**”。

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image13.jpeg)

4.  等待 20 秒，讓作運行並查看結果。

總結：

現在，你已經獲得了創建高效、可重用的工作流並使用 GitHub Actions
針對各種環境進行優化的實踐經驗。
