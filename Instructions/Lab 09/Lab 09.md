**Laboratoire 09 : Création de flux de travail pour utiliser
l'intégration continue (CI) pour vos projets**

Objectifs:

Imaginez que vous travaillez sur un projet logiciel où le maintien de
normes de qualité élevées est crucial. Pour vous assurer que votre code
reste robuste et exempt d'erreurs, vous décidez d'implémenter
l'intégration continue (CI) à l'aide de GitHub Actions. L'intégration
continue permet d'automatiser le processus d'exécution des tests et de
vérification de la qualité du code chaque fois que des modifications
sont apportées à la base de code. En créant des flux de travail CI, vous
pouvez automatiquement créer des fichiers Markdown, exécuter des tests
et recevoir des commentaires immédiats sur la qualité du code,
garantissant ainsi que votre projet répond à ses normes de qualité de
manière cohérente.

Dans cet atelier pratique, vous allez :

- Créer un flux de travail de test : configurez un flux de travail
  GitHub Actions spécialement conçu pour linter les fichiers Markdown et
  vérifier les problèmes de formatage.

- Configurer et mettre à jour le flux de travail : entraînez-vous à
  configurer le fichier de flux de travail pour définir les tâches et
  les étapes nécessaires au linting automatisé, et mettez-le à jour si
  nécessaire pour améliorer ses fonctionnalités.

- Créer un Pull Request : intégrez les modifications en créant une
  demande de tirage, ce qui vous permet de tester le flux de travail CI
  et d'observer comment il automatise les contrôles qualité.

- Analysez les résultats du flux de travail CI pour comprendre comment
  il signale les problèmes et garantit la qualité du code.

Exercice \#1 : Créer un dépôt à partir d'un modèle public

1.  Naviguez jusqu'au lien suivant :
    https://github.com/skills/test-with-actions

Dans cet atelier, vous allez créer le référentiel à l'aide d'un modèle
public « **skills-test-with-actions** ».

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image1.jpeg)

2.  Sélectionnez **Create a new repository** dans le menu **Use this
    template**.

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image2.jpeg)

3.  Entrez les détails suivants et sélectionnez **Create Repository**.

    - Nom du référentiel : **skills-test-with-actions**

    - Type de référentiel : **Public**

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image3.jpeg)

Exercice \#2 : Ajouter un workflow de test

1.  Accédez à l'onglet Actions dans le référentiel créé il y a quelque
    temps.

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image4.jpeg)

2.  Sous Actions dans la barre latérale gauche, sélectionnez **New
    workflow**.

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image5.jpeg)

3.  Sur la page **Choose a workflow**, accédez à **"Simple workflow"**
    et cliquez sur **Configure**.

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image6.jpeg)

4.  Sur la page suivante, renommez votre flux de travail en ci.yml et
    mettez-le à jour en supprimant les deux dernières étapes.

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image7.jpeg)

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image8.jpeg)

5.  Ajoutez le code suivant à la fin du workflow et cliquez sur **Commit
    changes** en haut à droite .

6.  \- name : Run markdown lint

7.  Run : |

8.  npm install remark-cli remark-preset-lint-consistent

Remarque npx . --use remark-preset-lint-consistent

**Remarque :** Assurez-vous que l'extrait de code ajouté au flux de
travail est correctement mis en retrait

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image9.jpeg)

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image10.jpeg)

9.  Dans la fenêtre **Commit changes**, sélectionnez **Create a new
    branch for this commit and start a pull request**.

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image11.jpeg)

10. Une fois que **Create a new branch for this commit and start a pull
    request** est sélectionnée, la fenêtre **Commit changes** se
    transforme en **Propose Changes**. Cliquez maintenant sur **Propose
    changes**.

![Une capture d'écran d'un écran d'ordinateur Le contenu généré par l'IA
peut être incorrect.](./media/image12.jpeg)

11. Sur la page suivante de **Open a pull request**, cliquez sur
    **Create pull reques.**

![Une capture d'écran d'un e-mail Le contenu généré par l'IA peut être
incorrect.](./media/image13.jpeg)

12. Attendez 20 secondes, puis actualisez cette page pour analyser les
    résultats.

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image14.jpeg)

Résumé:

Vous avez maintenant acquis une expérience pratique des pratiques
d'intégration continue à l'aide de GitHub Actions, améliorant ainsi
votre capacité à automatiser et à maintenir des normes de qualité
élevées dans vos projets logiciels.
