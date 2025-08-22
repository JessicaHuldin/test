```mermaid
graph BU

  %% ===== Epic (bakgrund) =====
  subgraph EpicA["Epic A<br/>IM21"]

    %% ===== Capabilities =====
    C_Miljo_lagring["Miljö & lagring i molnet<br/>IM31-1"]
    C_Dokumentextrahering["Dokumentextrahering<br/>IM31-2"]
    C_Annotering_feedback["Annotering & feedback<br/>IM31-3"]
    C_Modelltraning_utvardering["Modellträning & utvärdering<br/>IM31-4"]
    C_Klassificering_hierarkier["Klassificering & hierarkier<br/>IM31-5"]

    %% ===== Features =====
    F_11_Streamlit["Feature 1.1 – Köra Streamlit i molnet<br/>IM41"]
    F_12_Spara_molnet["Feature 1.2 – Spara filer och data i molnet<br/>IM41"]

    F_21_Ontologi["Feature 2.1 – Extrahera PDF med ontologi<br/>IM41"]

    F_31_Annotera["Feature 3.1 – Annotera i molnet<br/>IM41"]
    F_32_Redigera["Feature 3.2 – Redigera annoteringar<br/>IM41"]

    F_41_Retrain["Feature 4.1 – Retrain modellen<br/>IM41"]
    F_42_Evaluate_Analyze["Feature 4.2 – Evaluate & Analyze<br/>IM41"]

    F_51_PrimeArch["Feature 5.1 – Klassificera mot Prime Arch<br/>IM41"]

    %% ===== Stories =====
    %% Miljö & lagring 1.1
    S_IM51_1["IM51-1: Jag som administratör vill kunna starta och köra Streamlit-appen i Azure så att jag kan nå den via en webbadress<br/>IM51"]
    S_IM51_2["IM51-2: Jag som administratör vill kunna bekräfta att appen kör med rätt Docker-image så att jag vet att den bygger på senaste koden<br/>IM51"]

    %% Miljö & lagring 1.2
    S_IM51_3["IM51-3: Jag som systemägare vill kunna spara JSON-filer i Azure Storage så att data är centraliserad och säker<br/>IM51"]
    S_IM51_4["IM51-4: Jag som administratör vill kunna läsa upp en sparad JSON-fil från molnet så att den kan visas i annoteringsverktyget<br/>IM51"]

    %% Dokumentextrahering 2.1
    S_IM51_5["IM51-5: Jag som annotator vill att långa rubriker som bryts på flera rader ska slås ihop så att de blir en korrekt hel rubrik<br/>IM51"]
    S_IM51_6["IM51-6: Jag som annotator vill att paragrafer identifieras som hela stycken även om de bryts över rader så att sammanhanget bevaras<br/>IM51"]
    S_IM51_7["IM51-7: Jag som dokumentägare vill kunna dra/släppa en PDF till systemet så att den extraheras och sparas som JSON<br/>IM51"]

    %% Annotering & feedback 3.1 & 3.2
    S_IM51_8["IM51-8: Jag som annotator vill kunna markera varje textstycke som rubrik, paragraf eller brus så att modellen kan tränas korrekt<br/>IM51"]
    S_IM51_9["IM51-9: Jag som annotator vill kunna se modellens gissning och enkelt markera rätt eller fel så att feedback registreras<br/>IM51"]
    S_IM51_10["IM51-10: Jag som administratör vill att alla annoteringar sparas med vem som gjort dem och när så att vi har spårbarhet<br/>IM51"]
    S_IM51_11["IM51-11: Jag som annotator vill kunna ändra tidigare annoteringar om jag upptäcker fel så att datasetet är korrekt<br/>IM51"]

    %% Modellträning & utvärdering 4.1 & 4.2
    S_IM51_12["IM51-12: Jag som administratör vill kunna köra retrain-scriptet i molnet så att modellen uppdateras med senaste annoteringar<br/>IM51"]
    S_IM51_13["IM51-13: Jag som administratör vill att varje ny modellversion sparas med metadata så att vi kan backa till en tidigare version<br/>IM51"]
    S_IM51_14["IM51-14: Jag som administratör vill kunna köra evaluate-scriptet och se statistik över träffsäkerhet så att vi kan mäta förbättringar<br/>IM51"]
    S_IM51_15["IM51-15: Jag som administratör vill kunna köra analyze-scriptet för att se styrkor och svagheter i modellen<br/>IM51"]

    %% Klassificering & hierarkier 5.1
    S_IM51_16["IM51-16: Jag som annotator vill kunna märka upp en rubrik som R31, en paragraf som R41 och en mening som R51 så att vi får rätt klassificering<br/>IM51"]
    S_IM51_17["IM51-17: Jag som administratör vill att systemet bygger hierarkier (R51 under R41 under R31) så att vi kan analysera relationer mellan regler<br/>IM51"]

  end

  %% ===== Relationer =====
  %% Feature -> Capability
  F_11_Streamlit -- "ingår i" --> C_Miljo_lagring
  F_12_Spara_molnet -- "ingår i" --> C_Miljo_lagring

  F_21_Ontologi -- "ingår i" --> C_Dokumentextrahering

  F_31_Annotera -- "ingår i" --> C_Annotering_feedback
  F_32_Redigera -- "ingår i" --> C_Annotering_feedback

  F_41_Retrain -- "ingår i" --> C_Modelltraning_utvardering
  F_42_Evaluate_Analyze -- "ingår i" --> C_Modelltraning_utvardering

  F_51_PrimeArch -- "ingår i" --> C_Klassificering_hierarkier

  %% Story -> Feature
  S_IM51_1 -- "ingår i" --> F_11_Streamlit
  S_IM51_2 -- "ingår i" --> F_11_Streamlit

  S_IM51_3 -- "ingår i" --> F_12_Spara_molnet
  S_IM51_4 -- "ingår i" --> F_12_Spara_molnet

  S_IM51_5 -- "ingår i" --> F_21_Ontologi
  S_IM51_6 -- "ingår i" --> F_21_Ontologi
  S_IM51_7 -- "ingår i" --> F_21_Ontologi

  S_IM51_8 -- "ingår i" --> F_31_Annotera
  S_IM51_9 -- "ingår i" --> F_31_Annotera
  S_IM51_10 -- "ingår i" --> F_31_Annotera
  S_IM51_11 -- "ingår i" --> F_32_Redigera

  S_IM51_12 -- "ingår i" --> F_41_Retrain
  S_IM51_13 -- "ingår i" --> F_41_Retrain
  S_IM51_14 -- "ingår i" --> F_42_Evaluate_Analyze
  S_IM51_15 -- "ingår i" --> F_42_Evaluate_Analyze

  S_IM51_16 -- "ingår i" --> F_51_PrimeArch
  S_IM51_17 -- "ingår i" --> F_51_PrimeArch

  %% ===== Färgklasser =====
  classDef capability fill:#C5CDE9,stroke:#222,color:#000;
  classDef feature fill:#C5CDE9,stroke:#222,color:#000;
  classDef story fill:#C5CDE9,stroke:#222,color:#000;
  classDef epic fill:#C5CDE9,stroke:#000,color:#000,stroke-dasharray: 5 5;

  class C_Miljo_lagring,C_Dokumentextrahering,C_Annotering_feedback,C_Modelltraning_utvardering,C_Klassificering_hierarkier capability;
  class F_11_Streamlit,F_12_Spara_molnet,F_21_Ontologi,F_31_Annotera,F_32_Redigera,F_41_Retrain,F_42_Evaluate_Analyze,F_51_PrimeArch feature;
  class S_IM51_1,S_IM51_2,S_IM51_3,S_IM51_4,S_IM51_5,S_IM51_6,S_IM51_7,S_IM51_8,S_IM51_9,S_IM51_10,S_IM51_11,S_IM51_12,S_IM51_13,S_IM51_14,S_IM51_15,S_IM51_16,S_IM51_17 story;
  class EpicA epic;
```mermaid
