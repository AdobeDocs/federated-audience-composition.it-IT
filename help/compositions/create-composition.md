---
audience: end-user
title: Creare composizioni
description: Scopri come creare le composizioni
source-git-commit: 194ae763f5040f11eba0fe30aa302064f5d0606a
workflow-type: tm+mt
source-wordcount: '683'
ht-degree: 14%

---


# Creare ed eseguire una composizione {#create-compositions}

>[!CONTEXTUALHELP]
>id="dc_workflow_creation_properties"
>title="Proprietà del flusso di lavoro"
>abstract="In questa schermata, scegli il modello da utilizzare per creare il flusso di lavoro e specifica un’etichetta. Espandi la sezione OPZIONI AGGIUNTIVE per configurare altre impostazioni quali il nome interno del flusso di lavoro, la relativa cartella, il fuso orario e il gruppo di supervisori. Si consiglia vivamente di selezionare un gruppo di supervisori in modo che gli operatori vengano avvisati in caso di errore."

## Creare la composizione {#create}

Per creare una composizione, effettuate le seguenti operazioni:

1. Accedere a **[!UICONTROL Tipi di pubblico]** e selezionare il **[!UICONTROL Composizioni federate]** scheda.

1. Fai clic su **[!UICONTROL Crea composizione]** pulsante.

1. In **[!UICONTROL Proprietà]** , specificare un&#39;etichetta per la composizione e fare clic su **[!UICONTROL Crea]**.

1. Viene visualizzata l’area di lavoro della composizione. Ora puoi configurare la composizione aggiungendo tutte le attività necessarie per soddisfare le tue esigenze prima di eseguirla. Puoi anche configurare impostazioni aggiuntive, ad esempio l’etichetta della composizione o opzioni relative alla gestione degli errori all’esecuzione della composizione.

Per ulteriori informazioni, consulta le sezioni seguenti:

* [Configurare le impostazioni della composizione](#starting-audience)
* [Aggiungere attività](#action-activities)
* [Eseguite la composizione e monitoratene l&#39;esecuzione](#save)

## Configurare le impostazioni della composizione {#settings}

>[!CONTEXTUALHELP]
>id="dc_workflow_settings_properties"
>title="Proprietà di composizione"
>abstract="Questa sezione fornisce proprietà di composizione generiche accessibili anche durante la creazione della composizione."

>[!CONTEXTUALHELP]
>id="dc_workflow_settings_segmentation"
>title="Segmentazione della composizione"
>abstract="Per impostazione predefinita, vengono mantenute solo le tabelle di lavoro dell&#39;ultima esecuzione della composizione. È possibile abilitare questa opzione per mantenere tabelle di lavoro a scopo di test. Deve essere utilizzato **solo** in ambienti di sviluppo o di staging. Non deve mai essere controllato in un ambiente di produzione."

>[!CONTEXTUALHELP]
>id="dc_workflow_settings_error"
>title="Impostazioni di gestione degli errori"
>abstract="In questa sezione puoi definire come gestire gli errori durante l’esecuzione. Potete scegliere di sospendere il processo, ignorare un certo numero di errori o interrompere l&#39;esecuzione della composizione."

Fai clic su **Impostazioni** per accedere alle opzioni aggiuntive per la composizione:

* **[!UICONTROL Etichetta]**: modifica l’etichetta della composizione.

* **[!UICONTROL Mantieni il risultato delle popolazioni provvisorie tra due esecuzioni]**: per impostazione predefinita, vengono mantenute solo le tabelle di lavoro dell’ultima esecuzione della composizione. Le tabelle di lavoro delle esecuzioni precedenti vengono eliminate dal flusso di lavoro di pulizia, che viene eseguito su base giornaliera.

  Se questa opzione è attivata, le tabelle di lavoro verranno mantenute anche dopo l&#39;esecuzione della composizione. Puoi utilizzarlo a scopo di test e quindi deve essere utilizzato **solo** in ambienti di sviluppo o di staging. Questa opzione non deve mai essere selezionata in un flusso di lavoro di produzione.

* **[!UICONTROL Gestione degli errori]**: questa sezione ti consente di definire le azioni da intraprendere in caso di errori in un’attività di composizione. Sono disponibili tre opzioni:

   * **[!UICONTROL Sospendi il processo]**: la composizione viene automaticamente messa in pausa e il suo stato cambia in **[!UICONTROL Non riuscito]**. Una volta risolto il problema, riprendere la composizione utilizzando **[!UICONTROL Riprendi]** pulsanti.
   * **[!UICONTROL Ignora]**: lo stato dell’attività che ha attivato l’errore cambia in **[!UICONTROL Non riuscito]**, ma la composizione mantiene il **[!UICONTROL Avviato]** stato.
   * **[!UICONTROL Interrompi il processo]**: la composizione viene arrestata automaticamente e il suo stato cambia in **[!UICONTROL Non riuscito]**. Una volta risolto il problema, riavvia la composizione utilizzando **[!UICONTROL Inizio]** pulsante.

* **[!UICONTROL Errori consecutivi]**: specifica il numero di errori che possono essere ignorati prima dell’interruzione del processo. Una volta raggiunto questo numero, lo stato della composizione cambia in **[!UICONTROL Non riuscito]**. Se il valore di questo campo è 0, la composizione non verrà mai interrotta indipendentemente dal numero di errori.

## Aggiungere attività {#activities}

L’area di lavoro di composizione consente di configurare in modo da aggiungere tutte le attività necessarie nella composizione in base alle tue esigenze.

A questo scopo, fai clic sul pulsante + sul percorso della composizione, quindi aggiungi l’attività desiderata. Si apre il riquadro a destra, che consente di configurare la nuova attività aggiunta. [Ulteriori informazioni sulle attività nelle composizioni e su come configurarle](../compositions/activities/about-activities.md)

Per rimuovere un’attività dall’area di lavoro, selezionala e fai clic sul pulsante Elimina nel riquadro a destra. Se l’attività che desideri eliminare è padre di altre attività nella composizione, viene visualizzato un messaggio che ti consente di specificare se desideri eliminare solo l’attività selezionata o tutte le relative attività figlio.

## Eseguire la composizione {#execute}

Una volta che la composizione è pronta, fai clic su **[!UICONTROL Inizio]** per eseguirlo e salvare i tipi di pubblico risultanti in Adobe Experience Platform. &quot;È possibile monitorare l’esecuzione del flusso di lavoro utilizzando **Registri** pulsante. Sono disponibili tre schede per aiutarti a monitorare l’esecuzione:

* **[!UICONTROL Registri]**:
* **[!UICONTROL Attività]**:
* **[!UICONTROL Variabili]**:
