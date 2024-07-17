---
audience: end-user
title: Introduzione alle composizioni
description: Scopri come iniziare con le composizioni
source-git-commit: 0d6930b15be5013b57b8859dd3d21a5d3367ecae
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 13%

---

# Introduzione alle composizioni {#compositions}

## Che cos&#39;è una composizione? {#what}

Adobe Data Composition consente di creare composizioni, in cui è possibile sfruttare varie attività (suddivisione, esclusione...) in un’area di lavoro visiva per creare tipi di pubblico. Al termine, i tipi di pubblico risultanti vengono salvati in Adobe Experience Platform insieme ai tipi di pubblico esistenti e possono essere utilizzati in destinazioni come Journey Optimizer per eseguire il targeting dei clienti.

![](assets/composition-example.png)

## Accesso e gestione delle composizioni {#access}

>[!CONTEXTUALHELP]
>id="dc_composition_list"
>title="Composizioni"
>abstract="In questa schermata, puoi accedere all’elenco completo delle composizioni, controllarne lo stato, le date dell’ultima/successiva esecuzione e creare una nuova composizione."

Le composizioni sono accessibili dal menu **[!UICONTROL Tipi di pubblico]** di Adobe Experience Platform, nella scheda **Composizioni federate**.

Da questa schermata, puoi creare nuove composizioni e accedere a quelle esistenti. Potete anche duplicare o eliminare una composizione esistente facendo clic sul pulsante con i puntini di sospensione accanto al relativo nome.

![](assets/compositions-list.png)

Per perfezionare l’elenco e trovare facilmente la composizione che stai cercando, puoi cercare l’elenco e filtrare le composizioni in base ai loro stati o alle ultime date di elaborazione.

È inoltre possibile personalizzare l&#39;elenco aggiungendo o rimuovendo colonne. A tale scopo, fare clic sul pulsante **Configura colonna** s e aggiungere o rimuovere le colonne di output desiderate.

![](assets/compositions-columns.png)

## Stati delle composizioni {#status}

Le composizioni possono avere più stati:

* **[!UICONTROL Bozza]**: composizione creata e salvata.
* **[!UICONTROL In corso]**: la composizione è stata eseguita ed è attualmente in esecuzione.
* **[!UICONTROL Arrestato]**: l&#39;esecuzione della composizione è stata interrotta.
* **[!UICONTROL Sospeso]**: l&#39;esecuzione della composizione è stata sospesa.
* **[!UICONTROL Errore]**: l&#39;esecuzione della composizione ha rilevato un errore. Apri la composizione e accedi ai registri e alle attività per identificare l’errore e risolverlo.

Informazioni dettagliate su come avviare e monitorare una composizione sono disponibili in [questa sezione](../compositions/start-monitor-composition.md).