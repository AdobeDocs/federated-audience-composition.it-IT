---
audience: end-user
title: Targeting Con Più Entità Con Pubblico Federato Di Composizione Del Pubblico In Adobe Journey Optimizer
description: Scopri come eseguire il targeting dei profili dai tipi di pubblico di Federated Audience Composition nei percorsi Adobe Journey Optimizer.
source-git-commit: 297a1d5019737c35ee07967a6d7330d3ad0bac1d
workflow-type: tm+mt
source-wordcount: '496'
ht-degree: 3%

---


# Targeting con più entità con tipi di pubblico federati per la composizione del pubblico in Adobe Journey Optimizer

Con il targeting con più entità, puoi utilizzare gli attributi del pubblico di Federated Audience Composition come identificatori supplementari nei percorsi Adobe Journey Optimizer. Questi attributi ti consentono di attivare tipi di pubblico a più entità, ad esempio a livello di account o abbonamenti.

## Creare il pubblico in Federated Audience Composition {#create}

Per iniziare con il targeting di più entità, devi prima creare e salvare il pubblico in Federated Audience Composition.

Nell&#39;interfaccia utente di Composizione pubblico, aggiungi l&#39;attività **Genera pubblico** per creare il pubblico nell&#39;area di lavoro di composizione federata e l&#39;attività **Salva pubblico** per configurare le mappature del pubblico, l&#39;identità primaria e la scadenza dei dati.

![Viene visualizzata l&#39;interfaccia utente di Federated Audience Composition, che mostra il pubblico.](/help/connections/assets/multi-entity-targeting/build-activity.png)

Dopo aver completato le configurazioni del pubblico, seleziona **Inizio** per avviare l&#39;esecuzione della composizione. Questo pubblico e il relativo set di dati corrispondente saranno disponibili per l’utilizzo in Experience Platform.

Per ulteriori dettagli sulla creazione di una composizione in Federated Audience Composition, leggi [creare una guida alla composizione](/help/compositions/create-composition.md).

## Attivare il pubblico in Adobe Journey Optimizer {#activate}

Al termine dell’esecuzione della composizione, puoi attivare il pubblico in Journey Optimizer. Nella sezione **Gestione Percorsi** di Adobe Journey Optimizer, seleziona **Percorsi** seguito da **Crea percorso** per aprire l&#39;interfaccia utente del percorso.

![Il pulsante Crea percorso in Adobe Journey Optimizer è evidenziato.](/help/connections/assets/multi-entity-targeting/select-create-journey.png)

Nell&#39;interfaccia di percorso, aggiungi un nodo **Read audience**. Puoi configurare questo nodo fornendo un’etichetta e selezionando il pubblico creato in precedenza.

![Il nodo Read audience viene visualizzato nell&#39;interfaccia utente di Journey Optimizer.](/help/connections/assets/multi-entity-targeting/read-journey.png)

Dopo aver scelto il pubblico creato in precedenza, abilita **Usa identificatore supplementare**.

![La casella di controllo Usa identificatore supplementare è evidenziata.](/help/connections/assets/multi-entity-targeting/enable-use-supplemental-identifier.png)

Ora puoi scegliere un identificatore supplementare. Nella schermata del selettore, seleziona **Modalità avanzata** e passa a **Experience Platform**. All’interno di questa pagina, seleziona il nome del pubblico creato in precedenza e scegli l’identificatore supplementare da utilizzare per il pubblico.

![Viene visualizzato l&#39;editor espressioni.](/help/connections/assets/multi-entity-targeting/add-expression.png)

## Configurare le condizioni di percorso {#configure-journey}

Dopo aver attivato e configurato le impostazioni del pubblico, puoi continuare a configurare le altre condizioni del percorso. Per questo caso d&#39;uso, aggiungi un nodo **Optimizer** dopo il nodo **Read audience**, seguito da un nodo **Action**.

Dopo aver configurato i nodi rimanenti, selezionare **Pubblica** per completare la creazione del percorso.

![Il pulsante Pubblica è evidenziato.](/help/connections/assets/multi-entity-targeting/select-publish.png)

Il percorso eseguirà il targeting dei profili di pubblico in base all&#39;**identificatore supplementare** anziché all&#39;identificatore primario. Utilizzando questa funzione, ora puoi eseguire il targeting di più entità come ID abbonamento, ID account o ID ordine e attivarle nel canale desiderato.

## Passaggi successivi {#next-steps}

Dopo aver letto questa guida, ora sai come utilizzare identificatori supplementari dal pubblico Federated Audience Composition nei percorsi Journey Optimizer. Per ulteriori informazioni sull&#39;utilizzo di percorsi supplementari, leggere la [guida all&#39;uso di identificatori supplementari nei percorsi](https://experienceleague.adobe.com/it/docs/journey-optimizer/using/orchestrate-journeys/manage-journey/supplemental-identifier).
