**Lab 05: Verwalten von Software-Releases mit einem GitHub
Release-basierten Workflow**

Objektiv:

Stellen Sie sich vor, Sie sind Teil eines Softwareentwicklungsteams, das
an einem Projekt arbeitet, das regelmäßige Updates und Releases
erfordert. Um Ihre Software effizient zu verwalten, entscheiden Sie sich
für die Implementierung eines releasebasierten Workflows mithilfe von
GitHub. Dieser Workflow hilft Ihnen, die Versionierung zu handhaben und
Softwareiterationen effektiv zu verwalten, indem er sicherstellt, dass
jeden Release nachverfolgt und Probleme auf kontrollierte Weise behoben
werden.

In diesem praxisorientierten Lab werden Sie

- Erstellen eines Repositorys: Richten Sie ein Repository mit dem Namen
  skills-release-based-workflow ein, das als Grundlage für Ihren
  releasebasierten Workflow dient.

- Implementieren der Versionierung: Erkunden Sie die Konzepte der
  Versionierung und die Bedeutung der Nachverfolgung von
  Softwareiterationen.

- Erstellen eines Beta-Releases: Führen Sie die Schritte aus, um ein
  Beta-Release für die aktuelle Codebasis zu erstellen, einschließlich
  des Taggings und Veröffentlichens auf GitHub.

- Simulieren eines realen Szenarios: Führen Sie einen Fehler in die
  Codebasis ein und simulieren Sie ein allgemeines Szenario zum
  Identifizieren und Beheben von Problemen innerhalb des
  Release-Workflows.

Übung \#1: Einrichten eines neuen Repositorys (als Grundlage für einen
releasebasierten Workflow)

1.  Melden Sie sich bei Ihrem GitHub-Konto an.

2.  Navigieren Sie zu folgendem Link:
    https://github.com/skills/release-based-workflow

In diesem Lab erstellen Sie das Repository mit einer öffentlichen
Vorlage "**skills-release-based-workflow**".

![](./media/image1.jpeg)

3.  Wählen Sie im Menü **Use this template** die Option **Create a new
    repository** aus.

![](./media/image2.jpeg)

4.  Geben Sie die folgenden Details ein, und wählen Sie **Create
    Repository** aus.

    - Name des Repositorys: **skills-release-based-workflow**

    - Repository-Typ: **Public**

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image3.jpeg)

Übung \#2: Erstellen eines Releases für die aktuelle Codebasis

In dieser Übung erstellen wir ein Release für dieses Repository auf
GitHub.

- GitHub Releases verweisen auf einen bestimmten Commit.

- Releases können Versionshinweise in Markdown-Dateien und angehängten
  Binärdateien enthalten.

Hinweis: Bevor Sie einen releasebasierten Workflow für ein größeres
Release verwenden, erstellen Sie ein Tag und ein Release.

1.  Sobald das Repository erstellt ist (in Übung \#1), navigieren Sie in
    der rechten Seitenleiste der Seite zu **Releases** und klicken Sie
    auf **Create a new release.**

![](./media/image4.jpeg)

Tipp: Um zu dieser Seite zu gelangen, klicken Sie oben in Ihrem
Repository auf die Registerkarte **Code**. Suchen Sie dann den Abschnitt
**"Releases"** in der Seitenleiste auf der rechten Seite.

1.  Geben Sie auf der Seite **Releases/Tags** Folgendes ein:

    - Behalten Sie das **Target** als “main” bei

    - Geben Sie im Feld für **Choose a Tag** eine Zahl an.

Verwenden Sie in diesem Fall v0.9, und wählen Sie **Create new tag v0.9
on publish** aus.

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image5.jpeg)

2.  Geben Sie dem Release einen Titel, z. B. First beta release

**Hinweis:** Sie können dem Release auch eine kurze Beschreibung geben.

![](./media/image6.jpeg)

3.  Scrollen Sie auf der Seite nach unten, um das Kontrollkästchen neben
    **Set as a pre-release** zu aktivieren, da es sich um eine
    Beta-Version handelt, und klicken Sie auf **Publish** **release**.

![Ein Screenshot eines Telefons KI-generierte Inhalte können falsch
sein.](./media/image7.jpeg)

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image8.jpeg)

Übung \#3: Einen Fehler einführen (der später behoben werden soll)

Um die Voraussetzungen für später zu schaffen, fügen wir nun einen
Fehler hinzu, den wir im Rahmen des Release-Workflows in späteren
Schritten beheben werden. Ein Zweig "update-text-colors" ist bereits im
Repository erstellt (erstellt in Übung \#1) für Sie, also erstellen und
führen wir einen Pull-Request mit diesem Zweig zusammen.

1.  Klicken Sie in der Hauptnavigationsleiste auf die Registerkarte
    **Pull Requests**.

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image9.jpeg)

2.  Klicken Sie auf der nächsten Seite auf **New Pull Request.**

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image10.jpeg)

3.  Wählen Sie auf der Seite **Compare changes** Folgendes aus, und
    klicken Sie auf **Create pull request:**

    - Base: **release-v1.0** und

    - Compare: **update-text-colors**.

![](./media/image11.jpeg)

4.  Geben Sie auf der **Seite “Open a pull request”** Folgendes ein, und
    klicken Sie dann auf **Create pull request.**

    - Hinzufügen eines Titels: Legen Sie den Pull Request-Titel auf
      “Updated game text style” fest.

    - Hinzufügen einer Beschreibung: \## Description: Updated game text
      color to green

![](./media/image12.jpeg)

5.  Klicken Sie auf der Seite **Updated game text style \#1** auf
    **Merge pull request** und dann auf **Confirm page.**

![](./media/image13.jpeg)

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image14.jpeg)

6.  Löschen Sie auf der nächsten Seite den neu erstellten Zweig, indem
    Sie auf die Schaltfläche **Delete branch** klicken.

![](./media/image15.jpeg)

7.  Warten Sie etwa 20 Sekunden, während GitHub Actions die Seite
    automatisch aktualisiert.

![](./media/image16.jpeg)

**Zusammenfassung:**

Sie haben nun praktische Erfahrungen in der Einrichtung und Verwaltung
eines releasebasierten Workflows gesammelt, der Ihre Fähigkeit zur
Nachverfolgung von Versionen, zum Umgang mit Releases und zur
effizienten Behebung von Fehlern verbessert.

