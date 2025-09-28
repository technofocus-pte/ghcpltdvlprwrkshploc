**實驗室 22 - 使用 Github Copilot
聊天創建筆記本並根據測試數據提供答案簡介**

此數據集tested_worldwide.csv源自
Kaggle。該數據集包含一段時間內進行的測試數量，對於幫助理解每日報告的病例和瞭解
COVID-19 如何在每個國家/地區真正傳播非常重要。

**指示**

1.  從 Windows 的“開始”菜單打開 Visual Studio Code，然後打開導航到
    C：\Labfiles\CopilotHackathon 的文件夾

![A screenshot of a computer Description automatically
generated](./media/image1.png)

2.  單擊 **Yes,I Trust the Author** 按鈕。

![BrokenImage](./media/image2.png)

3.  單擊 右下角的 **Copilot** 圖標，然後選擇 **Github Copilot Chat。**

![BrokenImage](./media/image3.png)

4.  鍵入提示：在項目中創建新筆記本。使用命令 /newnotebook
    並將其命名為“COVID19 Worldwide Testing Data”

![BrokenImage](./media/image4.png)

5.  可以看到 Copilot 說明可幫助你提供說明。按照步驟作並創建筆記本。

- 按 **Ctrl+Shift+P** 打開命令面板**。**

  - 鍵入 Jupyter： Create New Blank Notebook，然後按 Enter。

![BrokenImage](./media/image5.png)

- 將創建一個新筆記本。使用名稱 COVID19WorldwideTesting Data.ipynb
  保存它。您還可以詢問 Copilot 如何保存新筆記本。

![BrokenImage](./media/image6.png)

- 轉到目標文件夾 - **excercisefiles-？dataengieer** 輸入
  COVID19WorldwideTesting Data.ipynb 並保存文件。

![BrokenImage](./media/image7.png)

6.  您應該會看到該文件是在 **dataengineer** 文件夾下創建的。

![A screenshot of a computer Description automatically
generated](./media/image8.png)

7.  使用 Copilot 和 Copilot 聊天來開發練習並支持您的學習。

**鍛煉**

我們的分析試圖為這個問題提供答案：**與進行的檢測數量相比，哪些國家報告的陽性病例數量最多？**

**任務 1：導入所需庫**

1.  單擊 Notebook 內核並鍵入 \#Import Required Libraries.Including
    Pandas，然後按 Enter 鍵

![A screenshot of a computer Description automatically
generated](./media/image9.png)

2.  按 Tab 鍵。它會帶你到隊伍的盡頭。按 Enter 鍵，然後再次按 Tab
    鍵添加所有庫。

![A screenshot of a computer Description automatically
generated](./media/image10.png)

\# Import the necessary libraries, including pandas.

\# Import Required Libraries

\# Here we are importing the necessary libraries for our task

import pandas as pd \# pandas 是一個為 Python
編程語言編寫的軟件庫，用於數據作和分析。

![A screenshot of a computer Description automatically
generated](./media/image11.png)

**任務 2：加載數據集**

1.  使用 pandas 從根級別加載“tested_worldwide.csv”文件。

2.  請 Github Copilot 幫助您瞭解如何加載數據。輸入 使用 pandas
    從根級別加載“tested_worldwide.csv”文件

![BrokenImage](./media/image12.png)

3.  在筆記本中輸入以下代碼並運行它。它將要求您選擇 **Python
    Environment**。選擇它。

![BrokenImage](./media/image13.png)

4.  選擇推薦的環境。腳本運行並提供結果。

![BrokenImage](./media/image14.png)

![A screenshot of a computer Description automatically
generated](./media/image15.png)

任務 3：瞭解數據

1.  使用 head（） 函數顯示數據集的前 5 行

2.  請 Github Copilot 幫助你編寫顯示數據集前 5 行的代碼。顯示數據集的前
    5 行

![BrokenImage](./media/image16.png)

3.  單擊 **+ code **以打開新的 kerner。只需輸入 \# 顯示數據集的前 5
    行。它會自動預測您的問題。只需按標簽，然後按 Enter。

![Screens screenshot of a computer screen Description automatically
generated](./media/image17.png)

4.  **Coiplot** 會預測您要查找的命令，因此請按 選項卡
    接受代碼。您始終可以選擇編輯/編寫自己的代碼。

![BrokenImage](./media/image18.png)

5.  按選項卡並接受代碼。運行內核。

![BrokenImage](./media/image19.png)

6.  您應該會看到結果。

![A screenshot of a computer screen Description automatically
generated](./media/image20.png)

![A screenshot of a computer Description automatically
generated](./media/image21.png)

7.  請助手幫助顯示數據框中的行數和列數。單擊 +code
    。輸入代碼，然後運行內核。您也可以使用下面的代碼

