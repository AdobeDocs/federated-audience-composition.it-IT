---
audience: end-user
title: Creare composizioni
description: Scopri come creare le composizioni
exl-id: 861440ab-ce14-46aa-a215-b86fc9ffeef0
source-git-commit: b73eba776e3e75f3ff7107bcf48f7b2f60048d08
workflow-type: tm+mt
source-wordcount: '231'
ht-degree: 58%

---

# Principi chiave per la creazione della composizione {#gs-composition-creation}

>[!CONTEXTUALHELP]
>id="dc_composition_creation_properties"
>title="Proprietà della composizione"
>abstract="In questa schermata, scegli il modello da utilizzare per creare la composizione e specifica un’etichetta. Espandi la sezione OPZIONI AGGIUNTIVE per configurare altre impostazioni quali il nome interno della composizione, la relativa cartella, il fuso orario e il gruppo di supervisori. Si consiglia vivamente di selezionare un gruppo di supervisori in modo che gli operatori vengano avvisati in caso di errore."

## Cosa c&#39;è all&#39;interno di una composizione {#gs-composition-inside}

La Federated Audience Composition di Experience Platform fornisce un’area di lavoro visiva che consente di creare tipi di pubblico sfruttando varie attività (suddivisione, arricchimento, ecc.).

Il diagramma di composizione è una rappresentazione di ciò che dovrebbe accadere. Descrive le varie attività da eseguire e il modo in cui vengono collegate tra loro.

![](assets/gs-compositions/composition-example.png){zoomable="yes"}{width="70%"}

Ogni composizione contiene:

* **[!UICONTROL Attività]**: un’attività è un’attività da eseguire. Le varie attività disponibili sono rappresentate nel diagramma tramite icone. Ogni attività presenta proprietà specifiche e altre proprietà comuni a tutte le attività.
* **[!UICONTROL Transizioni]**: le transizioni collegano un’attività di origine a un’attività di destinazione e ne definiscono la sequenza.
* **[!UICONTROL Tabelle di lavoro]**: la tabella di lavoro contiene tutte le informazioni riportate dalla transizione. Ogni composizione utilizza diverse tabelle di lavoro. I dati trasmessi in queste tabelle possono essere utilizzati in tutto il ciclo di vita della composizione.

## Passaggi chiave per creare una composizione {#gs-composition-steps}

I passaggi principali per creare una composizione sono i seguenti:

1. [Creare e configurare la composizione](../compositions/create-composition.md)
1. [Orchestrare le attività](../compositions/orchestrate-activities.md)
1. [Eseguite la composizione e monitoratene l&#39;esecuzione](../compositions/start-monitor-composition.md)
