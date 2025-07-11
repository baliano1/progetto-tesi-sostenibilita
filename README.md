# Progetto di Tesi: Sviluppo di una pagina web per il download dei report di sostenibilità di un’impresa del settore secondario

Questo repository contiene il codice sorgente per una pagina web sviluppata come progetto di tesi. L'obiettivo era selezionare un'azienda del settore secondario, analizzare il suo report di sostenibilità e creare un'interfaccia web per la sua consultazione e download.

**Azienda Selezionata:** Terna S.p.A.
**Documento di Riferimento:** Rapporto Integrato 2023 di Terna.

---

## 🎯 Obiettivo del Progetto

Lo scopo principale del progetto è stato quello di progettare e sviluppare una pagina web *single-page* che fungesse da portale per i report di sostenibilità di Terna. I requisiti chiave erano:

-   **Intuitività:** Creare un'esperienza utente semplice e chiara, che permettesse di accedere facilmente alle informazioni e ai download.
-   **Design Moderno:** Realizzare un'interfaccia esteticamente gradevole, con effetti visivi moderni (come il parallax e le animazioni) che riflettessero l'impegno dell'azienda verso l'innovazione.
-   **Comunicazione Efficace:** Tradurre i dati quantitativi e qualitativi del report in elementi visivi di impatto, come grafici e infografiche.
-   **Accessibilità:** Garantire che la pagina fosse utilizzabile e navigabile da un'ampia gamma di utenti.
-   **Vincolo Tecnico:** Sviluppare l'intera interfaccia, incluse le parti interattive, utilizzando **esclusivamente HTML5 e CSS3**, senza ricorrere a JavaScript.

---

## 🛠️ Tecnologie e Strumenti Utilizzati

L'intero progetto è stato realizzato con un approccio "purista" per dimostrare le piene potenzialità delle tecnologie web standard.

-   **Linguaggi:** HTML5, CSS3
-   **Librerie Esterne:**
    -   **Nessuna libreria JavaScript** è stata utilizzata. Tutta l'interattività è gestita tramite CSS.
    -   **Google Fonts** per l'integrazione dei caratteri tipografici ("Roboto" per il testo e "Orbitron" per il logo).
-   **Ambiente di Sviluppo:**
    -   **Sistema Operativo:** Linux
    -   **Editor di Codice:** Geany IDE

---

## 💻 Descrizione del Codice

Il progetto si compone di due file principali: `index.html` e `style.css`.

### **index.html**

Il documento HTML è stato strutturato utilizzando tag semantici di HTML5 per garantire accessibilità e una corretta indicizzazione dei contenuti.

-   **`<header>`:** Contiene il logo testuale "TERNA" e la barra di navigazione principale, resa fissa durante lo scorrimento (`position: sticky`).
-   **`<main>`:** Racchiude tutte le sezioni principali della pagina.
    -   **`#visione` (Sezione Hero):** La sezione di apertura con un'immagine di sfondo a pieno schermo e l'effetto parallax (`background-attachment: fixed`), che crea un'illusione di profondità.
    -   **`#dati-chiave` (Sezione Report):** È il cuore interattivo della pagina. La funzionalità "clicca per dettagli" è stata implementata con la tecnica del **"Checkbox Hack"**. Ogni card è una `<label>` associata a una `<input type="checkbox">` nascosta. Al click, lo stato della checkbox cambia, permettendo al CSS di applicare una trasformazione 3D (`transform: rotateY(180deg)`) che ruota la card e mostra il contenuto sul retro (`.card-back`).
    -   **`#timeline` (Sezione Traguardi):** Una timeline verticale realizzata interamente in CSS. Un pseudo-elemento `::after` crea la linea centrale, mentre i selettori `:nth-child(odd)` e `:nth-child(even)` posizionano gli eventi a destra e a sinistra.
    -   **Altre sezioni (`#infrastrutture`, `#progetti`, `#reports`):** Sono sezioni informative costruite con layout a griglia (`display: grid`), che le rende flessibili e responsive. Le card informative sono state differenziate (`.interactive-card` vs `.static-card`) per evitare conflitti di stile.

### **style.css**

Il foglio di stile è stato organizzato per essere leggibile, manutenibile e potente.

-   **Variabili CSS (`:root`):** All'inizio del file sono definite tutte le variabili per i colori e i font (`--primary-color`, ecc.). Questo permette di modificare rapidamente il tema grafico dell'intera pagina agendo su poche righe di codice.
-   **Layout Responsivo:** L'intera pagina è responsive grazie all'uso combinato di **Flexbox** (per l'header) e **CSS Grid** (per le sezioni a card). Le **Media Queries** (`@media`) vengono usate per adattare il layout a schermi più piccoli, come quelli dei tablet e degli smartphone, garantendo una perfetta visualizzazione su ogni dispositivo.
-   **Stili Interattivi:** La logica per l'effetto "flip" delle card è gestita dal selettore `:checked`. Quando la checkbox invisibile viene selezionata, il selettore `.card-toggle:checked ~ .info-card.interactive` applica la rotazione 3D.
-   **Grafici CSS Puri:** Tutti i grafici presenti (barre e ciambella) non sono immagini, ma elementi HTML stilizzati con CSS. Le barre sono semplici `div` la cui altezza è animata, mentre il grafico a ciambella è stato creato usando la proprietà `conic-gradient`.



Di seguito quale immagine della pagina web:



<img width="1908" height="917" alt="Schermata-Iniziale" src="https://github.com/user-attachments/assets/2a53a83e-15eb-4162-b561-f22b3f3c2db6" />

<img width="1904" height="917" alt="Schermata_Intermedia" src="https://github.com/user-attachments/assets/62f3ad4e-cab4-4b0a-8f9d-2c6cc6d4375d" />

<img width="1903" height="919" alt="Linea_temporale" src="https://github.com/user-attachments/assets/af4746c4-083c-46b4-871b-5e149db46443" />
