```mermaid
graph TD

  %% ===== Epic =====
  subgraph EpicA["Epic A<br/>IM21"]

    %% Capabilities
    C_Miljo_lagring["Miljö & lagring i molnet<br/>IM31-1"]
    C_Dokumentextrahering["Dokumentextrahering<br/>IM31-2"]
    C_Annotering_feedback["Annotering & feedback<br/>IM31-3"]
    C_Modelltraning_utvardering["Modellträning & utvärdering<br/>IM31-4"]
    C_Klassificering_hierarkier["Klassificering & hierarkier<br/>IM31-5"]

    %% Features
    F_11_Streamlit["Feature 1.1 – Köra Streamlit i molnet<br/>IM41"]
    F_12_Spara_molnet["Feature 1.2 – Spara filer och data i molnet<br/>IM41"]
    F_21_Ontologi["Feature 2.1 – Extrahera PDF med ontologi<br/>IM41"]
    F_31_Annotera["Feature 3.1 – Annotera i molnet<br/>IM41"]
    F_32_Redigera["Feature 3.2 – Redigera annoteringar<br/>IM41"]
    F_41_Retrain["Feature 4.1 – Retrain modellen<br/>IM41"]
    F_42_Evaluate["Feature 4.2 – Evaluate & Analyze<br/>IM41"]
    F_51_PrimeArch["Feature 5.1 – Klassificera mot Prime Arch<br/>IM41"]

    %% Stories (exempel, alla från pptx går att lägga in)
    S_IM51_1["IM51-1: Jag som administratör vill kunna starta och köra Streamlit-appen i Azure<br/>IM51"]
    S_IM51_2["IM51-2: Jag som administratör vill kunna bekräfta att appen kör med rätt Docker-image<br/>IM51"]
    S_IM51_3["IM51-3: Jag som systemägare vill kunna spara JSON-filer i Azure Storage<br/>IM51"]

  end

  %% Relationer Feature → Capability
  F_11_Streamlit -- "ingår i" --> C_Miljo_lagring
  F_12_Spara_molnet -- "ingår i" --> C_Miljo_lagring
  F_21_Ontologi -- "ingår i" --> C_Dokumentextrahering
  F_31_Annotera -- "ingår i" --> C_Annotering_feedback
  F_32_Redigera -- "ingår i" --> C_Annotering_feedback
  F_41_Retrain -- "ingår i" --> C_Modelltraning_utvardering
  F_42_Evaluate -- "ingår i" --> C_Modelltraning_utvardering
  F_51_PrimeArch -- "ingår i" --> C_Klassificering_hierarkier

  %% Relationer Story → Feature
  S_IM51_1 -- "ingår i" --> F_11_Streamlit
  S_IM51_2 -- "ingår i" --> F_11_Streamlit
  S_IM51_3 -- "ingår i" --> F_12_Spara_molnet

  %% Färger
  classDef capability fill:#C5CDE9,stroke:#222,color:#000;
  classDef feature fill:#C5CDE9,stroke:#222,color:#000;
  classDef story fill:#C5CDE9,stroke:#222,color:#000;
  classDef epic fill:#C5CDE9,stroke:#000,color:#000,stroke-dasharray: 5 5;

  class C_Miljo_lagring,C_Dokumentextrahering,C_Annotering_feedback,C_Modelltraning_utvardering,C_Klassificering_hierarkier capability;
  class F_11_Streamlit,F_12_Spara_molnet,F_21_Ontologi,F_31_Annotera,F_32_Redigera,F_41_Retrain,F_42_Evaluate,F_51_PrimeArch feature;
  class S_IM51_1,S_IM51_2,S_IM51_3 story;
  class EpicA epic;
```mermaid
