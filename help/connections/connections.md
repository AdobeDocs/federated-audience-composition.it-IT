---
audience: end-user
title: Creare e gestire connessioni con i Federated Database
description: Scopri come creare e gestire le connessioni con i Federated Database
badge: label="Disponibilità limitata" type="Informative"
exl-id: ab65cd8a-dfa0-4f09-8e9b-5730564050a1
source-git-commit: f549f1611bfe6deb6dc684e3a0d9c968ba7c184a
workflow-type: tm+mt
source-wordcount: '220'
ht-degree: 4%

---

# Creare connessioni {#connections-fdb}

Experience Platform Federated Audience Composition consente al cliente di creare e arricchire i tipi di pubblico dai data warehouse di terze parti e di importare i tipi di pubblico in Adobe Experience Platform.

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

   * [ Amazon Redshift](federated-db.md#amazon-redshift)
   * [Azure synapse](federated-db.md#azure-synapse-redshift)
   * [Google BigQuery](federated-db.md#google-big-query)
   * [Snowflake](federated-db.md#snowflake)
   * [Vertica Analytics](federated-db.md#vertica-analytics)

1. Dopo aver compilato i dettagli, fare clic sul pulsante **[!UICONTROL Verifica connessione]** e sul pulsante **[!UICONTROL Distribuisci funzioni]**.

1. Completa la creazione della connessione facendo clic sul pulsante **[!UICONTROL Salva]**.

   ![](assets/connections_testdeploy.png){zoomable="yes"}

   È disponibile una panoramica della connessione a Federated Database, come illustrato di seguito:

   ![](assets/connections_overview.png){zoomable="yes"}
