---
audience: end-user
title: Creare e gestire connessioni con i database federati
description: Scopri come creare e gestire le connessioni con i database federati
exl-id: ab65cd8a-dfa0-4f09-8e9b-5730564050a1
source-git-commit: eda1c6fc6344b0ad088b0f23b4d8edfb948d4151
workflow-type: tm+mt
source-wordcount: '1991'
ht-degree: 11%

---

# Creare connessioni {#connections-fdb}

>[!AVAILABILITY]
>
>Per accedere alle connessioni, è necessario disporre di una delle seguenti autorizzazioni:
>
>-**Gestisci database federato**
>&#x200B;>-**Visualizza database federato**
>
>Per ulteriori informazioni sulle autorizzazioni richieste, consulta la [Guida al controllo degli accessi](/help/governance-privacy-security/access-control.md).

La Federated Audience Composition di Experience Platform consente di creare e arricchire i tipi di pubblico dai data warehouse di terze parti e di importarli in Adobe Experience Platform.

## Database supportati {#supported-databases}

Per utilizzare il database federato e Adobe Experience Platform, è innanzitutto necessario stabilire una connessione tra le due origini. Federated Audience Composition consente di connettersi ai seguenti database.

* Amazon Redshift
* Azure Synapse Analytics
* Databricks
* Google BigQuery
* Microsoft Fabric
* Oracle
* Snowflake
* Vertica Analytics

## Crea connessione {#create}

Per creare una connessione, selezionare **[!UICONTROL Database federati]** nella sezione Dati federati.

![Il pulsante Database federati è evidenziato nel menu di navigazione a sinistra.](assets/home/select-federated.png){zoomable="yes" width="70%" align="center"}

Viene visualizzata la sezione Database federati. Selezionare **[!UICONTROL Aggiungi database federato]** per creare una connessione.

![Il pulsante Aggiungi database federato è evidenziato nella pagina di visualizzazione del database federato.](assets/home/add-federated.png){zoomable="yes" width="70%" align="center"}

Viene visualizzato il popover delle proprietà di connessione. È possibile assegnare un nome alla connessione e selezionare il tipo di database da creare.

![Vengono visualizzati i tipi di database federati.](assets/home/select-type.png){zoomable="yes" width="70%" align="center"}

Dopo aver selezionato un tipo, viene visualizzata la sezione **[!UICONTROL Dettagli]**. Questa sezione varia in base al tipo di database scelto in precedenza.

>[!BEGINTABS]

>[!TAB Amazon Redshift]

>[!AVAILABILITY]
>
>Sono supportati solo Amazon Redshift AWS, Amazon Redshift Spectrum e Amazon Redshift Serverless.

Dopo aver selezionato Amazon Redshift, puoi aggiungere i seguenti dettagli:

