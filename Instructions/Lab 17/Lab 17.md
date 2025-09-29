**Lab 17: Abilitare l'analisi segreta in un repository GitHub ed
eseguire il commit di un token**

Immaginare di essere uno sviluppatore di software che lavora a un
progetto team con un repository GitHub condiviso. Per garantire che il
codice rimanga sicuro e privo di perdite accidentali, si decide di
implementare la scansione segreta--- una funzionalità che consente di
identificare informazioni sensibili come token API o password che
potrebbero essere inavvertitamente inserite nel repository.

Obiettivo:

In questo laboratorio pratico, potrai:

1.  Abilitare Secret Scanning: Configurare la scansione segreta sul
    vostro repository GitHub per rilevare e contrassegnare
    automaticamente le informazioni sensibili.

2.  Commit di un token: Aggiungere intenzionalmente un token o altre
    informazioni sensibili al repository per testare l'efficacia della
    funzione di scansione segreta.

Esercizio \#1: Creare un repository GitHub e abilitare l'analisi dei
segreti

Attività \#1: Creare un repository utilizzando un modello

1.  Accedere al vostro account GitHub.

2.  Andare al seguente link:
    https://github.com/skills/introduction-to-secret-scanning

In questo laboratorio creerai il repository utilizzando un modello
pubblico "**skills-introduction-to-secret-scanning**".

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image1.jpeg)

3.  Selezionare **Create a new repository** nel menu **Use this
    template**.

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image2.jpeg)

4.  Immettere i dettagli seguenti e selezionare **Create Repository**.

    - Repository name: **skills-introduction-to-secret-scanning**

    - Repository type: **Public**

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image3.jpeg)

Attività \#2: Abilitare la scansione segreta

1.  Nella pagina di destinazione del repository appena creato,
    selezionare **Settings **dalla barra di navigazione superiore.

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image4.jpeg)

2.  Nella sezione **Security **della barra laterale, selezionare **Code
    security and analysis**.

**Nota**: è necessario scorrere verso il basso per visualizzare il menu
**Security**

![Uno screenshot di una finestra del browser I contenuti generati
dall'intelligenza artificiale potrebbero non essere
corretti.](./media/image5.jpeg)

3.  Scorrere verso il basso fino alla fine della pagina e fare clic su
    **Enable **per la scansione segreta.

**Nota:** Se viene visualizzato il pulsante **Disable**, significa che
la scansione segreta è già abilitata per l'archivio.

![Uno sfondo bianco con testo nero I contenuti generati
dall'intelligenza artificiale potrebbero non essere
corretti.](./media/image6.jpeg)

Se non è già abilitato, vedrai il pulsante **Enable **come mostrato di
seguito:

![Uno screenshot di un errore del computer I contenuti generati
dall'intelligenza artificiale potrebbero non essere
corretti.](./media/image7.jpeg)

**Nota:** Quando la scansione segreta è abilitata, viene inviata una
notifica e-mail relativa alle credenziali nel repository all'ID di posta
associato all'account. I token in questo repository Skills sono
inattivi. Non vi è alcun rischio per l'ambiente.

Ora che la scansione segreta è abilitata in questo repository, eseguiamo
il commit di un nuovo token per vedere come funziona.

Esercizio \#2: Commit di un token

In questo esercizio, eseguirai il commit di una chiave AWS e di un ID di
accesso al repository. Si tratta di un token inattivo che non può essere
utilizzato per accedere ad AWS.

1.  Nel riquadro in alto a sinistra della barra di navigazione
    principale, fare clic sulla scheda **Code** e selezionare il file
    **credentials.yml**.

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image8.jpeg)

2.  Fare clic sul pulsante **Edit** a destra.

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image9.jpeg)

3.  Copiare il testo seguente e incollarlo sotto il codice esistente nel
    riquadro di modifica del file **credentials.yml**.

4.  default:

5.  aws_access_key_id: AKIAQYLPMN5HNM4OZ56B

6.  aws_secret_access_key: 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

7.  output: json

region: us-east-2

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image10.jpeg)

8.  Fare clic sul pulsante **Commit changes **nell'angolo in alto a
    destra e fare nuovamente clic su **Commit Changes** nella finestra
    **Commit Changes**.

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image11.jpeg)

**Nota:** Dopo aver confermato le modifiche, riceverai un avviso nella
vostra casella di posta associata al vostro account GitHub.

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image12.jpeg)

Sommario:

A questo punto è possibile acquisire una comprensione pratica di come
abilitare e testare la scansione segreta per proteggere il codice e i
dati.
