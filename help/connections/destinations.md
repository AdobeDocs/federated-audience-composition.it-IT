---
audience: end-user
title: Arricchire il pubblico di Adobe Experience Platform con dati esterni
description: Scopri come perfezionare e arricchire i tipi di pubblico di Adobe Experience Platform con i dati dei database federati utilizzando la destinazione Federated Audiences Composition.
badge: label="Disponibilità limitata" type="Informative"
source-git-commit: 8cc7a4cb8cf5e98496ddf366b9212c25acfdbbd0
workflow-type: tm+mt
source-wordcount: '553'
ht-degree: 4%

---

# Arricchire il pubblico di Adobe Experience Platform con dati esterni {#connect-aep-fac}

>[!CONTEXTUALHELP]
>id="dc_new_destination"
>title="Creare una destinazione"
>abstract="Immetti le impostazioni per la connessione al nuovo Database federato. Utilizza il pulsante **[!UICONTROL Connetti alla destinazione]** per convalidare la configurazione."

Adobe Experience Platform consente l&#39;integrazione diretta dei tipi di pubblico da Audience Portal ai database esterni utilizzando la destinazione **Adobe Federated Audience Composition**. In questo modo puoi sfruttare i tipi di pubblico esistenti nelle composizioni e arricchirli o perfezionarli utilizzando i dati dei database esterni per creare nuovi tipi di pubblico.

A tal fine, devi impostare una nuova connessione in Adobe Experience Platform alla destinazione Federated Audience Composition di Adobe. Puoi utilizzare una pianificazione per inviare un determinato pubblico a frequenze regolari, selezionare attributi specifici da includere, ad esempio gli ID per la riconciliazione dei dati. Se hai applicato la governance e le policy sulla privacy al pubblico, queste verranno mantenute e rimandate al portale del pubblico una volta aggiornato.

Ad esempio, se archivi i punteggi di credito dei clienti nel tuo data warehouse e disponi di un pubblico Adobe Experience Platform che include i clienti interessati a un prodotto specifico negli ultimi due mesi, puoi perfezionare questo pubblico in base ai punteggi di credito utilizzando la destinazione Federated Audience Composition. Questo processo ti consente di filtrare il pubblico in modo da includere solo profili con punteggi di credito elevati senza trasferire dati sensibili del punteggio di credito dal data warehouse.

I passaggi principali per inviare il pubblico di Adobe Experience Platform ad Adobe Federated Audience Composition sono i seguenti:

1. Accedi al catalogo Destinazioni Adobe Experience Platform e seleziona la destinazione Federated Audience Composition.

   Nel riquadro destro selezionare **[!UICONTROL Configura nuova destinazione]**.

   ![](assets/destination-new.png)

1. Specifica un nome per la nuova connessione e scegli il **[!UICONTROL tipo di connessione]** da utilizzare e il **[!UICONTROL database federato]** a cui vuoi connetterti, quindi fai clic su **[!UICONTROL Avanti]**.

   ![](assets/destination-configure.png)

   La sezione **[!UICONTROL Avvisi]** consente di abilitare gli avvisi per ricevere notifiche sullo stato del flusso di dati verso la destinazione. Per ulteriori informazioni sugli avvisi, consulta la guida su [abbonamento a destinazioni avvisi tramite l&#39;interfaccia utente](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/ui/alerts).

1. Nel passaggio **[!UICONTROL Criteri di governance e azioni di applicazione]**, puoi definire i criteri di governance dei dati e garantire che i dati utilizzati siano conformi quando i tipi di pubblico vengono inviati e sono attivi.

   Dopo aver selezionato le azioni di marketing desiderate per la destinazione, fare clic su **[!UICONTROL Crea]**.

1. Viene creata la nuova connessione alla destinazione. Ora puoi attivare i tipi di pubblico da inviare alla destinazione. A tale scopo, selezionarlo dall&#39;elenco e fare clic su **[!UICONTROL Avanti]**

   ![](assets/destination-activate.png)

1. Selezionare il pubblico desiderato da inviare e fare clic su **[!UICONTROL Avanti]**.

1. Configura il nome del file e una pianificazione di esportazione per i tipi di pubblico selezionati.

   ![](assets/destination-schedule.png)

   >[!NOTE]
   >
   >Informazioni dettagliate su come configurare la pianificazione e i nomi dei file sono disponibili nella documentazione di Adobe Experience Platform:
   >* [Pianifica esportazione pubblico](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/ui/activate/activate-batch-profile-destinations#scheduling)
   >* [Configura nomi file](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/ui/activate/activate-batch-profile-destinations#configure-file-names)

1. Nel passaggio **[!UICONTROL Mappatura]**, seleziona l&#39;attributo e i campi di identità da esportare per il pubblico. Per ulteriori informazioni, vedi il [passaggio di mappatura](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/ui/activate/activate-batch-profile-destinations#mapping) nella documentazione di Adobe Experience Platform.

   ![](assets/destination-attributes.png)

1. Rivedi la configurazione di destinazione e le impostazioni del pubblico, quindi fai clic su **[!UICONTROL Fine]**.

   ![](assets/destination-review.png)

I tipi di pubblico selezionati vengono ora attivati per la nuova connessione. Puoi aggiungere altri tipi di pubblico da inviare con questa connessione tornando alla pagina **[!UICONTROL Attiva tipi di pubblico]**. Una volta attivati, i tipi di pubblico non possono essere rimossi.
