```mermaid
graph TD

  subgraph V1 [Vecka1]
    Repo["Repo-struktur"]:::emil
    Azure["Azure Storage setup"]:::emil
    Plan["Plan & backlog"]:::jessica
  end

  subgraph V2 [Vecka2]
    Streamlit["Streamlit-MVP"]:::emil
    TestApp["Testa Streamlit MVP"]:::jessica
  end

  Repo --> Azure
  Plan --> TestApp
  Streamlit --> TestApp

  classDef emil fill=#87CEEB,stroke=#1E90FF,color=#000;
  classDef jessica fill=#90EE90,stroke=#228B22,color=#000;

```mermaid
