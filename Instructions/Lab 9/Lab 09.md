**實驗 09：創建工作流以對項目使用持續集成 （CI）**

目標：

想像一下，您正在從事一個軟件項目，其中保持高質量標準至關重要。為了確保代碼保持健壯且沒有錯誤，您決定使用
GitHub Actions 實現持續集成 （CI）。CI
有助於在每次對代碼庫進行更改時自動執行運行測試和檢查代碼質量的過程。通過創建
CI 工作流程，您可以自動對 Markdown 文件進行
lint、運行測試並立即接收有關代碼質量的反饋，確保您的項目始終符合其質量標準。

在這個動手實驗室中，你將：

- 創建測試工作流程：設置專門設計用於 lint Markdown 文件並檢查格式問題的
  GitHub Actions 工作流程。

- 配置和更新工作流程：練習配置工作流文件以定義自動 linting
  所需的作業和步驟，並根據需要進行更新以增強其功能。

- 創建拉取請求：通過創建拉取請求來集成更改，允許您測試 CI
  工作流程並觀察它如何自動執行質量檢查。

- 分析 CI 工作流的結果，瞭解它如何報告問題並確保代碼質量。

練習 \#1：從公共模板創建新存儲庫

1.  瀏覽到以下鏈接：https://github.com/skills/test-with-actions

在本練習中，你將使用公共模板“**skills-test-with-actions**”創建存儲庫。

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image1.jpeg)

2.  選擇“**Use this template** ”菜單下的“**Create a new repository**”。 

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image2.jpeg)

3.  輸入以下詳細信息，然後選擇 **Create Repository**。

    1.  存儲庫名稱：**skills-test-with-actions**

&nbsp;

1.  存儲庫類型: **Public**

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image3.jpeg)

練習 \#2：添加測試工作流

1.  導航到不久前創建的存儲庫中的作選項卡。

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image4.jpeg)

2.  在左側邊欄的“Actions”下，選擇“**New workflow**”。

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image5.jpeg)

3.  在“**Choose a workflow** ”頁上，導航到“**Simple
    workflow**”，然後單擊“**Configure**”。

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image6.jpeg)

4.  在下一頁上，將工作流重命名為
    ci.yml，並通過刪除最後兩個步驟來更新工作流。

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image7.jpeg)

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image8.jpeg)

5.  在工作流末尾添加以下代碼，然後單擊右上角的 **Commit changes** 。

6.  \- name: Run markdown lint

7.  run: |

8.  npm install remark-cli remark-preset-lint-consistent

npx remark . --use remark-preset-lint-consistent

**注意：**請確保添加到工作流的代碼片段已正確縮進

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image9.jpeg)

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image10.jpeg)

9.  在“**Commit changes** ”窗口中，選擇“**Create a new branch for this
    commit and start a pull request**”。

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image11.jpeg)

10. 選擇“**Create a new branch for this commit and start a pull
    request**”後，“**Commit changes** ”窗口更改為“**Propose
    Changes** ”窗口。現在點擊 **Propose changes**。  

![A screenshot of a computer screen AI-generated content may be
incorrect.](./media/image12.jpeg)

11. 在“**Open a pull request**”的下一頁上，單擊“**Create pull
    request**”。

![A screenshot of a email AI-generated content may be
incorrect.](./media/image13.jpeg)

12. 等待 20 秒，然後刷新此頁面以分析結果。

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image14.jpeg)

總結：

您現在已經獲得了使用 GitHub Actions 進行 CI
實踐的實踐經驗，從而增強了您在軟件項目中自動化和維護高質量標準的能力。
