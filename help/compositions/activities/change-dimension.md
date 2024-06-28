---
audience: end-user
title: Utilizzare l’attività Modifica dimensione
description: Scopri come utilizzare l’attività Modifica dimensione
source-git-commit: 92d4a7cf1414ae74b2684619d295eca065a92ce2
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 52%

---

# Cambiare dimensione {#change-dimension}

>[!CONTEXTUALHELP]
>id="dc_orchestration_dimension_complement"
>title="Generare un complemento"
>abstract="Puoi generare una transizione in uscita aggiuntiva con la popolazione rimanente, che è stata esclusa come duplicato. A tale scopo, attiva l’opzione **Genera complemento**"

>[!CONTEXTUALHELP]
>id="dc_orchestration_change_dimension"
>title="Attività Cambia dimensione"
>abstract="Questa attività ti consente di modificare la dimensione targeting durante la creazione di un pubblico. Sposta l’asse in base al modello di dati e alla dimensione di input. Ad esempio, puoi passare dalla dimensione “contratti” alla dimensione “clienti”."

Il **Cambia dimensione** attività ti consente di modificare la dimensione di targeting durante la creazione del pubblico. Sposta l’asse in base al modello di dati e alla dimensione di input. <!--[Learn more on targeting dimensions](../../audience/about-recipients.md#targeting-dimensions)-->


## Configurare l’attività Cambia dimensione {#configure}

Per configurare l’attività **Cambia dimensione** segui questi passaggi:

1. Aggiungi un **Cambia dimensione** alla tua composizione.

1. Definisci la **Nuova dimensione target**. Durante la modifica della dimensione vengono conservati tutti i record.

1. Eseguite la composizione per visualizzare il risultato. Confrontare i dati nelle tabelle prima e dopo l&#39;attività di modifica della dimensione e confrontare la struttura delle tabelle di composizione.

<!--
## Example {#example}

In this example, we want to send an SMS delivery to all the profiles who have made a purchase. To do this, we first use a **[!UICONTROL Build audience]** activity linked to a custom "Purchase" targeting dimension to target all purchases that occurred.

We then use a **[!UICONTROL Change dimension]** activity to switch the workflow targeting dimension to "Recipients". This allows us to be able to target the recipients who match the query.
-->