8.  num_rows, num_cols = data.shape

9.  print("Number of rows:", num_rows)

print("Number of columns:", num_cols)

![BrokenImage](./media/image22.png)

10. 請您的 Copilot 幫助您顯示每列的數據類型。您還可以使用 data.dttypes

![A screenshot of a computer Description automatically
generated](./media/image23.png)

11. 要求 GitHub Copilot 提供“顯示每列中缺失值數”的代碼。

![A screenshot of a computer Description automatically
generated](./media/image24.png)

12. 添加一個新內核並添加以下代碼並運行它。您還可以使用 Copilot
    建議的代碼並檢查

13. missing_values = df.isnull().sum()

print(missing_values)

![A screenshot of a computer program Description automatically
generated](./media/image25.png)

14. 在新內核中運行以下代碼以顯示每列中唯一值的數量。請與助手聯繫，瞭解代碼和結果。

15. unique_values = df.nunique()

print(unique_values)

![A screenshot of a computer Description automatically
generated](./media/image26.png)

**任務 4：數據清理**

1.  運行以下代碼以刪除分析不需要的列。向助手詢問代碼並檢查結果。

data = df\[\['Country_Region', 'positive', 'total_tested'\]\]

![A screenshot of a computer Description automatically
generated](./media/image27.png)

2.  在新內核中鍵入 \#Rename 列以使其更具可讀性並接受代碼。

![A screenshot of a computer Description automatically
generated](./media/image28.png)

3.  您可以使用以下代碼並運行它。

