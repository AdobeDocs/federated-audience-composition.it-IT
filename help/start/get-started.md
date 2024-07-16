---
title: Guida introduttiva alla composizione federata del pubblico
description: Scopri cos’è Adobe Federated Audience Composition e come utilizzarlo in Adobe Experience Platform
source-git-commit: 25f623cde151824effddea34127a82e8d920f3e2
workflow-type: tm+mt
source-wordcount: '284'
ht-degree: 34%

---


# Guida introduttiva alla composizione federata del pubblico {#gs-fac}

Adobe Federated Audience Composition consente agli utenti delle app Adobe Experience Platform di accedere ai dati dei propri clienti memorizzati nel data warehouse aziendale. I dati dei clienti possono risiedere in più data warehouse e devono essere immediatamente accessibili, senza replica.

Federated Audience Composition di Adobe Experience Platform offre una soluzione semplice e potente per collegare il data warehouse aziendale direttamente all’interno di Adobe Real-time Customer Data Platform ed eseguire query sulle tabelle del data warehouse.

## Passaggi chiave {#gs-steps}

Adobe Federated Audience Composition consente di creare e aggiornare i tipi di pubblico di Adobe Experience Platform direttamente dal database, senza alcun processo di acquisizione.

![diagramma](assets/FAC-diagram.png)

Passaggi chiave:

* **Configurazione**

   1. Connettere Adobe Experience Platform e il data warehouse aziendale.
Sono supportati i seguenti database: Snowflake, Google Big Query, Azure synapse, Redshift.
Per ulteriori informazioni, consulta [questa pagina](../connections/federated-db.md).
   1. Crea schemi per selezionare i dati da rendere accessibili dall’interfaccia utente.
Per ulteriori informazioni, consulta [questa pagina](../customer/schemas.md).
   1. Crea collegamenti per il modello dati.
Per ulteriori informazioni, consulta [questa pagina](../data-management/gs-models.md).

* **Componi pubblico**

   1. Progetta ed esegui composizioni per creare tipi di pubblico.
Per ulteriori informazioni, consulta [questa pagina](../compositions/gs-compositions.md).
   1. Aggiorna o riutilizza i tipi di pubblico esistenti tramite il portale del pubblico e le destinazioni di Adobe Experience Platform.
Per ulteriori informazioni, consulta [questa pagina](../connections/destinations.md).

## Ulteriori informazioni {#learn}

<!-- Workflow + Workflow activities-->



>[!CONTEXTUALHELP]
>id="dc_workflow_settings_execution"
>title="Impostazioni di esecuzione"
>abstract="In questa sezione, puoi configurare le impostazioni relative all’esecuzione del flusso di lavoro, ad esempio il numero di giorni in cui viene mantenuta la cronologia del flusso di lavoro."




>[!CONTEXTUALHELP]
>id="dc_orchestration_query_enrichment_noneditable"
>title="Attività non modificabile"
>abstract="Quando un’attività **Query** o **Arricchimento** è configurata con dati aggiuntivi nella console; i dati di arricchimento vengono presi in considerazione e trasmessi nella transizione in uscita, ma non possono essere modificati."

<!-- Create a link -->

>[!CONTEXTUALHELP]
>id="dc_federated_database_create_link"
>title="Creare un collegamento"
>abstract="Definire le impostazioni del collegamento."
