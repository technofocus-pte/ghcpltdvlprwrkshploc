**实验室 23 - 使用 Github Copilot Chat 生成基于 Scikit-learn 和 Python
的决策树分类器**

**介绍**

diabetes.csv 最初来自美国国家糖尿病、消化和肾脏研究所

疾病。该数据集的目的是诊断性地预测患者是否患有糖尿病，

基于数据集中包含的某些诊断测量值。设置了几个约束

从更大的数据库中选择这些实例。特别是这里的所有患者都是女性

至少 21 岁具有皮马印第安血统。

从diabetes.csv您可以找到几个变量，其中一些是独立的

（几个医学预测变量）和只有一个目标因变量（结果）。

**任务 1：使用 Github Copilot Chat 创建笔记本的说明**

1.  在 **Explorer in Visual Studio code** 中，展开 **datascientist**。

2.  单击 右下角的 **Copilot** 图标，然后选择 **Github Copilot Chat。**

![](./media/image1.png)

3.  键入提示：在项目中创建新笔记本。使用命令 /newnotebook
    并将其命名为“Diabetes Tree Classifier”

![](./media/image2.png)

4.  单击 **Terminal -\> New Terminal** 工具栏中，如下图所示。

![](./media/image3.png)

5.  从终端中选择 Gitbash，然后运行 Copilot 在 **datascientist**
    家目录中建议的命令。 

cd \exercisefiles\datascientist

touch "DiabetesTreeClassifier.ipynb"

![](./media/image4.png)

![](./media/image5.png)

6.  您应该会看到该文件是在 **datascientist** 文件夹下创建的。

![](./media/image6.png)

7.  选择新创建的笔记本以开发练习。

![](./media/image7.png)

8.  使用 Copilot 和 Copilot 聊天来开发练习并支持您的学习。

**锻炼**

该项目的目标是构建一个基于 Scikit-learn 和 Python
的决策树分类器。分类器应该能够根据以下条件预测患者是否患有糖尿病

数据集中包含的某些诊断测量值。

**任务 2：导入构建决策树分类器所需的库**

1.  点击 Notebook 内核，输入 \# 导入必要的库，包括 pandas、sklearn
    等，然后按 Enter 并按 tab 接受代码

2.  按 Tab 键。它会带你到队伍的尽头。按 Enter 键，然后再次按 Tab
    键添加所有库。

3.  \# pandas for data manipulation and analysis

4.  \# matplotlib for data visualization

5.  \# train_test_split for splitting the data into training and testing
    sets

6.  \# DecisionTreeClassifier for decision tree classification

\# accuracy_score for evaluating the model

![](./media/image8.png)

![](./media/image9.png)

7.  运行代码，它会要求你选择 Python 环境，选择它并运行

![](./media/image10.png)

8.  等到导入所有库。

![](./media/image11.png)

**任务 3：加载数据集**

1.  打开**diabetes.csv**文件并观察列名称。

![](./media/image12.png)

2.  使用 pandas 或从 sklearn
    数据集加载糖尿病数据集。打开新代码内核并输入 \# 使用 pandas 或从
    sklearn 数据集加载糖尿病数据集 然后按 tab 接受代码

3.  打开 Github Copilot 聊天，并要求使用 pandas 或从 sklearn
    数据集加载糖尿病数据集。.它为您提供了使用 pandas 或从 sklearn
    数据集加载糖尿病数据集的代码

![](./media/image13.png)

4.  单击 +code 打开一个新内核，复制 Copilot
    建议的代码并运行。您还可以使用以下代码加载数据。

5.  \# Load the Diabetes Dataset

6.  col_names = \['pregnant', 'glucose', 'bp', 'skin', 'insulin', 'bmi',
    'pedigree', 'age', 'label'\]

7.  \# load dataset

8.  diabetes_df = pd.read_csv("diabetes.csv", header=None,
    names=col_names)

\# Display the first 5 rows of the DataFrame

![](./media/image14.png)

**任务 4 ： 探索性数据分析**

显示数据框中的行数和列数。显示每列的数据类型。显示每列中的缺失值数。显示每列中唯一值的数量。显示每列的基本统计信息。

1.  打开一个新的代码内核并键入数据帧的前 5 行 \#Display 按 Enter。按
    选项卡接受代码。您也可以使用以下代码。

2.  \#Display 数据帧的前 5 行

diabetes_df.head()

![](./media/image15.png)

3.  打开一个新的代码内核并键入每列的数据类型 \#Display。按 Enter 键。按
    选项卡接受代码。

![](./media/image16.png)

4.  打开一个新的代码内核，然后键入每列中缺失值 \#Display 数按 Enter。按
    Tab 接受代码。

![](./media/image17.png)

5.  打开一个新的代码内核，然后键入每列中的唯一值 \#Display 数按
    Enter。按 Tab 接受代码。

![](./media/image18.png)

6.  打开一个新的代码内核，并键入数据帧的汇总统计 \#Display。按 Enter
    键。按 选项卡接受代码。

![](./media/image19.png)

**任务 5 ： 特征选择**

1.  选择要用于预测的特征。您可以使用所有功能或功能子集。

2.  打开一个新的 Code 内核并键入 \# 将数据拆分为特征和目标变量。按 Enter
    键。按 选项卡接受代码。您可以向 Copilot
    聊天询问解释。您也可以使用以下代码并运行它。

3.  \#split dataset in features and target variable

4.  feature_cols = \['pregnant', 'insulin', 'bmi',
    'age','glucose','bp','pedigree'\]

5.  X = diabetes_df\[feature_cols\] \# Features

y = diabetes_df.label \# Target variable

![](./media/image20.png)

6.  将数据分为训练集和测试集。训练集将用于训练模型，测试集将用于评估模型。

7.  打开一个新的代码内核并键入 \# 将数据拆分为训练集和测试集 按
    Enter。按 Tab 接受代码。您可以向 Copilot
    聊天询问解释。您也可以使用以下代码并运行它。

8.  \# 将数据集拆分为训练集和测试集

X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.3,
random_state=1) \# 70% training and 30% test

![](./media/image21.png)

**任务 6 ： 构建决策树模型**

1.  使用训练集构建决策树模型。

2.  打开一个新的代码内核并键入 \# 将数据拆分为训练集和测试集 按
    Enter。按 Tab 接受代码。您可以向 Copilot
    聊天询问解释。您也可以使用以下代码并运行它。

3.  \# Building Decision Tree Model

4.  \# Create Decision Tree classifer object

5.  clf = DecisionTreeClassifier()

6.  \# Train Decision Tree Classifer

7.  clf = clf.fit(X_train,y_train)

8.  \#Predict 测试数据集的响应

y_pred = clf.predict(X_test)

9.  您可以看到 ValueError。要求 Github Copilot 解决该问题。按照 Copilot
    聊天说明并解决问题。

![](./media/image22.png)

10. 打开一个新的 Code 内核并输入 \# Model
    Accuracy，分类器多久正确一次？按 Enter 键。按
    选项卡接受代码。您可以向 Copilot
    聊天询问解释。您也可以使用以下代码并运行它。

11. \# Evaluating Model

12. \# Model Accuracy, how often is the classifier correct?

print("Accuracy:",metrics.accuracy_score(y_test, y_pred))

13. 使用测试集评估模型。

14. \# Evaluating Model

15. \# Model Accuracy, how often is the classifier correct?

print("Accuracy:",metrics.accuracy_score(y_test, y_pred))
