**實驗室 23 - 使用 Github Copilot Chat 生成基於 Scikit-learn 和 Python
的決策樹分類器**

**介紹**

diabetes.csv 最初來自美國國家糖尿病、消化和腎臟研究所

疾病。該數據集的目的是診斷性地預測患者是否患有糖尿病，

基於數據集中包含的某些診斷測量值。設置了幾個約束

從更大的數據庫中選擇這些實例。特別是這裡的所有患者都是女性

至少 21 歲具有皮馬印第安血統。

從diabetes.csv您可以找到幾個變量，其中一些是獨立的

（幾個醫學預測變量）和只有一個目標因變量（結果）。

**任務 1：使用 Github Copilot Chat 創建筆記本的說明**

1.  在 **Explorer in Visual Studio code** 中，展開 **datascientist**。

2.  單擊 右下角的 **Copilot** 圖標，然後選擇 **Github Copilot Chat。**

![A screenshot of a computer Description automatically
generated](./media/image1.png)

3.  鍵入提示：在項目中創建新筆記本。使用命令 /newnotebook
    並將其命名為“Diabetes Tree Classifier”

![A screenshot of a computer Description automatically
generated](./media/image2.png)

4.  單擊 **Terminal -\> New Terminal** 工具欄中，如下圖所示。

![BrokenImage](./media/image3.png)

5.  從終端中選擇 Gitbash，然後運行 Copilot 在 **datascientist**
    家目錄中建議的命令。 

cd \exercisefiles\datascientist

touch "DiabetesTreeClassifier.ipynb"

![BrokenImage](./media/image4.png)

![A screenshot of a computer Description automatically
generated](./media/image5.png)

6.  您應該會看到該文件是在 **datascientist** 文件夾下創建的。

![A screenshot of a computer Description automatically
generated](./media/image6.png)

7.  選擇新創建的筆記本以開發練習。

![A screenshot of a computer Description automatically
generated](./media/image7.png)

8.  使用 Copilot 和 Copilot 聊天來開發練習並支持您的學習。

**鍛煉**

該項目的目標是構建一個基於 Scikit-learn 和 Python
的決策樹分類器。分類器應該能夠根據以下條件預測患者是否患有糖尿病

數據集中包含的某些診斷測量值。

**任務 2：導入構建決策樹分類器所需的庫**

1.  點擊 Notebook 內核，輸入 \# 導入必要的庫，包括 pandas、sklearn
    等，然後按 Enter 並按 tab 接受代碼

2.  按 Tab 鍵。它會帶你到隊伍的盡頭。按 Enter 鍵，然後再次按 Tab
    鍵添加所有庫。

3.  \# pandas for data manipulation and analysis

4.  \# matplotlib for data visualization

5.  \# train_test_split for splitting the data into training and testing
    sets

6.  \# DecisionTreeClassifier for decision tree classification

\# accuracy_score for evaluating the model

![A computer screen shot of a computer Description automatically
generated](./media/image8.png)

![A screenshot of a computer Description automatically
generated](./media/image9.png)

7.  運行代碼，它會要求你選擇 Python 環境，選擇它並運行

![BrokenImage](./media/image10.png)

8.  等到導入所有庫。

![A screenshot of a computer program Description automatically
generated](./media/image11.png)

**任務 3：加載數據集**

1.  打開**diabetes.csv**文件並觀察列名稱。

![A screen shot of a computer Description automatically
generated](./media/image12.png)

2.  使用 pandas 或從 sklearn
    數據集加載糖尿病數據集。打開新代碼內核並輸入 \# 使用 pandas 或從
    sklearn 數據集加載糖尿病數據集 然後按 tab 接受代碼

3.  打開 Github Copilot 聊天，並要求使用 pandas 或從 sklearn
    數據集加載糖尿病數據集。.它為您提供了使用 pandas 或從 sklearn
    數據集加載糖尿病數據集的代碼

![A screenshot of a computer program Description automatically
generated](./media/image13.png)

4.  單擊 +code 打開一個新內核，複製 Copilot
    建議的代碼並運行。您還可以使用以下代碼加載數據。

5.  \# Load the Diabetes Dataset

6.  col_names = \['pregnant', 'glucose', 'bp', 'skin', 'insulin', 'bmi',
    'pedigree', 'age', 'label'\]

7.  \# load dataset

