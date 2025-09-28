**Lab 09: Erstellen von Workflows zur Verwendung von Continuous
Integration (CI) für Ihre Projekte**

Ziele:

Stellen Sie sich vor, Sie arbeiten an einem Softwareprojekt, bei dem die
Einhaltung hoher Qualitätsstandards entscheidend ist. Um
sicherzustellen, dass Ihr Code stabil und fehlerfrei bleibt, entscheiden
Sie sich für die Implementierung von Continuous Integration (CI)
mithilfe von GitHub Actions. CI hilft bei der Automatisierung des
Prozesses des Ausführens von Tests und des Überprüfens der Codequalität
bei jedem Wechsel an der Codebasis. Durch die Erstellung von
CI-Workflows können Sie Markdown-Dateien automatisch linten, Tests
ausführen und sofortiges Feedback zur Codequalität erhalten, um
sicherzustellen, dass Ihr Projekt seine Qualitätsstandards konsistent
erfüllt.

In diesem praxisorientierten Lab werden Sie:

- Erstellen eines Test-Workflows: Richten Sie einen GitHub
  Actions-Workflow ein, der speziell für das Linsen von Markdown-Dateien
  und die Überprüfung auf Formatierungsprobleme entwickelt wurde.

- Konfigurieren und Aktualisieren des Workflows: Üben Sie die
  Konfiguration der Workflowdatei, um die erforderlichen Aufträge und
  Schritte für das automatisierte Linting zu definieren, und
  aktualisieren Sie sie nach Bedarf, um ihre Funktionalität zu
  verbessern.

- Erstellen eines Pull Requests: Integrieren Sie die Änderungen, indem
  Sie einen Pull Request erstellen, mit dem Sie den CI-Workflow testen
  und beobachten können, wie die Qualitätsprüfungen automatisiert
  werden.

- Analysieren Sie die Ergebnisse des CI-Workflows, um zu verstehen, wie
  er Probleme meldet und die Codequalität sicherstellt.

Übung \#1: Erstellen eines neuen Repositorys aus einer öffentlichen
Vorlage

1.  Navigieren Sie zu folgendem Link:
    https://github.com/skills/test-with-actions

In diesem Lab erstellen Sie das Repository mithilfe einer öffentlichen
Vorlage "**skills-test-with-actions**".

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image1.jpeg)

2.  Wählen Sie im Menü **Use this template** die Option **Create a new
    repository** aus.

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image2.jpeg)

3.  Geben Sie die folgenden Details ein, und wählen Sie **Create
    Repository** aus.

    - Name des Repositorys: **skills-test-with-actions**

    - Repository-Typ: **Public**

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image3.jpeg)

Übung \#2: Hinzufügen eines Test-Workflows

1.  Navigieren Sie zur Registerkarte "Actions" in dem Repository, das
    vor einiger Zeit erstellt wurde.

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image4.jpeg)

2.  Wählen Sie in der linken Seitenleiste unter Actions die Option **New
    workflow** aus.

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image5.jpeg)

3.  Navigieren Sie auf der Seite **" Choose a workflow** **"** zu "
    **Simple workflow** " und klicken Sie auf **Configure**.

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image6.jpeg)

4.  Benennen Sie Ihren Workflow auf der nächsten Seite in ci.yml um, und
    aktualisieren Sie den Workflow, indem Sie die letzten beiden
    Schritte löschen.

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image7.jpeg)

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image8.jpeg)

5.  Fügen Sie am Ende des Workflows den folgenden Code hinzu, und
    klicken Sie oben rechts auf **Commit changes**.

6.  \- name: Run markdown lint

7.  run: |

8.  npm install remark-cli remark-preset-lint-consistent

npx remark . --use remark-preset-lint-consistent

**Hinweis:** Stellen Sie sicher, dass der Codeausschnitt, der dem
Workflow hinzugefügt wurde, ordnungsgemäß eingerückt ist

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image9.jpeg)

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image10.jpeg)

9.  Wählen Sie im Fenster **Commit changes** die Option **Create a new
    branch for this commit and start a pull request** aus.

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image11.jpeg)

10. Sobald die Option **Create a new branch for this commit and start a
    pull request** ausgewählt ist, ändert sich das Fenster **" Commit
    changes** " in das Fenster **" Propose Changes** **"**. Klicken Sie
    nun auf **Propose changes**.

![Ein Screenshot eines Computerbildschirms KI-generierte Inhalte können
falsch sein.](./media/image12.jpeg)

11. Klicken Sie auf der nächsten Seite von **Open a pull request** auf
    **Create pull request.**

![Ein Screenshot einer E-Mail KI-generierte Inhalte können falsch
sein.](./media/image13.jpeg)

12. Warten Sie 20 Sekunden, und aktualisieren Sie dann diese Seite, um
    die Ergebnisse zu analysieren.

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image14.jpeg)

Zusammenfassung:

Sie haben nun praktische Erfahrungen mit CI-Praktiken mit GitHub Actions
gesammelt und verbessern so Ihre Fähigkeit, hohe Qualitätsstandards in
Ihren Softwareprojekten zu automatisieren und aufrechtzuerhalten.

