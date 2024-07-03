---
audience: end-user
title: Creare composizioni
description: Scopri come creare le composizioni
source-git-commit: b946f8821d965fb00f79f6f5557adcfff1ee2387
workflow-type: tm+mt
source-wordcount: '561'
ht-degree: 47%

---


# Avviare e monitorare la composizione {#start-monitor}

Dopo aver creato la composizione e progettato le attività da eseguire nell’area di lavoro, puoi avviarla e monitorarne l’esecuzione.

## Avvia la composizione {#start}

Per avviare la composizione, passate alla **[!UICONTROL Composizioni]** o la campagna associata e fai clic sul pulsante **[!UICONTROL Inizio]** nell’angolo superiore destro dell’area di lavoro.

Una volta eseguita la composizione, ogni attività nell’area di lavoro viene eseguita in ordine sequenziale, fino al raggiungimento della fine della composizione.

Puoi monitorare l’avanzamento dei profili target in tempo reale utilizzando un flusso visivo. Questo consente di identificare rapidamente lo stato di ciascuna attività e il numero di profili che passano da un’attività all’altra.

## Transizioni composizione {#transitions}

Nelle composizioni, i dati trasportati da un’attività all’altra tramite transizioni vengono memorizzati in una tabella di lavoro temporanea. Questi dati possono essere visualizzati per ogni transizione. A questo scopo, seleziona una transizione per aprirne le proprietà sul lato destro dello schermo.

* Fai clic su **[!UICONTROL Anteprima schema]** per visualizzare lo schema della tabella di lavoro.
* Fai clic su **[!UICONTROL Anteprima risultati]** per visualizzare i dati trasportati nella transizione selezionata.

## Monitorare l’esecuzione dell’attività {#activities}

Gli indicatori visivi nell’angolo superiore a destra di ciascuna casella di attività ti consentono di controllarne l’esecuzione:

| Indicatore visivo | Descrizione |
|-----|------------|
|  | L’attività è attualmente in esecuzione. |
|  | L’attività richiede la tua attenzione. Ciò potrebbe implicare la conferma dell’invio di una consegna o l’adozione di un’azione necessaria. |
|  | L’attività ha rilevato un errore. Per risolvere il problema, apri i registri della composizione per ulteriori informazioni. |
|  | L’attività è stata eseguita correttamente. |

## Monitorare i registri e le attività {#logs-tasks}

Monitorare i registri e le attività di composizione è un passaggio chiave per analizzare le composizioni e assicurarti che vengano eseguite correttamente. Sono accessibili dall’icona **[!UICONTROL Registri]** disponibile nella barra degli strumenti delle azioni e nel riquadro delle proprietà di ogni attività.

Il **[!UICONTROL Registri e attività]** fornisce una cronologia dell’esecuzione della composizione, registrando tutte le azioni dell’utente e gli errori riscontrati. Questa cronologia viene salvata per la durata specificata nella composizione [opzioni di esecuzione](composition-settings.md). Durante questo periodo, tutti i messaggi vengono salvati, anche dopo un riavvio della composizione. Se non desideri salvare i messaggi di un’esecuzione precedente, fai clic sul pulsante **[!UICONTROL Elimina cronologia]**.

Sono disponibili due tipi di informazioni:

* Il **[!UICONTROL Log]** contiene la cronologia di esecuzione di tutte le attività di composizione. Questi registri indicizzano in ordine cronologico le operazioni effettuate e gli errori di esecuzione.
* Nella scheda **[!UICONTROL Attività]** viene illustrata la sequenza di esecuzione delle attività.

In entrambe le schede, puoi scegliere le colonne visualizzate e il loro ordine, applicare filtri e utilizzare il campo di ricerca per trovare rapidamente le informazioni desiderate.

## Comandi esecuzione composizione {#execution-commands}

La barra delle azioni nell&#39;angolo superiore destro fornisce i comandi che consentono di gestire l&#39;esecuzione della composizione. Puoi eseguire le seguenti operazioni:

* **[!UICONTROL Inizio]** / **[!UICONTROL Riprendi]** l’esecuzione della composizione, che assume quindi lo stato In corso. Se la composizione è stata sospesa, viene ripresa, altrimenti viene avviata e le attività iniziali vengono quindi attivate.

* **[!UICONTROL Pausa]** l’esecuzione della composizione, che assume quindi lo stato In pausa. Non verranno attivate nuove attività finché non viene ripresa, ma le operazioni in corso non vengono sospese.

* **[!UICONTROL Interrompi]** una composizione in esecuzione che assumerà lo stato Finished. Se possibile, le operazioni in corso vengono interrotte. Non è possibile riprendere la composizione dalla stessa posizione in cui è stata interrotta.
