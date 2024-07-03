---
audience: end-user
title: Creare composizioni
description: Scopri come creare le composizioni
source-git-commit: 4ccf3be01abb8d6cb2834f49d83b677edaa61ef7
workflow-type: tm+mt
source-wordcount: '253'
ht-degree: 36%

---


# Principi chiave per la creazione della composizione {#gs-composition-creation}

>[!CONTEXTUALHELP]
>id="dc_composition_creation_properties"
>title="Proprietà di composizione"
>abstract="In questa schermata, scegliete il modello da utilizzare per creare la composizione e specificate un&#39;etichetta. Espandere la sezione OPTIONS AGGIUNTIVI per configurare altre impostazioni quali il nome interno della composizione, la relativa cartella, il fuso orario e il gruppo di supervisori. Si consiglia vivamente di selezionare un gruppo di supervisori in modo che gli operatori vengano avvisati in caso di errore."

Federated Data Composition fornisce un’area di lavoro visiva che consente di creare tipi di pubblico sfruttando varie attività (suddivisione, arricchimento, ecc.).

## Cosa c&#39;è all&#39;interno di una composizione? {#gs-composition-inside}

Il diagramma di composizione è una rappresentazione di ciò che dovrebbe accadere. Descrive le varie attività da eseguire e il modo in cui vengono collegate tra loro.

![](assets/composition-example.png){zoomable="yes"} {zoomable="yes"}

Ogni composizione contiene:

* **Attività**: un’attività è un’attività da eseguire. Le varie attività disponibili sono rappresentate nel diagramma tramite icone. Ogni attività presenta proprietà specifiche e altre proprietà comuni a tutte le attività.

  In un diagramma di composizione, una determinata attività può produrre più attività, in particolare quando vi è un loop o azioni ricorrenti.

* **Transizioni**: le transizioni collegano un’attività di origine a un’attività di destinazione e ne definiscono la sequenza.

* **Tabelle di lavoro**: la tabella di lavoro contiene tutte le informazioni riportate dalla transizione. Ogni composizione utilizza diverse tabelle di lavoro. I dati trasmessi in queste tabelle possono essere utilizzati in tutto il ciclo di vita della composizione.

## Passaggi chiave per creare una composizione {#gs-composition-steps}

I passaggi principali per creare una composizione sono i seguenti:

1. [Creare la composizione](#create)
1. [Configurare le impostazioni della composizione](#starting-audience)
1. [Aggiungere e configurare le attività](#action-activities)
1. [Eseguite la composizione e monitoratene l&#39;esecuzione](#save)
