---
audience: end-user
title: Utilizzare l’attività Genera pubblico
description: Scopri come utilizzare l’attività Genera pubblico
source-git-commit: 4ba457f1dcd8b7997931a70d93a95f6a54c51cb5
workflow-type: tm+mt
source-wordcount: '251'
ht-degree: 37%

---


# Creazione del pubblico {#build-audience}

>[!CONTEXTUALHELP]
>id="dc_orchestration_build_audience"
>title="Attività Creazione del pubblico"
>abstract="Il **Creare un pubblico** attività ti consente di definire il pubblico che entrerà nella composizione."

Il **Creare un pubblico** attività ti consente di definire il pubblico che entrerà nella composizione.

Per definire la popolazione del pubblico, puoi eseguire le seguenti operazioni:

<!--* Select an existing audience, created as a list in the client console.-->
* Seleziona un pubblico di Adobe Experience Platform.
* Crea un nuovo pubblico con il generatore di modellatori di query definendo e combinando criteri di filtro.

Il **Creare un pubblico** L’attività può essere posizionata all’inizio della composizione o dopo qualsiasi altra attività. Qualsiasi attività può essere inserita dopo il **Creare un pubblico**.

## Configurare l’attività Creazione del pubblico {#build-audience-configuration}

>[!CONTEXTUALHELP]
>id="dc_orchestration_build_audience_audienceselector"
>title="Pubblico"
>abstract="Seleziona il pubblico."

Per configurare l’attività **Crea pubblico**, segui questi passaggi:

1. Aggiungi un’attività **Crea pubblico**.
1. Definisci un’etichetta.
1. Definisci il tipo di pubblico: **Crea una query personalizzata** o **Leggi pubblico**.
1. Configura il pubblico seguendo i passaggi descritti nelle schede seguenti.

>[!BEGINTABS]

>[!TAB Crea il tuo (query)]

Per creare una query personalizzata, effettua le seguenti operazioni:

1. Seleziona **Crea una query personalizzata**.
1. Scegli la **Dimensione targeting**. La dimensione targeting consente di definire la popolazione target dell’operazione: destinatari, beneficiari del contratto, operatore, iscritti, ecc. Per impostazione predefinita, il target viene selezionato dai destinatari.<!-- [Learn more about targeting dimensions](../../audience/about-recipients.md#targeting-dimensions)-->
1. Fai clic su **Continua**.
1. Utilizza il modellatore di query per definire la query, nello stesso modo in cui crei un pubblico durante la progettazione di una nuova e-mail. <!--[Learn how to work with the query modeler](../../query/query-modeler-overview.md)-->

>[!TAB Read audience]

Per selezionare un pubblico esistente, segui questi passaggi:

1. Seleziona **Leggi pubblico**.
1. Fai clic su **Continua**.
1. Seleziona il pubblico nello stesso modo in cui utilizzi un pubblico durante la progettazione di una nuova consegna. <!--Refer to this [section](../../audience/add-audience.md).-->

>[!ENDTABS]

<!--
## Examples{#build-audience-examples}

Here is an example of a workflow with two **Build audience** activities. The first one targets the poker players audience, followed by an email delivery. The second one targets the VIP clients audience, followed by an SMS delivery.

![](../assets/workflow-audience-example.png)
-->
