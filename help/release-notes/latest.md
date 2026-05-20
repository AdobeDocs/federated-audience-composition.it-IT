---
title: Note sulla versione di Federated Audience Composition
description: Ultimi aggiornamenti e note sulla versione per Federated Audience Composition.
exl-id: d4dcaf31-93cd-4a4e-888a-cf1bbdc4ca03
TQID: https://experienceleague.adobe.com/AqtqibUr1TNXwQ9lrtVoQ3CBNwyjSMS64e4s8y4iTSc
product_v2: id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
source-git-commit: 212090ab6e5537c4d23d73564affb64b146dada0
workflow-type: tm+mt
source-wordcount: 671
ht-degree: 12%

---

# Note sulla versione

[!DNL Federated Audience Composition] offre continuamente nuove funzioni, miglioramenti alle funzioni esistenti e correzioni di bug. In queste note sulla versione, tutte le modifiche sono consolidate. [!DNL Federated Audience Composition] è stato sviluppato in modalità nativa su [!DNL Adobe Experience Platform] e ne eredita le innovazioni e i miglioramenti più recenti. Ulteriori informazioni su queste modifiche sono disponibili nelle [Note sulla versione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=it){target="_blank"}.

## Versione di maggio 2026 {#fac-26-05}

La versione di maggio di Federated Audience Composition supporta le seguenti funzionalità:

| Autenticazione WIF (Workload Identity Federation) per Google Big Query |
| --- |
| È ora possibile connettersi a Google Big Query utilizzando l’autenticazione WIF. Per ulteriori dettagli sulla connessione tramite autenticazione WIF, leggere la [panoramica sulle connessioni](/help/connections/home.md#wif-configuration). |

## Versione di aprile 2026 {#fac-26-04}

La versione di aprile di Federated Audience Composition supporta le seguenti funzionalità e miglioramenti:

### Nuove funzionalità {#fac=26-04-feature}

| Nuovo connettore - Teradata |
| --- |
| Il connettore Teradata è ora disponibile per l’utilizzo con Federated Audience Composition. Puoi utilizzare il connettore Teradata per i casi d’uso per la creazione e l’arricchimento del pubblico. Per ulteriori informazioni sul connettore Teradata, leggere la [panoramica delle connessioni](/help/connections/home.md). |

### Miglioramenti {#fac-26-05-improvements}

Questa versione include i seguenti miglioramenti.

- **Targeting con più entità con tipi di pubblico federati di Composizione del pubblico nei percorsi di pubblico lettura di Adobe Journey Optimizer**

  Ora puoi sfruttare gli attributi del pubblico FAC come identificatori supplementari nei percorsi Read Audience di Journey Optimizer. Questo ti consente di attivare i tipi di pubblico a più entità, ad esempio a livello di account o abbonamenti.

  Per ulteriori informazioni, leggere la [guida all&#39;uso di identificatori supplementari nei percorsi](https://experienceleague.adobe.com/it/docs/journey-optimizer/using/orchestrate-journeys/manage-journey/supplemental-identifier).

### Miglioramenti {#fac-26-04-improvements}

Questa versione include i seguenti miglioramenti.

- **Supporto chiavi non crittografate per Snowflake**

  È ora possibile utilizzare chiavi non crittografate quando si utilizza l’autenticazione con coppia di chiavi per connettersi ai data warehouse di Snowflake.

  Per ulteriori informazioni sull&#39;utilizzo di chiavi non crittografate con Snowflake, leggere la [panoramica delle connessioni](/help/connections/home.md).

## Versione di marzo 2026 {#fac-26-03}

La versione di marzo di Federated Audience Composition supporta le seguenti funzionalità:

### Nuove funzionalità {#fac-26-03-feature}

| Segmentazione basata sull’intelligenza artificiale |
| --- |
| Ora puoi creare autonomamente composizioni di pubblico federato all’interno dell’Assistente IA. Quando si utilizza l’Assistente AI per creare il pubblico, l’Assistente AI genera un piano che, dopo l’approvazione, verrà eseguito nel browser. Per ulteriori informazioni sull&#39;utilizzo dell&#39;Assistente IA per la creazione di tipi di pubblico, leggere la [Panoramica dell&#39;Assistente IA](/help/start/ai-assistant.md). |

| Assistente AI per informazioni operative |
| --- |
| Ora puoi porre domande all’Assistente AI sulle informazioni operative all’interno di Federated Audience Composition. Le aree supportate includono connessioni, schemi e modelli di dati. Le composizioni federate sono **non** supportate con questa versione. Per ulteriori informazioni sull&#39;Assistente IA in Federated Audience Composition, leggere la [panoramica dell&#39;Assistente IA](/help/start/ai-assistant.md). |

## Versione di febbraio 2026 {#fac-26-02}

La versione di febbraio di Federated Audience Composition supporta le seguenti funzionalità:

### Nuove funzionalità {#fac-26-02-feature}

| Supporto di arricchimento dei campi |
| --- |
| È ora possibile utilizzare l’attività Salva campo nelle composizioni. L’attività Save field ti consente di arricchire gli schemi di Experience Platform unendo i dati provenienti da magazzini esterni, e di migliorare gli schemi di Experience Platform con attributi aggiuntivi. L’attività Save field supporta sia gli schemi B2B che B2C. Per ulteriori informazioni sull&#39;utilizzo di questa attività, leggere la [panoramica delle attività](../compositions/activities.md#save-fields). |

| Supporto dell’autenticazione avanzata per le banche dati |
| --- |
| Ora puoi connetterti a Federated Audience Composition con Databricks utilizzando l’autenticazione dell’entità servizio o OAuth 2.0. Per ulteriori informazioni sulla creazione di una connessione, leggere la [panoramica delle connessioni](../connections/home.md#create). |

## Versione di gennaio 2026 {#fac-26-01}

La versione di gennaio di Federated Audience Composition supporta le nuove funzionalità e i miglioramenti seguenti:

### Nuove funzionalità {#fac-26-01-feature}

| Supporto dell’autenticazione dell’entità servizio di Azure Synapse |
| --- |
| Ora puoi connetterti a Federated Audience Composition con Azure Synapse utilizzando un’entità servizio. Per ulteriori informazioni sulla creazione di una connessione, leggere la [panoramica delle connessioni](../connections/home.md#create). |

| Disponibilità per i clienti Adobe Experience Platform su Amazon Web Services (AWS) |
| --- |
| Ora puoi utilizzare Federated Audience Composition se la tua istanza di Experience Platform è su AWS. Per ulteriori informazioni su Experience Platform su AWS, consulta la [panoramica su più cloud](https://experienceleague.adobe.com/en/docs/experience-platform/landing/multi-cloud). |

### Miglioramenti {#fac-26-01-improvements}

Questa versione include i seguenti miglioramenti.

- **Configurazione della scadenza dei dati per i tipi di pubblico**

  È ora possibile impostare una scadenza dei dati quando si utilizza l&#39;attività **Save audience** in una composizione.

  Per ulteriori informazioni sulle scadenze dei dati in Federated Audience Composition, consulta la [guida delle attività](../compositions/activities.md#save-audience).
