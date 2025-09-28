**Lab 03: Erstellen Sie Ihr Online-Portfolio mit GitHub Pages und
Jekyll**

Objektiv:

Stellen Sie sich vor, Sie sind ein angehender Softwareentwickler in
einem Tech-Startup und möchten Ihre Projekte, Fähigkeiten und
Erfahrungen in einem Online-Portfolio präsentieren. Sie möchten eine
professionelle Plattform, um Ihre Arbeit zu präsentieren, daher
entscheiden Sie sich dafür, eine persönliche Website oder einen Blog mit
GitHub Pages zu erstellen. Diese Plattform ermöglicht es Ihnen,
GitHub-Repositories zu nutzen, um Ihre Website einfach zu
veröffentlichen und zu pflegen.

In diesem praxisorientierten Lab werden Sie:

- Erstellen Sie ein GitHub-Repository: Richten Sie ein neues Repository
  ein, das als Grundlage für Ihre persönliche Website dient.

- Aktivieren Sie GitHub Pages: Konfigurieren Sie GitHub Pages so, dass
  Ihre Website direkt aus Ihrem Repository gehostet wird.

- Stellen Sie Ihre erste Website mit Jekyll bereit: Verwenden Sie
  Jekyll, einen beliebten Generator für statische Websites, um mit
  minimalem Aufwand eine professionell aussehende Website zu erstellen
  und bereitzustellen.

Übung \#1: Erstellen eines Repositorys aus einer Vorlage

1.  Melden Sie sich bei Ihrem GitHub-Konto an.

2.  Navigieren Sie zu folgendem Link:
    https://github.com/skills/github-pages

In diesem Lab erstellen Sie das Repository mit einer öffentlichen
Vorlage "**skills-github-pages**".

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image1.jpeg)

3.  Wählen Sie im Menü **Use this template** die Option **Create a new
    repository** aus .

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image2.jpeg)

4.  Geben Sie die folgenden Details ein, und wählen Sie **Create
    Repository** aus.

    - Name des Repositorys: **skills-github-pages**

    - Repository-Typ: **Public**

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image3.jpeg)

Übung \#2: Aktivieren von GitHub Pages

1.  Nachdem das Repository erstellt wurde, navigieren Sie zur
    Startseite. Klicken Sie im Hauptnavigationsbereich auf das Symbol
    **Settings**.

![Ein Screenshot einer Webseite KI-generierte Inhalte können falsch
sein.](./media/image4.jpeg)

2.  Scrollen Sie auf der Einstellungsseite nach unten zu “Code und
    Automation” und klicken Sie auf **Pages.**

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image5.jpeg)

3.  Stellen Sie auf den GitHub-Seiten sicher, dass " **Deploy from a
    branch** " aus dem Dropdownmenü **"Source**" ausgewählt ist, und
    wählen Sie dann im Dropdownmenü **"Branch"** die Option "**main**"
    aus.

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image6.jpeg)

4.  Klicken Sie auf die Schaltfläche **Save**, um fortzufahren.

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image7.jpeg)

5.  Der GitHub Pages-Quellcode wird gespeichert. Warten Sie etwa eine
    Minute und aktualisieren Sie dann diese Seite. GitHub Actions wird
    automatisch auf den nächsten Schritt aktualisiert.

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image8.jpeg)

6.  Ihre Website ist jetzt live.

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image9.jpeg)

7.  Klicken Sie auf die Schaltfläche “Visit Site”, um Ihre Website
    anzuzeigen. Sie haben GitHub Pages aktiviert.

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image10.jpeg)

Übung \#3: Bereitstellen Ihrer Website mit Jekyll

Sie arbeiten in einem Zweig, **my-pages**, um diese Website großartig
aussehen zu lassen. In diesem Lab werden wir ein blogfähiges Theme
"minima" verwenden.

Jekyll verwendet eine Datei mit dem Titel **\_config.yml**, um
Einstellungen für Ihre Website, Ihr Theme und wiederverwendbare Inhalte
wie Ihren Website-Titel und Ihr GitHub-Handle zu speichern.

1.  Wählen Sie die Registerkarte **Code** Ihres Repositorys aus

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image11.jpeg)

2.  Erweitern Sie den **main**-Zweig und wählen Sie **my-pages** aus.

![Ein Screenshot einer Webseite KI-generierte Inhalte können falsch
sein.](./media/image12.jpeg)

Navigieren Sie im Zweig **my-pages** zur Datei **\_config.yml**

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image13.jpeg)

3.  Öffnen Sie den Dateieditor in der oberen rechten Ecke.

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image14.jpeg)

4.  Fügen Sie ein Theme hinzu: Legen Sie es auf **minima** fest, damit
    es in der **\_config.yml** Datei wie folgt angezeigt wird:

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image15.jpeg)

5.  Klicken Sie auf die Schaltfläche **Commit Changes**, um die
    Änderungen zu speichern.

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image16.jpeg)

**Hinweis:** Warten Sie etwa eine Minute und aktualisieren Sie dann
diese Seite. GitHub Actions wird automatisch auf den nächsten Schritt
aktualisiert.

6.  Um die aktualisierte Website zu überprüfen, klicken Sie unter GitHub
    Pages auf die Schaltfläche **Visit site**.

![Ein Screenshot einer Webseite KI-generierte Inhalte können falsch
sein.](./media/image17.jpeg)

7.  Das ausgewählte Theme wird angewendet. Sie können die anderen
    Konfigurationsvariablen wie title:, author: und description: weiter
    ändern, um Ihre Website weiter anzupassen

![Ein Screenshot eines Computers KI-generierte Inhalte können falsch
sein.](./media/image18.jpeg)

Zusammenfassung:

Sie haben nun eine Website mit GitHub-Pages erstellt und ein Theme
angewendet. Sie können diese Erfahrung nutzen, um eine Live-Website zu
erstellen, auf der Sie Ihre Softwareentwicklungsreise kontinuierlich
aktualisieren und präsentieren können, um Arbeitgebern, Mitwirkenden und
der Tech-Community zu erleichtern, Ihre Arbeit und Fähigkeiten zu sehen.
