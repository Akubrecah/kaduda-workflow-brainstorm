graph TD
    A[Kaambe Phone SMS] -->|Text: 'Hi, I'm John'| B(Twilio Gateway)
    B -->|Forward to| C{Your Python Server}
    
    C -->|Check Memory| D{New Number?}
    D -- Yes --> E[Create New Chat History]
    D -- No --> F[Load Previous Chat History]
    
    E --> G[Add 'Hi, I'm John' to History]
    F --> G
    
    G -->|Send Full History| H[Google Gemini API]
    H -->|Reply: 'Hello John!'| I[Update History with Reply]
    
    I -->|Shorten Text < 160 chars| J[Send Reply]
    J --> B
    B --> A