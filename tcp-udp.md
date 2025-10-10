```mermaid
graph TD
    A[TCP vs UDP]

    %% RAMI PRINCIPALI
    A --> B[TCP (Transmission Control Protocol)]
    A --> C[UDP (User Datagram Protocol)]

    %% TCP - DETTAGLI
    B --> B1[Connessione: Orientato alla connessione]
    B --> B2[Affidabilità: Conferma ricezione pacchetti]
    B --> B3[Controllo di flusso e congestione]
    B --> B4[Riordinamento pacchetti garantito]
    B --> B5[Intestazione più pesante (20+ byte)]
    B --> B6[Ritrasmissione automatica dei pacchetti persi]

    B --> B7[TCP - Applicazioni tipiche]
    B7 --> B71[HTTP/HTTPS - Navigazione web sicura]
    B7 --> B72[FTP - Trasferimento file affidabile]
    B7 --> B73[SMTP/IMAP/POP3 - Email]
    B7 --> B74[SSH - Accesso remoto sicuro]

    %% UDP - DETTAGLI
    C --> C1[Connessione: Non orientato alla connessione]
    C --> C2[Nessuna conferma di ricezione]
    C --> C3[Velocità elevata, basso overhead]
    C --> C4[Nessun riordinamento dei pacchetti]
    C --> C5[Nessun controllo di congestione o flusso]
    C --> C6[Intestazione leggera (8 byte)]
    C --> C7[Possibili perdite accettabili]

    C --> C8[UDP - Applicazioni tipiche]
    C8 --> C81[DNS - Risoluzione nomi]
    C8 --> C82[VoIP - Comunicazione in tempo reale]
    C8 --> C83[Streaming video/audio]
    C8 --> C84[Gaming online]
    C8 --> C85[DHCP - Assegnazione IP]

    %% CONFRONTO
    A --> D[Confronto diretto]
    D --> D1[TCP: +Affidabile / -Veloce]
    D --> D2[UDP: -Affidabile / +Veloce]
    D --> D3[TCP: Per dati critici]
    D --> D4[UDP: Per dati in tempo reale]

