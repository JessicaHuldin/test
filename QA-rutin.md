```mermaid
flowchart LR
  %% ===== Start =====
  A([Start]) --> B{Är detta en<br/>giltig mening?}

  %% ===== Steg 1: Giltig/ogiltig =====
  B -- Nej --> B1[Markera: OGILTIG mening]
  B1 --> B2[Logga: is_valid_sentence = false]
  B2 --> Z([Slut])

  B -- Ja --> C[Steg 2: Klassificera typ<br/>R51 eller EJ_R51]
  C --> D{Är klassificeringen<br/>korrekt?}

  %% ===== Korrekt =====
  D -- Ja --> E[Status = GODKÄND]
  E --> E1[Logga: is_valid_sentence=true,<br/>label ∈ {R51,EJ_R51}, status=GODKÄND]
  E1 --> G[[Export-kandidat till Gold]]

  %% ===== Fel: NYCKELORD =====
  D -- Nej --> F[Status = KORRIGERAD]
  F --> F1[Ange felkod = NYCKELORD]
  F1 --> F2[Textfält: missing_keyword<br/>(vilket nyckelord saknas?)]
  F2 --> F3[Logga: error_code=NYCKELORD,<br/>missing_keyword='…', label korrigerad]
  F3 --> G

  %% ===== Meta/lagring =====
  G --> H[Persistens (Silver → Gold):<br/>doc_id, para_id, sent_id, text,<br/>is_valid_sentence, label, status,<br/>error_code, missing_keyword,<br/>annotator_id, qa_timestamp]
  H --> Z

  %% ===== Stil =====
  classDef startend fill:#f2f2f2,stroke:#555,color:#111;
  classDef decision fill:#fff3cd,stroke:#c8a400,color:#333;
  classDef good fill:#d1f0d1,stroke:#138D18,color:#0b4f0b;
  classDef warn fill:#ffe0cc,stroke:#cc6b1c,color:#5a2f00;
  classDef invalid fill:#ffd6d6,stroke:#d33,color:#5a0000;
  classDef data fill:#e8f1ff,stroke:#2b6cb0,color:#0b3d73;

  class A,Z startend;
  class B,D decision;
  class E,E1 good;
  class F,F1,F2,F3 warn;
  class B1,B2 invalid;
  class G,H data;
```mermaid
