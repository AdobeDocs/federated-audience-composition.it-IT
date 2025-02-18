---
audience: end-user
title: Arricchire i tipi di pubblico di Adobe Experience Platform con dati esterni
description: Scopri come perfezionare e arricchire i tipi di pubblico di Adobe Experience Platform con i dati dei database federati utilizzando la destinazione Federated Audiences Composition.
exl-id: 03c2f813-21c9-4570-a3ff-3011f164a55e
source-git-commit: 2dc7e0ef359eb2b864f2d0e49ec4ff48f7c8bf61
workflow-type: tm+mt
source-wordcount: '586'
ht-degree: 8%

---

# Arricchire i tipi di pubblico di Adobe Experience Platform con dati esterni {#connect-aep-fac}

>[!CONTEXTUALHELP]
>id="dc_new_destination"
>title="Creare una destinazione"
>abstract="Immetti le impostazioni per la connessione al nuovo database federato. Utilizza il pulsante **[!UICONTROL Connetti alla destinazione]** per convalidare la configurazione."

Adobe Experience Platform consente l&#39;integrazione diretta dei tipi di pubblico da Audience Portal con i database esterni utilizzando la destinazione **Adobe Federated Audience Composition**. Con questa integrazione, puoi sfruttare i tipi di pubblico esistenti nelle composizioni e arricchirli o perfezionarli utilizzando i dati dei database esterni per creare nuovi tipi di pubblico.

A tal fine, devi impostare una nuova connessione in Adobe Experience Platform alla destinazione Federated Audience Composition di Adobe. Puoi utilizzare una pianificazione per inviare un determinato pubblico a frequenze regolari, selezionare attributi specifici da includere, ad esempio gli ID per la riconciliazione dei dati. Se hai applicato la governance e le policy sulla privacy al pubblico, queste verranno mantenute e rimandate al portale del pubblico una volta aggiornato.

Ad esempio, supponiamo che tu stia memorizzando le informazioni di acquisto nel tuo data warehouse e che un pubblico Adobe Experience Platform sia indirizzato ai clienti interessati a un prodotto specifico negli ultimi due mesi. Utilizzando la destinazione Federated Audience Composition puoi:

* Perfeziona il pubblico in base alle informazioni di acquisto. Ad esempio, puoi filtrare il pubblico in modo da eseguire il targeting dei clienti che hanno effettuato un acquisto superiore ai 150$.
* Arricchisci il pubblico con campi relativi agli acquisti, come il nome del prodotto e la quantità acquistata.

I passaggi principali per inviare i tipi di pubblico di Adobe Experience Platform ad Adobe Federated Audience Composition sono i seguenti:

1. Accedi al catalogo Destinazioni Adobe Experience Platform e seleziona la destinazione Federated Audience Composition.

   Nel riquadro destro selezionare **[!UICONTROL Configura nuova destinazione]**.

   ![](assets/destination-new.png)

1. Immettere un nome per la nuova connessione e selezionare **[!UICONTROL Tipo di connessione]** tra le connessioni disponibili seguenti:

   * Amazon Redshift
   * Azure Synapse Analytics
   * Google BigQuery
   * Snowflake
   * Vertica Analytics
   * Databricks

1. Selezionare il **[!UICONTROL database federato]** a cui connettersi e fare clic su **[!UICONTROL Avanti]**.

   ![](assets/destination-configure.png)

1. Nella sezione **[!UICONTROL Avvisi]**, puoi abilitare gli avvisi per ricevere notifiche sullo stato del flusso di dati verso la tua destinazione.

   Per ulteriori informazioni sugli avvisi, consulta la documentazione di Adobe Experience Platform relativa all&#39;abbonamento di [avvisi alle destinazioni tramite l&#39;interfaccia utente](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/ui/alerts){target="_blank"}

1. Nel passaggio **[!UICONTROL Criteri di governance e azioni di applicazione]**, puoi definire i criteri di governance dei dati e garantire che i dati utilizzati siano conformi quando i tipi di pubblico vengono inviati e sono attivi.

   Dopo aver selezionato le azioni di marketing desiderate per la destinazione, fare clic su **[!UICONTROL Crea]**.

1. Viene creata la nuova connessione alla destinazione. Ora puoi attivare i tipi di pubblico da inviare alla destinazione. A tale scopo, selezionarlo dall&#39;elenco e fare clic su **[!UICONTROL Avanti]**

   ![](assets/destination-activate.png)

1. Selezionare il pubblico desiderato da inviare e fare clic su **[!UICONTROL Avanti]**.

1. Configura il nome del file e una pianificazione di esportazione per i tipi di pubblico selezionati.

   ![](assets/destination-schedule.png)

   >[!NOTE]
   >
   >Informazioni dettagliate su come configurare pianificazione e nomi di file sono disponibili nelle seguenti sezioni della documentazione di Adobe Experience Platform:
   >
   >* [Pianifica esportazione pubblico](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/ui/activate/activate-batch-profile-destinations#scheduling){target="_blank"}
   >* [Configura nomi file](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/ui/activate/activate-batch-profile-destinations#configure-file-names){target="_blank"}

1. Nel passaggio **[!UICONTROL Mappatura]**, seleziona l&#39;attributo e i campi di identità da esportare per il pubblico. Per ulteriori informazioni, vedi il [passaggio di mappatura](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/ui/activate/activate-batch-profile-destinations#mapping){target="_blank"} nella documentazione di Adobe Experience Platform.

   ![](assets/destination-attributes.png)

1. Rivedi la configurazione di destinazione e le impostazioni del pubblico, quindi fai clic su **[!UICONTROL Fine]**.

   ![](assets/destination-review.png)

I tipi di pubblico selezionati vengono ora attivati per la nuova connessione. Puoi aggiungere altri tipi di pubblico da inviare con questa connessione tornando alla pagina **[!UICONTROL Attiva tipi di pubblico]**. Una volta attivati, i tipi di pubblico non possono essere rimossi.
