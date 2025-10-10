```mermaid
flowchart TD
    A["Trasporto nei protocolli Internet"] --> B["TCP (Transmission Control Protocol)"]
    A --> C["UDP (User Datagram Protocol)"]

    %% TCP caratteristiche
    B --> B1["Connessione orientata"]
    B --> B2["Affidabile: ritrasmissione e controllo errori"]
    B --> B3["Controllo di flusso e congestione"]
    B --> B4["Ordinamento dei pacchetti"]
    B --> B5["Maggiore overhead e latenza"]
   
    %% TCP applicazioni
    B --> D1["HTTP/HTTPS → navigazione web"]
    B --> D2["FTP → trasferimento file"]
    B --> D3["SMTP/IMAP/POP3 → email"]
    B --> D4["SSH → accesso remoto sicuro"]
    D1 --> E1["Esempio: caricamento di una pagina web (richiede dati completi e ordinati)"]
    D2 --> E2["Esempio: download di un file (serve affidabilità totale)"]

    %% UDP caratteristiche
    C --> C1["Senza connessione"]
    C --> C2["Nessuna garanzia di consegna"]
    C --> C3["No controllo di flusso né congestione"]
    C --> C4["Basso overhead, bassa latenza"]
    C --> C5["I pacchetti possono arrivare fuori ordine o mancare"]

    %% UDP applicazioni
    C --> F1["DNS → risoluzione nomi rapida"]
    C --> F2["VoIP → chiamate in tempo reale"]
    C --> F3["Streaming video/audio → continuità > affidabilità"]
    C --> F4["Online gaming → aggiornamenti rapidi di posizione"]
    F2 --> G1["Esempio: se un pacchetto VoIP si perde, la conversazione continua comunque"]
    F3 --> G2["Esempio: piccola perdita di frame accettabile pur di mantenere fluidità"]

    %% Confronto diretto
    B ---|Affidabilità| C
    B ---|Latenza maggiore| C
    B ---|Ordinamento pacchetti| C
    B ---|Controllo di congestione| C
    B ---|Uso tipico: dati critici| C
    C ---|Uso tipico: tempo reale| B