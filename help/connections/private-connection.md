---
title: Connettersi a Federated Audience Composition utilizzando una connessione privata
description: Scopri come impostare e connettersi a Federated Audience Composition utilizzando una connessione privata. Ciò include PrivateLink o una VPN da sito a sito.
source-git-commit: c4096e842caf383dee2e43bc80e18e1ac2036faf
workflow-type: tm+mt
source-wordcount: '1634'
ht-degree: 0%

---


# Connettività privata a Federated Audience Composition

Federated Audience Composition supporta connessioni private con più database. Le connessioni private consentono di connettersi ai data warehouse ospitati dal cliente senza attraversare la rete Internet pubblica.

## Database supportati {#supported-databases}

I seguenti database supportano la connettività privata a Federated Audience Composition:

| Database | Cloud | Tipo di connessione privata |
| -------- | ----- | ----------------------- |
| [!DNL Snowflake] | [!DNL Amazon Web Services] (AWS) | AWS PrivateLink (endpoint dell’interfaccia VPC) |
| [!DNL Snowflake] | [!DNL Microsoft Azure] | Azure PrivateLink (endpoint privato) |
| [!DNL Amazon Redshift] | [!DNL Amazon Web Services] (AWS) | AWS PrivateLink (endpoint Managed VPC) |
| [!DNL Databricks] | [!DNL Amazon Web Services] (AWS) | AWS PrivateLink (endpoint dell’interfaccia VPC) |
| [!DNL Databricks] | [!DNL Microsoft Azure] | VPN da sito a sito |
| [!DNL Databricks] | [!DNL Google Cloud Platform] (GCP) | VPN da sito a sito |
| [!DNL Azure Synapse Analytics] | [!DNL Microsoft Azure] | VPN da sito a sito |
| [!DNL Google BigQuery] | [!DNL Google Cloud Platform] (GCP) | VPN da sito a sito |

## Snowflake {#snowflake}

