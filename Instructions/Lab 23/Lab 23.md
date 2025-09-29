**Lab 23 - Costruire un classificatore di albero decisionale basato su
Scikit-learn e Python utilizzando Github Copilot Chat**

**INTRODUZIONE**

diabetes.csv è originario dell'Istituto Nazionale di Diabete e Digestivo
e Renale

Malattie. L'obiettivo del set di dati è prevedere diagnosticamente se un
paziente ha il diabete,

sulla base di alcune misurazioni diagnostiche incluse nel set di dati.
Sono stati posti diversi vincoli

sulla selezione di queste istanze da un database più ampio. In
particolare, tutti i pazienti qui sono donne

almeno 21 anni di origine indiana Pima.2

Da diabetes.csv puoi trovare diverse variabili, alcune delle quali sono
indipendenti

(diverse variabili predittive mediche) e una sola variabile dipendente
dal bersaglio (Outcome).

**Attività 1 : ISTRUZIONI per creare un notebook utilizzando Github
Copilot Chat**

1.  Da **Explorer in Visual Studio code,** espandere **Datascientist**.

2.  Fare clic sull'icona **Copilot** nell'angolo in basso a destra e
    selezionare **Github Copilot Chat.**

![Uno screenshot di un computer Descrizione generata
automaticamente](./media/image1.png)

3.  Digitare il prompt per creare un nuovo notebook in un
    progetto. Usare il comando /newnotebook e chiamalo "Diabetes Tree
    Classifier"

![Uno screenshot di un computer Descrizione generata
automaticamente](./media/image2.png)

4.  Fare clic su **Terminal -\> New Terminal** dalla barra degli
    strumenti come mostrato nell'immagine sottostante.

![Immagine rotta](./media/image3.png)

5.  Selezionare **Gitbash** dal terminale ed eseguire il comando
    suggerito da Copilot nella directory del **datascientist**.

cd \exercisefiles\datascientist

touch "DiabetesTreeClassifier.ipynb"

![Immagine rotta](./media/image4.png)

![Uno screenshot di un computer Descrizione generata
automaticamente](./media/image5.png)

6.  Dovresti vedere che il file è stato creato nella cartella
    **datascientist**.

![Uno screenshot di un computer Descrizione generata
automaticamente](./media/image6.png)

7.  Selezionare il notebook appena creato per sviluppare l'esercizio.

![Uno screenshot di un computer Descrizione generata
automaticamente](./media/image7.png)

8.  Usare Copilot e Copilot Chat per sviluppare l'esercizio e supportare
    il vostro apprendimento.

**ESERCIZIO**

L'obiettivo di questo progetto è quello di costruire un classificatore
di alberi decisionali basato su Scikit-learn e Python. Il classificatore
dovrebbe essere in grado di prevedere se un paziente ha il diabete o
meno in base a

alcune misure diagnostiche incluse nel set di dati.

**Attività 2 : Importazione delle librerie necessarie per creare un
classificatore di alberi decisionali**

1.  Fare clic su Notebook kernel e digitare \# Importare le librerie
    necessarie, inclusi pandas, sklearn, ecc. e premere Invio e premere
    Tab per accettare il codice

2.  Premere Tab. Vi porterà al capolinea. Premere Enter e premere
    nuovamente Tab per aggiungere tutte le librerie.

3.  \# Panda per la manipolazione e l'analisi dei dati

4.  \# matplotlib per la visualizzazione dei dati

5.  \# train_test_split per suddividere i dati in set di addestramento e
    test

6.  \# DecisionTreeClassifier per la classificazione dell'albero
    decisionale

\# accuracy_score per la valutazione del modello

![Una schermata del computer di un computer Descrizione generata
automaticamente](./media/image8.png)

![Uno screenshot di un computer Descrizione generata
automaticamente](./media/image9.png)

7.  Eseguire il codice, ti chiederà di selezionare l'ambiente Python,
    selezionarlo ed eseguire

![Immagine rotta](./media/image10.png)

8.  Attendere che tutte le librerie vengano importate.

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image11.png)

**Attività 3 : Caricamento del set di dati**

1.  Aprire il file **diabetes.csv** e osservare i nomi delle colonne.

![Una schermata di un computer Descrizione generata
automaticamente](./media/image12.png)

2.  Caricare il set di dati sul diabete utilizzando pandas o da set di
    dati sklearn. Aprire il nuovo kernel del codice e digitare \#
    Caricare il set di dati sul diabete utilizzando pandas o da set di
    dati sklearn E premi Tab per accettare il codice

3.  Aprire la chat di Github Copilot e chiedere di caricare il set di
    dati sul diabete utilizzando pandas o da set di dati sklearn. Ti dà
    il codice Load il set di dati sul diabete usando pandas o da set di
    dati sklearn

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image13.png)

4.  Fare clic su +code per aprire un nuovo kernel, copiare il codice
    suggerito da Copilot ed eseguire. È inoltre possibile utilizzare il
    codice seguente per caricare i dati.

5.  \# Load the Diabetes Dataset