8.  diabetes_df = pd.read_csv("diabetes.csv", header=None,
    names=col_names)

\# Display the first 5 rows of the DataFrame

![A screenshot of a computer Description automatically
generated](./media/image14.png)

**任務 4 ： 探索性數據分析**

顯示數據框中的行數和列數。顯示每列的數據類型。顯示每列中的缺失值數。顯示每列中唯一值的數量。顯示每列的基本統計信息。

1.  打開一個新的代碼內核並鍵入數據幀的前 5 行 \#Display 按 Enter。按
    選項卡接受代碼。您也可以使用以下代碼。

2.  \#Display 數據幀的前 5 行

diabetes_df.head()

![A screenshot of a computer Description automatically
generated](./media/image15.png)

3.  打開一個新的代碼內核並鍵入每列的數據類型 \#Display。按 Enter 鍵。按
    選項卡接受代碼。

![A screenshot of a computer program Description automatically
generated](./media/image16.png)

4.  打開一個新的代碼內核，然後鍵入每列中缺失值 \#Display 數按 Enter。按
    Tab 接受代碼。

![A screenshot of a computer program Description automatically
generated](./media/image17.png)

5.  打開一個新的代碼內核，然後鍵入每列中的唯一值 \#Display 數按
    Enter。按 Tab 接受代碼。

![A screenshot of a computer program Description automatically
generated](./media/image18.png)

6.  打開一個新的代碼內核，並鍵入數據幀的匯總統計 \#Display。按 Enter
    鍵。按 選項卡接受代碼。

![A screenshot of a computer Description automatically
generated](./media/image19.png)

**任務 5 ： 特徵選擇**

1.  選擇要用於預測的特徵。您可以使用所有功能或功能子集。

2.  打開一個新的 Code 內核並鍵入 \# 將數據拆分為特徵和目標變量。按 Enter
    鍵。按 選項卡接受代碼。您可以向 Copilot
    聊天詢問解釋。您也可以使用以下代碼並運行它。

3.  \#split dataset in features and target variable

4.  feature_cols = \['pregnant', 'insulin', 'bmi',
    'age','glucose','bp','pedigree'\]

5.  X = diabetes_df\[feature_cols\] \# Features

y = diabetes_df.label \# Target variable

![A screenshot of a computer screen Description automatically
generated](./media/image20.png)

6.  將數據分為訓練集和測試集。訓練集將用於訓練模型，測試集將用於評估模型。

7.  打開一個新的代碼內核並鍵入 \# 將數據拆分為訓練集和測試集 按
    Enter。按 Tab 接受代碼。您可以向 Copilot
    聊天詢問解釋。您也可以使用以下代碼並運行它。

8.  \# 將數據集拆分為訓練集和測試集

X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.3,
random_state=1) \# 70% training and 30% test

![A screenshot of a computer program Description automatically
generated](./media/image21.png)

**任務 6 ： 構建決策樹模型**

1.  使用訓練集構建決策樹模型。

2.  打開一個新的代碼內核並鍵入 \# 將數據拆分為訓練集和測試集 按
    Enter。按 Tab 接受代碼。您可以向 Copilot
    聊天詢問解釋。您也可以使用以下代碼並運行它。

3.  \# Building Decision Tree Model

4.  \# Create Decision Tree classifer object

5.  clf = DecisionTreeClassifier()

6.  \# Train Decision Tree Classifer

7.  clf = clf.fit(X_train,y_train)

8.  \#Predict 測試數據集的響應

y_pred = clf.predict(X_test)

9.  您可以看到 ValueError。要求 Github Copilot 解決該問題。按照 Copilot
    聊天說明並解決問題。

![A screenshot of a computer program Description automatically
generated](./media/image22.png)

10. 打開一個新的 Code 內核並輸入 \# Model
    Accuracy，分類器多久正確一次？按 Enter 鍵。按
    選項卡接受代碼。您可以向 Copilot
    聊天詢問解釋。您也可以使用以下代碼並運行它。

11. \# Evaluating Model

12. \# Model Accuracy, how often is the classifier correct?

print("Accuracy:",metrics.accuracy_score(y_test, y_pred))

13. 使用測試集評估模型。

14. \# Evaluating Model

15. \# Model Accuracy, how often is the classifier correct?

print("Accuracy:",metrics.accuracy_score(y_test, y_pred))
