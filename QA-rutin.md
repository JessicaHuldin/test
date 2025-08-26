```mermaid
flowchart LR
  A([Material att annotera<br/>X05]) --> A1[Bedöm mening<br/>P51]
  A1 --> B{Är detta en<br/>giltig mening?<br/>P52}

  B -- Nej --> B1[Markera ogiltig mening<br/>P51]
  B1 --> B1a[Ange felkod<br/>P51]
  B1a --> B2([Ogiltig mening<br/>X05])

  B -- Ja --> B3([Giltig mening<br/>X05])
  B3 --> B4[Kör extrahering av regelvillkor<br/>eller brus på aktuell<br/>P51]
  B4 --> C[Bedöm klassificering<br/>R51 eller brus<br/>P51]
  C --> D{Är klassificeringen korrekt?<br/>P52}

  D -- Ja --> E[Markera giltig extrahering<br/>P51]
  E --> F([Godkänd extrahering<br/>av R51 och brus<br/>X05])

  D -- Nej --> G[Markera ogiltig extrahering<br/>P51]
  G --> H[Ange felkod<br/>P51]
  H --> I([Extrahering annoterad<br/>för utveckling<br/>X05])

  %% === Styles ===
  classDef aktivitet fill:#138D18,stroke:#0b4f0b,color:#fff;
  classDef beslut fill:#138D18,stroke:#0b4f0b,color:#fff;
  classDef handelse fill:#DAD8D8,stroke:#555,color:#000;

  class A,B2,B3,F,I handelse;
  class A1,B1,B1a,B4,C,E,G,H aktivitet;
  class B,D beslut;
```mermaid
