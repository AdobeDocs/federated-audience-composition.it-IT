---
title: Accedere a Federated Audience Composition
description: Scopri le autorizzazioni richieste per Federated Audience Composition
exl-id: 84138456-218b-4beb-ae7b-146213b03cc2
hide: true
hidefromtoc: true
source-git-commit: e9cc50cbcbd076f784c924bd941e4396c14190ce
workflow-type: tm+mt
source-wordcount: '309'
ht-degree: 36%

---

# Accedere a Federated Audience Composition {#feature-access}

## Gestire l’accesso alle sandbox {#access-sandboxes}

Quando acquisti il componente aggiuntivo Composizione di pubblico federato, viene creato un profilo di prodotto per ogni sandbox attiva in quel momento. Questo profilo di prodotto viene creato in Admin Console nella scheda prodotto di **Adobe Experience Platform** e segue questa convenzione di denominazione: `ACP_FAC - <<SandboxName>> - admin.` per accedere alla composizione di pubblico federato per una sandbox specifica, è necessario aggiungere gli utenti al profilo di prodotto creato per tale sandbox.

Ad esempio, se viene attivata una nuova sandbox denominata “fac-test”, viene creato il profilo di prodotto corrispondente “ACP_FAC - fac-test - admin”. Per accedere alle composizione di pubblico federato con questa sandbox, gli utenti devono essere aggiunti a questo profilo di prodotto.

## Gestire l’accesso a Federated Audience Composition

>[!AVAILABILITY]
>
>Le autorizzazioni sono disponibili con la versione di marzo.

Per accedere a **Federated Audience Composition**, devi prima verificare che l&#39;autorizzazione **Manage Federated Data** sia assegnata ai ruoli appropriati. Questi ruoli devono quindi essere assegnati agli utenti che devono accedere a **Federated Audience Composition**.

Solo gli amministratori possono assegnare le autorizzazioni.

1. Passa al menu **[!UICONTROL Autorizzazioni]**.

1. Dal menu **[!UICONTROL Ruoli]**, seleziona il **[!UICONTROL Ruolo]** che desideri aggiornare.

   ![](assets/access_fda_1.png)

1. Fai clic su **[!UICONTROL Modifica]** per modificare le autorizzazioni del tuo ruolo.

   ![](assets/access_fda_2.png)

1. Aggiungi la risorsa **Federated Data**, quindi seleziona **[!UICONTROL Gestisci Federated Data]** dal menu a discesa.

   ![](assets/access_fda_3.png)

1. Dopo aver apportato le modifiche necessarie, fai clic su **[!UICONTROL Salva]**.

Tutti gli utenti già assegnati a questo ruolo avranno le loro autorizzazioni aggiornate automaticamente e avranno accesso a Federated Audience Composition.

Per assegnare questo ruolo a nuovi utenti:

1. Passa alla scheda **[!UICONTROL Utenti]** nel dashboard dei ruoli e fai clic su **[!UICONTROL Aggiungi utenti]**.

   ![](assets/access_fda_4.png)

1. Inserisci il nome o l’indirizzo e-mail dell’utente oppure selezionalo dall’elenco disponibile. Al termine, fai clic su **[!UICONTROL Salva]**.

L’utente riceverà quindi un’e-mail con le istruzioni per accedere all’istanza. Se l’utente non è già stato creato in precedenza, consulta [questa documentazione](https://experienceleague.adobe.com/it/docs/experience-platform/access-control/abac/permissions-ui/users).
