**Laboratoire n°04 : Examiner les demandes de tirage et résoudre les
conflits de fusion**

Objectif:

Imaginez que vous faites partie d'une équipe de développement
travaillant sur un projet avec plusieurs contributeurs. Au fur et à
mesure que des modifications sont apportées, il est crucial de les
examiner et de s'assurer que le travail de chacun s'intègre sans heurts.
Vous devez collaborer efficacement en gérant les demandes de tirage et
en résolvant les conflits de fusion pour maintenir l'intégrité du projet
et éviter les interruptions.

Dans cet atelier pratique, vous allez vous concentrer sur deux aspects
clés de la collaboration sur GitHub :

- Créer une demande de tirage : sélectionnez les branches appropriées,
  fournissez un titre et une description, puis soumettez une demande de
  tirage pour proposer des modifications.

- Examinez les demandes de tirage : examinez les modifications proposées
  dans les demandes de tirage, en vous assurant qu'elles répondent aux
  normes du projet et qu'elles sont prêtes pour l'intégration.

- Résoudre les conflits de fusion : entraînez-vous à résoudre les
  conflits qui surviennent lorsque des modifications dans différentes
  branches affectent les mêmes parties d'un fichier, garantissant ainsi
  une intégration et une collaboration fluides.

Exercice \#1 : Créer un dépôt à partir d'un modèle et créer une demande
de tirage

La demande de tirage montrera les modifications apportées à votre
branche à d'autres personnes. Cette pull request va conserver les
modifications que vous venez d'apporter sur votre branche et vous
proposer de les appliquer à la branche principale.

1.  Connectez-vous à votre compte GitHub.

2.  Naviguez jusqu'au lien suivant :
    https://github.com/skills/review-pull-requests

Dans cet atelier, vous allez créer le référentiel à l'aide d'un modèle
public « **skills-review-pull-requests** ».

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image1.jpeg)

3.  Sélectionnez **Create a new repository** dans le menu **Use this
    template**.

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image2.jpeg)

4.  Entrez les détails suivants et sélectionnez **Create Repository**.

    - Nom du dépôt : **skills-review-pull-requests**

    - Type de référentiel : **Public**

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image3.jpeg)

5.  Sur la page de navigation principale, sélectionnez l'onglet **Pull
    requests**.

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image4.jpeg)

6.  Sur la page suivante, sélectionnez **New pull request.**

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image5.jpeg)

7.  Sur la page **Compare changes** :

    - Dans la liste déroulante **base** :, sélectionnez **main** (par
      défaut, cette option est sélectionnée)

    - Dans la liste déroulante **compare** :, sélectionnez
      **update-game**,

Il est généralement nécessaire d'attendre quelques secondes et de
rafraîchir la page pour afficher les branches.

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image6.jpeg)

![Une capture d'écran d'un téléphone Le contenu généré par l'IA peut
être incorrect.](./media/image7.jpeg)

8.  Une fois que vous avez sélectionné **update-game** dans la liste
    déroulante **compare :**, la fenêtre **Comparing changes** s'ouvre.
    Cliquez sur **Create pull request**.

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image8.jpeg)

9.  Sur la page **Open a pull request page,** entrez ce qui suit :

    - **Add a title** pour votre demande de tirage : Mettre à jour le
      message de fin de partie

    - **Add a description** pour votre demande de tirage : Mettez à jour
      le message de fin de partie pour que les gens sachent comment
      jouer à nouveau

10. Cliquez sur **Create pull request**.

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image9.jpeg)

11. Attendez environ 20 secondes, puis actualisez cette page. GitHub
    Actions sera automatiquement mis à jour vers l'étape suivante.

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image10.jpeg)

Exercice \#2 : Mettre à jour une demande de tirage et résoudre les
conflits de fusion

1.  Naviguez jusqu'au lien suivant :
    https://github.com/skills/resolve-merge-conflicts

Dans cet atelier, vous allez créer le référentiel à l'aide d'un modèle
public « **skills-resolve-merge-conflicts** ».

![Une capture d'écran d'une page web Le contenu généré par l'IA peut
être incorrect.](./media/image11.jpeg)

2.  Sélectionnez **Create a new repository** dans le menu **Use this
    template**.

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image12.jpeg)

3.  Entrez les détails suivants et sélectionnez **Create Repository**.

    - Nom du dépôt : **skills-resolve-merge-conflicts**

    - Type de référentiel : **Public**

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image13.jpeg)

4.  Une fois le référentiel créé, sélectionnez l' onglet **Pull
    request** dans la barre de navigation principale.

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image14.jpeg)

5.  Cliquez sur **New pull request**.

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image15.jpeg)

6.  Créez une demande de tirage en sélectionnant les éléments suivants :

    - **my-resume** en tant que branche principale et

    - **main** en tant que branche de comparaison.

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image16.jpeg)

![Une capture d'écran d'un chat Le contenu généré par l'IA peut être
incorrect.](./media/image17.jpeg)

7.  Cliquez sur le bouton **Create pull request**

8.  Sur la page **Open a pull request,** entrez le titre Résolution des
    conflits de fusion, puis cliquez sur **Create pull request.**

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image18.jpeg)

9.  Attendez 20 secondes pendant que GitHub Actions se met
    automatiquement à jour et que la page affiche les détails des
    conflits, le cas échéant.

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image19.jpeg)

10. Cliquez sur **Resolve conflicts** pour continuer.

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image20.jpeg)

11. Examinez les conflits et résolvez-les.

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image21.jpeg)

12. Dans cet exercice, nous allons supprimer le conflit d'éléments de
    ligne et cliquer sur le bouton **Marquer comme résolu**.

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image22.jpeg)

13. Cliquez sur le bouton **Commit merge** et cochez la boîte de message
    d'avertissement (Heads up).

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image23.jpeg)

14. Cliquez sur **I understand, continue updating main.** Vous verrez
    les résultats finaux de la vérification\*\*.\*\*

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image24.jpeg)

**Résumé:**

Vous avez maintenant terminé la création et l'examen des demandes de
tirage pour les conflits et la résolution des conflits, des compétences
essentielles pour un travail d'équipe et une gestion de projet efficaces
sur GitHub.
