---
audience: end-user
title: Creare composizioni
description: Scopri come creare le composizioni
exl-id: 4f510805-b700-444d-89bb-832eaa1e3242
source-git-commit: 036dcb96d2d831e3a1d6ab50afef5b87e25b564b
workflow-type: tm+mt
source-wordcount: '1596'
ht-degree: 21%

---

# Creare una composizione

La funzione Composizione di pubblico federato consente di creare composizioni, sfruttando varie attività in un’area di lavoro visiva per creare tipi di pubblico. Dopo aver creato la composizione, i tipi di pubblico risultanti vengono salvati in Adobe Experience Platform e possono essere sfruttati nelle destinazioni di Experience Platform e Adobe Journey Optimizer per il targeting della clientela.

## Definire la composizione {#create}

>[!CONTEXTUALHELP]
>id="dc_composition_creation_properties"
>title="Proprietà della composizione"
>abstract="In questa schermata, scegli il modello da utilizzare per creare la composizione e specifica un’etichetta. Espandi la sezione OPZIONI AGGIUNTIVE per configurare altre impostazioni quali il nome interno della composizione, la relativa cartella, il fuso orario e il gruppo di supervisori. Si consiglia vivamente di selezionare un gruppo di supervisori in modo che gli operatori vengano avvisati in caso di errore."

Per creare una composizione, dovete prima definirne l&#39;etichetta e, facoltativamente, configurare ulteriori impostazioni.

Per creare una composizione, seleziona **[!UICONTROL Tipi di pubblico]** nella sezione **[!UICONTROL Cliente]**, seguito dalla scheda **[!UICONTROL Composizioni federate]**.

![Il percorso per accedere alla sezione Composizioni federate è evidenziato.](assets/create/access-compositions.png)

Viene visualizzata la pagina Sfoglia composizioni federate. Selezionare **[!UICONTROL Crea composizione]** per continuare con il processo di creazione della composizione.

![](assets/composition-create.png)

Nella sezione **[!UICONTROL Proprietà]**, specifica un&#39;etichetta per la composizione e seleziona un modello dati. Solo gli schemi associati a questo modello dati saranno disponibili nelle attività della composizione.

![](assets/composition-select-schema.png)

Seleziona **[!UICONTROL Crea]**. Viene visualizzata l’area di lavoro della composizione. Ora puoi configurare la composizione aggiungendo attività e transizioni all’area di lavoro.

## Area di lavoro composizione {#canvas}

Nella parte superiore dell’area di lavoro, puoi accedere a una barra degli strumenti che fornisce opzioni per gestire e navigare tra le attività.

![](assets/canvas-toolbar.png)

Le opzioni disponibili includono:

* **[!UICONTROL Selezione multipla]**: selezionare più attività per eliminarle tutte contemporaneamente oppure copiarle e incollarle.
* **[!UICONTROL Ruota]**: cambia l&#39;area di lavoro per visualizzarla verticalmente.
* **[!UICONTROL Adatta allo schermo]**: regola il livello di zoom dell&#39;area di lavoro sullo schermo.
* **[!UICONTROL Zoom avanti]** / **[!UICONTROL Zoom indietro]**: ingrandire o ridurre l&#39;area di lavoro.
* **[!UICONTROL Mappa di visualizzazione]**: apre uno snapshot dell&#39;area di lavoro che mostra che ci si trova.

## Aggiungere attività {#add-activities}

Nell’area di lavoro della composizione puoi aggiungere attività e transizioni per definire meglio il pubblico. Le attività ti consentono di *definire* i componenti all&#39;interno del pubblico, mentre le transizioni ti consentono di *organizzare* il flusso della composizione.

Per ulteriori informazioni sulle attività e sulle transizioni disponibili per l&#39;utilizzo, leggere la [panoramica delle attività](./activities.md).

## Gestire le attività {#manage-activities}

Puoi eseguire operazioni sulle attività aggiunte nel riquadro delle proprietà.

