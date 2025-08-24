```mermaid
flowchart TD
    A[Story identified and prioritized] --> B[PO presents goals and acceptance criteria]
    B --> C[Team Q and A scope and risks]
    C --> D[Vote 1 Planning Poker cards 1 2 3 5 8 13]
    D --> E{Agreement}
    E -- No --> F[Discuss extremes highest and lowest risks assumptions dependencies]
    F --> G[Vote again]
    G --> E
    E -- Yes --> H[Assign story points]
    H --> I[Update backlog for sprint planning]
    I --> J[Break down story into tasks development testing design]
    J --> K[Work on tasks during sprint]
    K --> L[Check Definition of Done coding testing documentation integration]
    L --> M[PO acceptance story done]
```mermaid
