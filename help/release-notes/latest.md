---
title: Note sulla versione di Federated Audience Composition
description: Ultimi aggiornamenti e note sulla versione per Federated Audience Composition.
exl-id: d4dcaf31-93cd-4a4e-888a-cf1bbdc4ca03
source-git-commit: 7d12773b36cb963f3d4251a9b88486864056a0fb
workflow-type: tm+mt
source-wordcount: '323'
ht-degree: 11%

---


# Note sulla versione

[!DNL Federated Audience Composition] offre continuamente nuove funzioni, miglioramenti alle funzioni esistenti e correzioni di bug. Tutte le modifiche sono consolidate in queste note sulla versione. [!DNL Federated Audience Composition] è stato creato in modalità nativa su [!DNL Adobe Experience Platform] e ne eredita le innovazioni e i miglioramenti più recenti. Ulteriori informazioni su queste modifiche sono disponibili nelle [Note sulla versione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=it){target="_blank"}.

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
