---
title: Prerequisiti e guardrail per la composizione di pubblico federato
description: Scopri i prerequisiti, le autorizzazioni e i guardrail per la composizione di pubblico federato
exl-id: 661a838f-146e-4d68-bb2d-319827caee3a
source-git-commit: 0b8781b5b33d96db7d7f23b3c399942b9cfe901f
workflow-type: tm+mt
source-wordcount: '259'
ht-degree: 88%

---

# Prerequisiti e guardrail {#fac-access}

La composizione di pubblico federato richiede i pacchetti Adobe Real-time Customer Data Platform e/o Adobe Journey Optimizer **Prime** o **Ultimate**. Per accedere a questa funzionalità, devi aver acquistato il componente aggiuntivo Composizione di pubblico federato.

>[!AVAILABILITY]
>
>Dopo aver ricevuto la notifica e-mail di benvenuto da Adobe, potrebbero essere necessarie alcune ore prima che l’interfaccia venga aggiornata e le funzioni siano disponibili.

## Sistemi supportati {#supported-systems}

La composizione di pubblico federato supporta i seguenti data warehouse cloud:

* Amazon Redshift
* Azure Synapse
* Databricks
* Google BigQuery
* Snowflake
* Vertica Analytics

Scopri come creare una connessione con questi sistemi in [questa pagina](../connections/connections.md).

## Sandbox

Quando acquisti Federated Audience Composition, hai diritto a due sandbox. Per ulteriori richieste di provisioning per la sandbox, contatta il tuo rappresentante Adobe.

## Autorizzazioni {#permissions}

Per accedere alla Composizione di pubblico federato, gli utenti devono essere aggiunti al profilo di prodotto specifico per la sandbox creato al momento dell’acquisto e si deve assegnare loro l’autorizzazione **[!UICONTROL Gestisci dati federati]**. [Ulteriori informazioni](feature-access.md)

## Elenco IP consentiti {#ip}

Per consentire alla composizione di pubblico federato di accedere ai database in modo sicuro, è necessario autorizzare gli indirizzi IP dei server della composizione di pubblico federato che vi accederanno. Questi indirizzi IP vengono visualizzati quando viene aggiunto un database federato nell’interfaccia utente di Adobe Experience Platform. [Ulteriori informazioni](../connections/connections.md)

Aggiungi questi indirizzi IP al tuo elenco consentiti per concedere l’accesso a una composizione di pubblico federato.

## Guardrail e limitazioni {#fac-guardrails}

* La Composizione di pubblico federato non è attualmente disponibile per la clientela [che acquisisce dati sanitari](https://experienceleague.adobe.com/it/docs/events/customer-data-management-voices-recordings/governance/healthcare-shield){target="_blank"}. [Ulteriori informazioni](https://experienceleague.adobe.com/it/docs/journey-optimizer/using/audiences-profiles-identities/audiences/about-audiences){target="_blank"}

<!--
* Federated Audience Composition is compatible with Privacy & Security Shield and can be used in all verticals except for healthcare industries. Currently, Federated Audience Composition cannot be licensed to customers looking to ingest health data. [Learn more](https://experienceleague.adobe.com/en/docs/events/customer-data-management-voices-recordings/governance/healthcare-shield){target="_blank"}-->

* I diritti, le limitazioni del prodotto e i guardrail relativi alle prestazioni elencati nella [documentazione di Adobe Real-Time Customer Data Platform](https://experienceleague.adobe.com/it/docs/experience-platform/profile/guardrails){target="_blank"} si applicano alla Federated Audience Composition.
