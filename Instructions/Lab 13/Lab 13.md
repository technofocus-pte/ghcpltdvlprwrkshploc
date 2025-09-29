**Laboratoire 13 : Créez une action JavaScript GitHub et automatisez des tâches personnalisées propres à votre flux de travail.**
  
**Objectifs:**

Imaginez que vous soyez chargé de créer une action GitHub personnalisée
pour automatiser des tâches spécifiques au sein de votre flux de
travail. Pour commencer, vous devez configurer un environnement de
développement pour l'écriture et le test de votre action JavaScript.
Cela implique l'initialisation d'un nouveau projet JavaScript, la
configuration de votre structure de projet et l'installation des
dépendances nécessaires. En suivant les étapes de cet atelier, vous
créerez une base solide pour développer votre action GitHub, ce qui vous
permettra de créer une automatisation adaptée aux besoins de votre
projet.

Dans cet atelier pratique, vous allez :

- **Cloner le dépôt** : Clonez le dépôt fourni sur votre machine locale
  pour démarrer votre processus de développement.

- **Accéder au dossier du projet** : Déplacez-vous dans le dossier du
  dépôt cloné où vous configurerez votre action.

- **Créer un dossier Action** : Créez un nouveau dossier dans le dépôt
  spécifiquement pour vos fichiers d’action.

- **Initialiser un projet npm** : Initialisez un nouveau projet npm dans
  le dossier de l’action afin de gérer les dépendances et la
  configuration.

- **Installer les dépendances** : Utilisez npm pour installer les
  dépendances nécessaires au développement de votre GitHub JavaScript
  Action.

- **Préparer le développement de l’action** : Configurez votre
  environnement de projet pour commencer à écrire et tester votre action
  GitHub JavaScript personnalisée.

Exercice : 1 Création d'un dépôt

1.  Naviguez jusqu'au lien suivant :
    https://github.com/skills/write-javascript-actions

Dans ce laboratoire, vous allez créer un dépôt à l'aide d'un modèle
public **skills-write-javascript-actions**

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image1.jpeg)

2.  Sélectionnez **Create a new repository** dans le **Use this
    template**.

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image2.jpeg)

3.  Entrez les détails suivants et sélectionnez **Create Repository.**

    - Repository name: **skills-write-javascript-actions**

    - Repository type: **Public**

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image3.jpeg)

Exercice \#2 : Initialiser un nouveau projet JavaScript

Une fois que vous avez installé les outils nécessaires localement,
suivez ces étapes pour commencer à créer votre première action.

1.  Sur la page d'accueil du dépôt **write-javascript-actions**, cliquez
    sur le bouton **Code** (de couleur verte) et copiez l'URL HTTPS sous
    l'onglet **Local**.

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image4.jpeg)

2.  Ouvrez maintenant **Command prompt** et clonez votre référentiel de
    compétences sur la machine locale :

git clone \<URL de ce dépôt \>.git

![Une capture d'écran d'un programme informatique Le contenu généré par
l'IA peut être incorrect.](./media/image5.jpeg)

**Remarque :** Habituellement, il est cloné sur le chemin suivant
« **C :\Users\Admin\skills-write-javascript-actions** »

3.  Accédez au dossier que vous venez de cloner :

cd C:\Users\Admin\skills-write-javascript-actions

![Une capture d'écran d'un programme informatique Le contenu généré par
l'IA peut être incorrect.](./media/image6.jpeg)

4.  Nous utiliserons la branche appelée main.

git switch main

![Une capture d'écran d'un programme informatique Le contenu généré par
l'IA peut être incorrect.](./media/image7.jpeg)

5.  Créez un nouveau dossier pour nos fichiers d'actions :

mkdir -p .github\actions\joke-action

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image8.jpeg)

6.  Accédez au dossier joke-action que vous venez de créer :

cd .github/actions/joke-action

![Une capture d'écran d'un programme informatique Le contenu généré par
l'IA peut être incorrect.](./media/image9.jpeg)

7.  Initialisez un nouveau projet :

npm init -y

![Une capture d'écran d'un programme informatique Le contenu généré par
l'IA peut être incorrect.](./media/image10.jpeg)

8.  Installez les dépendances request, request-promise et \\actions/core
    à l'aide de npm à partir du GitHub ToolKit
    (https://github.com/actions/toolkit) :

npm install -save request request-promise @actions/core

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image11.jpeg)

9.  Validez ces fichiers nouvellement ajoutés, nous supprimerons la
    nécessité de télécharger node_modules dans une étape ultérieure :

git add . && git commit -m « Ajouter des dépendances de projet »

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image12.jpeg)

**Remarque :** Si vous êtes invité à saisir l’adresse e-mail et le nom
d’utilisateur, saisissez la commande ci-dessous en remplaçant les
détails.

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image13.jpeg)

git config --global user.email « your_email@example.com »

git config --global user.name « Your Name »

**Remarque** : Remplacez par vos coordonnées.

10. Poussez vos modifications vers votre dépôt : entrez la commande
    ci-dessous et connectez-vous

git push

![Un écran d'ordinateur avec du texte blanc Le contenu généré par l'IA
peut être incorrect.](./media/image14.jpeg)

**Remarque :** Lorsque vous êtes invité à vous autoriser, connectez-vous
à votre compte GitHub et poursuivez le processus.

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image15.jpeg)

![Une capture d'écran d'un formulaire de connexion Le contenu généré par
l'IA peut être incorrect.](./media/image16.jpeg)

![Une capture d'écran d'une erreur informatique Le contenu généré par
l'IA peut être incorrect.](./media/image17.jpeg)

11. Attendez environ 20 secondes pendant que GitHub Actions actualise
    automatiquement la page pour poursuivre le traitement.

Résumé :

Vous avez désormais mis en place un environnement de développement
robuste pour créer et gérer votre GitHub JavaScript Action, établissant
ainsi les bases pour automatiser et améliorer vos workflows.
