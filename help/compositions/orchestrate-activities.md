---
audience: end-user
title: Creare composizioni
description: Scopri come creare le composizioni
source-git-commit: fd92c280094989cb64ff5151fb00b4a8b0e650f7
workflow-type: tm+mt
source-wordcount: '1034'
ht-degree: 34%

---


# Orchestrare le attività di composizione {#activities}

Dopo aver creato una composizione, puoi iniziare a orchestrare le diverse attività che eseguirà. A questo scopo, viene fornita un’area di lavoro visiva che consente di creare il diagramma di composizione. All’interno di questo diagramma, puoi aggiungere varie attività e collegarle in ordine sequenziale.

## Aggiungere attività {#add}

In questa fase della configurazione, il diagramma viene visualizzato con un’icona di avvio che rappresenta l’inizio del flusso di lavoro. Per aggiungere la prima attività, fai clic su **+** all&#39;icona di avvio.

Viene visualizzato un elenco di attività che possono essere aggiunte al diagramma. Le attività disponibili dipendono dalla posizione all’interno del diagramma di composizione. Ad esempio, quando aggiungi la prima attività, puoi iniziare la composizione eseguendo il targeting di un pubblico, suddividendo il percorso del flusso di lavoro o impostando un **Wait** per ritardare l’esecuzione del flusso di lavoro. D&#39;altra parte, dopo un **Creare un pubblico** attività, puoi perfezionare il target con le attività di targeting, inviare una consegna al pubblico con le attività di canale o organizzare il processo di composizione con le attività di controllo del flusso.

Una volta aggiunta un’attività al diagramma, viene visualizzato un riquadro a destra che consente di configurare l’attività appena aggiunta con impostazioni specifiche. Informazioni dettagliate su come configurare ogni attività sono disponibili in [questa sezione](activities/about-activities.md).

Ripetete questo processo per aggiungere tutte le attività desiderate, a seconda delle attività che desiderate eseguire nella composizione. Puoi anche inserire una nuova attività tra due attività. A questo scopo, fai clic su **+** sulla transizione tra le attività, seleziona l’attività desiderata e configurala nel riquadro a destra.

Per rimuovere un’attività, selezionala nell’area di lavoro e fai clic su **Elimina** nelle proprietà dell’attività.

>[!TIP]
>
>Hai la possibilità di personalizzare il nome delle transizioni tra ciascuna attività. A questo scopo, seleziona la transizione e modifica la relativa etichetta nel riquadro a destra.

## Barra degli strumenti {#toolbar}

La barra degli strumenti situata nell’angolo superiore destro dell’area di lavoro offre opzioni per manipolare facilmente le attività e navigare nell’area di lavoro:

