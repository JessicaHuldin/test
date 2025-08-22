graph TD

  %% Emil - teknisk kedja
  Repo["Repo-struktur"] --> Azure["Azure Storage setup"]
  Azure --> Ingest["Ingest pipeline (PDF→Lines)"]
  Ingest --> Segment["Baseline segmentering"]
  Segment --> Rules["Quick-and-dirty rules pipeline"]
  Rules --> E2E["Testköra hela kedjan (E2E)"]
  Rules --> Export["Export v1 (CSV/XMI)"]

  Streamlit["Streamlit-MVP"] --> Deploy["Deploy Streamlit i Azure"]
  Deploy --> AnnotReady["Team-ready for annotation"]

  Embed["Embeddings på plats"] --> ONNX["ONNX-export"]
  ONNX --> Classifiers["Baseline-klassificerare H1/H2/H3"]
  Classifiers --> Eval["Eval harness & schema checks"]
  Eval --> CI["GitHub Actions workflows"]
  CI --> MLflow["MLflow registry"]

  %% Jessica - annoteringskedja
  Plan["Plan & backlog"] --> Testplan["Testplan skeleton"]
  Testplan --> Schema["Schema-granskning"]
  Schema --> Guidelines["Annoteringsriktlinjer (v1)"]

  Guidelines --> TestApp["Testa Streamlit MVP"]
  TestApp --> AnnotPass["Första annoteringspass"]
  AnnotPass --> Log["Annoteringslogg"]
  Log --> Feedback["Feedback loop"]

  AnnotPass --> QA["QA-rutin"]
  QA --> Onboard["Onboardingplan annotatörer"]
  Onboard --> Train2["Träning med 2 annoterare"]
  Train2 --> Gold["Första Gold-versionen"]
  Gold --> Review["Sprint Review (mini)"]
