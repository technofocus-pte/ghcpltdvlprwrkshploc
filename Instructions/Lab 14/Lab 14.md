**Lab 14: Proteggere la supply chain del vostro repository**

Obiettivi:

Immaginare di essere responsabile del mantenimento della sicurezza di un
progetto software che si basa su varie dipendenze di terze parti. Per
garantire l'integrità e la sicurezza della supply chain del vostro
progetto, è fondamentale comprendere e gestire queste dipendenze in modo
efficace. Ciò comporta l'identificazione di potenziali vulnerabilità
all'interno delle dipendenze e l'applicazione delle patch necessarie per
proteggere il progetto. In questo lab imparerai come utilizzare la
funzione del grafico delle dipendenze di GitHub per monitorare e
rivedere le vostre dipendenze, assicurandoti che il vostro progetto
rimanga sicuro e aggiornato.

In questo laboratorio pratico, potrai:

- Abilitare Dependency Graph: Abilitare e verificare la funzione del
  grafico delle dipendenze nelle impostazioni del repository per
  visualizzare le dipendenze del vostro progetto.

- Aggiungere una nuova dipendenza: Aggiungere una nuova dipendenza al
  vostro progetto e assicurati che sia integrata correttamente.

- Esaminare il Dependency Graph: Utilizzare il grafico delle dipendenze
  per esaminare e confermare che la nuova dipendenza venga riflessa e
  monitorata correttamente.

Esercizio 01: Creare un nuovo repository

1.  Navigare fino al seguente link:
    https://github.com/skills/secure-repository-supply-chain

In questo lab creerai il repository utilizzando un modello pubblico
**skills-secure-repository-supply-chain**

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image1.jpeg)

2.  Selezionare **Create a new repository** nel menu **Use this
    template**.

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image2.jpeg)

3.  Immettere i dettagli seguenti e selezionare **Create Repository**.

    - Repository name: **skills-secure-repository-supply-chain**

    - Repository type: **Public**

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image3.jpeg)

Esercizio 02: Verificare che il grafico delle dipendenze sia abilitato

1.  Nella pagina di destinazione del repository appena creato, passare
    alla scheda **Settings**.

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image4.jpeg)

2.  Nella pagina **Settings,** selezionare **Code security and
    analysis **disponibile in **Security.**

![Uno screenshot di un accesso generale I contenuti generati
dall'intelligenza artificiale potrebbero non essere
corretti.](./media/image5.jpeg)

3.  Verificare/abilitare il Dependency graph. Se il repository è
    privato, verrà abilitato qui. Se il repository è pubblico, sarà
    abilitato per impostazione predefinita)

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image6.jpeg)

Esercizio 03: Aggiungere una nuova dipendenza e visualizzare il grafico
delle dipendenze

1.  Passare alla scheda **Code** e individuare la cartella
    **code/src/AttendeeSite**.

**Nota:** è possibile accedere alla cartella o utilizzare **Go to file**
cercare code/src/AttendeeSite

![Uno screenshot di una pagina web I contenuti generati
dall'intelligenza artificiale potrebbero non essere
corretti.](./media/image7.jpeg)

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image8.jpeg)

2.  Aprire il file **package-lock.json**.

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image9.jpeg)

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image10.jpeg)

3.  Inserire il seguente frammento di codice tra la riga \# 14 e la riga
    \#15

4.  "follow-redirects": {

&nbsp;

1.  "version": "1.14.1",

2.  "resolved":

3.  "https://registry.npmjs.org/follow-redirects/-/follow-redirects-1.14.1.tgz",

4.  "integrity":

5.  "sha512-HWqDgT7ZEkqRzBvc2s64vSZ/hfOceEol3ac/7tKwzuvEyWx3/4UegXh5oBOIotkGsObyk3xznnSRVADBgWSQVg=="

},

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image11.jpeg)

**Nota:** Assicurati che il frammento di codice aggiunto sia rientrato
correttamente come mostrato nello screenshot

5.  Fare clic su **Commit changes **in alto a destra.

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image12.jpeg)

6.  Nella barra di navigazione principale, fare clic sulla scheda
    **Insights**.

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image13.jpeg)

7.  Nel riquadro di navigazione a sinistra, fare clic su **Dependency
    graph**.

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image14.jpeg)

8.  Esaminare tutte le nuove dipendenze nell'hub Dependencies.

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image15.jpeg)

9.  Cercare i reindirizzamenti dei follower ed esaminare la nuova
    dipendenza che avete appena aggiunto.

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image16.jpeg)

Sommario:

Ora avete acquisito informazioni preziose sulla gestione delle
dipendenze del vostro progetto e sulla sicurezza della supply chain del
vostro repository, consentendoti di affrontare e mitigare in modo
proattivo i rischi per la sicurezza.
