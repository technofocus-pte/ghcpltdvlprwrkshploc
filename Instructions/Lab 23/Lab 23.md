**Lab 23 - Construir um classificador de árvore de decisão baseado em
Scikit-learn e Python usando Github Copilot Chat**

**INTRODUÇÃO**

O arquivo diabetes.csv é originalmente do National Institute of Diabetes
and Digestive and Kidney Diseases. O objetivo do conjunto de dados é
prever, de forma diagnóstica, se um paciente tem diabetes, com base em
determinadas medições diagnósticas incluídas no conjunto de dados.
Várias restrições foram aplicadas na seleção dessas instâncias a partir
de um banco de dados maior. Em particular, todos os pacientes aqui são
mulheres com pelo menos 21 anos de idade e de origem indígena Pima.

2- No arquivo diabetes.csv, você encontrará diversas variáveis, algumas
delas independentes (diversas variáveis médicas preditoras) e apenas uma
variável-alvo dependente (Resultado).

**Tarefa 1: INSTRUÇÕES para criar um notebook usando o Github Copilot
Chat**

1.  No **Explorer** **in Visual Studio Code**, expanda
    **datascientist**.

2.  Clique no ícone **Copilot** no canto inferior direito e selecione
    **Github Copilot Chat.**

![A screenshot of a computer Description automatically
generated](./media/image1.png)

3.  Digite o prompt create a new notebook in a project. Use o comando
    /newnotebook e nomeie-o como "Diabetes Tree Classifier".

![A screenshot of a computer Description automatically
generated](./media/image2.png)

4.  Clique em **Terminal -\> New Terminal** na barra de ferramentas,
    conforme mostrado na imagem abaixo.

![BrokenImage](./media/image3.png)

5.  Selecione **Gitbash** no terminal e execute o comando que o Copilot
    sugeriu no diretório **datascientist**.

cd \exercisefiles\datascientist

touch "DiabetesTreeClassifier.ipynb"

![BrokenImage](./media/image4.png)

![A screenshot of a computer Description automatically
generated](./media/image5.png)

6.  Você deverá ver que o arquivo foi criado dentro da pasta
    **datascientist**.

![A screenshot of a computer Description automatically
generated](./media/image6.png)

7.  Selecione o notebook recém-criado para desenvolver o exercício.

![A screenshot of a computer Description automatically
generated](./media/image7.png)

8.  Use o Copilot e o Copilot Chat para desenvolver o exercício e apoiar
    o seu aprendizado.

**EXERCÍCIO**

O objetivo deste projeto é construir um classificador de árvore de
decisão baseado em Scikit-learn e Python. O classificador deve ser capaz
de prever se um paciente tem diabetes ou não, com base em determinadas
medições de diagnóstico incluídas no conjunto de dados.

**Tarefa 2: Importando as bibliotecas necessárias para construir um
classificador de árvore de decisão.**

1.  Clique no Notebook do kernel e digite \# Import the necessary
    libraries, including pandas, sklearn, etc. e pressione Enter e
    depois Tab para aceitar o código

2.  Pressione Tab. Isso o levará até o final da linha. Pressione Enter e
    novamente Tab para adicionar todas as bibliotecas.

3.  \# pandas para manipulação e análise de dados

4.  \# matplotlib para visualização de dados

5.  \# train_test_split para dividir os dados em conjuntos de
    treinamento e teste

6.  \# DecisionTreeClassifier para classificação com árvore de decisão

\# accuracy_score para avaliar o modelo

![A computer screen shot of a computer Description automatically
generated](./media/image8.png)

![A screenshot of a computer Description automatically
generated](./media/image9.png)

7.  Execute o código. Será solicitado que você selecione o ambiente
    Python, selecione-o e execute.![BrokenImage](./media/image10.png)

8.  Aguarde até que todas as bibliotecas sejam importadas.

![A screenshot of a computer program Description automatically
generated](./media/image11.png)

**Tarefa 3: Carregando o conjunto de dados**

1.  Abra o arquivo **diabetes.csv** e observe os nomes das colunas.

![A screen shot of a computer Description automatically
generated](./media/image12.png)

2.  Carregue o conjunto de dados de diabetes usando pandas ou a partir
    dos conjuntos de dados do sklearn. Abra um novo kernel de código e
    digite: # Load the diabetes dataset using pandas or from sklearn
    datasets E pressione Tab para aceitar o código

3.  Abra o Github Copilot chat e peça para carregar o conjunto de dados
    de diabetes usando pandas ou sklearn datasets. Ele fornecerá o
    código para carregar o conjunto de dados de diabetes usando pandas
    ou sklearn datasets.

![A screenshot of a computer program Description automatically
generated](./media/image13.png)

4.  Clique em +code para abrir um novo kernel, copie o código sugerido
    pelo Copilot e execute. Você também pode usar o código abaixo para
    carregar os dados.

5.  \# Load the Diabetes Dataset

