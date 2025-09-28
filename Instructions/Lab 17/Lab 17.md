**Laboratoire 17 : Activation de l'analyse des secrets dans un
référentiel GitHub et validation d'un jeton**

Imaginez que vous êtes un développeur de logiciels travaillant sur un
projet d'équipe avec un dépôt GitHub partagé. Pour vous assurer que
votre code reste sécurisé et exempt de fuites accidentelles, vous
décidez de mettre en œuvre l'analyse des secrets--- une fonctionnalité
qui permet d'identifier les informations sensibles telles que les jetons
d'API ou les mots de passe qui peuvent être validés par inadvertance
dans le référentiel.

Objectif:

Dans cet atelier pratique, vous allez :

1.  Activer l'analyse des secrets : configurez l'analyse des secrets sur
    votre dépôt GitHub pour détecter et marquer automatiquement les
    informations sensibles.

2.  Valider un jeton : ajoutez intentionnellement un jeton ou d'autres
    informations sensibles au référentiel pour tester l'efficacité de la
    fonctionnalité d'analyse des secrets.

Exercice \#1 : Créer un référentiel GitHub et activer l'analyse des
secrets

Tâche \#1 : Créer un dépôt à l'aide d'un modèle

1.  Connectez-vous à votre compte GitHub.

2.  Naviguez jusqu'au lien suivant :
    https://github.com/skills/introduction-to-secret-scanning

Dans cet atelier, vous allez créer le référentiel à l'aide d'un modèle
public "**skills-introduction-to-secret-scanning**".

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image1.jpeg)

3.  Sélectionnez **Create a new repository** dans le menu **Use this
    template**.

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image2.jpeg)

4.  Entrez les détails suivants et sélectionnez **Create Repository**.

    - Nom du référentiel : **skills-introduction-to-secret-scanning**

    - Type de référentiel : **Public**

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image3.jpeg)

Tâche \#2 : Activer l'analyse des secrets

1.  Sur la page d'accueil du référentiel nouvellement créé, sélectionnez
    **Settings** dans la barre de navigation supérieure.

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image4.jpeg)

2.  Dans la section **Security** de la barre latérale, sélectionnez
    **Code security and analysis**.

**Remarque** : Vous devez faire défiler vers le bas pour voir le menu
**Security**

![Capture d'écran d'une fenêtre de navigateur Le contenu généré par l'IA
peut être incorrect.](./media/image5.jpeg)

3.  Faites défiler la page vers le bas et cliquez sur **Enable**
    l'analyse des secrets.

**Remarque :** Si vous voyez un bouton **Disable**, cela signifie que
l'analyse des secrets est déjà activée pour le référentiel.

![Un fond blanc avec du texte noir Le contenu généré par l'IA peut être
incorrect.](./media/image6.jpeg)

S'il n'est pas déjà activé, vous verrez le bouton **Enable** comme
indiqué ci-dessous :

![Une capture d'écran d'une erreur informatique Le contenu généré par
l'IA peut être incorrect.](./media/image7.jpeg)

**Remarque :** Lorsque l'analyse des secrets est activée, une
notification par e-mail concernant les informations d'identification
dans le référentiel est envoyée à l'ID de messagerie associé au compte.
Les jetons de ce dépôt de compétences sont inactifs. Il n'y a aucun
risque pour l'environnement.

Maintenant que l'analyse des secrets est activée dans ce dépôt, validons
un nouveau jeton pour voir comment il fonctionne.

Exercice \#2 : Valider un token

Dans cet exercice, vous allez valider une clé AWS et un ID d'accès dans
le référentiel. Il s'agit d'un jeton inactif qui ne peut pas être
utilisé pour se connecter à AWS.

1.  Dans le volet supérieur gauche de la barre de navigation principale,
    cliquez sur l'onglet **Code** et sélectionnez le fichier
    **credentials.yml**.

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image8.jpeg)

2.  Cliquez sur le bouton Edit à droite.

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image9.jpeg)

3.  Copiez le texte suivant et collez-le sous le code existant dans le
    volet d'édition du fichier **credentials.yml**.

4.  default:

5.  aws_access_key_id : AKIAQYLPMN5HNM4OZ56B

6.  aws_secret_access_key : Rm29CHLQCeaT6V/Rsw3UFWW1/UWQ0lhsWBa3bdca

7.  output: json

region: us-east-2

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image10.jpeg)

8.  Cliquez sur le bouton **Commit changes** dans le coin supérieur
    droit, puis cliquez à nouveau sur **Commit changes** dans la fenêtre
    **Commit changes**.

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image11.jpeg)

**Remarque :** Une fois que vous avez validé les modifications, vous
recevrez une alerte dans votre boîte aux lettres associée à votre compte
GitHub.

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image12.jpeg)

Résumé:

Vous avez maintenant acquis une compréhension pratique de la façon
d'activer et de tester l'analyse des secrets pour protéger votre code et
vos données.
