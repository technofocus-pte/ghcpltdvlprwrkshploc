**ラボ 22 - Github Copilot
チャットを使用してノートブックを作成し、テスト
データに基づいて回答を提供する概要**

このデータセットtested_worldwide.csvはKaggleから発信されています。このデータセットには、長期にわたって実施された検査の数が含まれており、毎日報告される症例を理解し、COVID-19が各国で実際にどのように広がっているかを理解するために重要です。

**指示**

1.  Windows の 「スタート」 メニューから Visual Studio Code
    を開き、フォルダーを開き、C:\Labfiles\CopilotHackathonに移動します

![コンピューターのスクリーンショット説明が自動的に生成されます](./media/image1.png)

2.  「**Yes,I Trust the Author** 」ボタンをクリックします。

![壊れた画像](./media/image2.png)

3.  右下隅にある **Copilot** アイコンをクリックし、**Github Copilot
    Chat** を選択します。

![壊れた画像](./media/image3.png)

4.  プロンプトを入力します
    プロジェクトに新しいノートブックを作成します。コマンド /newnotebook
    を使用して、"COVID19 Worldwide Testing Data" という名前を付けます。

![壊れた画像](./media/image4.png)

5.  手順に役立つ Copilot
    の手順を確認できます。手順に従って、ノートブックを作成します。

    - **Ctrl+Shift+P** を押してコマンド パレットを開きます。

    - 「Jupyter: Create New Blank
      Notebook」と入力し、Enterキーを押します。

![壊れた画像](./media/image5.png)

- 新しいノートブックが作成されます。COVID19WorldwideTesting Data.ipynbという名前で保存します。新しいノートブックの保存方法を
  Copilot に尋ねることもできます。

![壊れた画像](./media/image6.png)

- コピー先フォルダに移動します-**excercisefiles?dataengineer**   
  COVID19WorldwideTesting Data.ipynb を入力し、ファイルを保存します。

![壊れた画像](./media/image7.png)

6.  ファイルが
    **dataengineer**フォルダーの下に作成されたことがわかります。

![コンピューターのスクリーンショット説明が自動的に生成されます](./media/image8.png)

7.  Copilot と Copilot
    チャットを使用して演習を開発し、学習をサポートします。

**運動**

私たちの分析は、この質問に対する答えを提供しようとしています: **Which
countries have reported the highest number of positive cases in relation
to the number of tests conducted?**

**タスク1 : 必要なライブラリのインポート**

1.  Notebook kernel をクリックし「#Import Required Libraries.Including
    Pandas」と入力してEnterキーを押します。

![コンピューターのスクリーンショット説明が自動的に生成されます](./media/image9.png)

2.  タブキーを押します。列の最後まで連れて行ってくれます。Enter
    キーを押し、もう一度 Tab
    キーを押して、すべてのライブラリを追加します。

![コンピューターのスクリーンショット説明が自動的に生成されます](./media/image10.png)

\# Import the necessary libraries, including pandas.

\# Import Required Libraries

\# Here we are importing the necessary libraries for our task

import pandas as pd \#
pandasは、データ操作と分析のためにPythonプログラミング言語用に書かれたソフトウェアライブラリです。

![コンピューターのスクリーンショット説明が自動的に生成されます](./media/image11.png)

**タスク 2 : データセットのロード**

1.  pandas
    を使用して、ルートレベルから「tested_worldwide.csv」ファイルをロードします。

2.  データの読み込み方法については、Github Copilot
    に依頼してください。「Pandasを使用してルートレベルから「tested_worldwide.csv」ファイルをロードします。

![壊れた画像](./media/image12.png)

3.  ノートブックに以下のコードを入力して実行します。**Python
    Environment**を選択するように求められます。それを選択します。

![壊れた画像](./media/image13.png)

4.  推奨環境を選択します。スクリプトが実行され、結果が提供されます。

![壊れた画像](./media/image14.png)

![コンピューターのスクリーンショット説明が自動的に生成されます](./media/image15.png)

タスク 3 : データの理解

1.  head() 関数を使用して、データセットの最初の 5 行を表示します

2.  データセットの最初の 5 行を表示するコードについて、Github Copilot
    に依頼してください。データセットの最初の 5 行を表示します

![壊れた画像](./media/image16.png)

3.  **「+ code」**をクリックして、新しい kerner を開きます。#
    データセットの最初の 5
    行を表示すると入力するだけです。質問を自動的に予測します。タグを押してから
    Enterキーを押すだけです。

![画面
コンピュータ画面のスクリーンショット説明が自動生成される](./media/image17.png)

4.  **Copilot**は探しているコマンドを予測するので、タブを押してコードを受け入れます。独自のコードを編集/記述するオプションが常にあります。

![壊れた画像](./media/image18.png)

5.  タブを押してコードを受け入れます。カーネルを実行します。

![壊れた画像](./media/image19.png)

6.  結果が表示されます。

![コンピューター画面のスクリーンショット説明が自動的に生成されます](./media/image20.png)

![コンピューターのスクリーンショット説明が自動的に生成されます](./media/image21.png)

