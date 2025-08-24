```mermaid
flowchart LR
    A["Story ready<br/>X05"] --> B["PO presents story, goals and acceptence criteria<br/>P51"]
    B --> C["Team discusses scope and risks<br/>P51"
    C --> D["Vote planning poker cards 1,2,3,5,8,13,21<br/>P51"]
    D --> E{"Agreement?<br/>P52"}
    E -- No --> F["Discuss extremes: highest vs lowest, risks, assumption, dependencies<br/>P51"]
    F --> C
    E -- Yes --> G["Assign story points<br/>P51"]
    G --> H["update vacklog as input to Sprint Planning <br/>P51"]

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
