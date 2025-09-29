**Lab 03: Creare il vostro portfolio online con GitHub Pages e Jekyll**

Obiettivo:

Immaginare di essere uno sviluppatore di software in erba in una startup
tecnologica, desideroso di mostrare i tuoi progetti, le tue competenze e
le tue esperienze attraverso un portfolio online. Vuoi una piattaforma
professionale per mostrare il vostro lavoro, quindi decidi di creare un
sito web o un blog personale utilizzando GitHub Pages. Questa
piattaforma vi consente di sfruttare i repository GitHub per pubblicare
e mantenere facilmente il vostro sito web.

In questo laboratorio pratico, potrai:

- Creare un repository GitHub: Configurare un nuovo repository che
  fungerà da base per il vostro sito personale.

- Abilitare GitHub Pages: Configurare GitHub Pages per ospitare il
  vostro sito Web direttamente dal vostro repository.

- Distribuire il vostro primo sito utilizzando Jekyll: utilizza Jekyll,
  un popolare generatore di siti statici, per creare e distribuire un
  sito Web dall'aspetto professionale con il minimo sforzo.

Esercizio \#1: Creare un repository da un modello

1.  Accedere al vostro account GitHub.

2.  Accedere al seguente link: https://github.com/skills/github-pages

In questo laboratorio creerai il repository utilizzando un modello
pubblico "**skills-github-pages**".

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image1.jpeg)

3.  Selezionare **Create a new repository **nel menu **Use this
    template**.

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image2.jpeg)

4.  Immettere i dettagli seguenti e selezionare **Create Repository**.

    - Repository name: **skills-github-pages**

    - Repository type: **Public**

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image3.jpeg)

Esercizio \#2: Abilitare GitHub Pages

1.  Una volta creato il repository, andare alla home page. Nel riquadro
    di navigazione principale, fare clic sull'icona **Settings**.

![Uno screenshot di una pagina web I contenuti generati
dall'intelligenza artificiale potrebbero non essere
corretti.](./media/image4.jpeg)

2.  Nella pagina delle impostazioni, scorrere verso il basso fino a
    **Code and automation** e fare clic su **Pages.**

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image5.jpeg)

3.  Nelle pagine GitHub, assicurati che la pagina "**Deploy from a
    branch**" sia selezionata dal menu a discesa **Source**, quindi
    selezionare **main** dal menu a discesa **Branch**.

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image6.jpeg)

4.  Fare clic sul pulsante **Save **per continuare.

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image7.jpeg)

5.  L'origine delle pagine GitHub verrà salvata. Attendere circa un
    minuto, quindi aggiornare questa pagina. GitHub Actions si
    aggiornerà automaticamente al passaggio successivo.

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image8.jpeg)

6.  Il vostro sito è ora attivo.

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image9.jpeg)

7.  Fare clic sul pulsante **Visit Site** per visualizzare il vostro
    sito. Hai attivato le pagine GitHub.

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image10.jpeg)

Esercizio \#3: Distribuire il vostro sito utilizzando Jekyll

Lavorerai in un ramo, **my-pages**, per far sì che questo sito abbia un
bell'aspetto. In questo laboratorio utilizzeremo un tema pronto per il
blog. "minima".

Jekyll utilizza un file intitolato **\_config.yml** per memorizzare le
impostazioni del vostro sito, il vostro tema e i contenuti
riutilizzabili come il titolo del vostro sito e l'handle GitHub.

1.  Selezionare la scheda **Code** del vostro repository

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image11.jpeg)

2.  Espandere il ramo **main **e selezionare **my-pages**.

![Uno screenshot di una pagina web I contenuti generati
dall'intelligenza artificiale potrebbero non essere
corretti.](./media/image12.jpeg)

Nel ramo **my-pages,** individuare il file \_**config.yml**

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image13.jpeg)

3.  Aprire l'editor di file nell'angolo in alto a destra.

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image14.jpeg)

4.  Aggiungere un tema: imposta su **minima **in modo che venga
    visualizzato nel file \_config.yml come di seguito:

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image15.jpeg)

5.  Fare clic sul pulsante **Commit Changes **per salvare le modifiche.

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image16.jpeg)

**Nota:** Attendere circa un minuto, quindi aggiornare questa pagina.
GitHub Actions si aggiornerà automaticamente al passaggio successivo.

6.  Per controllare il sito aggiornato, fare clic sul pulsante **Visit
    site **sotto le pagine GitHub.

![Uno screenshot di una pagina web I contenuti generati
dall'intelligenza artificiale potrebbero non essere
corretti.](./media/image17.jpeg)

7.  Viene applicato il tema selezionato. Puoi continuare a modificare le
    altre variabili di configurazione, ad esempio title:, author:, e
    description:, per personalizzare ulteriormente il vostro sito

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image18.jpeg)

Sommario:

Ora avete creato un sito Web con pagine GitHub e applicato un tema. Puoi
utilizzare questa esperienza per creare un sito Web live in cui puoi
aggiornare e mostrare continuamente il vostro percorso di sviluppo
software, rendendo più facile per i datori di lavoro, i collaboratori e
la comunità tecnologica vedere il vostro lavoro e le vostre competenze.
