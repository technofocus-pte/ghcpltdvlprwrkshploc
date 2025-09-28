**Lab 22 - Erstellen eines Notebooks mit dem Github Copilot-Chat und
Bereitstellen von Antworten auf der Grundlage von Testdaten EINFÜHRUNG**

Dieser Datensatz tested_worldwide.csv stammt aus Kaggle. Dieser
Datensatz, der die Anzahl der im Laufe der Zeit durchgeführten Tests
enthält, ist wichtig, um die täglich gemeldeten Fälle zu verstehen und
zu verstehen, wie sich COVID-19 in den einzelnen Ländern wirklich
ausbreitet.

**ANWEISUNGEN**

1.  Öffnen Sie Visual Studio Code über das Windows-Startmenü, und öffnen
    Sie den Ordner, indem Sie zu C:\Labfiles\CopilotHackathon
    navigieren.

![Ein Screenshot eines Computers Beschreibung wird automatisch
generiert](./media/image1.png)

2.  Klicken Sie auf die Taste **Yes, I Trust the Author**.

![Defektes Bild](./media/image2.png)

3.  Klicken Sie auf das **Copilot**-Symbol in der rechten Ecke und
    wählen Sie **Github Copilot Chat**.

![Defektes Bild](./media/image3.png)

4.  Geben Sie Ihre Prompt

> Create a new notebook in a project. Use command /newnotebook and name
> it as "COVID19 Worldwide Testing Data"

![Defektes Bild](./media/image4.png)

5.  Sie können die Copilot-Anweisungen sehen, die Ihnen bei Anweisungen
    helfen. Führen Sie die Schritte aus, und erstellen Sie das Notebook.

    - Öffnen Sie die Befehlspalette, indem Sie **Ctrl+Shift+P** drücken.

    - Geben Sie “Jupyter: Create New Blank Notebook” ein, und drücken
      Sie die Eingabetaste.

![Defektes Bild](./media/image5.png)

- Ein neues Notizbuch wird erstellt. Speichern Sie es unter dem Namen
  COVID19WorldwideTesting Data.ipynb.Sie können Copilot auch fragen, wie
  ein neues Notebook gespeichert wird.

![Defektes Bild](./media/image6.png)

- Wechseln Sie in den Zielordner - **excercisefiles-? dataengineer,**
  geben Sie den Dateiname COVID19WorldwideTesting Data.ipynb ein und
  speichern Sie die Datei.

![Defektes Bild](./media/image7.png)

6.  Sie sollten sehen, dass die Datei im Ordner **dataengineer**
    erstellt wurde .

![Ein Screenshot eines Computers Beschreibung wird automatisch
generiert](./media/image8.png)

7.  Verwenden Sie Copilot und Copilot Chat, um die Übung zu entwickeln
    und Ihr Lernen zu unterstützen.

**ÜBUNG**

Unsere Analyse versucht, eine Antwort auf diese Frage zu geben: **Welche
Länder haben im Verhältnis zur Anzahl der durchgeführten Tests die
höchste Anzahl positiver Fälle gemeldet?**

**Aufgabe 1: Importieren der erforderlichen Bibliotheken**

1.  Klicken Sie auf Notebook-Kernel und geben Sie \#Import Required
    Libraries.Including Pandas ein und drücken Sie die Eingabetaste

![Ein Screenshot eines Computers Beschreibung wird automatisch
generiert](./media/image9.png)

2.  Drücken Sie die Tabulatortaste. Es bringt Sie bis zum Ende der
    Linie. Drücken Sie die Eingabetaste und erneut die Tabulatortaste,
    um alle Bibliotheken hinzuzufügen.

![Ein Screenshot eines Computers Beschreibung wird automatisch
generiert](./media/image10.png)

\# Import the necessary libraries, including pandas.

\# Import Required Libraries

\# Here we are importing the necessary libraries for our task

