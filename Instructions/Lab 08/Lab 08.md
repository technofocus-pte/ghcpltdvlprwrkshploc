**Lab 08: Creare un GitHub Action e utilizzarla in un flusso di lavoro**

Obiettivo:

Immaginare di far parte di un team di sviluppo che desidera semplificare
il processo di sviluppo del software automatizzando le attività
ripetitive. Per migliorare l'efficienza, decidi di sfruttare GitHub
Actions, che vi consente di automatizzare attività come test,
distribuzione e revisioni del codice direttamente all'interno del vostro
repository GitHub. Configurando un GitHub Action e integrandola nel
flusso di lavoro, puoi assicurarti che le attività essenziali vengano
eseguite automaticamente, risparmiando tempo e riducendo lo sforzo
manuale.

In questo laboratorio pratico, potrai:

- Configura un file del flusso di lavoro nella directory
  .github/workflows, definendo il contenuto e specificando gli eventi
  che attivano il flusso di lavoro.

- Esercitati ad aggiungere e confermare i file del flusso di lavoro al
  vostro repository per integrare GitHub Actions nel vostro processo di
  sviluppo.

Esercizio \#1: Creare un nuovo repository da un modello pubblico

1.  Accedere al seguente link:
    https://github.com/skills/hello-github-actions

In questo lab creerai il repository utilizzando un modello pubblico
"**skills-hello-github-actions**".

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image1.jpeg)

2.  Selezionare **Create a new repository **nel menu **Use this
    template**.

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image1.jpeg)

3.  Immettere i dettagli seguenti e selezionare **Create Repository**.

    - Repository name: **skills-hello-github-actions**

    - Repository type: **Public**

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image2.jpeg)

Esercizio \#2: Creare un file del flusso di lavoro

1.  Nella pagina di destinazione del repository appena creato, passare
    alla scheda **Pull requests**.

![Uno screenshot di una pagina web I contenuti generati
dall'intelligenza artificiale potrebbero non essere
corretti.](./media/image3.jpeg)

2.  Nella pagina successiva, fare clic sul pulsante **New pull
    request**.

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image4.jpeg)

3.  Nella pagina **Compare changes, **selezionare **base:
    main and compare: welcome-workflow** e fare clic su **Create pull
    request.**

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image5.jpeg)

4.  Nella pagina **Open a pull request, **fare clic su **Create pull
    request**.

![Uno screenshot di una richiesta via email I contenuti generati
dall'intelligenza artificiale potrebbero non essere
corretti.](./media/image6.jpeg)

5.  Passare alla scheda **Code**.

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image7.jpeg)

6.  Nella pagina successiva, dall'**elenco a discesa del ramo
    principale**, fare clic sul ramo **welcome-workflow**.

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image8.jpeg)

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image9.jpeg)

7.  Dopo aver modificato il ramo principale in **welcome-workflow**,
    passare alla cartella **.github/workflows**, quindi selezionare
    **Add file **e fare clic su **Create new file**.

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image10.jpeg)

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image11.jpeg)

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image12.jpeg)

8.  Nella pagina di creazione del file, immettere il nome del file come
    welcome.yml

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image13.jpeg)

9.  Nella pagina dell'editor aggiungere il seguente contenuto al file
    welcome.yml: e fare clic su **Commit changes.**

10. name: Post welcome comment

11. on:

12. pull_request:

13. types: \[opened\]

14. permissions:

pull-requests: write

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image14.jpeg)

15. Nella pagina **Commit changes **fare clic su **commit changes.**

16. Attendi 20 secondi per l'esecuzione delle azioni, quindi aggiorna
    questa opzione e un'azione chiuderà automaticamente questo
    passaggio.

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image15.jpeg)

Sommario:

Ora avete acquisito esperienza pratica nella configurazione e nella
gestione di GitHub Actions, migliorando la vostra capacità di
automatizzare e ottimizzare i flussi di lavoro di sviluppo del software.
