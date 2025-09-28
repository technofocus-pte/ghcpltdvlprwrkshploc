**Laboratoire 03 : Créez votre portfolio en ligne avec GitHub Pages et
Jekyll**

Objectif:

Imaginez que vous êtes un développeur de logiciels en herbe dans une
start-up technologique, désireux de présenter vos projets, vos
compétences et vos expériences à travers un portfolio en ligne. Vous
souhaitez disposer d'une plateforme professionnelle pour afficher votre
travail, c'est pourquoi vous décidez de créer un site web ou un blog
personnel à l'aide de GitHub Pages. Cette plateforme vous permet
d'exploiter les référentiels GitHub pour publier et gérer facilement
votre site web.

Dans cet atelier pratique, vous allez :

- Créez un référentiel GitHub : configurez un nouveau référentiel qui
  servira de base à votre site personnel.

- Activer GitHub Pages : configurez GitHub Pages pour héberger votre
  site web directement à partir de votre dépôt.

- Déployez votre premier site à l'aide de Jekyll : Utilisez Jekyll, un
  générateur de sites statiques populaire, pour créer et déployer un
  site Web d'aspect professionnel avec un minimum d'effort.

Exercice \#1 : Créer un référentiel à partir d'un modèle

1.  Connectez-vous à votre compte GitHub.

2.  Naviguez jusqu'au lien suivant :
    https://github.com/skills/github-pages

Dans cet atelier, vous allez créer le référentiel à l'aide d'un modèle
public « **skills-github-pages** ».

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image1.jpeg)

3.  Sélectionnez **Create a new repository** dans le menu **Use this
    template**.

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image2.jpeg)

4.  Entrez les détails suivants et sélectionnez **Create Repository**.

    - Nom du dépôt : **skills-github-pages**

    - Type de référentiel : **Public**

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image3.jpeg)

Exercice \#2 : Activer les pages GitHub

1.  Une fois le référentiel créé, accédez à la page d'accueil. Dans le
    volet de navigation principal, cliquez sur l'icône **Settings**.

![Une capture d'écran d'une page web Le contenu généré par l'IA peut
être incorrect.](./media/image4.jpeg)

2.  Dans la page de configuration, faites défiler jusqu'à Code et
    automatisation et cliquez sur **Pages.**

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image5.jpeg)

3.  Sur les pages GitHub, assurez-vous que l'option « **Deploy from a
    branch **» est sélectionnée dans le menu déroulant Source, puis
    sélectionnez **principal** dans le menu déroulant **Branch**.

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image6.jpeg)

4.  Cliquez sur le bouton **Save** pour continuer.

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image7.jpeg)

5.  La source GitHub Pages sera enregistrée. Attendez environ une minute
    puis actualisez cette page. GitHub Actions sera automatiquement mis
    à jour vers l'étape suivante.

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image8.jpeg)

6.  Votre site est maintenant en ligne.

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image9.jpeg)

7.  Cliquez sur le bouton Visiter le site pour voir votre site. Vous
    avez activé les pages GitHub.

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image10.jpeg)

Exercice \#3 : Déployer votre site à l'aide de Jekyll

Vous travaillerez dans une branche, **my-pages**, pour que ce site ait
fière allure. Dans cet atelier, nous allons utiliser un thème prêt à
l'emploi. « minima ».

Jekyll utilise un fichier intitulé **\_config.yml** pour stocker les
paramètres de votre site, votre thème et le contenu réutilisable comme
le titre de votre site et le handle GitHub.

1.  Sélectionnez l'onglet **Code** de votre dépôt

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image11.jpeg)

2.  Développez la branche **main** et sélectionnez **mes-pages**.

![Une capture d'écran d'une page web Le contenu généré par l'IA peut
être incorrect.](./media/image12.jpeg)

Dans la branche **my-pages**, accédez au fichier \_**config.yml**

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image13.jpeg)

3.  Ouvrez l'éditeur de fichiers dans le coin supérieur droit.

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image14.jpeg)

4.  Ajouter un thème : défini sur **minima** pour qu'il s'affiche dans
    le fichier \_config.yml comme ci-dessous :

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image15.jpeg)

5.  Cliquez sur le bouton **Commit Changes** pour enregistrer les
    modifications.

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image16.jpeg)

**Remarque :** Attendez environ une minute, puis actualisez cette page.
GitHub Actions sera automatiquement mis à jour vers l'étape suivante.

6.  Pour vérifier le site mis à jour, cliquez sur le bouton **Visit
    site** sous Pages GitHub.

![Une capture d'écran d'une page web Le contenu généré par l'IA peut
être incorrect.](./media/image17.jpeg)

7.  Le thème sélectionné est appliqué. Vous pouvez continuer à modifier
    les autres variables de configuration telles que title :, author :,
    et description :, pour personnaliser davantage votre site

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image18.jpeg)

Résumé:

Vous avez maintenant créé un site web avec des pages GitHub et appliqué
un thème. Vous pouvez utiliser cette expérience pour créer un site Web
en direct où vous pouvez continuellement mettre à jour et présenter
votre parcours de développement de logiciels, ce qui permet aux
employeurs, aux collaborateurs et à la communauté technologique de voir
plus facilement votre travail et vos compétences.
