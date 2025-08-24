```mermaid
flowchart LR
    A["Story ready\nX05"] --> B["Discuss\nP51"]
    B --> C["Vote\nP51"]
    C --> D{"Agreement\nP52"}
    D -- No --> E["Discuss extremes\nP51"]
    E --> C
    D -- Yes --> F["Assign story points\nP51"]
    F --> G["Plan sprint and create tasks\nP51"]
    G --> H["Do work and check DoD\nP51"]
    H --> I["PO acceptance\nP51"]

    %% Style
    style A fill:#138D18,stroke:#D9D9D9,color:#000000
    style B fill:#138D18,stroke:#000000,color:#000000
    style C fill:#138D18,stroke:#000000,color:#000000
    style D fill:#138D18,stroke:#000000,color:#000000
    style E fill:#138D18,stroke:#000000,color:#000000
    style F fill:#138D18,stroke:#000000,color:#000000
    style G fill:#138D18,stroke:#000000,color:#000000
    style H fill:#138D18,stroke:#000000,color:#000000
    style I fill:#138D18,stroke:#000000,color:#000000
```mermaid
