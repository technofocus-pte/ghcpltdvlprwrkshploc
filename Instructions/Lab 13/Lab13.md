**Lab 13: Schreiben einer GitHub-JavaScript-Aktion und Automatisieren
von benutzerdefinierten Aufgaben, die speziell auf Ihren Workflow
zugeschnitten sind**

Ziele:

Stellen Sie sich vor, Sie haben die Aufgabe, eine benutzerdefinierte
GitHub-Action zu erstellen, um bestimmte Aufgaben innerhalb Ihres
Workflows zu automatisieren. Um zu beginnen, müssen Sie eine
Entwicklungsumgebung zum Schreiben und Testen Ihrer JavaScript-Aktion
einrichten. Dazu gehören die Initialisierung eines neuen
JavaScript-Projekts, die Konfiguration Ihrer Projektstruktur und die
Installation der erforderlichen Abhängigkeiten. Indem Sie die Schritte
in diesem Lab befolgen, schaffen Sie eine solide Grundlage für die
Entwicklung Ihrer GitHub Action, die es Ihnen ermöglicht, eine
Automatisierung zu erstellen, die auf die Anforderungen Ihres Projekts
zugeschnitten ist.

In diesem praxisorientierten Lab werden Sie:

- Klonen des Repositorys: Klonen Sie das bereitgestellte Repository auf
  Ihren lokalen Computer, um den Entwicklungsprozess zu starten.

- Navigieren Sie zum Projektordner: Wechseln Sie zum geklonten
  Repository-Ordner, in dem Sie Ihre Aktion einrichten möchten.

- Aktionsordner erstellen: Richten Sie einen neuen Ordner innerhalb des
  Repositorys speziell für Ihre Aktionsdateien ein.

- npm-Projekt initialisieren: Initialisieren Sie ein neues npm-Projekt
  im Aktionsordner, um Abhängigkeiten und Konfiguration zu verwalten.

- Abhängigkeiten installieren: Verwenden Sie npm, um die erforderlichen
  Abhängigkeiten zu installieren, die für die Entwicklung Ihrer
  GitHub-JavaScript-Aktion erforderlich sind.

- Vorbereiten der Aktionsentwicklung: Konfigurieren Sie Ihre
  Projektumgebung, um mit dem Schreiben und Testen Ihrer
  benutzerdefinierten GitHub-JavaScript-Aktion zu beginnen.

Übung: 1 Ein neues Repository erstellen

1.  Navigieren Sie zu folgendem Link:
    https://github.com/skills/write-javascript-actions

In diesem Lab erstellen Sie das Repository mit einer öffentlichen
Vorlage **skills-write-javascript-actions**

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image1.jpeg)

2.  Wählen Sie im Menü **Use this template** die Option **Create a new
    repository** aus.

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image2.jpeg)

3.  Geben Sie die folgenden Details ein, und wählen Sie **Create
    Repository** aus.

    - Name des Repositorys: **skills-write-javascript-actions**

    - Repository-Typ: **Public**

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image3.jpeg)

Übung \#2: Initialisieren eines neuen JavaScript-Projekts

Nachdem Sie die erforderlichen Tools lokal installiert haben, führen Sie
die folgenden Schritte aus, um mit der Erstellung Ihrer ersten Aktion zu
beginnen.

1.  Klicken Sie auf der Zielseite des Repositorys
    **write-javascript-actions** auf die Schaltfläche **Code** (die
    grüne) und kopieren Sie die HTTPS-URL auf der Registerkarte
    **Local**.

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image4.jpeg)

2.  Öffnen Sie nun **Command prompt**, und klonen Sie Ihr
    Skills-Repository auf den lokalen Computer:

git clone \<this repository URL\>.git

![Ein Screenshot eines Computerprogramms KI-generierte Inhalte können
falsch sein.](./media/image5.jpeg)

**Hinweis:** Normalerweise wird es in den folgenden Pfad geklont:
"**C:\Users\Admin\skills-write-javascript-actions**"

3.  Navigieren Sie zu dem Ordner, den Sie gerade geklont haben:

cd C:\Users\Admin\skills-write-javascript-actions

![Ein Screenshot eines Computerprogramms KI-generierte Inhalte können
falsch sein.](./media/image6.jpeg)

4.  Wir werden den Zweig namens main verwenden.

git switch main

![Ein Screenshot eines Computerprogramms KI-generierte Inhalte können
falsch sein.](./media/image7.jpeg)

5.  Erstellen Sie einen neuen Ordner für unsere Aktionsdateien:

mkdir -p .github\actions\joke-action

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image8.jpeg)

6.  Navigieren Sie zu dem joke-action-Ordner, den Sie gerade erstellt
    haben:

cd .github/actions/joke-action

![Ein Screenshot eines Computerprogramms KI-generierte Inhalte können
falsch sein.](./media/image9.jpeg)

7.  Initialisieren Sie ein neues Projekt:

npm init -y

![Ein Screenshot eines Computerprogramms KI-generierte Inhalte können
falsch sein.](./media/image10.jpeg)

8.  Installieren Sie die Abhängigkeiten request, request-promise und
    \\actions/core mithilfe von npm aus dem GitHub ToolKit
    (https://github.com/actions/toolkit):

Npm install -save request request-promise @actions/core

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image11.jpeg)

9.  Committen Sie diese neu hinzugefügten Dateien, wir werden die
    Notwendigkeit beseitigen, node_modules in einem späteren Schritt
    hochzuladen:

git add . && git commit -m "add project dependencies"

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image12.jpeg)

**Hinweis:** Wenn Sie aufgefordert werden, die E-Mail-Adresse und den
Benutzernamen einzugeben, geben Sie den folgenden Befehl mit den
ersetzten Details ein.

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image13.jpeg)

git config --global user.email "your_email@example.com"

git config --global user.name "Your Name"

**Hinweis**: Ersetzen Sie durch Ihre Daten.

10. Pushen Sie Ihre Änderungen in Ihr Repository: Geben Sie den
    folgenden Befehl ein und melden Sie sich an

git push

![Ein Computerbildschirm mit weißem Text KI-generierte Inhalte können
falsch sein.](./media/image14.jpeg)

**Hinweis:** Wenn Sie zur Autorisierung aufgefordert werden, melden Sie
sich bei Ihrem GitHub-Konto an und setzen Sie den Vorgang fort.![Ein
Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image15.jpeg)

![Ein Screenshot eines Anmeldeformulars KI-generierte Inhalte können
falsch sein.](./media/image16.jpeg)

![Ein Screenshot eines Computerfehlers KI-generierte Inhalte können
falsch sein.](./media/image17.jpeg)

11. Warten Sie etwa 20 Sekunden, während GitHub Actions die Seite
    automatisch für die weitere Verarbeitung aktualisiert.

Zusammenfassung:

Sie haben nun eine robuste Entwicklungsumgebung für die Erstellung und
Verwaltung Ihrer GitHub-JavaScript-Aktion eingerichtet und damit die
Voraussetzungen für die Automatisierung und Verbesserung Ihrer Workflows
geschaffen.