![](assets/activity-actions.png)

Le opzioni includono:

* **[!UICONTROL Elimina]**: elimina l&#39;attività dall&#39;area di lavoro.
* **[!UICONTROL Disabilita]/[!UICONTROL Abilita]**: disabilita o abilita l&#39;attività. Quando la composizione viene eseguita, le attività disabilitate e le attività seguenti sullo stesso percorso non vengono eseguite e la composizione viene interrotta.
* **[!UICONTROL Pausa]/[!UICONTROL Riprendi]**: sospendi o riprendi l&#39;attività. Quando la composizione viene eseguita, viene messa in pausa in corrispondenza dell’attività in pausa. L’attività corrispondente e tutte quelle che la seguono nello stesso percorso non vengono eseguite.
* **[!UICONTROL Copia]**: copia l&#39;attività per incollarla in un&#39;altra posizione nella composizione. A tale scopo, selezionare il pulsante **+** in una transizione e selezionare **[!UICONTROL Incolla attività X]**. <!-- cannot copy multiple activities ? cannot paste in another composition?-->
* Configura **[!UICONTROL Opzioni di esecuzione]** per l&#39;attività selezionata. Le opzioni di esecuzione disponibili includono:
  +++Opzioni di esecuzione disponibili

  La sezione **[!UICONTROL Proprietà]** consente di configurare le impostazioni generiche relative all&#39;esecuzione dell&#39;attività:

   * **[!UICONTROL Esecuzione]**: definisci l&#39;azione da eseguire all&#39;avvio dell&#39;esecuzione.
   * **[!UICONTROL Durata massima esecuzione]**: specificare una durata, ad esempio &quot;30s&quot; o &quot;1h&quot;. Se l’attività non viene completata dopo la scadenza della durata specificata, viene attivato un avviso. Questo non ha alcun impatto sul funzionamento della composizione.
   * **[!UICONTROL Fuso orario]**: selezionare il fuso orario dell&#39;attività. La Federated Audience Composition consente di gestire le differenze di tempo tra più paesi nella stessa istanza. L’impostazione applicata viene configurata al momento della creazione dell’istanza.
   * **[!UICONTROL Affinità]**: forza l&#39;esecuzione dell&#39;attività di composizione su un computer specifico. A questo scopo, devi specificare una o più affinità per l’attività in questione.
   * **[!UICONTROL Comportamento]**: definire la procedura da seguire se vengono utilizzate attività asincrone.

  La sezione **[!UICONTROL Gestione degli errori]** consente di specificare l&#39;azione da eseguire in caso di errore dell&#39;attività.

  La sezione **[!UICONTROL Script di inizializzazione]** consente di inizializzare le variabili o modificare le proprietà dell&#39;attività. Selezionare il pulsante **[!UICONTROL Modifica codice]** e digitare il frammento di codice da eseguire. Lo script viene chiamato durante l’esecuzione dell’attività.

  +++
* **Registri e attività**: visualizza i registri e le attività per l&#39;attività selezionata.

## Avviare e monitorare la composizione {#start-and-monitor}

Dopo aver completato l’aggiunta delle attività alla composizione, puoi avviare l’esecuzione della composizione. Per avviare una composizione, selezionare il pulsante **[!UICONTROL Avvia]** nell&#39;angolo superiore destro dello schermo.

![](assets/execution-actions.png)

| Azione | Descrizione |
| ------ | ----------- |
| **Inizio** | Avvia l&#39;esecuzione della composizione e la sposta nello stato **In corso**. |
| **Pausa** | Sospende l&#39;esecuzione della composizione e la imposta sullo stato **In pausa**. Non verranno attivate nuove attività finché la composizione non verrà ripresa, ma le operazioni in corso sono **non** sospese. |
| **Riprendi** | Riprende l&#39;esecuzione della composizione in pausa e la imposta sullo stato **In corso**. |
| **Interrompi** | Interrompe l&#39;esecuzione della composizione e la imposta sullo stato **Finished**. **Impossibile** riprendere la composizione dalla stessa posizione da cui è stata interrotta. |
| **Riavvia** | Arresta e riavvia l&#39;esecuzione della composizione. |

