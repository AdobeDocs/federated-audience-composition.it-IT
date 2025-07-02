---
audience: end-user
title: Introduzione alle composizioni
description: Scopri come iniziare a utilizzare le composizioni
exl-id: 92142d16-3483-4f6e-afde-9f88d5d7d1c4
source-git-commit: 5c16e22587cbbbe5bc87cfa4f22210aa8108341c
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Introduzione alle composizioni {#compositions}

>[!AVAILABILITY]
>
>Per accedere alle composizioni, è necessario disporre di una delle seguenti autorizzazioni:
>
>-**Gestione composizioni federate**
>&#x200B;>-**Visualizzazione composizioni federate**
>
>Per ulteriori informazioni sulle autorizzazioni richieste, leggere la [guida al controllo degli accessi](/help/governance-privacy-security/access-control.md).

Federated Audience Composition consente di creare composizioni, in cui è possibile sfruttare varie attività in un’area di lavoro visiva per creare tipi di pubblico. Dopo aver creato la composizione, i tipi di pubblico risultanti vengono salvati in Adobe Experience Platform e possono essere utilizzati nelle destinazioni Experience Platform e in Adobe Journey Optimizer per eseguire il targeting dei clienti.

![Un flusso di lavoro di composizione di esempio viene visualizzato in Federated Audience Composition.](assets/gs-compositions/composition-example.png){zoomable="yes"}{width="70%"}

## Accesso e gestione delle composizioni {#access}

>[!CONTEXTUALHELP]
>id="dc_composition_list"
>title="Composizioni"
>abstract="In questa schermata, puoi accedere all’elenco completo delle composizioni, controllarne lo stato, le date dell’ultima/successiva esecuzione e creare una nuova composizione."

Le composizioni sono accessibili dal menu **[!UICONTROL Tipi di pubblico]** di Adobe Experience Platform, nella scheda **[!UICONTROL Composizioni federate]** della sezione **[!UICONTROL Clienti]**.

Da questa schermata, puoi creare nuove composizioni e accedere a quelle esistenti. Puoi anche duplicare o eliminare una composizione esistente selezionando il pulsante ![puntini di sospensione](/help/assets/icons/more.png) accanto al nome.

Puoi anche visualizzare informazioni sulle composizioni, tra cui il nome, lo stato, l’autore e la data dell’ultima modifica.

| Stato | Descrizione |
| ------ | ----------- |
| **[!UICONTROL Bozza]** | La composizione è stata creata e salvata. |
| **[!UICONTROL In corso]** | La composizione è stata eseguita ed è attualmente in esecuzione. |
| **[!UICONTROL Interrotto]** | L&#39;esecuzione della composizione è stata completata e interrotta. |
| **[!UICONTROL In pausa]** | L&#39;esecuzione della composizione è stata sospesa. |
| **[!UICONTROL Errato]** | Errore durante l&#39;esecuzione della composizione. Per visualizzare ulteriori informazioni sull’errore, apri la composizione e accedi ai registri. |

È possibile apprendere come avviare o interrompere una composizione nella [guida per avviare e monitorare la composizione](./start-monitor-composition.md).

![Viene visualizzato un elenco delle composizioni disponibili.](assets/gs-compositions/compositions-list.png){zoomable="yes"}{width="70%"}{align="center"}

Per perfezionare l’elenco e trovare la composizione che stai cercando, puoi cercare l’elenco e filtrare le composizioni in base ai loro stati o alle ultime date di elaborazione.

È inoltre possibile personalizzare l’elenco aggiungendo o rimuovendo colonne. A tale scopo, selezionare il pulsante **[!UICONTROL Configura colonne]** e aggiungere o rimuovere le colonne di output desiderate.

![Viene visualizzato un elenco delle colonne disponibili che è possibile aggiungere alla pagina di esplorazione delle composizioni.](assets/gs-compositions/compositions-columns.png){zoomable="yes"}{width="70%"}{align="center"}

### Applica etichette di accesso {#access-labels}

Per applicare le etichette di accesso a una composizione specifica, selezionare la composizione, seguita da **[!UICONTROL Gestisci accesso]**.

![Il pulsante &quot;Gestisci accesso&quot; è evidenziato nell&#39;area di lavoro della composizione.](assets/gs-compositions/select-manage-access.png){zoomable="yes"}{width="70%"}{align="center"}

Viene visualizzato il popover **[!UICONTROL Gestisci accesso]**. In questa pagina puoi applicare alla composizione le etichette di accesso e governance dei dati applicabili.

![Viene visualizzato il popover Gestisci accesso. Viene visualizzato un elenco di tutte le etichette disponibili che è possibile applicare alla composizione.](assets/gs-compositions/manage-access.png){zoomable="yes"}{width="70%"}{align="center"}

| Tipo di etichetta | Descrizione |
| ---------- | ----------- |
| Etichette per contratti | Le etichette del contratto (etichette &quot;C&quot;) vengono utilizzate per categorizzare i dati che hanno obblighi contrattuali o sono relativi ai criteri di governance dei dati della tua organizzazione. |
| Etichette di identità | Le etichette di identità (etichette &quot;I&quot;) vengono utilizzate per categorizzare i dati che possono identificare o contattare una persona specifica. |
| Etichette per dati sensibili | Le etichette sensibili (etichette &quot;S&quot;) vengono utilizzate per categorizzare l’utente e/o l’organizzazione in questione come sensibili. |
| Etichette per ecosistemi partner | Le etichette dell’ecosistema partner vengono utilizzate per categorizzare i dati provenienti da origini esterne all’organizzazione. |

Per ulteriori informazioni sulle etichette di accesso e governance dei dati, leggere il glossario delle [etichette di utilizzo dei dati](https://experienceleague.adobe.com/it/docs/experience-platform/data-governance/labels/reference).

## Passaggi successivi

Dopo aver letto questa guida, hai imparato ad accedere, gestire e creare etichette di accesso per le composizioni. Per ulteriori informazioni sull&#39;utilizzo dei tipi di pubblico nel loro insieme, consulta la [guida dei tipi di pubblico](../start/audiences.md).
