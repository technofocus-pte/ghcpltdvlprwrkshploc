**Laboratorio 22 - Crear un cuaderno con GitHub Copilot Chat y
proporcionar respuestas basadas en datos de prueba INTRODUCCIÓN**

Este conjunto de datos tested_worldwide.csv proviene de Kaggle. Este
conjunto de datos, que contiene el número de pruebas realizadas a lo
largo del tiempo, es importante para ayudar a comprender los casos
diarios reportados y entender cómo se está propagando realmente el
COVID-19 en cada país.

**INSTRUCCIONES**

1.  1\. Abra Visual Studio Code desde el menú Start de Windows y abra la
    carpeta navegando a C:\Labfiles\CopilotHackathon

![A screenshot of a computer Description automatically
generated](./media/image1.png)

2.  Haga clic en el botón **Yes,I Trust the Author**.

![BrokenImage](./media/image2.png)

3.  Haga clic en el icono de **Copilot** en la esquina inferior derecha
    y seleccione **GitHub Copilot Chat.**

![BrokenImage](./media/image3.png)

4.  Escriba su prompt create a new notebook in a project. Use el
    commando /newnotebook y nómbrelo como "COVID19 Worldwide Testing
    Data"

![BrokenImage](./media/image4.png)

5.  Puede ver que Copilot le mostrará instrucciones para ayudarle.  
    Siga los pasos y cree el notebook.

    - Abra la paleta de comandos presionando **Ctrl+Shift+P.**

    - Escriba Jupyter: Create New Blank Notebook y presione Enter.

![BrokenImage](./media/image5.png)

- Se creará un nuevo notebook. Guárdelo con el nombre
  COVID19WorldwideTesting Data.ipynb. También puede pedirle a Copilot
  cómo guardar un nuevo notebook.

![BrokenImage](./media/image6.png)

- Ir a la carpeta de destino - **excercisefiles-?
  dataengineer** ingrese COVID19WorldwideTesting Data.ipynb y guarde el
  archivo.

![BrokenImage](./media/image7.png)

6.  Debería ver que el archivo fue creado dentro de la carpeta
    **dataengineer**.

![A screenshot of a computer Description automatically
generated](./media/image8.png)

7.  Use Copilot y Copilot Chat para desarrollar el ejercicio y apoyar su
    aprendizaje.

**EJERCICIO**

Nuestro análisis intenta dar respuesta a esta pregunta: **¿Qué países
han reportado el mayor número de casos positivos en relación con el
número de pruebas realizadas?**

**Tarea 1: Importar las bibliotecas necesarias**

1.  Haga clic en Notebook kernel y escriba \#Import Required Libraries.
    Including Pandas y presione Enter

![A screenshot of a computer Description automatically
generated](./media/image9.png)

2.  Presione Tab. Esto lo llevará al final de la línea. Presione Enter y
    nuevamente presione Tab para agregar todas las librerías.

![A screenshot of a computer Description automatically
generated](./media/image10.png)

\# Import the necessary libraries, including pandas.

\# Import Required Libraries

\# Here we are importing the necessary libraries for our task

import pandas as pd \# pandas is a software library written for the
Python programming language for data manipulation and analysis.

![A screenshot of a computer Description automatically
generated](./media/image11.png)

**Tarea 2: Cargar el conjunto de datos**

1.  Use pandas para cargar el archivo 'tested_worldwide.csv' desde el
    nivel raíz

2.  Pídale ayuda a Github Copilot sobre cómo cargar datos. Ingrese Use
    pandas to load the 'tested_worldwide.csv' file from the root level

![BrokenImage](./media/image12.png)

3.  Ingrese el siguiente código en un Notebook y ejecútelo. Le pedirá
    que seleccione **Python Environment**. Selecciónelo.

![BrokenImage](./media/image13.png)

4.  Seleccione el entorno recomendado. El script se ejecuta y
    proporciona los resultados.

![BrokenImage](./media/image14.png)

![A screenshot of a computer Description automatically
generated](./media/image15.png)

Tarea 3: Comprender los datos

1.  Use la función head() para mostrar las primeras 5 filas del conjunto
    de datos

2.  Pídale a su GitHub Copilot que lo ayude con el código para mostrar
    las primeras 5 filas del conjunto de datos. display
    first 5 rows of the dataset

![BrokenImage](./media/image16.png)

3.  Haga clic en + code para abrir un nuevo kernel. Simplemente escriba
    \# display first 5 rows of dataset. Automáticamente predecirá su
    pregunta. Solo presione Tab y luego presione Enter.

![Screens screenshot of a computer screen Description automatically
generated](./media/image17.png)

4.  **Copilot** predice el comando que está buscando, así que presione
    Tab para aceptar el código. Siempre tiene la opción de
    editar/escribir su propio código.

![BrokenImage](./media/image18.png)

5.  Presione Tab y acepte el código. Ejecute el kernel.

![BrokenImage](./media/image19.png)

