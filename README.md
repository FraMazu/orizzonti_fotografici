# Orizzonti Fotografici 
### Strumento di Gestione Concorsi

Questo script Python è progettato per semplificare la gestione dei concorsi fotografici. Automatizza la creazione di cartelle, la preparazione di fogli di calcolo per i giurati, la generazione di presentazioni e l'elaborazione di una classifica finale basata sui voti.

---

## Funzionalità

  * **Organizzazione Automatica:** Crea una struttura di cartelle chiara (`pictures`, `judges`, `spreadsheet`, `leaderboard`) per ogni concorso, nominata in base al concorso e all'anno.
  * **Gestione Giurati:** Crea una sottocartella per ogni giurato, dove verranno salvati i rispettivi voti.
  * **Preparazione Fogli di Calcolo:** Analizza le foto presenti nella cartella `pictures` e genera un foglio di calcolo (file `.csv`) nella cartella `spreadsheet`. Questo foglio elenca le foto da valutare e i criteri di giudizio inseriti dall'utente.
  * **Generazione Presentazioni:**
      * Crea una presentazione (file `.pptx`) con una slide per ogni foto, mostrando il titolo estratto dal nome del file.
      * **Novità:** Genera una presentazione della classifica (`classifica.pptx`) con le foto della top 10, completa di titolo e autore.
  * **Leaderboard:** Elabora i voti inseriti dai giurati (nei file `.csv` all'interno delle rispettive cartelle) e genera una classifica consolidata (`classifica.csv`) nella cartella `leaderboard`.


## Come Usare il File
1. **Esegui il file relativo al tuo sistema operativo**

2. **Segui le istruzioni:** Lo script ti guiderà passo dopo passo:

      * Ti chiederà di inserire il nome del concorso.
      * Creerà le cartelle necessarie.
      * Se è la prima esecuzione, ti chiederà di inserire i nomi dei giurati e i criteri di valutazione.
      * Ti chiederà di inserire le foto nella cartella `pictures` (se non ci sono ancora).

4.  **Gestione dei Voti:**

      * Dopo la configurazione iniziale, lo script genererà un foglio di calcolo (`.csv`) con i titoli delle foto e i criteri.
      * Invia questo file a tutti i giurati.
      * Copia i file inviati dai giurati nella cartella di ogni giurato (es. `judges/giurato_1/`).
      * I giurati potranno aprire il file `.csv` con un programma come Excel o Fogli Google e inserire i loro voti.

5.  **Generazione della Classifica:**

      * Una volta che tutti i giurati hanno inserito i voti e salvato i file `.csv` nelle loro cartelle, esegui nuovamente lo script.
      * Lo script rileverà i voti e genererà la classifica finale (`classifica.csv` e `classifica.pptx`) nella cartella `leaderboard`.

> **Nota:** Non modificare nessun file al di fuori delle cartelle `pictures` e `judges`.