Quando la composizione è in esecuzione, ogni attività nell’area di lavoro viene eseguita in ordine sequenziale, fino al raggiungimento della fine della composizione. Puoi monitorare l’avanzamento dei profili target in tempo reale utilizzando un flusso visivo. Questo consente di identificare rapidamente lo stato di ciascuna attività e il numero di profili che passano da un’attività all’altra.

![](assets/composition-visual-flow.png)

Gli indicatori visivi nell’angolo in alto a destra di ciascuna attività mostrano lo stato dell’esecuzione:

| Indicatore visivo | Descrizione |
| ---------------- | ------------|
| ![](assets/activity-status-pending.png){zoomable="yes"}{width="70%"} | L’attività è attualmente in esecuzione. |
| ![](assets/activity-status-orange.png){zoomable="yes"}{width="70%"} | L’attività richiede la tua attenzione. Ciò potrebbe implicare la conferma dell’invio di una consegna o l’adozione di un’azione necessaria. |
| ![](assets/activity-status-red.png){zoomable="yes"}{width="70%"} | L’attività ha rilevato un errore. Per risolvere il problema, apri i registri della composizione per ulteriori informazioni. |
| ![](assets/activity-status-green.png){zoomable="yes"}{width="70%"} | L&#39;attività è stata eseguita correttamente. |

### Monitorare i registri e le attività {#monitor-logs}

Inoltre, potete visualizzare i registri di composizione per verificarne il corretto funzionamento. Seleziona **[!UICONTROL Registri]** nella barra degli strumenti delle azioni per visualizzare queste informazioni.

![](assets/logs-button.png)

Viene visualizzata la schermata **[!UICONTROL Registri di composizione e attività]**. Fornisce una cronologia dell’esecuzione della composizione, registrando tutte le azioni dell’utente e gli errori riscontrati.

La cronologia è organizzata in diverse schede, descritte di seguito:

* La scheda **[!UICONTROL Registro]** contiene la cronologia di esecuzione di tutte le attività di composizione. Questi registri indicizzano in ordine cronologico le operazioni effettuate e gli errori di esecuzione.
* La scheda **[!UICONTROL Attività]** descrive la sequenza di esecuzione delle attività. Il pulsante che si trova alla fine di ogni attività ti consente di elencare le variabili evento passate attraverso l’attività.
* Nella scheda **[!UICONTROL Variabili]** sono elencate tutte le variabili passate nella composizione. È disponibile quando si accede ai registri e alle attività solo dall’area di lavoro della composizione. È ora disponibile quando accedi ai registri dal riquadro delle proprietà di un’attività.

![](assets/logs-tasks.png)

In tutte le schede è possibile scegliere le colonne visualizzate e il relativo ordine, applicare filtri e utilizzare il campo di ricerca per trovare rapidamente le informazioni desiderate.

### Iscriversi agli avvisi {#alerts}

È inoltre possibile sottoscrivere avvisi per ricevere notifiche se le esecuzioni della composizione federata hanno avuto esito positivo o negativo.

Per iscriverti agli avvisi, seleziona l&#39;icona ![notifica](/help/assets/icons/bell.png), seguita dall&#39;icona ![impostazioni](/help/assets/icons/settings.png).

![Sono evidenziate sia le icone di notifica che le icone delle impostazioni.](assets/monitor/select-notifications.png){zoomable="yes"}{width="70%"}

Viene visualizzata la pagina delle impostazioni delle notifiche. In questa pagina, selezionare **[!UICONTROL Experience Platform]** e scegliere i canali di avvisi desiderati. Per visualizzare le notifiche nell&#39;interfaccia utente, selezionare **[!UICONTROL In-app]**.

