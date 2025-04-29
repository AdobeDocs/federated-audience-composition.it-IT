---
title: Autorizzazioni per accedere a un database esterno
description: Informazioni sui diritti specifici di ciascun motore di database
source-git-commit: 8cd1b967e004d84fda3788e442e41d2010f5ec24
workflow-type: tm+mt
source-wordcount: '560'
ht-degree: 3%

---

# Matrice di diritti FDA {#fda-rights}

La tabella seguente illustra i privilegi di database richiesti per ciascun sistema, consentendo agli utenti di eseguire operazioni su database esterni tramite FDA.

|   | Snowflake | Redshift | BigQuery Google | Databricks |
|:-:|:-:|:-:|:-:|:-:|
| **Connessione al database remoto** | UTILIZZO NEL MAGAZZINO, UTILIZZO NEL DATABASE e UTILIZZO NEI privilegi DELLO SCHEMA | Creazione di un utente collegato all’account AWS | Crea un account di servizio e concedi all’entità principale l’accesso al progetto | Utilizzare il privilegio CATALOG su Catalog e il privilegio CAN_USE su SQL Warehouse |
| **Creazione di tabelle** | Privilegio CREATE TABLE ON SCHEMA | CREA privilegio | Il ruolo assegnato all&#39;account del servizio deve contenere: bigquery.jobs.create e bigquery.tables.create | Utilizzare i privilegi SCHEMA e CREATE TABLE |
| **Creazione degli indici** | N/D | CREA privilegio | BigQuery supporta solo gli indici di ricerca. Il ruolo assegnato all&#39;account del servizio deve contenere le autorizzazioni bigquery.jobs.create, bigquery.tables.getData e bigquery.tables.createIndex | N/D |
| **Creazione di funzioni** | Privilegio CREATE FUNCTION ON SCHEMA | UTILIZZO ON Privilegio di linguaggio plpythonu per poter richiamare script python esterni | Il ruolo assegnato all&#39;account del servizio deve contenere: bigquery.jobs.create e bigquery.routines.create | Privilegio CREATE FUNCTION |
| **Creazione delle procedure** | N/D | UTILIZZO ON Privilegio di linguaggio plpythonu per poter richiamare script python esterni | Il ruolo assegnato all&#39;account del servizio deve contenere: bigquery.jobs.create e bigquery.routines.create |  N/D |
| **Rimozione di oggetti (tabelle, indici, funzioni, procedure)** | Proprietà dell&#39;oggetto | Possesso dell&#39;oggetto o utente avanzato | Il ruolo assegnato all&#39;account del servizio deve contenere le autorizzazioni bigquery.jobs.create, bigquery.routines.delete, bigquery.tables.delete e bigquery.tables.deleteIndex |
| **Esecuzioni di monitoraggio** | Privilegio MONITOR sull&#39;oggetto richiesto | Nessun privilegio richiesto per utilizzare il comando EXPLAIN | ruolo monitoring.viewer | privilegio CAN_VIEW |
| **Scrittura dei dati** | privilegi INSERT e/o UPDATE (a seconda dell&#39;operazione di scrittura) | Privilegi INSERT e UPDATE | Il ruolo assegnato all&#39;account del servizio deve contenere: bigquery.jobs.create e bigquery.tables.updateData |  MODIFICA privilegio |
| **Caricamento dei dati nelle tabelle** | CREATE STAGE ON SCHEMA, SELECT e INSERT sui privilegi della tabella di destinazione | Privilegi SELECT e INSERT | Il ruolo assegnato all&#39;account del servizio deve contenere: bigquery.jobs.create, bigquery.tables.getData e bigquery.tables.updateData | privilegi SELECT e MODIFY |
| **Accesso ai dati client** | SELEZIONARE i privilegi di TABELLE o VISTE FUTURE | SELECT privilegio | Il ruolo assegnato all&#39;account del servizio deve contenere: bigquery.jobs.create e bigquery.tables.getData per tabelle o il ruolo bigquery.dataViewer |  SELECT privilegio |
| **Accesso ai metadati** | SELEZIONARE il privilegio SCHEMA INFORMATION_SCHEMA | SELECT privilegio | bigquery.metadataViewer, ruolo |  SELEZIONARE il privilegio SCHEMA INFORMATION_SCHEMA |


|   | Microsoft Fabric | Azure Synapse Analytics | Vertica |
|:-:|:-:|:-:|:-:|
| **Connessione al database remoto** | Autorizzazione di lettura (predefinita) | Autorizzazione CONNECT | Nessun privilegio richiesto |
| **Creazione di tabelle** | CREA TABELLA SU DATABASE (warehouse) e MODIFICA SU SCHEMA | Autorizzazione CREA TABELLA | Privilegio CREATE ON SCHEMA |
| **Creazione degli indici** | N/D | Modifica autorizzazione | N/D |
| **Creazione di funzioni** | N/D | Autorizzazione CREATE FUNCTION | Privilegio CREATE ON SCHEMA |
| **Creazione delle procedure** | CREA PROCEDURA SU DATABASE (warehouse) e MODIFICA SU SCHEMA | autorizzazione CREA PROCEDURA | Privilegio CREATE ON SCHEMA |
| **Rimozione di oggetti (tabelle, indici, funzioni, procedure)** | MODIFICA IN BASE A SCHEMA | Modifica autorizzazione | proprietario dell&#39;oggetto o del privilegio DROP sull&#39;oggetto |
| **Esecuzioni di monitoraggio** | Autorizzazioni di Workspace Contributor o di livello superiore (queryinsights.exec_requests_history)  | autorizzazione CONTROL | Nessun privilegio richiesto per utilizzare l&#39;istruzione EXPLAIN |
| **Scrittura dei dati** | INSERISCI e/o AGGIORNA SU OGGETTO | Autorizzazioni INSERT e UPDATE | Privilegi INSERT e UPDATE |
| **Caricamento dei dati nelle tabelle** | SELECT ON OBJECT e INSERT ON OBJECT | CREA TABELLA, ESEGUI, SELEZIONA, INSERISCI, AGGIORNA, MODIFICA AUTORIZZAZIONI | INSERT privilege on table, USAGE privilege on schema |
| **Accesso ai dati client** | SELEZIONA SU OGGETTO | SELECT permission | SELECT privilegio |
| **Accesso ai metadati** | SELEZIONA SU INFORMATION_SCHEMA | Non è richiesta alcuna autorizzazione per descrivere la tabella | UTILIZZO SU SCHEMA, SELECT su TABELLA e anche privilegi su tabelle v_catalog.columns e v_catalog.view_columns |
