---
audience: end-user
title: Utilizzare l’attività Salva pubblico
description: Scopri come utilizzare l’attività Save audience
exl-id: fa67b1ee-8de6-4a71-b597-ade3f5587a38
source-git-commit: 3399de79baa5f8009b2ea6bfb084a5ce93f7a158
workflow-type: tm+mt
source-wordcount: '567'
ht-degree: 25%

---

# Salva pubblico {#save-audience}

>[!CONTEXTUALHELP]
>id="dc_orchestration_save_audience"
>title="Salva un pubblico"
>abstract="Utilizza questa attività per creare un pubblico nuovo dalla popolazione calcolata a monte nella composizione. I tipi di pubblico creati vengono aggiunti all’elenco dei tipi di pubblico e sono disponibili tramite il menu **Tipi di pubblico**."

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveaudience_outbound"
>title="Genera transizione in uscita"
>abstract="Utilizza questa opzione se desideri aggiungere una transizione dopo l’attività **Salva pubblico**."

>[!CONTEXTUALHELP]
>id="dc_orchestration_save_audience_primary_identity"
>title="Campo dell’identità primaria"
>abstract="Seleziona l’identità primaria da utilizzare per i profili."
>additional-url="https://experienceleague.adobe.com/it/docs/experience-platform/xdm/ui/fields/identity#define-a-identity-field" text="Ulteriori informazioni nella documentazione di Experience Platform"

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveaudience_namespace"
>title="Spazio dei nomi identità"
>abstract="Selezionare lo spazio dei nomi da utilizzare per i profili."
>additional-url="https://experienceleague.adobe.com/it/docs/experience-platform/identity/features/namespaces" text="Ulteriori informazioni nella documentazione di Experience Platform"

>[!IMPORTANT]
>
>Se il pubblico utilizza un criterio di unione **per la precedenza dei set di dati**, contatta l&#39;Assistenza clienti Adobe per aggiungere il set di dati `Halos UPS` al criterio di unione.
>
>Per ulteriori informazioni sui criteri di unione, leggere la [panoramica dei criteri di unione](https://experienceleague.adobe.com/it/docs/experience-platform/profile/merge-policies/overview).

L&#39;attività **[!UICONTROL Save audience]** ti consente di creare un nuovo pubblico dalla popolazione calcolata a monte in una composizione. I tipi di pubblico creati vengono aggiunti all&#39;elenco dei tipi di pubblico di Adobe Experience Platform e sono disponibili tramite il menu **Tipi di pubblico**. [Scopri come utilizzare i tipi di pubblico](../../start/audiences.md)

Questa attività è essenzialmente utilizzata per mantenere i gruppi di popolazione calcolati nella stessa composizione, convertendoli in tipi di pubblico riutilizzabili. Connettila ad altre attività di targeting, come a un’attività **Crea pubblico** o **Combina**.

L&#39;attività **[!UICONTROL Save Audience]** genera un nuovo schema di pubblico e un set di dati associato, che può contenere informazioni personali (PII) o informazioni sanitarie protette (PHI). Dopo la creazione del pubblico, collabora con l’amministratore per garantire che le etichette di governance dei dati appropriate vengano applicate in conformità ai criteri dei dati della tua organizzazione. Per ulteriori informazioni su come applicare le etichette di utilizzo dati, leggere la [guida utente delle etichette di utilizzo dati](https://experienceleague.adobe.com/it/docs/experience-platform/data-governance/labels/user-guide).

## Configurare l’attività Salva pubblico {#save-audience-configuration}

Per configurare l’attività **Salva pubblico**, segui questi passaggi:

1. Aggiungi un&#39;attività **Save audience** alla composizione.

   ![](../assets/save-audience.png)

1. Specifica l’etichetta del pubblico da creare.

   >[!IMPORTANT]
   >
   >L’etichetta del pubblico deve essere univoca nella sandbox corrente. Non può essere la stessa etichetta di un pubblico esistente.

1. Utilizza la sezione Mappature pubblico per selezionare i campi che desideri trasferire con il pubblico appena creato. A questo scopo, fai clic su **Aggiungi mappatura pubblico**, quindi scegli i campi del pubblico di origine e di destinazione.

   Ripeti l’operazione per aggiungere tutte le mappature del pubblico necessarie.

1. Seleziona l’identità principale e lo spazio dei nomi da utilizzare per identificare i profili target nel database:

   * **Campo identità primaria**: selezionare il campo da utilizzare per identificare i profili. Ad esempio, l’indirizzo e-mail o il numero di telefono.
   * **Spazio dei nomi identità**: selezionare lo spazio dei nomi da utilizzare per identificare i profili, ovvero il tipo di dati da utilizzare come chiave di identificazione. Ad esempio, se l&#39;indirizzo e-mail è stato selezionato come campo di identità principale, deve essere selezionato lo spazio dei nomi dell&#39;identità **E-mail**. Se l&#39;identificatore univoco è il numero di telefono, deve essere selezionato lo spazio dei nomi dell&#39;identità **Telefono**.

## Accedere al pubblico in Adobe Experience Platform {#access-audience}

Dopo aver eseguito la composizione, il pubblico risultante viene salvato in Adobe Experience Platform come pubblico esterno e disponibile in Adobe Real-Time CDP e/o Adobe Journey Optimizer in Audience Portal. Per ulteriori informazioni su Audience Portal, consulta la [panoramica di Audience Portal](https://experienceleague.adobe.com/it/docs/experience-platform/segmentation/ui/audience-portal){target="_blank"}.

Il pubblico creato include tutti i campi selezionati nella sezione Mappature pubblico. Puoi indirizzare questo pubblico in Journey Optimizer o attivarlo in qualsiasi destinazione supportata da Adobe Experience Platform.

[Ulteriori informazioni sono disponibili nella documentazione di Adobe Experience Platform](https://experienceleague.adobe.com/it/docs/experience-platform/segmentation/ui/audience-portal){target="_blank"}

<!--

## Example{#save-audience-example}

The following example illustrates a simple audience update from targeting. A scheduler is added to run the workflow once a month. A query recovers all the profiles subscribed to the different application services available. The **Save audience** activity updates the audience by deleting profiles that have unsubscribed from the service since the last workflow execution and by adding the newly subscribed profiles.
-->