6.  Debería ver los resultados.

![A screenshot of a computer screen Description automatically
generated](./media/image20.png)

![A screenshot of a computer Description automatically
generated](./media/image21.png)

7.  Pídale a su Copilot que le ayude con **Display the number of rows
    and columns in the dataframe**. Haga clic en +code, ingrese el
    código y luego ejecute el kernel. También puede usar el siguiente
    código

8.  num_rows, num_cols = data.shape

9.  print("Number of rows:", num_rows)

print("Number of columns:", num_cols)

![BrokenImage](./media/image22.png)

10. Pídale a su Copilot que le ayude con Display the data types of each
    column. También puede usar el siguiente código df.dttypes

![A screenshot of a computer Description automatically
generated](./media/image23.png)

11. Pídale a su GitHub Copilot que proporcione el código para Display
    the number of missing values in each column.

![A screenshot of a computer Description automatically
generated](./media/image24.png)

12. Agregue un nuevo kernel y copie el siguiente código, luego
    ejecútelo. También puede usar el código sugerido por Copilot y
    verificar.

13. missing_values = df.isnull().sum()

print(missing_values)

![A screenshot of a computer program Description automatically
generated](./media/image25.png)

14. Ejecute el siguiente código en un nuevo kernel para mostrar el
    número de valores únicos en cada columna. Verifique con su Copilot
    el código y los resultados.

15. unique_values = df.nunique()

print(unique_values)

![A screenshot of a computer Description automatically
generated](./media/image26.png)

**Tarea 4: Limpieza de datos**

1.  Ejecute el siguiente código para eliminar las columnas que no son
    necesarias para el análisis. Pídale a Copilot el código y verifique
    los resultados.

data = df\[\['Country_Region', 'positive', 'total_tested'\]\]

![A screenshot of a computer Description automatically
generated](./media/image27.png)

2.  Escriba #Rename the columns to make them more readable en un nuevo
    kernel y acepte el código.

![A screenshot of a computer Description automatically
generated](./media/image28.png)

3.  Puede usar el siguiente código y ejecutarlo.

