---
audience: end-user
title: Utilizzare l’attività Reconciliation
description: Scopri come utilizzare l’attività Reconciliation
source-git-commit: 4ba457f1dcd8b7997931a70d93a95f6a54c51cb5
workflow-type: tm+mt
source-wordcount: '518'
ht-degree: 23%

---


# Riconciliazione {#reconciliation}

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation"
>title="Attività di riconciliazione"
>abstract="Il **Reconciliation** attività ti consente di definire il collegamento tra i dati nel database e i dati in una tabella di lavoro."

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

Il **Reconciliation** activity (attività) consente di definire il collegamento tra i dati nel database e i dati in una tabella di lavoro, ad esempio i dati caricati da un sistema esterno.

<!--For example, the **Reconciliation** activity can be placed after a **Load file** activity to import non-standard data into the database. In this case, the **Reconciliation** activity lets you define the link between the data in the Adobe Campaign database and the data in the work table.-->

Il **Reconciliation** L’attività ti consente di collegare dati non identificati a risorse esistenti. L&#39;operazione Reconciliation implica che i dati che si stanno unendo sono già presenti nel database. Ad esempio, se desideri riconciliare le informazioni sugli acquisti che mostrano quale prodotto è stato acquistato in un determinato momento da un determinato cliente, ecc., il prodotto e il cliente devono già esistere nel database.

## Configurare l’attività di riconciliazione {#reconciliation-configuration}

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation_targeting"
>title="Schema"
>abstract="Seleziona il nuovo schema da applicare ai dati. Uno schema, noto anche come dimensione di targeting, consente di definire la popolazione target: destinatari, abbonati all’app, operatori, abbonati, ecc. Per impostazione predefinita, viene selezionato lo schema corrente della composizione."

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation_rules"
>title="Regole di riconciliazione"
>abstract="Seleziona le regole di riconciliazione da utilizzare per la deduplica. Per utilizzare gli attributi, seleziona l’opzione **Attributi semplici** e scegli i campi di origine e di destinazione. Per creare una condizione di riconciliazione personalizzata utilizzando query modeler, seleziona l’opzione **Condizioni di riconciliazione avanzate**."

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation_targeting_selection"
>title="Selezionare una dimensione di targeting"
>abstract="Seleziona lo schema, noto anche come dimensione di targeting, con cui riconciliare i dati in entrata."

>[!CONTEXTUALHELP]
>id="dc_orchestration_keep_unreconciled_data"
>title="Mantenere i dati non riconciliati"
>abstract="Per impostazione predefinita, i dati non riconciliati vengono conservati nella transizione in uscita e sono disponibili nella tabella di lavoro per utilizzi futuri. Per rimuovere i dati non riconciliati, disattiva l’opzione **Mantieni i dati non riconciliati**."

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation_attribute"
>title="Attributo di riconciliazione"
>abstract="Selezionare l&#39;attributo da utilizzare per riconciliare i dati e confermare."

Per configurare il **Reconciliation** attività:

1. Aggiungi un **Reconciliation** attività nella composizione.

1. Seleziona la **Nuovo schema**. Uno schema, noto anche come dimensione di targeting, consente di definire la popolazione target: destinatari, abbonati all’app, operatori, abbonati, ecc.

1. Seleziona i campi da utilizzare per la riconciliazione. Puoi utilizzare uno o più criteri di riconciliazione.

   1. Per utilizzare gli attributi per riconciliare i dati, selezionare **Attributi semplici** quindi fare clic sul pulsante **Aggiungi regola** pulsante.
   1. Seleziona la **Source** e **Destinazione** campi per la riconciliazione. Il **Source** campo. Il **Destinazione** corrisponde ai campi dello schema selezionato.

      I dati vengono riconciliati quando l’origine e la destinazione sono uguali. Ad esempio, seleziona la **E-mail** per deduplicare i profili in base al loro indirizzo e-mail.

      Per aggiungere un altro criterio di riconciliazione, fai clic su **Aggiungi regola** pulsante. Se sono specificate più condizioni di unione, è necessario verificarle TUTTE in modo che i dati possano essere collegati tra loro.

      ![](../assets/reconciliation-rules.png)

   1. Per utilizzare altri attributi per riconciliare i dati, selezionare **Condizioni di riconciliazione avanzate** quindi fare clic sul pulsante **Creare condizioni** pulsante. Puoi quindi creare una condizione di riconciliazione personalizzata utilizzando Query Modeler.

      ![](../assets/reconciliation-advanced.png)

1. È possibile filtrare i dati da riconciliare utilizzando **Crea filtro** pulsante. Questo consente di creare una condizione personalizzata utilizzando il modellatore di query.

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