df.rename(columns={'Country_Region': 'Country', 'positive': 'Positive
Cases', 'total_tested': 'Total Tested'}, inplace=True)

![A screenshot of a computer Description automatically
generated](./media/image29.png)

4.  要求您的助手刪除具有缺失值的行並在新內核中運行代碼或鍵入具有缺失值的行
    \#Drop 在新內核中按 Enter。按選項卡並接受代碼

![A screenshot of a computer Description automatically
generated](./media/image30.png)

5.  添加新的 +Code 內核並將列的數據類型 \#Convert 適當的類型輸入，按
    **tag **接受代碼，再次輸入並按
    Tab。生成陽性病例、檢測總數和國家/地區的代碼，然後運行它。

![A screenshot of a computer Description automatically
generated](./media/image31.png)

6.  添加一個新的 +Code 內核並鍵入每列中缺失值的數量 \#Display 然後按
    Enter。按 Tab 並接受代碼。您也可以在 GitHub Copilot 聊天中提問

![A screenshot of a computer program Description automatically
generated](./media/image32.png)

![A screenshot of a computer screen Description automatically
generated](./media/image33.png)

**任務 5：提取 Covid-19 病例最多的前十個國家。**

1.  讓您的 Copilot
    聊天幫助您編寫代碼創建一個包含每個國家/地區陽性病例總數的新數據框
    或者打開新代碼並鍵入一個包含每個國家/地區陽性病例總數的新數據框
    \#Create 然後按 Etner。按 Tab 鍵訪問代碼。

![A screenshot of a computer Description automatically
generated](./media/image34.png)

2.  在新代碼中，輸入以下提示，並在每個提示後輸入以接受代碼並運行它。

3.  \# Group the data by 'Country' and calculate the sum of 'Positive
    Cases'

4.  total_positive_cases = data.groupby('Country')\['Positive
    Cases'\].sum()

5.  \# Create a new dataframe with the total positive cases for each
    country

6.  df_total_positive_cases = pd.DataFrame({'Country':
    total_positive_cases.index, 'Total Positive Cases':
    total_positive_cases.values})

7.  \# Display the new dataframe

df_total_positive_cases

![A screenshot of a computer screen Description automatically
generated](./media/image35.png)

8.  要求 Copilot 按正案例總數的降序對數據幀進行排序 或鍵入 \#
    按正面案例總數的降序對數據幀進行排序
    在新的代碼內核中，按標簽接受代碼並運行它。

![A screenshot of a computer Description automatically
generated](./media/image36.png)

9.  請您的 Github Copilot 聊天幫助您顯示陽性病例最多的前十個國家或輸入
    \#
    在新代碼內核中顯示陽性病例最多的前十個國家並運行它。請記住，您只需要顯示。

![A screenshot of a computer Description automatically
generated](./media/image37.png)

**任務 6：識別針對已測試病例的最高陽性**

1.  請 GitHub Copilot Chat
    幫助你創建包含為每個國家/地區進行的測試總數的新數據框，或打開新的代碼內核並鍵入
    \# 創建一個包含為每個國家/地區進行的測試總數的新數據框，然後按 Tab
    鍵訪問代碼。如果需要，您可以編輯代碼並運行它。

2.  \# Group the data by 'Country' and calculate the sum of 'Total
    Tested'

3.  total_tests = data.groupby('Country')\['Total Tested'\].sum()

4.  

5.  \# Create a new dataframe with the total tests conducted for each
    country

6.  df_total_tests = pd.DataFrame({'Country': total_tests.index, 'Total
    Tests': total_tests.values})

7.  

8.  \# Display the new dataframe

df_total_tests

![A screenshot of a computer Description automatically
generated](./media/image38.png)

9.  詢問您的 Github Copilot Chat 按執行的測試總數的降序對數據幀進行排序
    或打開一個新的代碼內核，鍵入 \#
    按執行的測試總數的降序對數據幀進行排序 然後按 tab
    鍵訪問代碼並運行它。

![A screenshot of a computer program Description automatically
generated](./media/image39.png)

10. 詢問您的 Github Copilot Chat 顯示進行最多測試的前十個國家
    或打開一個新的代碼內核，輸入 \# 顯示進行最多測試的前十個國家 然後按
    tab 鍵訪問代碼並運行它。

![A screenshot of a computer program Description automatically
generated](./media/image40.png)

**任務7：根據檢測數量確定陽性病例數最多的前三個國家**

1.  詢問您的 Github Copilot Chat
    合併前面步驟中創建的兩個數據幀，或者打開一個新的代碼內核並輸入 \#
    Display 進行最多測試的前十個國家/地區，然後按 tab
    鍵訪問代碼並運行它。

![A screenshot of a computer Description automatically
generated](./media/image41.png)

2.  詢問您的 Github Copilot Chat
    創建一個包含陽性病例與所進行測試數量的比率的新列
    或打開一個新的代碼內核並輸入 \#
    創建一個包含陽性病例與所進行測試數量的比率的新列 然後按 tab
    接受代碼並運行它。

![A screenshot of a computer Description automatically
generated](./media/image42.png)

3.  詢問您的 Github Copilot Chat
    按陽性病例與所進行測試次數的比率的降序對數據幀進行排序
    或打開一個新的代碼內核並鍵入 \#
    按陽性病例與所進行測試次數的比率降序對數據幀進行排序
    然後按選項卡接受代碼並運行它。

![A screenshot of a computer Description automatically
generated](./media/image43.png)

4.  詢問您的 Github Copilot 聊天
    顯示陽性病例與所進行測試數量比例最高的前三個國家
    或者打開一個新的代碼內核並輸入陽性病例與所進行測試數量比例最高的前三個國家
    \#Display 然後按選項卡接受代碼並運行它

5.  \#顯示陽性病例占檢測數量比例最高的前三個國家

6.  top_countries = merged_df.nlargest(3, 'Positive Test Rate')

top_countries\[\['Country', 'Positive Test Rate'\]\]

![A screenshot of a computer Description automatically
generated](./media/image44.png)

**任務 8：顯示結果**

1.  要求您的 Github Copilot Chat 顯示結果
    一個圖表，顯示陽性病例與數字比例最高的前三個國家
    或者打開一個新的代碼內核並輸入 \# 顯示結果
    一個圖表，顯示陽性病例與數字比率最高的前三個國家
    然後按選項卡接受代碼並運行它

2.  \#Display 結果中，顯示陽性病例與數字之比最高的前三個國家

3.  將 matplotlib.pyplot 導入為 plt

top_countries.plot(x='Country', y='Positive Test Rate', kind='bar')

![A screenshot of a computer program Description automatically
generated](./media/image45.png)

4.  要求您的 Github Copilot Chat
    在顯示陽性病例最多的前十個國家/地區的圖表中顯示結果
    或者打開一個新的代碼內核並輸入 \#
    在顯示陽性病例最多的前十個國家/地區的圖表中顯示結果
    然後按選項卡接受代碼並運行它

5.  在圖表中 \#Display 結果，該圖表顯示了陽性病例最多的前十個國家

6.  將 matplotlib.pyplot 導入為 plt

7.  df_total_positive_cases.head(10).plot(x='Country', y='Total Positive
    Cases', kind='bar')

8.  plt.xlabel('Country')

9.  plt.ylabel('Total Positive Cases')

10. plt.title('Top Ten Countries with the Most Positive Cases')

plt.show()

![A screenshot of a computer screen Description automatically
generated](./media/image46.png)

11. 要求您的 Github Copilot Chat
    以顯示測試最多的前十個國家/地區的圖表顯示結果
    或者打開一個新的代碼內核並輸入 \#
    在顯示測試最多的前十個國家/地區的圖表中顯示結果
    然後按選項卡接受代碼並運行它

![A screenshot of a computer Description automatically
generated](./media/image47.png)

**任務 9：結論**

1.  你的結論是什麼？

2.  這種分析有什麼局限性？

3.  接下來會採取哪些步驟來改進這種分析？
