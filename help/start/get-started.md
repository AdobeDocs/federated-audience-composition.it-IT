---
title: Guida introduttiva di Experience Platform Federated Audience Composition
description: Scopri cos’è Adobe Federated Audience Composition e come utilizzarlo in Adobe Experience Platform
badge: label="Disponibilità limitata" type="Informative"
exl-id: 43464aea-9c1d-4f1f-859f-82f209f350b7
source-git-commit: 75f997e4b1c0338a635dff43e2254757fbc5ec69
workflow-type: tm+mt
source-wordcount: '708'
ht-degree: 8%

---

# Guida introduttiva alla composizione federata del pubblico {#gs-fac}

Federated Audience Composition è una funzionalità aggiuntiva per [Adobe Real-time Customer Data Platform](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/home){target="_blank"} e [Adobe Journey Optimizer](https://experienceleague.adobe.com/it/docs/journey-optimizer/using/ajo-home){target="_blank"} che consente di creare e arricchire i tipi di pubblico dai data warehouse di terze parti e di importare i tipi di pubblico in Adobe Experience Platform. Federated Audience Composition offre una soluzione semplice e potente per collegare il data warehouse aziendale direttamente all’interno di Adobe Real-time Customer Data Platform e/o Adobe Journey Optimizer ed eseguire query sulle tabelle del data warehouse.

Adobe Federated Audience Composition consente agli utenti delle app Adobe Experience Platform di accedere ai dati dei propri clienti archiviati nei data warehouse e nelle piattaforme di archiviazione cloud, come Amazon Redshift, Azure synapse Analytics e altro ancora. I dati dei clienti possono risiedere in più data warehouse e sono ora accessibili immediatamente, senza replica. Le piattaforme supportate sono elencate in [questa pagina](../connections/federated-db.md#supported-db).

## Funzionalità {#rn-capabilities}

La Federated Audience Composition estende il valore di Real-Time CDP e Journey Optimizer con un approccio completo alla cura e all’attivazione del pubblico:

* Espandi l’accesso ai set di dati critici basati su data warehouse per creare tipi di pubblico di alto valore: utilizza i data warehouse esistenti come sistema principale di record, sfruttando al contempo le applicazioni migliori per fornire ai clienti esperienze ottimali.

* Supporto completo per casi di utilizzo di coinvolgimento: Federated Audience Composition, in combinazione con Real-Time CDP o Journey Optimizer supporta esperienze personalizzate avviate dal marchio con tipi di pubblico federati e offre esperienze istantanee attivate da eventi in tempo reale, combinate con attributi di persona per soddisfare i requisiti dei casi di utilizzo tra i team.

* Minimizzare lo spostamento e la duplicazione dei dati: crea tipi di pubblico da set di dati che risiedono in un data warehouse aziendale senza copiare i dati sottostanti per gestire profili di marketing e tipi di pubblico utilizzabili.

* Utilizza un singolo sistema per flussi di lavoro basati sull’esperienza: cura i tipi di pubblico acquisiti e federati in Adobe Experience Platform e coordina le esperienze in uscita su tutti i canali.

## Casi d’uso {#rn-uc}

Tramite un’interfaccia utente di semplice marketing, puoi creare regole di segmento per eseguire query nel data warehouse su un elenco di utenti idonei per un segmento specifico necessario per le campagne di marketing, accedere ai tipi di pubblico esistenti nel warehouse per l’attivazione o arricchire i tipi di pubblico di Adobe Experience Platform con punti dati aggiuntivi esistenti nel warehouse.

In questa versione sono disponibili due casi d’uso:

1. Creazione di pubblico: crea nuovi tipi di pubblico dai set di dati aziendali senza copiare i dati sottostanti e attivali con le destinazioni predefinite&#x200B;

1. Arricchimento del pubblico: arricchisci i tipi di pubblico esistenti in Adobe Experience Platform utilizzando dati del pubblico composti che sono stati federati dal data warehouse aziendale. Questi dati non verranno mantenuti nei profili cliente di Adobe Experience Platform.

![diagramma](assets/fac-use-cases.png){zoomable="yes"}{width="75%" align="center"}

## Passaggi chiave {#gs-steps}

Adobe Federated Audience Composition consente di creare e aggiornare i tipi di pubblico di Adobe Experience Platform direttamente dal database, senza alcun processo di acquisizione.

![diagramma](assets/steps-diagram.png){zoomable="yes"}{width="85%" align="center"}

Passaggi chiave:

1. **Integrazione dei dati**: riunisci i dati provenienti da varie origini e uniscili in un set di dati unificato. Scopri come connettere le app Adobe Experience Platform al tuo data warehouse aziendale, i database supportati e come configurarli: vedi [questa sezione](../connections/federated-db.md).

2. **Modellazione dati**: progetta e crea modelli di dati e schemi che definiscono la struttura, le relazioni e i vincoli dei dati. Ulteriori informazioni sugli schemi in [questa pagina](../customer/schemas.md). Scopri come creare collegamenti per il modello dati in [questa pagina](../data-management/gs-models.md).

3. **Trasformazione dei dati**: applicare tecniche di manipolazione dei dati per modificare il formato, la struttura o i valori degli elementi dati in modo da renderli compatibili o idonei per applicazioni o analisi specifiche.

4. **Utilizzo dati**: crea, orchestra e crea tipi di pubblico. Scopri come comporre il pubblico in [questa pagina](../compositions/gs-compositions.md). Puoi anche aggiornare o riutilizzare i tipi di pubblico esistenti tramite il portale del pubblico di Adobe Experience Platform e Destinazioni. Per ulteriori informazioni, consulta [questa pagina](../connections/destinations.md).


>[!NOTE]
>
>Dopo aver eseguito la composizione, il pubblico risultante viene salvato in Adobe Experience Platform come pubblico esterno e disponibile in Adobe Real-Time Customer Data Platform e/o Adobe Journey Optimizer. È reso accessibile nel menu **Tipi di pubblico**. [Ulteriori informazioni](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/audience-portal){target="_blank"}
>



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
