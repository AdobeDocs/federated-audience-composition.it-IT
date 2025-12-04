---
audience: end-user
title: Creare composizioni
description: Scopri come creare le composizioni
exl-id: 1f288312-dd6a-4a62-8ee6-fa2417954d5c
source-git-commit: e0bf1f76f7f781fb6fcc3b44898ba805d87a25c9
workflow-type: tm+mt
source-wordcount: '738'
ht-degree: 24%

---

# Avviare e monitorare la composizione {#start-monitor}

Dopo aver creato la composizione e progettato le attività da eseguire nell’area di lavoro, puoi avviarla e monitorarne l’esecuzione.

## Avvia la composizione {#start}

Per avviare una composizione, fare clic sul pulsante **[!UICONTROL Avvia]** nell&#39;angolo superiore destro dello schermo. Quando la composizione è in esecuzione, ogni attività nell’area di lavoro viene eseguita in ordine sequenziale, fino al raggiungimento della fine della composizione.

Puoi monitorare l’avanzamento dei profili target in tempo reale utilizzando un flusso visivo. Questo consente di identificare rapidamente lo stato di ciascuna attività e il numero di profili che passano da un’attività all’altra.

![](assets/composition-visual-flow.png)

## Transizioni composizione {#transitions}

Nelle composizioni, i dati trasportati da un’attività all’altra tramite transizioni vengono memorizzati in una tabella di lavoro temporanea. Questi dati possono essere visualizzati per ogni transizione. A questo scopo, seleziona una transizione per aprirne le proprietà sul lato destro dello schermo.

* Fai clic su **[!UICONTROL Anteprima schema]** per visualizzare lo schema della tabella di lavoro.
* Fai clic su **[!UICONTROL Anteprima risultati]** per visualizzare i dati trasportati nella transizione selezionata. Questa opzione è disponibile solo se è abilitata l&#39;opzione **[!UICONTROL Mantieni il risultato delle popolazioni provvisorie tra due esecuzioni]**. [Ulteriori informazioni](create-composition.md#settings).

![](assets/transition-preview.png)

## Monitorare l’esecuzione dell’attività {#activities}

Gli indicatori visivi nell’angolo superiore a destra di ciascuna casella di attività ti consentono di controllarne l’esecuzione:

| Indicatore visivo | Descrizione |
|-----|------------|
| ![](assets/activity-status-pending.png){zoomable="yes"}{width="70%"} | L’attività è attualmente in esecuzione. |
| ![](assets/activity-status-orange.png){zoomable="yes"}{width="70%"} | L’attività richiede la tua attenzione. Ciò potrebbe implicare la conferma dell’invio di una consegna o l’adozione di un’azione necessaria. |
| ![](assets/activity-status-red.png){zoomable="yes"}{width="70%"} | L’attività ha rilevato un errore. Per risolvere il problema, apri i registri della composizione per ulteriori informazioni. |
| ![](assets/activity-status-green.png){zoomable="yes"}{width="70%"} | L’attività è stata eseguita correttamente. |

## Monitorare i registri e le attività {#logs-tasks}

Monitorare i registri e le attività di composizione è un passaggio chiave per analizzare le composizioni e assicurarti che vengano eseguite correttamente. Sono accessibili dal pulsante **[!UICONTROL Registri]** disponibile nella barra degli strumenti delle azioni e nel riquadro delle proprietà di ogni attività.

![](assets/logs-button.png)

La schermata **[!UICONTROL Registri di composizione e attività]** fornisce una cronologia dell&#39;esecuzione della composizione, registrando tutte le azioni dell&#39;utente e gli errori riscontrati.

<!-- à confirmer, pas trouvé dans les options = The workflow history is saved for the duration specified in the workflow execution options. During this duration, all the messages are therefore saved, even after a restart. If you do not want to save the messages from a previous execution, you have to purge the history by clicking the ![](assets/delete_darkgrey-24px.png) button.-->

