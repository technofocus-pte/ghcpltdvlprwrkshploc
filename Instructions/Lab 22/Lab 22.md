**Laboratoire 22 - Créez un bloc-notes à l'aide du chat Github Copilot
et fournissez des réponses basées sur les données de test INTRODUCTION**

Ce jeu de données provient tested_worldwide.csv de Kaggle. Cet ensemble
de données, qui contient le nombre de tests effectués au fil du temps,
est important pour aider à donner un sens aux cas signalés
quotidiennement et à comprendre comment la COVID-19 se propage
réellement dans chaque pays.

**INSTRUCTIONS**

1.  Ouvrez Visual Studio Code à partir du menu Démarrer de Windows et
    ouvrez le dossier accédant à C :\Labfiles\CopilotHackathon

![Une capture d'écran d'un ordinateur Description générée
automatiquement](./media/image1.png)

2.  Cliquez sur le bouton **Yes,I Trust the Author**.

![BrokenImage](./media/image2.png)

3.  Cliquez sur l'icône **Copilot** dans le coin inférieur droit et
    sélectionnez **Github Copilot Chat.**

![BrokenImage](./media/image3.png)

4.  Tapez votre invite à créer un bloc-notes dans un projet. Utilisez la
    commande /newnotebook et nommez-la "COVID19 Worldwide Testing Data"

![BrokenImage](./media/image4.png)

5.  Vous pouvez voir les instructions du Copilot qui vous aident à
    obtenir des instructions. Suivez les étapes et créez le bloc-notes.

    - Open the command palette by pressing **Ctrl+Shift+P.**

    - Tapez Jupyter : Create New Blank Notebook et appuyez sur Entrée.

![BrokenImage](./media/image5.png)

- Un nouveau notebook sera créé. Enregistrez-le sous le nom
  COVID19WorldwideTesting Data.ipynb. Vous pouvez également demander à
  Copilot comment enregistrer un nouveau carnet.

![BrokenImage](./media/image6.png)

- Allez dans le dossier de destination - **excercisefiles- ?,** entrez
  le fichier COVID19WorldwideTesting Data.ipynb et enregistrez (save) le
  fichier.

![BrokenImage](./media/image7.png)

6.  Vous devez voir que le fichier a été créé dans le dossier
    **dataengineer**.

![Une capture d'écran d'un ordinateur Description générée
automatiquement](./media/image8.png)

7.  Utilisez Copilot et Copilot Chat pour développer l'exercice et
    soutenir votre apprentissage.

**EXERCICE**

Notre analyse tente d'apporter une réponse à cette question : **quels
sont les pays qui ont signalé le plus grand nombre de cas positifs par
rapport au nombre de tests effectués ?**

**Tâche 1 : Importer les bibliothèques requises**

1.  Cliquez sur Notebook kernel et tapez \#Import Required
    Libraries.Including Pandas et appuyez sur Entrée

![Une capture d'écran d'un ordinateur Description générée
automatiquement](./media/image9.png)

2.  Appuyez sur la touche d'arrêt. Il vous emmènera jusqu'au bout de la
    ligne. Appuyez sur Entrée, puis appuyez à nouveau sur Tab pour
    ajouter toutes les bibliothèques.

![Une capture d'écran d'un ordinateur Description générée
automatiquement](./media/image10.png)

\# Importez les bibliothèques nécessaires, y compris pandas.

\# Importer les bibliothèques requises

\# Ici, nous importons les bibliothèques nécessaires à notre tâche

import pandas as \# pandas est une bibliothèque logicielle écrite pour
le langage de programmation Python pour la manipulation et l'analyse de
données.

![Une capture d'écran d'un ordinateur Description générée
automatiquement](./media/image11.png)

**Tâche 2 : Charger le jeu de données**

1.  Utilisez pandas pour charger le fichier 'tested_worldwide.csv' à
    partir du niveau racine.

2.  Demandez à Github Copilot de vous aider à charger les données.
    Entrez Use pandas pour charger le fichier 'tested_worldwide.csv' à
    partir du niveau racine

![BrokenImage](./media/image12.png)

3.  Entrez le code ci-dessous dans un bloc-notes et exécutez-le. Il vous
    demandera de sélectionner **Python Environment**. Sélectionnez-le.

![BrokenImage](./media/image13.png)

4.  Sélectionnez l'environnement recommandé. script s'exécute et fournit
    les résultats.

![BrokenImage](./media/image14.png)

![Une capture d'écran d'un ordinateur Description générée
automatiquement](./media/image15.png)