7.  コパイロットに、dataframeの行数と列数を表示することを手伝ってもらいます。+コードをクリックします。コードを入力し、カーネルを実行します。以下のコードを使用することもできます

8.  num_rows, num_cols = data.shape

9.  print("Number of rows:", num_rows)

print("Number of columns:", num_cols)

![壊れた画像](./media/image22.png)

10. コパイロットにこの手伝いを依頼してください
    各列のデータ型を表示します
    。また、data.dttypesを使用することもできます。

![コンピューターのスクリーンショット説明が自動的に生成されます](./media/image23.png)

11. GitHub Copilot
    に、各列に欠損値の数を表示するためのコードを提供するように依頼します。

![コンピューターのスクリーンショット説明が自動的に生成されます](./media/image24.png)

12. 新しいカーネルを追加し、以下のコードを追加して実行します。Copilot
    が提案したコードを使用して、

13. missing_values = df.isnull().sum()

print(missing_values)

![コンピュータプログラムのスクリーンショット説明が自動的に生成されます](./media/image25.png)

14. 新しいカーネルで以下のコードを実行して、各列の一意の値の数を表示します。コードと結果については、コパイロットに確認してください。

15. unique_values = df.nunique()

print(unique_values)

![コンピューターのスクリーンショット説明が自動的に生成されます](./media/image26.png)

**タスク4 : データ・クリーニング**

1.  以下のコードを実行して、分析に不要な列を削除します。コパイロットにコードを依頼し、結果を確認します。

> data = df\[\['Country_Region', 'positive', 'total_tested'\]\]

![コンピューターのスクリーンショット説明が自動的に生成されます](./media/image27.png)

2.  「#Rename the columns to make them more
    readable 」入力し、コードを受け入れます。

![コンピューターのスクリーンショット説明が自動的に生成されます](./media/image28.png)

3.  以下のコードを使用して実行できます。

