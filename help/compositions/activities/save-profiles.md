---
audience: end-user
title: Utilizzare l’attività Salva profili
description: Scopri come utilizzare l’attività Salva profili
exl-id: 1c840838-32d5-4ceb-8430-835a235b7436
source-git-commit: ca975be136155f69bc84362fde8c283b1c4edffe
workflow-type: tm+mt
source-wordcount: '374'
ht-degree: 18%

---

# Salva i profili {#save-profile}

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile"
>title="Salva i profili"
>abstract="L’attività Salva profili consente di arricchire i profili di Experience Platform mediante la federazione di dati provenienti da warehouse esterni, in modo da migliorare i profili clienti con attributi aggiuntivi. "

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_aepschemalist"
>title="Seleziona schema Experience Platform"
>abstract="Scegli lo schema Experience Platform per i profili."

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_primaryidentitynamespace"
>title="Seleziona campo dell’identità primaria"
>abstract="Seleziona l’identità primaria da utilizzare per identificare i profili target nel database."

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_selectaepschema"
>title="Seleziona schema Experience Platform"
>abstract="Scegli lo schema Experience Platform per i profili."

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_updatemode"
>title="Modalità di aggiornamento Salva profilo"
>abstract="Le modalità di aggiornamento disponibili per l’attività Save profile includono l’aggiornamento completo e l’aggiornamento incrementale."

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_updatemode_full"
>title="Aggiornamento completo"
>abstract="La modalità di aggiornamento completo aggiorna l’intero set di profili per l’arricchimento."

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_updatemode_incremental"
>title="Aggiornamento incrementale"
>abstract="La modalità di aggiornamento incrementale aggiorna i profili che sono stati modificati dall’ultima esecuzione dell’arricchimento."

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_primaryidentityfield"
>title="Campo dell’identità primaria"
>abstract="Il campo dell’identità primaria indica la fonte di verità quando si uniscono i profili per l’arricchimento."

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_requiredfieldscheck"
>title="Criteri dei campi obbligatori"
>abstract="Un campo obbligatorio è un attributo che deve essere compilato per ogni profilo o record durante l’esportazione dei dati. Se manca un campo obbligatorio, l’esportazione non sarà completa o valida."

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_primaryidentitycheck"
>title="Criteri del campo di identità primaria"
>abstract="L’identificatore univoco di ciascun profilo o record. In questo modo, ogni record può essere riconosciuto e abbinato in modo distinto, evitando la duplicazione dei dati."

L&#39;attività **Salva profili** consente di arricchire i profili Adobe Experience Platform con dati federati da warehouse esterni.

Questa attività viene generalmente utilizzata per migliorare i profili dei clienti inserendo attributi e informazioni aggiuntivi senza spostare o duplicare fisicamente i dati nella piattaforma.

## Configurare l’attività Salva profili {#save-profile-configuration}

Segui questi passaggi per configurare l&#39;attività **Salva profili**:

1. Aggiungi un&#39;attività **Salva profili** alla composizione.

   ![](../assets/save-profile.png)

1. Specifica l’etichetta dei profili da creare.

   >[!IMPORTANT]
   >
   >L’etichetta del pubblico deve essere univoca nella sandbox corrente. Non può essere la stessa etichetta di un pubblico esistente.

1. Seleziona lo schema Adobe Experience Platform da utilizzare.

   ![](../assets/save-profile-2.png)

1. Scegli il campo di identità principale che verrà utilizzato per identificare i profili nel database.

1. Se si desidera riconciliare attributi di dati aggiuntivi, fare clic su **Aggiungi attributi**.

   Quindi, specifica il campo **Source** (dati esterni) e il campo **Destination** (campo schema) per ogni attributo che desideri mappare.

   ![](../assets/save-profile-3.png)

1. Una volta configurata, fai clic su **Inizio**.
