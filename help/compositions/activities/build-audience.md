---
audience: end-user
title: Utilizzare l’attività Genera pubblico
description: Scopri come utilizzare l’attività Genera pubblico
source-git-commit: 5fe470ce83a5c3d3df7717bc1203849d99edf430
workflow-type: tm+mt
source-wordcount: '237'
ht-degree: 39%

---


# Creazione del pubblico {#build-audience}

>[!CONTEXTUALHELP]
>id="dc_orchestration_build_audience"
>title="Attività Creazione del pubblico"
>abstract="L’attività **Creazione del pubblico** consente di definire il pubblico che sarà inserito nella composizione."

L’attività **Creazione del pubblico** consente di definire il pubblico che sarà inserito nella composizione.

Per definire la popolazione del pubblico, puoi eseguire le seguenti operazioni:

<!--* Select an existing audience, created as a list in the client console.-->
* Seleziona un pubblico di Adobe Experience Platform.
* Crea un nuovo pubblico con il generatore di modellatori di query definendo e combinando criteri di filtro.

L&#39;attività **Genera pubblico** può essere posizionata all&#39;inizio della composizione o dopo qualsiasi altra attività. Qualsiasi attività può essere inserita dopo il **Genera pubblico**.

## Configurare l’attività Creazione del pubblico {#build-audience-configuration}

>[!CONTEXTUALHELP]
>id="dc_orchestration_build_audience_audienceselector"
>title="Pubblico"
>abstract="Selezionare il pubblico."

Per configurare l’attività **Crea pubblico**, segui questi passaggi:

1. Aggiungi un’attività **Crea pubblico**.
1. Definisci un’etichetta.
1. Specifica se desideri creare un pubblico o selezionarne uno esistente.
1. Configura il pubblico seguendo i passaggi descritti nelle schede seguenti.

>[!BEGINTABS]

>[!TAB Crea pubblico]

Per creare un pubblico personalizzato, segui questi passaggi:

1. Seleziona **Crea pubblico**.
1. Scegli lo **schema**, noto anche come dimensione di targeting. Lo schema ti consente di definire la popolazione target dell’operazione: destinatari, beneficiari del contratto, operatore, abbonati, ecc. Per impostazione predefinita, lo schema viene selezionato dai destinatari.
1. Fai clic su **Continua**.
1. Utilizza il modellatore di query per definire la query. [Scopri come utilizzare Query Modeler](../../query/query-modeler-overview.md)

>[!TAB Read audience]

Per selezionare un pubblico esistente, segui questi passaggi:

1. Seleziona **Leggi pubblico**.
1. Fai clic su **Continua**.
1. Selezionare il pubblico.

>[!ENDTABS]

<!--
## Examples{#build-audience-examples}

Here is an example of a workflow with two **Build audience** activities. The first one targets the poker players audience, followed by an email delivery. The second one targets the VIP clients audience, followed by an SMS delivery.

![](../assets/workflow-audience-example.png)
-->
