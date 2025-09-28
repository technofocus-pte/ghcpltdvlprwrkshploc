**Lab 08: Erstellen einer GitHub-Aktion und deren Verwendung in einem
Workflow**

Objektiv:

Stellen Sie sich vor, Sie sind Teil eines Entwicklungsteams, das Ihren
Softwareentwicklungsprozess durch die Automatisierung sich
wiederholender Aufgaben optimieren möchte. Um die Effizienz zu
verbessern, entscheiden Sie sich für GitHub Actions, mit denen Sie
Aufgaben wie Tests, Bereitstellung und Codeüberprüfungen direkt in Ihrem
GitHub-Repository automatisieren können. Indem Sie eine GitHub Action
einrichten und in Ihren Workflow integrieren, können Sie sicherstellen,
dass wesentliche Aufgaben automatisch ausgeführt werden, was Zeit spart
und den manuellen Aufwand reduziert.

In diesem praxisorientierten Lab werden Sie:

- Richten Sie eine Workflow-Datei im Verzeichnis .github/workflows ein,
  definieren Sie den Inhalt und geben Sie die Ereignisse an, die den
  Workflow auslösen.

- Üben Sie das Hinzufügen und Committen von Workflowdateien zu Ihrem
  Repository, um GitHub Actions in Ihren Entwicklungsprozess zu
  integrieren.

Übung \#1: Erstellen eines neuen Repositorys aus einer öffentlichen
Vorlage

1.  Navigieren Sie zu folgendem Link:
    https://github.com/skills/hello-github-actions

In diesem Lab erstellen Sie das Repository mithilfe einer öffentlichen
Vorlage "**skills-hello-github-actions**".

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image1.jpeg)

2.  Wählen Sie im Menü **Use this template** die Option **Create a new
    repository** aus.

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image1.jpeg)

3.  Geben Sie die folgenden Details ein, und wählen Sie **Create
    Repository** aus.

    - Name des Repositorys: **skills-hello-github-actions**

    - Repository-Typ: **Public**

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image2.jpeg)

Übung \#2: Erstellen einer Workflow-Datei

1.  Navigieren Sie auf der Landingpage des neu erstellten Repositorys
    zur Registerkarte **Pull Requests**.

![Ein Screenshot einer Webseite KI-generierte Inhalte können falsch
sein.](./media/image3.jpeg)

2.  Klicken Sie auf der nächsten Seite auf die Schaltfläche **New pull
    request**.

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image4.jpeg)

3.  Wählen Sie auf der Seite **" Compare changes "** die Option **"base:
    main"** und **"compare: welcome-workflow"** aus und klicken Sie auf
    **" Create pull request ".**

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image5.jpeg)

4.  Klicken Sie auf der Seite **Open a pull request** auf **Create pull
    request**.

![Ein Screenshot einer E-Mail-Anfrage KI-generierte Inhalte können
falsch sein.](./media/image6.jpeg)

5.  Navigieren Sie zur Registerkarte **Code**.

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image7.jpeg)

6.  Klicken Sie auf der nächsten Seite in der **Dropdown-Liste " main
    branch** " auf den Zweig **" welcome-workflow** ".

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image8.jpeg)

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image9.jpeg)

7.  Sobald der Hauptzweig in **welcome-workflow** geändert wurde,
    navigieren Sie zum Ordner**.github/workflows**, wählen Sie dann
    **Add file** aus und klicken Sie auf **Create new file**.

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image10.jpeg)

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image11.jpeg)

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image12.jpeg)

8.  Geben Sie auf der Seite zur Dateierstellung den Dateinamen als
    **welcome.yml**

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image13.jpeg)

9.  Fügen Sie auf der Editor-Seite den folgenden Inhalt zur
    welcome.yml-Datei hinzu: und klicken Sie auf **Commit changes.**

10. name: Post welcome comment

11. on:

12. pull_request:

13. types: \[opened\]

14. permissions:

pull-requests: write

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image14.jpeg)

15. Klicken Sie auf der Seite **"Commit changes"** auf **" commit
    changes ".**

16. Warten Sie 20 Sekunden, bis die Aktionen ausgeführt werden, und
    aktualisieren Sie diese dann, und eine Aktion schließt diesen
    Schritt automatisch.

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image15.jpeg)

Zusammenfassung:

Sie haben nun praktische Erfahrungen in der Einrichtung und Verwaltung
von GitHub Actions gesammelt und verbessern so Ihre Fähigkeit, Ihre
Workflows in der Softwareentwicklung zu automatisieren und zu
optimieren.

