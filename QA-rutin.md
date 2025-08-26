```mermaid
flowchart LR
  A([Start]) --> A1[Bedöm mening]
  A1 --> B{Är detta en<br/>giltig mening?}

  B -- Nej --> B1[Markera: OGILTIG mening]
  B1 --> Z([Slut])

  B -- Ja --> C[Bedöm klassificering<br/>R51 eller EJ_R51]
  C --> D{Är klassificeringen korrekt?}

  D -- Ja --> E[Markera giltig extrahering]
  E --> F[Status: GODKÄND]
  F --> Z([Slut])

  D -- Nej --> G[Status: KORRIGERAD]
  G --> G1[Ange felkod: NYCKELORD]
  G1 --> G2[Textfält: missing_keyword<br/>vilket nyckelord saknas]
  G2 --> Z([Slut])
```mermaid
