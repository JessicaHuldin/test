```mermaid
flowchart TD
    A[Story identified and prioritized in Product Backlog] --> B[PO presents story, goals and acceptance criteria]
    B --> C[Q&A: team discusses scope and risks]
    C --> D[Vote #1 – Planning Poker cards 1, 2, 3, 5, 8, 13]
    D --> E{Agreement?}
    E -- No --> F[Discuss extremes: highest vs lowest, risks, assumptions, dependencies]
    F --> G[Vote again]
    G --> E
    E -- Yes --> H[Assign Story Points]
    H --> I[Update backlog as input to Sprint Planning]
    I --> J[Break down story into tasks<br/>(development, testing, design...)]
    J --> K[Work on tasks during sprint]
    K --> L[Check Definition of Done<br/>(coding, testing, documentation, integration)]
    L --> M[PO/Stakeholder Acceptance<br/>story considered Done]
```mermaid