import pandas as pd \# pandas ist eine Softwarebibliothek, die für die
Programmiersprache Python zur Datenmanipulation und -analyse geschrieben
wurde.

![Ein Screenshot eines Computers Beschreibung wird automatisch
generiert](./media/image11.png)

**Aufgabe 2: Laden des Datasets**

1.  Verwenden Sie Pandas, um die 'tested_worldwide.csv'-Datei von der
    Root-Ebene zu laden.

2.  Bitten Sie Github Copilot um Hilfe beim Laden von Daten. Geben Sie
    ein: Use pandas to load the 'tested_worldwide.csv' file from the
    root level.

![Defektes Bild](./media/image12.png)

3.  Geben Sie den folgenden Code in ein Notebook ein, und führen Sie ihn
    aus. Sie werden aufgefordert, **Python Environment** auszuwählen.
    Wählen Sie es aus.

![Defektes Bild](./media/image13.png)

4.  Wählen Sie die empfohlene Umgebung aus. Das Skript wird ausgeführt
    und stellt die Ergebnisse bereit.

![Defektes Bild](./media/image14.png)

![Ein Screenshot eines Computers Beschreibung wird automatisch
generiert](./media/image15.png)

Aufgabe 3 : Verstehen der Daten

1.  Verwenden Sie die Funktion head(), um die ersten 5 Zeilen des
    Datensatzes anzuzeigen

2.  Bitten Sie Ihren Github Copilot, Ihnen mit dem Code zur Anzeige der
    ersten 5 Zeilen des Datensatzes zu helfen.

> display first 5 rows of the dataset ![Defektes
> Bild](./media/image16.png)

3.  Klicken Sie auf **+ Code**, um den neuen Kerner zu öffnen. Geben Sie
    einfach “# display first 5 rows of dataset” ein. Ihre Frage wird
    automatisch vorhergesagt. Drücken Sie einfach Tag und dann die
    Eingabetaste.

![Bildschirme Screenshot eines Computerbildschirms Beschreibung
automatisch generiert](./media/image17.png)

4.  **Copilot** sagt den Befehl voraus, den Sie suchen, also drücken Sie
    die Tabulatortaste, um den Code zu übernehmen. Sie haben immer die
    Möglichkeit, Ihren eigenen Code zu bearbeiten/zu schreiben.

![Defektes Bild](./media/image18.png)

5.  Drücken Sie die Tabulatortaste und akzeptieren Sie den Code. Führen
    Sie den Kernel aus.

![Defektes Bild](./media/image19.png)

6.  Die Ergebnisse sollten angezeigt werden.

![Ein Screenshot eines Computerbildschirms Beschreibung wird automatisch
generiert](./media/image20.png)

![Ein Screenshot eines Computers Beschreibung wird automatisch
generiert](./media/image21.png)

7.  Bitten Sie Ihren Copilot um Hilfe bei der Anzeige der Anzahl der
    Zeilen und Spalten im Datenrahmen. Klicken Sie auf +code.Geben Sie
    den Code ein und führen Sie dann den Kernel aus. Sie können auch den
    folgenden Code verwenden

8.  num_rows, num_cols = data.shape

9.  print("Number of rows:", num_rows)

print("Number of columns:", num_cols)

![Defektes Bild](./media/image22.png)

10. Bitten Sie Ihren Copilot, Ihnen dabei zu helfen: Zeigen Sie die
    Datentypen der einzelnen Spalten an. Sie können auch
    **data.dttypes** verwenden

![Ein Screenshot eines Computers Beschreibung wird automatisch
generiert](./media/image23.png)

11. Bitten Sie Ihren GitHub Copilot, Code für die Anzeige der Anzahl
    fehlender Werte in jeder Spalte bereitzustellen.

![Ein Screenshot eines Computers Beschreibung wird automatisch
generiert](./media/image24.png)

12. Fügen Sie einen neuen Kernel hinzu, fügen Sie den folgenden Code
    hinzu und führen Sie ihn aus. Sie können auch den von Copilot
    vorgeschlagenen Code verwenden und überprüfen.

