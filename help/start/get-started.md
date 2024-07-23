---
title: Guida introduttiva alla composizione federata del pubblico
description: Scopri cos’è Adobe Federated Audience Composition e come utilizzarlo in Adobe Experience Platform
badge: label="Disponibilità limitata" type="Informative"
source-git-commit: 6cfd3bd85d7811e00e716042502c7d7b23fa4ad9
workflow-type: tm+mt
source-wordcount: '478'
ht-degree: 12%

---


# Guida introduttiva alla composizione federata del pubblico {#gs-fac}

Federated Audience Composition è un componente aggiuntivo per Adobe Real-time Customer Data Platform e Adobe Journey Optimizer che consente di creare e arricchire i tipi di pubblico dai data warehouse di terze parti e di importarli in Adobe Experience Platform. Federated Audience Composition offre una soluzione semplice e potente per collegare il data warehouse aziendale direttamente all’interno di Adobe Real-time Customer Data Platform e/o Adobe Journey Optimizer ed eseguire query sulle tabelle del data warehouse.

Adobe Federated Audience Composition consente agli utenti delle app Adobe Experience Platform di accedere ai dati dei propri clienti archiviati nei data warehouse e nelle piattaforme di archiviazione cloud, come Amazon Redshift, Azure synapse Analytics e altro ancora. I dati dei clienti possono risiedere in più data warehouse e sono ora accessibili immediatamente, senza replica. Le piattaforme supportate sono elencate in [questa pagina](../connections/federated-db.md#supported-db).

## Casi d’uso {#rn-uc}

Tramite un’interfaccia utente di semplice marketing, puoi creare regole di segmento per eseguire query nel data warehouse su un elenco di utenti idonei per un segmento specifico necessario per le campagne di marketing, accedere ai tipi di pubblico esistenti nel warehouse per l’attivazione o arricchire i tipi di pubblico di Adobe Experience Platform con punti dati aggiuntivi esistenti nel warehouse.

In questa versione sono disponibili due casi d’uso: segmentazione del pubblico e arricchimento del pubblico. L’arricchimento del profilo sarà disponibile in una versione futura.

![diagramma](assets/fac-use-cases.png){zoomable="yes"}

## Passaggi chiave {#gs-steps}

Adobe Federated Audience Composition consente di creare e aggiornare i tipi di pubblico di Adobe Experience Platform direttamente dal database, senza alcun processo di acquisizione.

![diagramma](assets/steps-diagram.png){zoomable="yes"}

Passaggi chiave:

1. **Integrazione dei dati**: riunisci i dati provenienti da varie origini e uniscili in un set di dati unificato. Scopri come connettere le app Adobe Experience Platform al tuo data warehouse aziendale, i database supportati e come configurarli: vedi [questa sezione](../connections/federated-db.md).

2. **Modellazione dati**: progetta e crea modelli di dati e schemi che definiscono la struttura, le relazioni e i vincoli dei dati. Ulteriori informazioni sugli schemi in [questa pagina](../customer/schemas.md). Scopri come creare collegamenti per il modello dati in [questa pagina](../data-management/gs-models.md).

3. **Trasformazione dei dati**: applicare tecniche di manipolazione dei dati per modificare il formato, la struttura o i valori degli elementi dati in modo da renderli compatibili o idonei per applicazioni o analisi specifiche.

4. **Utilizzo dati**: crea, orchestra e crea tipi di pubblico. Scopri come comporre il pubblico in [questa pagina](../compositions/gs-compositions.md). Puoi anche aggiornare o riutilizzare i tipi di pubblico esistenti tramite il portale del pubblico di Adobe Experience Platform e Destinazioni. Per ulteriori informazioni, consulta [questa pagina](../connections/destinations.md).



## Ulteriori informazioni {#learn}

<!-- Workflow + Workflow activities-->

Vedi le domande frequenti in [questa pagina](faq.md).

>[!CONTEXTUALHELP]
>id="dc_workflow_settings_execution"
>title="Impostazioni di esecuzione"
>abstract="In questa sezione puoi configurare le impostazioni relative all’esecuzione del flusso di lavoro, ad esempio il numero di giorni in cui viene mantenuta la cronologia della composizione."




>[!CONTEXTUALHELP]
>id="dc_orchestration_query_enrichment_noneditable"
>title="Attività non modificabile"
>abstract="Quando un’attività **Query** o **Arricchimento** è configurata con dati aggiuntivi nella console; i dati di arricchimento vengono presi in considerazione e trasmessi nella transizione in uscita, ma non possono essere modificati."

<!-- Create a link -->

>[!CONTEXTUALHELP]
>id="dc_federated_database_create_link"
>title="Creare un collegamento"
>abstract="Definire le impostazioni del collegamento."
