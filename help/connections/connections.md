---
audience: end-user
title: Creare e gestire connessioni con i Federated Database
description: Scopri come creare e gestire le connessioni con i Federated Database
badge: label="Disponibilità limitata" type="Informative"
source-git-commit: c1c035d3783af6c3bc94f2ba0aff7ba515fb68e2
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 5%

---

# Creare connessioni {#connections-fdb}

Lavorare con un database federato direttamente in AEP implica stabilire una connessione con esso.

Per impostare una connessione con il database, passare alla sezione **[!UICONTROL DATI FEDERATI]** e nel collegamento **[!UICONTROL Database federati]** fare clic sul pulsante **[!UICONTROL Aggiungi database federato]**.

![](assets/connections_list.png){zoomable="yes"}

Accederai alla finestra per la connessione **[!UICONTROL Proprietà]**, con il nome e il tipo del database.

![](assets/connections_name.png){zoomable="yes"}

Selezionandone il tipo potrai accedere ad altre proprietà da compilare. [Ulteriori informazioni sui database supportati](federated-db.md).

![](assets/connections_details.png){zoomable="yes"}

In base al tipo di database, scopri nei collegamenti riportati di seguito le informazioni necessarie per configurare la connessione:

* [ Amazon Redshift](federated-db.md#amazon-redshift)
* [Azure synapse](federated-db.md#azure-synapse-redshift)
* [Google BigQuery](federated-db.md#google-big-query)
* [Snowflake](federated-db.md#snowflake)
* [Vertica Analytics](federated-db.md#vertica-analytics)

Dopo aver compilato i dettagli, fare clic sul pulsante **[!UICONTROL Verifica connessione]** e sul pulsante **[!UICONTROL Distribuisci funzioni]**.
Completa la creazione della connessione facendo clic sul pulsante **[!UICONTROL Salva]**.

![](assets/connections_testdeploy.png){zoomable="yes"}

Avrai una panoramica della connessione al Federated Database come questa:

![](assets/connections_overview.png){zoomable="yes"}
