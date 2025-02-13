---
audience: end-user
title: Introduzione ai modelli di dati
description: Scopri come iniziare con i modelli di dati
exl-id: 8f9e9895-dcd7-4718-8922-4f7fefe9ed94
source-git-commit: 61a7b66d16358a4a1c3d4b2ae153e856d8f682f7
workflow-type: tm+mt
source-wordcount: '413'
ht-degree: 15%

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

1. Nella sezione **[!UICONTROL Federated Data]**, accedi al menu **[!UICONTROL Models]** e passa alla scheda **[!UICONTROL Data model]**.

   Fare clic sul pulsante **[!UICONTROL Crea modello dati]**.

   ![](assets/datamodel_create.png){zoomable="yes"}

1. Definisci il nome del modello dati e fai clic sul pulsante **[!UICONTROL Crea]**.

1. Dal dashboard del modello dati, fai clic su **[!UICONTROL Aggiungi schemi]** per scegliere lo schema associato al modello dati.

   ![](assets/datamodel_schemas.png){zoomable="yes"}

1. Fai clic su **[!UICONTROL Aggiungi pubblico]** per definire i gruppi target.

1. Stabilisci connessioni tra tabelle nel modello dati per garantire relazioni di dati accurate. [Ulteriori informazioni](#data-model-links)

1. Dopo aver completato la configurazione, fai clic su **[!UICONTROL Salva]** per applicare le modifiche.

## Crea collegamenti {#data-model-links}

Per creare collegamenti tra tabelle del modello dati, effettua le seguenti operazioni:

1. Fai clic sul menu **[!UICONTROL Crea collegamento]** di una delle tabelle oppure fai clic sul pulsante **[!UICONTROL Crea collegamenti]** e scegli le due tabelle:

   ![](assets/datamodel_createlinks.png){zoomable="yes"}

1. Compila il modulo specificato per definire il collegamento.

   ![](assets/datamodel_link.png){zoomable="yes"}

   **Cardinalità**

   * **1-N**: una occorrenza della tabella di origine può avere diverse occorrenze corrispondenti della tabella di destinazione, ma una occorrenza della tabella di destinazione può avere al massimo una occorrenza corrispondente della tabella di origine.

   * **N-1**: una occorrenza della tabella di destinazione può avere diverse occorrenze corrispondenti della tabella di origine, ma una occorrenza della tabella di origine può avere al massimo una occorrenza corrispondente della tabella di destinazione.

   * **1-1**: una occorrenza della tabella di origine può avere al massimo una occorrenza corrispondente della tabella di destinazione.

Di seguito sono elencati tutti i collegamenti definiti per il modello dati:

![](assets/datamodel_alllinks.png){zoomable="yes"}

## Video introduttivo {#data-model-video}

Scopri come creare un modello dati in questo video:

>[!VIDEO](https://video.tv.adobe.com/v/3432020)
