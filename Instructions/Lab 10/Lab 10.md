**Lab 10: Usare GitHub Actions per pubblicare il progetto in un'immagine
Docker**

Obiettivi:

Si supponga di sviluppare un progetto software che si desidera
impacchettare e distribuire come immagine Docker. Per semplificare il
processo di distribuzione e garantire che l'immagine Docker venga
pubblicata in modo coerente nei pacchetti GitHub, si decide di usare
GitHub Actions per l'automazione. Ciò ti consentirà di impostare un
flusso di lavoro che automatizza la pubblicazione della tua immagine
Docker ogni volta che vengono apportate modifiche, assicurando che il
tuo progetto sia sempre aggiornato e disponibile per la distribuzione.

In questo laboratorio pratico, potrai:

- Configurare un file del flusso di lavoro GitHub Actions che
  automatizza il processo di creazione e pubblicazione dell'immagine
  Docker.

- Configurare il flusso di lavoro per creare l'immagine Docker ed
  eseguirne il push nei pacchetti GitHub, assicurandoti che l'immagine
  venga pubblicata correttamente.

- Creare una richiesta pull per visualizzare tutte le modifiche
  apportate.

Esercizio \#1: Creare un nuovo repository da un modello pubblico

1.  Navigare fino al seguente link:
    https://github.com/skills/publish-packages

In questo lab creerai il repository utilizzando un modello pubblico
"**skills-publish-packages**".

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image1.jpeg)

2.  Selezionare **Create a new repository **nel menu **Use this
    template**.

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image2.jpeg)

3.  Immettere i dettagli seguenti e selezionare **Create Repository**.

    - Repository name: **skills-publish-packages**

    - Repository type: **Public**

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image3.jpeg)

Esercizio 2: Creare un file di flusso di lavoro e configurarlo

1.  Fare clic sul pulsante **Code** nella barra di navigazione
    principale del repository appena creato.

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image4.jpeg)

2.  Nel menu a discesa del ramo principale, selezionare ramo **cd**.

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image5.jpeg)

3.  Nella pagina successiva, vai alla cartella **.github/workflows/**,
    quindi selezionare **Add file **e fare clic su **Create new file**.

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image6.jpeg)

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image7.jpeg)

4.  Nel campo **Name your file**, inserire publish.yml

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image8.jpeg)

5.  Aggiungere il codice seguente al file **publish.yml**.

6.  name: Publish to Docker

7.  on:

8.  push:

9.  branches:

10. \- main

11. permissions:

12. packages: write

13. contents: read

14. jobs:

15. publish:

16. runs-on: ubuntu-latest

17. steps:

18. \- name: Checkout

19. uses: actions/checkout@v4

20. \# Add your test steps here if needed...

21. \- name: Docker meta

22. id: meta

23. uses: docker/metadata-action@v5

24. with:

25. images: ghcr.io/YOURNAME/publish-packages/game

26. tags: type=sha

27. \- name: Login to GHCR

28. uses: docker/login-action@v3

29. with:

30. registry: ghcr.io

31. username: ${{ github.repository_owner }}

32. password: ${{ secrets.GITHUB_TOKEN }}

33. \- name: Build container

34. uses: docker/build-push-action@v5

35. with:

36. context: .

37. push: true

tags: ${{ steps.meta.outputs.tags }}

38. Sostituire YOURNAME con il vostro nome utente.

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image9.jpeg)

39. Assicurati che il nome dell'immagine sia univoco, fare clic su
    **Commit changes.**

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image10.jpeg)

40. Fare nuovamente clic su **Commit changes**.

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image11.jpeg)

41. Creare ora una richiesta pull per visualizzare tutte le modifiche
    apportate nell'esercizio precedente.

42. Fare clic sulla scheda **Pull Requests **sulla barra di spostamento.

43. Fare clic su **New pull request**.

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image12.jpeg)

44. Nella pagina **Comparing changes,** impostare **base**: main e
    **compare**:cd e quindi fare clic su **Create pull request.**

![Uno screenshot di una chat I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image13.jpeg)

45. Nella pagina **Add a title **fare clic su **Create pull request.**

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image14.jpeg)

46. Attendere 20 secondi per l'esecuzione delle azioni e rivedi i
    risultati.

![Uno screenshot di un computer I contenuti generati dall'intelligenza
artificiale potrebbero non essere corretti.](./media/image15.jpeg)

Sommario:

Ora avete acquisito esperienza pratica nell'uso di GitHub Actions per
automatizzare la pubblicazione di immagini Docker, migliorando la vostra
capacità di semplificare i processi di distribuzione e mantenere
aggiornate le distribuzioni dei progetti.
