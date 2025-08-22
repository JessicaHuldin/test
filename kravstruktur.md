```mermaid
graph TD
  %% Noder och subgrafer
  subgraph CAP["Capability: Dokumentextrahering"]
  C_Dokumentextrahering["Dokumentextrahering"]
    subgraph FEAT_Extrahera_PDF_med_ontologi_Feature_2_1_["Feature: Extrahera PDF med ontologi (Feature 2.1)"]
    F_Extrahera_PDF_med_ontologi_Feature_2_1_["Extrahera PDF med ontologi (Feature 2.1)"]
    S_Jag_som_annotator_vill_att_paragrafer_identifieras_som_hela_styc["Jag som annotator vill att paragrafer identifieras som hela stycken i PDF:en så att jag kan annotera per stycke"]
    S_Jag_som_annotator_vill_kunna_annotera_enskilda_paragrafer_i_det["Jag som annotator vill kunna annotera enskilda paragrafer i det extraherade PDF‑innehållet så att jag kan ge feedback"]
    end
  end
  subgraph CAP["Capability: Klassificering & hierarkier"]
  C_Klassificering___hierarkier["Klassificering & hierarkier"]
    subgraph FEAT_Klassificera_mot_Prime_Arch_Feature_5_1_["Feature: Klassificera mot Prime Arch (Feature 5.1)"]
    F_Klassificera_mot_Prime_Arch_Feature_5_1_["Klassificera mot Prime Arch (Feature 5.1)"]
    S_Jag_som_administrat_r_vill_att_systemet_bygger_en_hierarkisk_l["Jag som administratör vill att systemet bygger en hierarkisk label‑struktur enligt Prime Arch så att dokument kan hittas"]
    S_Jag_som_administrat_r_vill_kunna_konfigurera_mappning_mellan_["Jag som administratör vill kunna konfigurera mappning mellan interna etiketter och Prime Arch‑noder"]
    end
  end
  subgraph CAP["Capability: Miljö & lagring i molnet"]
  C_Milj___lagring_i_molnet["Miljö & lagring i molnet"]
    subgraph FEAT_Spara_filer_och_data_i_molnet_Feature_1_2_["Feature: Spara filer och data i molnet (Feature 1.2)"]
    F_Spara_filer_och_data_i_molnet_Feature_1_2_["Spara filer och data i molnet (Feature 1.2)"]
    S_Jag_som_administrat_r_vill_kunna_l_sa_upp_en_sparad_annoterin["Jag som administratör vill kunna läsa upp en sparad annotering från blob‑lagring för att granska"]
    end
  end
  subgraph CAP["Capability: Modellträning & utvärdering"]
  C_Modelltr_ning___utv_rdering["Modellträning & utvärdering"]
    subgraph FEAT_Retrain_modellen_Feature_4_1_["Feature: Retrain modellen (Feature 4.1)"]
    F_Retrain_modellen_Feature_4_1_["Retrain modellen (Feature 4.1)"]
    S_Jag_som_administrat_r_vill_kunna_k_ra_retrain_jobbet_f_r_att["Jag som administratör vill kunna köra retrain‑jobbet för att förbättra modellen"]
    end
  end
  subgraph CAP["Capability: Miljö & lagring i molnet"]
  C_Milj___lagring_i_molnet_1["Miljö & lagring i molnet"]
    subgraph FEAT_Okategoriserat["Feature: Okategoriserat"]
    F_Okategoriserat["Okategoriserat"]
    S_Jag_som_administrat_r_vill_kunna_hantera_varje_fils_lagringsp["Jag som administratör vill kunna hantera varje fils lagringsplats och åtkomst"]
    end
  end
  subgraph CAP["Capability: Annotering & feedback"]
  C_Annotering___feedback["Annotering & feedback"]
    subgraph FEAT_Annotera_i_molnet_Feature_3_1_["Feature: Annotera i molnet (Feature 3.1)"]
    F_Annotera_i_molnet_Feature_3_1_["Annotera i molnet (Feature 3.1)"]
    S_Jag_som_annotator_vill_kunna_annotera_direkt_i_webbgr_nssnitt["Jag som annotator vill kunna annotera direkt i webbgränssnittet"]
    end
    subgraph FEAT_Redigera_annoteringar_feature_3_2__["Feature: Redigera annoteringar (feature 3.2)"]
    F_Redigera_annoteringar_feature_3_2___["Redigera annoteringar (feature 3.2)"]
    S_Jag_som_annotator_vill_kunna_redigera_tidigare_gjorda_annoter["Jag som annotator vill kunna redigera tidigare gjorda annoteringar"]
    end
  end

  %% Färgklasser
  classDef story fill:#C5CDE9,stroke:#222,color:#000;
  classDef feature fill:#C5CDE9,stroke:#222,color:#000;
  classDef capability fill:#C5CDE9,stroke:#222,color:#000;

  %% Klasskoppling
  class S_Jag_som_administrat_r_vill_att_systemet_bygger_en_hierarkisk_l,S_Jag_som_administrat_r_vill_kunna_hantera_varje_fils_lagringsp,S_Jag_som_administrat_r_vill_kunna_k_ra_retrain_jobbet_f_r_att,S_Jag_som_administrat_r_vill_kunna_konfigurera_mappning_mellan_,S_Jag_som_administrat_r_vill_kunna_l_sa_upp_en_sparad_annoterin,S_Jag_som_annotator_vill_att_paragrafer_identifieras_som_hela_styc,S_Jag_som_annotator_vill_kunna_annotera_direkt_i_webbgr_nssnitt,S_Jag_som_annotator_vill_kunna_annotera_enskilda_paragrafer_i_det,S_Jag_som_annotator_vill_kunna_redigera_tidigare_gjorda_annoter story;
  class F_Annotera_i_molnet_Feature_3_1_,F_Extrahera_PDF_med_ontologi_Feature_2_1_,F_Klassificera_mot_Prime_Arch_Feature_5_1_,F_Okategoriserat,F_Redigera_annoteringar_feature_3_2___,F_Retrain_modellen_Feature_4_1_,F_Spara_filer_och_data_i_molnet_Feature_1_2_ feature;
  class C_Annotering___feedback,C_Dokumentextrahering,C_Klassificering___hierarkier,C_Milj___lagring_i_molnet,C_Milj___lagring_i_molnet_1,C_Modelltr_ning___utv_rdering capability;

  %% Relationer
  F_Extrahera_PDF_med_ontologi_Feature_2_1_ -- "ingår i" --> C_Dokumentextrahering
  S_Jag_som_annotator_vill_att_paragrafer_identifieras_som_hela_styc -- "ingår i" --> F_Extrahera_PDF_med_ontologi_Feature_2_1_
  S_Jag_som_annotator_vill_kunna_annotera_enskilda_paragrafer_i_det -- "ingår i" --> F_Extrahera_PDF_med_ontologi_Feature_2_1_
  F_Klassificera_mot_Prime_Arch_Feature_5_1_ -- "ingår i" --> C_Klassificering___hierarkier
  S_Jag_som_administrat_r_vill_att_systemet_bygger_en_hierarkisk_l -- "ingår i" --> F_Klassificera_mot_Prime_Arch_Feature_5_1_
  S_Jag_som_administrat_r_vill_kunna_konfigurera_mappning_mellan_ -- "ingår i" --> F_Klassificera_mot_Prime_Arch_Feature_5_1_
  F_Spara_filer_och_data_i_molnet_Feature_1_2_ -- "ingår i" --> C_Milj___lagring_i_molnet
  S_Jag_som_administrat_r_vill_kunna_l_sa_upp_en_sparad_annoterin -- "ingår i" --> F_Spara_filer_och_data_i_molnet_Feature_1_2_
  F_Retrain_modellen_Feature_4_1_ -- "ingår i" --> C_Modelltr_ning___utv_rdering
  S_Jag_som_administrat_r_vill_kunna_k_ra_retrain_jobbet_f_r_att -- "ingår i" --> F_Retrain_modellen_Feature_4_1_
  F_Okategoriserat -- "ingår i" --> C_Milj___lagring_i_molnet_1
  S_Jag_som_administrat_r_vill_kunna_hantera_varje_fils_lagringsp -- "ingår i" --> F_Okategoriserat
  F_Annotera_i_molnet_Feature_3_1_ -- "ingår i" --> C_Annotering___feedback
  S_Jag_som_annotator_vill_kunna_annotera_direkt_i_webbgr_nssnitt -- "ingår i" --> F_Annotera_i_molnet_Feature_3_1_
  F_Redigera_annoteringar_feature_3_2___ -- "ingår i" --> C_Annotering___feedback
  S_Jag_som_annotator_vill_kunna_redigera_tidigare_gjorda_annoter -- "ingår i" --> F_Redigera_annoteringar_feature_3_2___
```mermaid
