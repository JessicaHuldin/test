```mermaid
flowchart LR
  A([Start]) --> B{Är detta en<br/>giltig mening?}

  B -- Nej --> B1[Markera: OGILTIG mening]
  B1 --> B2[Logga: is_valid_sentence = false]
  B2 --> Z([Slut])

  B -- Ja --> C[Steg 2: Klassificera typ<br/>R51 eller EJ_R51]
  C --> D{Är klassificeringen korrekt?}

  D -- Ja --> E[Status: GODKÄND]
  E --> E1[Logga: is_valid_sentence=true,<br/>label: R51/EJ_R51, status: GODKÄND]
  E1 --> G[Exportkandidat till Gold]

  D -- Nej --> F[Status: KORRIGERAD]
  F --> F1[Ange felkod: NYCKELORD]
  F1 --> F2[Textfält: missing_keyword<br/>vilket nyckelord saknas]
  F2 --> F3[Logga: error_code=NYCKELORD,<br/>missing_keyword, label korrigerad]
  F3 --> G

  G --> H[Persistens Silver->Gold:<br/>doc_id, para_id, sent_id, text,<br/>is_valid_sentence, label, status,<br/>error_code, missing_keyword,<br/>annotator_id, qa_timestamp]
  H --> Z([Slut])
```mermaid