>[!AVAILABILITY]
>
>Per utilizzare la connettività privata con [!DNL Snowflake], **è necessario** essere almeno sul livello business critical o superiore su [!DNL Snowflake]. Per ulteriori informazioni sulla connettività privata con [!DNL Snowflake], leggere la [guida alla connettività privata nella documentazione di Snowflake](https://docs.snowflake.com/en/user-guide/private-connectivity-inbound).

L&#39;utilizzo della connettività privata con [!DNL Snowflake] dipende dal provider cloud su cui si trova l&#39;istanza di [!DNL Snowflake].

### Amazon Web Services (AWS) {#snowflake-aws}

>[!IMPORTANT]
>
>Prima di continuare, assicurati di ottenere l’ID account AWS dall’Assistenza clienti di Adobe. Una volta ottenuto l&#39;ID dell&#39;account AWS, contattare il supporto di [!DNL Snowflake] in modo che [!DNL Snowflake] possa autorizzare l&#39;account AWS a utilizzare PrivateLink.

Una volta che il tuo account AWS è stato autorizzato per l&#39;utilizzo con [!DNL Snowflake], dovrai ottenere i valori inclusi `privatelink-vpce-id`, `privatelink-account-url` e `privatelink_ocsp-url` in modo da poter ottenere l&#39;endpoint dell&#39;interfaccia VPC.

È possibile ottenere questi valori eseguendo i seguenti comandi nell&#39;account [!DNL Snowflake] come ACCOUNTADMIN:

`SELECT SYSTEM$GET_PRIVATELINK_CONFIG();`
`SELECT SYSTEM$ALLOWLIST_PRIVATELINK();`

Dopo aver eseguito questi comandi, puoi inviare l’output SQL completo all’Assistenza clienti di Adobe in modo che Adobe possa creare automaticamente l’endpoint dell’interfaccia di VPC.

Per informazioni più dettagliate sulla creazione di una connessione PrivateLink con AWS, consulta la [guida di AWS PrivateLink](https://docs.snowflake.com/en/user-guide/admin-security-privatelink).

Se desideri autorizzare PrivateLink per l’utilizzo con un ambiente di staging interno, contatta l’Assistenza clienti di Adobe per abilitare l’ambiente.

Per informazioni più dettagliate sulla creazione di una connessione PrivateLink con AWS per gli ambienti di staging interni, leggere la [guida degli endpoint dell&#39;interfaccia AWS VPC per le fasi interne](https://docs.snowflake.com/en/user-guide/private-internal-stages-aws).

### Microsoft Azure {#snowflake-azure}

Per Microsoft Azure, è necessario ottenere i valori inclusi `privatelink-pls-id`, `privatelink-account-url` e `privatelink_ocsp-url` per creare l&#39;endpoint privato di Azure.

Puoi ottenere questi valori eseguendo i seguenti comandi nell’account Snowflake:

`SELECT SYSTEM$GET_PRIVATELINK_CONFIG();`
`SELECT SYSTEM$ALLOWLIST_PRIVATELINK();`

Dopo aver eseguito questi comandi, puoi inviare l’output SQL completo all’Assistenza clienti di Adobe in modo che Adobe possa creare automaticamente l’endpoint privato di Azure.

Dopo che Adobe ha creato l’endpoint privato di Azure, puoi ottenere l’ID della risorsa dell’endpoint privato. Ora che disponi dell&#39;ID della risorsa dell&#39;endpoint privato, contatta il supporto [!DNL Snowflake] per autorizzare il tuo account [!DNL Snowflake], fornendo al contempo l&#39;ID della risorsa.

Per informazioni più dettagliate sulla creazione di una connessione PrivateLink con Azure, consulta la [guida di Azure PrivateLink](https://docs.snowflake.com/en/user-guide/privatelink-azure).

Se si desidera autorizzare PrivateLink per l&#39;utilizzo con un ambiente di staging interno, eseguire il comando seguente in [!DNL Snowflake], fornendo l&#39;ID della risorsa stage interno fornito dall&#39;Assistenza clienti di Adobe:

`SELECT SYSTEM$AUTHORIZE_STAGE_PRIVATELINK_ACCESS('<internal-stage-private-endpoint-resource-id>');`

Per informazioni più dettagliate sulla creazione di una connessione PrivateLink con Azure per gli ambienti di staging interni, consulta la [guida degli endpoint privati Azure per le fasi interne](https://docs.snowflake.com/en/user-guide/private-internal-stages-azure).

## Amazon Redshift {#amazon-redshift}

Sia i cluster con provisioning che Redshift Serverless supportano connessioni private con Federated Audience Composition.

>[!IMPORTANT]
>
>Prima di iniziare, contatta l’Assistenza clienti di Adobe per ricevere l’ID del tuo account Amazon Web Services (AWS) e l’ID di Virtual Private Cloud (VPC). Per ottenere l&#39;accesso all&#39;endpoint tra account, sono necessari **entrambi** di questi valori. Per informazioni più dettagliate sulla concessione dell&#39;accesso a VPC, leggere la [guida alla concessione dell&#39;accesso a VPC](https://docs.aws.amazon.com/redshift/latest/mgmt/managing-cluster-cross-vpc-console-grantor.html).

Una volta ottenuti sia gli ID AWS che VPC, accedi ad AWS Management Console per concedere l’accesso tra account diversi per un endpoint VPC gestito.

Per un cluster con provisioning, annotare sia l&#39;identificatore del cluster **Redshift** che i valori dell&#39;ID dell&#39;account AWS **del proprietario del cluster**. Per un server Redshift, annota sia il **nome gruppo di lavoro** che i valori **ID account AWS proprietario**.

Dopo aver ottenuto questi valori, condividi tali dettagli con l’Assistenza clienti di Adobe in modo che Adobe possa creare l’endpoint VPC gestito. Adobe condividerà quindi con te i seguenti dettagli di connessione: **URL endpoint Redshift**, **URL JDBC Redshift** e **URL ODBC Redshift**.

## Databricks {#databricks}

>[!AVAILABILITY]
>
>Per utilizzare la connettività privata con i database, **è necessario** che si trovi in un piano Enterprise per i database. Per ulteriori informazioni sulla connettività privata con Databricks, leggere la [guida sui concetti dei collegamenti privati](https://docs.databricks.com/aws/en/security/network/concepts/privatelink-concepts).

L’utilizzo della connettività privata con i database dipende dal provider di cloud su cui si trova l’istanza dei database.

### Amazon Web Services {#databricks-aws}

Prima di effettuare la configurazione con Amazon Web Services, contatta l’Assistenza clienti di Adobe in modo che possa creare un endpoint di interfaccia VPC front-end (in entrata) che punti a Databricks. Questo endpoint riguarda la connettività ODBC di Federated Audience Composition nell’area di lavoro Databricks.

Dopo aver ottenuto l’ID dell’endpoint VPC e l’area geografica AWS dall’Assistenza clienti di Adobe, è necessario registrare l’endpoint VPC con le informazioni fornite da Adobe.

Dopo aver registrato l&#39;endpoint VPC, è necessario creare un oggetto Impostazioni di accesso privato (PAS). Quando crei l&#39;endpoint, imposta il **Livello di accesso privato** a un livello di **Endpoint** e seleziona l&#39;endpoint VPC creato in precedenza. Per ulteriori informazioni sulla creazione di impostazioni di accesso privato, leggere la [guida alla configurazione di PrivateLink in entrata](https://docs.databricks.com/aws/en/security/network/front-end/front-end-private-connect#step-3-create-private-access-settings).

Dopo aver configurato le impostazioni di accesso privato, puoi collegare l’endpoint VPC all’area di lavoro. Per ulteriori informazioni sulla creazione dell&#39;area di lavoro con PrivateLink, leggere la [guida alla configurazione di PrivateLink in entrata](https://docs.databricks.com/aws/en/security/network/front-end/front-end-private-connect#step-4-create-your-workspace-with-private-link-objects).

Dopo aver configurato tutte le impostazioni, puoi condividere l’URL dell’area di lavoro Databricks con l’Assistenza clienti di Adobe. Dopo aver condiviso l’URL dell’area di lavoro Databricks, Adobe può configurare le impostazioni DNS necessarie per indirizzare le richieste all’endpoint dell’area di lavoro.

### Microsoft Azure {#databricks-azure}

Una VPN da sito a sito viene utilizzata per connettersi in modo sicuro da Adobe all’area di lavoro Databricks su Azure. Devi configurare un gateway VPN Azure per stabilire il tunnel VPN per trasmettere in modo sicuro i tuoi dati ad Adobe.

Dopo aver configurato il gateway VPN Azure e l&#39;endpoint privato Databricks, condividi i seguenti dettagli con il rappresentante dell&#39;Assistenza clienti Adobe: **Azure Virtual Network Gateway**, **Databricks Private Endpoint IP**, **Databricks Workspace URL** e **Autonomous System Number (ASN)**.

Con questi dettagli, Adobe può stabilire i tunnel VPN necessari per la connessione. Dopo aver stabilito i tunnel VPN, Adobe fornisce **gli indirizzi IP pubblici e privati del tunnel VPN**, **le chiavi già condivise** e **il numero di sistema autonomo**.

Ora puoi configurare i tunnel VPN nel gateway Azure VNet. Per ulteriori informazioni, leggere la [guida alla connessione di AWS e Azure tramite un gateway VPN](https://learn.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-howto-aws-bgp).

### Piattaforma Google Cloud {#databricks-gcp}

Una VPN da sito a sito viene utilizzata per connettersi in modo sicuro da Adobe all’area di lavoro Databricks su Google Cloud Platform. Per stabilire il tunnel VPN per trasmettere in modo sicuro i dati ad Adobe, devi configurare un gateway VPN ad alta disponibilità e un router cloud per Google Cloud Platform.

Dopo aver configurato il gateway VPN GCP HA e il router cloud, condividi i seguenti dettagli con il tuo rappresentante dell’Assistenza clienti Adobe: **gateway VPN GCP HA**, **URL Workspace Databricks**, **IP di connessione di servizio privato (PSC)** e **Numero di sistema autonomo (ASN)**.

Con questi dettagli, Adobe può stabilire i tunnel VPN necessari per la connessione. Dopo aver stabilito i tunnel VPN, Adobe fornisce **gli indirizzi IP pubblici e privati del tunnel VPN**, **le chiavi già condivise** e **il numero di sistema autonomo**.

Ora puoi configurare i tunnel VPN nell’account Google Cloud Platform. Per ulteriori informazioni, leggere la [guida alla creazione di connessioni VPN HA](https://docs.cloud.google.com/network-connectivity/docs/vpn/tutorials/create-ha-vpn-connections-google-cloud-aws).

## Azure Synapse Analytics {#azure-synapse}

Per connettersi con Azure Synapse Analytics, devi innanzitutto creare un gateway di rete virtuale Azure e un endpoint privato Synapse. Il gateway di rete virtuale Azure consente di inviare traffico crittografato tra una rete virtuale Azure e Synapse, mentre l&#39;endpoint privato Synapse consente di disporre di una connessione privata per la trasmissione sicura dei dati.

Dopo aver configurato il gateway di rete virtuale Azure e l&#39;endpoint privato Synapse, condividere i seguenti dettagli con il rappresentante dell&#39;Assistenza clienti Adobe: **Azure Virtual Network Gateway**, **Synapse Private Endpoint IP**, **Synapse Workspace URL** e **Autonomous Service Number (ASN)**.

Con questi dettagli, Adobe può stabilire i tunnel VPN necessari per la connessione. Dopo aver stabilito i tunnel VPN, Adobe fornisce le **coppie VPN-tunnel**, **chiavi già condivise** e **numero di sistema autonomo**.

Ora puoi configurare i tunnel VPN nel gateway Azure VNet. Per ulteriori informazioni, leggere la [guida alla connessione di AWS e Azure tramite un gateway VPN](https://learn.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-howto-aws-bgp).

## Google BigQuery {#gbq}

Per connetterti a Google Big Query, devi innanzitutto creare un gateway VPN ad alta disponibilità di Google Cloud Platform e un router cloud.

Dopo aver configurato il gateway VPN GCP HA e il router cloud, condividi i seguenti dettagli con il rappresentante dell’Assistenza clienti Adobe: **gateway VPN GCP HA**, **IP di connessione di servizio privato (PSC)** e **Numero di sistema autonomo (ASN)**.

Con questi dettagli, Adobe può stabilire i tunnel VPN necessari per la connessione. Dopo aver stabilito i tunnel VPN, Adobe fornisce **gli indirizzi IP pubblici e privati del tunnel VPN**, **le chiavi già condivise** e **il numero di sistema autonomo**.

Ora puoi configurare i tunnel VPN nell’account Google Cloud Platform. Per ulteriori informazioni, leggere la [guida alla creazione di connessioni VPN HA](https://docs.cloud.google.com/network-connectivity/docs/vpn/tutorials/create-ha-vpn-connections-google-cloud-aws).
