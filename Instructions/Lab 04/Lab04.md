**Lab 04: Überprüfen von Pull Requests und Lösen von Mergekonflikten**

Objektiv:

Stellen Sie sich vor, Sie sind Teil eines Entwicklungsteams, das an
einem Projekt mit mehreren Mitwirkenden arbeitet. Wenn Änderungen
vorgenommen werden, ist es wichtig, diese Änderungen zu überprüfen und
sicherzustellen, dass sich die Arbeit aller reibungslos integriert. Sie
müssen effektiv zusammenarbeiten, indem Sie Pull Requests verwalten und
Merge-Konflikte lösen, um die Integrität des Projekts zu wahren und
Unterbrechungen zu vermeiden.

In diesem praxisorientierten Lab konzentrieren Sie sich auf zwei
wichtige Aspekte der Zusammenarbeit auf GitHub:

- Erstellen eines Pull Requests: Wählen Sie die entsprechenden Branches
  aus, geben Sie einen Titel und eine Beschreibung an und übermitteln
  Sie einen Pull Request, um Änderungen vorzuschlagen.

- Pull Requests überprüfen: Untersuchen Sie die in Pull Requests
  vorgeschlagenen Änderungen und stellen Sie sicher, dass sie den
  Projektstandards entsprechen und für die Integration bereit sind.

- Merge-Konflikte lösen: Üben Sie das Lösen von Konflikten, die
  entstehen, wenn Änderungen in verschiedenen Zweigen dieselben Teile
  einer Datei betreffen, um eine reibungslose Integration und
  Zusammenarbeit zu gewährleisten.

Übung \#1: Erstellen eines Repositorys aus einer Vorlage und Erstellen
eines Pull Requests

Der Pull Request zeigt anderen Personen die Änderungen in Ihrem Branch
an. Dieser Pull Request behält die Änderungen bei, die Sie gerade an
Ihrem Branch vorgenommen haben, und schlägt vor, sie auf den Hauptbranch
anzuwenden.

1.  Melden Sie sich bei Ihrem GitHub-Konto an.

2.  Navigieren Sie zu folgendem Link:
    https://github.com/skills/review-pull-requests

In diesem Lab erstellen Sie das Repository mithilfe einer öffentlichen
Vorlage "**skills-review-pull-requests**".

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image1.jpeg)

3.  Wählen Sie im Menü **Use this template** die Option **Create a new
    repository** aus.

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image2.jpeg)

4.  Geben Sie die folgenden Details ein, und wählen Sie **Create
    Repository** aus.

    - Name des Repositorys: **skills-review-pull-requests**

    - Repository-Typ: **Public**

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image3.jpeg)

5.  Wählen Sie auf der Hauptnavigationsseite die Registerkarte **Pull
    Requests** aus.

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image4.jpeg)

6.  Wählen Sie auf der nächsten Seite **New pull request** aus.

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image5.jpeg)

7.  Auf der Seite **Compare changes**:

    - Wählen Sie in der Dropdown-Liste **"base:"** die Option **"main"**
      aus (standardmäßig ist diese Option ausgewählt)

    - Wählen Sie in der Dropdown-Liste **“compare**:” **update-game**
      aus.

In der Regel ist es notwendig, einige Sekunden zu warten und die Seite
zu aktualisieren, um die Zweige anzuzeigen.

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image6.jpeg)

![Ein Screenshot eines Telefons KI-generierte Inhalte können falsch
sein.](./media/image7.jpeg)

8.  Sobald Sie **update-game** in der Dropdown-Liste **compare:**
    ausgewählt haben, öffnet sich das Fenster **Comparing changes**.
    Klicken Sie auf **Create pull request**.

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image8.jpeg)

9.  Geben Sie auf der **Seite Open a pull request** Folgendes ein:

    - **Fügen Sie einen Titel** für Ihren Pull Request hinzu: Update the
      game over message.

    - **Fügen Sie eine Beschreibung** für Ihren Pull Request hinzu:
      Update the game over message so people know how to play again.

10. Klicken Sie auf **Create pull request**.

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image9.jpeg)

11. Warten Sie ca. 20 Sekunden und aktualisieren Sie dann diese Seite.
    GitHub Actions wird automatisch auf den nächsten Schritt
    aktualisiert.

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image10.jpeg)

Übung \#2: Aktualisieren eines Pull Requests und Beheben von
Merge-Konflikten

1.  Navigieren Sie zu folgendem Link:
    https://github.com/skills/resolve-merge-conflicts

In diesem Lab erstellen Sie das Repository mithilfe einer öffentlichen
Vorlage "**skills-resolve-merge-conflicts**".

![Ein Screenshot einer Webseite KI-generierte Inhalte können falsch
sein.](./media/image11.jpeg)

2.  Wählen Sie im Menü **Use this template** die Option **Create a new
    repository** aus.

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image12.jpeg)

3.  Geben Sie die folgenden Details ein, und wählen Sie **Create
    Repository** aus.

    - Name des Repositorys: **skills-resolve-merge-conflicts**

    - Repository-Typ: **Public**

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image13.jpeg)

4.  Nachdem das Repository erstellt wurde, wählen Sie in der
    Hauptnavigationsleiste die Registerkarte **Pull Request** aus.

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image14.jpeg)

5.  Klicken Sie auf die Schaltfläche **New pull request**.

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image15.jpeg)

6.  Erstellen Sie einen Pull Request, indem Sie Folgendes auswählen:

    - **my-resume** als Head-Branch und

    - **main** als Compare-Branch.

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image16.jpeg)

![Ein Screenshot eines Chats KI-generierte Inhalte können falsch
sein.](./media/image17.jpeg)

7.  Klicken Sie auf die Schaltfläche **Create pull request**

8.  Geben Sie auf der Seite **Open a pull request** den Titel als
    “Resolving merge conflicts” ein Und klicken Sie auf **Create pull
    request.**

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image18.jpeg)

9.  Warten Sie 20 Sekunden, bis GitHub Actions automatisch aktualisiert
    wird und auf der Seite ggf. Details zu Konflikten angezeigt werden.

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image19.jpeg)

10. Klicken Sie auf **Resolve conflicts**, um fortzufahren.

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image20.jpeg)

11. Überprüfen Sie die Konflikte, und lösen Sie sie.

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image21.jpeg)

12. Löschen Sie in dieser Übung den Einzelpostenkonflikt und klicken Sie
    auf die Schaltfläche **Mark as resolved**.

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image22.jpeg)

13. Klicken Sie auf die Schaltfläche **Commit merge** und überprüfen Sie
    das Meldungsfeld (Heads-up Message Box).

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image23.jpeg)

14. Klicken Sie auf **I understand, continue updating main.** Sie sehen
    die endgültigen Prüfergebnisse\*\*.\*\*

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image24.jpeg)

**Zusammenfassung:**

Jetzt haben Sie das Erstellen und Überprüfen von Pull Requests für
Konflikte und das Lösen von Konflikten abgeschlossen, wesentliche
Fähigkeiten für effektive Teamarbeit und Projektmanagement auf GitHub.

