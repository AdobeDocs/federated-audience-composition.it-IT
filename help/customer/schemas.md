---
audience: end-user
title: Introduzione agli schemi
description: Scopri come iniziare con gli schemi
badge: label="Disponibilità limitata" type="Informative"
source-git-commit: 96508e648b2f97dd9410df617ed3a5fd8b354b52
workflow-type: tm+mt
source-wordcount: '289'
ht-degree: 31%

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


## Che cos’è uno schema? {#schema-start}

Uno schema è un oggetto all’interno dell’applicazione che definisce il modo in cui i dati sono legati alle tabelle del database.
Uno schema fa riferimento a una tabella.

## Creare uno schema {#schema-create}

Nella sezione **[!UICONTROL FEDERATED DATA]**, vai al collegamento **[!UICONTROL Models]**. Troverai la scheda **[!UICONTROL Schema]**.
Fai clic sul pulsante **[!UICONTROL Crea schema]**.

![](assets/schema_create.png){zoomable="yes"}

Seleziona il database di origine nell&#39;elenco a discesa e fai clic sulla scheda **[!UICONTROL Aggiungi tabelle]**

![](assets/schema_tables.png){zoomable="yes"}

Sarà possibile accedere a tutte le tabelle del database e per le quali è possibile creare uno schema.

Aggiungendo le tabelle, potrai accedere ai relativi campi e gestire per mantenere ciò di cui hai realmente bisogno.

![](assets/schema_fields.png){zoomable="yes"}

## Come si modifica uno schema? {#schema-edit}

Per modificare uno schema, fai clic sul nome dello schema nella cartella degli schemi. Accedi alla pagina seguente.
Fai clic sul pulsante **[!UICONTROL Modifica]**.

![](assets/schema_edit.png){zoomable="yes"}

## Come visualizzare in anteprima i dati in uno schema? {#schema-preview}

Per visualizzare in anteprima i dati nella tabella rappresentata dallo schema, passa alla scheda **[!UICONTROL Dati]** come indicato di seguito.

![](assets/schema_data.png){zoomable="yes"}

È possibile modificare la panoramica dei dati facendo clic sul pulsante **[!UICONTROL Configura colonne]**.

![](assets/schema_columns.png){zoomable="yes"}

## Eliminare uno schema? {#schema-delete}

Per eliminare uno schema, fai clic sul pulsante **[!UICONTROL Altro]**, quindi su **[!UICONTROL Elimina]**.

![](assets/schema_delete.png){zoomable="yes"}