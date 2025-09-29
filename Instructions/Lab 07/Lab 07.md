**Lab 07: Codifica con GitHub Codespaces e Visual Studio Code**

Obiettivo:

Immaginare di essere uno sviluppatore che lavora a un progetto che
richiede un ambiente di sviluppo ospitato nel cloud per facilitare la
collaborazione e semplificare il flusso di lavoro. Per migliorare la
produttività e gestire la configurazione di sviluppo in modo più
efficace, si decide di usare GitHub Codespaces con Visual Studio Code.
Questa configurazione consente di creare e personalizzare gli ambienti
di sviluppo direttamente nel cloud, semplificando la collaborazione con
il team e la gestione efficiente delle configurazioni di progetto.

In questo laboratorio pratico, potrai:

- Avviare uno spazio di codice: Creare e avviare uno spazio di codice
  GitHub utilizzando modelli predefiniti.

- Personalizzare le configurazioni: Personalizzare le configurazioni del
  vostro progetto all'interno dello spazio di codice per adattarle alle
  vostre esigenze di sviluppo.

- Gestire Codespaces: Gestire e navigare in modo efficiente i vostri
  spazi di codice, garantendo un processo di sviluppo fluido e
  organizzato.

- Push del codice nel repository: Esercitati a inviare le modifiche al
  codice dallo spazio di codice al repository GitHub, rafforzando la
  vostra capacità di integrare il lavoro di sviluppo con il controllo
  della versione.

Esercizio \#1: Configurare un nuovo repository e avviare un GitHub
Codespace)

1.  Accedere al vostro account GitHub.

2.  Navigare al seguente link:
    https://github.com/skills/code-with-codespaces

In questo lab creerai il repository utilizzando un modello pubblico
"**skills-code-with-codespaces**".

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image1.jpeg)

3.  Selezionare **Create a new repository **nel menu **Use this
    template**.

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image2.jpeg)

4.  Immettere i dettagli seguenti e selezionare **Create Repository**.

    - Repository name: **skills-code-with-codespaces**

    - Repository type: **Public**

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image3.jpeg)

5.  Una volta creato il repository, fare clic sul pulsante **Code**.

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image4.jpeg)

6.  Selezionare la scheda **Codespaces** nella finestra pop-up, quindi
    fare clic sul pulsante **Create codespace on main**.

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image5.jpeg)

**Nota:** Codespace si aprirà in una nuova scheda del browser.

7.  Il browser visualizzerà un editor basato sul Web di VS Code e
    dovrebbe essere presente un terminale come mostrato di seguito.

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image6.jpeg)

8.  Attendere 2 minuti affinché lo spazio di codice (una macchina
    virtuale) si avvii.

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image7.jpeg)

9.  Tornare al repository **skills-code-with-codespaces** e fare clic
    sul pulsante **Code**

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image8.jpeg)

**Nota:** Se lo spazio di codice appena creato non viene caricato,
aggiornare la pagina.

10. Fare clic sui puntini di sospensione **...** nello spazio di codice
    attivo\*\*.\*\*

**Nota**: Il nome dello spazio di codice potrebbe differire nel vostro
caso

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image9.jpeg)

11. Selezionare **Open in Visual Studio Code **nel menu a comparsa.

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image10.jpeg)

12. Un pop-up chiederà conferma per aprire lo spazio di codice
    nell'applicazione VS code. Selezionare **Open Visual Studio
    Code **per aprire lo spazio di codice.

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image11.jpeg)

13. Ti verrà chiesto di installare l'estensione di GitHub Codespaces,
    fare clic su **Install extension and open URI.**

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image12.jpeg)

14. Una volta installato, vedrai un pop-up che richiede autorizzazioni
    aggiuntive. Fare clic su **Authorize Visual Studio code**

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image13.jpeg)

15. Confermare l'accesso inserendo la password del vostro account
    GitHub.

![Uno screenshot di un modulo di accesso I contenuti generati
dall'intelligenza artificiale potrebbero non essere
corretti.](./media/image14.jpeg)

**Nota:** Se viene visualizzato il pop-up Consentire autorizzazioni
Windows Firewall, consentire di procedere ulteriormente.

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image15.jpeg)

Esercizio \#2: Inviare il codice al repository dallo spazio di codice

1.  Dall'interno dello spazio di codice nella finestra VS Code explorer,
    selezionare il file index.html.

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image16.jpeg)

2.  Sostituire l'intestazione h1 con la seguente:

\<h1\>Hello from the codespace!\</h1\>

3.  Salvare il file.

**Nota:** Il file dovrebbe essere salvato automaticamente.

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image17.jpeg)

4.  Utilizzare il terminale VS Code per eseguire il commit della
    modifica del file immettendo il messaggio di commit seguente:

git commit -a -m "Adding hello from the codespace!"

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image18.jpeg)

5.  Inviare nuovamente le modifiche al repository. Dal terminale VS Code
    immettere:

git push

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image19.jpeg)

6.  Il nuovo codice di VS è stato inserito nel repository.

7.  Tornare alla home page del repository e visualizzare il index.html
    per verificare che il nuovo codice sia stato inviato al repository.

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image20.jpeg)

8.  Attendere circa 20 secondi, quindi aggiorna questo GitHub Actions si
    aggiornerà automaticamente al passaggio successivo.

Sommario:

A questo punto sono stati utilizzati GitHub Codespaces e Visual Studio
Code per

- Creare e avviare un GitHub Codespace utilizzando modelli predefiniti.

- Push del codice nel repository: Esercitati a inviare le modifiche al
  codice dallo spazio di codice al repository GitHub, rafforzando la
  vostra capacità di integrare il lavoro di sviluppo con il controllo
  della versione.
