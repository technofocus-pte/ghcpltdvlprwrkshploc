**Lab 09: Creare flussi di lavoro per utilizzare Continuous Integration
(CI) per i progetti**

Obiettivi:

Immaginare di lavorare a un progetto software in cui il mantenimento di
standard di alta qualità è fondamentale. Per garantire che il codice
rimanga affidabile e privo di errori, si decide di implementare
l'integrazione continua (CI) utilizzando GitHub Actions. L'integrazione
continua consente di automatizzare il processo di esecuzione dei test e
di controllo della qualità del codice ogni volta che vengono apportate
modifiche alla base di codice. Creando flussi di lavoro CI, puoi
eseguire automaticamente il linping dei file Markdown, eseguire test e
ricevere feedback immediati sulla qualità del codice, assicurandoti che
il tuo progetto soddisfi costantemente i suoi standard di qualità.

In questo laboratorio pratico, potrai:

- Creare un flusso di lavoro di test: Configura un flusso di lavoro
  GitHub Actions progettato specificamente per lint i file Markdown e
  verificare la presenza di problemi di formattazione.

- Configurare e aggiornare il flusso di lavoro: Esercitati a configurare
  il file del flusso di lavoro per definire i lavori e i passaggi
  necessari per il linting automatizzato e aggiornalo secondo necessità
  per migliorarne la funzionalità.

- Creare una richiesta pull: Integrare le modifiche creando una
  richiesta pull, che vi consente di testare il flusso di lavoro CI e
  osservare come automatizza i controlli di qualità.

- Analizzare i risultati del flusso di lavoro CI per capire in che modo
  segnala i problemi e garantisce la qualità del codice.

Esercizio \#1: Creare un nuovo repository da un modello pubblico

1.  Accedere al seguente link:
    https://github.com/skills/test-with-actions

In questo lab creerai il repository utilizzando un modello pubblico
"**skills-test-with-actions**".

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image1.jpeg)

2.  Selezionare **Create a new repository **nel menu **Use this
    template**.

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image2.jpeg)

3.  Immettere i dettagli seguenti e selezionare **Create Repository**.

    - Repository name: **skills-test-with-actions**

    - Repository type: **Public**

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image3.jpeg)

Esercizio \#2: Aggiungere un flusso di lavoro di test

1.  Passare alla scheda **Actions** nel repository creato qualche tempo
    fa.

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image4.jpeg)

2.  In **Actions** nella barra laterale sinistra, selezionare **New
    workflow**.

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image5.jpeg)

3.  Nella pagina **Choose a workflow**, vai a "**Simple workflow**" e
    fare clic su **Configure**.

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image6.jpeg)

4.  Nella pagina successiva, rinomina il flusso di lavoro come ci.yml e
    aggiornare il flusso di lavoro eliminando gli ultimi due passaggi.

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image7.jpeg)

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image8.jpeg)

5.  Aggiungere il seguente codice alla fine del flusso di lavoro e fare
    clic su **Commit changes **in alto a destra.

6.  \- name: Run markdown lint

7.  run: |

8.  npm install remark-cli remark-preset-lint-consistent

npx remark . --use remark-preset-lint-consistent

**Nota:** Assicurati che lo snippet di codice aggiunto al flusso di
lavoro sia rientrato correttamente

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image9.jpeg)

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image10.jpeg)

9.  Nella finestra **Commit changes **selezionare **Create a new branch
    for this commit and start a pull request.**

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image11.jpeg)

10. Dopo aver selezionato **Create a new branch for this commit and
    start a pull request**, la finestra **Commit changes **viene
    modificata nella finestra **Propose Changes**. Ora fare clic su
    **Propose changes**.

![Uno screenshot dello schermo di un computer I contenuti generati
dall'intelligenza artificiale potrebbero non essere
corretti.](./media/image12.jpeg)

11. Nella pagina successiva di **Open a pull request,** fare clic su
    **Create pull request.**

![Uno screenshot di un'e-mail I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image13.jpeg)

12. Attendere 20 secondi, quindi aggiornare questa pagina per analizzare
    i risultati.

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image14.jpeg)

Sommario:

Ora avete acquisito esperienza pratica con le pratiche di CI utilizzando
GitHub Actions, migliorando la vostra capacità di automatizzare e
mantenere standard di alta qualità nei vostri progetti software.
