**Laboratoire 14 : Sécurisez la chaîne d'approvisionnement de votre
dépôt**

Objectifs:

Imaginez que vous soyez responsable du maintien de la sécurité d'un
projet logiciel qui repose sur diverses dépendances tierces. Pour
garantir l'intégrité et la sécurité de la chaîne d'approvisionnement de
votre projet, il est essentiel de comprendre et de gérer efficacement
ces dépendances. Cela implique d'identifier les vulnérabilités
potentielles au sein de vos dépendances et d'appliquer les correctifs
nécessaires pour sécuriser votre projet. Dans cet atelier, vous allez
apprendre à utiliser la fonctionnalité de dependency graph de GitHub
pour surveiller et examiner vos dépendances, en vous assurant que votre
projet reste sécurisé et à jour.

Dans cet atelier pratique, vous allez :

- Activer Dependency Graph : activez et vérifiez la fonctionnalité de
  graphe de dépendances dans les paramètres de votre référentiel pour
  visualiser les dépendances de votre projet.

- Ajouter une nouvelle dépendance (New Dependency) : ajoutez une
  nouvelle dépendance à votre projet et assurez-vous qu'elle est
  correctement intégrée.

- Examiner Dependency Graph: utilisez le graphique de dépendances pour
  vérifier et confirmer que la nouvelle dépendance est correctement
  reflétée et surveillée.

Exercice 01 : Création d'un référentiel

1.  Naviguez jusqu'au lien suivant :
    https://github.com/skills/secure-repository-supply-chain

Dans cet atelier, vous allez créer le référentiel à l'aide d'un modèle
public **skills-secure-repository-supply-chain**

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image1.jpeg)

2.  Sélectionnez **Create a new repository** dans le menu **Use this
    template**.

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image2.jpeg)

3.  Entrez les détails suivants et sélectionnez **Create Repository**.

    - Nom du référentiel : **skills-secure-repository-supply-chain**

    - Type de référentiel : **Public**

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image3.jpeg)

Exercice 02 : Vérifier que Dependency graph est activé

1.  Sur la page d'accueil du référentiel nouvellement créé, accédez à l'
    onglet **Settings**.

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image4.jpeg)

2.  Sur la page **Settings**, sélectionnez **Code security and
    analysis** disponibles sous **Security.**

![Une capture d'écran d'un identifiant général Le contenu généré par
l'IA peut être incorrect.](./media/image5.jpeg)

3.  Vérifier/activer Dependency graph. (Si le dépôt est privé, vous
    l'activerez ici. Si le dépôt est public, il sera activé par défaut)

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image6.jpeg)

Exercice 03 : Ajouter une nouvelle dépendance et afficher votre
graphique de dépendances

1.  Accédez à l'onglet **Code** et recherchez le dossier
    **code/src/AttendeeSite**.

**Remarque :** Vous pouvez soit accéder au dossier, soit utiliser le
**Go to** recherche code/src/AttendeeSite

![Une capture d'écran d'une page web Le contenu généré par l'IA peut
être incorrect.](./media/image7.jpeg)

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image8.jpeg)

2.  Ouvrez le fichier **package-lock.json**.

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image9.jpeg)

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image10.jpeg)

3.  Insérez l'extrait de code suivant entre la ligne \# 14 et la ligne
    \# 15

4.  "follow-redirects": {

5.  "version": "1.14.1",

6.  "resolved":

7.  "https://registry.npmjs.org/follow-redirects/-/follow-redirects-1.14.1.tgz",

8.  "integrity":

9.  "sha512-HWqDgT7ZEkqRzBvc2s64vSZ/hfOceEol3ac/7tKwzuvEyWx3/4UegXh5oBOIotkGsObyk3xznnSRVADBgWSQVg=="

},

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image11.jpeg)

**Remarque :** Assurez-vous que l'extrait de code ajouté est
correctement mis en retrait, comme indiqué dans la capture d'écran

10. Cliquez sur **Commit changes** en haut à droite.

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image12.jpeg)

11. Dans la barre de navigation principale, cliquez sur l'**onglet
    Insights**.

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image13.jpeg)

12. Dans le volet de navigation de gauche, cliquez sur **Dependency
    graph**.

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image14.jpeg)

13. Passez en revue toutes les nouvelles dépendances sur le hub
    Dépendances.

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image15.jpeg)

14. Recherchez follow-redirects et passez en revue la nouvelle
    dépendance que vous venez d'ajouter.

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image16.jpeg)

Résumé:

Vous avez maintenant acquis des informations précieuses sur la gestion
des dépendances de votre projet et la sécurisation de la chaîne
d'approvisionnement de votre dépôt, ce qui vous permet de traiter et
d'atténuer de manière proactive les risques de sécurité.
