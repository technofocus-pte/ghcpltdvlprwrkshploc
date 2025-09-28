**Lab 12: Erstellen von Bereitstellungsworkflows mit GitHub Actions und
Microsoft Azure**

Ziele:

Stellen Sie sich vor, Sie verwalten ein Softwareprojekt mit komplexen
Bereitstellungsanforderungen, die mehrere Umgebungen umfassen,
einschließlich Staging und Produktion. Um Ihren Bereitstellungsprozess
zu optimieren und Konsistenz zu gewährleisten, entscheiden Sie sich für
die Automatisierung mit GitHub Actions und Microsoft Azure. Durch das
Konfigurieren von Bereitstellungsworkflows können Sie Triggers basierend
auf Labels einrichten, die auf Pull Requests angewendet werden, die das
Einrichten von Umgebungen, das Bereitstellen im Staging und das
automatische Beenden von Umgebungen verarbeiten. Dieser Ansatz trägt
dazu bei, die Effizienz aufrechtzuerhalten und manuelle Eingriffe in die
Bereitstellungspipeline zu reduzieren.

In diesem praxisorientierten Lab werden Sie:

- Konfigurieren Sie Workflows so, dass Umgebungen mithilfe von
  Azure-Ressourcen automatisch erstellt und eingerichtet werden, wenn
  ein bestimmtes Label auf einen Pull Request angewendet wird.

- Richten Sie Bereitstellungsaufgaben innerhalb der Workflows ein, um
  Ihr Projekt automatisch in einer Staging-Umgebung bereitzustellen,
  sobald Sie das entsprechende Label erhalten.

Übung 1: Erstellen eines neuen Repositorys

1.  Navigieren Sie zu folgendem Link:
    https://github.com/skills/deploy-to-azure

In diesem Lab erstellen Sie das Repository mithilfe einer öffentlichen
Vorlage **skills-deploy-to-azure**

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image1.jpeg)

2.  Wählen Sie im Menü **Use this template** die Option **Create a new
    repository** aus.

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image2.jpeg)

3.  Geben Sie die folgenden Details ein, und wählen Sie **Create
    Repository** aus.

    - Name des Repositorys: **skills-deploy-to-azure**

    - Repository-Typ: **Public**

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image3.jpeg)

Übung 2: Konfigurieren GITHUB_TOKEN-Berechtigungen

Zu Beginn jeder Workflowausführung erstellt GitHub automatisch ein
eindeutiges GITHUB_TOKEN Geheimnis, das in Ihrem Workflow verwendet
werden kann. Wir müssen sicherstellen, dass dieses Token über die
erforderlichen Berechtigungen verfügt.

1.  Gehen Sie auf der Landingpage des neu erstellten Repositorys zu
    **Settings** \> **Actions** \> **General**.

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image4.jpeg)

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image5.jpeg)

2.  Scrollen Sie nach unten zu **Workflow permissions**, aktivieren Sie
    **Read and write permissions** und klicken Sie auf **Save**.

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image6.jpeg)

**Hinweis:** Dies ist erforderlich, damit der Workflow das Image in das
Container-Registry hochladen kann.

Übung 3: Konfigurieren eines Triggers basierend auf Labels

1.  Wechseln Sie in der Navigationsleiste zur Registerkarte **Actions**

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image7.jpeg)

2.  Klicken Sie auf der Seite **Actions** im Navigationsbereich auf der
    linken Seite auf **New Workflow**.

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image8.jpeg)

3.  Suchen Sie auf der Seite **Choose a workflow** nach \\ **simple
    workflow** \\ und klicken Sie auf **Configure**

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image9.jpeg)

4.  Benennen Sie Ihren Workflow **deploy-staging.yml**

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image10.jpeg)

5.  Bearbeiten Sie auf der Editorseite den Inhalt der Datei und
    entfernen Sie alle Trigger und Jobs. Die resultierende Datei sieht
    wie unten gezeigt aus.

6.  name: Stage the app

7.  on:

8.  pull_request:

9.  types: \[labeled\]

10. jobs:

11. build:

12. runs-on: ubuntu-latest

if: contains(github.event.pull_request.labels.\*.name, 'stage')

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image11.jpeg)

**Hinweis:** Bitte stellen Sie sicher, dass das hinzugefügte
Code-Snippet richtig eingerückt ist, wie im Screenshot gezeigt

13. Klicken Sie oben rechts auf der Seite auf die Schaltfläche **Commit
    changes**.

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image12.jpeg)

14. Wählen Sie im Fenster **Commit Changes** die Option **Create a new
    branch for this commit and start a pull request** aus.

**Hinweis:** Das Fenster **Commit changes** ändert sich zu **Propose
changes.**

Benennen Sie **new branch** als **staging-workflow** und klicken Sie auf
**Propose changes**.

![Ein Screenshot eines Chats KI-generierte Inhalte können falsch
sein.](./media/image13.jpeg)

15. Klicken Sie auf der nächsten Seite von **Open a pull request** auf
    **Create pull request**.

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image14.jpeg)

16. Warten Sie 20 Sekunden, bis Aktionen ausgeführt wurden, und
    überprüfen Sie die Ergebnisse.

Zusammenfassung:

Jetzt haben Sie praktische Erfahrungen in der Automatisierung von
Bereitstellungsworkflows mit GitHub Actions gesammelt, um die Effizienz
und Zuverlässigkeit Ihres Bereitstellungsprozesses zu verbessern.