6.  col_names = \['pregnant', 'glucose', 'bp', 'skin', 'insulin', 'bmi',
    'pedigree', 'age', 'label'\]

7.  \# load dataset

8.  diabetes_df = pd.read_csv("diabetes.csv", header=None,
    names=col_names)

\# Display the first 5 rows of the DataFrame

![A screenshot of a computer Description automatically
generated](./media/image14.png)

**Tarefa 4 : Análise Exploratória de Dados**

Exiba o número de linhas e colunas na estrutura de dados. Exiba os tipos
de dados de cada coluna. Exiba o número de valores ausentes em cada
coluna. Exiba o número de valores únicos em cada coluna. Exiba as
estatísticas básicas de cada coluna.

1.  Abra um novo Code kernel e digite: \#Display the first 5 rows of the
    dataframe e Pressione Enter. Pressione Tab para aceitar o código.
    Você também pode usar o código abaixo:

2.  \#Display the first 5 rows of the dataframe diabetes_df.head()

![A screenshot of a computer Description automatically
generated](./media/image15.png)

3.  Abra um novo Code kernel e digite: \#Display the data types of each
    column. Pressione Enter. Pressione Tab para aceitar o código.

![A screenshot of a computer program Description automatically
generated](./media/image16.png)

4.  Abra um novo Code kernel e digite: \#Display the number of missing
    values in each column. Pressione Enter. Pressione Tab para aceitar o
    código.

![A screenshot of a computer program Description automatically
generated](./media/image17.png)

5.  Abra um novo Code kernel e digite: \#Display the number of unique
    values in each colum.  Pressione Enter. Pressione Tab para aceitar o
    código.

![A screenshot of a computer program Description automatically
generated](./media/image18.png)

6.  Abra um novo Code kernel e digite: #Display the summary statistics
    of the dataframe. Pressione Enter. Pressione Tab para aceitar o
    código.

![A screenshot of a computer Description automatically
generated](./media/image19.png)

**Tarefa 5: Seleção de recursos**

1.  Selecione os recursos que você deseja usar para a previsão. Você
    pode usar todos os recursos ou um subconjunto deles.

2.  Abra um novo Code kernel e digite: # Split the data into features
    and target variables. Pressione Enter. Pressione Tab para aceitar o
    código. Você pode pedir uma explicação ao chat Copilot. Você também
    pode usar o código abaixo e executá-lo.

3.  \#split dataset in features and target variable

4.  feature_cols = \['pregnant', 'insulin', 'bmi',
    'age','glucose','bp','pedigree'\]

5.  X = diabetes_df\[feature_cols\] \# Features

y = diabetes_df.label \# Target variable

![A screenshot of a computer screen Description automatically
generated](./media/image20.png)

6.  Divida os dados em conjuntos de treinamento e teste. O conjunto de
    treinamento será usado para treinar o modelo e o conjunto de teste
    será usado para avaliar o modelo.

7.  Abra um novo Code kernel e digite: # Split the data into training
    and testing sets e pressione Enter. Pressione Tab para aceitar o
    código. Você pode pedir uma explicação ao chat Copilot. Você também
    pode usar o código abaixo e executá-lo.

8.  \# Split dataset into training set and test set

X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.3,
random_state=1) \# 70% training and 30% test

![A screenshot of a computer program Description automatically
generated](./media/image21.png)

**Tarefa 6: Construir um modelo de árvore de decisão**

1.  Construa um modelo de árvore de decisão usando o conjunto de
    treinamento.

2.  Abra um novo Code kernel e digite: # Split the data into training
    and testing sets e pressione Enter. Pressione Tab para aceitar o
    código. Você pode pedir uma explicação ao chat Copilot. Você também
    pode usar o código abaixo e executá-lo.

3.  \# Building Decision Tree Model

4.  \# Create Decision Tree classifer object

5.  clf = DecisionTreeClassifier()

6.  \# Train Decision Tree Classifer

7.  clf = clf.fit(X_train,y_train)

8.  \#Predict the response for test dataset

y_pred = clf.predict(X_test)

9.  Você pode ver ValueError. Peça ao Github Copilot para corrigir o
    problema. Siga as instruções do chat do Copilot e corrija o
    problema.

![A screenshot of a computer program Description automatically
generated](./media/image22.png)

10. Abra um novo Code kernel e digite: # Model Accuracy, how often is
    the classifier correct? Pressione Enter. Pressione Tab para aceitar
    o código. Você pode pedir uma explicação ao chat Copilot. Você
    também pode usar o código abaixo e executá-lo.

11. \# Evaluating Model

12. \# Model Accuracy, how often is the classifier correct?

print("Accuracy:",metrics.accuracy_score(y_test, y_pred))

13. Evaluate the model using the testing set.

14. \# Evaluating Model

15. \# Model Accuracy, how often is the classifier correct?

print("Accuracy:",metrics.accuracy_score(y_test, y_pred))