La cronologia è organizzata in diverse schede, descritte di seguito:

* La scheda **[!UICONTROL Registro]** contiene la cronologia di esecuzione di tutte le attività di composizione. Questi registri indicizzano in ordine cronologico le operazioni effettuate e gli errori di esecuzione.
* La scheda **[!UICONTROL Attività]** descrive la sequenza di esecuzione delle attività. Il pulsante che si trova alla fine di ogni attività ti consente di elencare le variabili evento passate attraverso l’attività.
* Nella scheda **[!UICONTROL Variabili]** sono elencate tutte le variabili passate nella composizione. È disponibile quando si accede ai registri e alle attività solo dall’area di lavoro della composizione. È ora disponibile quando accedi ai registri dal riquadro delle proprietà di un’attività.  <!-- à confirmer-->

![](assets/logs-tasks.png)

In tutte le schede è possibile scegliere le colonne visualizzate e il relativo ordine, applicare filtri e utilizzare il campo di ricerca per trovare rapidamente le informazioni desiderate.

## Iscriversi agli avvisi {#alerts}

Inoltre, puoi abbonarti agli avvisi per ricevere notifiche se le esecuzioni della composizione federata hanno avuto esito positivo o negativo.

Per iscriverti agli avvisi, seleziona l&#39;icona ![notifica](/help/assets/icons/bell.png), seguita dall&#39;icona ![impostazioni](/help/assets/icons/settings.png).

![Sono evidenziate sia le icone di notifica che le icone delle impostazioni.](assets/monitor/select-notifications.png){zoomable="yes"}{width="70%"}

Viene visualizzata la pagina delle impostazioni delle notifiche. In questa pagina, selezionare **[!UICONTROL Experience Platform]** e scegliere i canali di avvisi desiderati. Per visualizzare le notifiche nell&#39;interfaccia utente, selezionare **[!UICONTROL In-app]**.

![La casella di controllo In-app è selezionata nella sezione Experience Platform.](assets/monitor/add-alerts.png){zoomable="yes"}{width="50%"}

Selezionando **[!UICONTROL In-app]**, riceverai una notifica relativa ai successi e agli errori di esecuzione della composizione.

![Vengono visualizzati gli avvisi che mostrano gli errori e i successi della composizione.](assets/monitor/view-alerts.png){zoomable="yes"}{width="70%"}

## Comandi esecuzione composizione {#execution-commands}

La barra delle azioni nell&#39;angolo superiore destro fornisce i comandi che consentono di gestire l&#39;esecuzione della composizione.

![](assets/execution-actions.png)

Le azioni disponibili sono:

* **[!UICONTROL Inizio]**: avvia l&#39;esecuzione della composizione, che assume lo stato **[!UICONTROL In corso]**. La composizione viene avviata e le attività iniziali vengono attivate.

* **[!UICONTROL Riprendi]**: riprende l&#39;esecuzione della composizione messa in pausa. La composizione assume lo stato **[!UICONTROL In corso]**.

* **[!UICONTROL Sospendi]** l&#39;esecuzione della composizione, che assume quindi lo stato **[!UICONTROL In pausa]**. Non verranno attivate nuove attività finché non viene ripresa, ma le operazioni in corso non vengono sospese.

* **[!UICONTROL Interrompi]** una composizione in esecuzione, che assumerà lo stato **[!UICONTROL Completato]**. Se possibile, le operazioni in corso vengono interrotte. Non è possibile riprendere la composizione dalla stessa posizione in cui è stata interrotta.

* **[!UICONTROL Riavvia]**: interrompe e riavvia una composizione. Nella maggior parte dei casi, questo consente di riavviare più rapidamente, poiché l&#39;arresto richiede un certo periodo di tempo e il pulsante **[!UICONTROL Avvia]** è disponibile solo quando l&#39;interruzione è effettiva.

