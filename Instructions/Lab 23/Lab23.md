**Lab 23 - Erstellen eines Entscheidungsbaum-Klassifikators basierend
auf Scikit-learn und Python mit Github Copilot Chat**

**EINLEITUNG**

diabetes.csv stammt ursprünglich vom National Institute of Diabetes and
Digestive and Kidney

Krankheiten. Ziel des Datensatzes ist es, diagnostisch vorherzusagen, ob
ein Patient an Diabetes leidet,

basierend auf bestimmten diagnostischen Messungen, die im Datensatz
enthalten sind. Es wurden mehrere Einschränkungen festgelegt

auf die Auswahl dieser Instanzen aus einer größeren Datenbank.
Insbesondere sind hier alle Patienten weiblich

mindestens 21 Jahre alt und von den Pima-Indianern abstammen.2

Von diabetes.csv aus finden Sie mehrere Variablen, von denen einige
unabhängig sind

(mehrere medizinische Prädiktorvariablen) und nur eine zielabhängige
Variable (Outcome).

**Aufgabe 1: ANWEISUNGEN zum Erstellen eines Notebooks mit Github
Copilot Chat**

1.  Erweitern Sie im **Explorer in Visual Studio Code** die Option
    **datascientist**.

2.  Klicken Sie auf das **Copilot**-Symbol in der rechten Ecke und
    wählen Sie **Github Copilot Chat**.

![Ein Screenshot eines Computers Beschreibung wird automatisch
generiert](./media/image1.png)

3.  Geben Sie Ihre Prompt

> create a new notebook in a project. Use command /newnotebook and name
> it as "Diabetes Tree Classifier"

![Ein Screenshot eines Computers Beschreibung wird automatisch
generiert](./media/image2.png)

4.  Klicken Sie auf **Terminal -\> New Terminal** aus der Symbolleiste,
    wie in der folgenden Abbildung gezeigt.

![Defektes Bild](./media/image3.png)

5.  Wählen Sie im Terminal **Gitbash** aus, und führen Sie den Befehl
    aus, den Copilot im **datascientist**-Verzeichnis vorgeschlagen hat.

cd \exercisefiles\datascientist

touch "DiabetesTreeClassifier.ipynb"

![Defektes Bild](./media/image4.png)

![Ein Screenshot eines Computers Beschreibung wird automatisch
generiert](./media/image5.png)

6.  Sie sollten sehen, dass die Datei im Ordner **"datascientist**"
    erstellt wurde.

![Ein Screenshot eines Computers Beschreibung wird automatisch
generiert](./media/image6.png)

7.  Wählen Sie das neu erstellte Notebook aus, um die Übung zu
    entwickeln.

![Ein Screenshot eines Computers Beschreibung wird automatisch
generiert](./media/image7.png)

8.  Verwenden Sie Copilot und Copilot Chat, um die Übung zu entwickeln
    und Ihr Lernen zu unterstützen.

**ÜBUNG**

Das Ziel dieses Projekts ist es, einen Entscheidungsbaum-Klassifikator
auf Basis von Scikit-learn und Python zu erstellen. Der Klassifikator
sollte in der Lage sein, vorherzusagen, ob ein Patient Diabetes hat oder
nicht, basierend auf

bestimmte diagnostische Messungen, die im Datensatz enthalten sind.

**Aufgabe 2 : Importieren der erforderlichen Bibliotheken zum Erstellen
eines Entscheidungsbaumklassifikators**

1.  Klicken Sie auf Notebook-Kernel und geben Sie ein: \# Import the
    necessary libraries, including pandas, sklearn usw. ein, und drücken
    Sie die Eingabetaste und drücken Sie die Tabulatortaste, um den Code
    zu akzeptieren

2.  Drücken Sie die Tabulatortaste. Es bringt Sie bis zum Ende der
    Linie. Drücken Sie die Eingabetaste und erneut die Tabulatortaste,
    um alle Bibliotheken hinzuzufügen.

3.  \# pandas for data manipulation and analysis

