**Lab 05: Gestire le versioni del software con un flusso di lavoro
basato sulle versioni di GitHub**

Obiettivo:

Immaginare di far parte di un team di sviluppo software che lavora su un
progetto che richiede aggiornamenti e rilasci regolari. Per gestire il
software in modo efficiente, si decide di implementare un flusso di
lavoro basato sulle versioni utilizzando GitHub. Questo flusso di lavoro
consente di gestire il controllo delle versioni e le iterazioni software
in modo efficace, garantendo che ogni versione venga tracciata e che i
problemi vengano risolti in modo controllato.

In questo laboratorio pratico, imparerai,

- Creare un repository: Configurare un repository denominato
  skills-release-based-workflow che funga da base per il flusso di
  lavoro basato sul rilascio.

- Implementare il controllo delle versioni: Esplorare i concetti di
  controllo delle versioni e l'importanza di tenere traccia delle
  iterazioni software.

- Creare una versione beta: Seguire la procedura per creare una versione
  beta per la codebase corrente, inclusi l'assegnazione di tag e il
  rilascio su GitHub.

- Simulare uno scenario reale: Introdurre un bug nella codebase,
  simulando uno scenario comune di identificazione e risoluzione dei
  problemi all'interno del flusso di lavoro di rilascio.

Esercizio \#1: Impostazione di un nuovo repository (che funga da base
per il flusso di lavoro basato sulla versione)

1.  Accedere al vostro account GitHub.

2.  Navigare fino al seguente link:
    https://github.com/skills/release-based-workflow

In questo lab creerai il repository utilizzando un modello pubblico
"**skills-release-based-workflow**".

![](./media/image1.jpeg)

3.  Selezionare **Create a new repository **nel menu **Use this
    template**.

![](./media/image2.jpeg)

4.  Immettere i dettagli seguenti e selezionare **Create Repository**.

    - Repository name: **skills-release-based-workflow**

    - Repository type: **Public**

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image3.jpeg)

Esercizio \#2: Creare una versione per la codebase corrente

In questo esercizio, creeremo una versione per questo repository su
GitHub.

- Le versioni di GitHub puntano a un commit specifico.

- Le versioni possono includere note di rilascio nei file Markdown e nei
  file binari allegati.

Nota: Prima di utilizzare un flusso di lavoro basato sulla versione per
una versione più grande, creiamo un tag e una versione.

1.  Una volta creato il repository (nell'Esercizio \#1), andare su
    **Releases **nella barra laterale destra della pagina e fare clic su
    **Create a new release.**

![](./media/image4.jpeg)

Suggerimento: Per accedere a questa pagina, fare clic sulla scheda
**Code** nella parte superiore del repository. Quindi, trovare la
sezione **Releases **nella barra laterale a destra.

1.  Nella pagina **Releases/Tags,** immettere quanto segue:

    - Keep the **Target** as main

    - In the field for **Choose a Tag**, specify a number.

In questo caso, utilizzare la versione 0.9 e selezionare **Create new
tag v0.9 on publish**

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image5.jpeg)

2.  Assegnare un titolo alla versione, ad esempio **First beta release**

**Nota:** Puoi anche fornire una breve descrizione della pubblicazione.

![](./media/image6.jpeg)

3.  Scorrere la pagina verso il basso per selezionare la casella di
    controllo accanto a **Set as a pre-release**, poiché rappresenta una
    versione beta, e fare clic su **Publish release**.

![Uno screenshot di un telefono I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image7.jpeg)

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image8.jpeg)

Esercizio \#3: Introdurre un bug (da correggere in seguito)

Per preparare il terreno per un secondo momento, aggiungiamo ora un bug
che risolveremo come parte del flusso di lavoro di rilascio nei passaggi
successivi. Un ramo "update-text-colors" è già stato creato nel
repository (creato nell'Esercizio \#1) per te, quindi creiamo e uniamo
una richiesta pull con questo ramo.

1.  Nella barra di navigazione principale, fare clic sulla scheda **Pull
    requests**.

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image9.jpeg)

2.  Nella pagina successiva fare clic su **New pull request.**

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image10.jpeg)

3.  Nella pagina **Compare changes **selezionare quanto segue e fare
    clic su **Create pull request,**

    - base: **release-v1.0** e

    - compare: **update-text-colors**.

![](./media/image11.jpeg)

4.  Nella pagina **Open a pull request,** immettere quanto segue e
    quindi fare clic su **Create pull request.**

    - **Add a title**: Impostare il titolo della richiesta di pull su
      **Updated game text style**

    - **Add a description**: \## Description: Updated game text color to
      green

![](./media/image12.jpeg)

5.  Nella pagina **Updated game text style \#1 **fare clic su **Merge
    pull request**, quindi su **Confirm page.**

![](./media/image13.jpeg)

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image14.jpeg)

6.  Nella pagina successiva, eliminare il ramo appena creato facendo
    clic sul pulsante **Delete branch**.

![](./media/image15.jpeg)

7.  Attendere circa 20 secondi mentre GitHub Actions aggiorna
    automaticamente la pagina.

![](./media/image16.jpeg)

**Sommario:**

Ora hai acquisito esperienza pratica nella creazione e nella gestione di
un flusso di lavoro basato sui rilasci, migliorando la vostra capacità
di tenere traccia delle versioni, gestire i rilasci e risolvere i bug in
modo efficiente.
