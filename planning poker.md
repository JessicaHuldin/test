```mermaid
flowchart LR
    A["Story ready<br/>X05"] --> B["Discuss<br/>P51"]
    B --> C["Vote<br/>P51"]
    C --> D{"Agreement<br/>P52"}
    D -- No --> E["Discuss extremes<br/>P51"]
    E --> C
    D -- Yes --> F["Assign story points<br/>P51"]
    F --> G["Plan sprint and create tasks<br/>P51"]
    G --> H["Do work and check DoD<br/>P51"]
    H --> I["PO acceptance<br/>P51"]

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
