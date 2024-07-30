---
audience: end-user
title: Utilizzare i tipi di pubblico
description: Scopri come utilizzare i tipi di pubblico
badge: label="Disponibilità limitata" type="Informative"
exl-id: c6507624-1dc9-43f9-a3ad-c3dc9689f8c7
source-git-commit: f549f1611bfe6deb6dc684e3a0d9c968ba7c184a
workflow-type: tm+mt
source-wordcount: '311'
ht-degree: 27%

---

# Utilizzare i tipi di pubblico {#gs-audiences}

Experience Platform di Federated Audience Composition consente di [creare composizioni](../compositions/gs-compositions.md), in cui è possibile sfruttare varie attività in un&#39;area di lavoro visiva per creare tipi di pubblico e memorizzarli in Adobe Experience Platform Audience Portal.

Puoi quindi indirizzare questi tipi di pubblico in Journey Optimizer o attivarli in qualsiasi destinazione supportata da Adobe Experience Platform.

## Creazione di tipi di pubblico tramite composizioni {#creation}

Per creare tipi di pubblico utilizzando la composizione Pubblico federato, devi creare una composizione che includa un&#39;attività **[!UICONTROL Salva pubblico]**. Questa attività ti consente di salvare il pubblico in Audience Portal e di selezionare i campi dai database esterni da includere nel pubblico. [Scopri come configurare un’attività Salva pubblico](../compositions/activities/save-audience.md)

Il pubblico creato con Adobe Federated Data Composition include tutti i campi selezionati nell&#39;attività **[!UICONTROL Save audience]** e viene memorizzato in Audience Portal insieme a tutti i tipi di pubblico di Adobe Experience Platform.

Dopo aver eseguito la composizione, il pubblico risultante viene salvato in Adobe Experience Platform come pubblico esterno e disponibile in Adobe Real-Time Customer Data Platform e/o Adobe Journey Optimizer.

Puoi attivare questi tipi di pubblico in qualsiasi destinazione supportata da Adobe Experience Platform. Scopri come utilizzare le destinazioni in [Adobe Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/home){target="_blank"}

>[!NOTE]
>
>I tipi di pubblico creati con Composizione di pubblico federato di Adobe non possono essere modificati. Per apportare modifiche a uno di questi tipi di pubblico, devi creare un nuovo pubblico utilizzando una composizione.

## Accedere al pubblico in Adobe Experience Platform {#access-audience}

I tipi di pubblico creati mediante Federated Audience Composition sono accessibili in Audience Portal, accessibile dal menu **Audiences**.

La scheda **[!UICONTROL Sfoglia]** elenca tutti i tipi di pubblico esistenti memorizzati in Adobe Experience Platform. Per riconoscere, tra i tipi di pubblico elencati, quelli creati con Composizione di pubblico federato, osserva la colonna **[!UICONTROL Origine]** o utilizza i filtri disponibili nel riquadro a sinistra.

![](assets/audiences-list.png)

Per ulteriori informazioni su come utilizzare i tipi di pubblico in Adobe Experience Platform, consulta la [documentazione di Audience Portal](https://experienceleague.adobe.com/it/docs/experience-platform/segmentation/ui/audience-portal){target="_blank"}

<!-- add link to this donc once published: https://jira.corp.adobe.com/browse/PLAT-198674-->