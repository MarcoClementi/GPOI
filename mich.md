```mermaid
flowchart TD
    A([Protocolli di Trasporto - Livello 4 OSI]) --> B([TCP - Transmission Control Protocol])
    A --> C([UDP - User Datagram Protocol])

    %% --- TCP SECTION ---
    B --> B1[[Connessione: Orientato alla connessione]]
    B1 --> B1a[Stabilisce connessione prima della trasmissione]
    B1 --> B1b[Usa 3-Way Handshake: SYN → SYN-ACK → ACK]

    B --> B2[[Affidabilità: Controllo errori e ritrasmissioni]]
    B2 --> B2a[Utilizza checksum per rilevare errori]
    B2 --> B2b[Ritrasmette pacchetti persi]
    B2 --> B2c[Conferma ricezione con ACK]

    B --> B3[[Ordine dei dati garantito]]
    B3 --> B3a[Ogni pacchetto ha un numero di sequenza]
    B3 --> B3b[Riassembla i segmenti nell’ordine corretto]

    B --> B4[[Controllo di flusso e congestione]]
    B4 --> B4a[Gestisce la velocità di trasmissione]
    B4 --> B4b[Evita sovraccarico di rete con finestra scorrevole]

    B --> B5([Overhead maggiore])
    B --> B6([Più lento ma molto affidabile])
    B --> B7([Adatto a dati che non devono andare persi])
    B --> B8([Utilizza buffer e gestione della finestra TCP])

    %% TCP Applications
    B --> D1[[Applicazioni tipiche TCP]]
    D1 --> D1a[HTTP/HTTPS → Navigazione Web]
    D1 --> D1b[FTP → Trasferimento file affidabile]
    D1 --> D1c[SMTP/POP3/IMAP → Email]
    D1 --> D1d[SSH → Accesso remoto sicuro]
    D1 --> D1e[Telnet → Terminale remoto]
    D1 --> D1f[Database (MySQL, PostgreSQL)]
    D1 --> D1g[Google Drive → Backup e sincronizzazione]

    %% --- UDP SECTION ---
    C --> C1[[Connessione: Senza connessione (connectionless)]]
    C1 --> C1a[Nessuna fase di handshake]
    C1 --> C1b[Ogni pacchetto inviato indipendentemente]

    C --> C2[[Nessuna garanzia di consegna]]
    C2 --> C2a[Nessuna conferma ACK]
    C2 --> C2b[Nessuna ritrasmissione automatica]

    C --> C3[[Nessun controllo di flusso o congestione]]
    C3 --> C3a[Il mittente invia alla massima velocità possibile]
    C3 --> C3b[Perdita di pacchetti non blocca la comunicazione]

    C --> C4([Meno overhead])
    C --> C5([Più veloce ma meno affidabile])
    C --> C6([Ideale per dati in tempo reale])
    C --> C7([Ogni pacchetto è autonomo])
    C --> C8([Utilizza checksum semplice per errori])

    %% UDP Applications
    C --> E1[[Applicazioni tipiche UDP]]
    E1 --> E1a[DNS → Risoluzione rapida nomi di dominio]
    E1 --> E1b[DHCP → Assegnazione IP dinamica]
    E1 --> E1c[VoIP (Skype, Zoom) → Comunicazioni vocali live]
    E1 --> E1d[Streaming video/audio (YouTube, Netflix, Twitch)]
    E1 --> E1e[Gaming online (Fortnite, Valorant, CS2)]
    E1 --> E1f[NTP → Sincronizzazione oraria]
    E1 --> E1g[Multicast IPTV e dirette streaming]
    E1 --> E1h[Sensori IoT e telemetria]

    %% --- CONFRONTO DIRETTO ---
    A --> F([Confronto TCP vs UDP])
    F --> F1[TCP: Affidabilità > Velocità]
    F --> F2[UDP: Velocità > Affidabilità]
    F --> F3[TCP: Comunicazioni sequenziali e sicure]
    F --> F4[UDP: Comunicazioni rapide e indipendenti]
    F --> F5[TCP usa 3-way handshake]
    F --> F6[UDP non usa handshake]
    F --> F7[TCP: Ideale per trasferimenti completi]
    F --> F8[UDP: Ideale per dati in tempo reale]
    F --> F9[TCP: Elevato controllo → più overhead]
    F --> F10[UDP: Nessun controllo → minore ritardo]
    F --> F11[TCP: Porte comuni → 80(HTTP), 443(HTTPS), 21(FTP)]
    F --> F12[UDP: Porte comuni → 53(DNS), 67-68(DHCP), 123(NTP)]

    %% --- SCELTA PROTOCOLLO ---
    F --> G[[Scelta del protocollo]]
    G --> G1[Serve affidabilità e ordine? → TCP]
    G --> G2[Serve velocità e bassa latenza? → UDP]
