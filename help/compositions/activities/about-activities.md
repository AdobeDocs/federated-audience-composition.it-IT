---
audience: end-user
title: Utilizzare le attività
description: Scopri come utilizzare le attività
exl-id: 1e4e5f53-636f-4f1c-bf2f-cc3b5d6d6dda
source-git-commit: 2a21dcde345febdaad0934c8835df5f7ae8c30f6
workflow-type: tm+mt
source-wordcount: '289'
ht-degree: 17%

---

# Utilizzare le attività {#activities}

In Federated Audience Composition puoi creare composizioni utilizzando due tipi di attività:

* **Le attività di targeting** ti consentono di creare una o più destinazioni definendo un pubblico e suddividendo o combinando questi tipi di pubblico tramite operazioni di intersezione, unione o esclusione.
* **Le attività del controllo di flusso** sono specifiche per l&#39;organizzazione e l&#39;esecuzione delle composizioni. Il loro compito principale è quello di coordinare le altre attività.

## Attività di targeting

* [Genera attività pubblico](build-audience.md): definisci la popolazione target. Puoi selezionare un pubblico esistente o utilizzare il modellatore di query per definire una query personalizzata.
* [Modifica origine dati](./change-data-source.md): modifica l&#39;origine dati utilizzata dalla composizione.
* [Modifica dimensione](change-dimension.md): modifica lo schema, noto anche come dimensione di targeting, durante la creazione della composizione.
* [Combina](combine.md): esegui la segmentazione del gruppo in entrata. Puoi utilizzare un’unione, un’intersezione o un’esclusione.
* [Deduplicazione](deduplication.md): elimina i duplicati nei risultati delle attività in entrata.
* [Arricchimento](enrichment.md): definisci i dati aggiuntivi da elaborare nella composizione. Questa attività consente di sfruttare la transizione in entrata e può essere configurata in modo da completare la transizione in uscita con dati aggiuntivi.
* [Riconciliazione](reconciliation.md): definire il collegamento tra i dati nel database e i dati in una tabella di lavoro, ad esempio i dati caricati da un file esterno.
* [Salva pubblico](save-audience.md): aggiorna un pubblico esistente o crea un nuovo pubblico dalla popolazione calcolata a monte in una composizione.
* [Dividi](split.md): segmenta la popolazione in ingresso in diversi sottoinsiemi.

## Attività di controllo del flusso

* [AND-join](and-join.md): sincronizza più rami di esecuzione di una composizione.
* **Fine**: contrassegna graficamente la fine di una composizione. Questa attività non ha alcun impatto funzionale ed è pertanto facoltativa.
* [Fork](fork.md): crea transizioni in uscita per avviare più attività contemporaneamente.
* [Scheduler](scheduler.md): pianifica l&#39;avvio della composizione.
* [Attendi](wait.md): sospende temporaneamente l&#39;esecuzione di una parte di una composizione.
