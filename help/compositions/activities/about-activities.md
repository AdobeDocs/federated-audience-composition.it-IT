---
audience: end-user
title: Utilizzare le attività
description: Scopri come utilizzare le attività
source-git-commit: 13e7e75fe1dc175fce9464fa58c7a50b5e6107d4
workflow-type: tm+mt
source-wordcount: '274'
ht-degree: 16%

---


# Utilizzare le attività {#activities}

In Federated Audience Composition puoi creare composizioni utilizzando due tipi di attività:

* **Attività di targeting** consente di creare uno o più target definendo un pubblico e suddividendo o combinando questi tipi di pubblico tramite operazioni di intersezione, unione o esclusione.
* **Controllo del flusso** Le attività sono specifiche per organizzare ed eseguire composizioni. Il loro compito principale è quello di coordinare le altre attività.

## Attività di targeting

* [Creare un’attività di pubblico](build-audience.md): definisci la popolazione target. Puoi selezionare un pubblico esistente o utilizzare il modellatore di query per definire una query personalizzata.
* [Cambia dimensione](change-dimension.md): modifica la dimensione di targeting durante la creazione della composizione.
* [Combina](combine.md): esegui la segmentazione sulla popolazione in entrata. Puoi utilizzare un’unione, un’intersezione o un’esclusione.
* [Deduplicazione](deduplication.md): elimina i duplicati nei risultati delle attività in entrata.
* [Arricchimento](enrichment.md): definisci i dati aggiuntivi da elaborare nella composizione. Questa attività consente di sfruttare la transizione in entrata e può essere configurata in modo da completare la transizione in uscita con dati aggiuntivi.
* [Reconciliation](reconciliation.md): definisce il collegamento tra i dati nel database e i dati in una tabella di lavoro, ad esempio i dati caricati da un file esterno.
* [Salva pubblico](save-audience.md): aggiorna un pubblico esistente o creane uno nuovo dalla popolazione calcolata a monte in una composizione.
* [Dividi](split.md): segmenta la popolazione in ingresso in diversi sottoinsiemi.

## Attività di controllo del flusso

* [Unione AND](and-join.md): sincronizza più rami di esecuzione di un flusso di lavoro.
* **Fine** : contrassegna graficamente la fine di un flusso di lavoro. Questa attività non ha alcun impatto funzionale ed è pertanto facoltativa.
* [Fork](fork.md): crea transizioni in uscita per avviare più attività in contemporanea.
* [Scheduler](scheduler.md): pianifica l’avvio del flusso di lavoro.
* [Wait](wait.md): sospende temporaneamente l’esecuzione di una parte di un flusso di lavoro.