Tâche 3 : Comprendre les données

1.  Utilisez la fonction head() pour afficher les 5 premières lignes du
    jeu de données

2.  Demandez à votre Github Copilot de vous aider avec le code pour
    afficher les 5 premières lignes du jeu de données. Afficher les 5
    premières lignes du jeu de données

![BrokenImage](./media/image16.png)

3.  Cliquez sur **+ code** pour ouvrir le nouveau kerner. Entrez
    simplement \# afficher les 5 premières lignes de l'ensemble de
    données. Il prédira automatiquement votre question. Il suffit
    d'appuyer sur tag, puis sur Entrée.

![Captures d'écran d'un écran d'ordinateur Description générée
automatiquement](./media/image17.png)

4.  **Copilot** prédit la commande que vous recherchez, alors appuyez
    sur la touche pour accepter le code. Vous avez toujours la
    possibilité d'éditer/écrire votre propre code.

![BrokenImage](./media/image18.png)

5.  Appuyez sur l'onglet et acceptez le code. Exécutez Kernel.

![BrokenImage](./media/image19.png)

6.  Vous devriez voir les résultats.

![Une capture d'écran d'un écran d'ordinateur Description générée
automatiquement](./media/image20.png)

![Une capture d'écran d'un ordinateur Description générée
automatiquement](./media/image21.png)

7.  Demandez à votre copilote de vous aider à afficher le nombre de
    lignes et de colonnes dans le dataframe. Cliquez sur +code .entrez
    le code puis lancez le noyau. Vous pouvez également utiliser le code
    ci-dessous

8.  num_rows, num_cols = data.shape

9.  print("Number of rows:", num_rows)

print("Number of columns:", num_cols)

![BrokenImage](./media/image22.png)

10. Demandez à votre Copilot de vous aider avec cela Affichez les types
    de données de chaque colonne. Vous pouvez également utiliser
    data.dttypes

![Une capture d'écran d'un ordinateur Description générée
automatiquement](./media/image23.png)

11. Demandez à votre copilote GitHub de fournir du code pour Afficher le
    nombre de valeurs manquantes dans chaque colonne.

![Une capture d'écran d'un ordinateur Description générée
automatiquement](./media/image24.png)

12. Ajoutez un nouveau noyau et ajoutez le code ci-dessous et
    exécutez-le. Vous pouvez également utiliser le code suggéré par
    Copilot et vérifier

13. missing_values = df.isnull().sum()

print(missing_values)

![Une capture d'écran d'un programme d'ordinateur Description générée
automatiquement](./media/image25.png)

14. Exécutez le code ci-dessous dans le nouveau noyau pour afficher le
    nombre de valeurs uniques dans chaque colonne. Vérifiez auprès de
    votre copilote le code et les résultats.

15. unique_values = df.nunique()

print(unique_values)

![Une capture d'écran d'un ordinateur Description générée
automatiquement](./media/image26.png)

**Tâche 4 : Nettoyage des données**

1.  Exécutez le code ci-dessous pour supprimer les colonnes qui ne sont
    pas nécessaires à l'analyse. Demandez le code à votre copilote et
    vérifiez les résultats.

data = df\[\['Country_Region', 'positive', 'total_tested'\]\]![Une
capture d'écran d'un ordinateur Description générée
automatiquement](./media/image27.png)

2.  Tapez \#Rename les colonnes pour les rendre plus lisibles Dans un
    nouveau kernel et acceptez le code.

![Une capture d'écran d'un ordinateur Description générée
automatiquement](./media/image28.png)

3.  Vous pouvez utiliser le code ci-dessous et l'exécuter.

