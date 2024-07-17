---
audience: end-user
title: Utilizzare l’attività Deduplication
description: Scopri come utilizzare l’attività Deduplication
badge: label="Disponibilità limitata" type="Informative"
source-git-commit: 7a3d03543f6f903c3f7f66299b600807cf15de5e
workflow-type: tm+mt
source-wordcount: '565'
ht-degree: 73%

---


# Deduplica {#deduplication}

>[!CONTEXTUALHELP]
>id="dc_orchestration_deduplication_fields"
>title="Campi per identificare i duplicati"
>abstract="Nella sezione **[!UICONTROL Campi per identificare i duplicati]** , fai clic sul pulsante **[!UICONTROL Aggiungi attributo]** per specificare i campi per i quali i valori identici consentono l’identificazione dei duplicati, ad esempio: indirizzo e-mail, nome, cognome e così via. L’ordine dei campi consente di specificare quali elaborare per primi."

>[!CONTEXTUALHELP]
>id="dc_orchestration_deduplication"
>title="Attività Deduplica"
>abstract="L’attività **Deduplica** consente di eliminare i duplicati nei risultati delle attività in entrata. Viene utilizzato principalmente dopo le attività di targeting e prima delle attività che consentono l’utilizzo di dati mirati."

>[!CONTEXTUALHELP]
>id="dc_orchestration_deduplication_complement"
>title="Generare un complemento"
>abstract="Puoi generare una transizione in uscita aggiuntiva con la popolazione rimanente, che è stata esclusa come duplicato. A tale scopo, attiva l’opzione **[!UICONTROL Genera complemento]**."

>[!CONTEXTUALHELP]
>id="dc_orchestration_deduplication_settings"
>title="Impostazioni di deduplica"
>abstract="Per eliminare i duplicati nei dati in arrivo, definisci il metodo di deduplica nei campi seguenti. Per impostazione predefinita, viene mantenuto un solo record. Devi anche selezionare la modalità di deduplica in base a un’espressione o a un attributo. Per impostazione predefinita, il record da escludere dai duplicati viene selezionato in modo casuale."

L&#39;attività **Deduplication** ti consente di eliminare i duplicati nei risultati delle attività in entrata, ad esempio i profili duplicati nell&#39;elenco dei destinatari. L’attività **Deduplica** viene generalmente utilizzata dopo le attività di targeting e prima delle attività che consentono l’utilizzo di dati mirati.

## Configurare l’attività Deduplica{#deduplication-configuration}

Per configurare l’attività **Deduplica** segui questi passaggi:

1. Aggiungi un&#39;attività **Deduplicazione** alla composizione.

1. Se l&#39;attività dispone di diverse transizioni in entrata, selezionare la transizione da utilizzare per eseguire la deduplicazione dall&#39;elenco a discesa **[!UICONTROL Set principale]**

1. Nella sezione **[!UICONTROL Campi per identificare i duplicati]** , fai clic sul pulsante **[!UICONTROL Aggiungi attributo]** per specificare i campi per i quali i valori identici consentono l’identificazione dei duplicati, ad esempio: indirizzo e-mail, nome, cognome e così via. L’ordine dei campi consente di specificare quali elaborare per primi.

   ![](../assets/deduplication.png)

1. Nella sezione **[!UICONTROL Impostazioni deduplicazione]** selezionare il numero di **[!UICONTROL duplicati univoci da mantenere]**. Il valore predefinito per questo campo è 1. Il valore 0 ti consente di conservare tutti i duplicati.

   Ad esempio, se i record A e B sono considerati duplicati del record Y e il record C è considerato un duplicato del record Z:

   * Se il valore del campo è 1: vengono conservati solo i record Y e Z.
   * Se il valore del campo è 0: vengono conservati tutti i record.
   * Se il valore del campo è 2: vengono conservati i record C e Z e due record tra A, B e Y, per caso o a seconda del metodo di deduplicazione selezionato successivamente.

1. Seleziona il **[!UICONTROL Metodo di deduplica]** da utilizzare:

   * **[!UICONTROL Selezione casuale]**: seleziona casualmente il record da escludere dai duplicati.
   * **[!UICONTROL Utilizzo di un&#39;espressione]**: conservare i record in cui il valore dell&#39;espressione immessa è il minore o il maggiore.
   * **[!UICONTROL Valori non vuoti]**: conservare i record per i quali l&#39;espressione non è vuota.
   * **[!UICONTROL Elenco di valori]**: definire una priorità di valore per uno o più campi. Per definire i valori, fai clic su **[!UICONTROL Attributo]** per selezionare un campo o creare un’espressione, quindi aggiungi i valori nella tabella appropriata. Per definire un nuovo campo, fare clic sul pulsante **[!UICONTROL Aggiungi]** situato sopra l&#39;elenco dei valori.

1. Se desideri sfruttare il gruppo rimanente, seleziona l’opzione **[!UICONTROL Genera complemento]**. Il complemento è costituito da tutti i duplicati. Verrà quindi aggiunta all’attività un’ulteriore transizione.

<!--
## Example{#deduplication-example}

In the following example, use a deduplication activity to exclude duplicates from the target before sending a delivery. The identified duplicated profiles are added to a dedicated audience that can be reused if necessary. Choose the **Email** address to identify the duplicates. Keep 1 entry and select the **Random** deduplication method.

![](../assets/workflow-deduplication-example.png)
-->
