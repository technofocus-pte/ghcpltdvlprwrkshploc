**Lab 17: Aktivieren des Secret-Scannings in einem GitHub-Repository und
Commit eines Tokens**

Stellen Sie sich vor, Sie sind ein Softwareentwickler, der an einem
Teamprojekt mit einem gemeinsam genutzten GitHub-Repository arbeitet. Um
sicherzustellen, dass Ihr Code sicher und frei von versehentlichen Lecks
bleibt, entscheiden Sie sich für die Implementierung von Secret
Scanning---eine Funktion, die dabei hilft, vertrauliche Informationen
wie API-Token oder Passwörter zu identifizieren, die möglicherweise
versehentlich in das Repository übernommen wurden.

Objektiv:

In diesem praxisorientierten Lab werden Sie:

1.  Secret Scanning aktivieren: Konfigurieren Sie das Secret Scanning in
    Ihrem GitHub-Repository, um vertrauliche Informationen automatisch
    zu erkennen und zu kennzeichnen.

2.  Einen Token committen: Fügen Sie dem Repository absichtlich ein
    Token oder andere vertrauliche Informationen hinzu, um die
    Wirksamkeit der Secret-Scanning-Funktion zu testen.

Übung \#1: Erstellen Sie ein GitHub-Repository und aktivieren Sie das
Secret Scanning

Aufgabe \#1: Erstellen eines Repositorys mit einer Vorlage

1.  Melden Sie sich bei Ihrem GitHub-Konto an.

2.  Navigieren Sie zu folgendem Link:
    https://github.com/skills/introduction-to-secret-scanning

In diesem Lab erstellen Sie das Repository mithilfe der öffentlichen
Vorlage "**skills-introduction-to-secret-scanning**".

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image1.jpeg)

3.  Wählen Sie im Menü **Use this template** die Option **Create a new
    repository** aus.

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image2.jpeg)

4.  Geben Sie die folgenden Details ein, und wählen Sie **Create
    Repository** aus.

    - Name des Repositorys: **skills-introduction-to-secret-scanning**

    - Repository-Typ: **Public**

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image3.jpeg)

Aufgabe \#2: Aktivieren Sie das Secret Scanning

1.  Wählen Sie auf der Startseite des neu erstellten Repositorys in der
    oberen Navigationsleiste **Settings** aus.

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image4.jpeg)

2.  Wählen Sie in der Seitenleiste im Abschnitt **"Security**" die
    Option "**Code security and analysis**" aus.

**Hinweis**: Sie müssen nach unten scrollen, um das Menü "**Security**"
anzuzeigen

![Ein Screenshot eines Browserfensters KI-generierte Inhalte können
falsch sein.](./media/image5.jpeg)

3.  Scrollen Sie zum Ende der Seite und klicken Sie auf **Enable** für
    Secret Scanning.

**Hinweis:** Wenn die Schaltfläche **Disable** angezeigt wird, bedeutet
dies, dass das Secret Scanning für das Repository bereits aktiviert ist.

![Ein weißer Hintergrund mit schwarzem Text KI-generierte Inhalte können
falsch sein.](./media/image6.jpeg)

Wenn sie noch nicht aktiviert ist, wird die Schaltfläche **Enable** wie
unten angezeigt:

![Ein Screenshot eines Computerfehlers KI-generierte Inhalte können
falsch sein.](./media/image7.jpeg)

**Hinweis:** Wenn das Secret Scanning aktiviert ist, wird eine
E-Mail-Benachrichtigung über Anmeldeinformationen im Repository an die
E-Mail-ID gesendet, die dem Konto zugeordnet ist. Die Token in diesem
Skills-Repository sind inaktiv. Es besteht kein Risiko für die Umgebung.

Nachdem das Secret Scanning in diesem Repository aktiviert ist, führen
wir einen Commit für ein neues Token aus, um zu sehen, wie es
funktioniert.

Übung \#2: Commit für ein Token

In dieser Übung übergeben Sie einen AWS-Schlüssel und eine Zugriffs-ID
an das Repository. Dabei handelt es sich um ein inaktives Token, das
nicht für die Anmeldung bei AWS verwendet werden kann.

1.  Klicken Sie im oberen linken Bereich der Hauptnavigationsleiste auf
    die Registerkarte **Code**, und wählen Sie die Datei
    **credentials.yml** aus.

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image8.jpeg)

2.  Klicken Sie rechts auf die Schaltfläche **Edit**.

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image9.jpeg)

3.  Kopieren Sie den folgenden Text, und fügen Sie ihn unter dem
    vorhandenen Code im Bearbeitungsbereich der
    **credentials.yml**-Datei ein .

4.  default:

5.  aws_access_key_id: AKIAQYLPMN5HNM4OZ56B

6.  aws_secret_access_key: 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

7.  output: json

region: us-east-2

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image10.jpeg)

8.  Klicken Sie auf die Schaltfläche **Commit changes** in der oberen
    rechten Ecke und klicken Sie im Fenster **Commit Changes** erneut
    auf **Commit Changes**.

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image11.jpeg)

**Hinweis:** Nachdem Sie die Änderungen übernommen haben, erhalten Sie
eine Benachrichtigung in Ihrem Postfach, das mit Ihrem GitHub-Konto
verknüpft ist.

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image12.jpeg)

Zusammenfassung:

Jetzt haben Sie ein praktisches Verständnis dafür gewonnen, wie Sie das
Secret Scanning aktivieren und testen, um Ihren Code und Ihre Daten zu
schützen.

