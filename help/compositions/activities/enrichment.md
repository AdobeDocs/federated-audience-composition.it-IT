---
audience: end-user
title: Utilizzare l’attività Enrichment
description: Scopri come utilizzare l’attività Enrichment
source-git-commit: b21306cefe6e9e66263012110a7f89f2d92b38a5
workflow-type: tm+mt
source-wordcount: '1123'
ht-degree: 40%

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

## Aggiungere un’attività Enrichment {#enrichment-configuration}

Per configurare l’attività **Arricchimento** segui questi passaggi:

1. Aggiungi attività come **Crea pubblico** e **Combina**.
1. Aggiungi un’attività **Arricchimento**.
1. Se nella composizione sono state configurate più transizioni, puoi utilizzare **[!UICONTROL Set primario]** per definire quale transizione deve essere utilizzata come set principale da arricchire con i dati.

## Aggiungere dati di arricchimento {#enrichment-add}

1. Clic **Aggiungere dati di arricchimento** e seleziona l’attributo da utilizzare per arricchire i dati.

   Puoi selezionare due tipi di dati di arricchimento: un singolo attributo di arricchimento dalla dimensione di destinazione o un collegamento di raccolta. Ciascuno di questi tipi è descritto negli esempi seguenti:

   * [Attributo di arricchimento singolo](#single-attribute)
   * [Collegamento raccolta](#collection-link)

<!--
>[!NOTE]
>
>The **Edit expression button** in the attribute selection screen allows you to build advanced expressions to select the attribute. [Learn how to work with the expression editor](../../query/expression-editor.md)-->

## Creare collegamenti tra tabelle {#create-links}

Il **[!UICONTROL Definizione collegamento]** consente di creare un collegamento tra i dati della tabella di lavoro e il database. Ad esempio, se carichi i dati da un file che contiene il numero di account, il paese e l’e-mail dei destinatari, ora puoi creare un collegamento alla tabella dei paesi per aggiornare queste informazioni nei rispettivi profili.

Sono disponibili diversi tipi di collegamenti:

* **[!UICONTROL Collegamento semplice con cardinalità 1]**: ogni record del set principale può essere associato a un solo record dei dati collegati.
* **[!UICONTROL Collegamento semplice con cardinalità 0 o 1]**: ogni record del set principale può essere associato a 0 o 1 record dei dati collegati, ma non a più di uno.
* **[!UICONTROL Collegamento raccolta con cardinalità N]**: ogni record del set principale può essere associato a 0, 1 o più record (N) dei dati collegati.

Per creare un collegamento, effettua le seguenti operazioni:

1. In **[!UICONTROL Definizione collegamento]** , fare clic sul pulsante **[!UICONTROL Aggiungi collegamento]** pulsante.

1. In **Tipo di relazione** scegliere il tipo di collegamento che si desidera creare.

1. Identifica la destinazione a cui vuoi collegare il set principale:

   * Per collegare una tabella esistente nel database, scegliere **[!UICONTROL Schema del database]** e seleziona la tabella desiderata da **[!UICONTROL Schema di destinazione]** campo.
   * Per collegare i dati della transizione di input, scegli **Schema temporaneo** e seleziona la transizione di cui desideri utilizzare i dati.

1. Definisci i criteri di riconciliazione per far corrispondere i dati del set principale con lo schema collegato. Sono disponibili due tipi di join:

   * **Unione semplice**: seleziona un attributo specifico per far corrispondere i dati dei due schemi. Clic **Aggiungi join** e seleziona la **Source** e **Destinazione** attributi da utilizzare come criteri di riconciliazione.
   * **Unione avanzata**: crea un join utilizzando condizioni avanzate. Clic **Aggiungi join** e fai clic su **Crea condizione** per aprire Query Modeler.

Un esempio di composizione utilizzando i collegamenti è disponibile nel [Esempi](#link-example) sezione.

## Esempi {#example}

### Attributo di arricchimento singolo {#single-attribute}

In questo caso, viene semplicemente aggiunto un attributo di arricchimento singolo, ad esempio, la data di nascita. Segui questi passaggi:

1. Fai clic all’interno del campo **Attributo**.
1. Seleziona un campo semplice dalla dimensione di targeting, nel nostro esempio la data di nascita.
1. Fai clic su **Conferma**.

### Collegamento di raccolta {#collection-link}

In questo caso d’uso più complesso, selezioneremo un collegamento di raccolta che è un collegamento con cardinalità 1-N tra le tabelle. Recuperiamo i tre ultimi acquisti che sono inferiori a 100 $. A questo scopo è necessario definire:

* un attributo di arricchimento: il campo **Importo totale**
* il numero di righe da recuperare: 3
* un filtro: per escludere gli articoli superiori a 100 $
* un ordinamento: ordine decrescente sul campo **Data ordine**.

#### Aggiungere l’attributo {#add-attribute}

Qui puoi selezionare il collegamento di raccolta da utilizzare come dati di arricchimento.

1. Fai clic all’interno del campo **Attributo**.
1. Fai clic su **Visualizza gli attributi avanzati**.
1. Seleziona il campo **Importo totale** dalla tabella **Acquisti**.

#### Definire le impostazioni di raccolta{#collection-settings}

A questo punto, definisci come vengono raccolti i dati e quanti record recuperare.

1. Seleziona **Raccogli dati** nel menu a discesa **Seleziona la modalità di raccolta dei dati**.
1. Digita “3” nel campo **Righe da recuperare (colonne da creare)**.

Se, ad esempio, desideri ottenere l’importo medio degli acquisti per un cliente, seleziona **Dati aggregati** e seleziona **Media** nel menu a discesa **Funzione di aggregazione**.

#### Definire i filtri{#collection-filters}

Ora puoi definire il valore massimo per l’attributo di arricchimento. Gli elementi superiori a 100$ vengono filtrati. <!--[Learn how to work with the query modeler](../../query/query-modeler-overview.md)-->

1. Fai clic su **Modifica filtri**.
1. Aggiungi i due filtri seguenti: **Importo totale** esiste E **Importo totale** è minore di 100. Il primo filtra i valori NULL, in quanto apparirebbero come il valore maggiore.
1. Fai clic su **Conferma**.

#### Definire l’ordinamento{#collection-sorting}

Ora è necessario applicare l’ordinamento per recuperare i tre acquisti **più recenti**.

1. Attiva l’opzione **Abilita ordinamento**.
1. Fai clic all’interno del campo **Attributo**.
1. Seleziona il campo **Data ordine**.
1. Fai clic su **Conferma**.
1. Seleziona **Decrescente** nel menu a discesa **Ordina**.


### Arricchimento con dati collegati {#link-example}

L’esempio seguente mostra una composizione configurata per creare un collegamento tra due transizioni. La prima transizione esegue il targeting dei dati di profilo utilizzando un’attività Query, mentre la seconda include i dati di acquisto memorizzati in un file caricato tramite un’attività Load file.

* Il primo **Arricchimento** l’attività collega il nostro set principale (dati provenienti dal **Query** con lo schema da **Carica file** attività. Questo ci consente di far corrispondere ogni profilo target della query con i dati di acquisto corrispondenti.
* Un secondo **Arricchimento** per arricchire i dati dalla tabella della composizione con i dati di acquisto provenienti dalla sezione **Carica file** attività. Questo ci consente di utilizzare tali dati in ulteriori attività, ad esempio per personalizzare i messaggi inviati ai clienti con le informazioni sul loro acquisto.





<!--

Add other fields
use it in delivery


cardinality between the tables (1-N)
1. select attribute to use as enrichment data

    display advanced fields option
    i button

    note: attributes from the target dimension

1. Select how the data is collected
1. number of records to retrieve if want to retrieve a collection of multiple records
1. Apply filters and build rule

    select an existing filter
    save the filter for reuse
    view results of the filter visually or in code view

1. sort records using an attribute

leverage enrichment data in campaign

where we can use the enrichment data: personalize email, other use cases?

## Example

-->
