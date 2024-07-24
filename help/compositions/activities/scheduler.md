---
audience: end-user
title: Utilizzare l’attività Scheduler
description: Scopri come utilizzare l’attività Scheduler
exl-id: 3e8be2a2-2227-42f4-a512-b9e686ba0f66
source-git-commit: 122bd469e04d72d2dac0f606c8ab4e195100d4a4
workflow-type: tm+mt
source-wordcount: '456'
ht-degree: 36%

---

# Modulo di pianificazione {#scheduler}

>[!CONTEXTUALHELP]
>id="dc_orchestration_scheduler"
>title="Attività del Modulo di pianificazione"
>abstract="L&#39;attività **Scheduler** consente di pianificare l&#39;avvio della composizione del pubblico. Dovresti considerare questa attività come un avvio pianificato. Può essere utilizzata solo come prima attività di una composizione."

L’attività del **Modulo di pianificazione** è un’attività di **Controllo del flusso**. Consente di pianificare l&#39;inizio della composizione. Dovresti considerare questa attività come un avvio pianificato. Può essere utilizzata solo come prima attività della composizione.

Se hai configurato una connessione alla destinazione Federated Data Composition, puoi utilizzare questa attività per inviare su pubblico Adobe Experience Platform a frequenze regolari. [Scopri come arricchire il pubblico di Adobe Experience Platform con dati esterni](../../connections/destinations.md)

![](../assets/scheduler.png)

## Configurare l’attività di pianificazione {#scheduler-configuration}

>[!CONTEXTUALHELP]
>id="dc_orchestration_schedule_validity"
>title="Validità del modulo di pianificazione"
>abstract="È possibile definire un periodo di validità per il modulo di pianificazione. Può essere permanente (impostazione predefinita) o valido fino a una data specifica."

>[!CONTEXTUALHELP]
>id="dc_orchestration_schedule_options"
>title="Opzioni del modulo di pianificazione"
>abstract="Definisci la frequenza del modulo di pianificazione. Può essere eseguito in un determinato momento, una o più volte al giorno, alla settimana o al mese."

Per configurare l’attività del **Modulo di pianificazione**, segui questi passaggi:

1. Aggiungi un&#39;attività **Scheduler** alla composizione.

1. Configura la **Frequenza di esecuzione**:

   * **Una volta**: la composizione viene eseguita una sola volta.
   * **Giornaliero**: la composizione viene eseguita a un&#39;ora specifica, una volta al giorno.
   * **Più volte al giorno:** la composizione viene eseguita regolarmente più volte al giorno. Puoi impostare esecuzioni in orari specifici o periodicamente.

     >[!NOTE]
     >
     >Non pianificare l&#39;esecuzione di una composizione per più di 15 minuti, poiché questa operazione potrebbe ostacolare le prestazioni complessive del sistema e creare blocchi nel database.

   * **Settimanale**: la composizione viene eseguita in un determinato momento, una o più volte alla settimana.
   * **Mensile**: la composizione viene eseguita in un determinato momento, una o più volte al mese. Potete selezionare i mesi, quando dovete eseguire la composizione. Puoi anche impostare le esecuzioni in un giorno feriale specifico del mese, ad esempio il secondo martedì del mese.

1. Definisci i dettagli di esecuzione in base alla frequenza selezionata. I campi dettagliati possono variare a seconda della frequenza utilizzata (tempo, frequenza di ripetizione, giorni specificati, ecc.).

1. Fai clic su **Anteprima ora di lancio** per controllare la pianificazione delle prossime dieci esecuzioni della composizione.

1. Definisci il periodo di validità del modulo di pianificazione:

   * **Permanente (non scade mai)**: la composizione viene eseguita, in base alla frequenza specificata, senza alcun limite all&#39;intervallo di tempo o al numero di iterazioni.

   * **Periodo di validità**: la composizione viene eseguita in base alla frequenza specificata, fino a una data specifica. È necessario specificare le date di inizio e di fine.

>[!NOTE]
>
>Se si desidera avviare subito la composizione, è possibile fare clic sull&#39;**Attività in sospeso** nella barra delle azioni superiore della pianificazione. Questo pulsante è disponibile solo dopo aver avviato la composizione.

<!--## Example{#scheduler-example}

In the following example, the activity is configured so that the composition runs several times a day at 9 and 12 AM, every day of the week from October 1st, 2023 to January 1st, 2024.-->
