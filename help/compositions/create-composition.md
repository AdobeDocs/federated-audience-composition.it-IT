---
audience: end-user
title: Creare composizioni
description: Scopri come creare le composizioni
exl-id: 4f510805-b700-444d-89bb-832eaa1e3242
source-git-commit: 65052ffcd8c70817aa428bea7f8b6baa0a49a1b0
workflow-type: tm+mt
source-wordcount: '499'
ht-degree: 21%

---

# Creare e configurare la composizione {#create}

Il primo passaggio per creare una composizione consiste nel definirne l’etichetta e, se necessario, configurare ulteriori impostazioni.

## Creare la composizione {#create-the-composition}

1. Accedi al menu **[!UICONTROL Tipi di pubblico]** e seleziona la scheda **[!UICONTROL Composizioni federate]**.

1. Fare clic sul pulsante **[!UICONTROL Crea composizione]**.

   ![](assets/composition-create.png)

1. Nella sezione **[!UICONTROL Proprietà]**, specifica un&#39;etichetta per la composizione e seleziona un modello dati. Solo gli schemi associati a questo modello dati saranno disponibili nelle attività della composizione.

   ![](assets/composition-select-schema.png)

1. Fai clic su **[!UICONTROL Crea]**. Viene visualizzata l’area di lavoro della composizione. Ora puoi configurare la composizione aggiungendo tutte le attività necessarie per soddisfare le tue esigenze prima di eseguirla:

   * [Scopri come coordinare le attività](orchestrate-activities.md)
   * [Scopri come avviare e monitorare una composizione](start-monitor-composition.md)

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

Quando accedete a una composizione, potete accedere a impostazioni avanzate che consentono, ad esempio, di definire il comportamento della composizione in caso di errore. Per accedere a queste opzioni aggiuntive, fare clic sul pulsante **[!UICONTROL Impostazioni]** nella sezione superiore della schermata di creazione della composizione.

![](assets/composition-create-settings.png)

Le impostazioni disponibili sono le seguenti:

* **[!UICONTROL Etichetta]**: modifica l&#39;etichetta della composizione.

* **[!UICONTROL Mantieni il risultato delle popolazioni provvisorie tra due esecuzioni]**: per impostazione predefinita, vengono mantenute solo le tabelle di lavoro dell&#39;ultima esecuzione della composizione. Le tabelle di lavoro delle esecuzioni precedenti sono eliminate da una composizione tecnica, che viene eseguita su base giornaliera.

  Se questa opzione è attivata, le tabelle di lavoro verranno mantenute anche dopo l&#39;esecuzione della composizione. Puoi utilizzarlo a scopo di test e quindi deve essere utilizzato **solo** in ambienti di sviluppo o di staging. Non deve mai essere controllato in una composizione di produzione.

* **[!UICONTROL Gestione degli errori]**: questa opzione consente di definire le azioni da eseguire in caso di errori in un&#39;attività di composizione. Sono disponibili tre opzioni:

   * **[!UICONTROL Sospendi il processo]**: la composizione viene automaticamente sospesa e il suo stato cambia in **[!UICONTROL Non riuscito]**. Una volta risolto il problema, riprendere la composizione utilizzando i pulsanti **[!UICONTROL Riprendi]**.
   * **[!UICONTROL Ignora]**: lo stato dell&#39;attività che ha attivato l&#39;errore diventa **[!UICONTROL Non riuscito]**, ma la composizione mantiene lo stato **[!UICONTROL Avviato]**.
   * **[!UICONTROL Interrompi il processo]**: la composizione viene interrotta automaticamente e il suo stato cambia in **[!UICONTROL Non riuscito]**. Una volta risolto il problema, riavviare la composizione utilizzando il pulsante **[!UICONTROL Avvia]**.

* **[!UICONTROL Errori consecutivi]**: specificare il numero di errori che possono essere ignorati prima dell&#39;interruzione del processo. Una volta raggiunto questo numero, lo stato della composizione diventa **[!UICONTROL Non riuscito]**. Se il valore di questo campo è 0, la composizione non verrà mai interrotta indipendentemente dal numero di errori.
