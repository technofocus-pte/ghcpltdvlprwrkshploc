**Lab 14: Sichern Sie die Lieferkette Ihres Repositories**

Ziele:

Stellen Sie sich vor, Sie sind für die Aufrechterhaltung der Sicherheit
eines Softwareprojekts verantwortlich, das auf verschiedenen
Abhängigkeiten von Drittanbietern beruht. Um die Integrität und
Sicherheit der Lieferkette Ihres Projekts zu gewährleisten, ist es
entscheidend, diese Abhängigkeiten zu verstehen und effektiv zu
verwalten. Dazu gehört die Identifizierung potenzieller Schwachstellen
in Ihren Abhängigkeiten und das Anwenden notwendiger Patches, um Ihr
Projekt zu schützen. In diesem Lab erfahren Sie, wie Sie die
**Dependency Graph**-Funktion von GitHub verwenden, um Ihre
Abhängigkeiten zu überwachen und zu überprüfen und sicherzustellen, dass
Ihr Projekt sicher und aktuell bleibt.

In diesem praxisorientierten Lab werden Sie:

- Dependency Graph aktivieren: Aktivieren und überprüfen Sie die
  Funktion für das Dependency Graph in Ihren Repository-Einstellungen,
  um die Abhängigkeiten Ihres Projekts zu visualisieren.

- Neue Abhängigkeit hinzufügen: Fügen Sie Ihrem Projekt eine neue
  Abhängigkeit hinzu und stellen Sie sicher, dass sie ordnungsgemäß
  integriert ist.

- Dependency Graph überprüfen: Verwenden Sie das Dependency Graph, um zu
  überprüfen und zu bestätigen, dass die neue Abhängigkeit korrekt
  widergespiegelt und überwacht wird.

Übung 01: Erstellen eines neuen Repositorys

1.  Navigieren Sie zu folgendem Link:
    https://github.com/skills/secure-repository-supply-chain

In diesem Lab erstellen Sie das Repository mithilfe einer öffentlichen
Vorlage **skills-secure-repository-supply-chain**

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image1.jpeg)

2.  Wählen Sie im Menü **Use this template** die Option **Create a new
    repository** aus.

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image2.jpeg)

3.  Geben Sie die folgenden Details ein, und wählen Sie **Create
    Repository** aus.

    - Name des Repositorys: **skills-secure-repository-supply-chain**

    - Repository-Typ: **Public**

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image3.jpeg)

Übung 02: Überprüfen, ob das Dependency Graph aktiviert ist

1.  Navigieren Sie auf der Landingpage des neu erstellten Repositorys
    zur Registerkarte **Settings**.

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image4.jpeg)

2.  Wählen Sie auf der Seite **Settings** die Option **Code security and
    analysis** aus, die unter **Security** verfügbar ist**.**

![Ein Screenshot eines allgemeinen Logins KI-generierte Inhalte können
falsch sein.](./media/image5.jpeg)

3.  Überprüfen/aktivieren Sie das Dependency Graph. (Wenn das Repository
    privat ist, aktivieren Sie es hier. Wenn das Repository öffentlich
    ist, ist es standardmäßig aktiviert.)

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image6.jpeg)

Übung 03: Hinzufügen einer neuen Abhängigkeit und Anzeigen Ihres
Dependency Graph

1.  Navigieren Sie zur Registerkarte **Code,** und suchen Sie den Ordner
    **code/src/AttendeeSite**.

**Hinweis:** Sie können entweder zum Ordner navigieren oder die **Go to
file**-Suche mit dem Pfad code/src/AttendeeSite verwenden.

![Ein Screenshot einer Webseite KI-generierte Inhalte können falsch
sein.](./media/image7.jpeg)

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image8.jpeg)

2.  Öffnen Sie die **package-lock.json**-Datei.

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image9.jpeg)

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image10.jpeg)

3.  Fügen Sie den folgenden Codeausschnitt zwischen Zeile \# 14 und
    Zeile \# 15 ein

4.  "follow-redirects": {

5.  "version": "1.14.1",

6.  "resolved":

7.  "https://registry.npmjs.org/follow-redirects/-/follow-redirects-1.14.1.tgz",

8.  "integrity":

9.  "sha512-HWqDgT7ZEkqRzBvc2s64vSZ/hfOceEol3ac/7tKwzuvEyWx3/4UegXh5oBOIotkGsObyk3xznnSRVADBgWSQVg=="

},

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image11.jpeg)

**Hinweis:** Bitte stellen Sie sicher, dass das hinzugefügte
Code-Snippet richtig eingerückt ist, wie im Screenshot gezeigt

10. Klicken Sie oben rechts auf **Commit changes**.

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image12.jpeg)

11. Klicken Sie in der Hauptnavigationsleiste auf die **Registerkarte
    Insights**.

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image13.jpeg)

12. Klicken Sie im linken Navigationsbereich auf das **Dependency
    Graph.**

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image14.jpeg)

13. Überprüfen Sie alle neuen Abhängigkeiten im Hub "Dependencies".

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image15.jpeg)

14. Suchen Sie nach follow-redirects und überprüfen Sie die neue
    Abhängigkeit(Dependency), die Sie gerade hinzugefügt haben.

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image16.jpeg)

Zusammenfassung:

Sie haben nun wertvolle Einblicke in das Management der Abhängigkeiten
Ihres Projekts und die Sicherung der Lieferkette Ihres Repositorys
gewonnen, die es Ihnen ermöglichen, Sicherheitsrisiken proaktiv
anzugehen und zu mindern.