4.  \# matplotlib for data visualization

5.  \# train_test_split for splitting the data into training and testing
    sets

6.  \# DecisionTreeClassifier for decision tree classification

\# accuracy_score for evaluating the model

![Ein Computer-Screenshot eines Computers Beschreibung wird automatisch
generiert](./media/image8.png)

![Ein Screenshot eines Computers Beschreibung wird automatisch
generiert](./media/image9.png)

7.  Führen Sie den Code aus, Sie werden aufgefordert, die
    Python-Umgebung auszuwählen, sie auszuwählen und auszuführen

![Defektes Bild](./media/image10.png)

8.  Warten Sie, bis alle Bibliotheken importiert sind.

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image11.png)

**Aufgabe 3 : Laden des Datensatzes**

1.  Öffnen Sie die Datei **diabetes.csv** und beachten Sie die
    Spaltennamen.

![Ein Screenshot eines Computers Beschreibung wird automatisch
generiert](./media/image12.png)

2.  Laden Sie das Diabetes-Dataset mit Pandas oder aus sklearn-Datasets.
    Öffnen Sie den neuen Code-Kernel und geben Sie ein: \## Load the
    diabetes dataset using pandas or from sklearn datasets und drücken
    Sie die Tabulatortaste, um den Code zu akzeptieren.

3.  Öffnen Sie den Github Copilot-Chat, und bitten Sie darum, das
    Diabetes-Dataset mit Pandas oder aus sklearn-Datasets zu laden.Es
    gibt Ihnen den Code. Laden Sie das Diabetes-Dataset mit Pandas oder
    aus sklearn-Datasets

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image13.png)

4.  Klicken Sie auf +Code, um einen neuen Kernel zu öffnen, kopieren Sie
    den Code, der von Copilot vorgeschlagen wurde, und führen Sie ihn
    aus. Sie können auch den folgenden Code verwenden, um Daten zu
    laden.

5.  \# Load the Diabetes Dataset

6.  col_names = \['pregnant', 'glucose', 'bp', 'skin', 'insulin', 'bmi',
    'pedigree', 'age', 'label'\]

7.  \# load dataset

8.  diabetes_df = pd.read_csv("diabetes.csv", header=None,
    names=col_names)

\# Display the first 5 rows of the DataFrame

![Ein Screenshot eines Computers Beschreibung wird automatisch
generiert](./media/image14.png)

**Aufgabe 4 : Explorative Datenanalyse**

Zeigen Sie die Anzahl der Zeilen und Spalten im Datenrahmen an. Zeigen
Sie die Datentypen der einzelnen Spalten an. Zeigen Sie die Anzahl der
fehlenden Werte in jeder Spalte an. Zeigt die Anzahl der Einzelwerte in
jeder Spalte an. Zeigen Sie die grundlegenden Statistiken jeder Spalte
an.

1.  Öffnen Sie einen neuen Code-Kernel und geben Sie ein: \# Display the
    first 5 rows of the dataframe. Drücken Sie die Eingabetaste. Drücken
    Sie die Tabulatortaste, um den Code zu übernehmen. Sie können auch
    den folgenden Code verwenden.

2.  \#Display the first 5 rows of the dataframe

diabetes_df.head()

![Ein Screenshot eines Computers Beschreibung wird automatisch
generiert](./media/image15.png)

3.  Öffnen Sie einen neuen Code-Kernel, und geben Sie ein: \#Display the
    data types of each column. Drücken Sie die Eingabetaste. Drücken Sie
    die Tabulatortaste, um den Code zu übernehmen.

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image16.png)

4.  Öffnen Sie einen neuen Code-Kernel, und geben Sie ein: \#Display the
    number of missing values in each column. Drücken Sie die
    Eingabetaste. Drücken Sie die Tabulatortaste, um den Code zu
    übernehmen.

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image17.png)

5.  Öffnen Sie einen neuen Code-Kernel, und geben Sie ein: \# Display
    the number of unique values in each column. Drücken Sie die
    Eingabetaste. Drücken Sie die Tabulatortaste, um den Code zu
    übernehmen.

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image18.png)

