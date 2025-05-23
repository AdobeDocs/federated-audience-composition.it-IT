---
title: Accedere alla Composizione di pubblico federato
description: Ulteriori informazioni sulle autorizzazioni richieste per la Composizione di pubblico federato
exl-id: 84138456-218b-4beb-ae7b-146213b03cc2
source-git-commit: 7f8ba57e0fd53350690e391e015f5161b2b7d04e
workflow-type: tm+mt
source-wordcount: '553'
ht-degree: 40%

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

In alternativa, puoi assegnare agli utenti uno dei ruoli preesistenti, a seconda delle autorizzazioni di cui hanno bisogno. Per ulteriori informazioni sull&#39;assegnazione di ruoli preesistenti a un utente, leggere la [guida sulla gestione degli utenti per un profilo di prodotto](https://experienceleague.adobe.com/it/docs/experience-platform/access-control/ui/users).

| Nome ruolo | Autorizzazioni |
| --------- | ----------- |
| Gestori dati FAC | <ul><li>Gestisci composizioni federate</li><li>Visualizza database federati</li><li>Visualizzare gli schemi federati</li><li>Visualizza dati schema federato</li><li>Visualizza modelli dati federati</li></ul> |
| Gestori composizione FAC | <ul><li>Gestisci composizioni federate</li></ul> |
| Amministratori FAC | <ul><li>Gestisci dati federati</li></ul> |

L’utente riceverà quindi un’e-mail con istruzioni per accedere all’istanza. Se l’utente non è già stato creato in precedenza, consulta [questa documentazione](https://experienceleague.adobe.com/it/docs/experience-platform/access-control/abac/permissions-ui/users).