df.rename(columns={'Country_Region': 'Country', 'positive': 'Positive
Cases', 'total_tested': 'Total Tested'}, inplace=True)

![コンピューターのスクリーンショット説明が自動的に生成されます](./media/image29.png)

4.  コパイロットに、欠損値のある行を削除する 新しいカーネルで「#Drop the
    rows that have missing values」入力する 新しいカーネルで Enter
    キーを押すように依頼します。タブを押してコードを受け入れます

![コンピューターのスクリーンショット説明が自動的に生成されます](./media/image30.png)

5.  新しい +Code カーネルを追加し、「#Convert the data types of the
    columns to the appropriate
    types」入力し、**tag**を押してコードを受け入れ、もう一度入力して Tab
    キーを押します。陽性症例、検査済み総数、および国のコードを生成し、実行します。

![コンピューターのスクリーンショット説明が自動的に生成されます](./media/image31.png)

6.  新しい +Code カーネルを追加し、「#Display the number of missing
    values in each column」入力します。Tab
    キーを押してコードを受け入れます。GitHub Copilot
    チャットで質問することもできます

![コンピュータプログラムのスクリーンショット説明が自動的に生成されます](./media/image32.png)

![コンピューター画面のスクリーンショット説明が自動的に生成されます](./media/image33.png)

**タスク5:Covid-19症例が最も多い上位10か国を抽出します。**

1.  Copilot チャットにコードの手伝いを依頼する
    各国の陽性症例の総数を含む新しいdataframeを作成する
    または、新しいコードを開き、「#Create a new dataframe that contains
    the total number of positive cases for each
    country」入力して、Enterを押します。Tabキーを押してコードに受け入れます。

![コンピューターのスクリーンショット説明が自動的に生成されます](./media/image34.png)

2.  In a new code enter below prompts and enter after each prompt to
    accept the code and run it.

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

![コンピューター画面のスクリーンショット説明が自動的に生成されます](./media/image35.png)

8.  Copilot にdataframeをポジティブ
    ケースの総数の降順に並べ替えるように依頼する または、「# Sort the
    dataframe in descending order of the total number of positive
    cases」と入力します 新しいコード
    カーネルでタグを押してコードを受け入れて実行します。

![コンピューターのスクリーンショット説明が自動的に生成されます](./media/image36.png)

9.  Github Copilot チャットに「Display the top ten countries with the
    most positive cases」または、新しいコード カーネルに「# Display the
    top ten countries with the most positive
    cases」と入力して実行します。表示するだけでよいことを忘れないでください。

![コンピューターのスクリーンショット説明が自動的に生成されます](./media/image37.png)

**タスク 6 : テストされた症例に対する最も陽性的なものを特定する**

1.  GitHub Copilot Chat
    にこれを手伝ってもらいます。「Create a new dataframe that contains
    the total number of tests conducted for each country」、または「 \#
    Create a new dataframe that contains the total number of tests
    conducted for each country」と入力し、Tab
    キーを押してコードにアクセスします。必要に応じてコードを編集して実行できます。

2.  \#
    データを「国」でグループ化し、「テスト済み合計」の合計を計算します

3.  total_tests = data.groupby('国')「'テスト済み合計'」.sum()

4.  

5.  \# 各国で実施されたテストの合計を含む新しいdataframeを作成します

6.  df_total_tests = PD。DataFrame({'国': total_tests.index,
    '合計テスト数': total_tests.values})

7.  

8.  \# 新しいdataframeを表示する

df_total_tests

![コンピューターのスクリーンショット説明が自動的に生成されます](./media/image38.png)

9.  Github Copilot Chat「Sort the dataframe in descending order of the
    total number of tests conducted」または「# Sort the dataframe in
    descending order of the total number of tests
    conducted」と入力し、tabを押してコードを受け入れて実行します。

![コンピュータプログラムのスクリーンショット説明が自動的に生成されます](./media/image39.png)

10. Github Copilot Chatに「Display the top ten countries with the most
    tests conducted」または、新しいコードカーネルを開き、「# Display the
    top ten countries with the most tests
    conducted」と入力し、Tabを押してコードを受け入れて実行します。

![コンピュータプログラムのスクリーンショット説明が自動的に生成されます](./media/image40.png)

**タスク7:実施された検査の数に対して陽性者数が最も多い上位3か国を特定する**

1.  Github Copilot チャットに「前の手順で作成した 2
    つのデータフレームをマージする」と尋ねるか、新しいコード
    カーネルを開き、「# 最もテストが実施された上位 10
    か国を表示する」と入力し、Tabキーを押してコードを受け入れて実行します。

![コンピューターのスクリーンショット説明が自動的に生成されます](./media/image41.png)

2.  Github Copilot Chatに「Create a new column that contains the
    ratio of positive cases to the number of tests
    conducted 」と尋ねるか、新しいコードカーネルを開き、「# Create a new
    column that contains the ratio of positive cases to the number of
    tests conducted」と入力し、tabを押してコードを受け入れて実行します。

![コンピューターのスクリーンショット説明が自動的に生成されます](./media/image42.png)

3.  Github Copilot Chatに「Sort the dataframe in descending order of the
    ratio of positive cases to the number of tests
    conducted」または、新しいコードカーネルを開き、「# Sort the
    dataframe in descending order of the ratio of positive cases to the
    number of tests
    conducted」と入力して質問します。そしてタブを押してコードを受け入れて実行します。

![コンピューターのスクリーンショット説明が自動的に生成されます](./media/image43.png)

4.  Github Copilot Chatに「Display the top three countries with the
    highest ratio of positive cases to the number of tests
    conducted 」または、新しいコードカーネルを開いて「#Display the top
    three countries with the highest ratio of positive cases to the
    number of tests
    conducted」と入力し、タブを押してコードを受け入れて実行します。

5.  \#Display the top three countries with the highest ratio of positive
    cases to the number of tests conducted

6.  top_countries = merged_df.nlargest(3, 'Positive Test Rate')

top_countries\[\['Country', 'Positive Test Rate'\]\]

![コンピューターのスクリーンショット説明が自動的に生成されます](./media/image44.png)

**タスク8 : 結果の表示**

1.  Github Copilot Chatに「Display the results a chart that shows the
    top three countries with the highest ratio of positive cases to the
    number」または、新しいコードカーネルを開いて「# Display the results
    a chart that shows the top three countries with the highest ratio of
    positive cases to the
    number」と入力し、タブを押してコードを受け入れて実行します

2.  \#Display the results a chart that shows the top three countries
    with the highest ratio of positive cases to the number

3.  import matplotlib.pyplot as plt

top_countries.plot(x='Country', y='Positive Test Rate', kind='bar')

![コンピュータプログラムのスクリーンショット説明が自動的に生成されます](./media/image45.png)

4.  Github Copilot Chatに「Display the results in a chart that shows the
    top ten countries with the most positive
    cases」を依頼するか、新しいコードカーネルを開き、「# Display the
    results in a chart that shows the top ten countries with the most
    positive cases」と入力し、タブを押してコードを受け入れて実行します。

&nbsp;

5.  \#Display the results in a chart that shows the top ten countries
    with the most positive cases

6.  import matplotlib.pyplot as plt

7.  df_total_positive_cases.head(10).plot(x='Country', y='Total Positive
    Cases', kind='bar')

8.  plt.xlabel('Country')

9.  plt.ylabel('Total Positive Cases')

10. plt.title('Top Ten Countries with the Most Positive Cases')

plt.show()

![コンピューター画面のスクリーンショット説明が自動的に生成されます](./media/image46.png)

11. Github Copilot Chatに「Display the results in a chart that shows the
    top ten countries with the most tests
    conducted」と依頼するか、新しいコードカーネルを開いて「# Display the
    results in a chart that shows the top ten countries with the most
    tests
    conducted」と入力し、タブを押してコードを受け入れて実行します。

![コンピューターのスクリーンショット説明が自動的に生成されます](./media/image47.png)

**タスク 9: 結論**

1.  結論は何ですか?

2.  この分析の限界は何ですか?

3.  この分析を改善するために、次のステップは何ですか?
