**Laboratoire 11 : Rendre un flux de travail réutilisable et utiliser
une stratégie matricielle pour exécuter plusieurs versions de nœud**

Objectifs:

Imaginez que vous gériez plusieurs référentiels au sein d'un projet qui
partagent des flux de travail communs pour des tâches telles que la
création, les tests et le déploiement. Pour éviter la redondance et
maintenir la cohérence entre ces dépôts, vous décidez d'implémenter des
flux de travail réutilisables à l'aide de GitHub Actions. En utilisant
le déclencheur d'appel de flux de travail, vous pouvez centraliser vos
configurations de flux de travail, en vous assurant que les
modifications sont apportées à un seul endroit et appliquées
automatiquement dans tous les référentiels concernés. De plus, vous
utiliserez des stratégies matricielles pour tester vos flux de travail
avec plusieurs versions de Node.js, améliorant ainsi la compatibilité et
l'évolutivité.

Dans cet atelier pratique, vous allez :

- Utilisez le déclencheur workflow_call pour rendre vos flux de travail
  réutilisables dans plusieurs dépôts, réduisant ainsi la redondance de
  configuration.

- Accédez à votre référentiel, mettez à jour le fichier de flux de
  travail pour inclure le déclencheur workflow_call et validez les
  modifications.

- Créez une demande de tirage pour comparer les modifications et les
  exceptions.

Exercice \#1 : créer un nouveau dépôt.

1.  Naviguez jusqu'au lien suivant :
    https://github.com/skills/reusable-workflows

Dans cet atelier, vous allez créer le référentiel à l'aide d'un modèle
public « **skills-reusable-workflows** ».

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image1.jpeg)

2.  Sélectionnez **Create a new repository** dans le menu **Use this
    template**.

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image2.jpeg)

3.  Entrez les détails suivants et sélectionnez **Create Repository**.

    - Nom du référentiel : **skills-reusable-workflows**

    - Type de référentiel : **Public**

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image3.jpeg)

Exercice \#2 : Ajouter un déclencheur workflow_call à un workflow

1.  Sur la page d'accueil du référentiel nouvellement créé, accédez à l'
    onglet **Code**\*\*.\*\*

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image4.jpeg)

2.  Dans la liste déroulante de la branche principale, sélectionnez la
    branche **reusable-workflow**.

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image5.jpeg)

3.  Après avoir changé de branche, accédez au dossier
    **.github/workflows/**, puis sélectionnez **reusable-workflow.yml**
    fichier.

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image6.jpeg)

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image7.jpeg)

4.  Dans l' éditeur de fichiers **reusable-workflow.yml**, sélectionnez
    **Edit in place**.

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image8.jpeg)

5.  Remplacez le déclencheur d'événement **workflow_dispatch** par le
    déclencheur d' événement **workflow_call** et cliquez sur **Commit
    changes**.

**Remarque** : Remplacez le bloc de code de la **ligne \#3** à la
**ligne \# 8** par celui ci-dessous

sur:

workflow_call :

inputs:

node:

required: true

type: string![Une capture d'écran d'un ordinateur Le contenu généré par
l'IA peut être incorrect.](./media/image9.jpeg)

6.  Dans la fenêtre **Commit changes**, cliquez sur **Commit changes.**

![Une capture d'écran d'une capture d'écran d'une nouvelle branche Le
contenu généré par l'IA peut être incorrect.](./media/image10.jpeg)

Exercice \#3 : Créer une demande de tirage pour afficher les
modifications apportées lors de l'exercice précédent

1.  Sélectionnez l'onglet **Pull requests**, puis cliquez sur **New pull
    request**.

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image11.jpeg)

2.  Sur la page **Comparing changes**, définissez **base** comme
    **main** et **compare** comme **reusable-workflow.**

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image12.jpeg)

3.  Sur la page **Open a pull request**, cliquez sur **Create pull
    request.**

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image13.jpeg)

4.  Attendez 20 secondes pour que les actions s'exécutent et examinez
    les résultats.

Résumé:

Vous avez maintenant acquis une expérience pratique dans la création de
flux de travail efficaces et réutilisables et leur optimisation pour
divers environnements à l'aide de GitHub Actions.
