```mermaid

flowchart TD
    A[Story identifierad<br/>och prioriterad i Product Backlog] --> B[PO presenterar story<br/>målsättning & acceptanskriterier]
    B --> C[Frågor & förtydliganden<br/>teamet diskuterar omfattning & risker]
    C --> D[Första omgången röstning<br/>(Planning Poker-kort: 1,2,3,5,8,13...)]
    D --> E{Enighet?}
    E -- Nej, stor spridning --> F[Diskussion: högst vs lägst<br/>risker, antaganden, beroenden]
    F --> G[Ny röstning]
    G --> E
    E -- Ja, samsyn nådd --> H[Story får estimerat värde<br/>(Story Points)]
    H --> I[Backlogen uppdateras<br/>underlag till Sprint Planning]

```mermaid
