---
audience: end-user
title: Utilizzare l’attività Genera pubblico
description: Scopri come utilizzare l’attività Genera pubblico
exl-id: 6fad3e49-e654-4f68-a125-50056c4ae980
source-git-commit: 65052ffcd8c70817aa428bea7f8b6baa0a49a1b0
workflow-type: tm+mt
source-wordcount: '244'
ht-degree: 29%

---

# Crea pubblico {#build-audience}

>[!CONTEXTUALHELP]
>id="dc_orchestration_build_audience"
>title="Attività Crea pubblico"
>abstract="L’attività **Crea pubblico** consente di definire il pubblico che sarà inserito nella composizione."

L&#39;attività **Genera pubblico** ti consente di definire il pubblico che entrerà nella composizione. Per definire la popolazione del pubblico, puoi eseguire le seguenti operazioni:

* Seleziona un pubblico Adobe Experience Platform esistente.
* Crea un nuovo pubblico con Query Modeler definendo e combinando criteri di filtro.

## Configurare l’attività Crea pubblico {#build-audience-configuration}

>[!CONTEXTUALHELP]
>id="dc_orchestration_build_audience_audienceselector"
>title="Pubblico"
>abstract="Seleziona il pubblico."

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

   ![](../assets/build-audience-create.png)

1. Fai clic su **Continua**.
1. Utilizza il modellatore di query per definire la query, quindi conferma. [Scopri come utilizzare Query Modeler](../../query/query-modeler-overview.md)

>[!TAB Read audience]

Per selezionare un pubblico esistente, segui questi passaggi:

1. Seleziona **Leggi pubblico**.
1. Fai clic su **Continua**.

   ![](../assets/build-audience-read.png)

1. Seleziona il pubblico.

>[!ENDTABS]

>[!NOTE]
>
>L&#39;opzione **Genera una transizione in uscita** consente di aggiungere una transizione in uscita che verrà attivata alla fine dell&#39;esecuzione dell&#39;attività se la popolazione del pubblico è vuota.

<!--
## Examples{#build-audience-examples}

Here is an example of a workflow with two **Build audience** activities. The first one targets the poker players audience, followed by an email delivery. The second one targets the VIP clients audience, followed by an SMS delivery.

![](../assets/workflow-audience-example.png)
-->