| Campo | Descrizione |
| ----- | ----------- |
| Server | Nome dell&#39;origine dati. |
| Account | Il nome utente dell’account. |
| Password | La password dell&#39;account. |
| Database | Nome del database. Se è specificato nel nome del server, questo campo può essere lasciato vuoto. |
| Schema di lavoro | Nome dello schema del database da utilizzare per le tabelle di lavoro. Ulteriori informazioni su questa funzione sono disponibili nella [documentazione sugli schemi di Amazon](https://docs.aws.amazon.com/redshift/latest/dg/r_Schemas_and_tables.html){target="_blank"}.<br/><br/>**Nota:** è possibile utilizzare qualsiasi schema del database, inclusi gli schemi utilizzati per l&#39;elaborazione dati temporanea, purché si disponga delle autorizzazioni necessarie per connettersi a questo schema. Tuttavia, **devi** utilizzare schemi di lavoro distinti per collegare più sandbox allo stesso database. |

>[!TAB Azure Synapse Analytics]

>[!NOTE]
>
>Se desideri creare una connessione sicura utilizzando Azure Synapse Analytics, contatta il rappresentante dell’Assistenza clienti di Adobe.

Dopo aver selezionato Azure Synapse Analytics, puoi aggiungere i seguenti dettagli:

| Campo | Descrizione |
| ----- | ----------- |
| Server | URL del server Azure Synapse. |
| Account | Il nome utente dell’account Azure Synapse. |
| Password | Password per l&#39;account di sincronizzazione di Azure. |
| Database | Nome del database. Se è specificato nel nome del server, questo campo può essere lasciato vuoto. |
| Opzioni | Opzioni aggiuntive per la connessione. Per Azure Synapse Analytics puoi specificare il tipo di autenticazione supportato dal connettore. Attualmente, Federated Audience Composition supporta `ActiveDirectoryMSI`. Per ulteriori informazioni sulle stringhe di connessione, leggere la sezione [esempi di stringhe di connessione nella documentazione di Microsoft](https://learn.microsoft.com/it-IT/sql/connect/odbc/using-azure-active-directory?view=sql-server-ver15#example-connection-strings){target="_blank"} . |

>[!TAB Database]

>[!NOTE]
>
>È supportato l’accesso sicuro al data warehouse esterno Databricks tramite collegamento privato. Ciò include connessioni sicure ai database Databricks ospitati su Amazon Web Services (AWS) tramite collegamento privato e a quelli ospitati su Microsoft Azure tramite VPN. Contatta il rappresentante Adobe per assistenza nella configurazione dell’accesso sicuro.

Dopo aver selezionato Database, è possibile aggiungere i seguenti dettagli:

| Campo | Descrizione |
| ----- | ----------- |
| Server | Il nome del server di database. |
| Percorso HTTP | Percorso del cluster o della warehouse. Per ulteriori informazioni sul percorso, leggere la [documentazione dei database sui dettagli della connessione](https://docs.databricks.com/aws/en/integrations/compute-details){target="_blank"}. |
| Password | Token di accesso per il server DatabaseKit. Per ulteriori informazioni su questo valore, leggere la [documentazione sui token di accesso personali](https://docs.databricks.com/aws/en/dev-tools/auth/pat){target="_blank"}. |
| Catalogo | Nome del catalogo dei database. Per ulteriori informazioni sui cataloghi in Databricks, leggere la [documentazione Databricks sui cataloghi](https://docs.databricks.com/aws/en/catalogs/){target="_blank"} |
| Schema di lavoro | Nome dello schema di database da utilizzare per le tabelle di lavoro. <br/><br/>**Nota:** puoi utilizzare lo schema **any** dal database, inclusi gli schemi utilizzati per l&#39;elaborazione dati temporanea, purché tu disponga delle autorizzazioni necessarie per connettersi a questo schema. Tuttavia, **devi** utilizzare schemi di lavoro distinti per collegare più sandbox allo stesso database. |
| Opzioni | Opzioni aggiuntive per la connessione. Le opzioni disponibili sono elencate nella tabella seguente. |

Per i database, è possibile impostare le seguenti opzioni aggiuntive:

| Opzioni | Descrizione |
| ------- | ----------- |
| TimeZoneName | Nome del fuso orario da utilizzare. Questo valore rappresenta il parametro di sessione `TIMEZONE`. Per ulteriori informazioni sui fusi orari, leggere la [documentazione relativa ai databrick sui fusi orari](https://docs.databricks.com/aws/en/sql/language-manual/parameters/timezone#:~:text=The%20system%20default%20is%20UTC%20.){target="_blank"}. |

>[!TAB Google BigQuery]

Dopo aver selezionato Google BigQuery, puoi aggiungere i seguenti dettagli:

| Campo | Descrizione |
| ----- | ----------- |
| Account del servizio | L’indirizzo e-mail dell’account di servizio. Per ulteriori informazioni, leggere la [documentazione dell&#39;account del servizio cloud Google](https://cloud.google.com/iam/docs/service-accounts-create){target="_blank"}. |
| Progetto | ID del progetto. Per ulteriori informazioni, leggere la [documentazione del progetto Google Cloud](https://cloud.google.com/resource-manager/docs/creating-managing-projects){target="_blank"}. |
| Set di dati | Nome del set di dati. Per ulteriori informazioni, leggere la [documentazione del set di dati di Google Cloud](https://cloud.google.com/bigquery/docs/datasets-intro){target="_blank"}. |
| Percorso file chiave | File di chiave del server. Sono supportati solo `json` file. |
| Opzioni | Opzioni aggiuntive per la connessione. Le opzioni disponibili sono elencate nella tabella seguente. |

Per Google BigQuery, puoi impostare le seguenti opzioni aggiuntive:

| Opzioni | Descrizione |
| ------- | ----------- |
| ProxyType | Tipo di proxy utilizzato per connettersi a BigQuery. I valori supportati sono `HTTP`, `http_no_tunnel`, `socks4` e `socks5`. |
| ProxyHost | Il nome host o l’indirizzo IP in cui è possibile raggiungere il proxy. |
| ProxyUid | Numero di porta su cui è in esecuzione il proxy. |
| ProxyPwd | Password per il proxy. |
| bgpath | **Nota:** applicabile solo per lo strumento **bulk-load** (Cloud SDK). <br/><br/> Percorso della directory bin di Cloud SDK sul server. È necessario impostare questa opzione solo se la directory `google-cloud-sdk` è stata spostata in un&#39;altra posizione o se si desidera evitare di utilizzare la variabile PATH. |
| GCloudConfigName | **Nota:** applicabile solo per lo strumento **bulk-load** (Cloud SDK) sopra la versione 7.3.4. <br/><br/> Il nome della configurazione che memorizza i parametri per il caricamento dei dati. Per impostazione predefinita, questo valore è `accfda`. |
| GCloudDefaultConfigName | **Nota:** applicabile solo per lo strumento **bulk-load** (Cloud SDK) sopra la versione 7.3.4. <br/><br/> Il nome della configurazione temporanea per ricreare la configurazione principale per il caricamento dei dati. Per impostazione predefinita, questo valore è `default`. |
| GCloudRecreateConfig | **Nota:** applicabile solo per lo strumento **bulk-load** (Cloud SDK) precedente alla versione 7.3.4. <br/><br/> Valore booleano che consente di decidere se il meccanismo di bulk-load deve ricreare, eliminare o modificare automaticamente le configurazioni di Google Cloud SDK. Se questo valore è impostato su `false`, il meccanismo di caricamento collettivo carica i dati utilizzando una configurazione esistente nel computer. Se questo valore è impostato su `true`, assicurati che la configurazione sia configurata correttamente. In caso contrario, verrà visualizzato l&#39;errore `No active configuration found. Please either create it manually or remove the GCloudRecreateConfig option` e il meccanismo di caricamento tornerà al meccanismo di caricamento predefinito. |

>[!TAB Microsoft Fabric]

Dopo aver selezionato Microsoft Fabric, è possibile aggiungere i seguenti dettagli:

| Campo | Descrizione |
| ----- | ----------- |
| Server | URL del server Microsoft Fabric. |
| ID applicazione | ID applicazione per Microsoft Fabric. Per ulteriori informazioni sull&#39;ID applicazione, leggere la [documentazione di Microsoft Fabric sulla configurazione dell&#39;applicazione](https://learn.microsoft.com/en-us/fabric/workload-development-kit/create-entra-id-app){target="_blank"}. |
| Segreto client | Segreto client per l&#39;applicazione. Per ulteriori informazioni sul segreto client, leggere la [documentazione di Microsoft Fabric sulla configurazione dell&#39;applicazione](https://learn.microsoft.com/en-us/fabric/workload-development-kit/create-entra-id-app#step-8-generate-a-secret-for-your-application){target="_blank"}. |
| Opzioni | Opzioni aggiuntive per la connessione. Le opzioni disponibili sono elencate nella tabella seguente. |

Per Microsoft Fabric, è possibile impostare le seguenti opzioni aggiuntive:

| Opzione | Descrizione |
| ------ | ----------- |
| Autenticazione | Tipo di autenticazione utilizzato dal connettore. I valori supportati includono: `ActiveDirectoryMSI`. Per ulteriori informazioni, leggere la [documentazione di Microsoft sulla connettività di magazzino](https://learn.microsoft.com/en-us/fabric/data-warehouse/connectivity){target="_blank"}. |

>[!TAB Oracle]

>[!IMPORTANT]
>
>Federated Audience Composition supporta la configurazione di connessioni federate con i database di Oracle nella versione 11g o successiva e in hosting su AWS, Azure, Exadata o un cloud privato (purché sia accessibile da una rete esterna). Per ulteriori domande relative alla configurazione del database di Oracle o se devi creare una connessione sicura ad Oracle, contatta il rappresentante dell’Assistenza clienti di Adobe.

Dopo aver selezionato Oracle, puoi aggiungere i seguenti dettagli:

| Campo | Descrizione |
| ----- | ----------- |
| Server | L’URL del server Oracle. |
| Account | Il nome utente dell’account. |
| Password | La password dell’account. |

>[!TAB Snowflake]

>[!NOTE]
>
>È supportato l’accesso sicuro al data warehouse esterno di Snowflake tramite collegamento privato. Il tuo account di Snowflake deve essere ospitato su Amazon Web Services (AWS) o su Azure e situato nella stessa area geografica dell’ambiente di composizione di pubblico federato. Contatta il tuo rappresentante Adobe per assistenza nella configurazione dell’accesso sicuro all’account Snowflake.

Dopo aver selezionato Snowflake, puoi aggiungere i seguenti dettagli:

| Campo | Descrizione |
| ----- | ----------- |
| Server | Nome del server. |
| Utente | Il nome utente dell’account. |
| Password | La password dell’account. |
| Database | Nome del database. Se è specificato nel nome del server, questo campo può essere lasciato vuoto. |
| Schema di lavoro | Nome dello schema di database da utilizzare per le tabelle di lavoro. <br/><br/>**Nota:** puoi utilizzare lo schema **any** dal database, inclusi gli schemi utilizzati per l&#39;elaborazione dati temporanea, purché tu disponga delle autorizzazioni necessarie per connettersi a questo schema. Tuttavia, **devi** utilizzare schemi di lavoro distinti per collegare più sandbox allo stesso database. |
| Chiave privata | La chiave privata per la connessione al database. È possibile caricare un file `.pem` dal sistema locale. |
| Opzioni | Opzioni aggiuntive per la connessione. Le opzioni disponibili sono elencate nella tabella seguente. |

Per Snowflake, puoi impostare le seguenti opzioni aggiuntive:

| Opzioni | Descrizione |
| ------- | ----------- |
| schema di lavoro | Nome dello schema di database da utilizzare per le tabelle di lavoro. |
| TimeZoneName | Nome del fuso orario da utilizzare. Questo valore rappresenta il parametro di sessione `TIMEZONE`. Per impostazione predefinita, viene utilizzato il fuso orario del sistema. Per ulteriori informazioni sui fusi orari, leggere la [documentazione di Snowflake sui fusi orari](https://docs.snowflake.com/en/sql-reference/parameters#timezone){target="_blank"}. |
| WeekStart | Il giorno in cui vuoi far iniziare la settimana. Questo valore rappresenta il parametro di sessione `WEEK_START`. Per ulteriori informazioni sull&#39;inizio della settimana, leggere la [documentazione di Snowflake sul parametro di inizio settimana](https://docs.snowflake.com/en/sql-reference/parameters#week-start){target="_blank"} |
| UseCachedResult | Valore booleano che determina se verranno utilizzati i risultati di Snowflake memorizzati nella cache. Questo valore rappresenta il parametro di sessione `USE_CACHED_RESULTS`. Per impostazione predefinita, questo valore è impostato su true. Per ulteriori informazioni su questo parametro, leggere la [documentazione di Snowflake sui risultati persistenti](https://docs.snowflake.com/en/user-guide/querying-persisted-results){target="_blank"}. |
| bulkThreads | Il numero di thread da utilizzare per il caricatore in blocco di Snowflake. Maggiore è il numero di thread aggiunti, migliori saranno le prestazioni per carichi di massa più grandi. Per impostazione predefinita, questo valore è impostato su 1. |
| chunkSize | Dimensione del file del blocco di ogni caricatore bulk. Se utilizzato contemporaneamente a più thread, puoi migliorare le prestazioni dei carichi in blocco. Per impostazione predefinita, questo valore è impostato su 128 MB. Per ulteriori informazioni sulle dimensioni dei blocchi, leggere la [documentazione di Snowflake sulla preparazione dei file di dati](https://docs.snowflake.com/en/user-guide/data-load-considerations-prepare){target="_blank"}. |
| StageName | Il nome di un ambiente di staging interno con preprovisioning. Questo può essere utilizzato in carichi di massa invece di creare una nuova fase temporanea. |

>[!TAB Vertica Analytics]

Dopo aver selezionato Vertica Analytics, puoi aggiungere i seguenti dettagli:

| Campo | Descrizione |
| ----- | ----------- |
| Server | URL del server Vertica Analytics. |
| Account | Il nome utente dell’account. |
| Password | La password dell’account. |
| Database | Nome del database. Se è specificato nel nome del server, questo campo può essere lasciato vuoto. |
| Schema di lavoro | Nome dello schema di database da utilizzare per le tabelle di lavoro. <br/><br/>**Nota:** puoi utilizzare lo schema **any** dal database, inclusi gli schemi utilizzati per l&#39;elaborazione dati temporanea, purché tu disponga delle autorizzazioni necessarie per connettersi a questo schema. Tuttavia, **devi** utilizzare schemi di lavoro distinti per collegare più sandbox allo stesso database. |
| Opzioni | Opzioni aggiuntive per la connessione. Le opzioni disponibili sono elencate nella tabella seguente. |

Per Vertica Analytics, puoi impostare le seguenti opzioni aggiuntive:

| Opzioni | Descrizione |
| ------- | ----------- |
| TimeZoneName | Nome del fuso orario da utilizzare. Questo valore rappresenta il parametro di sessione `TIMEZONE`. Per ulteriori informazioni sui fusi orari, consulta la [documentazione di Vertica Analytics sui fusi orari](https://docs.vertica.com/24.1.x/en/admin/configuring-db/config-procedure/using-time-zones-with/){target="_blank"} |

>[!ENDTABS]

Dopo aver aggiunto i dettagli della connessione, tieni presente le seguenti impostazioni aggiuntive:

>[!NOTE]
>
>Per utilizzare Federated Audience Composition per un database specifico, è necessario eseguire l&#39;elenco consentiti di **tutti** gli indirizzi IP associati a tale database.

| Impostazioni | Dettagli |
| -------- | ------- |
| Attiva connessione | Interruttore booleano che determina se la connessione verrà abilitata automaticamente. |
| IP server | Un popover che visualizza gli indirizzi IP che devono essere inseriti nell&#39;elenco Consentiti per connettersi al database. |
| Verifica connessione | Consente di verificare i dettagli di configurazione. |

È ora possibile selezionare **[!UICONTROL Distribuisci funzioni]**, seguito da **[!UICONTROL Aggiungi]** per finalizzare la connessione tra il database federato e Experience Platform.
