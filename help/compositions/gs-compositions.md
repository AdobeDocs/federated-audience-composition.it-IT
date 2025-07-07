---
audience: end-user
title: Introduzione alle composizioni
description: Scopri come iniziare a utilizzare le composizioni
exl-id: 92142d16-3483-4f6e-afde-9f88d5d7d1c4
source-git-commit: 5c16e22587cbbbe5bc87cfa4f22210aa8108341c
workflow-type: ht
source-wordcount: '551'
ht-degree: 100%

---

# Introduzione alle composizioni {#compositions}

>[!AVAILABILITY]
>
>Per accedere alle composizioni, è necessario disporre di una delle seguenti autorizzazioni:
>
>-**Gestione composizioni federate**
>>-**Visualizzazione composizioni federate**
>
>Per ulteriori informazioni sulle autorizzazioni richieste, consulta la [Guida al controllo degli accessi](/help/governance-privacy-security/access-control.md).

La funzione Composizione di pubblico federato consente di creare composizioni, sfruttando varie attività in un’area di lavoro visiva per creare tipi di pubblico. Dopo aver creato la composizione, i tipi di pubblico risultanti vengono salvati in Adobe Experience Platform e possono essere sfruttati nelle destinazioni di Experience Platform e Adobe Journey Optimizer per il targeting della clientela.

![Un flusso di lavoro di composizione di esempio visualizzato in Composizione di pubblico federato.](assets/gs-compositions/composition-example.png){zoomable="yes"}{width="70%"}

## Accesso e gestione delle composizioni {#access}

>[!CONTEXTUALHELP]
>id="dc_composition_list"
>title="Composizioni"
>abstract="In questa schermata, puoi accedere all’elenco completo delle composizioni, controllarne lo stato, le date dell’ultima/successiva esecuzione e creare una nuova composizione."

Le composizioni sono accessibili dal menu **[!UICONTROL Tipi di pubblico]** nella scheda **[!UICONTROL Composizioni federate]**, nella sezione **[!UICONTROL Cliente]**.

Da questa schermata, puoi creare nuove composizioni e accedere a quelle esistenti. Puoi anche duplicare o eliminare una composizione esistente selezionando il pulsante con i ![puntini di sospensione](/help/assets/icons/more.png) accanto al nome.

Puoi anche visualizzare informazioni sulle composizioni, tra cui il nome, lo stato, l’autore e la data dell’ultima modifica.

| Stato | Descrizione |
| ------ | ----------- |
| **[!UICONTROL Bozza]** | La composizione è stata creata e salvata. |
| **[!UICONTROL In corso]** | La composizione è stata eseguita ed è attualmente in esecuzione. |
| **[!UICONTROL Arrestata]** | L’esecuzione della composizione è completa ed è stata interrotta. |
| **[!UICONTROL In pausa]** | L’esecuzione della composizione è stata messa in pausa. |
| **[!UICONTROL Errata]** | L’esecuzione della composizione ha riscontrato un errore. Per visualizzare ulteriori informazioni sull’errore, apri la composizione e accedi ai registri. |

Puoi scoprire come avviare o interrompere una composizione nella [guida per avviare e monitorare la composizione](./start-monitor-composition.md).

![Viene visualizzato un elenco delle composizioni disponibili.](assets/gs-compositions/compositions-list.png){zoomable="yes"}{width="70%"}{align="center"}

Per perfezionare l’elenco e trovare la composizione che stai cercando, puoi filtrarlo in base agli stati delle composizioni o alle ultime date di elaborazione.

Puoi anche personalizzare l’elenco aggiungendo o rimuovendo colonne. A tale scopo, seleziona il pulsante **[!UICONTROL Configura colonne]** e aggiungi o rimuovi le colonne di output desiderate.

![Viene visualizzato un elenco delle colonne disponibili che puoi aggiungere alla pagina di ricerca delle le composizioni.](assets/gs-compositions/compositions-columns.png){zoomable="yes"}{width="70%"}{align="center"}

### Applicare le etichette di accesso {#access-labels}

Per applicare le etichette di accesso a una composizione specifica, seleziona la composizione e poi **[!UICONTROL Gestisci accesso]**.

![Il pulsante “Gestisci accesso” è evidenziato nell’area di lavoro della composizione.](assets/gs-compositions/select-manage-access.png){zoomable="yes"}{width="70%"}{align="center"}

Viene visualizzato il popover **[!UICONTROL Gestisci accesso]**. In questa pagina puoi applicare alla composizione le etichette di accesso e governance dei dati applicabili.

![Viene visualizzato il popover Gestisci accesso. Viene visualizzato un elenco di tutte le etichette disponibili che è possibile applicare alla composizione.](assets/gs-compositions/manage-access.png){zoomable="yes"}{width="70%"}{align="center"}

| Tipo etichetta | Descrizione |
| ---------- | ----------- |
| Etichette per contratti | Le etichette per contratti (“C”) vengono utilizzate per categorizzare i dati con obblighi contrattuali o relativi ai criteri di governance dei dati della tua organizzazione. |
| Etichette di identità | Le etichette di identità (“I”) vengono utilizzate per categorizzare i dati che possono essere identificare o contattare una persona specifica. |
| Etichette per dati sensibili | Le etichette per dati sensibili (“S”) vengono utilizzate per categorizzare i dati che tu o la tua organizzazione considerate come sensibili. |
| Etichette dell’ecosistema dei partner | Le etichette dell’ecosistema dei partner vengono utilizzate per categorizzare i dati provenienti da origini esterne all’organizzazione. |

Per ulteriori informazioni sull’utilizzo delle etichette di accesso e governance dei dati, consulta il [Glossario delle etichette di utilizzo dei dati](https://experienceleague.adobe.com/it/docs/experience-platform/data-governance/labels/reference).

## Passaggi successivi

Dopo aver letto questa guida, hai imparato come accedere, gestire e creare etichette di accesso per le composizioni. Per ulteriori informazioni sull’utilizzo dei tipi di pubblico in generale, consulta la [guida ai tipi di pubblico](../start/audiences.md).
