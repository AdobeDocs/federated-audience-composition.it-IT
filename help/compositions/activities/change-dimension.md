---
audience: end-user
title: Utilizzare l’attività Modifica dimensione
description: Scopri come utilizzare l’attività Modifica dimensione
exl-id: e71017bd-6d2f-4ace-b2d9-cbfbb537d127
source-git-commit: 65052ffcd8c70817aa428bea7f8b6baa0a49a1b0
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 49%

---

# Cambiare dimensione {#change-dimension}

>[!CONTEXTUALHELP]
>id="dc_orchestration_dimension_complement"
>title="Generare un complemento"
>abstract="Puoi generare una transizione in uscita aggiuntiva con la popolazione rimanente, che è stata esclusa come duplicato. A tale scopo, attiva l’opzione **[!UICONTROL Genera complemento]**"

>[!CONTEXTUALHELP]
>id="dc_orchestration_change_dimension"
>title="Attività Cambia dimensione"
>abstract="Questa attività consente di modificare lo schema, noto anche come dimensione targeting durante la creazione di un pubblico. Sposta l’asse in base al modello di dati e alla schema di input. Ad esempio, puoi passare dallo schema “contratti” allo schema “clienti”."

L&#39;attività **Modifica dimensione** consente di modificare lo schema, noto anche come dimensione di targeting, durante la creazione del pubblico. Sposta l’asse a seconda del modello di dati e dello schema di input.

## Configurare l’attività Cambia dimensione {#configure}

Per configurare l’attività **Cambia dimensione** segui questi passaggi:

1. Aggiungi un&#39;attività **Modifica dimensione** alla composizione.

   ![](../assets/change-dimension.png)

1. Definisci il **nuovo schema**. Durante la modifica dello schema, vengono conservati tutti i record.

1. Eseguite la composizione per visualizzare il risultato. Confrontare i dati nelle tabelle prima e dopo l&#39;attività **Modifica dimensione** e confrontare la struttura delle tabelle di composizione.

<!--
## Example {#example}

In this example, we want to send an SMS delivery to all the profiles who have made a purchase. To do this, we first use a **[!UICONTROL Build audience]** activity linked to a custom "Purchase" targeting dimension to target all purchases that occurred.

We then use a **[!UICONTROL Change dimension]** activity to switch the workflow targeting dimension to "Recipients". This allows us to be able to target the recipients who match the query.
-->

