---
audience: end-user
title: Utilizzare l’attività Attendi
description: Scopri come utilizzare l’attività Attendi
source-git-commit: e2e708a21aa0e2d1724f5ba79caf10ef803ae818
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 60%

---

# Attendere {#wait}

>[!CONTEXTUALHELP]
>id="dc_orchestration_wait"
>title="Attività Attendi"
>abstract="L’attività **Attendi** viene utilizzata per ritardare la transizione da un’attività a un’altra."

Il **Wait** Le attività consentono di passare un certo periodo di tempo tra due attività eseguite. Ad esempio, per attendere diversi giorni dopo un’attività di consegna e-mail, quindi analizzare le aperture e i clic generati durante questo periodo prima di eseguire eventuali operazioni di follow-up (e-mail di promemoria, creazione di un pubblico, ecc.).

## Configurazione{#wait-configuration}

Per configurare l’attività **Attendi**, segui questi passaggi:

1. Aggiungi un **Wait** attività nella composizione.

1. Specifica la **Durata** dell’attesa tra le transizioni in entrata e in uscita.

1. Selezionare l&#39;unità di tempo in **Periodi** campo: secondi, minuti, ore, giorni.

