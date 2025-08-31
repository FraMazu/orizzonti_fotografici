# 🚀 Orizzonti Fotografici: Guida alla Gestione Concorsi

Benvenuto\! Questo strumento è stato creato per rendere la gestione dei tuoi concorsi fotografici semplice e automatica. Dimentica la creazione manuale di cartelle e fogli di calcolo: questo programma si occupa di tutto, dalla preparazione dei materiali per la giuria alla classifica finale.

Segui questa guida per iniziare.

### ✨ Funzionalità Principali

  * **Creazione Automatica della Struttura:** Genera istantaneamente tutte le cartelle necessarie per un nuovo concorso.
  * **"Jury Kit" con un Click:** Crea un pacchetto completo per la giuria con CSV per i voti, presentazione PowerPoint delle foto e un archivio `.zip` pronto da inviare.
  * **Classifica Intelligente:** Calcola la classifica finale gestendo correttamente i pari merito con un sistema "denso" (es. 1°, 2°, 2°, 3°), senza saltare posizioni.
  * **Presentazione Vincitori:** Genera un file PowerPoint con i primi 10 classificati, pronto per la cerimonia di premiazione.

-----

## ✅ Download e Primo Avvio

Lo strumento è un'applicazione autonoma. Non serve installare nulla.

1.  **Scarica il File Corretto:**

      * Per **Windows**, scarica il file `.exe`.
      * Per **macOS**, scarica il file `.app`.

2.  **Primo Avvio (Importante\!):**
    Sia Windows che macOS potrebbero mostrare un avviso di sicurezza la prima volta che avvii il programma, perché non è scaricato dai loro App Store ufficiali.

      * Su **Windows:** Potrebbe apparire una schermata "Windows ha protetto il PC". Clicca su `Ulteriori informazioni` e poi su `Esegui comunque`.
      * Su **macOS:** Potresti vedere un messaggio che dice che "l'app non può essere aperta perché proviene da uno sviluppatore non identificato". Vai in `Impostazioni di Sistema` \> `Privacy e Sicurezza`, scorri in basso e troverai un pulsante per consentire l'apertura del programma. In alternativa, fai clic destro sull'icona dell'app e scegli `Apri`.

-----

## 🔢 L'Interfaccia: Menu a Numeri

Il programma è controllato tramite un semplice menu a numeri che apparirà nella finestra di comando. Per fare una scelta:

1.  Digita il **numero** corrispondente all'azione che vuoi compiere.
2.  Premi il tasto **Invio** (Enter).

-----

## 📸 Flusso di Lavoro: Dalla Creazione alla Classifica

### 1\. Creare un Nuovo Concorso

1.  **Avvia il Programma:** Fai doppio clic sull'icona dell'eseguibile.
2.  **Crea il Concorso:** Scegli l'opzione **`>> CREA UN NUOVO CONCORSO <<`**.
3.  **Inserisci i Dettagli:**
      * **Nome:** Digita un nome per il concorso (es. "Bianco e Nero 2025") e premi Invio.
      * **Scadenza (Opzionale):** Puoi inserire una data di scadenza nel formato `GG/MM/AAAA`.

Verrà creata automaticamente una cartella per il tuo concorso con questa struttura:

```
Nome Del Concorso/
├── 📁 judges/         # Cartelle personali dei giurati per i loro voti
├── 📁 jury_kit/        # Materiali generati per la giuria (CSV, PPTX, foto)
├── 📁 leaderboard/     # Classifica finale e PPTX dei vincitori
└── 📁 pictures/        # Qui vanno messe le foto originali del concorso
```

### 2\. Aggiungere le Foto

1.  Trova la cartella del concorso appena creata.
2.  Apri la sottocartella `pictures`.
3.  **Copia al suo interno tutte le foto** che parteciperanno al concorso.

> ### ⚠️ **Importante: Come Nominare i File delle Foto**
>
> Per estrarre correttamente l'autore e il titolo, i tuoi file devono usare **due trattini `--`** come separatore:
>
>   * **Metodo Consigliato:** `Nome Autore--Titolo della Foto.jpg`
>     *(Esempio: `Mario Rossi--Tramonto a Trieste.jpg`)*
>
>   * **Metodi Alternativi:** `Nome_Autore--Titolo_della_Foto.jpg`
>
> **N.B.** Lo script è flessibile: se il separatore `--` non viene trovato, l'intero nome del file verrà considerato come il titolo della foto e l'autore risulterà "Sconosciuto".

