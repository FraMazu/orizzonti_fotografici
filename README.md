Certamente. Ho riscritto la guida dal punto di vista di un utente che utilizzerà un eseguibile (`.exe` o `.app`) con un semplice doppio clic, senza mai toccare il terminale o comandi come `pip`.

Ho messo in evidenza l'interfaccia a menu numerico come standard, ho aggiunto una sezione sul primo avvio (importante per le autorizzazioni di sicurezza di Windows/macOS) e ho aggiornato le FAQ.

Ecco la nuova guida, pronta per essere inclusa con i tuoi file eseguibili.

-----

# 🚀 Orizzonti Fotografici: Guida alla Gestione Concorsi

Benvenuto\! Questo strumento è stato creato per rendere la gestione dei tuoi concorsi fotografici semplice e automatica. Dimentica la creazione manuale di cartelle e fogli di calcolo: questo programma si occupa di tutto, dalla preparazione dei materiali per la giuria alla classifica finale.

Segui questa guida per iniziare.

-----

## ✅ Download e Primo Avvio

Lo strumento è un'applicazione autonoma. Non serve installare nulla.

1.  **Scarica il File Corretto:**

      - Per **Windows**, scarica il file `.exe`.
      - Per **macOS**, scarica il file `.app` (o l'eseguibile fornito).

2.  **Primo Avvio (Importante\!):**
    Sia Windows che macOS potrebbero mostrare un avviso di sicurezza la prima volta che avvii il programma, perché non è scaricato dai loro App Store ufficiali.

      - Su **Windows:** Potrebbe apparire una schermata "Windows ha protetto il PC". Clicca su `Ulteriori informazioni` e poi su `Esegui comunque`.
      - Su **macOS:** Potresti vedere un messaggio che dice che "l'app non può essere aperta perché proviene da uno sviluppatore non identificato". Vai in `Impostazioni di Sistema` \> `Privacy e Sicurezza`, scorri in basso e troverai un pulsante per consentire l'apertura del programma. In alternativa, fai clic destro sull'icona dell'app e scegli `Apri`.

-----

## 🔢 L'Interfaccia: Menu a Numeri

Il programma è controllato tramite un semplice menu a numeri che apparirà nella finestra di comando. Per fare una scelta:

1.  Digita il **numero** corrispondente all'azione che vuoi compiere.
2.  Premi il tasto **Invio** (Enter).

È tutto qui\! Non servono comandi complicati.

-----

## 📸 Flusso di Lavoro: Dalla Creazione alla Classifica

Ecco i passaggi tipici per gestire un concorso dall'inizio alla fine.

### 1\. Creare un Nuovo Concorso

1.  **Avvia il Programma:** Fai doppio clic sull'icona dell'eseguibile.
2.  **Crea il Concorso:** Ti verrà presentata una lista. Scegli l'opzione **`[1] >> CREA UN NUOVO CONCORSO <<`**.
3.  **Inserisci i Dettagli:**
      - **Nome:** Digita un nome per il concorso (es. "Bianco e Nero 2025") e premi Invio. Verrà creata una cartella con questo nome.
      - **Scadenza (Opzionale):** Puoi inserire una data di scadenza nel formato `GG/MM/AAAA`. Se la lasci vuota, il concorso risulterà sempre "attivo".

A questo punto, la struttura delle cartelle (`pictures`, `judges`, ecc.) verrà creata automaticamente.

### 2\. Aggiungere le Foto

1.  Trova la cartella del concorso che è stata appena creata.
2.  Apri la sottocartella `pictures`.
3.  **Copia al suo interno tutte le foto** che parteciperanno al concorso.

> ### ⚠️ **Importante: Come Nominare i File delle Foto**
>
> Per estrarre correttamente l'autore e il titolo, i tuoi file devono seguire una di queste convenzioni:
>
>   * **Metodo Consigliato (più semplice):**
>
>     ```
>     Nome Autore--Titolo della Foto.jpg
>     ```
>
>     *Esempio:* `Mario Rossi--Tramonto a Trieste.jpg`
>
>   * **Metodo Alternativo:**
>
>     ```
>     Nome_Autore--Titolo_della_Foto.jpg
>     ```
>
>     *Esempio:* `Mario_Rossi--Tramonto_a_Trieste.jpg`
>   *  **Metodo Alternativo:**
>
>     ```
>     NomeAutore--TitoloDellaFoto.jpg
>     ```
>
>     *Esempio:* `MarioRossi--TramontoATrieste.jpg`
>   *  **Metodo Alternativo:**
>
>     ```
>     nome-autore--titolo-della-foto.jpg
>     ```
>
>     *Esempio:* `mario-rossi--tramonto-a-trieste.jpg`
>
> Lo script si occuperà di normalizzare il testo (es. maiuscole e minuscole).
> Lo script è flessibile e gestisce automaticamente spazi o maiuscole, ma il separatore `--` è fondamentale.

### 3\. Sincronizzare e Preparare i Materiali

Questa è la fase chiave, dove lo script crea i materiali per la giuria.

1.  Nel menu principale, scegli l'opzione **`🔄 Sincronizza foto/criteri`**.
2.  **Definisci i Criteri:** Lo script ti chiederà di confermare o modificare i criteri di valutazione (es. "Tecnica", "Creatività").
3.  **Conferma le Modifiche:** Ti verrà mostrata un'anteprima delle modifiche. Dai la conferma per procedere.

Lo script genererà o aggiornerà due file essenziali:

  - `spreadsheet/..._giuria.csv`: Il foglio di calcolo da inviare ai giurati.
  - `presentations/... .pptx`: La presentazione con tutte le foto e i titoli.

### 4\. Gestire i Giurati

Puoi registrare i tuoi giurati in qualsiasi momento.

1.  Nel menu principale, scegli **`🛠️ Gestisci Giurati`**.
2.  Da qui potrai **aggiungere**, **rinominare** o **eliminare** i giurati. Per ognuno verrà creata una cartella personale.

### 5\. La Fase di Votazione

Questa fase avviene al di fuori del programma.

1.  **Distribuisci il Materiale:** Vai nella cartella `spreadsheet` e invia il file `.csv` a tutti i giurati.
2.  **Raccogli i Voti:** Ogni giurato compilerà il file e te lo restituirà.
3.  **Organizza i File Ricevuti:** Prendi ogni file `.csv` compilato e inseriscilo nella cartella del rispettivo giurato, che si trova in `judges/Nome_del_Giurato/`.

### 6\. Generare la Classifica Finale

Quando hai raccolto i voti, sei pronto per il risultato finale.

1.  Nel menu principale, scegli **`🏆 Genera Classifica Finale`**.
2.  Lo script controllerà la presenza dei file di voto.
      - **Controllo di Sicurezza:** Se mancano i voti di alcuni giurati, lo script ti avviserà e chiederà conferma prima di procedere.
3.  **Risultati Pronti\!** Vai nella cartella `leaderboard` per trovare:
      - **`classifica.csv`**: Il foglio di calcolo finale con tutti i punteggi e le medie.
      - **`classifica.pptx`**: Una presentazione pronta per la proiezione con le foto vincitrici.

-----

## 💡 Domande Frequenti (FAQ)
  - **Posso aggiungere o togliere foto da un concorso già avviato?**
    Sì. Aggiungi/rimuovi i file dalla cartella `pictures`, poi esegui l'azione **`🔄 Sincronizza foto/criteri`**. Lo script rileverà le modifiche e aggiornerà tutto. Ricorda di inviare il nuovo file `.csv` ai giurati\!

  - **Come cambio la data di scadenza di un concorso?**
    Nel menu principale, scegli l'opzione **`✏️ Modifica data di scadenza`**.

  - **Cosa succede se rinomino una foto?**
    Lo script la vedrà come una foto rimossa e una aggiunta. Eseguendo l'azione **`🔄 Sincronizza`**, tutto verrà aggiornato correttamente.
