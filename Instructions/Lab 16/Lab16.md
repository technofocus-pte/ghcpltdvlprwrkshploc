Lab 16: Entfernen des Commit-Verlaufs aus einem Git-Repository

Objektiv:

Stellen Sie sich vor, Sie sind Teil eines Entwicklungsteams, das an
einem Projekt arbeitet, bei dem vertrauliche Informationen wie
API-Schlüssel oder Datenbankanmeldeinformationen versehentlich in Ihr
Git-Repository übertragen wurden. Versehentliche Commits können mit Git
schwierig zu entfernen sein.

In diesem Lab werden Sie folgende Aufgaben erfüllen:

- Klonen Sie das Repository mit versehentlich übertragenen vertraulichen
  Daten.

- Entfernen/löschen Sie die Datei mit vertraulichen Daten aus dem
  geklonten Repository und führen Sie einen Commit für die Entfernung
  aus.

- Änderungen an GitHub pushen: Laden Sie das aktualisierte Repository
  auf GitHub hoch, um die Änderungen widerzuspiegeln.

### Übung \#1: Erstellen des Repositories mit dem versehentlichen Commit-Verlauf (vertrauliche Daten)

1.  Melden Sie sich bei Ihrem GitHub-Konto an.

2.  Navigieren Sie zu folgendem Link:
    <https://github.com/skills/change-commit-history>

> In diesem Lab erstellen Sie das Repository mit einer öffentlichen
> Vorlage "**skills-change-commit-history**".
>
> ![](./media/image1.png)

3.  Wählen Sie im Menü **Use this template** die Option **Create a new
    repository** aus.

> ![Ein Screenshot eines Computers Beschreibung wird automatisch
> generiert](./media/image2.png)

4.  Geben Sie die folgenden Details ein, und wählen Sie **Create
    Repository** aus.

- Name des Repositorys: **skills-change-commit-history**

- Repository-Typ: **Public**

![](./media/image3.png)

### Übung \# 2: Entfernen/Löschen der Datei (.env im Projektstammverzeichnis) mit vertraulichen Daten

1.  Navigieren Sie auf der Zielseite des geklonten Repositories zu
    **Code\>Local\>HTTPS,** und kopieren Sie die URL.

![](./media/image4.png)

2.  Öffnen Sie Windows Powershell und geben Sie den folgenden Befehl
    ein.

**git clone \<your-repository-url\>**

**Hinweis**: Ersetzen Sie diese URL durch die URL, die Sie in Schritt 1
kopiert haben.

> ![](./media/image5.png)

3.  Wechseln Sie in Ihr Repository-Verzeichnis, und geben Sie den
    folgenden Befehl ein.

**+++cd “C:\Users\Admin\skills-change-commit-history”+++**

**Hinweis**: Ersetzen Sie durch den Repository-Namen

> ![](./media/image6.png)

4.  Führen Sie den folgenden Befehl aus, um .env aus dem
    Stammverzeichnis zu löschen:

**+++git rm .env+++**

> ![Ein Screenshot eines Computerbildschirms Beschreibung wird
> automatisch generiert](./media/image7.png)

5.  Commit für das Entfernen der .env-Datei

**+++git commit -m "remove .env file”+++**

> ![Ein Screenshot eines Computers Beschreibung wird automatisch
> generiert](./media/image8.png)
>
> **Tipp**: Wie entferne ich die .env-Datei vollständig aus dem
> Git-Verlauf und schreibe den gesamten Verlauf mit neuen Commit-Hashes
> neu?
>
> Verwenden Sie die folgenden Befehle, um:

- Die .env-Datei vollständig aus dem Git-Verlauf zu entfernen und den
  gesamten Verlauf neu zu schreiben

- **git filter-branch --force --index-filter 'git rm --cached
  --ignore-unmatch.env' --prune-empty --tag-name-filter cat -- --all**

- Die Entfernung auf GitHub zu pushen

> **git push origin --force –all**

6.  Pushen Sie die Entfernung auf GitHub:

**git push**

> ![Ein Screenshot eines Computerprogramms Beschreibung wird automatisch
> generiert](./media/image9.png)

Zusammenfassung:

Jetzt haben Sie die Bereinigung Ihres Git-Repositories abgeschlossen und
sichergestellt, dass vertrauliche Inhalte nicht im Verlauf des
Repositories verfügbar gemacht werden.

