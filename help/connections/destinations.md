---
audience: end-user
title: Arricchire i tipi di pubblico di Adobe Experience Platform con dati esterni
description: Scopri come perfezionare e arricchire i tipi di pubblico di Adobe Experience Platform con i dati dei database federati utilizzando la destinazione Federated Audiences Composition.
exl-id: 03c2f813-21c9-4570-a3ff-3011f164a55e
TQID: https://experienceleague.adobe.com/g32ycFuhXFq68NmBJjunWZT3m4JpmL108bhMSs-4EYc
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
topic_v2:
  - id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adeb
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: ce79e1b9216ca69020155978ac84f29577c5ff8d
workflow-type: tm+mt
source-wordcount: 774
ht-degree: 5%

---

# Arricchire i tipi di pubblico di Adobe Experience Platform con dati esterni {#connect-aep-fac}

>[!CONTEXTUALHELP]
>id="dc_new_destination"
>title="Creare una destinazione"
>abstract="Immetti le impostazioni per la connessione al nuovo database federato. Utilizza il pulsante **[!UICONTROL Connetti alla destinazione]** per convalidare la configurazione."

Adobe Experience Platform consente l&#39;integrazione diretta dei tipi di pubblico da Audience Portal con i database esterni utilizzando la destinazione **Adobe Federated Audience Composition**. Con questa integrazione, puoi sfruttare i tipi di pubblico esistenti nelle composizioni e arricchirli o perfezionarli utilizzando i dati dei database esterni per creare nuovi tipi di pubblico.

A tal fine, devi impostare una nuova connessione in Adobe Experience Platform alla destinazione Federated Audience Composition di Adobe. Puoi utilizzare una pianificazione per inviare un determinato pubblico a frequenze regolari, selezionare attributi specifici da includere, ad esempio gli ID per la riconciliazione dei dati. Se hai applicato la governance e le policy sulla privacy al pubblico, queste verranno mantenute e rimandate al portale del pubblico una volta aggiornato.

Ad esempio, supponiamo che tu stia memorizzando le informazioni di acquisto nel tuo data warehouse e che un pubblico Adobe Experience Platform sia indirizzato ai clienti interessati a un prodotto specifico negli ultimi due mesi. Utilizzando la destinazione Federated Audience Composition puoi:

* Perfeziona il pubblico in base alle informazioni di acquisto. Ad esempio, puoi filtrare il pubblico in modo da eseguire il targeting solo dei clienti che hanno effettuato un acquisto superiore a 150 $.
* Arricchisci il pubblico con campi relativi agli acquisti, come il nome del prodotto e la quantità acquistata.

## Attiva pubblico nella destinazione {#activate}

Nel catalogo Destinazioni di Adobe Experience Platform, seleziona la destinazione Federated Audience Composition. Nel riquadro di destra, selezionare **[!UICONTROL Configura nuova destinazione]**.

![Il pulsante Configura nuova destinazione è evidenziato nel catalogo delle destinazioni.](assets/destinations/new.png)

Viene visualizzata la pagina **[!UICONTROL Configura nuova destinazione]**. In questa pagina è possibile configurare i dettagli della destinazione, inclusi il nome, la descrizione, il tipo di connessione e il database federato.

![Viene visualizzata la pagina Configura nuova destinazione, che mostra i dettagli da aggiungere per creare la destinazione.](assets/destinations/configure.png)

Nella sezione **[!UICONTROL Avvisi]**, puoi abilitare gli avvisi per ricevere notifiche sullo stato del flusso di dati verso la tua destinazione. Questi includono avvisi per ritardi nell’esecuzione dei flussi di dati, errori di esecuzione, successi dell’esecuzione, avvii dell’esecuzione e salti di attivazione.

Per ulteriori informazioni sugli avvisi, consulta la documentazione di Adobe Experience Platform relativa all&#39;abbonamento di [avvisi alle destinazioni tramite l&#39;interfaccia utente](https://experienceleague.adobe.com/it/docs/experience-platform/destinations/ui/alerts){target="_blank"}.

![Vengono visualizzati gli avvisi disponibili per la destinazione.](assets/destinations/alerts.png)

Al termine della configurazione dei dettagli della destinazione, seleziona **[!UICONTROL Successivo]**. Viene visualizzato il passaggio **[!UICONTROL Criteri di governance e azioni di applicazione]**. In questa pagina puoi definire i criteri di governance dei dati e assicurarti che i dati utilizzati siano conformi quando i tipi di pubblico vengono inviati e sono attivi.

Al termine della selezione delle azioni di marketing desiderate per la destinazione, selezionare **[!UICONTROL Crea]**.

Viene creata la nuova connessione alla destinazione. Ora puoi attivare i tipi di pubblico da inviare alla destinazione. Scegli la destinazione alla quale desideri attivare i tipi di pubblico, seguita da **[!UICONTROL Successivo]**.

![Il pulsante di attivazione è evidenziato.](assets/destinations/activate.png)

Viene visualizzato il passaggio **[!UICONTROL Pianificazione]**. Puoi selezionare i tipi di pubblico desiderati che desideri attivare nella destinazione. Per impostare una pianificazione, seleziona ![icona matita](assets/do-not-localize/Smock_Edit_18_N.svg) per modificare la pianificazione dell&#39;esportazione.

![Viene visualizzata la pagina Attiva destinazione.](assets/destinations/schedule.png)

Viene visualizzato il popover **[!UICONTROL Pianificazione]**. In questo popover puoi definire le opzioni di esportazione dei file, la frequenza e impostare la pianificazione.

![Viene visualizzato il popover della pianificazione.](assets/destinations/schedule-2.png)

>[!NOTE]
>
>Per attivare i tipi di pubblico più rapidamente, seleziona l&#39;opzione **[!UICONTROL Dopo la valutazione del segmento]** per attivare il processo di attivazione subito dopo il completamento del processo di segmentazione batch giornaliero di Platform.
>
>Per informazioni dettagliate su come configurare la pianificazione e i nomi di file, consulta le sezioni seguenti della documentazione di Adobe Experience Platform:
>
>* [Pianifica esportazione pubblico](https://experienceleague.adobe.com/it/docs/experience-platform/destinations/ui/activate/activate-batch-profile-destinations#scheduling){target="_blank"}
>* [Configura nomi file](https://experienceleague.adobe.com/it/docs/experience-platform/destinations/ui/activate/activate-batch-profile-destinations#configure-file-names){target="_blank"}

Nel passaggio **[!UICONTROL Mappatura]**, seleziona l&#39;attributo e i campi di identità da esportare per il pubblico.

>[!IMPORTANT]
>
>**impossibile** utilizzare le colonne generate dal sistema durante l&#39;attivazione nelle destinazioni. Se si seleziona una colonna generata dal sistema, si verifica un errore.

Per ulteriori informazioni, consulta la [sezione di mappatura](https://experienceleague.adobe.com/it/docs/experience-platform/destinations/ui/activate/activate-batch-profile-destinations#mapping){target="_blank"} nella documentazione di Adobe Experience Platform.

![Viene visualizzata la pagina degli attributi di mappatura.](assets/destinations/attributes.png)

Rivedi la configurazione di destinazione e le impostazioni del pubblico, quindi seleziona **[!UICONTROL Fine]**.

![Viene visualizzata la pagina della destinazione di revisione.](assets/destinations/review.png)

I tipi di pubblico selezionati vengono ora attivati per la nuova connessione. Puoi aggiungere altri tipi di pubblico da inviare con questa connessione tornando alla pagina **[!UICONTROL Attiva tipi di pubblico]**. Una volta attivati, i tipi di pubblico non possono essere rimossi.
