---
audience: end-user
title: Utilizzare l’attività Scheduler
description: Scopri come utilizzare l’attività Scheduler
source-git-commit: 4dca96ae81d1f70c8f20509fdbd9ec31e05c01dc
workflow-type: tm+mt
source-wordcount: '417'
ht-degree: 47%

---


# Modulo di pianificazione {#scheduler}

>[!CONTEXTUALHELP]
>id="dc_orchestration_scheduler"
>title="Attività del Modulo di pianificazione"
>abstract="L’attività del **Modulo di pianificazione** consente di pianificare quando viene avviato il flusso di lavoro. Dovresti considerare questa attività come un avvio pianificato. Può essere utilizzata solo come prima attività del flusso di lavoro."

L’attività del **Modulo di pianificazione** è un’attività di **Controllo del flusso**. Consente di pianificare l&#39;inizio della composizione. Dovresti considerare questa attività come un avvio pianificato. Può essere utilizzata solo come prima attività della composizione.

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

1. Aggiungi un’attività del **Modulo di pianificazione** al flusso di lavoro.

1. Configura la **Frequenza di esecuzione**:

   * **Una volta**: la composizione viene eseguita una sola volta.

   * **Giornaliero**: la composizione viene eseguita una volta al giorno a un’ora specifica.

   * **Più volte al giorno:** la composizione viene eseguita regolarmente diverse volte al giorno. Puoi impostare esecuzioni in orari specifici o periodicamente.

     >[!NOTE]
     >
     >Non pianificare l&#39;esecuzione di una composizione per più di 15 minuti, poiché questa operazione potrebbe ostacolare le prestazioni complessive del sistema e creare blocchi nel database.

   * **Ogni settimana**: la composizione viene eseguita in un determinato momento, una o più volte alla settimana.

   * **Mensile**: la composizione viene eseguita in un determinato momento, una o più volte al mese. Potete selezionare i mesi, quando dovete eseguire la composizione. Puoi anche impostare le esecuzioni in un giorno feriale specifico del mese, ad esempio il secondo martedì del mese.

1. Definisci i dettagli di esecuzione in base alla frequenza selezionata. I campi dettagliati possono variare a seconda della frequenza utilizzata (tempo, frequenza di ripetizione, giorni specificati, ecc.).

1. Clic **Anteprima orari di avvio** per controllare la pianificazione delle dieci esecuzioni successive della composizione.

1. Definisci il periodo di validità del modulo di pianificazione:

   * **Permanente (non scade mai)**: la composizione viene eseguita, in base alla frequenza specificata, senza alcun limite all’intervallo di tempo o al numero di iterazioni.

   * **Periodo di validità**: la composizione viene eseguita in base alla frequenza specificata, fino a una data specifica. È necessario specificare le date di inizio e di fine.

>[!NOTE]
>
>Se desiderate iniziare subito la composizione, potete fare clic sul pulsante **Esegui attività in sospeso** nella barra delle azioni superiore dell&#39;utilità di pianificazione. Questo pulsante è disponibile solo dopo aver avviato la composizione.

<!--## Example{#scheduler-example}

In the following example, the activity is configured so that the composition runs several times a day at 9 and 12 AM, every day of the week from October 1st, 2023 to January 1st, 2024.-->

