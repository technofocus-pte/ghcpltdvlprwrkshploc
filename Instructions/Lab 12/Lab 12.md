**Laboratoire 12 : Création de workflows de déploiement à l'aide de
GitHub Actions et de Microsoft Azure**

Objectifs:

Imaginez que vous gériez un projet logiciel avec des exigences de
déploiement complexes qui impliquent plusieurs environnements, y compris
le transfert et la production. Pour rationaliser votre processus de
déploiement et garantir sa cohérence, vous décidez de l'automatiser à
l'aide de GitHub Actions et de Microsoft Azure. En configurant les
workflows de déploiement, vous pouvez configurer des déclencheurs basés
sur des étiquettes appliquées aux demandes de tirage, qui gèrent
automatiquement la mise en rotation des environnements, le déploiement
vers des environnements intermédiaires et le démantèlement automatique.
Cette approche permet de maintenir l'efficacité et de réduire les
interventions manuelles dans le pipeline de déploiement.

Dans cet atelier pratique, vous allez :

- Configurez des flux de travail pour créer et configurer
  automatiquement des environnements à l'aide de ressources Azure
  lorsqu'une étiquette spécifique est appliquée à une demande de tirage.

- Configurez des tâches de déploiement dans les flux de travail pour
  déployer automatiquement votre projet dans un environnement
  intermédiaire dès réception de l'étiquette appropriée.

Exercice 1 : Création d'un dépôt

1.  Naviguez jusqu'au lien suivant :
    https://github.com/skills/deploy-to-azure

Dans cet atelier, vous allez créer le référentiel à l'aide d'un modèle
public **skills-deploy-to-azure**

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image1.jpeg)

2.  Sélectionnez **Create a new repository** dans le menu **Use this
    template**.

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image2.jpeg)

3.  Entrez les détails suivants et sélectionnez **Create Repository**.

    - Nom du référentiel : **skills-deploy-to-azure**

    - Type de référentiel : **Public**

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image3.jpeg)

Exercice 2 : Configurer les autorisations GITHUB_TOKEN

Au début de chaque exécution de flux de travail, GitHub crée
automatiquement un secret GITHUB_TOKEN unique à utiliser dans votre flux
de travail. Nous devons nous assurer que ce jeton dispose des
autorisations requises.

1.  Sur la page d'accueil du référentiel nouvellement créé, accédez à
    **Settings \> Actions \> General**.

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image4.jpeg)

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image5.jpeg)

2.  Faites défiler jusqu'à **Workflow permissions** et activez les
    **Read and write permissions**, puis cliquez sur **Save**.

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image6.jpeg)

**Remarque :** Ceci est nécessaire pour que le flux de travail
télécharge l'image dans le registre de conteneurs.

Exercice 3 : Configurer un déclencheur basé sur des libellés

1.  Dans la barre de navigation, accédez à l'onglet **Actions**

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image7.jpeg)

2.  Sur la page **Actions,** cliquez sur **New workflow** dans le volet
    de navigation sur le côté gauche.

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image8.jpeg)

3.  Sur la page **Choose a workflow**, recherchez \\**simple
    workflow**\\ et cliquez sur **Configure**

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image9.jpeg)

4.  Nommez votre flux de travail deploy-staging.yml

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image10.jpeg)

5.  Dans la page de l'éditeur, modifiez le contenu du fichier et
    supprimez tous les déclencheurs et tâches. Le fichier résultant
    ressemblera à ce qui est indiqué ci-dessous.

6.  name : Stage the app

7.  on:

8.  pull_request :

9.  Types : \[labeled\]

10. jobs :

11. build:

12. runs-on: ubuntu-latest

if : contains(github.event.pull_request.labels.\*.name, 'stage')

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image11.jpeg)

**Remarque :** Assurez-vous que l'extrait de code ajouté est
correctement mis en retrait, comme indiqué dans la capture d'écran

13. Cliquez sur le bouton **Commit changes** en haut à droite de la
    page.

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image12.jpeg)

14. Dans la fenêtre **Commit Changes**, sélectionnez **Create a new
    branch for this commit and start a pull request.**

**Remarque : Valider les modifications** de la fenêtre Modifications sur
**Proposer des modifications**.

Nommez la **nouvelle branche (new branch)** **staging-workflow** et
cliquez sur **Propose changes**.

![Une capture d'écran d'un chat Le contenu généré par l'IA peut être
incorrect.](./media/image13.jpeg)

15. Sur la page suivante de **Open a pull request**, cliquez sur
    **Create pull request**.

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image14.jpeg)

16. Attendez 20 secondes pour que les actions s'exécutent et examinez
    les résultats.

Résumé:

Vous avez maintenant acquis une expérience pratique de l'automatisation
des flux de travail de déploiement à l'aide de GitHub Actions, ce qui
améliore l'efficacité et la fiabilité de votre processus de déploiement.