6.  col_names = \['pregnant', 'glucose', 'bp', 'skin', 'insulin', 'bmi',
    'pedigree', 'age', 'label'\]

7.  \# load dataset

8.  diabetes_df = pd.read_csv("diabetes.csv", header=None,
    names=col_names)

\# Display the first 5 rows of the DataFrame

![Uno screenshot di un computer Descrizione generata
automaticamente](./media/image14.png)

**Attività 4: Exploratory Data Analysis**

Visualizzare il numero di righe e colonne nel frame di dati.
Visualizzare i tipi di dati di ogni colonna. Visualizzare il numero di
valori mancanti in ogni colonna. Visualizzare il numero di valori
univoci in ogni colonna. Visualizza le statistiche di base di ogni
colonna.

1.  Aprire un nuovo Code kernel e digitare \#Display prime 5 righe del
    dataframe. Premere Enter. Premere la scheda per accettare il codice.
    Puoi anche utilizzare il codice qui sotto.

2.  \#Display the first 5 rows of the dataframe

diabetes_df.head()

![Uno screenshot di un computer Descrizione generata
automaticamente](./media/image15.png)

3.  Aprire un nuovo Code kernel e digitare \#Display i tipi di dati di
    ogni colonna. Premere la scheda per accettare il codice.

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image16.png)

4.  Aprire un nuovo Code kernel e digitare \#Display il numero di valori
    mancanti in ogni colonna. Premere Enter. Premere la scheda per
    accettare il codice.

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image17.png)

5.  Aprire un nuovo Code kernel e digitare \#Display il numero di valori
    univoci in ogni colonna. Premere Enter. Premi la scheda per
    accettare il codice.

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image18.png)

6.  Aprire un nuovo Code kernel e digitare \#Display le statistiche di
    riepilogo del dataframe. Premere Enter. Premi la scheda per
    accettare il codice.

![Uno screenshot di un computer Descrizione generata
automaticamente](./media/image19.png)

**Attività 5: Selezione delle funzioni**

1.  Selezionare le funzionalità che si desidera utilizzare per la stima.
    È possibile utilizzare tutte le funzionalità o un sottoinsieme di
    funzionalità.

2.  Aprire un nuovo Code kernel e digita \# Dividi i dati in
    funzionalità e variabili di destinazione. Premere Enter. Premi la
    scheda per accettare il codice. Puoi chiedere spiegazioni alla chat
    di Copilot. Puoi anche utilizzare il codice seguente ed eseguirlo.

3.  \#split dataset in features and target variable

4.  feature_cols = \['pregnant', 'insulin', 'bmi',
    'age','glucose','bp','pedigree'\]

5.  X = diabetes_df\[feature_cols\] \# Features

y = diabetes_df.label \# Target variable

![Uno screenshot dello schermo di un computer Descrizione generata
automaticamente](./media/image20.png)

6.  Suddividere i dati in set di training e di test. Il set di training
    verrà utilizzato per addestrare il modello e il set di testing verrà
    utilizzato per valutare il modello.

7.  Aprire un nuovo Code kernel e digitare \# Suddividere i dati in set
    di training e di test Premere Enter. Premi la scheda per accettare
    il codice. Puoi chiedere spiegazioni alla chat di Copilot. Puoi
    anche utilizzare il codice seguente ed eseguirlo.

8.  \# Split dataset into training set and test set

X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.3,
random_state=1) \# 70% training and 30% test

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image21.png)

**Attività 6: Costruzione di un modello di albero decisionale**

1.  Creare un modello di albero delle decisioni utilizzando il set di
    training.

2.  Aprire un nuovo Code kernel e digitare \# Suddividere i dati in set
    di training e di test Premere Invio. Premere la scheda per accettare
    il codice. Puoi chiedere spiegazioni alla chat di Copilot. Puoi
    anche utilizzare il codice seguente ed eseguirlo.

3.  \# Building Decision Tree Model

4.  \# Create Decision Tree classifer object

5.  clf = DecisionTreeClassifier()

6.  \# Train Decision Tree Classifer

7.  clf = clf.fit(X_train,y_train)

8.  \#Predict the response for test dataset

y_pred = clf.predict(X_test)

9.  È possibile visualizzare ValueError. Chiedere a Github Copilot di
    risolvere il problema. Seguire le istruzioni della chat di Copilot e
    risolvi il problema.

![Uno screenshot di un programma per computer Descrizione generata
automaticamente](./media/image22.png)

10. Aprire un nuovo Code kernel e digita \# Model Accuracy, con quale
    frequenza il classificatore è corretto? Premere Invio. Premere la
    scheda per accettare il codice. Puoi chiedere spiegazioni alla chat
    di Copilot. Puoi anche utilizzare il codice seguente ed eseguirlo.

11. \# Evaluating Model

12. \# Model Accuracy, how often is the classifier correct?

print("Accuracy:",metrics.accuracy_score(y_test, y_pred))

13. Evaluate the model using the testing set.

14. \# Evaluating Model

15. \# Model Accuracy, how often is the classifier correct?

print("Accuracy:",metrics.accuracy_score(y_test, y_pred))