6.  Öffnen Sie einen neuen Code-Kernel, und geben Sie ein: \##Display
    the summary statistics of the dataframe. Drücken Sie die
    Eingabetaste. Drücken Sie die Tabulatortaste, um den Code zu
    übernehmen.

![Ein Screenshot eines Computers Beschreibung wird automatisch
generiert](./media/image19.png)

**Aufgabe 5 : Auswahl von Funktionen**

1.  Wählen Sie die Features aus, die Sie für die Vorhersage verwenden
    möchten. Sie können alle Funktionen oder eine Teilmenge von
    Funktionen verwenden.

2.  Öffnen Sie einen neuen Code-Kernel, und geben Sie ein: \# Split the
    data into features and target variables. Drücken Sie die
    Eingabetaste. Drücken Sie die Tabulatortaste, um den Code zu
    übernehmen. Sie können den Copilot-Chat um eine Erklärung bitten.
    Sie können auch den folgenden Code verwenden und ausführen.

3.  \#split dataset in features and target variable

4.  feature_cols = \['pregnant', 'insulin', 'bmi',
    'age','glucose','bp','pedigree'\]

5.  X = diabetes_df\[feature_cols\] \# Features

y = diabetes_df.label \# Target variable

![Ein Screenshot eines Computerbildschirms Beschreibung wird automatisch
generiert](./media/image20.png)

6.  Unterteilen Sie die Daten in Trainings- und Testsätze. Der
    Trainingssatz wird zum Trainieren des Modells verwendet, und der
    Testsatz wird zum Auswerten des Modells verwendet.

7.  Öffnen Sie einen neuen Code-Kernel, und geben Sie ein: \# Split the
    data into training and testing sets. Drücken Sie die Eingabetaste.
    Drücken Sie die Tabulatortaste, um den Code zu übernehmen. Sie
    können den Copilot-Chat um eine Erklärung bitten. Sie können auch
    den folgenden Code verwenden und ausführen.

8.  \# Split dataset into training set and test set

X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.3,
random_state=1) \# 70% training and 30% test

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image21.png)

**Aufgabe 6: Erstellen eines Entscheidungsbaummodells**

1.  Erstellen Sie ein Entscheidungsbaummodell mithilfe des
    Trainingssatzes.

2.  Öffnen Sie einen neuen Code-Kernel, und geben Sie ein: \# Split the
    data into training and testing sets. Drücken Sie die Eingabetaste.
    Drücken Sie die Tabulatortaste, um den Code zu übernehmen. Sie
    können den Copilot-Chat um eine Erklärung bitten. Sie können auch
    den folgenden Code verwenden und ausführen.

3.  \# Building Decision Tree Model

4.  \# Create Decision Tree classifer object

5.  clf = DecisionTreeClassifier()

6.  \# Train Decision Tree Classifer

7.  clf = clf.fit(X_train,y_train)

8.  \#Predict the response for test dataset

y_pred = clf.predict(X_test)

9.  Sie können ValueError sehen. Bitten Sie Github Copilot, das Problem
    zu beheben. Befolgen Sie die Anweisungen im Copilot-Chat und beheben
    Sie das Problem.

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image22.png)

10. Öffnen Sie einen neuen Code-Kernel und geben Sie ein: \# Model
    Accuracy, how often is the classifier correct? Drücken Sie die
    Eingabetaste. Drücken Sie die Tabulatortaste, um den Code zu
    übernehmen. Sie können den Copilot-Chat um eine Erklärung bitten.
    Sie können auch den folgenden Code verwenden und ausführen.

11. \# Evaluating Model

12. \# Model Accuracy, how often is the classifier correct?

print("Accuracy:",metrics.accuracy_score(y_test, y_pred))

13. Werten Sie das Modell mithilfe des Testsatzes aus.

14. \# Evaluating Model

15. \# Model Accuracy, how often is the classifier correct?

print("Accuracy:",metrics.accuracy_score(y_test, y_pred))

