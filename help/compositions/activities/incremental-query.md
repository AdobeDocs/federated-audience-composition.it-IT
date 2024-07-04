---
audience: end-user
title: Utilizzare l’attività Incremental query
description: Scopri come utilizzare l’attività Incremental query
hide: true
hidefromtoc: true
source-git-commit: 13e7e75fe1dc175fce9464fa58c7a50b5e6107d4
workflow-type: tm+mt
source-wordcount: '590'
ht-degree: 18%

---

# Query incrementale {#incremental-query}

>[!CONTEXTUALHELP]
>id="dc_orchestration_incrementalquery"
>title="Query incrementale"
>abstract="Il **Query incrementale** attività ti consente di eseguire query sul database utilizzando Query Modeler. Ogni volta che questa attività viene eseguita, i risultati delle esecuzioni precedenti sono esclusi. Ciò ti consente di eseguire il targeting solo per nuovi elementi."

>[!CONTEXTUALHELP]
>id="dc_orchestration_incrementalquery_history"
>title="Cronologia della query incrementale"
>abstract="Cronologia della query incrementale"

>[!CONTEXTUALHELP]
>id="dc_orchestration_incrementalquery_processeddata"
>title="Dati elaborati della query incrementale"
>abstract="Dati elaborati della query incrementale"

Il **Query incrementale** attività consente di eseguire query sul database su base pianificata. Ogni volta che questa attività viene eseguita, i risultati delle esecuzioni precedenti sono esclusi. Ciò ti consente di eseguire il targeting solo per nuovi elementi.

Il **[!UICONTROL Query incrementale]** L’attività può essere utilizzata per vari tipi di utilizzi:

* Segmentazione di singoli utenti per definire il target di un messaggio, un pubblico, ecc.
* Esportazione dei dati. Ad esempio, puoi utilizzare l’attività per esportare regolarmente i nuovi registri in file. Può essere utile se desideri utilizzare i dati di registro in strumenti di reporting o BI esterni.

La popolazione già interessata dalle esecuzioni precedenti è memorizzata nella composizione. Ciò significa che due composizioni avviate dallo stesso modello non condividono lo stesso registro. Tuttavia, due attività basate sulla stessa query incrementale nella stessa composizione utilizzano lo stesso registro.

Se il risultato di una query incrementale è uguale a 0 durante una delle esecuzioni, la composizione viene sospesa fino alla successiva esecuzione programmata della query. Le transizioni e le attività che seguono la query incrementale non vengono quindi elaborate prima dell’esecuzione successiva.

## Configurare l’attività Incremental query {#incremental-query-configuration}

Per configurare il **Query incrementale** attività:

1. Aggiungi un **Query incrementale** attività nella composizione.

1. In **[!UICONTROL Pubblico]** , scegli il **Dimensione targeting** quindi fai clic su **[!UICONTROL Continua]**.

   La dimensione targeting consente di definire la popolazione target dell’operazione: destinatari, beneficiari del contratto, operatore, iscritti, ecc. Per impostazione predefinita, il target viene selezionato dai destinatari. <!--[Learn more about targeting dimensions](../../audience/about-recipients.md#targeting-dimensions)-->

1. Utilizza il modellatore di query per definire la query, nello stesso modo in cui crei un pubblico durante la progettazione di una nuova e-mail. <!--[Learn how to work with the query modeler](../../query/query-modeler-overview.md)-->

1. In **[!UICONTROL Dati elaborati]** selezionare la modalità incrementale da utilizzare:

   * **[!UICONTROL Escludi risultati dell’esecuzione precedente]**: ogni volta che l’attività viene eseguita, i risultati delle esecuzioni precedenti sono esclusi.

     I record già oggetto di targeting nelle esecuzioni precedenti possono essere registrati per un numero massimo di giorni dal giorno in cui sono stati oggetto di targeting. A tale scopo, utilizza **[!UICONTROL Cronologia in giorni]** campo. Se questo valore è zero, i destinatari non vengono mai eliminati dal registro.

   * **[!UICONTROL Utilizza un campo data]**: questa opzione ti consente di escludere i risultati delle esecuzioni precedenti in base a un campo data specifico. A questo scopo, scegli il campo data desiderato dall’elenco di attributi disponibili per la dimensione di targeting selezionata. Nelle esecuzioni successive della composizione, verranno recuperati solo i dati che sono stati modificati o creati dopo l’ultima data di esecuzione.

     Dopo la prima esecuzione della composizione, **[!UICONTROL Data ultima esecuzione]** diventa disponibile. Specifica la data che verrà utilizzata per l’esecuzione successiva e viene aggiornata automaticamente ogni volta che la composizione viene eseguita. Puoi comunque ignorare questo valore immettendone manualmente uno nuovo in modo tale che sia adatto alle tue esigenze.

   >[!NOTE]
   >
   >Il **[!UICONTROL Utilizza un campo data]** consente una maggiore flessibilità a seconda del campo data selezionato. Ad esempio, se il campo specificato corrisponde a una data di modifica, la modalità campo data ti consente di recuperare i dati che sono stati aggiornati di recente, mentre l’altra modalità esclude semplicemente le registrazioni che erano già state oggetto di targeting in un’esecuzione precedente, anche se sono state modificate dopo l’ultima esecuzione della composizione.

<!--

## Example {#incremental-query-example}

The following example shows the configuration of a workflow which filters every week the profiles in the Adobe Campaign database that are subscribed to the Yoga Newsletter service, to send them a welcome email.

![](../assets/incremental-query-example.png)

The workflow is made up of the following elements:

* A **[!UICONTROL Scheduler]** activity, to execute the workflow every Monday at 6 am.
* An **[!UICONTROL Incremental query]** activity, which targets all of the current subscribers during the first execution, then only the new subscribers of that week during the following executions.
* An **[!UICONTROL Email delivery]** activity.
-->
