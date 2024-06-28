---
audience: end-user
title: Utilizzo del query modeler
description: Scopri come utilizzare Query Modeler.
source-git-commit: f6730819712ffcbe815517a4406dac7e8fb9779c
workflow-type: tm+mt
source-wordcount: '376'
ht-degree: 21%

---

# Utilizzo del query modeler {#segment-builder}

>[!CONTEXTUALHELP]
>id="dc_orchestration_querymodeler_querymessage"
>title="Query modeler"
>abstract="Definisci i criteri di filtro per i destinatari o qualsiasi altra dimensione di targeting dal database."

Query Modeler semplifica il processo di filtraggio del database in base a vari criteri. Inoltre, Query Modeler è in grado di gestire in modo efficiente query molto complesse e lunghe, offrendo maggiore flessibilità e precisione. Inoltre, supporta filtri predefiniti all’interno di condizioni, consentendoti di perfezionare le query con facilità e allo stesso tempo di utilizzare espressioni avanzate e operatori per strategie complete di targeting del pubblico e segmentazione.

## Accedere al query modeler

Il query modeler è disponibile in ogni contesto in cui è necessario definire regole per filtrare i dati.

| Utilizzo | Esempio |
|  ---  |  ---  |
| **Definire i tipi di pubblico**: specifica la popolazione di cui desideri eseguire il targeting nelle composizioni e crea facilmente nuovi tipi di pubblico su misura per le tue esigenze. | ![](assets/access-audience.png){zoomable="yes"}{width="200" align="center" zoomable="yes"} |
| **Personalizzare le attività del flusso di lavoro**: applica regole nelle attività del flusso di lavoro, ad esempio **Dividi** e **Reconciliation**, per allinearlo ai requisiti specifici. [Ulteriori informazioni sulle attività del flusso di lavoro](../compositions/activities/about-activities.md) | ![](assets/access-workflow.png){zoomable="yes"}{width="200" align="center" zoomable="yes"} |
| **Filtri preimpostati**: crea filtri preimpostati che fungono da scelte rapide durante varie operazioni di filtraggio, sia nell’utilizzo di elenchi di dati che nella formazione del tipo di pubblico per una consegna. | ![](assets/access-predefined-filter.png){zoomable="yes"}{width="200" align="center" zoomable="yes"} |
| **Personalizzare gli elenchi**: crea regole personalizzate per filtrare i dati visualizzati in elenchi come destinatari, elenchi di consegne, ecc. | ![](assets/access-lists.png){zoomable="yes"}{width="200" align="center" zoomable="yes"} |

## Interfaccia del query modeler {#interface}

Il modellatore di query fornisce un’area di lavoro centrale in cui creare la query e un riquadro a destra che fornisce informazioni sulla query.

![](assets/query-interface.png){zoomable="yes"}

### Area di lavoro centrale {#canvas}

L’area di lavoro centrale di Query Modeler è il luogo in cui puoi aggiungere e combinare i diversi componenti che creano la query. [Scopri come creare una query](build-query.md)

La barra degli strumenti situata nell’angolo superiore destro dell’area di lavoro offre opzioni per manipolare facilmente i componenti della query e navigare nell’area di lavoro:

* **Modalità di selezione multipla**: seleziona più componenti filtro per copiarli e incollarli nella posizione desiderata.
* **Ruota**: cambia l’area di lavoro verticalmente.
* **Adatta allo schermo**: adatta il livello di zoom dell’area di lavoro allo schermo.
* **Zoom indietro** / **Zoom in**: zoom indietro o nell’area di lavoro.
* **Visualizza mappa**: apre un’istantanea dell’area di lavoro che mostra la tua posizione.

### Riquadro delle proprietà della regola {#rule-properties}

Sul lato destro, il **[!UICONTROL Proprietà delle regole]** fornisce informazioni sulla query. Consente di eseguire varie operazioni per verificare la query e assicurarsi che sia adatta alle tue esigenze. [Scopri come controllare e convalidare la query](build-query.md#check-and-validate-your-query)
