```mermaid
graph TD

  %% --- Vecka 1 ---
  subgraph V1 [Vecka 1 (tors-fre)]
    Repo["Repo-struktur"]:::emil
    Azure["Azure Storage setup"]:::emil
    Ingest["Ingest pipeline (PDF→Lines)"]:::emil
    Segment["Baseline segmentering"]:::emil
    Rules["Quick-and-dirty rules pipeline"]:::emil
    E2E["Testköra hela kedjan (E2E)"]:::emil

    Plan["Plan & backlog"]:::jessica
    Testplan["Testplan skeleton"]:::jessica
    Schema["Schema-granskning"]:::jessica
    Guidelines["Annoteringsriktlinjer (v1)"]:::jessica
  end

  %% --- Vecka 2 ---
  subgraph V2 [Vecka 2 (mån-fre)]
    Streamlit["Streamlit-MVP"]:::emil
    Deploy["Deploy Streamlit i Azure"]:::emil
    AnnotReady["Team-ready for annotation"]:::emil

    Embed["Embeddings på plats"]:::emil
    ONNX["ONNX-export"]:::emil
    Classifiers["Baseline-klassificerare H1/H2/H3"]:::emil
    Eval["Eval harness & schema checks"]:::emil
    CI["GitHub Actions workflows"]:::emil
    MLflow["MLflow registry"]:::emil
    Export["Export v1 (CSV/XMI)"]:::emil

    TestApp["Testa Streamlit MVP"]:::jessica
    AnnotPass["Första annoteringspass"]:::jessica
    Log["Annoteringslogg"]:::jessica
    Feedback["Feedback loop"]:::jessica
    QA["QA-rutin"]:::jessica
    Onboard["Onboardingplan annotatörer"]:::jessica
    Train2["Träning med 2 annoterare"]:::jessica
    Gold["Första Gold-versionen"]:::jessica
    Review["Sprint Review (mini)"]:::jessica
  end

  %% --- Beroenden Emil ---
  Repo --> Azure --> Ingest --> Segment --> Rules --> E2E
  Rules --> Export
  Streamlit --> Deploy --> AnnotReady
  Embed --> ONNX --> Classifiers --> Eval --> CI --> MLflow

  %% --- Beroenden Jessica ---
  Plan --> Testplan --> Schema --> Guidelines
  Guidelines --> TestApp --> AnnotPass --> Log --> Feedback
  AnnotPass --> QA --> Onboard --> Train2 --> Gold --> Review

  %% --- Styles ---
  classDef emil fill=#87CEEB,stroke=#1E90FF,color=#000;
  classDef jessica fill=#90EE90,stroke=#228B22,color=#000;
```mermaid