df.rename(columns={'Country_Region': 'Country', 'positive': 'Positive
Cases', 'total_tested': 'Total Tested'}, inplace=True)![Une capture
d'écran d'un ordinateur Description générée
automatiquement](./media/image29.png)

4.  Demandez à votre copilote de supprimer les lignes qui ont des
    valeurs manquantes et d'exécuter le code dans un nouveau noyau ou de
    taper \#Drop lignes qui ont des valeurs manquantes Dans le nouveau
    noyau, appuyez sur Entrée. Appuyez sur l'onglet et acceptez le code

![Une capture d'écran d'un ordinateur Description générée
automatiquement](./media/image30.png)

5.  Ajoutez un nouveau noyau +Code et tapez \#Convert types de données
    des colonnes aux types appropriés, appuyez sur **tag** pour accepter
    le code, entrez à nouveau et appuyez sur Tab. Générez du code pour
    les cas positifs, le nombre total de tests et le pays, puis
    exécutez-le.

![Une capture d'écran d'un ordinateur Description générée
automatiquement](./media/image31.png)

6.  Ajoutez un nouveau noyau +Code et tapez \#Display le nombre de
    valeurs manquantes dans chaque colonne, puis appuyez sur Entrée.
    Appuyez sur la touche de tabulation et acceptez le code. Vous pouvez
    également demander dans le chat GitHub Copilot

![Une capture d'écran d'un programme d'ordinateur Description générée
automatiquement](./media/image32.png)

![Une capture d'écran d'un écran d'ordinateur Description générée
automatiquement](./media/image33.png)

**Tâche 5 : Extraire les dix premiers pays avec le plus de cas de
Covid-19.**

1.  Demandez à votre chat Copilot de vous aider avec le code Créez une
    nouvelle trame de données qui contient le nombre total de cas
    positifs pour chaque pays Ou ouvrez un nouveau code et tapez
    \#Create une nouvelle trame de données qui contient le nombre total
    de cas positifs pour chaque pays et appuyez sur Etner. Appuyez sur
    la touche pour accéder au code.

![Une capture d'écran d'un ordinateur Description générée
automatiquement](./media/image34.png)

2.  Dans un nouveau code, entrez les invites ci-dessous et entrez après
    chaque invite pour accepter le code et l'exécuter.

3.  \# Group the data by 'Country' and calculate the sum of 'Positive
    Cases'

4.  total_positive_cases = data.groupby('Country')\['Positive
    Cases'\].sum()

5.  \# Create a new dataframe with the total positive cases for each
    country

6.  df_total_positive_cases = pd.DataFrame({'Country':
    total_positive_cases.index, 'Total Positive Cases':
    total_positive_cases.values})

7.  

8.  \# Display the new dataframe

df_total_positive_cases

![Une capture d'écran d'un écran d'ordinateur Description générée
automatiquement](./media/image35.png)

9.  Demandez à Copilot de trier la trame de données par ordre
    décroissant du nombre total de cas positifs Ou tapez \# Trier la
    trame de données par ordre décroissant du nombre total de cas
    positifs Dans le nouveau noyau de code, appuyez sur tag pour
    accepter le code et l'exécuter.

![Une capture d'écran d'un ordinateur Description générée
automatiquement](./media/image36.png)

10. Demandez à votre chat Github Copilot de vous aider à afficher les
    dix premiers pays avec le plus de cas positifs Ou tapez \# Display
    les dix premiers pays avec le plus de cas positifs dans le nouveau
    noyau de code et exécutez-le. N'oubliez pas que vous avez juste
    besoin d'afficher.

![Une capture d'écran d'un ordinateur Description générée
automatiquement](./media/image37.png)

**Tâche 6 : Identifier le nombre de cas positifs les plus élevés par
rapport aux cas testés**

1.  Demandez à votre GitHub Copilot Chat de vous aider pour créez une
    nouvelle trame de données (Create a new dataframe) qui contient le
    nombre total de tests effectués pour chaque pays ou ouvrez le
    nouveau noyau de code et tapez \# Create a new dataframe qui
    contient le nombre total de tests effectués pour chaque pays et
    appuyez sur la touche de tabulation pour accéder au code. Vous
    pouvez modifier le code si nécessaire et l'exécuter.

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

![Une capture d'écran d'un ordinateur Description générée
automatiquement](./media/image38.png)

9.  Demandez à votre Github Copilot Chat Triez le dataframe par ordre
    décroissant du nombre total de tests effectués Ou ouvrez un nouveau
    noyau de code ,tapez \# Trier le dataframe par ordre décroissant du
    nombre total de tests effectués Et appuyez sur tab pour caccep le
    code et exécutez-le.

![Une capture d'écran d'un programme d'ordinateur Description générée
automatiquement](./media/image39.png)

10. Demandez à votre chat Github Copilot Affichez les dix premiers pays
    avec le plus de tests effectués Ou ouvrez un nouveau noyau de code,
    tapez \# Affichez les dix premiers pays avec le plus de tests
    effectués Et appuyez sur tab pour caccep le code et exécutez-le.

![Une capture d'écran d'un programme d'ordinateur Description générée
automatiquement](./media/image40.png)

**Tâche 7 : Identifier les trois premiers pays ayant eu le plus grand
nombre de cas positifs par rapport au nombre de tests effectués**

1.  Demandez à votre chat Github Copilot Fusionnez les deux dataframes
    créés dans les étapes précédentes Ou ouvrez un nouveau code kernel
    et tapez \# Display les dix premiers pays avec le plus de tests
    effectués Et appuyez sur tab pour cacceper le code et l'exécuter.

![Une capture d'écran d'un ordinateur Description générée
automatiquement](./media/image41.png)

2.  Demandez à votre chat Github Copilot Créez une nouvelle colonne qui
    contient le rapport entre les cas positifs et le nombre de tests
    effectués Ou ouvrez un nouveau noyau de code et tapez \# Create une
    nouvelle colonne qui contient le rapport entre les cas positifs et
    le nombre de tests effectués Et appuyez sur la touche de tabulation
    pour accepter le code et l'exécuter.

![Une capture d'écran d'un ordinateur Description générée
automatiquement](./media/image42.png)

3.  Demandez à votre Github Copilot Chat Triez la dataframe par ordre
    décroissant du rapport entre les cas positifs et le nombre de tests
    effectués Ou ouvrez un nouveau noyau de code et tapez \# Triez la
    dataframe par ordre décroissant du rapport entre les cas positifs et
    le nombre de tests effectués Et appuyez sur l'onglet pour accepter
    le code et l'exécuter.

![Une capture d'écran d'un ordinateur Description générée
automatiquement](./media/image43.png)

4.  Demandez à votre chat Github Copilot Affichez les trois premiers
    pays avec le plus grand ratio de cas positifs par rapport au nombre
    de tests effectués Ou ouvrez un nouveau noyau de code et tapez
    \#Display les trois premiers pays avec le rapport le plus élevé de
    cas positifs par rapport au nombre de tests effectués Et appuyez sur
    l'onglet pour accepter le code et l'exécuter

5.  \#Display les trois premiers pays ayant le plus grand ratio de cas
    positifs par rapport au nombre de tests effectués

6.  top_countries = merged_df.nlargest(3, 'Positive Test Rate')

top_countries\[\['Country', 'Positive Test Rate'\]\]

![Une capture d'écran d'un ordinateur Description générée
automatiquement](./media/image44.png)

**Tâche 8 : Affichage des résultats**

1.  Demandez à votre chat Github Copilot d'afficher les résultats un
    graphique qui montre les trois premiers pays avec le rapport le plus
    élevé de cas positifs par rapport au nombre Ou ouvrez un nouveau
    noyau de code et tapez \# Affichez les résultats un graphique qui
    montre les trois premiers pays avec le rapport le plus élevé de cas
    positifs par rapport au nombre Et appuyez sur l'onglet pour accepter
    le code et l'exécuter

2.  \#Display les résultats un graphique qui montre les trois pays ayant
    le ratio le plus élevé de cas positifs par rapport au nombre

3.  import matplotlib.pyplot as plt

top_countries.plot(x='Country', y='Positive Test Rate', kind='bar')

![Une capture d'écran d'un programme d'ordinateur Description générée
automatiquement](./media/image45.png)

4.  Demandez à votre chat Github Copilot d'afficher les résultats dans
    un graphique qui montre les dix premiers pays avec le plus de cas
    positifs Ou ouvrez un nouveau noyau de code et tapez \# Display les
    résultats dans un graphique qui montre les dix premiers pays avec le
    plus de cas positifs Et appuyez sur l'onglet pour accepter le code
    et l'exécuter

5.  \#Display the results in a chart that shows the top ten countries
    with the most positive cases

6.  import matplotlib.pyplot as plt

7.  df_total_positive_cases.head(10).plot(x='Country', y='Total Positive
    Cases', kind='bar')

8.  plt.xlabel('Country')

9.  plt.ylabel('Total Positive Cases')

10. plt.title('Top Ten Countries with the Most Positive Cases')

plt.show()

![Une capture d'écran d'un écran d'ordinateur Description générée
automatiquement](./media/image46.png)

11. Demandez à votre chat Github Copilot d'afficher les résultats dans
    un graphique qui montre les dix premiers pays avec le plus de tests
    effectués Ou ouvrez un nouveau noyau de code et tapez \# Display les
    résultats dans un graphique qui montre les dix premiers pays avec le
    plus de tests effectués Et appuyez sur l'onglet pour accepter le
    code et l'exécuter

![Une capture d'écran d'un ordinateur Description générée
automatiquement](./media/image47.png)

**Task 9: Conclusion**

1.  Quelles sont vos conclusions ?

2.  Quelles sont les limites de cette analyse ?

3.  Quelles sont les prochaines étapes que vous prendriez pour améliorer
    cette analyse ?
