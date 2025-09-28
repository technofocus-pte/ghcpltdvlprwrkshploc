**Laboratoire 10 : Utiliser GitHub Actions pour publier votre projet
dans une image Docker**

Objectifs:

Imaginez que vous développez un projet logiciel que vous souhaitez
empaqueter et distribuer en tant qu'image Docker. Pour rationaliser le
processus de déploiement et vous assurer que votre image Docker est
publiée de manière cohérente dans GitHub Packages, vous décidez
d'utiliser GitHub Actions pour l'automatisation. Cela vous permettra de
mettre en place un flux de travail qui automatise la publication de
votre image Docker chaque fois que des modifications sont apportées,
garantissant ainsi que votre projet est toujours à jour et disponible
pour le déploiement.

Dans cet atelier pratique, vous allez :

- Configurez un fichier de flux de travail GitHub Actions qui automatise
  le processus de création et de publication de votre image Docker.

- Configurez le flux de travail pour générer votre image Docker et
  l'envoyer aux packages GitHub, en vous assurant que l'image est
  correctement publiée.

- Créez une demande de tirage pour afficher toutes les modifications que
  vous avez apportées.

Exercice \#1 : Créer un dépôt à partir d'un modèle public

1.  Naviguez jusqu'au lien suivant :
    https://github.com/skills/publish-packages

Dans cet atelier, vous allez créer le référentiel à l'aide d'un modèle
public « **skills-publish-packages** ».

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image1.jpeg)

2.  Sélectionnez **Create a new repository** dans le menu **Use this
    template**.

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image2.jpeg)

3.  Entrez les détails suivants et sélectionnez **Create Repository**.

    - Nom du dépôt : **skills-publish-packages**

    - Type de référentiel : **Public**

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image3.jpeg)

Exercice 2 : Création d'un fichier de flux de travail et configuration
du flux de travail

1.  Cliquez sur le bouton **Code** dans la barre de navigation
    principale du dépôt que vous venez de créer.

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image4.jpeg)

2.  Dans la liste déroulante de la branche **main**, sélectionnez branch
    **cd**.

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image5.jpeg)

3.  Sur la page suivante, accédez au dossier **.github/workflows/**,
    puis sélectionnez **Add file**, puis cliquez sur **Create new
    file**.

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image6.jpeg)

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image7.jpeg)

4.  Dans le champ **Name your file**, saisissez publish.yml

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image8.jpeg)

5.  Add the following code to the **publish.yml** file.

6.  name: Publish to Docker

7.  on:

8.  push:

9.  branches:

10. \- main

11. permissions:

12. packages: write

13. contents: read

14. jobs:

15. publish:

16. runs-on: ubuntu-latest

17. steps:

18. \- name: Checkout

19. uses: actions/checkout@v4

20. \# Add your test steps here if needed...

21. \- name: Docker meta

22. id: meta

23. uses: docker/metadata-action@v5

24. with:

25. images: ghcr.io/YOURNAME/publish-packages/game

26. tags: type=sha

27. \- name: Login to GHCR

28. uses: docker/login-action@v3

29. with:

30. registry: ghcr.io

31. username: ${{ github.repository_owner }}

32. password: ${{ secrets.GITHUB_TOKEN }}

33. \- name: Build container

34. uses: docker/build-push-action@v5

35. with:

36. context: .

37. push: true

tags: ${{ steps.meta.outputs.tags }}

38. Replace YOURNAME with your username.

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image9.jpeg)

39. Assurez-vous que le nom de l'image est unique, cliquez sur **Commit
    changes.**

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image10.jpeg)

40. Cliquez à nouveau sur **Commit changes**.

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image11.jpeg)

41. Créez maintenant une demande de tirage pour afficher toutes les
    modifications que vous avez apportées dans l'exercice ci-dessus.

42. Cliquez sur l' onglet **Pull Requests** dans la barre de navigation.

43. Cliquez sur **New pull request**.

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image12.jpeg)

44. Sur la page **Comparing changes**, définissez **base** : main et
    **compare** :cd, puis cliquez sur **Create pull request.**

![Une capture d'écran d'un chat Le contenu généré par l'IA peut être
incorrect.](./media/image13.jpeg)

45. Sur la page **Add a title**, cliquez sur **Create pull request.**

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image14.jpeg)

46. Attendez 20 secondes pour que les actions s'exécutent et examinez
    les résultats.

![Une capture d'écran d'un ordinateur Le contenu généré par l'IA peut
être incorrect.](./media/image15.jpeg)

Résumé:

Vous avez maintenant acquis une expérience pratique de l'utilisation de
GitHub Actions pour automatiser la publication d'images Docker, ce qui
améliore votre capacité à rationaliser les processus de déploiement et à
maintenir à jour les distributions de projet.
