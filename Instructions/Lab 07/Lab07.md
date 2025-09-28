**Lab 07: Codieren mit GitHub Codespaces und Visual Studio Code**

Objektiv:

Stellen Sie sich vor, Sie sind ein Entwickler, der an einem Projekt
arbeitet, das eine in der Cloud gehostete Entwicklungsumgebung
erfordert, um die Zusammenarbeit zu erleichtern und Ihren Workflow zu
optimieren. Um Ihre Produktivität zu steigern und Ihr Entwicklungssetup
effektiver zu verwalten, entscheiden Sie sich für die Verwendung von
GitHub Codespaces mit Visual Studio Code. Mit diesem Setup können Sie
Entwicklungsumgebungen direkt in der Cloud erstellen und anpassen, was
die Zusammenarbeit mit Ihrem Team und die effiziente Verwaltung von
Projektkonfigurationen erleichtert.

In diesem praxisorientierten Lab werden Sie:

- Einen Codespace starten: Erstellen und starten Sie einen GitHub
  Codespace mit vordefinierten Vorlagen.

- Konfigurationen anpassen: Passen Sie Ihre Projektkonfigurationen
  innerhalb des Codespace an Ihre Entwicklungsanforderungen an.

- Codespaces verwalten: Verwalten und navigieren Sie effizient in Ihren
  Codespaces und sorgen Sie so für einen reibungslosen und organisierten
  Entwicklungsprozess.

- Code in das Repository pushen: Üben Sie, Ihre Codeänderungen aus dem
  Codespace in das GitHub-Repository zu pushen, um Ihre Fähigkeit zu
  stärken, Entwicklungsarbeit in die Versionskontrolle zu integrieren.

Übung \#1: Richten Sie ein neues Repository ein und erstellen Sie einen
GitHub Codespace

1.  Melden Sie sich bei Ihrem GitHub-Konto an.

2.  Navigieren Sie zu folgendem Link:
    https://github.com/skills/code-with-codespaces

In diesem Lab erstellen Sie das Repository mit einer öffentlichen
Vorlage "**skills-code-with-codespaces**".

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image1.jpeg)

3.  Wählen Sie im Menü **Use this template** die Option **Create a new
    repository** aus.

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image2.jpeg)

4.  Geben Sie die folgenden Details ein, und wählen Sie **Create
    Repository** aus.

    - Name des Repositorys: **skills-code-with-codespaces**

    - Repository-Typ: **Public**

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image3.jpeg)

5.  Nachdem das Repository erstellt wurde, klicken Sie auf die
    Schaltfläche **Code**.

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image4.jpeg)

6.  Wählen Sie im Popup-Fenster die Registerkarte **Codespaces** aus,
    und klicken Sie dann auf die Schaltfläche **Create codespace on
    main**.

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image5.jpeg)

**Hinweis:** Der Codespace wird in einem neuen Browser-Tab geöffnet.

7.  Im Browser wird ein webbasierter VS Code-Editor angezeigt, und es
    sollte ein Terminal vorhanden sein, wie unten gezeigt.

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image6.jpeg)

8.  Warten Sie 2 Minuten, bis der Codespace (eine virtuelle Maschine)
    vollständig gestartet ist.![Ein Screenshot eines Computers
    KI-generierte Inhalte können falsch sein.](./media/image7.jpeg)

9.  Navigieren Sie zurück zum Repository **skills-code-with-codespaces**
    und klicken Sie auf die Schaltfläche **Code**

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image8.jpeg)

**Hinweis:** Wenn der neu erstellte Codespace nicht geladen wird,
aktualisieren Sie die Seite.

10. Klicken Sie auf die Auslassungspunkte **...** im aktiven
    Codespace\*\*.\*\*

**Hinweis**: Der Name des Codespaces kann in Ihrem Fall unterschiedlich
sein

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image9.jpeg)

11. Wählen Sie im Popupmenü die Option **Open in Visual Studio Code**
    aus.

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image10.jpeg)

12. In einem Popup-Fenster werden Sie um Bestätigung gebeten, um den
    Codespace in der VS-Codeanwendung zu öffnen. Wählen Sie **Open
    Visual Studio Code** aus, um den Codespace zu öffnen.

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image11.jpeg)

13. Sie werden aufgefordert, die GitHub Codespaces-Erweiterung zu
    installieren, Klicken Sie auf **Install extension and open URI**.

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image12.jpeg)

14. Nach der Installation wird ein Popup-Fenster angezeigt, in dem Sie
    nach zusätzlichen Berechtigungen gefragt werden. Klicken Sie auf
    **Authorize** **Visual Studio-Code**

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image13.jpeg)

15. Bestätigen Sie den Zugriff, indem Sie das Passwort für Ihr
    GitHub-Konto eingeben.

![Ein Screenshot eines Anmeldeformulars KI-generierte Inhalte können
falsch sein.](./media/image14.jpeg)

**Hinweis:** Wenn das Popup-Fenster "Berechtigungen für die
Windows-Firewall zulassen" angezeigt wird, erlauben Sie bitte,
fortzufahren.

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image15.jpeg)

Übung \#2: Pushen Sie Code aus dem Codespace in Ihr Repository

1.  Wählen Sie im Codebereich im VS Code-Explorer-Fenster die Datei
    **index.html** aus.

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image16.jpeg)

2.  Ersetzen Sie den h1-Header durch Folgendes:

\<h1\>Hello from the codespace!\</h1\>

3.  Speichern Sie die Datei.

**Hinweis:** Die Datei sollte automatisch gespeichert werden.

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image17.jpeg)

4.  Verwenden Sie das VS Code-Terminal, um die Dateiänderung zu
    bestätigen, indem Sie die folgende Commitnachricht eingeben:

git commit -a -m "Adding hello from the codespace!"

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image18.jpeg)

5.  Übertragen Sie die Änderungen zurück in Ihr Repository. Geben Sie im
    VS Code-Terminal Folgendes ein:

git push

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image19.jpeg)

6.  Der neue Code von VS wurde in Ihr Repository übertragen!

7.  Wechseln Sie zurück zur Startseite Ihres Repositorys und sehen Sie
    die Datei index.html an, um zu überprüfen, ob der neue Code in Ihr
    Repository übertragen wurde.

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image20.jpeg)

8.  Warten Sie etwa 20 Sekunden und aktualisieren Sie dann GitHub
    Actions wird automatisch auf den nächsten Schritt aktualisiert.

Zusammenfassung:

Sie haben GitHub Codespaces und Visual Studio Code jetzt verwendet, um

- Einen GitHub Codespace mithilfe vordefinierter Vorlagen zu erstellen
  und zu starten.

- Pushen von Code in das Repository: Üben Sie, Ihre Codeänderungen aus
  dem Codespace in das GitHub-Repository zu pushen, um Ihre Fähigkeit zu
  stärken, Entwicklungsarbeit in die Versionskontrolle zu integrieren.

