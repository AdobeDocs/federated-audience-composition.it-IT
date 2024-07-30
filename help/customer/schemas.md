---
audience: end-user
title: Introduzione agli schemi
description: Scopri come iniziare con gli schemi
badge: label="Disponibilità limitata" type="Informative"
exl-id: 2c939185-f1c1-4f2b-ae1b-e2539e121eff
source-git-commit: 91324185f91c552128774ad35e73c70b7cc33ac8
workflow-type: tm+mt
source-wordcount: '451'
ht-degree: 22%

---

# Introduzione agli schemi {#schemas}

>[!CONTEXTUALHELP]
>id="dc_schema_create_select_tables"
>title="Selezionare tabelle"
>abstract="Seleziona le tabelle da aggiungere per il modello dati."

>[!CONTEXTUALHELP]
>id="dc_schema_create_key"
>title="Chiave"
>abstract="Seleziona una chiave per la riconciliazione dei dati."

>[!CONTEXTUALHELP]
>id="dc_schema_create_schema_name"
>title="Nome dello schema"
>abstract="Immetti il nome dello schema."


>[!CONTEXTUALHELP]
>id="dc_schema_edit_description"
>title="Descrizione dello schema"
>abstract="Nella descrizione dello schema sono elencate le colonne, i tipi e le etichette. Puoi anche verificare la chiave di riconciliazione per lo schema. Per aggiornare la definizione dello schema, fai clic sull’icona a forma di matita."

>[!CONTEXTUALHELP]
>id="dc_schema_filter_sources"
>title="Selezionare il database di origine da filtrare"
>abstract="Puoi filtrare gli schemi in base alla loro origine. Seleziona uno o più database federati per visualizzarne i relativi schemi."

## Che cos’è uno schema {#schema-start}

Uno schema è una rappresentazione di una tabella del database. Si tratta di un oggetto all&#39;interno dell&#39;applicazione che definisce il modo in cui i dati vengono legati alle tabelle del database.

Creando uno schema, puoi definire una rappresentazione della tabella in Experience Platform di Federated Audience Composition:

* Assegna un nome descrittivo e una descrizione per semplificare la comprensione da parte dell’utente
* Decidere la visibilità di ciascun campo in base al suo utilizzo reale
* Selezionare la chiave primaria per collegare gli schemi, in base alle esigenze nel [modello dati](../data-management/gs-models.md#data-model-start)

>[!CAUTION]
>
>Quando connetti più sandbox con lo stesso database, devi utilizzare schemi di lavoro distinti.
>

## Crea uno schema {#schema-create}

Per creare schemi in Federated Audience Composition, segui i passaggi seguenti:

1. Nella sezione **[!UICONTROL FEDERATED DATA]**, vai al collegamento **[!UICONTROL Models]**. Passare alla scheda **[!UICONTROL Schema]** e fare clic sul pulsante **[!UICONTROL Crea schema]**.

   ![](assets/schema_create.png){zoomable="yes"}

   Questo passaggio consente di accedere a una nuova schermata con un elenco a discesa in cui è possibile trovare i database connessi all’ambiente. Ulteriori informazioni sulla connessione al database in [questa sezione](../connections/connections.md#connections-fdb).

1. Selezionare il database di origine nell&#39;elenco e fare clic sulla scheda **[!UICONTROL Aggiungi tabelle]**.

   ![](assets/schema_tables.png){zoomable="yes"}

   Viene quindi visualizzato l&#39;elenco di tutte le tabelle del database.

1. Aggiungendo le tabelle per le quali si desidera creare lo schema, è possibile accedere ai relativi campi come indicato di seguito:

   ![](assets/schema_fields.png){zoomable="yes"}

   Per ogni tabella è possibile:

   * modificare l’etichetta dello schema
   * aggiungi una descrizione
   * rinominare tutti i campi e impostarne la visibilità
   * seleziona la chiave primaria dello schema

   Ad esempio, per la tabella seguente importata:

   ![](assets/schema_lumaorder.png){zoomable="yes"}

   Lo schema può essere definito come segue:

   ![](assets/schema_lumaorders.png){zoomable="yes"}

## Modificare uno schema {#schema-edit}

Per modificare uno schema:

1. Fai clic sul nome dello schema nella cartella degli schemi.

1. Fai clic sul pulsante **[!UICONTROL Modifica]**.

   ![](assets/schema_edit.png){zoomable="yes"}

   Puoi accedere alle stesse opzioni disponibili per [la creazione di uno schema](#schema-create).

   ![](assets/schema_edit_orders.png){zoomable="yes"}

## Visualizzare l’anteprima dei dati in uno schema {#schema-preview}

Per visualizzare in anteprima i dati nella tabella rappresentata dallo schema, passa alla scheda **[!UICONTROL Dati]** come indicato di seguito.

Fai clic sul collegamento **[!UICONTROL Calcola]** per visualizzare in anteprima il numero totale di registrazioni.

![](assets/schema_data.png){zoomable="yes"}

Fai clic sul pulsante **[!UICONTROL Configura colonne]** per modificare la visualizzazione dei dati.

![](assets/schema_columns.png){zoomable="yes"}

## Eliminare uno schema {#schema-delete}

Per eliminare uno schema, fai clic sul pulsante **[!UICONTROL Altro]**, quindi scegli **[!UICONTROL Elimina]**.

![](assets/schema_delete.png){zoomable="yes"}
