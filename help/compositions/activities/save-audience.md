---
audience: end-user
title: Utilizzare l’attività Save audience
description: Scopri come utilizzare l’attività Save audience
source-git-commit: 6b7a0ae164bdb09b1f5fc067a13e304eec9c5201
workflow-type: tm+mt
source-wordcount: '358'
ht-degree: 26%

---


# Salvare il pubblico {#save-audience}

>[!CONTEXTUALHELP]
>id="dc_orchestration_save_audience"
>title="Salva un pubblico"
>abstract="Utilizza questa attività per aggiornare un pubblico esistente o crearne uno nuovo dalla popolazione calcolata a monte nella composizione. I tipi di pubblico creati vengono aggiunti all’elenco dei tipi di pubblico e sono disponibili tramite il menu **Tipi di pubblico**."

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveaudience_outbound"
>title="Genera transizione in uscita"
>abstract="Utilizza questa opzione se desideri aggiungere una transizione dopo l’attività **Salva pubblico**."

>[!CONTEXTUALHELP]
>id="dc_orchestration_save_audience_primary_identity"
>title="Campo identità primaria"
>abstract="Seleziona l’identità principale da utilizzare per i profili."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-platform/xdm/ui/fields/identity#define-a-identity-field" text="Ulteriori informazioni sono disponibili nella documentazione di Experience Platform"

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveaudience_namespace"
>title="Spazio dei nomi identità"
>abstract="Seleziona lo spazio dei nomi da utilizzare per i profili."
>additional-url="https://experienceleague.adobe.com/it/docs/experience-platform/identity/features/namespaces" text="Ulteriori informazioni sono disponibili nella documentazione di Experience Platform"

Il **Salva pubblico** attività ti consente di aggiornare un pubblico esistente o crearne uno nuovo dalla popolazione calcolata a monte in una composizione. I tipi di pubblico creati vengono aggiunti all’elenco dei tipi di pubblico delle applicazioni e sono disponibili tramite il menu **Tipi di pubblico**.

Questa attività è essenzialmente utilizzata per mantenere i gruppi di popolazione calcolati nella stessa composizione, convertendoli in tipi di pubblico riutilizzabili. Connettila ad altre attività di targeting, come a un’attività **Crea pubblico** o **Combina**.

## Configurare l’attività Salva pubblico {#save-audience-configuration}

Per configurare l’attività **Salva pubblico**, segui questi passaggi:

1. Aggiungi un **Salva pubblico** alla tua composizione.

   ![](../assets/save-audience.png)

1. Specifica l’etichetta del pubblico da creare.

1. Clic **Aggiungi mappatura pubblico** quindi scegli i campi pubblico di origine e di destinazione:

   * **Campo pubblico Source**:
   * **Campo pubblico di destinazione**:

   Ripeti l’operazione per aggiungere tutte le mappature del pubblico necessarie.

1. Seleziona l’identità principale e lo spazio dei nomi da utilizzare per identificare i profili target nel database:

   * **Campo di identità primaria**: seleziona il campo da utilizzare per identificare i profili. Ad esempio, l’indirizzo e-mail o il numero di telefono.
   * **Spazio dei nomi dell’identità**: seleziona lo spazio dei nomi da utilizzare per identificare i profili, ovvero il tipo di dati da utilizzare come chiave di identificazione. Ad esempio, se l’indirizzo e-mail è stato selezionato come campo di identità principale, lo spazio dei nomi dell’identità **E-mail** deve essere selezionato. Se l’identificatore univoco è il numero di telefono, allora lo spazio dei nomi dell’identità **Telefono** deve essere selezionato.

Dopo aver eseguito la composizione, il pubblico risultante viene salvato in Adobe Experience Platform <!-- to check-->, e resi accessibili nel **Tipi di pubblico** menu.

<!--

## Example{#save-audience-example}

The following example illustrates a simple audience update from targeting. A scheduler is added to run the workflow once a month. A query recovers all the profiles subscribed to the different application services available. The **Save audience** activity updates the audience by deleting profiles that have unsubscribed from the service since the last workflow execution and by adding the newly subscribed profiles.
-->
