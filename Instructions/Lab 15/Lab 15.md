**Laboratoire 15 : Activer CodeQL pour sécuriser votre code source**

Objectif:

Imaginez que vous êtes un développeur de logiciels travaillant sur un
projet critique pour votre entreprise, où la sécurité de votre
application est une priorité absolue. Face aux préoccupations
croissantes concernant les cybermenaces et les violations de données, il
est essentiel de s'assurer que votre code est exempt de vulnérabilités
et de pratiques de codage non sécurisées. Dans cet atelier pratique,
vous allez activer GitHub Code Scanning pour examiner automatiquement
votre code source à la recherche de problèmes de sécurité potentiels.

Dans cet atelier pratique, vous allez activer GitHub Code Scanning pour
examiner automatiquement votre code source à la recherche de problèmes
de sécurité potentiels.

Exercice \#1 : Créer un dépôt à partir d'un modèle public

1.  Connectez-vous à votre compte GitHub.

2.  Naviguez jusqu'au lien suivant :
    https://github.com/skills/introduction-to-codeql

Dans cet atelier, vous allez créer le référentiel à l'aide d'un modèle
public "**skills-introduction-to-codeql**".

![](./media/image1.jpeg)

3.  Sélectionnez **Create a new repository** dans le menu **Use this
    template**.

![](./media/image2.jpeg)

4.  Entrez les détails suivants et sélectionnez **Create Repository**.

    - Nom du dépôt :**skills-introduction-to-codeql**

    - Type de référentiel : **Public**

![](./media/image3.jpeg)

Exercice \#2 : Activer l'analyse de code avec CodeQL

1.  Sur la page d'accueil du référentiel nouvellement créé, accédez à
    l'onglet **Settings**.

![](./media/image4.jpeg)

2.  Dans la section **Security** de la barre latérale gauche,
    sélectionnez **Code security and analysis**.

![](./media/image5.jpeg)

3.  Faites défiler jusqu'à la section intitulée Analyse de code, cliquez
    sur le menu déroulant **Set-up**  et choisissez **Default**.

![](./media/image6.jpeg)

4.  Sélectionnez les options suivantes et cliquez sur **Enable CodeQL**

    - Langues à analyser : Ce sont les langues qui seront scannées par
      CodeQL. Dans ce cas, nous allons scanner en Python.

    - Suites de requêtes : les requêtes CodeQL sont regroupées dans des
      bundles appelés « suites ». Cette section vous permet de choisir
      la suite de requêtes à utiliser. Nous laisserons cet ensemble
      défini par défaut pour cet exercice.

    - Événements : Cette section indique à CodeQL quand effectuer une
      analyse. Dans ce cas, il est configuré pour analyser n'importe
      quelle demande de tirage vers la branche principale.

![](./media/image7.jpeg)

5.  Attendez environ 20 secondes, puis actualisez cette page pour
    continuer.

![](./media/image8.jpeg)

Résumé:

Vous avez maintenant activé GitHub Code Scanning pour examiner
automatiquement votre code source à la recherche de problèmes de
sécurité potentiels.
