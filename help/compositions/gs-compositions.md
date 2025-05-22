---
audience: end-user
title: Introduzione alle composizioni
description: Scopri come iniziare a utilizzare le composizioni
exl-id: 92142d16-3483-4f6e-afde-9f88d5d7d1c4
source-git-commit: e26b3cfda7c4de98d1e47fc40edd2b87859c6209
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 90%

---

# Introduzione alle composizioni {#compositions}

>[!AVAILABILITY]
>
>Per accedere alle composizioni, è necessario disporre di una delle seguenti autorizzazioni:
>
>-**Gestisci composizioni federate**
>-**Visualizza composizioni federate**
>
>Per ulteriori informazioni sulle autorizzazioni richieste, consulta la [Guida all&#39;accesso a Federated Audience Composition](/help/start/feature-access.md).

## Che cos’è una composizione? {#what}

La funzione Composizione del pubblico di Adobe consente di creare composizioni, sfruttando varie attività (suddivisione, esclusione...) in un’area di lavoro visiva per creare tipi di pubblico. Al termine, i tipi di pubblico risultanti vengono salvati in Adobe Experience Platform insieme ai tipi di pubblico esistenti e possono essere sfruttati nelle destinazioni di Adobe Experience Platform e Adobe Journey Optimizer per il targeting della clientela. [Scopri come utilizzare i tipi di pubblico](../start/audiences.md)

![](assets/composition-example.png)

## Accesso e gestione delle composizioni {#access}

>[!CONTEXTUALHELP]
>id="dc_composition_list"
>title="Composizioni"
>abstract="In questa schermata, puoi accedere all’elenco completo delle composizioni, controllarne lo stato, le date dell’ultima/successiva esecuzione e creare una nuova composizione."

Le composizioni sono accessibili dal menu **[!UICONTROL Tipi di pubblico]** di Adobe Experience Platform, nella scheda **[!UICONTROL Composizioni federate]**.

Da questa schermata, puoi creare nuove composizioni e accedere a quelle esistenti. Puoi anche duplicare o eliminare una composizione esistente facendo clic sul pulsante con i puntini di sospensione accanto al relativo nome.

![](assets/compositions-list.png)

Per perfezionare l’elenco e trovare facilmente la composizione che stai cercando, puoi cercare l’elenco e filtrare le composizioni in base ai loro stati o alle ultime date di elaborazione.

È inoltre possibile personalizzare l’elenco aggiungendo o rimuovendo colonne. A tale scopo, fai clic sul pulsante **[!UICONTROL Configura colonne]** e aggiungi o rimuovi le colonne di output desiderate.

![](assets/compositions-columns.png)

## Stati delle composizioni {#status}

Le composizioni possono avere più stati:

* **[!UICONTROL Bozza]**: la composizione è stata creata e salvata.
* **[!UICONTROL In corso]**: la composizione è stata eseguita ed è attualmente in esecuzione.
* **[!UICONTROL Interrotto]**: l’esecuzione della composizione è stata completata ed è stata interrotta.
* **[!UICONTROL In pausa]**: l’esecuzione della composizione è stata messa in pausa.
* **[!UICONTROL Errato]**: l’esecuzione della composizione ha riscontrato un errore. Apri la composizione e accedi ai registri e alle attività per identificare l’errore e risolverlo.

Informazioni dettagliate su come avviare e monitorare una composizione sono disponibili in [questa pagina](../compositions/start-monitor-composition.md).
