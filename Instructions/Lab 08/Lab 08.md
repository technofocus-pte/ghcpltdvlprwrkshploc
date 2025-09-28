**Laboratoire 08 : Création d'une action GitHub et utilisation dans un
workflow**

Objectif:

Imaginez que vous faites partie d'une équipe de développement qui
souhaite rationaliser votre processus de développement de logiciels en
automatisant les tâches répétitives. Pour améliorer votre efficacité,
vous décidez d'utiliser GitHub Actions, qui vous permet d'automatiser
des tâches telles que les tests, le déploiement et les revues de code
directement dans votre dépôt GitHub. En configurant une action GitHub et
en l'intégrant à votre flux de travail, vous pouvez vous assurer que les
tâches essentielles sont effectuées automatiquement, ce qui vous fait
gagner du temps et réduit les efforts manuels.

Dans cet atelier pratique, vous allez :

- Configurez un fichier de flux de travail dans le répertoire
  .github/workflows, en définissant le contenu et en spécifiant les
  événements qui déclenchent le flux de travail.

- Entraînez-vous à ajouter et à valider des fichiers de flux de travail
  dans votre dépôt pour intégrer GitHub Actions dans votre processus de
  développement.

Exercice \#1 : Créer un dépôt à partir d'un modèle public

1.  Naviguez jusqu'au lien suivant :
    https://github.com/skills/hello-github-actions

Dans cet atelier, vous allez créer le référentiel à l'aide d'un modèle
public « **skills-hello-github-actions** ».

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image1.jpeg)

2.  Sélectionnez **Create a new repository** dans le menu **Use this
    template**.

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image1.jpeg)

3.  Entrez les détails suivants et sélectionnez **Create Repository**.

    - Nom du dépôt : **skills-hello-github-actions**

    - Type de référentiel : **Public**

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image2.jpeg)

Exercice \#2 : Créer un fichier de workflow

1.  Sur la page d'accueil du dépôt nouvellement créé, accédez à l'
    onglet **Pull requests**.

![Une capture d'écran d'une page web Le contenu généré par l'IA peut
être incorrect.](./media/image3.jpeg)

2.  Sur la page suivante, cliquez sur le bouton **New pull request**.

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image4.jpeg)

3.  Sur la page **Compare changes**, sélectionnez **base : main** et
    **compare: welcome-workflow** et cliquez sur **Create pull
    request.**

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image5.jpeg)

4.  Sur la page **Open a pull request**, cliquez sur **Create pull
    request**.

![Une capture d'écran d'une demande par e-mail Le contenu généré par
l'IA peut être incorrect.](./media/image6.jpeg)

5.  Accédez à l'onglet **Code**.

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image7.jpeg)

6.  Sur la page suivante, dans la **main branch dropdown**, cliquez sur
    la branche **welcome-workflow**.

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image8.jpeg)

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image9.jpeg)

7.  Une fois la branche principale remplacée par **welcome-workflow**,
    accédez au dossier **.github/workflows**, puis sélectionnez **Add
    file** et cliquez sur **Create new file**.

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image10.jpeg)

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image11.jpeg)

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image12.jpeg)

8.  Sur la page de création de fichier, entrez le nom du fichier
    welcome.yml

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image13.jpeg)

9.  Sur la page de l'éditeur, ajoutez le contenu suivant au fichier
    welcome.yml : et cliquez sur **Commit changes.**

10. name: Post welcome comment

11. on:

12. pull_request:

13. types: \[opened\]

14. permissions:

pull-requests: write

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image14.jpeg)

15. Sur la page **Commit changes**, cliquez sur **commit changes.**

16. Attendez 20 secondes pour que les actions s'exécutent, puis
    actualisez-les et une action fermera automatiquement cette étape.

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image15.jpeg)

Résumé:

Vous avez maintenant acquis une expérience pratique dans la
configuration et la gestion de GitHub Actions, améliorant ainsi votre
capacité à automatiser et à optimiser vos flux de travail de
développement de logiciels.
