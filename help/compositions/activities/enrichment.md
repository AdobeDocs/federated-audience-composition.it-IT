---
audience: end-user
title: Utilizzare l’attività Enrichment
description: Scopri come utilizzare l’attività Enrichment
source-git-commit: 5180a92c24b08aa24506bd09a992c9e1573b33bc
workflow-type: tm+mt
source-wordcount: '387'
ht-degree: 39%

---


# Arricchimento {#enrichment}

>[!CONTEXTUALHELP]
>id="dc_orchestration_enrichment"
>title="Attività Arricchimento"
>abstract="L’attività di **Arricchimento** consente di migliorare i dati mirati con informazioni aggiuntive provenienti dal database. Viene comunemente utilizzato in una composizione dopo attività di segmentazione."

>[!CONTEXTUALHELP]
>id="dc_orchestration_enrichment_data"
>title="Attività di Arricchimento"
>abstract="Una volta aggiunti i dati di arricchimento alla composizione, questi possono essere utilizzati nelle attività aggiunte dopo **Arricchimento** attività per segmentare i profili in gruppi distinti in base a comportamenti, preferenze e scelte."

>[!CONTEXTUALHELP]
>id="dc_orchestration_enrichment_simplejoin"
>title="Definizione dei collegamenti"
>abstract="Crea un collegamento tra i dati della tabella di lavoro e il database federato."

>[!CONTEXTUALHELP]
>id="dc_orchestration_enrichment_reconciliation"
>title="Riconciliazione dell’arricchimento"
>abstract="Imposta i parametri di riconciliazione."

>[!CONTEXTUALHELP]
>id="dc_targetdata_personalization_enrichmentdata"
>title="Dati di arricchimento"
>abstract="Selezionate i dati da utilizzare per arricchire la composizione. Puoi selezionare due tipi di dati di arricchimento: un attributo di arricchimento singolo dalla dimensione target oppure un collegamento raccolta, che è un collegamento con cardinalità 1-N tra le tabelle."

Il **Arricchimento** attività ti consente di migliorare i dati di destinazione con informazioni aggiuntive dal database federato. Viene comunemente utilizzato nelle composizioni dopo le attività di segmentazione.

I dati di arricchimento possono provenire:

* **Dalla stessa tabella di lavoro** come quello di destinazione nella composizione:

  *Eseguire il targeting di un gruppo di clienti e aggiungere il campo &quot;Data di nascita&quot; alla tabella di lavoro corrente*.

* **Da un’altra tabella di lavoro**:

  *Esegui il targeting di un gruppo di clienti e aggiungere i campi “Importo” e “Tipo di prodotto” provenienti dalla tabella “Acquisto”*.

Una volta aggiunti i dati di arricchimento alla composizione, questi possono essere utilizzati nelle attività aggiunte dopo **Arricchimento** attività per segmentare i clienti in gruppi distinti in base a comportamenti, preferenze e scelte.

<!--For instance, you can add to the working table information related to customers' purchases and use this data to personalize emails with their latest purchase or the amount spent on these purchases.-->

## Configurare l’attività di Arricchimento {#enrichment-configuration}

Per configurare l’attività **Arricchimento** segui questi passaggi:

1. Aggiungi attività come **Crea pubblico** e **Combina**.
1. Aggiungi un’attività **Arricchimento**.

   ![](../assets/enrichment.png)

1. Se nella composizione sono state configurate più transizioni, puoi utilizzare **[!UICONTROL Set primario]** per definire quale transizione deve essere utilizzata come set principale da arricchire con i dati.

1. Clic **Aggiungere dati di arricchimento** e seleziona l’attributo da utilizzare per arricchire i dati.

   ![](../assets/enrichment-add.png)

   >[!NOTE]
   >
   >Il **Pulsante espressione Modifica** nella schermata di selezione degli attributi consente di creare espressioni avanzate per selezionare l’attributo.

<!--PAS VU SUR INSTANCE: You can select two types of enrichment data: a single enrichment attribute from the target dimension, or a collection link. Each of these types is detailed in the examples below:

    * [Single enrichment attribute](#single-attribute)
    * [Collection lnk](#collection-link)-->

## Esempi {#example}

### Attributo di arricchimento singolo {#single-attribute}

In questo caso, viene semplicemente aggiunto un attributo di arricchimento singolo, ad esempio, la data di nascita. Segui questi passaggi:

1. Fai clic all’interno del campo **Attributo**.
1. Seleziona un campo semplice dalla dimensione di targeting, nel nostro esempio la data di nascita.
1. Fai clic su **Conferma**.

<!--### Collection link {#collection-link}

In this more complex use case, we will select a collection link which is a link with a 1-N cardinality between tables. Let's retrieve the three latest purchases that are less than 100$. For this you need to define:

* an enrichment attribute: the **Total amount** field
* the number of lines to retrieve: 3
* a filter: filter out items that are greater than 100$
* a sorting: descendant sorting on the **Order date** field. 

#### Add the attribute {#add-attribute}

This is where you select the collection link to use as enrichment data.

1. Click inside the **Attribute** field.
1. Click **Display advanced attributes**.
1. Select the **Total amount** field from the **Purchases** table. 

#### Define the collection settings{#collection-settings}

Then, define how the data is collected and the number of records to retrieve.

1. Select **Collect data** in the **Select how the data is collected** drop-down.
1. Type "3" in the **Lines to retrieve (Columns to create)** field. 

If you want, for example, to get the average amount of purchases for a customer, select **Aggregated data** instead, and select **Average** in the **Aggregate function** drop-down.

#### Define the filters{#collection-filters}

Here, we define the maximum value for the enrichment attribute. We filter out items that are greater than 100$. [Learn how to work with the query modeler](../../query/query-modeler-overview.md)

1. Click **Edit filters**.
1. Add the two following filters: **Total amount** exists AND **Total amount** is less than 100. The first one filters NULL values as they would appear as the greatest value.
1. Click **Confirm**.

#### Define the sorting{#collection-sorting}

We now need to apply sorting in order to retrieve the three **latest** purchases.

1. Activate the **Enable sorting** option.
1. Click inside the **Attribute** field.
1. Select the **Order date** field.
1. Click **Confirm**. 
1. Select **Descending** from the **Sort** drop-down.-->
