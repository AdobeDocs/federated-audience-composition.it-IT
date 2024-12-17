---
title: Domande frequenti
description: Domande frequenti sulla composizione di pubblico federato di Adobe Experience Platform
exl-id: 68cc0ae5-5c41-425f-8b10-ab3515294006
source-git-commit: 1bdab901b7aae3019b672a34eab184405c927f56
workflow-type: tm+mt
source-wordcount: '1004'
ht-degree: 82%

---

# Domande frequenti {#faq}

Di seguito è riportato un elenco di domande frequenti sulla composizione di pubblico federato di Adobe Experience Platform. Sono inoltre disponibili domande frequenti globali per il servizio di segmentazione di Adobe Experience Platform in [questa pagina](https://experienceleague.adobe.com/it/docs/experience-platform/segmentation/faq){target="_blank"}.


+++Quali sono le autorizzazioni necessarie per accedere alla composizione di pubblico federato?

La composizione di pubblico federato richiede i pacchetti Adobe Real-time Customer Data Platform e Adobe Journey Optimizer Prime o Ultimate. Devi anche aver acquistato il componente aggiuntivo Composizione di pubblico federato.

Per utilizzare la composizione di pubblico federato, ogni utente deve essere aggiunto a un profilo specifico creato per ogni sandbox. Per ulteriori informazioni, consulta la pagina [Accedere alla composizione di pubblico federato](access-prerequisites.md).

+++

+++Quali data warehouse cloud sono supportati?

L’elenco dei sistemi supportati con la composizione di pubblico federato è disponibile in [questa pagina](../start/access-prerequisites.md#supported-systems).

+++


+++È possibile eseguire query su più data warehouse nella stessa composizione?

Sì, è possibile eseguire query su più data warehouse nella stessa composizione e combinare dati provenienti da più origini.  In genere, ogni [attività di composizione](../compositions/orchestrate-activities.md) (Query, Arricchimento, Suddivisione, ecc.) esegue una o più istruzioni SQL in base alla configurazione dell’attività, ai database di destinazione (possono esistere più casi di Federated Data Access) e agli output di una o più tabelle di lavoro con il risultato dell’esecuzione. Tali tabelle di lavoro vengono utilizzate come input per attività consecutive.

+++

+++ È possibile accedere all’intero database utilizzando la composizione di pubblico federato?

No, è possibile configurare l’accesso a un database o a uno schema dedicato o condiviso. Ti consigliamo di creare uno schema dedicato solo per la composizione di pubblico federato e di copiare/condividere set di dati del caso di business.
+++

+++È possibile accedere a tutte le tabelle nello schema dedicato?

Sì, una volta connessa, la composizione di pubblico federato può essere utilizzata per scoprire tutte le tabelle in base ai diritti iniziali definiti, quindi puoi utilizzare l’editor schema visivo per:

* Individuare le colonne e le chiavi primarie dalle tabelle
* Creare etichette intuitive per tali tabelle
* Creare etichette intuitive per ogni colonna
* Nascondere colonne non necessarie
* Salvare la descrizione di tali tabelle
+++

+++Esiste un’archiviazione temporanea nella composizione di pubblico federato?

No, la composizione di pubblico federato archivia solo i metadati (descrizioni dello schema). Nessun dato cliente è in fase di transizione. <!--The Audience export flow is done directly from Adobe Experience Platform Audience Portal (via [Destination](../connections/destinations.md)) to the customer database. The creation and update flow is done directly from your data warehouse database to Adobe Experience Platform Audience Portal.-->

+++

+++La composizione di pubblico federato memorizza una copia fisica dell’elenco di persone da inviare ai sistemi a valle?

La composizione di pubblico federato non conserva una copia fisica dei dati. La frequenza è configurata nella composizione per definire quanto spesso verranno aggiornati i dati. I dati del pubblico risultanti non vengono memorizzati da Adobe Experience Platform più a lungo di quanto richiesto dai casi d’uso o dalle azioni del cliente.

Ad esempio:

* Per la creazione del pubblico, il pubblico viene creato nel data warehouse, quindi puoi utilizzare la composizione di pubblico federato per ulteriori attività di composizione e manipolazione dei dati prima di pubblicare il pubblico risultante e gli attributi associati tramite Adobe Experience Platform Audience Portal. La definizione del pubblico e gli attributi associati vengono trasmessi ad Adobe Experience Platform.
Tieni presente che la scadenza corrente dei dati per i tipi di pubblico generati esternamente è di 30 giorni. Questa scadenza riduce la quantità di dati in eccesso archiviati all’interno di un’organizzazione. Al termine del periodo di scadenza dei dati, il set di dati associato rimane visibile all’interno dell’inventario dei set di dati, ma non è possibile attivare il pubblico e il conteggio dei profili viene visualizzato come zero. Ulteriori informazioni sono disponibili nella [documentazione di Adobe Experience Platform](https://experienceleague.adobe.com/it/docs/experience-platform/segmentation/faq#how-long-do-externally-generated-audiences-last-for){target="_blank"}.

* In caso di un Arricchimento pubblico, il punto di partenza è un pubblico Adobe Experience Platform esistente. Ecco due scenari da esaminare:
   1. Acquisire attributi aggiuntivi del payload del pubblico dal data warehouse federato: in questo caso, gli attributi aggiuntivi aggiunti verranno visualizzati come parte della definizione del pubblico. La scadenza dei dati per i tipi di pubblico generati esternamente è la stessa, ovvero 30 giorni.
   1. Perfeziona il pubblico di Adobe Experience Platform esistente in base agli attributi aggiuntivi presenti nel data warehouse. <!--For example, you have an audience of customers who have shown interest in a particular product on the website for the last two months. You now want to take this audience and further segment it using Federated Audience Composition to only include customers who have a high credit score. The credit score is deemed sensitive and individual credit score data points are not copied over from the data warehouse.-->
+++

+++Se i dati dei pattern di casi d’uso per la creazione del pubblico e l’arricchimento del pubblico non vengono mantenuti, come vengono memorizzati temporaneamente?

I dati del pubblico risultanti non persistono a tempo indefinito in Adobe Experience Platform o nella composizione di pubblico federato. Non verranno conservati più a lungo di quanto richiesto dal tuo caso d’uso. Gli attributi del pubblico portati come parte del payload del pubblico persisteranno solo come parte della definizione del pubblico. La durata della persistenza si basa sul TTL per qualsiasi pubblico; il valore predefinito è 30 giorni.

+++

+++È possibile eliminare un pubblico caricato personalizzato?

No, nella versione corrente non è possibile eliminare i tipi di pubblico personalizzati caricati.

+++

+++Se vengono combinati dati provenienti da più origini, in che modo vengono uniti? Utilizzando Identity Service?

No, Identity service non viene utilizzato durante una composizione. I dati tra le varie origini utilizzate nella composizione vengono uniti tramite logica definita dall’utente (come espressa nel modello sottostante), ad esempio ID CRM, numero account utente, ecc. È necessario selezionare l’identità utilizzata come identificatore nel pubblico per la selezione nel data warehouse. In un pubblico risultante dalla composizione di pubblico federato, è necessario identificare lo spazio dei nomi identità per l’identità nel set di dati risultante.

+++

+++In che modo le preferenze di consenso del cliente vengono rispettate per i tipi di pubblico generati esternamente e importati in Federated Audience Composition?

Poiché i dati del cliente vengono acquisiti da più canali, i criteri di unione e unione delle identità consentono di consolidarli in un unico profilo cliente in tempo reale. Le informazioni sulle preferenze di consenso dei clienti vengono memorizzate e valutate a livello di profilo.

Le destinazioni a valle di Real-Time CDP e Journey Optimizer controllano ogni profilo per individuare le preferenze di consenso prima dell’attivazione. Le informazioni sul consenso di ciascun profilo vengono confrontate con i requisiti del consenso per una particolare destinazione. Se il profilo non soddisfa i requisiti, non viene inviato a una destinazione.

Quando un pubblico esterno viene acquisito in Federated Audience Composition, viene riconciliato con i profili esistenti utilizzando un ID primario come e-mail o ECID. Di conseguenza, i criteri di consenso esistenti rimarranno in vigore per tutta la durata dell’attivazione.

>[!NOTE]
>
>Poiché le variabili di payload non sono memorizzate nel profilo, ma nel data lake, non devi includere le informazioni sul consenso nei tipi di pubblico generati esternamente. Utilizza invece altri canali di acquisizione Adobe Experience Platform in cui vengono importati i dati del profilo.

+++