13. missing_values = df.isnull().sum()

print(missing_values)

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image25.png)

14. Führen Sie den folgenden Code im neuen Kernel aus, um die Anzahl der
    eindeutigen Werte in jeder Spalte anzuzeigen. Erkundigen Sie sich
    bei Ihrem Copilot nach Code und Ergebnissen.

15. unique_values = df.nunique()

> print(unique_values)![Ein Screenshot eines Computers Beschreibung wird
> automatisch generiert](./media/image26.png)

**Aufgabe 4: Datenbereinigung**

1.  Führen Sie den folgenden Code aus, um die Spalten zu löschen, die
    für die Analyse nicht benötigt werden. Fragen Sie Ihren Copilot nach
    dem Code und überprüfen Sie die Ergebnisse.

data = df\[\['Country_Region', 'positive', 'total_tested'\]\]

![Ein Screenshot eines Computers Beschreibung wird automatisch
generiert](./media/image27.png)

2.  Geben Sie ein: \#Rename the columns to make them more readable In a
    new kernel and accept the code.

![Ein Screenshot eines Computers Beschreibung wird automatisch
generiert](./media/image28.png)

3.  Sie können den folgenden Code verwenden und ausführen.

df.rename(columns={'Country_Region': 'Country', 'positive': 'Positive
Cases', 'total_tested': 'Total Tested'}, inplace=True)

![Ein Screenshot eines Computers Beschreibung wird automatisch
generiert](./media/image29.png)

4.  Bitten Sie Ihren Copilot, die Zeilen mit fehlenden Werten zu löschen
    und den Code in einem neuen Kernel auszuführen oder geben Sie ein:
    \#Drop the rows that have missing values. Im neuen Kernel drücken
    Sie die Eingabetaste. Drücken Sie die Tabulatortaste und akzeptieren
    Sie den Code

![Ein Screenshot eines Computers Beschreibung wird automatisch
generiert](./media/image30.png)

5.  Fügen Sie einen neuen +Code-Kernel hinzu, und geben Sie ein:
    \##Convert the data types of the columns to the appropriate types,
    drücken Sie **Tab**, um den Code zu akzeptieren, dann erneut Enter
    und nochmals Tab. Generieren Sie den Code für **Positive cases,
    Total Tested und Country** und führen Sie ihn aus.

![Ein Screenshot eines Computers Beschreibung wird automatisch
generiert](./media/image31.png)

6.  Fügen Sie einen neuen +Code-Kernel hinzu und geben Sie ein:
    \#Display the number of missing values in each column und drücken
    Sie die Eingabetaste. Drücken Sie die Tabulatortaste und akzeptieren
    Sie den Code. Sie können auch im GitHub Copilot-Chat fragen.

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image32.png)

![Ein Screenshot eines Computerbildschirms Beschreibung wird automatisch
generiert](./media/image33.png)

**Aufgabe 5 : Extraktion der zehn Länder mit den meisten
Covid-19-Fällen.**

1.  Bitten Sie Ihren Copilot-Chat, Ihnen beim Code zu helfen Erstellen
    Sie einen neuen Datenrahmen, der die Gesamtzahl der positiven Fälle
    für jedes Land enthält. Oder öffnen Sie einen neuen Code, geben Sie
    ein: \# Create a new dataframe that contains the total number of
    positive cases for each country und drücken Sie Enter. Drücken Sie
    die Tabulatortaste, um den Code zu bestätigen.

![Ein Screenshot eines Computers Beschreibung wird automatisch
generiert](./media/image34.png)

2.  Geben Sie in einem neuen Code die folgenden Prompts ein, und geben
    Sie nach jeder Prompt ein, um den Code zu akzeptieren und
    auszuführen.

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

![Ein Screenshot eines Computerbildschirms Beschreibung wird automatisch
generiert](./media/image35.png)

8.  Bitten Sie Copilot, den Datenrahmen in absteigender Reihenfolge der
    Gesamtzahl der positiven Fälle zu sortieren Oder geben Sie ein: \#
    \# Sort the dataframe in descending order of the total number of
    positive cases. Im neuen Code-Kernel drücken Sie Tag, um den Code zu
    akzeptieren und auszuführen.

![Ein Screenshot eines Computers Beschreibung wird automatisch
generiert](./media/image36.png)

9.  Bitten Sie GitHub Copilot Chat, Ihnen dabei zu helfen, die Top Ten
    Länder mit den meisten positiven Fällen anzuzeigen. Oder geben Sie
    in einem neuen Code-Kernel ein: \# \# Display the top ten countries
    with the most positive cases und führen Sie ihn aus. Denken Sie
    daran: Es soll nur die Anzeige erfolgen.

![Ein Screenshot eines Computers Beschreibung wird automatisch
generiert](./media/image37.png)

**Aufgabe 6 : Identifizierung der höchsten positiven Ergebnisse im
Vergleich zu getesteten Fällen**

1.  Bitten Sie Ihren GitHub Copilot Chat, Ihnen dabei zu helfen ein
    neues DataFrame zu erstellen, das die Gesamtzahl der durchgeführten
    Tests pro Land enthält. Oder öffnen Sie einen neuen Code-Kernel und
    geben Sie ein: \# Create a new dataframe that contains the total
    number of tests conducted for each country und drücken Sie die
    Tabulatortaste, um den Code zu akzeptieren. Sie können den Code bei
    Bedarf bearbeiten und anschließend ausführen.

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

![Ein Screenshot eines Computers Beschreibung wird automatisch
generiert](./media/image38.png)

9.  Fragen Sie Ihren Github Copilot Chat. Sortieren Sie den Datenrahmen
    in absteigender Reihenfolge der Gesamtzahl der durchgeführten Tests
    Oder öffnen Sie einen neuen Code-Kernel, geben Sie ein: \# Sort the
    dataframe in descending order of the total number of tests conducted
    und drücken Sie die Tabulatortaste, um den Code zu akzeptieren und
    auszuführen.

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image39.png)

