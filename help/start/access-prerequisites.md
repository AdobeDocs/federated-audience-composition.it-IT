---
title: Prerequisiti e guardrail per la composizione di pubblico federato
description: Scopri i prerequisiti, le autorizzazioni e i guardrail per la composizione di pubblico federato
exl-id: 661a838f-146e-4d68-bb2d-319827caee3a
TQID: https://experienceleague.adobe.com/VBIotVn1VyiFJChb3mM0VDLUSbG9aQOmbfGnfGgqvhU
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
feature_v2:
  - id: fdbb8fc9-ffa3-4b86-88fe-aa4c5a3e1bc6
subfeature_v2:
  - id: b75843fa-0a67-4a44-a6b1-cc627b0481dc
topic_v2:
  - id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adeb
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: fda4d9d7b45833d7e080ae80f42b7ca5ce36b3ad
workflow-type: tm+mt
source-wordcount: 386
ht-degree: 100%

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
* Microsoft Fabric

Scopri come creare una connessione con questi sistemi nella [panoramica sulle connessioni](../connections/home.md).

## Sandbox

Quando acquisti Composizione di pubblico federato, hai diritto a due sandbox. Per ulteriori richieste di provisioning per la sandbox, contatta il tuo rappresentante Adobe.

Per visualizzare l’elenco delle sandbox attive della composizione di pubblico federato, segui i passaggi seguenti:

1. Da Composizione di pubblico federato, accedi al menu **[!UICONTROL Utilizzo licenze]** in **[!UICONTROL Amministrazione]**.

1. Seleziona l’icona ![](assets/do-not-localize/Smock_InfoOutline_18_N.svg) da **[!UICONTROL Volume totale di dati in uscita]** per accedere alle proprietà della sandbox.

   ![](assets/sandbox_1.png)

1. Le informazioni sulla sandbox sono visualizzate nel popover Proprietà.

   ![](assets/sandbox_2.png)

## Autorizzazioni {#permissions}

Per accedere alla Composizione di pubblico federato, gli utenti devono essere aggiunti al profilo di prodotto specifico per la sandbox creato al momento dell’acquisto e si deve assegnare loro l’autorizzazione **[!UICONTROL Gestisci dati federati]**. [Ulteriori informazioni](/help/governance-privacy-security/access-control.md)

## Elenco IP consentiti {#ip}

Per consentire alla composizione di pubblico federato di accedere ai database in modo sicuro, è necessario autorizzare gli indirizzi IP dei server della composizione di pubblico federato che vi accederanno. Questi indirizzi IP vengono visualizzati quando viene aggiunto un database federato nell’interfaccia utente di Adobe Experience Platform. [Ulteriori informazioni](../connections/home.md)

Aggiungi questi indirizzi IP al tuo elenco consentiti per concedere l’accesso a una composizione di pubblico federato.

## Criteri di unione {#merge-policies}

Se la sandbox utilizza un criterio di unione **precedenza set di dati**, contatta l’Assistenza clienti Adobe per aggiungere il set di dati `Halos UPS` al criterio di unione.

Per ulteriori informazioni sui criteri di unione, consulta la [panoramica sui criteri di unione](https://experienceleague.adobe.com/it/docs/experience-platform/profile/merge-policies/overview).

## Guardrail e limitazioni {#fac-guardrails}

* La composizione di pubblico federato è soggetta alle limitazioni del prodotto e ai guardrail delle prestazioni elencati nella [documentazione di Real-time Customer Data Platform di Adobe](https://experienceleague.adobe.com/it/docs/experience-platform/profile/guardrails){target="_blank"}.

* La composizione di pubblico federato supporta l’esportazione di tipi di pubblico di grandi dimensioni, anche con file di dimensioni superiori a 1 GB. Per prestazioni ottimali, la dimensione massima consigliata del file è di 20 GB.