![La casella di controllo In-app è selezionata nella sezione Experience Platform.](assets/monitor/add-alerts.png){zoomable="yes"}{width="50%"}

Selezionando **[!UICONTROL In-app]**, riceverai una notifica relativa ai successi e agli errori di esecuzione della composizione.

![Vengono visualizzati gli avvisi che mostrano gli errori e i successi della composizione.](assets/monitor/view-alerts.png){zoomable="yes"}{width="70%"}

## Configurare le impostazioni della composizione {#settings}

>[!CONTEXTUALHELP]
>id="dc_composition_settings_properties"
>title="Proprietà della composizione"
>abstract="In questa sezione sono illustrate le proprietà generiche della composizione accessibili anche durante la relativa creazione."

>[!CONTEXTUALHELP]
>id="dc_composition_settings_segmentation"
>title="Segmentazione della composizione"
>abstract="Per impostazione predefinita, vengono mantenute solo le tabelle di lavoro dell’ultima esecuzione della composizione. È possibile abilitare questa opzione per mantenere tabelle di lavoro a scopo di test. Deve essere utilizzata **solo** in ambienti di sviluppo o di staging. Questa opzione non deve mai essere selezionata in un’ambiente di produzione."

>[!CONTEXTUALHELP]
>id="dc_composition_settings_error"
>title="Errore di impostazioni di gestione"
>abstract="In questa sezione puoi definire la gestione degli errori durante l’esecuzione. Puoi scegliere di sospendere il processo, ignorare un certo numero di errori o interrompere l’esecuzione della composizione."

Quando accedete a una composizione, potete accedere a impostazioni avanzate che consentono, ad esempio, di definire il comportamento della composizione in caso di errore.

Per accedere a queste opzioni aggiuntive, seleziona **[!UICONTROL Impostazioni]** nella sezione superiore della schermata di creazione della composizione.

![](assets/composition-create-settings.png)

| Impostazioni | Descrizione |
| -------- | ----------- |
| **[!UICONTROL Etichetta]** | Aggiornate il nome assegnato alla composizione. |
| **[!UICONTROL Mantieni il risultato delle popolazioni provvisorie tra due esecuzioni]** | Se questa opzione è attivata, le tabelle di lavoro verranno mantenute anche dopo l&#39;esecuzione della composizione. Per impostazione predefinita, vengono mantenute solo le tabelle di lavoro dell’ultima esecuzione della composizione. Le tabelle di lavoro delle esecuzioni precedenti vengono rimosse su base giornaliera. Abilitare questa impostazione solo in un ambiente di sviluppo o di staging. **non abilitare mai** questa impostazione in un ambiente di produzione. |
| **[!UICONTROL Gestione degli errori]** | Definisce le azioni intraprese in caso di errore nella composizione. Sono disponibili tre opzioni: <ul><li>**[!UICONTROL Sospendi il processo]**: la composizione viene automaticamente sospesa e il suo stato cambia in **[!UICONTROL Non riuscito]**. Una volta risolto il problema, riprendere la composizione utilizzando i pulsanti **[!UICONTROL Riprendi]**.</li><li>**[!UICONTROL Ignora]**: lo stato dell&#39;attività che ha attivato l&#39;errore diventa **[!UICONTROL Non riuscito]**, ma la composizione mantiene lo stato **[!UICONTROL Avviato]**.</li><li>**[!UICONTROL Interrompi il processo]**: la composizione viene interrotta automaticamente e il suo stato cambia in **[!UICONTROL Non riuscito]**. Una volta risolto il problema, riavviare la composizione utilizzando il pulsante **[!UICONTROL Avvia]**.</li></ul> |
| **[!UICONTROL Errori consecutivi]** | Specificare il numero di errori che possono essere ignorati prima dell&#39;interruzione del processo. Una volta raggiunto questo numero, lo stato della composizione diventa **[!UICONTROL Non riuscito]**. Se il valore di questo campo è 0, la composizione non verrà mai interrotta indipendentemente dal numero di errori. |