10. Fragen Sie Ihren Github Copilot Chat Zeigen Sie die Top Ten Länder
    mit den meisten durchgeführten Tests an Oder öffnen Sie einen neuen
    Code-Kernel, geben Sie ein: \# Display the top ten countries with
    the most tests conducted und drücken Sie die Tabulatortaste, um den
    Code zu akzeptieren und auszuführen.

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image40.png)

**Aufgabe 7 : Identifizierung der drei Länder mit den meisten positiven
Fällen im Vergleich zur Anzahl der durchgeführten Tests**

1.  Fragen Sie Ihren Github Copilot Chat. Führen Sie die beiden in den
    vorherigen Schritten erstellten Datenrahmen zusammen Oder öffnen Sie
    einen neuen Code-Kernel und geben Sie ein: \# Display the top ten
    countries with the most tests conducted und drücken Sie die
    Tabulatortaste, um den Code zu akzeptieren und auszuführen.

![Ein Screenshot eines Computers Beschreibung wird automatisch
generiert](./media/image41.png)

2.  Fragen Sie Ihren Github Copilot Chat. Erstellen Sie eine neue
    Spalte, die das Verhältnis der positiven Fälle zur Anzahl der
    durchgeführten Tests enthält Oder öffnen Sie einen neuen Code-Kernel
    und geben Sie ein: \# Create a new column that contains the ratio of
    positive cases to the number of tests conducted und drücken Sie die
    Tabulatortaste, um den Code zu akzeptieren und auszuführen.

![Ein Screenshot eines Computers Beschreibung wird automatisch
generiert](./media/image42.png)

