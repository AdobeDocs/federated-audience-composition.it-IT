---
title: Domande frequenti
description: Domande frequenti
badge: label="Disponibilità limitata" type="Informative"
source-git-commit: 6cfd3bd85d7811e00e716042502c7d7b23fa4ad9
workflow-type: tm+mt
source-wordcount: '916'
ht-degree: 2%

---


# Domande frequenti {#faq}

Di seguito è riportato un elenco di domande frequenti sulla Federated Audience Composition. Sono inoltre disponibili domande frequenti globali per il servizio di segmentazione di Adobe Experience Platform in [questa pagina](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/faq){target="_blank"}.


+++Quali sono le autorizzazioni necessarie per accedere a Federated Audience Composition?

Non esistono autorizzazioni specifiche per Federated Audience Composition. L’unico prerequisito per accedere a questa funzionalità è aver acquistato il componente aggiuntivo Federated Audience Composition.

+++

+++Quali warehouse cloud sono supportati?

Per questa versione, Federated Audience Composition è compatibile con:

*  Amazon Redshift
* Azure synapse
* Google BigQuery
* Snowflake
* Vertica Analytics

+++


+++È possibile eseguire query su più data warehouse nella stessa composizione?

Sì, è possibile eseguire query in più warehouse nella stessa composizione e combinare dati provenienti da più origini.  In genere, ogni [attività di composizione](../compositions/orchestrate-activities.md) (Query, Enrichment, Split, ecc.) esegue una o più istruzioni SQL in base alla configurazione dell&#39;attività, ai database di destinazione (possono esistere più casi di accesso ai dati federati) e agli output di una o più tabelle di lavoro con il risultato dell&#39;esecuzione. Tali tabelle di lavoro vengono utilizzate come input per attività consecutive.

+++

+++ Posso accedere all’intero database utilizzando Federated Audience Composition?

No, è possibile configurare l&#39;accesso a un database o a uno schema dedicato o condiviso. Ti consigliamo di creare uno schema dedicato solo per Federated Audience Composition e di copiare/condividere set di dati del caso aziendale.
+++



+++Posso accedere a tutte le tabelle nello schema dedicato?

Sì, una volta connessa, Federated Audience Composition può essere utilizzato per scoprire tutte le tabelle in base ai diritti iniziali definiti, quindi puoi utilizzare l’editor schema visivo per:

* Individuare le colonne e le chiavi primarie dalle tabelle
* Creare etichette intuitive per tali tabelle
* Creare etichette intuitive per ogni colonna
* Nascondi colonne non necessarie
* Salva la descrizione di tali tabelle
+++


+++Esiste un’archiviazione temporanea in Federated Audience Composition?

No, Federated Audience Composition memorizza solo i metadati (descrizioni dello schema). Nessun dato cliente è in fase di transizione. Il flusso di esportazione del pubblico viene eseguito direttamente da Adobe Experience Platform Audience Portal (tramite [Destination](../connections/destinations.md)) al database del cliente. Il flusso di creazione e aggiornamento viene eseguito direttamente dal database del data warehouse a Adobe Experience Platform Audience Portal.

+++

+++Federated Audience Composition memorizza una copia fisica dell’elenco di persone da inviare ai sistemi a valle?

Federated Audience Composition non mantiene una copia fisica dei dati. La frequenza è configurata nella composizione per definire la frequenza con cui verranno aggiornati i dati. I dati del pubblico risultanti non vengono memorizzati da Adobe Experience Platform più a lungo di quanto richiesto dai casi d’uso o dalle azioni del cliente.

Ad esempio:

* Nel caso della segmentazione del pubblico, il pubblico viene creato nel tuo data warehouse e puoi utilizzare la Composizione federata del pubblico per ulteriori attività di composizione e manipolazione dei dati prima di pubblicare il pubblico risultante e gli attributi associati tramite Adobe Experience Platform Audience Portal. La definizione del pubblico e gli attributi associati vengono trasmessi a Adobe Experience Platform.
Tieni presente che la scadenza corrente dei dati per i tipi di pubblico generati esternamente è di 30 giorni. Questa scadenza riduce la quantità di dati in eccesso archiviati all’interno di un’organizzazione. Al termine del periodo di scadenza dei dati, il set di dati associato rimane visibile all’interno dell’inventario dei set di dati, ma non è possibile attivare il pubblico e il conteggio dei profili viene visualizzato come zero. Ulteriori informazioni nella [documentazione di Adobe Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/faq#how-long-do-externally-generated-audiences-last-for){target="_blank"}.

* Nel caso di un pubblico di tipo Arricchimento pubblico, il punto di partenza è un pubblico Adobe Experience Platform esistente. Si possono esaminare due scenari:
   1. Acquisisci attributi aggiuntivi del payload del pubblico dal data warehouse federato: in questo caso, gli attributi aggiuntivi aggiunti verranno visualizzati come parte della definizione del pubblico. La scadenza dei dati per i tipi di pubblico generati esternamente è la stessa di cui sopra, ovvero 30 giorni.
   1. Perfeziona il pubblico Adobe Experience Platform esistente in base agli attributi aggiuntivi presenti nel data warehouse. Ad esempio, un pubblico di clienti ha mostrato interesse per un particolare prodotto sul sito web negli ultimi due mesi. Ora vuoi prendere questo pubblico e segmentarlo ulteriormente utilizzando Federated Audience Composition per includere solo i clienti che hanno un punteggio di credito elevato. Il punteggio di credito è considerato sensibile e i singoli punti dati del punteggio di credito non vengono copiati dal data warehouse.
+++

+++Se i dati dei pattern di casi di utilizzo di segmentazione del pubblico e arricchimento del pubblico non vengono mantenuti, come vengono memorizzati temporaneamente?

I dati del pubblico risultanti non persistono a tempo indefinito in Adobe Experience Platform o nella Federated Audience Composition. Non verrà conservato più a lungo di quanto richiesto dal tuo caso d’uso. Gli attributi del pubblico portati come parte del payload del pubblico persisteranno solo come parte della definizione del pubblico. La durata della persistenza si basa sul TTL per qualsiasi pubblico; il valore predefinito è 30 giorni.

+++

+++Posso eliminare un pubblico caricato personalizzato?

Puoi eliminare i tipi di pubblico non utilizzati nell’attivazione a valle direttamente in Audience Portal selezionando semplicemente elimina dal menu delle azioni. Ulteriori informazioni nella [documentazione di Adobe Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/faq#how-do-i-put-an-audience-in-the-deleted-state){target="_blank"}.

+++

+++Se combino dati provenienti da più origini, in che modo uniamo i dati? Stiamo utilizzando il servizio Identity?

No, il servizio Identity non viene utilizzato durante una composizione. I dati tra le varie sorgenti utilizzate nella composizione vengono uniti tramite logica definita dall’utente (come espressa nel modello sottostante), ad esempio ID CRM, numero account utente, ecc. È necessario selezionare l’identità utilizzata come identificatore nel pubblico per la selezione nel data warehouse. In un pubblico risultante da Federated Audience Composition, devi identificare lo spazio dei nomi dell’identità nel set di dati risultante.

+++

<!--
+++If I want to combine federated data with datasets that live in Adobe Experience Platform, how is this done?

Likewise, the Identity Service is not being leveraged in this scenario either. The data model underpinning a composition needs to express how the data warehouse data and the audience to be enriched are related. e.g. assume an existing audience in Adobe Experience Platform contains several attributes, among which is the CRM ID. Assume transactional data is in the data warehouse containing purchases with various attributes, including the CRM ID of the purchaser. The end-user would have to specify that the CRM ID for both objects is used to stitch the two objects together.

+++
-->