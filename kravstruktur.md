```mermaid
graph BT

  %% ========= Noder =========
  %% Capabilities (överst)
  C_Dokumentextrahering["Dokumentextrahering<br/>IM31"]
  C_Klassificering___hierarkier["Klassificering & hierarkier<br/>IM31"]
  C_Milj___lagring_i_molnet["Miljö & lagring i molnet<br/>IM31"]
  C_Modelltr_ning___utv_rdering["Modellträning & utvärdering<br/>IM31"]
  C_Annotering___feedback["Annotering & feedback<br/>IM31"]

  %% Features (mitten)
  F_Extrahera_PDF_med_ontologi_Feature_2_1_["Extrahera PDF med ontologi (Feature 2.1)<br/>IM41"]
  F_Klassificera_mot_Prime_Arch_Feature_5_1_["Klassificera mot Prime Arch (Feature 5.1)<br/>IM41"]
  F_Spara_filer_och_data_i_molnet_Feature_1_2_["Spara filer och data i molnet (Feature 1.2)<br/>IM41"]
  F_Retrain_modellen_Feature_4_1_["Retrain modellen (Feature 4.1)<br/>IM41"]
  F_Okategoriserat["Okategoriserat<br/>IM41"]
  F_Annotera_i_molnet_Feature_3_1_["Annotera i molnet (Feature 3.1)<br/>IM41"]
  F_Redigera_annoteringar_feature_3_2___["Redigera annoteringar (feature 3.2)<br/>IM41"]

  %% Stories (nederst)
  S_Paragrafer_identifieras_som_hela_stycken["Jag som annotator vill att paragrafer identifieras som hela stycken i PDF:en så att jag kan annotera per stycke<br/>IM51"]
  S_Annotera_enskilda_paragrafer["Jag som annotator vill kunna annotera enskilda paragrafer i det extraherade PDF‑innehållet så att jag kan ge feedback<br/>IM51"]
  S_Bygga_hierarkisk_labelstruktur["Jag som administratör vill att systemet bygger en hierarkisk label‑struktur enligt Prime Arch så att dokument kan hittas<br/>IM51"]
  S_Konfigurera_mappning_PrimeArch["Jag som administratör vill kunna konfigurera mappning mellan interna etiketter och Prime Arch‑noder<br/>IM51"]
  S_L_sa_upp_sparad_annotering["Jag som administratör vill kunna läsa upp en sparad annotering från blob‑lagring för att granska<br/>IM51"]
  S_K_ra_retrain_jobbet["Jag som administratör vill kunna köra retrain‑jobbet för att förbättra modellen<br/>IM51"]
  S_Hantera_lagringsplats_och_atkomst["Jag som administratör vill kunna hantera varje fils lagringsplats och åtkomst<br/>IM51"]
  S_Annotera_i_webbgr_nssnitt["Jag som annotator vill kunna annotera direkt i webbgränssnittet<br/>IM51"]
  S_Redigera_tidigare_annoteringar["Jag som annotator vill kunna redigera tidigare gjorda annoteringar<br/>IM51"]

  %% ========= Relationer =========
  %% Feature → Capability ("ingår i")
  F_Extrahera_PDF_med_ontologi_Feature_2_1_ -- "ingår i" --> C_Dokumentextrahering
  F_Klassificera_mot_Prime_Arch_Feature_5_1_ -- "ingår i" --> C_Klassificering___hierarkier
  F_Spara_filer_och_data_i_molnet_Feature_1_2_ -- "ingår i" --> C_Milj___lagring_i_molnet
  F_Retrain_modellen_Feature_4_1_ -- "ingår i" --> C_Modelltr_ning___utv_rdering
  F_Okategoriserat -- "ingår i" --> C_Milj___lagring_i_molnet
  F_Annotera_i_molnet_Feature_3_1_ -- "ingår i" --> C_Annotering___feedback
  F_Redigera_annoteringar_feature_3_2___ -- "ingår i" --> C_Annotering___feedback

  %% Story → Feature ("ingår i")
  S_Paragrafer_identifieras_som_hela_stycken -- "ingår i" --> F_Extrahera_PDF_med_ontologi_Feature_2_1_
  S_Annotera_enskilda_paragrafer -- "ingår i" --> F_Extrahera_PDF_med_ontologi_Feature_2_1_
  S_Bygga_hierarkisk_labelstruktur -- "ingår i" --> F_Klassificera_mot_Prime_Arch_Feature_5_1_
  S_Konfigurera_mappning_PrimeArch -- "ingår i" --> F_Klassificera_mot_Prime_Arch_Feature_5_1_
  S_L_sa_upp_sparad_annotering -- "ingår i" --> F_Spara_filer_och_data_i_molnet_Feature_1_2_
  S_K_ra_retrain_jobbet -- "ingår i" --> F_Retrain_modellen_Feature_4_1_
  S_Hantera_lagringsplats_och_atkomst -- "ingår i" --> F_Okategoriserat
  S_Annotera_i_webbgr_nssnitt -- "ingår i" --> F_Annotera_i_molnet_Feature_3_1_
  S_Redigera_tidigare_annoteringar -- "ingår i" --> F_Redigera_annoteringar_feature_3_2___

  %% ========= Färgklasser =========
  classDef capability fill:#C5CDE9,stroke:#222,color:#000;
  classDef feature fill:#C5CDE9,stroke:#222,color:#000;
  classDef story fill:#C5CDE9,stroke:#222,color:#000;

  class C_Dokumentextrahering,C_Klassificering___hierarkier,C_Milj___lagring_i_molnet,C_Modelltr_ning___utv_rdering,C_Annotering___feedback capability;
  class F_Extrahera_PDF_med_ontologi_Feature_2_1_,F_Klassificera_mot_Prime_Arch_Feature_5_1_,F_Spara_filer_och_data_i_molnet_Feature_1_2_,F_Retrain_modellen_Feature_4_1_,F_Okategoriserat,F_Annotera_i_molnet_Feature_3_1_,F_Redigera_annoteringar_feature_3_2___ feature;
  class S_Paragrafer_identifieras_som_hela_stycken,S_Annotera_enskilda_paragrafer,S_Bygga_hierarkisk_labelstruktur,S_Konfigurera_mappning_PrimeArch,S_L_sa_upp_sparad_annotering,S_K_ra_retrain_jobbet,S_Hantera_lagringsplats_och_atkomst,S_Annotera_i_webbgr_nssnitt,S_Redigera_tidigare_annoteringar story;
```mermaid
