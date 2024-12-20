---
audience: end-user
title: Introduzione ai modelli di dati
description: Scopri come iniziare con i modelli di dati
exl-id: 8f9e9895-dcd7-4718-8922-4f7fefe9ed94
source-git-commit: 65052ffcd8c70817aa428bea7f8b6baa0a49a1b0
workflow-type: tm+mt
source-wordcount: '378'
ht-degree: 16%

---

# Introduzione ai modelli di dati {#data-model}

>[!CONTEXTUALHELP]
>id="dc_model_menu"
>title="Utilizzare i modelli"
>abstract="In questa schermata sono elencati gli schemi e i modelli di dati. Puoi creare schemi e modelli di dati dal pulsante **Crea**."

>[!CONTEXTUALHELP]
>id="dc_datamodel_add_schema"
>title="Selezionare gli schemi"
>abstract="Seleziona gli schemi per il modello dati."


>[!CONTEXTUALHELP]
>id="dc_datamodel_add_audience"
>title="Selezionare un pubblico"
>abstract="Seleziona il pubblico per il modello dati."

>[!CONTEXTUALHELP]
>id="dc_datamodel_properties"
>title="Proprietà del modello dati"
>abstract="Immetti l’etichetta del modello dati."


## Che cos’è un modello dati {#data-model-start}

Un modello dati è un set di schemi, tipi di pubblico e i collegamenti tra di essi. Viene utilizzato per federare i tipi di pubblico con i dati dei database.

Ulteriori informazioni su [schemi](../customer/schemas.md#schema-start).

Ulteriori informazioni su [tipi di pubblico](../start/audiences.md).

Ad esempio, di seguito è riportata una rappresentazione di un modello dati : le tabelle con il loro nome e i collegamenti tra di esse.

![](assets/datamodel.png){zoomable="yes"}

In Federated Audience Composition, è possibile creare molti modelli di dati.

La loro creazione sarà basata sul caso d’uso: scegli le tabelle necessarie e collegale in base alle tue esigenze.

## Creare un modello dati {#data-model-create}

Per creare un modello dati, effettua le seguenti operazioni:

1. Nella sezione **[!UICONTROL FEDERATED DATA]**, vai al collegamento **[!UICONTROL Models]** e passa alla scheda **[!UICONTROL Data model]**.

   ![](assets/datamodel_create.png){zoomable="yes"}

1. Fai clic sul pulsante **[!UICONTROL Crea modello dati]** per definire il nome del modello dati, quindi fai clic sul pulsante **[!UICONTROL Crea]**.

   ![](assets/datamodel_name.png){zoomable="yes"}

1. Quindi aggiungi gli schemi, i tipi di pubblico e i collegamenti del modello di dati.

   ![](assets/datamodel_schemas.png){zoomable="yes"}

### Crea collegamenti {#data-model-links}

Per creare collegamenti tra tabelle del modello dati, effettua le seguenti operazioni:

1. Fai clic sul menu **[!UICONTROL Crea collegamento]** di una delle tabelle oppure fai clic sul pulsante **[!UICONTROL Crea collegamenti]** e scegli le due tabelle:

   ![](assets/datamodel_createlinks.png){zoomable="yes"}

1. Compila il modulo specificato per definire il collegamento.

   ![](assets/datamodel_link.png){zoomable="yes"}

   **Cardinalità**

   * 1-N: una occorrenza della tabella sorgente può avere diverse occorrenze corrispondenti della tabella di destinazione, ma una occorrenza della tabella di destinazione può avere al massimo una occorrenza corrispondente della tabella sorgente.

   * N-1: una occorrenza della tabella di destinazione può avere diverse occorrenze corrispondenti della tabella di origine, ma una occorrenza della tabella di origine può avere al massimo una occorrenza corrispondente della tabella di destinazione.

   * 1-1: una occorrenza della tabella sorgente può avere al massimo una occorrenza corrispondente della tabella di destinazione.

Di seguito sono elencati tutti i collegamenti definiti per il modello dati:

![](assets/datamodel_alllinks.png){zoomable="yes"}

## Video introduttivo {#data-model-video}

Scopri come creare un modello dati in questo video:

>[!VIDEO](https://video.tv.adobe.com/v/3432020)
