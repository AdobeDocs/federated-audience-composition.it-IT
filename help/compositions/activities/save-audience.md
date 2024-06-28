---
audience: end-user
title: Utilizzare l’attività Save audience
description: Scopri come utilizzare l’attività Fork
source-git-commit: 05a023a7f7aab719f3771030a7ac8bba57e5bee3
workflow-type: tm+mt
source-wordcount: '405'
ht-degree: 67%

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

1. Nell’elenco a discesa **Modalità**, seleziona l’azione da eseguire:

   * **Crea o aggiorna un pubblico esistente**: definisci un’**etichetta del pubblico**. Se il pubblico esiste già, verrà aggiornato; altrimenti verrà creato un nuovo pubblico.

   * **Aggiorna un pubblico esistente**: scegli il **Pubblico** che desideri aggiornare dall’elenco dei tipi di pubblico esistenti.

1. Seleziona la **Modalità di aggiornamento** che verrà applicata ai tipi di pubblico esistenti:

   * **Sostituisci il contenuto del pubblico con nuovi dati**: viene sostituito tutto il contenuto del pubblico. I vecchi dati vanno perduti. Vengono conservati solo i dati della transizione in entrata dell’attività Salva pubblico. Questa opzione elimina il tipo di pubblico e la dimensione di targeting del pubblico aggiornato.

   * **Completa il pubblico con i nuovi dati**: il vecchio contenuto del pubblico viene conservato e vi vengono aggiunti i dati della transizione in entrata dell’attività Salva pubblico.

1. Seleziona l’opzione **Genera una transizione in uscita** se desideri aggiungere una transizione dopo l’attività **Salva pubblico**.

Il contenuto del pubblico salvato è quindi disponibile nella relativa visualizzazione dettagliata, accessibile dal menu **Tipi di pubblico**. Le colonne disponibili in questa visualizzazione corrispondono alle colonne della transizione in entrata della **Salva pubblico** attività.

<!--

## Example{#save-audience-example}

The following example illustrates a simple audience update from targeting. A scheduler is added to run the workflow once a month. A query recovers all the profiles subscribed to the different application services available. The **Save audience** activity updates the audience by deleting profiles that have unsubscribed from the service since the last workflow execution and by adding the newly subscribed profiles.
-->
