📄 Progetto di Tesi: Pagina di Sostenibilità Terna
Questo repository contiene il progetto di tesi incentrato sullo sviluppo di una pagina web per la consultazione e il download dei report di sostenibilità.

🏢 

Azienda Selezionata: Terna S.p.A. 

📖 

Documento di Riferimento: Rapporto Integrato 2023 di Terna 

🎯 Obiettivo del Progetto
Lo scopo principale del progetto è stato quello di progettare e sviluppare una pagina web single-page che fungesse da portale per i report di sostenibilità di Terna.  I requisiti chiave erano:


Intuitività: Creare un'esperienza utente semplice e chiara, che permettesse di accedere facilmente alle informazioni e ai download. 


Design Moderno: Realizzare un'interfaccia esteticamente gradevole, con effetti visivi moderni che riflettessero l'impegno dell'azienda verso l'innovazione. 


Comunicazione Efficace: Tradurre i dati del report in elementi visivi di impatto, come grafici e infografiche. 


Accessibilità: Garantire che la pagina fosse utilizzabile e navigabile da un'ampia gamma di utenti. 


Vincolo Tecnico: Sviluppare l'intera interfaccia, incluse le parti interattive, utilizzando esclusivamente HTML5 e CSS3, senza ricorrere a JavaScript. 

🛠️ Tecnologie e Strumenti Utilizzati
L'intero progetto è stato realizzato con un approccio "purista" per dimostrare le piene potenzialità delle tecnologie web standard. 


Linguaggi: HTML5, CSS3 

Librerie Esterne:

🚫 Nessuna libreria JavaScript è stata utilizzata. Tutta l'interattività è gestita tramite CSS. 

✒️ Google Fonts per l'integrazione del carattere tipografico "Roboto".

Ambiente di Sviluppo:

🐧 

Sistema Operativo: Linux 

📝 

Editor di Codice: Geany IDE 

💻 Descrizione del Codice
Il progetto si compone di due file principali: 

index.html e style.css. 

File index.html
Il documento HTML è stato strutturato utilizzando tag semantici di 

HTML5 per garantire accessibilità e una corretta indicizzazione dei contenuti. 


<header>: Contiene il logo testuale "TERNA" e la barra di navigazione principale, resa fissa durante lo scorrimento (position: sticky). 


<main>: Racchiude tutte le sezioni principali della pagina. 

#visione (Sezione Hero): La sezione di apertura con un'immagine di sfondo a pieno schermo.

#dati-chiave (Sezione Report): È il cuore interattivo della pagina. La funzionalità "clicca per dettagli" è stata implementata con la tecnica del "Checkbox Hack". Ogni card è una 

<label> associata a una <input type="checkbox"> nascosta. Al click, lo stato della checkbox cambia, permettendo al CSS di applicare una trasformazione 3D (

transform: rotateY(180deg)) che ruota la card e mostra il contenuto sul retro. 

#timeline: Una timeline orizzontale (che diventa verticale su schermi piccoli) realizzata interamente in CSS. Un pseudo-elemento ::before crea la linea centrale, mentre i singoli item si dispongono lungo di essa tramite CSS Grid.


Altre sezioni (#strategia, #progetti, #reports, etc.): Sono sezioni informative costruite con layout a griglia (display: grid), che le rende flessibili e responsive. 

File style.css
Il foglio di stile è stato organizzato per essere leggibile, manutenibile e potente. 


Variabili CSS (:root): All'inizio del file sono definite tutte le variabili per i colori, permettendo di modificare rapidamente il tema grafico agendo su poche righe di codice. 


Layout Responsivo: L'intera pagina è responsive grazie all'uso combinato di Flexbox e CSS Grid. Le Media Queries (

@media) vengono usate per adattare il layout a schermi più piccoli, garantendo una perfetta visualizzazione su ogni dispositivo. 


Stili Interattivi: La logica per l'effetto "flip" delle card è gestita dal selettore :checked. Quando la checkbox invisibile viene selezionata, il selettore 

.card-toggle:checked ~ .info-card.interactive applica la rotazione 3D. 


Grafici CSS Puri: Tutti i grafici (barre e ciambella) non sono immagini, ma elementi HTML stilizzati con CSS. Le barre sono 

div la cui altezza è animata, mentre il grafico a ciambella usa la proprietà conic-gradient. 
