---
title: Prerequisiti e guardrail per la Federated Audience Composition
description: Scopri i prerequisiti, le autorizzazioni e i guardrail per Federated Audience Composition
badge: label="Disponibilità limitata" type="Informative"
source-git-commit: e6858ecd06e97b952e59738f299afc90fddeafb7
workflow-type: tm+mt
source-wordcount: '286'
ht-degree: 2%

---

# Prerequisiti e guardrail {#fac-access}

La composizione federata del pubblico richiede pacchetti Adobe Real-time Customer Data Platform e/o Adobe Journey Optimizer **Prime** o **Ultimate**. Per accedere a questa funzionalità, devi aver acquistato il componente aggiuntivo Federated Audience Composition.

>[!AVAILABILITY]
>
>Dopo aver ricevuto la notifica e-mail di benvenuto da Adobe, potrebbero essere necessarie alcune ore prima che l’interfaccia venga aggiornata e le funzioni disponibili.

## Autorizzazioni {#permissions}

Quando acquisti il componente aggiuntivo Federated Audience Composition, viene creato un profilo di prodotto per ogni sandbox attiva in quel momento. Questo profilo di prodotto viene creato nell&#39;Admin Console della scheda prodotto **Adobe Experience Platform** e segue questa convenzione di denominazione: `ACP_FAC - <<SandboxName>> - admin.` Per accedere a Federated Audience Composition per una sandbox specifica, è necessario aggiungere gli utenti al profilo di prodotto creato per tale sandbox.

Ad esempio, se viene attivata una nuova sandbox denominata &quot;fac-test&quot;, viene creato il profilo di prodotto corrispondente &quot;ACP_FAC - fac-test - admin&quot;. Per accedere a Federated Audience Composition con questa sandbox, gli utenti devono essere aggiunti a questo profilo di prodotto.

## Inserimento di IP nell’elenco Consentiti {#ip}

Per consentire in modo sicuro a Federated Audience Composition di accedere ai database, contatta il rappresentante del tuo Adobe per ottenere gli indirizzi IP dei server Federated Audience Composition che vi accederanno.

Aggiungi questi indirizzi IP al tuo elenco consentiti per concedere l’accesso a Federated Audience Composition.

## Protezioni e limitazioni {#fac-guardrails}

* La Federated Audience Composition è compatibile con Privacy &amp; Security Shield e può essere utilizzata in tutti i verticali ad eccezione delle industrie sanitarie. Attualmente, Federated Audience Composition non può essere concesso in licenza ai clienti che desiderano acquisire dati sullo stato. [Ulteriori informazioni](https://experienceleague.adobe.com/en/docs/events/customer-data-management-voices-recordings/governance/healthcare-shield){target="_blank"}

* A questo componente aggiuntivo si applicano i diritti, le limitazioni del prodotto e i guardrail relativi alle prestazioni elencati nella [documentazione di Adobe Real-time Customer Data Platform](https://experienceleague.adobe.com/en/docs/experience-platform/profile/guardrails){target="_blank"}.