3.  Fragen Sie Ihren Github Copilot Chat.Sortieren Sie den Datenrahmen
    in absteigender Reihenfolge des Verhältnisses positiver Fälle zur
    Anzahl der durchgeführten Tests Oder öffnen Sie einen neuen
    Code-Kernel und geben Sie ein: \# Sort the dataframe in descending
    order of the ratio of positive cases to the number of tests
    conducted und drücken Sie die Tabulatortaste, um den Code zu
    akzeptieren und auszuführen.

![Ein Screenshot eines Computers Beschreibung wird automatisch
generiert](./media/image43.png)

4.  Fragen Sie Ihren Github Copilot Chat. Zeigen Sie die drei Länder mit
    dem höchsten Verhältnis positiver Fälle zur Anzahl der
    durchgeführten Tests an Oder öffnen Sie einen neuen Code-Kernel und
    geben Sie ein: \#Display the top three countries with the highest
    ratio of positive cases to the number of tests conducted und drücken
    Sie die Tabulatortaste, um den Code zu akzeptieren und auszuführen.

5.  \#Display the top three countries with the highest ratio of positive
    cases to the number of tests conducted

6.  top_countries = merged_df.nlargest(3, 'Positive Test Rate')

top_countries\[\['Country', 'Positive Test Rate'\]\]

![Ein Screenshot eines Computers Beschreibung wird automatisch
generiert](./media/image44.png)

**Aufgabe 8 : Anzeigen der Ergebnisse**

1.  Bitten Sie Ihren Github Copilot Chat, die Ergebnisse in einem
    Diagramm darzustellen, das die Top drei Länder mit dem höchsten
    Verhältnis von positiven Fällen zur Anzahl der Tests zeigt Oder
    öffnen Sie einen neuen Code-Kernel und geben Sie ein: \# Display the
    results a chart that shows the top three countries with the highest
    ratio of positive cases to the number und drücken Sie die
    Tabulatortaste, um den Code zu akzeptieren und auszuführen.

2.  \#Display the results a chart that shows the top three countries
    with the highest ratio of positive cases to the number

3.  import matplotlib.pyplot as plt

top_countries.plot(x='Country', y='Positive Test Rate', kind='bar')

![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
generiert](./media/image45.png)

4.  Bitten Sie GitHub Copilot Chat, die Ergebnisse in einem Diagramm
    darzustellen, das die Top Ten Länder mit den meisten positiven
    Fällen zeigt. Oder öffnen Sie einen neuen Code-Kernel und geben Sie
    ein: \#Display the results in a chart that shows the top ten
    countries with the most positive cases und drücken Sie die
    Tabulatortaste, um den Code zu akzeptieren und auszuführen.

5.  \#Display the results in a chart that shows the top ten countries
    with the most positive cases

6.  import matplotlib.pyplot as plt

7.  df_total_positive_cases.head(10).plot(x='Country', y='Total Positive
    Cases', kind='bar')

8.  plt.xlabel('Country')

9.  plt.ylabel('Total Positive Cases')

10. plt.title('Top Ten Countries with the Most Positive Cases')

plt.show()

![Ein Screenshot eines Computerbildschirms Beschreibung wird automatisch
generiert](./media/image46.png)

11. Bitten Sie Ihren Github Copilot Chat, die Ergebnisse in einem
    Diagramm darzustellen, das die Top Ten Länder mit den meisten
    durchgeführten Tests zeigt. Oder öffnen Sie einen neuen Code-Kernel
    und geben Sie ein: \# Display the results in a chart that shows the
    top ten countries with the most tests conducted Und drücken Sie die
    Tabulatortaste, um den Code zu akzeptieren und auszuführen

![Ein Screenshot eines Computers Beschreibung wird automatisch
generiert](./media/image47.png)

**Aufgabe 9: Schlussfolgerung**

1.  Was sind Ihre Schlussfolgerungen?

2.  Was sind die Grenzen dieser Analyse?

3.  Was sind die nächsten Schritte, die Sie unternehmen würden, um diese
    Analyse zu verbessern?

