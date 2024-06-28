---
audience: end-user
title: Introduzione alle composizioni
description: Scopri come iniziare con le composizioni
source-git-commit: 8f4242b02f2cd135bf4adc3a69db08fe1f812e4e
workflow-type: tm+mt
source-wordcount: '305'
ht-degree: 14%

---

# Introduzione alle composizioni {#compositions}

>[!CONTEXTUALHELP]
>id="dc_workflow_settings_properties"
>title="Proprietà di composizione"
>abstract="Questa sezione fornisce proprietà di composizione generiche accessibili anche durante la creazione della composizione."

>[!CONTEXTUALHELP]
>id="dc_workflow_settings_segmentation"
>title="Segmentazione della composizione"
>abstract="Per impostazione predefinita, vengono mantenute solo le tabelle di lavoro dell&#39;ultima esecuzione della composizione. È possibile abilitare questa opzione per mantenere tabelle di lavoro a scopo di test. Deve essere utilizzato **solo** in ambienti di sviluppo o di staging. Non deve mai essere controllato in un ambiente di produzione."




## Cos&#39;è una composizione? {#compositions-start}


>[!CONTEXTUALHELP]
>id="dc_workflow_list"
>title="Composizioni"
>abstract="In questa schermata puoi accedere all’elenco completo delle composizioni, verificarne lo stato corrente, le date dell’ultima/successiva esecuzione e creare una nuova composizione."


## Impostazioni di gestione degli errori  {#error-settings}

>[!CONTEXTUALHELP]
>id="dc_workflow_settings_error"
>title="Impostazioni di gestione degli errori"
>abstract="In questa sezione puoi definire come gestire gli errori durante l’esecuzione. Potete scegliere di sospendere il processo, ignorare un certo numero di errori o interrompere l&#39;esecuzione della composizione."

* **[!UICONTROL Gestione degli errori]**: questo campo ti consente di definire le azioni da intraprendere in caso di errori in un’attività di composizione.
Sono disponibili tre opzioni:

   * **[!UICONTROL Sospendi il processo]**: la composizione viene automaticamente messa in pausa e il suo stato cambia in **[!UICONTROL Non riuscito]**. Una volta risolto il problema, riprendere la composizione utilizzando **[!UICONTROL Riprendi]** pulsanti.
   * **[!UICONTROL Ignora]**: lo stato dell’attività che ha attivato l’errore cambia in **[!UICONTROL Non riuscito]**, ma la composizione mantiene il **[!UICONTROL Avviato]** stato.
   * **[!UICONTROL Interrompi il processo]**: la composizione viene arrestata automaticamente e il suo stato cambia in **[!UICONTROL Non riuscito]**. Una volta risolto il problema, riavvia la composizione utilizzando **[!UICONTROL Inizio]** pulsante.

* **[!UICONTROL Errori consecutivi]**: questo campo diventa disponibile quando il valore **[!UICONTROL Ignora]** è selezionato nel campo **[!UICONTROL In caso di errori]**. È possibile specificare il numero di errori che possono essere ignorati prima dell’interruzione del processo. Una volta raggiunto questo numero, lo stato della composizione cambia in **[!UICONTROL Non riuscito]**. Se il valore di questo campo è 0, la composizione non verrà mai interrotta indipendentemente dal numero di errori.
