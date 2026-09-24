---
audience: end-user
title: Panoramica degli schemi
description: Scopri come creare e utilizzare gli schemi per la Federated Audience Composition nell’interfaccia utente di Adobe Experience Platform.
TQID: https://experienceleague.adobe.com/cpkFeiskYDpixNo01llqC3UKK8XfewN7XC2yAf1wOYQ
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
    internal-label: Experience Cloud
topic_v2:
  - id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adeb
    internal-label: Governance
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
    internal-label: Security
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
    internal-label: Privacy
source-git-commit: 3b159f95e28414b75b44e41e822e9e3d0e35b537
workflow-type: tm+mt
source-wordcount: '796'
ht-degree: 3%
---
# Panoramica degli schemi {#schemas}

>[!AVAILABILITY]
>
>La nuova esperienza schemi è disponibile solo per alcuni clienti. Per ulteriori informazioni, contatta l’Assistenza clienti di Adobe.
>
>Se non hai accesso alla nuova esperienza schemi, leggi la [panoramica schemi](./schemas.md).
>
>Per accedere agli schemi, è necessario disporre di una delle seguenti autorizzazioni:
>
>-**Gestisci schema federato**
>-**Visualizza schema federato**
>
>Per ulteriori informazioni sulle autorizzazioni richieste, consulta la [Guida al controllo degli accessi](/help/governance-privacy-security/access-control.md).

Uno schema è una rappresentazione di una tabella del database. Si tratta di un oggetto all&#39;interno dell&#39;applicazione che definisce il modo in cui i dati vengono legati alle tabelle del database.

Creando uno schema, puoi definire una rappresentazione della tabella in Experience Platform Federated Audience Composition:

* Assegna un nome descrittivo e una descrizione per semplificare la comprensione da parte dell’utente
* Decidere la visibilità di ciascun campo in base al suo utilizzo reale
* Selezionare la chiave primaria per collegare gli schemi, in base alle esigenze nel [modello dati](../data-modelling/models.md#data-model-start)

>[!CAUTION]
>
>Quando connetti più sandbox con lo stesso database, devi utilizzare schemi di lavoro distinti.

## Creare uno schema {#create}

>[!CONTEXTUALHELP]
>id="platform_schemas_manageconfiguration"
>title="Gestisci configurazione"
>abstract="Contenuto vuoto temporaneo."

Per creare uno schema in Federated Audience Composition, seleziona **[!UICONTROL Schemi]** nella sezione **[!UICONTROL Gestione dati]** dell&#39;interfaccia utente di Experience Platform. Nell&#39;interfaccia utente Schemi, selezionare **[!UICONTROL Crea schema]**.

![I pulsanti Schemi e Crea schema sono entrambi evidenziati nell&#39;interfaccia utente Schemi.](/help/data-modelling/assets/integrated/select-create-schema.png)

Una volta visualizzato il popover Crea schema, seleziona **[!UICONTROL Relazionale]**, seguito da **[!UICONTROL Scopri schemi]** e **[!UICONTROL Successivo]** per creare uno schema per la Composizione di pubblico federato.

![Il pulsante Discover schemas è evidenziato nella finestra a comparsa Create a relational schema.](/help/data-modelling/assets/integrated/select-discover-schemas.png)

Viene visualizzato il popover **[!UICONTROL Seleziona database federato]**. In questo popover è possibile selezionare il [database di origine](/help/connections/home.md), seguito da **[!UICONTROL Avanti]**.

![Viene visualizzato il popover Seleziona database federato.](/help/data-modelling/assets/integrated/select-federated-database.png)

## Definisci schema {#define}

>[!CONTEXTUALHELP]
>id="platform_schemas_primarycompositekey"
>title="Chiave composita"
>abstract="Chiave dello schema composta da più colonne di schema. Contrassegna le colonne da utilizzare come chiave composita."

Dopo aver scelto il database federato, è ora possibile definire lo schema. Viene visualizzata la schermata **[!UICONTROL Aggiungi dati]**. In questa pagina è possibile selezionare **[!UICONTROL Aggiungi tabella]** per scegliere le tabelle da aggiungere allo schema.

![Il pulsante Aggiungi tabella è evidenziato nella schermata Aggiungi dati.](/help/data-modelling/assets/integrated/select-add-table.png)

Viene visualizzato il popover **[!UICONTROL Seleziona tabella]**. In questo popover è possibile selezionare le tabelle da utilizzare per creare lo schema.

![Viene visualizzato il popover Seleziona tabella.](/help/data-modelling/assets/integrated/select-table.png){zoomable="yes"}

Ogni tabella selezionata genera uno schema con le colonne selezionate. Per ogni tabella, puoi modificare l’etichetta dello schema, aggiungere una descrizione, rinominare l’etichetta del campo, impostare la visibilità dell’etichetta del campo e selezionare la chiave primaria dello schema.

![Le tabelle selezionate vengono visualizzate nella pagina Aggiungi dati.](/help/data-modelling/assets/integrated/tables-added.png){zoomable="yes"}

>[!NOTE]
>
>Se si sceglie **[!UICONTROL Chiave composita]** ma si seleziona una sola chiave da utilizzare, la chiave verrà trattata come una chiave primaria dello schema standard.

Inoltre, puoi creare una chiave composta da più colonne di schema. Selezionare **[!UICONTROL Chiave composita]** e contrassegnare le chiavi da utilizzare come chiave composita.

![Sono selezionati sia l&#39;opzione Tasto composito che gli schemi.](/help/data-modelling/assets/integrated/composite-key.png){zoomable="yes"}

Al termine della configurazione, seleziona **[!UICONTROL Fine]** per completare la creazione dello schema.

## Modificare uno schema {#schema-edit}

Per modificare uno schema, seleziona l&#39;icona ![puntini di sospensione](/help/assets/icons/more.png) accanto allo schema creato in precedenza nella pagina **Schemi**, seguita da **[!UICONTROL Modifica]**.

![Il pulsante Modifica schema è evidenziato.](/help/data-modelling/assets/integrated/edit-schema.png)

Nella finestra **[!UICONTROL Modifica schema]** è possibile visualizzare l&#39;Editor di schema. Per ulteriori informazioni sull&#39;utilizzo dell&#39;Editor di schema, leggere la [guida dell&#39;interfaccia utente dello schema](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/ui/resources/schemas#customize-schema).

![Viene visualizzato l&#39;Editor di schema.](/help/data-modelling/assets/integrated/schema-editor.png)

### Modifica relazioni {#relationship-edit}

Per modificare le relazioni per uno schema, selezionare **[!UICONTROL Visualizza diagramma entità]** nell&#39;Editor schema.

![Il pulsante Visualizza diagramma entità è evidenziato.](/help/data-modelling/assets/integrated/view-entity-diagram.png)

Viene visualizzata la pagina del diagramma entità. In questa pagina è possibile creare collegamenti per stabilire relazioni tra gli schemi.

![Viene visualizzato il diagramma entità.](/help/data-modelling/assets/integrated/entity-diagram.png)

Per ulteriori informazioni sulla creazione di collegamenti, leggere la scheda Visualizzazione area di lavoro della [panoramica modelli dati](/help/data-modelling/models.md#data-model-links).

## Visualizzare l’anteprima dei dati in uno schema {#schema-preview}

Per visualizzare in anteprima i dati nella tabella rappresentata dallo schema, passare alla sezione **[!UICONTROL Set di dati]** e selezionare **[!UICONTROL Sfoglia]**.

![I set di dati e i pulsanti Sfoglia sono evidenziati.](/help/data-modelling/assets/integrated/datasets-browse.png)

Seleziona ![tre punti](/help/assets/icons/more.png), seguito da **[!UICONTROL Anteprima set di dati]** per visualizzare un&#39;anteprima dei dati nello schema.

![Il pulsante Anteprima set di dati è evidenziato.](/help/data-modelling/assets/integrated/select-preview-dataset.png)

## Aggiornare uno schema {#schema-refresh}

È possibile aggiornare, aggiungere o rimuovere tabelle in un database federato. In questi casi, è necessario aggiornare lo schema in Adobe Experience Platform per allinearlo alle modifiche più recenti. Per aggiornare lo schema, seleziona il pulsante **[!UICONTROL Altro]**, seguito da **[!UICONTROL Gestisci configurazione]**.

![Il pulsante Gestisci configurazione è evidenziato.](/help/data-modelling/assets/integrated/manage-configuration.png)

Viene visualizzato il popover **[!UICONTROL Modifica configurazione]**. Seleziona **[!UICONTROL Aggiorna]** per aggiornare lo schema.

![Il pulsante Aggiorna schema è evidenziato.](/help/data-modelling/assets/integrated/refresh-schema.png)

## Eliminare uno schema {#schema-delete}

Per eliminare uno schema nell&#39;Editor di schema, selezionare **[!UICONTROL Altro]**, seguito da **[!UICONTROL Elimina]**.

![Il pulsante Elimina schema è evidenziato.](/help/data-modelling/assets/integrated/delete-schema.png)
