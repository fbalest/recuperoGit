# Verifica di Laboratorio Git (MAX 10pt)

## Esercizio 1 (1pt)

1. Creare un repository Git in locale.
2. Effettuare le seguenti **modifiche** (in più commit):
    1. Creare un nuovo file di testo.
    2. Aggiungere del contenuto al file.
3. Creare un repository su GitHub e collegarlo a quello locale.
4. Pushare le modifiche sul repository remoto su GitHub.
5. **Consegnare uno screenshot** con i comandi eseguiti dalla bash e il repository locale.

---

## Esercizio 2 (3pt)

1. Creare una **copia locale** di questo repository.
2. Creare un nuovo **branch** e fare le seguenti **modifiche** a un file `.css` (in più commit):
    1. Cambiare il colore di sfondo della pagina.
    2. Modificare la font-size di un paragrafo.
    3. Allineare il testo di un header (`h1`) al centro.
3. Fusione delle modifiche: riportare solo la modifica relativa alla dimensione del paragrafo e all’allineamento dell’header sul branch `main`.
4. Pushare le modifiche sul repository remoto su GitHub.
5. **Consegnare uno screenshot** con i comandi eseguiti dalla bash.

---

## Esercizio 3 (3pt)

1. Creare una **copia locale** di questo repository.
2. Creare un nuovo branch e apportare le seguenti **modifiche** (in più commit):
    1. Aggiungere una riga al file `es3.txt` con il proprio nome.
    2. Aggiungere una seconda riga con il proprio cognome.
3. Creare una nuova commit sul branch `main` con il proprio nome e la città di residenza.
4. Eseguire il merge del branch con il branch `main` e risolvere eventuali conflitti (accettando entrambe le modifiche, in caso di conflitto).
5. Eseguire il pull dal repository remoto.
6. **Consegnare uno screenshot** con i comandi eseguiti dalla bash e il repository locale.

---

## Esercizio 4 (10pt)

Simula un ciclo di sviluppo software su più mesi, dove i gruppi A e B lavorano in parallelo con modifiche sullo stesso codice base, introducendo conflitti, nuove versioni e rilasci. Ogni mese ci sono operazioni di merge, tag, risoluzione conflitti e rilasci di versioni multiple. La gestione dei conflitti sarà fondamentale in più occasioni.

### Calendario di sviluppo:

#### 1. **Primo mese:**
- **Gruppo A:** Esegue delle modifiche su un nuovo branch chiamato `feature-1`. Le modifiche consistono in **3 commit**:  
  - Modifica al file `index.html` per aggiungere una nuova sezione.
  - Modifica al file `style.css` per applicare un nuovo tema al sito.
  - Aggiunta di un nuovo file `script.js` per l'implementazione di una funzionalità JS.
- **Gruppo B:** Esegue delle modifiche in parallelo su un altro branch chiamato `feature-2`. Le modifiche consistono in **2 commit**:
  - Modifica al file `index.html` per aggiornare il layout.
  - Aggiunta di un nuovo file `about.html` per una nuova pagina.
- Alla fine del mese, **Gruppo A** rilascia una versione `v1.0.0` direttamente dal branch `main` e crea un **Tag** `v1.0.0`.  
- **Gruppo B** esegue un **merge** del branch `feature-2` nel branch `main`, ma ci sono dei conflitti con `index.html` (perché entrambi i gruppi hanno modificato lo stesso file). Risolvere il conflitto accettando le modifiche di entrambi.

#### 2. **Secondo mese:**
- **Gruppo A:** Esegue delle modifiche su un nuovo branch chiamato `feature-3` (questo sarà un branch a lungo termine). Le modifiche consistono in **4 commit**:
  - Aggiunta di una nuova sezione nella pagina `index.html`.
  - Modifiche al file `style.css` per un nuovo stile di layout.
  - Modifica al file `script.js` per integrare una nuova funzionalità.
  - Aggiornamento della documentazione in un nuovo file `README.md`.
