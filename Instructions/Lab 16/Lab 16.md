Lab 16: Rimozione della cronologia dei Commit da un repository Git

Obiettivo:

Immaginare di far parte di un team di sviluppo che lavora su un progetto
in cui informazioni sensibili, come le chiavi API o le credenziali del
database, sono state accidentalmente salvate nel tuo repository Git. I
commit accidentali possono essere difficili da rimuovere con Git.

In questo laboratorio, potrai:

- Clonare il repository con dati sensibili di cui è stato eseguito il
  commit accidentale.

- Rimuovere/eliminare il file contenente dati sensibili dal repository
  clonato e Confermare la rimozione.

- Push delle modifiche su GitHub: Caricare il repository aggiornato su
  GitHub per riflettere le modifiche.

### Esercizio \#1: Creare il repository con la cronologia dei commit accidentali (dati sensibili)

1.  Accedere al vostro account GitHub.

2.  Accedere al seguente link:
    <https://github.com/skills/change-commit-history>

> In questo laboratorio creerai il repository utilizzando un modello
> pubblico "**skills-change-commit-history**".
>
> ![](./media/image1.png)

3.  Selezionare **Create a new repository** nel menu **Use this
    template**.

> ![Uno screenshot di un computer Descrizione generata
> automaticamente](./media/image2.png)

4.  Immettere i dettagli seguenti e selezionare **Create Repository**.

- Repository name: **skills-change-commit-history**

- Repository type: **Public**

![](./media/image3.png)

### Esercizio \# 2: Rimuovere/eliminare il file (.env nella directory principale del progetto) contenente dati sensibili

1.  Nella pagina di destinazione del repository clonato, andare a
    **Code\>Local\>HTTPS** e copiare l'URL.

![](./media/image4.png)

2.  Aprire Windows Powershell e inserire il seguente comando.

**git clone \<your-repository-url\>**

**Nota**: Sostituire con l'URL che avete copiato nel passaggio 1.

> ![](./media/image5.png)

3.  Passare alla directory del repository, immettere il comando
    seguente.

**+++cd “C:\Users\Admin\skills-change-commit-history”+++**

**Nota**: Sostituire con il nome del repository

> ![](./media/image6.png)

4.  Eseguire il seguente comando per eliminare .env dalla directory
    principale,

**+++git rm .env**+++

> ![Uno screenshot dello schermo di un computer Descrizione generata
> automaticamente](./media/image7.png)

5.  Commit la rimozione del file .env

**+++git commit -m "remove .env file”+++**

> ![Schermata di un computer Descrizione generata
> automaticamente](./media/image8.png)
>
> **Suggerimento**: Come rimuovere completamente il file .env dalla
> cronologia Git e riscrivere la cronologia totale con nuovi hash di
> commit?
>
> Utilizzare i seguenti comandi per:

- Rimuovere completamente il file .env dalla cronologia Git e riscrivere
  la cronologia totale

> **git filter-branch --force --index-filter 'git rm --cached
> --ignore-unmatch.env' --prune-empty --tag-name-filter cat -- --all**

- Inviare la rimozione a GitHub

> **git push origine --force –all**

6.  Inviare la rimozione a GitHub:

**git push**

> ![Schermata di un programma per computer Descrizione generata
> automaticamente](./media/image9.png)

Sommario:

A questo punto è stata completata la pulizia del repository Git,
assicurandosi che il contenuto sensibile non venga esposto nella
cronologia del repository.
