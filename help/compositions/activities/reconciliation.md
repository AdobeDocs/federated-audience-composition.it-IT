---
audience: end-user
title: Utilizzare l’attività Reconciliation
description: Scopri come utilizzare l’attività Reconciliation
source-git-commit: 5fe470ce83a5c3d3df7717bc1203849d99edf430
workflow-type: tm+mt
source-wordcount: '526'
ht-degree: 39%

---


# Riconciliazione {#reconciliation}

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation"
>title="Attività di riconciliazione"
>abstract="L’attività **Riconciliazione** consente di definire il collegamento tra i dati nel database e quelli in una tabella di lavoro."

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation_field"
>title="Campo di selezione riconciliazione"
>abstract="Campo di selezione riconciliazione"

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation_condition"
>title="Condizione di creazione riconciliazione"
>abstract="Condizione di creazione riconciliazione"

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation_complement"
>title="Complemento generato da riconciliazione"
>abstract="Complemento generato da riconciliazione"

L&#39;attività **Reconciliation** ti consente di definire il collegamento tra i dati nel database e i dati in una tabella di lavoro, ad esempio i dati caricati da un sistema esterno.

<!--For example, the **Reconciliation** activity can be placed after a **Load file** activity to import non-standard data into the database. In this case, the **Reconciliation** activity lets you define the link between the data in the Adobe Campaign database and the data in the work table.-->

L&#39;attività **Reconciliation** consente di collegare dati non identificati a risorse esistenti. L&#39;operazione Reconciliation implica che i dati che si stanno unendo sono già presenti nel database. Ad esempio, se desideri riconciliare le informazioni sugli acquisti che mostrano quale prodotto è stato acquistato in un determinato momento da un determinato cliente, ecc., il prodotto e il cliente devono già esistere nel database.

## Configurare l’attività di riconciliazione {#reconciliation-configuration}

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation_targeting"
>title="Schema"
>abstract="Seleziona il nuovo schema da applicare ai dati. Uno schema, noto anche come dimensione targeting, consente di definire la popolazione di destinazione: destinatari, abbonati all’app, operatori, iscritti, ecc. Per impostazione predefinita, è selezionato lo schema corrente della composizione."

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation_rules"
>title="Regole di riconciliazione"
>abstract="Seleziona le regole di riconciliazione da utilizzare per la deduplica. Per utilizzare gli attributi, seleziona l’opzione **Attributi semplici** e scegli i campi di origine e di destinazione. Per creare una condizione di riconciliazione personalizzata utilizzando query modeler, seleziona l’opzione **Condizioni di riconciliazione avanzate**."

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation_targeting_selection"
>title="Selezionare una dimensione di targeting"
>abstract="Seleziona lo schema, noto anche come dimensione targeting, per i dati in entrata da riconciliare."

>[!CONTEXTUALHELP]
>id="dc_orchestration_keep_unreconciled_data"
>title="Mantenere i dati non riconciliati"
>abstract="Per impostazione predefinita, i dati non riconciliati vengono conservati nella transizione in uscita e sono disponibili nella tabella di lavoro per utilizzi futuri. Per rimuovere i dati non riconciliati, disattiva l’opzione **Mantieni i dati non riconciliati**."

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation_attribute"
>title="Attributo di riconciliazione"
>abstract="Seleziona l’attributo da utilizzare per riconciliare i dati e conferma."

Per configurare l&#39;attività **Reconciliation**, eseguire la procedura seguente:

1. Aggiungi un&#39;attività **Reconciliation** nella composizione.

1. Seleziona il **nuovo schema**. Uno schema, noto anche come dimensione di targeting, consente di definire la popolazione target: destinatari, abbonati all’app, operatori, abbonati, ecc.

1. Seleziona i campi da utilizzare per la riconciliazione. Puoi utilizzare uno o più criteri di riconciliazione.

   1. Per utilizzare gli attributi per riconciliare i dati, seleziona l&#39;opzione **Attributi semplici**, quindi fai clic sul pulsante **Aggiungi regola**.
   1. Selezionare i campi **Source** e **Destination** per la riconciliazione. Il campo **Source**. Il campo **Destinazione** corrisponde ai campi dello schema selezionato.

      I dati vengono riconciliati quando l’origine e la destinazione sono uguali. Ad esempio, seleziona i campi **E-mail** per deduplicare i profili in base al loro indirizzo e-mail.

      Per aggiungere un altro criterio di riconciliazione, fare clic sul pulsante **Aggiungi regola**. Se sono specificate più condizioni di unione, è necessario verificarle TUTTE in modo che i dati possano essere collegati tra loro.

      ![](../assets/reconciliation-rules.png)

   1. Per utilizzare altri attributi per riconciliare i dati, selezionare l&#39;opzione **Condizioni di riconciliazione avanzate**, quindi fare clic sul pulsante **Crea condizioni**. Puoi quindi creare una condizione di riconciliazione personalizzata utilizzando Query Modeler. [Scopri come utilizzare Query Modeler](../../query/query-modeler-overview.md)

      ![](../assets/reconciliation-advanced.png)

1. Puoi filtrare i dati da riconciliare utilizzando il pulsante **Crea filtro**. Questo consente di creare una condizione personalizzata utilizzando il modellatore di query.

Per impostazione predefinita, i dati non riconciliati vengono conservati nella transizione in uscita e sono disponibili nella tabella di lavoro per utilizzi futuri. Per rimuovere i dati non riconciliati, disattiva l’opzione **Mantieni i dati non riconciliati**.

<!--
## Example {#reconciliation-example}

The following example demonstrates a workflow that creates an audience of profiles directly from an imported file containing new clients. It is made up of the following activities:

The workflow is designed as follows:

![](../assets/workflow-reconciliation-sample-1.0.png)

 
It is built with the following activities:

* A [Load file](load-file.md) activity uploads a file containing profiles data that were extracted from an external tool.

    For example:

    ```
    lastname;firstname;email;birthdate;
    JACKMAN;Megan;megan.jackman@testmail.com;07/08/1975;
    PHILLIPS;Edward;phillips@testmail.com;09/03/1986;
    WEAVER;Justin;justin_w@testmail.com;11/15/1990;
    MARTIN;Babe;babeth_martin@testmail.net;11/25/1964;
    REESE;Richard;rreese@testmail.com;02/08/1987;
    ```

* A **Reconciliation** activity which identifies the incoming data as profiles, by using the **email** and **Date of birth** fields as reconciliation criteria.

    ![](../assets/workflow-reconciliation-sample-1.1.png)

* A [Save audience](save-audience.md) activity to create a new audience based on these updates. You can also replace the **Save audience** activity by an **End** activity if no specific audience needs to be created or updated. Recipient profiles are updated in any case when you run the workflow.


## Compatibility {#reconciliation-compat}

The **Reconciliation** activity does not exist in the Client console. All **Enrichments** activities created in the Client console with the reconciliation options enabled are displayed as **Reconciliation** activities in Campaign Web user interface.
-->
