---
audience: end-user
title: Cambia attività di Data Source
description: Scopri come utilizzare l’attività di modifica dell’origine dati per modificare l’origine dati utilizzata dalla composizione, fornendo maggiore flessibilità nella gestione dei dati in una composizione.
exl-id: 8f8e627a-fef9-42b8-a42a-bfa1c421b202
source-git-commit: 59983bb7fd0f8886cc38bfcfc8d7005db4747ac0
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 3%

---

# Modificare l’origine dati

>[!IMPORTANT]
>
>Le attività **[!UICONTROL Cambia dimensione]** e **[!UICONTROL Cambia origine dati]** devono **non** essere aggiunte in una riga. Se devi utilizzare entrambe le attività consecutivamente, includi un&#39;attività **[!UICONTROL Arricchimento]** tra di esse. In questo modo si garantisce la corretta esecuzione e si evitano potenziali conflitti o errori.

L&#39;attività **[!UICONTROL Modifica origine dati]** consente di modificare l&#39;origine dati utilizzata dalla composizione.

## Configurare {#configure}

Dopo aver aggiunto un&#39;attività **[!UICONTROL Modifica origine dati]** all&#39;area di lavoro, è possibile definire l&#39;origine dati per il flusso di lavoro.

![L&#39;opzione dell&#39;origine dati è evidenziata nell&#39;area di lavoro Federated Audience Composition.](/help/compositions/assets/change-data-source/configure.png){zoomable="yes"}{width="70%"}

| Origine | Descrizione |
| ------ | ----------- |
| Account esterno FDA | Un database cloud esterno connesso a Federated Audience Composition. |

Dopo aver selezionato **[!UICONTROL l&#39;account esterno FDA]**, puoi scegliere con quale account esterno connetterti.

![Viene visualizzato il popover con le opzioni dell&#39;account esterno.](/help/compositions/assets/change-data-source/fda-external-account.png){zoomable="yes"}{width="70%"}
