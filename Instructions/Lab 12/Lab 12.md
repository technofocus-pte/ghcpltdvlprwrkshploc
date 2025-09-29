**Lab 12: Creazione di flussi di lavoro di distribuzione con GitHub
Actions e Microsoft Azure**

Obiettivi:

Immaginare di gestire un progetto software con requisiti di
distribuzione complessi che coinvolgono più ambienti, tra cui staging e
produzione. Per semplificare il processo di distribuzione e garantire la
coerenza, si decide di automatizzarlo utilizzando GitHub Actions e
Microsoft Azure. Configurando i flussi di lavoro di distribuzione, è
possibile impostare trigger basati su etichette applicate alle richieste
pull, che gestiranno automaticamente l'avvio degli ambienti, la
distribuzione in staging e l'eliminazione automatica degli ambienti.
Questo approccio consente di mantenere l'efficienza e riduce
l'intervento manuale nella pipeline di distribuzione.

In questo laboratorio pratico, potrai:

- Configurare i flussi di lavoro per creare e configurare
  automaticamente gli ambienti usando le risorse di Azure quando viene
  applicata un'etichetta specifica a una richiesta pull.

- Configurare le attività di distribuzione all'interno dei flussi di
  lavoro per distribuire automaticamente il vostro progetto in un
  ambiente di staging dopo aver ricevuto l'etichetta appropriata.

Esercizio 1: Creare un nuovo repository

1.  Navigare fino al seguente link:
    https://github.com/skills/deploy-to-azure

In questo lab si creerà il repository usando un modello pubblico
**skills-deploy-to-azure**

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image1.jpeg)

2.  Selezionare **Create a new repository **nel menu **Use this
    template**.

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image2.jpeg)

3.  Immettere i dettagli seguenti e selezionare **Create Repository**.

    - Repository name: **skills-deploy-to-azure**

    - Repository type: **Public**

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image3.jpeg)

Esercizio 2: Configurare le autorizzazioni GITHUB_TOKEN

All'inizio di ogni esecuzione del flusso di lavoro, GitHub crea
automaticamente un segreto di GITHUB_TOKEN univoco da utilizzare nel
flusso di lavoro. Dobbiamo assicurarci che questo token disponga delle
autorizzazioni necessarie.

1.  Nella pagina di destinazione del repository appena creato, andare su
    **Settings \> Actions \> General**.

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image4.jpeg)

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image5.jpeg)

2.  Scorrere verso il basso fino a **Workflow permissions **e abilitare
    **Read and write permissions** e fare clic su **Save**.

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image6.jpeg)

**Nota:** Questa operazione è necessaria per il flusso di lavoro per
caricare l'immagine nel registro contenitori.

Esercizio 3: Configurare un trigger basato sulle etichette

1.  Sulla barra di navigazione, andare alla scheda **Actions** 

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image7.jpeg)

2.  Nella pagina **Actions,** fare clic su **New workflow **nel riquadro
    di spostamento a sinistra.

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image8.jpeg)

3.  Nella pagina **Choose a workflow**, cercare \\**simple workflow**\\
    e fare clic su **Configure**

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image9.jpeg)

4.  Assegnare un nome al vostro flusso di lavoro deploy-staging.yml

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image10.jpeg)

5.  Nella pagina dell'editor, modificare il contenuto del file e
    rimuovere tutti i trigger e i processi. Il file risultante apparirà
    come mostrato di seguito.

6.  name: Stage the app

7.  on:

8.  pull_request:

9.  types: \[labeled\]

10. jobs:

11. build:

12. runs-on: ubuntu-latest

if: contains(github.event.pull_request.labels.\*.name, 'stage')

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image11.jpeg)

**Nota:** Assicurati che il frammento di codice aggiunto sia rientrato
correttamente come mostrato nello screenshot

13. Fare clic sul pulsante **Commit changes **in alto a destra della
    pagina.

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image12.jpeg)

14. Nella finestra **Commit Changes,** selezionare **Create a new branch
    for this commit and start a pull request.**

**Nota: Commit changes **alla finestra delle modifiche in **Propose
Changes**.

Assegnare al **nuovo ramo** il nome **staging-workflow **e fare clic su
**Propose changes**.

![Uno screenshot di una chat I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image13.jpeg)

15. Nella pagina successiva di **Open a pull request **fare clic su
    **Create pull request**.

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image14.jpeg)

16. Attendere 20 secondi per l'esecuzione delle azioni e rivedere i
    risultati.

Sommario:

Ora avete acquisito esperienza pratica nell'automazione dei flussi di
lavoro di distribuzione utilizzando GitHub Actions, migliorando
l'efficienza e l'affidabilità del vostro processo di distribuzione.
