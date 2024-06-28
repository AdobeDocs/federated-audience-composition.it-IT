---
audience: end-user
title: Utilizzare l’attività AND-join
description: Scopri come utilizzare l’attività AND-join
source-git-commit: e2e708a21aa0e2d1724f5ba79caf10ef803ae818
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 66%

---

# AND-join {#join}

>[!CONTEXTUALHELP]
>id="dc_orchestration_and-join"
>title="Attività AND-join"
>abstract="Il **And-join** attività consente di sincronizzare più rami di esecuzione di una composizione. Viene attivata al termine di tutte le attività precedenti. Questo ti consente di assicurarti che alcune attività siano terminate prima di continuare a eseguire la composizione."

Il **And-join** attività consente di sincronizzare più rami di esecuzione di una composizione.

Questa attività attiva la relativa transizione in uscita solo dopo che tutte le transizioni in entrata sono state attivate, in altre parole, dopo che tutte le attività precedenti sono state completate. Questo ti consente di verificare che alcune attività siano state completate prima di continuare a eseguire la composizione.

## Configurare l’attività And-join {#and-join-configuration}

>[!CONTEXTUALHELP]
>id="dc_orchestration_and-join_merging"
>title="Configurare l’attività And-join"
>abstract="Seleziona le attività che vuoi unire. Nel menu a discesa **Set primario**, scegli la popolazione di transizione in entrata da mantenere."

Per configurare l’attività **Unione AND**, segui questi passaggi:

1. Aggiungi più attività, come le attività del canale, per creare almeno due rami di esecuzione diversi.
1. Aggiungi un’attività **Unione AND** a uno dei rami.
1. Nella sezione **Opzioni di unione**, seleziona tutte le attività precedenti che desideri unire.
1. Nel menu a discesa **Set primario**, scegli la popolazione di transizione in entrata da mantenere. La transizione in uscita può contenere solo una delle popolazioni di transizione in entrata.