* **Modalità di selezione multipla**: seleziona più attività per eliminarle tutte contemporaneamente o copiarle e incollarle. Consulta [questa sezione](#copy).
* **Ruota**: cambia l’area di lavoro verticalmente.
* **Adatta allo schermo**: adatta il livello di zoom dell’area di lavoro allo schermo.
* **Zoom indietro** / **Zoom in**: zoom indietro o nell’area di lavoro.
* **Visualizza mappa**: apre un’istantanea dell’area di lavoro che mostra la tua posizione.


## Gestire le attività {#manage}

Quando si aggiungono attività, nel riquadro delle proprietà sono disponibili pulsanti di azione che consentono di eseguire più operazioni. Puoi eseguire le seguenti operazioni:

* **Elimina** l’attività dall’area di lavoro.
* **Disattiva/Attiva** l’attività. Quando il flusso di lavoro viene eseguito, le attività disabilitate e le attività successive sullo stesso percorso non vengono eseguite e il flusso di lavoro viene interrotto.
* **Copia** l’attività. Consulta [questa sezione](#copy).
* Accedi a **Registri e attività**.
* **Pausa/Riprendi** l’attività. Quando il flusso di lavoro viene eseguito, viene messo in pausa in corrispondenza dell’attività in pausa. L’attività corrispondente e tutte quelle che la seguono nello stesso percorso non vengono eseguite.

Diversi **Targeting** attività, come **Combina** o **Deduplicazione**, ti consente di elaborare la popolazione rimanente e di includerla in un’ulteriore transizione in uscita. Ad esempio, se utilizzi un’ **Dividi** attività, il complemento è costituito dalla popolazione che non corrisponde a nessuno dei sottoinsiemi precedentemente definiti. Per utilizzare questa funzionalità, attiva **Genera complemento** opzione.

## Copiare attività {#copy}

Puoi copiare le attività del flusso di lavoro e incollarle in qualsiasi flusso di lavoro. Il flusso di lavoro di destinazione può trovarsi in una scheda del browser diversa.

Per copiare le attività, puoi scegliere tra due opzioni:

* copia un’attività utilizzando il pulsante azione.

* copia più attività tramite il pulsante della barra degli strumenti.

Per incollare le attività copiate, fai clic su **+** su una transizione e selezionare &quot;Paste X activity&quot; (Incolla attività X).

## Execution options {#execution}

Tutte le attività ti consentono di gestire le relative opzioni di esecuzione. Seleziona un’attività e fai clic su **Opzioni di esecuzione** pulsante. Questo ti consente di definire la modalità di esecuzione dell’attività e il comportamento in caso di errori.

### Proprietà

Il **Esecuzione** consente di definire l&#39;azione da eseguire all&#39;avvio dell&#39;attività.

Il **Durata massima dell’esecuzione** consente di specificare una durata, ad esempio &quot;30s&quot; o &quot;1h&quot;. Se l’attività non viene completata dopo la scadenza della durata specificata, viene attivato un avviso. Questo non ha alcun impatto sul funzionamento del flusso di lavoro.

Il **Fuso orario** consente di selezionare il fuso orario dell’attività. Adobe Campaign consente di gestire le differenze di tempo tra più paesi nella stessa istanza. L’impostazione applicata viene configurata al momento della creazione dell’istanza.

**Affinità** consente di forzare l’esecuzione di un flusso di lavoro o di un’attività del flusso di lavoro su un determinato computer. A questo scopo, devi specificare una o più affinità per il flusso di lavoro o l’attività in questione.

Il **Comportamento** consente di definire la procedura da seguire se vengono utilizzate attività asincrone.

### Gestione degli errori

Il **In caso di errore** consente di specificare l’azione da eseguire in caso di errore dell’attività.

### Script di inizializzazione

Il **Script di inizializzazione** consente di inizializzare le variabili o modificare le proprietà dell’attività. Fai clic su **Modifica codice** e digitare il frammento di codice da eseguire. Lo script viene chiamato durante l’esecuzione dell’attività.

## Esempio {#example}

Di seguito è riportato un esempio di flusso di lavoro progettato per inviare un’e-mail ai clienti (diversi da clienti VIP) che hanno un’email e sono interessati alle macchine da caffè.

A questo scopo, sono state aggiunte le seguenti attività:

* Un’attività **[!UICONTROL Fork]** che divide il flusso di lavoro in tre percorsi (uno per ogni set clienti),
* Attività **[!UICONTROL Creazione del pubblico]** per eseguire il targeting dei tre set clienti:

   * Clienti con un’e-mail,
   * Clienti appartenenti al pubblico “Interessati alle macchine da caffè” preesistente,
   * Clienti appartenenti al pubblico “VIP o premio” preesistente.

* Un’attività **[!UICONTROL Combina]** che raggruppa i clienti con un’e-mail e quelli interessati alle macchine da caffè,
* Un’attività **[!UICONTROL Combina]** che esclude clienti VIP,
* Un’attività **[!UICONTROL Consegna e-mail]** che invia un’e-mail ai clienti risultanti.

Dopo aver completato il flusso di lavoro, aggiungi l’attività **[!UICONTROL Fine]** alla fine del diagramma. Questa attività ti consente di contrassegnare visivamente la fine di un flusso di lavoro e non ha alcun impatto funzionale.

Dopo aver progettato correttamente il diagramma del flusso di lavoro, è possibile eseguirlo e tenere traccia dell&#39;avanzamento delle varie attività.