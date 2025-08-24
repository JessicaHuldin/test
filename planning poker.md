```mermaid
flowchart TD
    A[Story identified and prioritized in Product Backlog] --> B[PO presents story, goals and acceptance criteria]
    B --> C[Q&A: team discusses scope and risks]
    C --> D[Vote #1 – Planning Poker cards 1, 2, 3, 5, 8, 13, 21]
    D --> E{Agreement?}
    E -- No --> F[Discuss extremes: highest vs lowest, risks, assumptions, dependencies]
    F --> G[Vote again]
    G --> E
    E -- Yes --> H[Assign Story Points]
    H --> I[Update backlog as input to Sprint Planning]
%% Style
    style A fill:#D9D9D9,stroke:#000000,color:#000000
    style B fill:#138D18,stroke:#000000,color:#000000
    style C fill:#138D18,stroke:#000000,color:#000000
    style D fill:#138D18,stroke:#000000,color:#000000
    style E fill:#138D18,stroke:#000000,color:#000000
    style F fill:#138D18,stroke:#000000,color:#000000
    style G fill:#138D18,stroke:#000000,color:#000000
    style H fill:#138D18,stroke:#000000,color:#000000
    style I fill:#138D18,stroke:#000000,color:#000000
```mermaid
