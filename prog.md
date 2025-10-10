```mermaid
graph TD
    A[TCP vs UDP]

    %% RAMI PRINCIPALI
    A --> B[TCP (Transmission Control Protocol)]
    A --> C[UDP (User Datagram Protocol)]

    %% TCP - DETTAGLI
    B --> B1[Connessione: Orientato alla connessione]
    B --> B2[Affidabilità: Conferma ricezione pacchetti]
    B --> B3[Controllo di flusso: Regola la velocità]
    B --> B4[Controllo di congestione: Evita sovraccarichi]
    B --> B5[Riordinamento: Pacchetti ricevuti in ordine]
    B --> B6[Intestazione più pesante (20+ byte)]
    B --> B7[Ritrasmissione automatica dei pacchetti persi]

    B --> B8[TCP - Applicazioni tipiche]
    B8 --> B81[HTTP/HTTPS - Navigazione web sicura]
    B8 --> B82[FTP - Trasferimento file con conferma]
    B8 --> B83[SMTP/IMAP/POP3 - Email affidabile]
    B8 --> B84[SSH - Accesso remoto sicuro]

    %% UDP - DETTAGLI
    C --> C1[Connessione: Non orientato alla connessione]
    C --> C2[Nessuna conferma: Nessuna garanzia di ricezione]
    C --> C3[Velocità: Più veloce, meno overhead]
    C --> C4[Ordine: Nessun riordinamento dei pacchetti]
    C --> C5[Non gestisce congestione o flusso]
    C --> C6[Intestazione leggera (8 byte)]
    C --> C7[Possibili perdite accettabili]

    C --> C8[UDP - Applicazioni tipiche]
    C8 --> C81[DNS - Risoluzione nomi veloce]
    C8 --> C82[VoIP - Comunicazione vocale in tempo reale]
    C8 --> C83[Streaming video/audio - Fluidità prioritaria]
    C8 --> C84[Gaming online - Bassa latenza importante]
    C8 --> C85[DHCP - Assegnazione IP rapida]

    %% CONFRONTO DIRETTO (OPZIONALE)
    A --> D[Confronto pratico]
    D --> D1[TCP: Maggiore affidabilità, più lento]
    D --> D2[UDP: Minore affidabilità, più veloce]
    D --> D3[TCP: Ideale per dati critici]
    D --> D4[UDP: Ideale per dati in tempo reale]

