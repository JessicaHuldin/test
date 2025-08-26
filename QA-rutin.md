```mermaid
flowchart LR
  A([Start]) --> A1[Bedöm mening]
  A1 --> B{Är detta en<br/>giltig mening?}

  B -- Nej --> B1[Markera: OGILTIG mening]
  B1 --> B2[Ogiltig mening]
  B2 --> Z([Slut])

  B -- Ja --> B3[Giltig mening]
  B3 --> C[Bedöm klassificering<br/>R51 eller EJ_R51]
  C --> D{Är klassificeringen korrekt?}

  D -- Ja --> E[Markera giltig extrahering]
  E --> F[Status: GODKÄND]
  F --> Z([Slut])

  D -- Nej --> G[Markera ogiltig extrahering]
  G --> H[Ange felkod]
  H --> I[Annoterad extrahering]
  I --> Z([Slut])
```mermaid
