---
audience: end-user
title: Utilizzare l’attività Salva profili
description: Scopri come utilizzare l’attività Salva profili
source-git-commit: e1720d60f542d7f43986dbc7e6e40b83d0a524a1
workflow-type: tm+mt
source-wordcount: '238'
ht-degree: 0%

---

# Salvare profili {#save-profile}

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile"
>title="Salva i profili"
>abstract="L’attività Save Profiles ti consente di arricchire i profili Experience Platform unendo i dati provenienti da magazzini esterni, per migliorare i profili dei clienti con attributi aggiuntivi. "

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_aepschemalist"
>title="Seleziona schema AEP"
>abstract="Scegli lo schema Experience Platform per i profili."

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_primaryidentitynamespace"
>title="Seleziona il campo di identificazione principale"
>abstract="Seleziona l’identità primaria da utilizzare per identificare i profili target nel database."

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_selectaepschema"
>title="Seleziona schema AEP"
>abstract="Scegli lo schema Experience Platform per i profili."

L&#39;attività **Salva profili** consente di arricchire i profili Adobe Experience Platform con dati federati da warehouse esterni.

Questa attività viene generalmente utilizzata per migliorare i profili dei clienti inserendo attributi e informazioni aggiuntivi senza spostare o duplicare fisicamente i dati nella piattaforma

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
