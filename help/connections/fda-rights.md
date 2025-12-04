---
title: Autorizzazioni per accedere a un database esterno
description: Informazioni sulle autorizzazioni necessarie per accedere ed eseguire attività su ciascun motore di database
exl-id: 287fb4a4-5767-4337-96be-dceca55f756d
source-git-commit: e0bf1f76f7f781fb6fcc3b44898ba805d87a25c9
workflow-type: tm+mt
source-wordcount: '418'
ht-degree: 5%

---

# Matrice di diritti Federated Data Access (FDA) {#fda-rights}

La tabella seguente illustra le autorizzazioni di database richieste per ogni sistema, consentendo di eseguire operazioni su database esterni tramite Federated Data Access (FDA).

|   | Snowflake | Redshift | Google BigQuery | Databricks |
|:-:|:-:|:-:|:-:|:-:|
| **Connessione al database remoto** | Privilegi di `USAGE ON WAREHOUSE`, `USAGE ON DATABASE` e `USAGE ON SCHEMA` | Creare un utente collegato all’account AWS | Crea un account di servizio e concedi all’entità principale l’accesso al progetto | Autorizzazione `USE CATALOG` per il catalogo e autorizzazione `CAN_USE` per SQL Warehouse |
| **Creazione di tabelle** | privilegio `CREATE TABLE ON SCHEMA` | Autorizzazione `CREATE` | Il ruolo assegnato all&#39;account del servizio deve contenere: `bigquery.jobs.create` e `bigquery.tables.create` autorizzazioni | `USE SCHEMA` e `CREATE TABLE` autorizzazioni |
| **Creazione degli indici** | N/D | Autorizzazione `CREATE` | BigQuery supporta solo gli indici di ricerca. Il ruolo assegnato all&#39;account del servizio deve contenere: `bigquery.jobs.create`, `bigquery.tables.getData` e `bigquery.tables.createIndex` autorizzazioni | N/D |
| **Creazione di funzioni** | privilegio `CREATE FUNCTION ON SCHEMA` | Autorizzazione `USAGE ON LANGUAGE plpythonu` per poter chiamare script Python esterni | Il ruolo assegnato all&#39;account del servizio deve contenere: `bigquery.jobs.create` e `bigquery.routines.create` autorizzazioni | Autorizzazione `CREATE FUNCTION` |
| **Creazione delle procedure** | N/D | Autorizzazione `USAGE ON LANGUAGE plpythonu` per poter chiamare script Python esterni | Il ruolo assegnato all&#39;account del servizio deve contenere: `bigquery.jobs.create` e `bigquery.routines.create` autorizzazioni |  N/D |
| **Rimozione di oggetti (tabelle, indici, funzioni, procedure)** | Proprietà dell&#39;oggetto | Possesso dell&#39;oggetto o utente avanzato | Il ruolo assegnato all&#39;account del servizio deve contenere: `bigquery.jobs.create`, `bigquery.routines.delete`, `bigquery.tables.delete` e `bigquery.tables.deleteIndex` autorizzazioni | N/D |
| **Esecuzioni di monitoraggio** | Privilegio `MONITOR` sull&#39;oggetto richiesto | Nessuna autorizzazione richiesta per utilizzare il comando `EXPLAIN` | Ruolo `monitoring.viewer` | Autorizzazione `CAN_VIEW` |
| **Scrittura dei dati** | `INSERT` e/o `UPDATE` privilegi (a seconda dell&#39;operazione di scrittura) | `INSERT` e `UPDATE` autorizzazioni | Il ruolo assegnato all&#39;account del servizio deve contenere: `bigquery.jobs.create` e `bigquery.tables.updateData` | Autorizzazione `MODIFY` |
| **Caricamento dei dati nelle tabelle** | `CREATE STAGE ON SCHEMA`, `SELECT` e `INSERT` sui privilegi della tabella di destinazione | `SELECT` e `INSERT` autorizzazioni | Il ruolo assegnato all&#39;account del servizio deve contenere: `bigquery.jobs.create`, `bigquery.tables.getData` e `bigquery.tables.updateData` | `SELECT` e `MODIFY` autorizzazioni |
| **Accesso ai dati client** | `SELECT on (FUTURE) TABLE(S)` o `VIEW(S)` privilegi | Autorizzazione `SELECT` | Il ruolo assegnato all&#39;account del servizio deve contenere: `bigquery.jobs.create` e `bigquery.tables.getData` per le tabelle o il ruolo `bigquery.dataViewer` | Autorizzazione `SELECT` |
| **Accesso ai metadati** | privilegio `SELECT on INFORMATION_SCHEMA SCHEMA` | Autorizzazione `SELECT` | Ruolo `bigquery.metadataViewer` |  Autorizzazione `SELECT on INFORMATION_SCHEMA SCHEMA` |


|   | Microsoft Fabric | Azure Synapse Analytics | Vertica |
|:-:|:-:|:-:|:-:|
| **Connessione al database remoto** | Autorizzazione di lettura (predefinita) | Autorizzazione `CONNECT` | Nessun privilegio richiesto |
| **Creazione di tabelle** | `CREATE TABLE ON DATABASE` (warehouse) e `ALTER ON SCHEMA` | Autorizzazione `CREATE TABLE` | privilegio `CREATE ON SCHEMA` |
| **Creazione degli indici** | N/D | Autorizzazione `ALTER` | N/D |
| **Creazione di funzioni** | N/D | Autorizzazione `CREATE FUNCTION` | privilegio `CREATE ON SCHEMA` |
| **Creazione delle procedure** | `CREATE PROCEDURE ON DATABASE` (warehouse) e `ALTER ON SCHEMA` | Autorizzazione `CREATE PROCEDURE` | privilegio `CREATE ON SCHEMA` |
| **Rimozione di oggetti (tabelle, indici, funzioni, procedure)** | `ALTER ON SCHEMA` | Autorizzazione `ALTER` | Possedere l&#39;oggetto o il privilegio `DROP` sull&#39;oggetto |
| **Esecuzioni di monitoraggio** | Autorizzazioni di Workspace Contributor o superiori (`queryinsights.exec_requests_history`) | Autorizzazione `CONTROL` | Nessun privilegio richiesto per utilizzare l&#39;istruzione `EXPLAIN` |
| **Scrittura dei dati** | `INSERT` e/o `UPDATE ON OBJECT` | `INSERT` e `UPDATE` autorizzazioni | `INSERT` e `UPDATE` privilegi |
| **Caricamento dei dati nelle tabelle** | `SELECT ON OBJECT` e `INSERT ON OBJECT` | Autorizzazioni `CREATE TABLE`, `EXECUTE`, `SELECT`, `INSERT`, `UPDATE` e `ALTER` | Privilegio `INSERT` sulla tabella, privilegio `USAGE` sullo schema |
| **Accesso ai dati client** | `SELECT ON OBJECT` | Autorizzazione `SELECT` | privilegio `SELECT` |
| **Accesso ai metadati** | `SELECT ON INFORMATION_SCHEMA` | Non è richiesta alcuna autorizzazione per descrivere la tabella | `USAGE ON SCHEMA`, `SELECT on TABLE` e anche privilegi sulle tabelle `v_catalog.columns` e `v_catalog.view_columns` |
