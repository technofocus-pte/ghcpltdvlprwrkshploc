**Lab 11: Wiederverwendbarkeit eines Workflows und Verwendung einer
Matrixstrategie zum Ausführen mehrerer Versionen des Knotens**

Ziele:

Stellen Sie sich vor, Sie verwalten mehrere Repositorys innerhalb eines
Projekts, die gemeinsame Workflows für Aufgaben wie Erstellen, Testen
und Bereitstellen verwenden. Um Redundanzen zu vermeiden und die
Konsistenz in diesen Repositorys zu wahren, entscheiden Sie sich für die
Implementierung wiederverwendbarer Workflows mithilfe von GitHub
Actions. Durch die Verwendung des Workflow-Call-Triggers können Sie Ihre
Workflow-Konfigurationen zentralisieren und sicherstellen, dass
Änderungen an einem Ort vorgenommen und automatisch auf alle relevanten
Repositorys angewendet werden. Darüber hinaus nutzen Sie
Matrixstrategien, um Ihre Workflows mit mehreren Versionen von Node.js
zu testen und so die Kompatibilität und Skalierbarkeit zu verbessern.

In diesem praxisorientierten Lab werden Sie:

- Verwenden Sie den workflow_call-Trigger, um Ihre Workflows über
  mehrere Repositories hinweg wiederverwendbar zu machen und so die
  Konfigurationsredundanz zu reduzieren.

- Navigieren Sie zu Ihrem Repository, aktualisieren Sie die
  Workflow-Datei, um den workflow_call-Trigger einzuschließen, und
  übernehmen Sie die Änderungen.

- Erstellen Sie einen Pull Request, um die Änderungen und Ausnahmen zu
  vergleichen.

Übung \#1: Erstellen Sie ein neues Repository.

1.  Navigieren Sie zu folgendem Link:
    https://github.com/skills/reusable-workflows

In diesem Lab erstellen Sie das Repository mit einer öffentlichen
Vorlage "**skills-reusable-workflows**".

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image1.jpeg)

2.  Wählen Sie im Menü **Use this template** die Option **Create a new
    repository** aus.

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image2.jpeg)

3.  Geben Sie die folgenden Details ein, und wählen Sie **Create
    Repository** aus.

    - Name des Repositorys: **skills-reusable-workflows**

    - Repository-Typ: **Public**

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image3.jpeg)

Übung \#2: Hinzufügen eines workflow_call-Triggers zu einem Workflow

1.  Navigieren Sie auf der Landingpage des neu erstellten Repositorys
    zur Registerkarte **Code**\*\*.\*\*

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image4.jpeg)

2.  Wählen Sie in der Dropdown-Liste "main branch" den Zweig
    **"reusable-workflow"** aus.

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image5.jpeg)

3.  Nachdem Sie den Zweig geändert haben, navigieren Sie zum Ordner
    **.github/workflows/** und wählen Sie dann die Datei
    **reusable-workflow.yml** aus.

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image6.jpeg)

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image7.jpeg)

4.  Wählen Sie im **reusable-workflow.yml** Datei-Editor die Option
    **Edit in place** aus.

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image8.jpeg)

5.  Ersetzen Sie den Ereignisauslöser **workflow_dispatch** durch den
    Ereignisauslöser **workflow_call** und klicken Sie auf **Commit
    changes**.

**Hinweis**: Ersetzen Sie den Codeblock von **Zeile \#3** bis **Zeile \#
8** durch den folgenden

on:

workflow_call:

inputs:

node:

required: true

type: string

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image9.jpeg)

6.  Klicken Sie im Fenster **Commit changes** auf **Commit changes.**

![Ein Screenshot eines Screenshots eines neuen Zweigs KI-generierte
Inhalte können falsch sein.](./media/image10.jpeg)

Übung \#3: Erstellen Sie einen Pull Request, um die Änderungen
anzuzeigen, die in der vorherigen Übung vorgenommen wurden

1.  Wählen Sie die Registerkarte **Pull Requests** aus und klicken Sie
    dann auf **New pull request**.

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image11.jpeg)

2.  Legen Sie auf der **Seite “Comparing changes”** **base** als
    **main** und **compare** als **reusable-workflow** fest.

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image12.jpeg)

3.  Klicken Sie auf der Seite **Open a pull request** auf **Create pull
    request.**

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image13.jpeg)

4.  Warten Sie 20 Sekunden, bis Aktionen ausgeführt wurden, und
    überprüfen Sie die Ergebnisse.

Zusammenfassung:

Jetzt haben Sie praktische Erfahrungen darin gesammelt, effiziente,
wiederverwendbare Workflows zu erstellen und diese mithilfe von GitHub
Actions für verschiedene Umgebungen zu optimieren.

