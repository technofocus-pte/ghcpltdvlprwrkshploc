**Lab 13: Scrivere GitHub JavaScript Action e automatizza le attività
personalizzate uniche per il vostro flusso di lavoro**

Obiettivi:

Immaginare di avere il compito di creare un'azione GitHub personalizzata
per automatizzare attività specifiche all'interno del tuo flusso di
lavoro. Per iniziare, è necessario configurare un ambiente di sviluppo
per la scrittura e il test dell'azione JavaScript. Ciò comporta
l'inizializzazione di un nuovo progetto JavaScript, la configurazione
della struttura del progetto e l'installazione delle dipendenze
necessarie. Seguendo i passaggi di questo lab, creerai una solida base
per lo sviluppo della vostra GitHub Action, consentendoti di creare
un'automazione su misura per le esigenze del vostro progetto.

In questo laboratorio pratico, potrai:

- Clonare il repository: clonare il repository fornito sul vostro
  computer locale per avviare il processo di sviluppo.

- Passare alla cartella del progetto: Passare alla cartella del
  repository clonato in cui imposterai l'azione.

- Creare cartella azioni: Configurare una nuova cartella all'interno del
  repository specifica per i file delle azioni.

- Inizializzare progetto npm: InizializzaRE un nuovo progetto npm nella
  cartella delle azioni per gestire le dipendenze e la configurazione.

- InstallaRE dipendenze: Utilizzare npm per installare le dipendenze
  necessarie per lo sviluppo dell'azione JavaScript GitHub.

- Prepararsi per lo sviluppo dell'azione: configurare l'ambiente del
  progetto per iniziare a scrivere e testare l'azione JavaScript GitHub
  personalizzata.

Esercizio: 1 Creare un nuovo repository

1.  Accedere al seguente link:
    https://github.com/skills/write-javascript-actions

In questo laboratorio creerai il repository utilizzando un modello
pubblico **skills-write-javascript-actions**

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image1.jpeg)

2.  Selezionare **Create a new repository **nel menu **Use this
    template**.

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image2.jpeg)

3.  Immettere i dettagli seguenti e selezionare **Create Repository**.

    - Repository name: **skills-write-javascript-actions**

    - Repository type: **Public**

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image3.jpeg)

Esercizio \#2: Inizializzare un nuovo progetto JavaScript

Dopo aver installato gli strumenti necessari in locale, seguire questi
passaggi per iniziare a creare la vostra prima azione.

1.  Nella pagina di destinazione del repository
    **write-javascript-actions**, fare clic sul pulsante **Code**
    (quello di colore verde) e copiare l'URL HTTPS nella scheda
    **Local**.

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image4.jpeg)

2.  Ora aprire **Command prompt **e clonare il vostro repository di
    abilità sul computer locale:

git clone \<this repository URL\>.git

![Uno screenshot di un programma per computer I contenuti generati
dall'intelligenza artificiale potrebbero non essere
corretti.](./media/image5.jpeg)

**Nota:** Di solito viene clonato nel seguente percorso
"**C:\Users\Admin\skills-write-javascript-actions**"

3.  Andare alla cartella che hai appena clonato:

cd C:\Users\Admin\skills-write-javascript-actions

![Uno screenshot di un programma per computer I contenuti generati
dall'intelligenza artificiale potrebbero non essere
corretti.](./media/image6.jpeg)

4.  Useremo il ramo chiamato main.

git switch main

![Uno screenshot di un programma per computer I contenuti generati
dall'intelligenza artificiale potrebbero non essere
corretti.](./media/image7.jpeg)

5.  Creare una nuova cartella per i nostri file di azioni:

mkdir -p .github\actions\joke-action

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image8.jpeg)

6.  Andare alla cartella joke-action che hai appena creato:

cd .github/actions/joke-action

![Uno screenshot di un programma per computer I contenuti generati
dall'intelligenza artificiale potrebbero non essere
corretti.](./media/image9.jpeg)

7.  Inizializzare un nuovo progetto:

npm init -y

![Uno screenshot di un programma per computer I contenuti generati
dall'intelligenza artificiale potrebbero non essere
corretti.](./media/image10.jpeg)

8.  Installare le dipendenze request, request-promise e \\actions/core
    utilizzando npm dal GitHub ToolKit
    (https://github.com/actions/toolkit):

Npm install -save request request-promise @actions/core

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image11.jpeg)

9.  Eseguire il commit dei file appena aggiunti, rimuoveremo la
    necessità di caricare node_modules in un passaggio successivo:

git add . && git commit -m "add project dependencies"

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image12.jpeg)

**Nota:** Se viene richiesto di inserire l'e-mail dell'utente e il nome
utente, immettere il comando seguente con i dettagli sostituiti.

![Schermata di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image13.jpeg)

git config --global user.email "your_email@example.com"

git config --global user.name "Your Name"

**Nota**: Sostituire con i vostri dati.

10. Inviare le modifiche al vostro repository: Inserire il comando
    seguente e accedere

git push

![Schermo di un computer con testo bianco I contenuti generati
dall'intelligenza artificiale potrebbero non essere
corretti.](./media/image14.jpeg)

**Nota:** Quando viene richiesto di autorizzare, accedere all'account
GitHub e continuare il processo.

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image15.jpeg)

![Uno screenshot di un modulo di accesso I contenuti generati
dall'intelligenza artificiale potrebbero non essere
corretti.](./media/image16.jpeg)

![Uno screenshot di un errore del computer I contenuti generati
dall'intelligenza artificiale potrebbero non essere
corretti.](./media/image17.jpeg)

11. Attendere circa 20 secondi mentre GitHub Actions aggiorna
    automaticamente la pagina per un'ulteriore elaborazione.

Sommario:

A questo punto è stato creato un ambiente di sviluppo affidabile per la
creazione e la gestione dell'azione JavaScript GitHub, ponendo le basi
per l'automazione e il miglioramento dei flussi di lavoro.
