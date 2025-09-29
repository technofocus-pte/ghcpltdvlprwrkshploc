**Lab 11: Rendere riutilizzabile un flusso di lavoro e utilizzare una
strategia a matrice per eseguire più versioni del nodo**

Obiettivi:

Immaginare di gestire più repository all'interno di un progetto che
condividono flussi di lavoro comuni per attività come la creazione, il
test e la distribuzione. Per evitare la ridondanza e mantenere la
coerenza tra questi repository, si decide di implementare flussi di
lavoro riutilizzabili utilizzando GitHub Actions. Utilizzando il trigger
di chiamata del flusso di lavoro, è possibile centralizzare le
configurazioni del flusso di lavoro, assicurando che le modifiche
vengano apportate in un'unica posizione e applicate automaticamente in
tutti i repository pertinenti. Inoltre, sfrutterai le strategie a
matrice per testare i tuoi flussi di lavoro con più versioni di Node.js,
migliorando la compatibilità e la scalabilità.

In questo laboratorio pratico, potrai:

- Utilizzare il trigger workflow_call per rendere i flussi di lavoro
  riutilizzabili in più repository, riducendo la ridondanza della
  configurazione.

- Passare al repository, aggiornare il file del flusso di lavoro in modo
  che includa il trigger workflow_call ed eseguire il commit delle
  modifiche.

- Creare una richiesta pull per confrontare le modifiche e le eccezioni.

Esercizio \#1: Creare un nuovo repository.

1.  Accedere al seguente link:
    https://github.com/skills/reusable-workflows

In questo lab creerai il repository utilizzando un modello pubblico
"**skills-reusable-workflows**".

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image1.jpeg)

2.  Selezionare **Create a new repository **nel menu **Use this
    template**.

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image2.jpeg)

3.  Immettere i dettagli seguenti e selezionare **Create Repository**.

    - Repository name: **skills-reusable-workflows**

    - Repository type: **Public**

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image3.jpeg)

Esercizio \#2: Aggiungere un trigger workflow_call a un flusso di lavoro

1.  Nella pagina di destinazione del repository appena creato, passare
    alla scheda **Code**\*\*.\*\*

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image4.jpeg)

2.  Nell'elenco a discesa del ramo principale selezionare il ramo
    **reusable-workflow**.

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image5.jpeg)

3.  Dopo aver modificato il ramo, andare alla cartella
    **.github/workflows/**, quindi selezionare il file
    **reusable-workflow.yml**.

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image6.jpeg)

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image7.jpeg)

4.  Nell'editor di file **reusable-workflow.yml** selezionare **Edit in
    place**.

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image8.jpeg)

5.  Sostituire il trigger dell'evento **workflow_dispatch** con il
    trigger dell'evento **workflow_call** e fare clic su **Commit
    changes**.

**Nota**: Sostituire il blocco di codice dalla **Line \#3 **alla **Line
\# 8 **con quello sottostante

on:

workflow_call:

inputs:

node:

required: true

type: string

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image9.jpeg)

6.  Nella finestra **Commit changes **fare clic su **Commit changes.**

![Uno screenshot di uno screenshot di un nuovo ramo I contenuti generati
dall'intelligenza artificiale potrebbero non essere
corretti.](./media/image10.jpeg)

Esercizio \#3: Creare una richiesta pull per visualizzare le modifiche
apportate nell'esercizio precedente

1.  Selezionare la scheda **Pull requests**, quindi fare clic su **New
    pull request**.

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image11.jpeg)

2.  Nella pagina **Comparing changes**, impostare **base** come
    **main **e **compare **come **reusable-workflow.**

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image12.jpeg)

3.  Nella pagina **Open a pull request, **fare clic su **Create pull
    request.**

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image13.jpeg)

4.  Attendere 20 secondi per l'esecuzione delle azioni e rivedere i
    risultati.

Sommario:

Ora avete acquisito esperienza pratica nella creazione di flussi di
lavoro efficienti e riutilizzabili e nell'ottimizzazione per vari
ambienti utilizzando GitHub Actions.