df.rename(columns={'Country_Region': 'Country', 'positive': 'Positive
Cases', 'total_tested': 'Total Tested'}, inplace=True)

![A screenshot of a computer Description automatically
generated](./media/image29.png)

4.  Pídale a su Copilot que elimine las filas que tienen valores
    faltantes y ejecute el código en un nuevo kernel o escriba \#Drop
    the rows that have missing values en un nuevo kernel, presione
    Enter. Presione la tecla Tab y acepte el código.

![A screenshot of a computer Description automatically
generated](./media/image30.png)

5.  Agregue un nuevo kernel con +Code y escriba \#Convert the data types
    of the columns to the appropriate types, presione **Tab** para
    aceptar el código, luego nuevamente Enter y presione Tab. Genere el
    código para Positive cases, Total Tested y country, y luego
    ejecútelo.

![A screenshot of a computer Description automatically
generated](./media/image31.png)

6.  Agregue un nuevo kernel con +Code y escriba \#Display the number of
    missing values in each column, luego presione Enter. Presione Tab y
    acepte el código. También puede preguntar en GitHub Copilot chat.

![A screenshot of a computer program Description automatically
generated](./media/image32.png)

![A screenshot of a computer screen Description automatically
generated](./media/image33.png)

**Tarea 5: Extraer los diez principales países con más casos de
Covid-19**

1.  Pídale a su Copilot Chat que le ayude con el código
    Create a new dataframe that contains the total number of positive
    cases for each country o abra un nuevo código y escriba \#Create a
    new dataframe that contains the total number of positive cases for
    each country y presione Enter. Presione Tab para aceptar el código.

![A screenshot of a computer Description automatically
generated](./media/image34.png)

2.  En un nuevo código, ingrese los siguientes prompts y presione Enter
    después de cada uno para aceptar el código y ejecutarlo.

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

8.  Pida a Copilot que ordene el dataframe en orden descendente del
    número total de casos positivos. O bien, escriba \# Sort the
    dataframe in descending order of the total number of positive cases
    en el nuevo kernel de código, presione Tab para aceptar el código y
    ejecútelo.

![A screenshot of a computer Description automatically
generated](./media/image36.png)

9.  Pida a su Github Copilot chat que le ayude con Display the top ten
    countries with the most positive cases. O bien, escriba \# Display
    the top ten countries with the most positive cases en un nuevo
    kernel de código y ejecútelo. Recuerde: solo necesita mostrar los
    resultados.

![A screenshot of a computer Description automatically
generated](./media/image37.png)

**Tarea 6: Identificar los casos positivos más altos en relación con los
casos analizados**

1.  Pida ayuda a su GitHub Copilot Chat para esto: Crear un nuevo
    dataframe que contenga el número total de pruebas realizadas para
    cada país o abra un nuevo kernel de código y escriba # Create a new
    dataframe that contains the total number of tests conducted for each
    country y presione tab para aceptar el código. Puede editar el
    código si es necesario y ejecutarlo.

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

9.  Pida a su Github Copilot Chat ordenar el dataframe en orden
    descendente del número total de pruebas realizadas o abra un nuevo
    kernel de código, escriba # Sort the dataframe in descending order
    of the total number of tests conducted y presione tab para aceptar
    el código y ejecutarlo.

![A screenshot of a computer program Description automatically
generated](./media/image39.png)

10. Pida a su Github Copilot Chat mostrar los diez países con el mayor
    número de pruebas realizadas o abra un nuevo kernel de código,
    escriba # Display the top ten countries with the most tests
    conducted y presione tab para aceptar el código y ejecutarlo.

![A screenshot of a computer program Description automatically
generated](./media/image40.png)

**Tarea 7: Identificar los tres principales países que han tenido el
mayor número de casos positivos en relación con el número de pruebas
realizadas**

1.  Pídale a su Github Copilot Chat que fusione los dos dataframes
    creados en los pasos anteriores o abra un nuevo kernel de código y
    escriba \# Display the top ten countries with the most tests
    conducted y presione tab para aceptar el código y ejecútelo.

![A screenshot of a computer Description automatically
generated](./media/image41.png)

2.  Pídale a su Github Copilot Chat que cree una nueva columna que
    contenga la proporción de casos positivos respecto al número de
    pruebas realizadas o abra un nuevo kernel de código y escriba \#
    Create a new column that contains the ratio of positive cases to the
    number of tests conducted y presione tab para aceptar el código y
    ejecútelo.

![A screenshot of a computer Description automatically
generated](./media/image42.png)

3.  Pídale a su Github Copilot Chat que ordene el dataframe en orden
    descendente de la proporción de casos positivos respecto al número
    de pruebas realizadas o abra un nuevo kernel de código y escriba \#
    Sort the dataframe in descending order of the ratio of positive
    cases to the number of tests conducted y presione tab para aceptar
    el código y ejecútelo.

![A screenshot of a computer Description automatically
generated](./media/image43.png)

4.  Pídale a su Github Copilot Chat que muestre los tres países con la
    mayor proporción de casos positivos respecto al número de pruebas
    realizadas o abra un nuevo kernel de código y escriba \#Display the
    top three countries with the highest ratio of positive cases to the
    number of tests conducted y presione tab para aceptar el código y
    ejecútelo.

5.  \#Display the top three countries with the highest ratio of positive
    cases to the number of tests conducted

6.  top_countries = merged_df.nlargest(3, 'Positive Test Rate')

top_countries\[\['Country', 'Positive Test Rate'\]\]

![A screenshot of a computer Description automatically
generated](./media/image44.png)

**Tarea 8: Mostrar los resultados**

1.  Pídale a su Github Copilot Chat que muestre los resultados en una
    gráfica que muestre los tres principales países con la mayor
    proporción de casos positivos en relación al número O abra un nuevo
    kernel de código y escriba \# Display the results a chart that shows
    the top three countries with the highest ratio of positive cases to
    the number y presione Tab para aceptar el código y ejecútelo.

2.  \#Display the results a chart that shows the top three countries
    with the highest ratio of positive cases to the number

3.  import matplotlib.pyplot as plt

top_countries.plot(x='Country', y='Positive Test Rate', kind='bar')

![A screenshot of a computer program Description automatically
generated](./media/image45.png)

4.  Pídale a su Github Copilot Chat que muestre los resultados en una
    gráfica que muestre los diez principales países con la mayor
    cantidad de casos positivos o abra un nuevo kernel de código y
    escriba # Display the results in a chart that shows the top ten
    countries with the most positive cases y presione Tab para aceptar
    el código y ejecútelo

5.  \#Display the results in a chart that shows the top ten countries
    with the most positive cases

6.  import matplotlib.pyplot as plt

7.  df_total_positive_cases.head(10).plot(x='Country', y='Total Positive
    Cases', kind='bar')

8.  plt.xlabel('Country')

9.  plt.ylabel('Total Positive Cases')

10. plt.title('Top Ten Countries with the Most Positive Cases')

plt.show()

![A screenshot of a computer screen Description automatically
generated](./media/image46.png)

11. Pídale a su Github Copilot Chat que muestre los resultados en una
    gráfica que muestre los diez principales países con la mayor
    cantidad de pruebas realizadas o abra un nuevo kernel de código y
    escriba # Display the results in a chart that shows the top ten
    countries with the most tests conducted y presione Tab para aceptar
    el código y ejecútelo

![A screenshot of a computer Description automatically
generated](./media/image47.png)

**Tarea 9: Conclusión**

1.  ¿Cuáles son sus conclusiones?

2.  ¿Cuáles son las limitaciones de este análisis?

3.  ¿Cuáles son los siguientes pasos que tomaría para mejorar este
    análisis?
