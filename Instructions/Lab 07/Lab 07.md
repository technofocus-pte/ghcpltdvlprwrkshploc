**Laboratoire 07 : Codage avec GitHub Codespaces et Visual Studio Code**

Objectif:

Imaginez que vous êtes un développeur travaillant sur un projet qui
nécessite un environnement de développement hébergé dans le cloud pour
faciliter la collaboration et rationaliser votre flux de travail. Pour
améliorer votre productivité et gérer plus efficacement votre
configuration de développement, vous décidez d'utiliser GitHub
Codespaces avec Visual Studio Code. Cette configuration vous permet de
créer et de personnaliser des environnements de développement
directement dans le cloud, ce qui facilite la collaboration avec votre
équipe et la gestion efficace des configurations de projet.

Dans cet atelier pratique, vous allez :

- Démarrer un Codespace : créez et lancez un Codespace GitHub à l'aide
  de modèles prédéfinis.

- Personnaliser les configurations : personnalisez les configurations de
  votre projet dans le codespace pour répondre à vos besoins de
  développement.

- Gérer les codespaces : gérez et naviguez efficacement dans vos
  codespaces, garantissant un processus de développement fluide et
  organisé.

- Envoyer le code au référentiel : entraînez-vous à pousser vos
  modifications de code de l'espace de code vers le référentiel GitHub,
  renforçant ainsi votre capacité à intégrer le travail de développement
  au contrôle de version.

Exercice \#1 : Configurer un nouveau dépôt et lancer un codespace
GitHub)

1.  Connectez-vous à votre compte GitHub.

2.  Naviguez jusqu'au lien suivant :
    https://github.com/skills/code-with-codespaces

Dans cet atelier, vous allez créer le référentiel à l'aide d'un modèle
public « **skills-code-with-codespaces** ».

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image1.jpeg)

3.  Sélectionnez **Create a new repository** dans le menu **Use this
    template**.

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image2.jpeg)

4.  Entrez les détails suivants et sélectionnez **Create Repository**.

    - Nom du dépôt : **skills-code-with-codespaces**

    - Type de référentiel : **Public**

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image3.jpeg)

5.  Une fois le référentiel créé, cliquez sur le bouton **Code**.

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image4.jpeg)

6.  Sélectionnez l'onglet **Codespaces** dans la fenêtre contextuelle,
    puis cliquez sur le bouton **the Create codespace on main**.

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image5.jpeg)

**Remarque :** Le codespace s'ouvre dans un nouvel onglet du navigateur.

7.  Le navigateur affichera un éditeur Web VS Code et un terminal doit
    être présent comme indiqué ci-dessous.

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image6.jpeg)

8.  Attendez 2 minutes que le codespace (une machine virtuelle) se mette
    en marche.

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image7.jpeg)

9.  Revenez au référentiel **skills-code-with-codespaces** et cliquez
    sur le bouton **Code**

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image8.jpeg)

**Remarque :** si le codespace nouvellement créé ne se charge pas,
actualisez la page.

10. Cliquez sur les points de suspension **...** dans le codespace
    actif\*\*.\*\*

**Remarque** : Le nom de l'espace de code peut différer dans votre cas

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image9.jpeg)

11. Sélectionnez **Ouvrir dans Visual Studio Code** dans le menu
    contextuel.

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image10.jpeg)

12. Une fenêtre contextuelle vous demandera de confirmer l'ouverture du
    codespace dans l'application VS code. Sélectionnez **Open Visual
    Studio Code** pour ouvrir le codespace.

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image11.jpeg)

13. Vous serez invité à installer l'extension GitHub Codespaces, à
    cliquer sur **Install extension and open URI**.

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image12.jpeg)

14. Une fois installé, vous verrez une fenêtre contextuelle demandant
    des autorisations supplémentaires. **Click Authorize Visual Studio
    code**

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image13.jpeg)

15. Confirmez l'accès en saisissant le mot de passe de votre compte
    GitHub.

![Une capture d'écran d'un formulaire de connexion Le contenu généré par
l'IA peut être incorrect.](./media/image14.jpeg)

**Remarque :** Si vous voyez la fenêtre contextuelle Allow Windows
Firewall, veuillez autoriser la poursuite de la procédure.

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image15.jpeg)

Exercice \#2 : Envoyer du code vers votre référentiel à partir de
l'espace de code

1.  Dans l'espace de code de la fenêtre de l'explorateur VS Code,
    sélectionnez le fichier index.html.

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image16.jpeg)

2.  Remplacez l'en-tête h1 par ce qui suit :

\<h1\>Hello from the codespace!\</h1\>

3.  Enregistrez le fichier.

**Remarque :** Le fichier doit être enregistré automatiquement.

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image17.jpeg)

4.  Utilisez le terminal VS Code pour valider la modification du fichier
    en saisissant le message de validation suivant :

5.  git commit -a -m "Adding hello from the codespace!"

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image18.jpeg)

6.  Repoussez les modifications dans votre dépôt. À partir du terminal
    VS Code, entrez :

git push

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image19.jpeg)

7.  Le nouveau code de VS a été poussé vers votre dépôt !

8.  Revenez à la page d'accueil de votre dépôt et affichez les
    index.html pour vérifier que le nouveau code a été envoyé à votre
    dépôt.

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image20.jpeg)

9.  Attendez environ 20 secondes, puis actualisez ces actions GitHub
    pour passer automatiquement à l'étape suivante.

Résumé:

Vous avez maintenant utilisé GitHub Codespaces et Visual Studio Code
pour

- Créez et lancez un codespace GitHub à l'aide de modèles prédéfinis.

- Envoyer le code au référentiel : entraînez-vous à pousser vos
  modifications de code de l'espace de code vers le référentiel GitHub,
  renforçant ainsi votre capacité à intégrer le travail de développement
  au contrôle de version.
