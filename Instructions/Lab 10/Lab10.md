**Lab 10: Verwenden von GitHub Actions zum Veröffentlichen Ihres
Projekts in einem Docker-Image**

Ziele:

Stellen Sie sich vor, Sie entwickeln ein Softwareprojekt, das Sie als
Docker-Image verpacken und verteilen möchten. Um den
Bereitstellungsprozess zu optimieren und sicherzustellen, dass Ihr
Docker-Image konsistent in GitHub Packages veröffentlicht wird,
entscheiden Sie sich für die Verwendung von GitHub Actions für die
Automatisierung. Auf diese Weise können Sie einen Workflow einrichten,
der die Veröffentlichung Ihres Docker-Images automatisiert, wenn
Änderungen vorgenommen werden, um sicherzustellen, dass Ihr Projekt
immer auf dem neuesten Stand und für die Bereitstellung verfügbar ist.

In diesem praxisorientierten Lab werden Sie:

- Richten Sie eine GitHub Actions-Workflowdatei ein, die den Prozess der
  Erstellung und Veröffentlichung Ihres Docker-Images automatisiert.

- Konfigurieren Sie den Workflow, um Ihr Docker-Image zu erstellen und
  an GitHub Packages zu pushen, um sicherzustellen, dass das Image
  ordnungsgemäß veröffentlicht wird.

- Erstellen Sie einen Pull Request, um alle Änderungen anzuzeigen, die
  Sie vorgenommen haben.

Übung \#1: Erstellen eines neuen Repositorys aus einer öffentlichen
Vorlage

1.  Navigieren Sie zu folgendem Link:
    https://github.com/skills/publish-packages

In diesem Lab erstellen Sie das Repository mit einer öffentlichen
Vorlage "**skills-publish-packages**".

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image1.jpeg)

2.  Wählen Sie im Menü **Use this template** die Option **Create a new
    repository** aus.

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image2.jpeg)

3.  Geben Sie die folgenden Details ein, und wählen Sie **Create
    Repository** aus.

    - Name des Repositorys: **skills-publish-packages**

    - Repository-Typ: **Public**

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image3.jpeg)

Übung 2: Erstellen einer Workflowdatei und Konfigurieren des Workflows

1.  Klicken Sie auf die Schaltfläche **Code** in der
    Hauptnavigationsleiste des Repositorys, das Sie gerade erstellt
    haben.

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image4.jpeg)

2.  Wählen Sie in der Dropdown-Liste **"main branch"** die Option "**cd
    branch**" aus.

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image5.jpeg)

3.  Navigieren Sie auf der nächsten Seite zum Ordner
    **.github/workflows/**, wählen Sie **Add file** aus und klicken Sie
    auf **Create new file**.

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image6.jpeg)

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image7.jpeg)

4.  Geben Sie im Feld **Name your file** “publish.yml”

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image8.jpeg)

5.  Fügen Sie der **publish.yml**-Datei den folgenden Code hinzu.

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

38. Ersetzen Sie YOURNAME durch Ihren Benutzernamen.

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image9.jpeg)

39. Stellen Sie sicher, dass der Bildname eindeutig ist, klicken Sie auf
    **Commit changes.**

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image10.jpeg)

40. Klicken Sie erneut auf **Commit changes**.

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image11.jpeg)

41. Erstellen Sie nun einen Pull Request, um alle Änderungen anzuzeigen,
    die Sie in der obigen Übung vorgenommen haben.

42. Klicken Sie in der Navigationsleiste auf die Registerkarte **Pull
    Requests**.

43. Klicken Sie auf **New Pull Request**.

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image12.jpeg)

44. Legen Sie auf der Seite **Comparing changes** **“base: main”** und
    **“compare:cd”** fest, und klicken Sie dann auf **Create pull
    request.**

![Ein Screenshot eines Chats KI-generierte Inhalte können falsch
sein.](./media/image13.jpeg)

45. Klicken Sie auf der Seite **Add a title** auf **Create pull
    request.**

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image14.jpeg)

46. Warten Sie 20 Sekunden, bis Aktionen ausgeführt wurden, und
    überprüfen Sie die Ergebnisse.

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image15.jpeg)

Zusammenfassung:

Sie haben jetzt praktische Erfahrungen in der Verwendung von GitHub
Actions gesammelt, um die Veröffentlichung von Docker-Images zu
automatisieren und Ihre Fähigkeit zu verbessern, Bereitstellungsprozesse
zu optimieren und Projektverteilungen auf dem neuesten Stand zu halten.

