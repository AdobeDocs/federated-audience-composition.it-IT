---
title: Prerequisiti e guardrail per la composizione di pubblico federato
description: Scopri i prerequisiti, le autorizzazioni e i guardrail per la composizione di pubblico federato
badge: label="Disponibilità limitata" type="Informative"
source-git-commit: 07170ee709c9e3c4ad0bb2390aa0d44adae3b059
workflow-type: ht
source-wordcount: '274'
ht-degree: 100%

---

# Prerequisiti e guardrail {#fac-access}

La composizione di pubblico federato richiede i pacchetti Adobe Real-time Customer Data Platform e/o Adobe Journey Optimizer **Prime** o **Ultimate**. Per accedere a questa funzionalità, devi aver acquistato il componente aggiuntivo Composizione di pubblico federato.

>[!AVAILABILITY]
>
>Dopo aver ricevuto la notifica e-mail di benvenuto da Adobe, potrebbero essere necessarie alcune ore prima che l’interfaccia venga aggiornata e le funzioni siano disponibili.

## Autorizzazioni {#permissions}

Quando acquisti il componente aggiuntivo Composizione di pubblico federato, viene creato un profilo di prodotto per ogni sandbox attiva in quel momento. Questo profilo di prodotto viene creato in Admin Console nella scheda prodotto di **Adobe Experience Platform** e segue questa convenzione di denominazione: `ACP_FAC - <<SandboxName>> - admin.` per accedere alla composizione di pubblico federato per una sandbox specifica, è necessario aggiungere gli utenti al profilo di prodotto creato per tale sandbox.

Ad esempio, se viene attivata una nuova sandbox denominata “fac-test”, viene creato il profilo di prodotto corrispondente “ACP_FAC - fac-test - admin”. Per accedere alle composizione di pubblico federato con questa sandbox, gli utenti devono essere aggiunti a questo profilo di prodotto.

## Elenco IP consentiti {#ip}

Per consentire a una composizione di pubblico federato di accedere ai database in modo sicuro, contatta il rappresentante Adobe per ottenere gli indirizzi IP dei server di una composizione di pubblico federato che vi accederanno.

Aggiungi questi indirizzi IP al tuo elenco consentiti per concedere l’accesso a una composizione di pubblico federato.

## Guardrail e limitazioni {#fac-guardrails}

* La composizione di pubblico federato non è attualmente disponibile per i clienti [che acquisiscono dati sanitari](https://experienceleague.adobe.com/it/docs/events/customer-data-management-voices-recordings/governance/healthcare-shield){target="_blank"} e per i clienti Adobe Journey Optimizer Privacy and Security Shield. [Ulteriori informazioni](https://experienceleague.adobe.com/it/docs/journey-optimizer/using/audiences-profiles-identities/audiences/about-audiences){target="_blank"}.

<!--
* Federated Audience Composition is compatible with Privacy & Security Shield and can be used in all verticals except for healthcare industries. Currently, Federated Audience Composition cannot be licensed to customers looking to ingest health data. [Learn more](https://experienceleague.adobe.com/en/docs/events/customer-data-management-voices-recordings/governance/healthcare-shield){target="_blank"}-->

* A questo componente aggiuntivo si applicano i diritti, le limitazioni del prodotto e i guardrail delle prestazioni elencati nella [documentazione di Real-time Customer Data Platform di Adobe](https://experienceleague.adobe.com/it/docs/experience-platform/profile/guardrails){target="_blank"}.
