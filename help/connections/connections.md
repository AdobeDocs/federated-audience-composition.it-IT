---
audience: end-user
title: Creare e gestire connessioni con i database federati
description: Scopri come creare e gestire le connessioni con i database federati
badge: label="Disponibilità limitata" type="Informative"
exl-id: ab65cd8a-dfa0-4f09-8e9b-5730564050a1
source-git-commit: c2d4ec21f497a1c4ad9c1701b4283edd16ca0611
workflow-type: tm+mt
source-wordcount: '220'
ht-degree: 16%

---

# Creare connessioni {#connections-fdb}

La composizione di pubblico federato di Experience Platform consente di creare e arricchire i tipi di pubblico dai data warehouse di terze parti e di importarli in Adobe Experience Platform.

Per utilizzare il database federato e Adobe Experience Platform, è innanzitutto necessario stabilire una connessione. Questa connessione viene impostata in un’interfaccia utente dedicata disponibile nell’interfaccia utente di Adobe Experience Platform, come descritto in questa pagina.

Per impostare una connessione al database, eseguire la procedura seguente:

1. Passa alla sezione **[!UICONTROL FEDERATED DATA]** nella barra a sinistra.

1. Nel collegamento **[!UICONTROL Database federati]**, fare clic sul pulsante **[!UICONTROL Aggiungi database federato]**.

   ![](assets/connections_list.png){zoomable="yes"}

1. Imposta la connessione **[!UICONTROL Proprietà]**, con il nome e il tipo del database.

   ![](assets/connections_name.png){zoomable="yes"}

   Selezionandone il tipo puoi accedere ad altre proprietà da compilare. Ulteriori informazioni sui database supportati in [questa pagina](federated-db.md).

   ![](assets/connections_details.png){zoomable="yes"}

   Le impostazioni di configurazione dipendono dal tipo di database. Sfoglia i collegamenti di seguito per accedere ai dettagli necessari per configurare la connessione:

   * [Amazon Redshift](federated-db.md#amazon-redshift)
   * [Azure Synapse](federated-db.md#azure-synapse-redshift)
   * [Google BigQuery](federated-db.md#google-big-query)
   * [Snowflake](federated-db.md#snowflake)
   * [Vertica Analytics](federated-db.md#vertica-analytics)

1. Dopo aver compilato i dettagli, fare clic sul pulsante **[!UICONTROL Verifica connessione]** e sul pulsante **[!UICONTROL Distribuisci funzioni]**.

1. Completa la creazione della connessione facendo clic sul pulsante **[!UICONTROL Salva]**.

   ![](assets/connections_testdeploy.png){zoomable="yes"}

   È disponibile una panoramica della connessione al database federato, come illustrato di seguito:

   ![](assets/connections_overview.png){zoomable="yes"}
