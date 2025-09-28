**Laboratorio 23 - Crear un clasificador de árbol de decisión basado en
Scikit-learn y Python usando GitHub Copilot Chat**

**INTRODUCCIÓN**

Diabetes.csv proviene originalmente del National Institute of Diabetes
and Digestive and Kidney Diseases. El objetivo del conjunto de datos es
predecir de manera diagnóstica si un paciente tiene diabetes, basado en
ciertas mediciones diagnósticas incluidas en el conjunto de datos. Se
establecieron varias restricciones en la selección de estas instancias a
partir de una base de datos más grande. En particular, todos los
pacientes aquí son mujeres de al menos 21 años de edad y de ascendencia
Pima.

A partir de diabetes.csv se pueden encontrar varias variables, algunas
de ellas son independientes (varias variables predictoras médicas) y
solo una variable dependiente objetivo (Outcome).

**Tarea 1: INSTRUCCIONES para crear un notebook usando GitHub Copilot
Chat**

1.  Desde **Explorer in Visual Studio code**, expanda **datascientist**.

2.  Haga clic en el icono de **Copilot** en la esquina inferior derecha
    y seleccione **GitHub Copilot Chat.**

![A screenshot of a computer Description automatically
generated](./media/image1.png)

3.  Escriba su prompt create a new notebook in a project.  
    Use el comando /newnotebook y nómbrelo como "Diabetes Tree
    Classifier"

![A screenshot of a computer Description automatically
generated](./media/image2.png)

4.  Haga clic en **Terminal -\> New Terminal** desde la barra de
    herramientas, como se muestra en la imagen a continuación.

![BrokenImage](./media/image3.png)

5.  Seleccione **Gitbash** desde la terminal y ejecute el comando que
    Copilot sugirió en el directorio **datascientist**.

cd \exercisefiles\datascientist

touch "DiabetesTreeClassifier.ipynb"

![BrokenImage](./media/image4.png)

![A screenshot of a computer Description automatically
generated](./media/image5.png)

6.  Debería ver que el archivo fue creado dentro de la carpeta
    **datascientist**.

![A screenshot of a computer Description automatically
generated](./media/image6.png)

7.  Seleccione el notebook recién creado para desarrollar el ejercicio.

![A screenshot of a computer Description automatically
generated](./media/image7.png)

8.  Use Copilot y Copilot Chat para desarrollar el ejercicio y apoyar su
    aprendizaje.

**EJERCICIO**

El objetivo de este proyecto es construir un clasificador de árbol de
decisión basado en Scikit-learn y Python. El clasificador debe ser capaz
de predecir si un paciente tiene diabetes o no, en función de ciertas
mediciones diagnósticas incluidas en el conjunto de datos.

**Tarea 2: Importar las bibliotecas necesarias para construir un
clasificador de árbol de decisión**

1.  Haga clic en Notebook kernel y escriba \# Import the necessary
    libraries, including pandas, sklearn, etc. y presione Enter, luego
    presione Tab para aceptar el código.

2.  Presione Tab. Esto lo llevará al final de la línea. Presione Enter y
    nuevamente presione Tab para agregar todas las bibliotecas.

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

7.  Ejecute el código. Le pedirá que seleccione el entorno de Python,
    selecciónelo y ejecútelo.

![BrokenImage](./media/image10.png)

8.  Espere hasta que todas las bibliotecas se importen.

![A screenshot of a computer program Description automatically
generated](./media/image11.png)

**Tarea 3: Cargar el conjunto de datos**

1.  Abra el archivo **diabetes.csv** y observe los nombres de las
    columnas.

![A screen shot of a computer Description automatically
generated](./media/image12.png)

2.  Cargue el conjunto de datos diabetes usando pandas o desde sklearn
    datasets. Abra un nuevo kernel de código y escriba \# Load the
    diabetes dataset using pandas or from sklearn datasets y presione
    Tab para aceptar el código

3.  Abra GitHub Copilot chat y pida Load the diabetes dataset using
    pandas or from sklearn datasets. Le proporcionará el código para
    cargar el conjunto de datos diabetes usando pandas o sklearn
    datasets

![A screenshot of a computer program Description automatically
generated](./media/image13.png)

4.  Haga clic en +code para abrir un nuevo kernel, copie el código que
    le sugirió Copilot y ejecútelo.

5.  \# Load the Diabetes Dataset

6.  col_names = \['pregnant', 'glucose', 'bp', 'skin', 'insulin', 'bmi',
    'pedigree', 'age', 'label'\]

7.  \# load dataset

8.  diabetes_df = pd.read_csv("diabetes.csv", header=None,
    names=col_names)

