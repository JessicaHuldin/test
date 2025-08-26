```mermaid
flowchart LR
  A([Material att annotera]) --> A1[Bedöm mening]
  A1 --> B{Är detta en<br/>giltig mening?}

  B -- Nej --> B1[Markera: OGILTIG mening]
  B1 --> B2[Ogiltig mening]

  B -- Ja --> B3[Giltig mening]
  B3 --> C[Bedöm klassificering<br/>R51 eller EJ_R51]
  C --> D{Är klassificeringen korrekt?}

  D -- Ja --> E[Markera giltig extrahering]
  E --> F[Godkänd extrahering<br/>av R51 och brus]

  D -- Nej --> G[Markera ogiltig extrahering]
  G --> H[Ange felkod]
  H --> I[Ogiltig extrahering]

```mermaid
