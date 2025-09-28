Laboratoire 16 : Suppression de l'historique des validations d'un
référentiel Git (Git repository) (Git Repository)

Objectif :

Imaginez que vous faites partie d'une équipe de développement
travaillant sur un projet où des informations sensibles, telles que des
clés API ou des informations d'identification de base de données, ont
été accidentellement validées dans votre référentiel Git (Git
repository). Les commits accidentels peuvent être difficiles à supprimer
avec Git.

Dans cet atelier, vous allez :

- Clonez le référentiel (repository) avec des données sensibles validées
  accidentellement.

- Supprimez/supprimez le fichier contenant des données sensibles du
  référentiel cloné et validez la suppression.

- Envoyer les modifications à GitHub : chargez le référentiel mis à jour
  sur GitHub pour refléter les modifications.

### Exercice \#1 : Créer le référentiel (repository) avec l'historique des validations accidentelles (données sensibles)

1.  Connectez-vous à votre compte GitHub.

2.  Naviguez jusqu'au lien suivant :
    <https://github.com/skills/change-commit-history>

> Dans cet atelier, vous allez créer le référentiel à l'aide d'un modèle
> public “**skills-change-commit-history**”.
>
> ![](./media/image1.png)

3.  Sélectionnez **Create a new repository** dans le menu **Use this
    template**.

> ![Une capture d'écran d'un ordinateur Description générée
> automatiquement](./media/image2.png)

4.  Entrez les détails suivants et sélectionnez **Créer un
    référentiel**.

- Nom du dépôt : **skills-change-commit-history**

- Type de référentiel : **Public**

![](./media/image3.png)

### Exercice \# 2 : Supprimer/supprimer le fichier (.env in the project root directory) contenant des données sensibles

1.  Sur la page d'accueil du référentiel cloné, accédez à
    **Code\>Local\>HTTPS** et copiez l'URL.

![](./media/image4.png)

2.  Ouvrez Windows Powershell et entrez la commande suivante.

**git clone \<your-repository-url\>**

**Remarque** : remplacez par l'URL que vous avez copiée à l'étape 1.

> ![](./media/image5.png)

3.  Basculez vers le répertoire de votre référentiel, entrez la commande
    suivante.

**+++cd “C:\Users\Admin\skills-change-commit-history”+++**

**Remarque** : remplacez par le nom du référentiel (repository)

> ![](./media/image6.png)

4.  Exécutez la commande suivante pour supprimer .env du répertoire
    racine,

**+++git rm .env+++**

> ![Une capture d'écran d'un écran d'ordinateur Description générée
> automatiquement](./media/image7.png)

5.  Valider la suppression du fichier .env

**+++git commit -m "remove .env file”+++**

> ![Une capture d'écran d'un ordinateur Description générée
> automatiquement](./media/image8.png)
>
> **Astuce** : Comment supprimer complètement le fichier .env de
> l'historique Git et réécrire l'historique total avec de nouveaux
> hachages de commit ?
>
> Utilisez les commandes suivantes pour :

- Supprimez complètement le fichier .env de l'historique Git et
  réécrivez l'historique total

- **git filter-branch --force --index-filter 'git rm --cached
  --ignore-unmatch.env' --prune-empty --tag-name-filter cat -- --all**

- Envoyer la suppression à GitHub

> **git push origin --force –all**

6.  Poussez la suppression sur GitHub :

**git push**

> ![Capture d'écran d'un programme informatique Description générée
> automatiquement](./media/image9.png)

Résumé:

Vous avez maintenant terminé le nettoyage de votre référentiel Git (Git
repository), en vous assurant que le contenu sensible n'est pas exposé
dans l'historique du référentiel.
