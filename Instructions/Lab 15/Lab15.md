**Lab 15: Aktivieren von CodeQL zum Sichern des Quellcodes**

Objektiv:

Stellen Sie sich vor, Sie sind ein Softwareentwickler, der an einem
kritischen Projekt für Ihr Unternehmen arbeitet, bei dem die
Gewährleistung der Sicherheit Ihrer Anwendung oberste Priorität hat.
Angesichts der wachsenden Besorgnis über Cyberbedrohungen und
Datenschutzverletzungen ist es wichtig, sicherzustellen, dass Ihr Code
frei von Schwachstellen und unsicheren Codierungspraktiken ist. In
dieser praktischen Übung aktivieren Sie GitHub Code Scanning, um Ihren
Quellcode automatisch auf potenzielle Sicherheitsprobleme zu überprüfen.

In dieser praktischen Übung aktivieren Sie GitHub Code Scanning, um
Ihren Quellcode automatisch auf potenzielle Sicherheitsprobleme zu
überprüfen.

Übung \#1: Erstellen eines neuen Repositorys aus einer öffentlichen
Vorlage

1.  Melden Sie sich bei Ihrem GitHub-Konto an.

2.  Navigieren Sie zu folgendem Link:
    https://github.com/skills/introduction-to-codeql

In diesem Lab erstellen Sie das Repository mit einer öffentlichen
Vorlage "**skills-introduction-to-codeql**".

![](./media/image1.jpeg)

3.  Wählen Sie im Menü **Use this template** die Option **Create a new
    repository** aus.

![](./media/image2.jpeg)

4.  Geben Sie die folgenden Details ein, und wählen Sie **Create
    Repository** aus.

    - Name des Repositorys:**skills-introduction-to-codeql**

    - Repository-Typ: **Public**

![](./media/image3.jpeg)

Übung \#2: Aktivieren von Code-Scanning mit CodeQL

1.  Navigieren Sie auf der Landingpage des neu erstellten Repositorys
    zur Registerkarte **Settings**.

![](./media/image4.jpeg)

2.  Wählen Sie im Abschnitt **Security** in der linken Seitenleiste die
    Option **Code security and analysis** aus.

![](./media/image5.jpeg)

3.  Scrollen Sie nach unten zum Abschnitt Code-Scanning, klicken Sie auf
    das Dropdown-Menü **"Setup"** und wählen Sie **"Default**" aus.

![](./media/image6.jpeg)

4.  Wählen Sie die folgenden Optionen aus und klicken Sie auf **Enable
    CodeQL**

    - Zu analysierende Sprachen: Dies sind die Sprachen, die von CodeQL
      gescannt werden. In diesem Fall scannen wir in Python.

    - Query-Suites: CodeQL-Abfragen werden in Paketen verpackt, die als
      "Suites" bezeichnet werden. In diesem Abschnitt können Sie
      auswählen, welche Abfrage-Suite verwendet werden soll. Wir
      belassen diese Einstellung als Standard für diese Übung.

    - Ereignisse(Events): Dieser Abschnitt teilt CodeQL mit, wann
      gescannt werden soll. In diesem Fall ist es so eingestellt, dass
      jeder Pull Request an den main-Zweig gescannt wird.

![](./media/image7.jpeg)

5.  Warten Sie etwa 20 Sekunden und aktualisieren Sie dann diese Seite,
    um fortzufahren.

![](./media/image8.jpeg)

Zusammenfassung:

Jetzt haben Sie GitHub Code Scanning aktiviert, um Ihren Quellcode
automatisch auf potenzielle Sicherheitsprobleme zu überprüfen.

