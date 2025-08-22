```mermaid
graph BT

  %% ===== Epic =====
  subgraph EpicA["Epic A<br/>IM21"]

    %% Capabilities (överst)
    C_Annotering___feedback["Annotering & feedback<br/>IM31"]
    C_Dokumentextrahering["Dokumentextrahering<br/>IM31"]
    C_Klassificering___hierarkier["Klassificering & hierarkier<br/>IM31"]
    C_Milj___lagring_i_molnet["Miljö & lagring i molnet<br/>IM31"]
    C_Modelltr_ning___utv_rdering["Modellträning & utvärdering<br/>IM31"]
    C_Prime_Arch_integrering["Prime Arch integrering<br/>IM31"]
    C_Systemadministration["Systemadministration<br/>IM31"]

    %% Features (mitten)
    F_Annotera_i_molnet_Feature_3_1_["Annotera i molnet (Feature 3.1)<br/>IM41"]
    F_Extrahera_PDF_med_ontologi_Feature_2_1_["Extrahera PDF med ontologi (Feature 2.1)<br/>IM41"]
    F_Klassificera_mot_Prime_Arch_Feature_5_1_["Klassificera mot Prime Arch (Feature 5.1)<br/>IM41"]
    F_Okategoriserat["Okategoriserat<br/>IM41"]
    F_Redigera_annoteringar_feature_3_2___["Redigera annoteringar (feature 3.2)<br/>IM41"]
    F_Retrain_modellen_Feature_4_1_["Retrain modellen (Feature 4.1)<br/>IM41"]
    F_S_para_filer_och_data_i_molnet_Feature_1_2_["Spara filer och data i molnet (Feature 1.2)<br/>IM41"]
    F_Systemh_llbarhet_Feature_6_3_["Systemhållbarhet (Feature 6.3)<br/>IM41"]
    F_Tillg_nglighet_Feature_7_2_["Tillgänglighet (Feature 7.2)<br/>IM41"]

    %% Stories (nederst)
    S_Jag_som_annotator_vill_att_paragrafer_identifieras_som_hela_styc["Jag som annotator vill att paragrafer identifieras som hela stycken i PDF:en så att jag kan annotera per stycke<br/>IM51"]
    S_Jag_som_annotator_vill_kunna_annotera_enskilda_paragrafer_i_det["Jag som annotator vill kunna annotera enskilda paragrafer i det extraherade PDF-innehållet så att jag kan ge feedback<br/>IM51"]
    S_Jag_som_annotator_vill_kunna_annotera_direkt_i_webbgr_nssnitt["Jag som annotator vill kunna annotera direkt i webbgränssnittet<br/>IM51"]
    S_Jag_som_annotator_vill_kunna_redigera_tidigare_gjorda_annoter["Jag som annotator vill kunna redigera tidigare gjorda annoteringar<br/>IM51"]
    S_Jag_som_administrat_r_vill_att_systemet_bygger_en_hierarkisk_l["Jag som administratör vill att systemet bygger en hierarkisk label-struktur enligt Prime Arch så att dokument kan hittas<br/>IM51"]
    S_Jag_som_administrat_r_vill_kunna_konfigurera_mappning_mellan_["Jag som administratör vill kunna konfigurera mappning mellan interna etiketter och Prime Arch-noder<br/>IM51"]
    S_Jag_som_administrat_r_vill_kunna_l_sa_upp_en_sparad_annoterin["Jag som administratör vill kunna läsa upp en sparad annotering från blob-lagring för att granska<br/>IM51"]
    S_Jag_som_administrat_r_vill_kunna_k_ra_retrain_jobbet_f_r_att["Jag som administratör vill kunna köra retrain-jobbet för att förbättra modellen<br/>IM51"]
    S_Jag_som_administrat_r_vill_kunna_hantera_varje_fils_lagringsp["Jag som administratör vill kunna hantera varje fils lagringsplats och åtkomst<br/>IM51"]
    S_Jag_som_dokument_gare_vill_kunna_exportera_annoteringar_som_CSV["Jag som dokumentägare vill kunna exportera annoteringar som CSV för vidare analys<br/>IM51"]
    S_Jag_som_dokument_gare_vill_kunna_l_gga_till_och_ta_bort_komme["Jag som dokumentägare vill kunna lägga till och ta bort kommentarer på annoteringar<br/>IM51"]
    S_Jag_som_systemadministrat_r_vill_kunna_audit_logga_viktiga_h["Jag som systemadministratör vill kunna audit-logga viktiga händelser i systemet<br/>IM51"]
    S_Jag_som_systemadministrat_r_vill_kunna_configurera_rollbaser["Jag som systemadministratör vill kunna konfigurera rollbaserad åtkomst (RBAC)<br/>IM51"]
    S_Prime_Arch_synk_ska_kunna_k_ras_nattetid["Prime-Arch-synk ska kunna köras nattetid<br/>IM51"]
    S_Systemet_ska_klara_av_5000_aktiva_dokument_utan_perf_tapp["Systemet ska klara av 5000 aktiva dokument utan perf-tapp<br/>IM51"]
    S_UI_ska_uppfylla_WCAG_2_1_AA["UI ska uppfylla WCAG 2.1 AA<br/>IM51"]
    S_Uppladdningsfl_det_ska_hantera_100MB_PDFer["Uppladdningsflödet ska hantera 100MB PDFer<br/>IM51"]
    S__versyn_av_lagringsklasser_ska_genomf_ras_kvartalsvis["Översyn av lagringsklasser ska genomföras kvartalsvis<br/>IM51"]
    S__vervakning_med_larm_ska_finnas_f_r_kritiska_tj_nster["Övervakning med larm ska finnas för kritiska tjänster<br/>IM51"]
    S__vervaka_blob_lagring_f_r_kostnadsoptimering["Övervaka blob-lagring för kostnadsoptimering<br/>IM51"]
    S__vervaka_molnresurser_f_r_h_llbarhet["Övervaka molnresurser för hållbarhet<br/>IM51"]
    S__vervaka_tillg_nglighet_och_sla["Övervaka tillgänglighet och SLA<br/>IM51"]
    S__vervaka_tillg_nglighet_per_region["Övervaka tillgänglighet per region<br/>IM51"]
    S__verv_kning_av_systemets_milj_p_verkan["Överväkning av systemets miljöpåverkan<br/>IM51"]

  end

  %% ===== Relationer =====
  F_Annotera_i_molnet_Feature_3_1_ -- "ingår i" --> C_Annotering___feedback
  F_Extrahera_PDF_med_ontologi_Feature_2_1_ -- "ingår i" --> C_Dokumentextrahering
  F_Klassificera_mot_Prime_Arch_Feature_5_1_ -- "ingår i" --> C_Klassificering___hierarkier
  F_Okategoriserat -- "ingår i" --> C_Milj___lagring_i_molnet
  F_Redigera_annoteringar_feature_3_2___ -- "ingår i" --> C_Annotering___feedback
  F_Retrain_modellen_Feature_4_1_ -- "ingår i" --> C_Modelltr_ning___utv_rdering
  F_S_para_filer_och_data_i_molnet_Feature_1_2_ -- "ingår i" --> C_Milj___lagring_i_molnet
  F_Systemh_llbarhet_Feature_6_3_ -- "ingår i" --> C_Systemadministration
  F_Tillg_nglighet_Feature_7_2_ -- "ingår i" --> C_Prime_Arch_integrering

  S_Jag_som_annotator_vill_att_paragrafer_identifieras_som_hela_styc -- "ingår i" --> F_Extrahera_PDF_med_ontologi_Feature_2_1_
  S_Jag_som_annotator_vill_kunna_annotera_enskilda_paragrafer_i_det -- "ingår i" --> F_Extrahera_PDF_med_ontologi_Feature_2_1_
  S_Jag_som_annotator_vill_kunna_annotera_direkt_i_webbgr_nssnitt -- "ingår i" --> F_Annotera_i_molnet_Feature_3_1_
  S_Jag_som_annotator_vill_kunna_redigera_tidigare_gjorda_annoter -- "ingår i" --> F_Redigera_annoteringar_feature_3_2___
  S_Jag_som_administrat_r_vill_att_systemet_bygger_en_hierarkisk_l -- "ingår i" --> F_Klassificera_mot_Prime_Arch_Feature_5_1_
  S_Jag_som_administrat_r_vill_kunna_konfigurera_mappning_mellan_ -- "ingår i" --> F_Klassificera_mot_Prime_Arch_Feature_5_1_
  S_Jag_som_administrat_r_vill_kunna_l_sa_upp_en_sparad_annoterin -- "ingår i" --> F_S_para_filer_och_data_i_molnet_Feature_1_2_
  S_Jag_som_administrat_r_vill_kunna_k_ra_retrain_jobbet_f_r_att -- "ingår i" --> F_Retrain_modellen_Feature_4_1_
  S_Jag_som_administrat_r_vill_kunna_hantera_varje_fils_lagringsp -- "ingår i" --> F_Okategoriserat
  S_Jag_som_dokument_gare_vill_kunna_exportera_annoteringar_som_CSV -- "ingår i" --> F_Okategoriserat
  S_Jag_som_dokument_gare_vill_kunna_l_gga_till_och_ta_bort_komme -- "ingår i" --> F_Okategoriserat
  S_Jag_som_systemadministrat_r_vill_kunna_audit_logga_viktiga_h -- "ingår i" --> F_Systemh_llbarhet_Feature_6_3_
  S_Jag_som_systemadministrat_r_vill_kunna_configurera_rollbaser -- "ingår i" --> F_Systemh_llbarhet_Feature_6_3_
  S_Prime_Arch_synk_ska_kunna_k_ras_nattetid -- "ingår i" --> F_Tillg_nglighet_Feature_7_2_
  S_Systemet_ska_klara_av_5000_aktiva_dokument_utan_perf_tapp -- "ingår i" --> F_Systemh_llbarhet_Feature_6_3_
  S_UI_ska_uppfylla_WCAG_2_1_AA -- "ingår i" --> F_Tillg_nglighet_Feature_7_2_
  S_Uppladdningsfl_det_ska_hantera_100MB_PDFer -- "ingår i" --> F_S_para_filer_och_data_i_molnet_Feature_1_2_
  S__versyn_av_lagringsklasser_ska_genomf_ras_kvartalsvis -- "ingår i" --> F_Systemh_llbarhet_Feature_6_3_
  S__vervakning_med_larm_ska_finnas_f_r_kritiska_tj_nster -- "ingår i" --> F_Tillg_nglighet_Feature_7_2_
  S__vervaka_blob_lagring_f_r_kostnadsoptimering -- "ingår i" --> F_Systemh_llbarhet_Feature_6_3_
  S__vervaka_molnresurser_f_r_h_llbarhet -- "ingår i" --> F_Systemh_llbarhet_Feature_6_3_
  S__vervaka_tillg_nglighet_och_sla -- "ingår i" --> F_Tillg_nglighet_Feature_7_2_
  S__vervaka_tillg_nglighet_per_region -- "ingår i" --> F_Tillg_nglighet_Feature_7_2_
  S__verv_kning_av_systemets_milj_p_verkan -- "ingår i" --> F_Systemh_llbarhet_Feature_6_3_

  %% ===== Färgklasser =====
  classDef capability fill:#C5CDE9,stroke:#222,color:#000;
  classDef feature fill:#C5CDE9,stroke:#222,color:#000;
  classDef story fill:#C5CDE9,stroke:#222,color:#000;
  classDef epic fill:#C5CDE9,stroke:#000,color:#000,stroke-dasharray: 5 5;

  class C_Annotering___feedback,C_Dokumentextrahering,C_Klassificering___hierarkier,C_Milj___lagring_i_molnet,C_Modelltr_ning___utv_rdering,C_Prime_Arch_integrering,C_Systemadministration capability;
  class F_Annotera_i_molnet_Feature_3_1_,F_Extrahera_PDF_med_ontologi_Feature_2_1_,F_Klassificera_mot_Prime_Arch_Feature_5_1_,F_Okategoriserat,F_Redigera_annoteringar_feature_3_2___,F_Retrain_modellen_Feature_4_1_,F_S_para_filer_och_data_i_molnet_Feature_1_2_,F_Systemh_llbarhet_Feature_6_3_,F_Tillg_nglighet_Feature_7_2_ feature;
  class S_Jag_som_annotator_vill_att_paragrafer_identifieras_som_hela_styc,S_Jag_som_annotator_vill_kunna_annotera_enskilda_paragrafer_i_det,S_Jag_som_annotator_vill_kunna_annotera_direkt_i_webbgr_nssnitt,S_Jag_som_annotator_vill_kunna_redigera_tidigare_gjorda_annoter,S_Jag_som_administrat_r_vill_att_systemet_bygger_en_hierarkisk_l,S_Jag_som_administrat_r_vill_kunna_konfigurera_mappning_mellan_,S_Jag_som_administrat_r_vill_kunna_l_sa_upp_en_sparad_annoterin,S_Jag_som_administrat_r_vill_kunna_k_ra_retrain_jobbet_f_r_att,S_Jag_som_administrat_r_vill_kunna_hantera_varje_fils_lagringsp,S_Jag_som_dokument_gare_vill_kunna_exportera_annoteringar_som_CSV,S_Jag_som_dokument_gare_vill_kunna_l_gga_till_och_ta_bort_komme,S_Jag_som_systemadministrat_r_vill_kunna_audit_logga_viktiga_h,S_Jag_som_systemadministrat_r_vill_kunna_configurera_rollbaser,S_Prime_Arch_synk_ska_kunna_k_ras_nattetid,S_Systemet_ska_klara_av_5000_aktiva_dokument_utan_perf_tapp,S_UI_ska_uppfylla_WCAG_2_1_AA,S_Uppladdningsfl_det_ska_hantera_100MB_PDFer,S__versyn_av_lagringsklasser_ska_genomf_ras_kvartalsvis,S__vervakning_med_larm_ska_finnas_f_r_kritiska_tj_nster,S__vervaka_blob_lagring_f_r_kostnadsoptimering,S__vervaka_molnresurser_f_r_h_llbarhet,S__vervaka_tillg_nglighet_och_sla,S__vervaka_tillg_nglighet_per_region,S__verv_kning_av_systemets_milj_p_verkan story;
  class EpicA epic;
```mermaid