### 3\. Sincronizzare e Creare il "Jury Kit"

Questa è l'azione chiave da eseguire ogni volta che si aggiungono/rimuovono foto o si modificano i criteri.

1.  Nel menu principale, scegli l'opzione **`🔄 Sincronizza e Crea/Aggiorna Jury Kit`**.
2.  **Definisci i Criteri:** Lo script ti chiederà di confermare o modificare i criteri di valutazione.
3.  **Conferma le Modifiche:** Dopo un'anteprima, dai l'ok per procedere.

Lo script genererà e aggiornerà i seguenti elementi:

  * **La cartella `jury_kit`**, che ora conterrà il foglio `.csv` per la votazione, la presentazione `.pptx` e una sottocartella `original_pictures`.
  * **Un file ZIP pronto da inviare\!** Nella cartella principale del concorso, troverai un archivio `nome-concorso_jury_kit.zip`. **Questo è l'unico file che devi inviare ai giurati.**

### 4\. Gestire i Giurati

1.  Nel menu principale, scegli **`🛠️ Gestisci Giurati`**.
2.  Da qui potrai **aggiungere**, **rinominare** o **eliminare** i giurati.

### 5\. La Fase di Votazione

1.  **Distribuisci il Materiale:** Invia il file **`nome-concorso_jury_kit.zip`** a tutti i giurati.
2.  **Raccogli i Voti:** Ogni giurato ti restituirà il suo file `.csv` compilato.
3.  **Organizza i File Ricevuti:** Inserisci ogni `.csv` ricevuto nella cartella del rispettivo giurato (`judges/Nome_del_Giurato/`).

### 6\. Generare la Classifica Finale

1.  Nel menu principale, scegli **`🏆 Genera Classifica Finale`**.
2.  Lo script controllerà i voti e ti avviserà se ne manca qualcuno.
3.  **Risultati Pronti\!** Vai nella cartella `leaderboard` per trovare:
      * **`classifica.csv`**: La classifica completa in formato tabellare.
      * **`classifica.pptx`**: Una presentazione pronta per la proiezione con i vincitori dal 10° al 1° posto.

-----

## 💡 Domande Frequenti (FAQ)

  * **Dove vengono salvate le cartelle e i file?**
    La prima volta che avvii il programma, verrà creata una cartella principale chiamata `Concorsi Orizzonti Fotografici`. Questa cartella si troverà **nello stesso posto in cui hai messo ed eseguito il file `.exe` o `.app`**. Tutti i tuoi concorsi verranno salvati al suo interno.

  * **Perché ricevo un errore di "Accesso Negato" o "Permission Denied"?**
    Questo accade quasi sempre perché un file che lo script sta cercando di modificare (es. `classifica.csv`, `giuria.pptx`) è **attualmente aperto** sul tuo computer (in Excel, PowerPoint, Blocco Note, ecc.). Assicurati di **chiudere tutti i file** relativi al concorso prima di eseguire un'azione nello script.

  * **Come funziona la classifica in caso di pareggio?**
    Lo script usa un sistema di "classifica densa". Se due foto ottengono lo stesso punteggio e si classificano al secondo posto, la foto successiva si classificherà al terzo posto (non al quarto). Non ci sono "salti" di posizione.

  * **Posso aggiungere o togliere foto da un concorso già avviato?**
    Sì. Aggiungi/rimuovi i file dalla cartella `pictures`, poi esegui di nuovo l'azione **`🔄 Sincronizza e Crea/Aggiorna Jury Kit`**. Lo script rileverà le modifiche e aggiornerà tutto. Ricorda di inviare il nuovo file `..._jury_kit.zip` ai giurati\!

  * **Come cambio la data di scadenza di un concorso?**
    Nel menu principale, scegli l'opzione **`✏️ Modifica data di scadenza`**.