- **Gruppo B:** Esegue delle modifiche in parallelo su un nuovo branch chiamato `feature-4`. Le modifiche consistono in **3 commit**:
  - Aggiunta di una nuova sezione al `footer` nel file `index.html`.
  - Modifica del file `style.css` per un nuovo tema.
  - Aggiornamento della pagina `about.html` con nuove informazioni.
- Alla fine del mese, **Gruppo A** rilascia una nuova versione `v1.1.0` dal branch `main` e crea un **Tag** `v1.1.0`.  
- **Gruppo B** esegue il merge di `feature-4` su `main`. Tuttavia, in questo caso, il file `style.css` è stato modificato da entrambi i gruppi, quindi si verifica un conflitto che va risolto accettando entrambe le modifiche.

#### 3. **Terzo mese:**
- **Gruppo A:** Risolve un bug nel file `script.js` introdotto nella versione `v1.1.0`. Questo fix viene fatto nel branch `bugfix-v1.1.1`, che contiene **2 commit**:
  - Correzione di un errore nel codice JS.
  - Aggiornamento della documentazione nel `README.md`.
- **Gruppo B:** Introduce una nuova funzionalità sul file `index.html` nel branch `feature-5`. Le modifiche consistono in **2 commit**:
  - Aggiunta di una nuova sezione al `header`.
  - Modifica alla pagina `about.html` con nuovi dettagli.
- Alla fine del mese, **Gruppo A** rilascia la versione `v1.1.1` come versione di bugfix e crea un **Tag** `v1.1.1`.  
- **Gruppo B** esegue il merge delle modifiche nel branch `main` con la versione `v1.1.1`. Ci saranno conflitti con `index.html` e `style.css` che devono essere risolti accettando entrambe le modifiche.

#### 4. **Quarto mese:**
- **Gruppo A:** Inizia a lavorare su una versione innovativa del prodotto nel branch `feature-6`. Le modifiche consistono in **3 commit**:
  - Aggiunta di una nuova funzionalità interattiva nel `index.html`.
  - Modifica e ottimizzazione del file `style.css`.
  - Aggiunta di nuove funzionalità interattive nel `script.js`.
- **Gruppo B:** Rilascia la versione `v1.2.0` con una nuova feature nel file `about.html` e aggiorna il file `style.css`. Le modifiche sono **3 commit**:
  - Aggiunta di una sezione nella pagina `about.html`.
  - Modifiche alle proprietà CSS in `style.css`.
  - Ottimizzazione del layout nel file `index.html`.
- Alla fine del mese, **Gruppo A** rilascia la versione `v2.0.0` dal branch `feature-6` direttamente come una versione innovativa.
- **Gruppo B** rilascia la versione `v1.2.0` dal branch `main`.

#### 5. **Quinto mese:**
- Viene deciso di separare il lavoro sui rami principali e lasciarli evolvere in due percorsi distinti:  
  - La versione `1.x.x` continuerà a essere sviluppata e mantenuta in un branch `legacy-1.x`.  
  - La versione `2.x.x` diventerà la principale, e tutte le nuove funzionalità saranno sviluppate su di essa.
- **Gruppo A:** Crea un nuovo branch `legacy-1.x` a partire da `v1.2.0` e trasferisce le modifiche più recenti relative a questa versione.
- **Gruppo B:** Sposta il lavoro sul branch `main` per concentrarsi sulla versione `2.x.x`, che diventerà il ramo principale.

Alla fine del mese:
- **Gruppo A** effettua un merge di `main` in `legacy-1.x`.
- **Gruppo B** continua a sviluppare sul branch `main` e crea la versione `v2.1.0`.

---

### Dettagli Aggiuntivi:

- Durante i vari merge, è richiesto che tu risolva i conflitti manualmente, scegliendo la strategia di fusione più appropriata (accettare entrambe le modifiche, scegliere una versione rispetto all'altra, ecc.).  