\# Display the first 5 rows of the DataFrame

![A screenshot of a computer Description automatically
generated](./media/image14.png)

**Tarea 4: Análisis exploratorio de datos**

Mostrar el número de filas y columnas en el dataframe. Mostrar los tipos
de datos de cada columna. Mostrar el número de valores faltantes en cada
columna. Mostrar el número de valores únicos en cada columna. Mostrar
las estadísticas básicas de cada columna.

1.  Abra un nuevo kernel de código y escriba \#Display the first 5 rows
    of the dataframe. Presione Enter. Presione la tecla Tab para aceptar
    el código.  
    También puede usar el siguiente código.

2.  \#Display the first 5 rows of the dataframe

diabetes_df.head()

![A screenshot of a computer Description automatically
generated](./media/image15.png)

3.  Abra un nuevo kernel de código y escriba \#Display the data types of
    each column. Presione Enter. Presione la tecla Tab para aceptar el
    código.

![A screenshot of a computer program Description automatically
generated](./media/image16.png)

4.  Abra un nuevo kernel de código y escriba \#Display the number of
    missing values in each column. Presione Enter. Presione la tecla Tab
    para aceptar el código.

![A screenshot of a computer program Description automatically
generated](./media/image17.png)

5.  Abra un nuevo kernel de código y escriba \#Display the number of
    unique values in each column. Presione Enter. Presione la tecla Tab
    para aceptar el código.

![A screenshot of a computer program Description automatically
generated](./media/image18.png)

6.  Abra un nuevo kernel de código y escriba \#Display the summary
    statistics of the dataframe. Presione Enter. Presione la tecla Tab
    para aceptar el código.

![A screenshot of a computer Description automatically
generated](./media/image19.png)

**Tarea 5: Selección de funciones**

1.  Seleccione las funciones que desea usar para la predicción. Puede
    usar todas las funciones o un subconjunto de ellas.

2.  Abra un nuevo kernel de código y escriba \# Split the data into
    features and target variables. Presione Enter. Presione la tecla Tab
    para aceptar el código. Puede pedir a Copilot chat una explicación.
    También puede usar el siguiente código y ejecutarlo.

3.  \#split dataset in features and target variable

4.  feature_cols = \['pregnant', 'insulin', 'bmi',
    'age','glucose','bp','pedigree'\]

5.  X = diabetes_df\[feature_cols\] \# Features

y = diabetes_df.label \# Target variable

![A screenshot of a computer screen Description automatically
generated](./media/image20.png)

6.  Divida los datos en conjuntos de entrenamiento y prueba. El conjunto
    de entrenamiento se usará para entrenar el modelo y el conjunto de
    prueba se usará para evaluarlo.

7.  Abra un nuevo kernel de código y escriba \# Split the data into
    training and testing sets. Presione Enter. Presione la tecla Tab
    para aceptar el código. Puede pedir a Copilot chat una explicación.

8.  \# Split dataset into training set and test set

X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.3,
random_state=1) \# 70% training and 30% test

![A screenshot of a computer program Description automatically
generated](./media/image21.png)

**Tarea 6: Construir el modelo de árbol de decisión**

1.  Cree un modelo de árbol de decisión usando el conjunto de
    entrenamiento.

2.  Abra un nuevo kernel de código y escriba \# Split the data into
    training and testing sets. Presione Enter. Presione Tab para aceptar
    el código. Puede pedir a Copilot chat una explicación. También puede
    usar el siguiente código y ejecutarlo.

3.  \# Building Decision Tree Model

4.  \# Create Decision Tree classifer object

5.  clf = DecisionTreeClassifier()

6.  \# Train Decision Tree Classifer

7.  clf = clf.fit(X_train,y_train)

8.  \#Predict the response for test dataset

y_pred = clf.predict(X_test)

9.  Puede ver ValueError. Pida a GitHub Copilot que solucione el
    problema. Siga las instrucciones de Copilot Chat y corrija el
    problema.

![A screenshot of a computer program Description automatically
generated](./media/image22.png)

10. Abra un nuevo kernel de código y escriba \# Model Accuracy, how
    often is the classifier correct? Presione Enter. Presione la tecla
    Tab para aceptar el código. Puede pedir a Copilot chat una
    explicación. También puede usar el siguiente código y ejecutarlo.

11. \# Evaluating Model

12. \# Model Accuracy, how often is the classifier correct?

print("Accuracy:",metrics.accuracy_score(y_test, y_pred))

13. Evaluate the model using the testing set.

14. \# Evaluating Model

15. \# Model Accuracy, how often is the classifier correct?

print("Accuracy:",metrics.accuracy_score(y_test, y_pred))
