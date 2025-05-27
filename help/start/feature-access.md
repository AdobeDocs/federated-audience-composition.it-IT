---
title: Accedere alla Composizione di pubblico federato
description: Ulteriori informazioni sulle autorizzazioni richieste per la Composizione di pubblico federato
exl-id: 84138456-218b-4beb-ae7b-146213b03cc2
source-git-commit: 62bbed4818caf06539234f97d4c0d1cf9c9a52d1
workflow-type: tm+mt
source-wordcount: '479'
ht-degree: 46%

---

# Accedere alla Composizione di pubblico federato {#feature-access}

## Gestire l’accesso alle sandbox {#access-sandboxes}

Quando acquisti la funzionalità Composizione di pubblico federato di Adobe Experience Platform, viene creato un profilo di prodotto per ogni sandbox attiva in quel momento. Questo profilo di prodotto viene creato in Admin Console nella scheda prodotto di **Adobe Experience Platform** e segue questa convenzione di denominazione: `ACP_FAC - <<SandboxName>> - admin.` per accedere alla composizione di pubblico federato per una sandbox specifica, è necessario aggiungere gli utenti al profilo di prodotto creato per tale sandbox.

Ad esempio, se viene attivata una nuova sandbox denominata “fac-test”, viene creato il profilo di prodotto corrispondente “ACP_FAC - fac-test - admin”. Per accedere alle composizione di pubblico federato con questa sandbox, gli utenti devono essere aggiunti a questo profilo di prodotto.

## Gestire l’accesso alla Composizione di pubblico federato

Per accedere a **Federated Audience Composition**, devi prima assicurarti di assegnare le autorizzazioni necessarie per accedere a diversi aspetti di Federated Audience Composition. Questi ruoli devono quindi essere assegnati agli utenti che devono accedere a **Federated Audience Composition**.

Nota: solo gli amministratori possono assegnare le autorizzazioni.

1. Passa al menu **[!UICONTROL Autorizzazioni]**.

1. Dal menu **[!UICONTROL Ruoli]**, seleziona il **[!UICONTROL Ruolo]** che desideri aggiornare.

   ![](assets/access_fda_1.png)

1. Seleziona **[!UICONTROL Modifica]** per modificare le autorizzazioni del tuo ruolo.

   ![](assets/access_fda_2.png)

1. Aggiungi le autorizzazioni richieste per l’utente. Puoi aggiungere le seguenti autorizzazioni per accedere a Federated Audience Composition:

   | Autorizzazione | Descrizione |
   | ---------- | ----------- |
   | Gestisci dati federati | Utilizza questa autorizzazione per gestire tutti gli aspetti di Federated Audience Composition. Questa autorizzazione include le autorizzazioni Gestisci database federato, Gestisci schema federato, Gestisci modello dati federato e Gestisci composizioni federate. |
   | Gestisci database federato | Utilizzare questa autorizzazione per aggiungere, visualizzare, aggiornare ed eliminare le connessioni ai database federati. |
   | Visualizza Federated Database | Utilizzare questa autorizzazione per visualizzare le connessioni ai database federati. |
   | Gestisci schema federato | Utilizzare questa autorizzazione per creare, visualizzare, aggiornare, eliminare e aggiornare schemi. |
   | Visualizza dati schema federato | Utilizza questa autorizzazione per visualizzare la scheda dati all’interno della sezione schema. |
   | Visualizza schema federato | Utilizzare questa autorizzazione per visualizzare le tabelle dello schema. |
   | Gestisci Federated Data Model | Utilizza questa autorizzazione per creare, visualizzare, aggiornare ed eliminare modelli di dati. |
   | Visualizza Federated Data Model | Utilizza questa autorizzazione per visualizzare i modelli di dati. |
   | Visualizza prova di verifica federativa | Utilizza questa autorizzazione per visualizzare l’audit trail per Federated Audience Composition. |
   | Gestisci composizioni federate | Utilizzare questa autorizzazione per creare, visualizzare, aggiornare ed eliminare composizioni federate. |
   | Visualizza composizioni federate | Utilizzare questa autorizzazione per visualizzare le composizioni federate. |

   ![](assets/permissions.png)

1. Dopo aver apportato le modifiche necessarie, seleziona **[!UICONTROL Salva]**.

Tutti gli utenti già assegnati a questo ruolo avranno le autorizzazioni aggiornate automaticamente e l’accesso alla Composizione di pubblico federato.

Per assegnare questo ruolo ai nuovi utenti:

1. Passa alla scheda **[!UICONTROL Utenti]** nel dashboard Ruolo e seleziona **[!UICONTROL Aggiungi utenti]**.

   ![](assets/access_fda_4.png)

1. Inserisci il nome o l’indirizzo e-mail dell’utente oppure selezionalo dall’elenco disponibile. Al termine, seleziona **[!UICONTROL Salva]**.

<!-- Alternatively, you can assign one of the pre-existing roles to the users, depending on what permissions they need. For more information on assigning pre-existing roles to a user, please read the [guide on managing users for a product profile](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/ui/users).

| Role name | Permissions |
| --------- | ----------- |
| FAC Data Managers | <ul><li>Manage Federated Compositions</li><li>View Federated Databases</li><li>View Federated Schemas</li><li>View Federated Schema Data</li><li>View Federated Data Models</li></ul> |
| FAC Composition Managers | <ul><li>Manage Federated Compositions</li></ul> |
| FAC Administrators | <ul><li>Manage Federated Data</li></ul> | -->

L’utente riceverà quindi un’e-mail con istruzioni per accedere all’istanza. Se l’utente non è già stato creato in precedenza, consulta [questa documentazione](https://experienceleague.adobe.com/it/docs/experience-platform/access-control/abac/permissions-ui/users).
