---
title: Panoramica dell’Assistente IA
description: Scopri come utilizzare l’Assistente IA, tra cui conoscenza del prodotto, insight operativi e creazione di composizioni di pubblico federato.
exl-id: f7493a57-e42d-43f9-b20a-1b9b90477a74
TQID: https://experienceleague.adobe.com/j-KXucjaZa4dNSjg5POqxh7KOSUHG5CnBkBLFA6rPVs
product_v2: id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
topic_v2: id: c1579802-ddd4-4214-8a91-97b2066abe11id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adebid: d095671a-1355-40aa-8b5f-06c33c68080bid: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: fda4d9d7b45833d7e080ae80f42b7ca5ce36b3ad
workflow-type: ht
source-wordcount: 646
ht-degree: 100%

---

# Panoramica dell’Assistente IA {#ai-assistant}

L’Assistente IA è una funzione dell’interfaccia utente progettata per aiutarti ad accedere e comprendere i concetti di Adobe. Puoi utilizzarlo per una migliore comprensione dei casi d’uso di conoscenza del prodotto in diversi prodotti di Adobe Experience Cloud, tra cui la Composizione di pubblico federato.

>[!CAUTION]
>
>Prima di poter utilizzare l’Assistente IA, devi accettare le linee guida per l’utente sull’intelligenza artificiale generativa di Adobe Experience Cloud. Ulteriori informazioni sull’accordo sono disponibili nella [panoramica dell’Assistente IA (legacy)](https://experienceleague.adobe.com/it/docs/experience-platform/ai-assistant/home){target="_blank"}.

Nella composizione di pubblico federato, puoi accedere alla conoscenza del prodotto per scoprire i concetti di Adobe riguardanti i vari aspetti del processo. L’Assistente AI supporta quattro tipi di casi d’uso: **Ricerca aperta** che esplora i concetti del prodotto in base nella documentazione di Experience League, **Apprendimento mirato e risoluzione dei problemi** (che ti consente di porre domande su caratteristiche o funzionalità specifiche), **Insight operativi** (che ti consente di porre domande sui tuoi oggetti nella composizione di pubblico federato) e **Creazione di Composizioni di pubblico federato**.

## Accesso {#access}

Per accedere all’Assistente IA, seleziona ![icona Assistente IA](/help/start/assets/ai-assistant/icon.png) nella barra superiore.L’Assistente IA viene visualizzato nella sezione a destra dello schermo. Puoi selezionare ![Approfondisci testo alternativo immagine](assets/do-not-localize/Smock_FullScreen_18_N.svg "icona Espandi") per espandere la finestra dell’Assistente IA.

![L’icona Assistente IA viene evidenziata e mostra come accedere all’Assistente AI.](/help/start/assets/ai-assistant/access.png)

## Uso dell’Assistente IA {#using}

Una volta aperto l’Assistente IA, inserisci la domanda nel campo nella parte inferiore dello schermo e premi Invio.Viene visualizzata la risposta alla domanda. Puoi utilizzare il pollice su o il pollice giù per valutare la risposta.

![Nell’Assistente IA viene visualizzata una domanda e una risposta di esempio.](/help/start/assets/ai-assistant/sample-question-answer.png)

## Domande di esempio {#sample-questions}

Le query seguenti mostrano i tipi di domande disponibili che puoi porre all’Assistente IA:

| Tipo di query | Domanda di esempio |
| ---------- | --------------- |
| Ricerca aperta | <ul><li>Che cos’è la composizione di pubblico federato?</li></ul> |
| Apprendimento mirato | <ul><li>Come si configura un account del database federato Snowflake?</li><li>Come si crea una composizione federata?</li></ul> |
| Insight operativi | <ul><li>Quanti database federati sono presenti nella mia sandbox?</li><li>Quanti schemi ho creato negli ultimi 30 giorni?</li></ul> |
| Creazione di una Composizione di pubblico federato | <ul><li>Crea un pubblico federato di clienti che vivono nel Regno Unito.</li></ul> |

Inoltre, puoi utilizzare l’Assistente IA per creare autonomamente una composizione di pubblico federato.

## Creazione di un pubblico {#create-audience}

Puoi utilizzare l’Assistente IA per creare una composizione di pubblico federato utilizzando prompt in linguaggio naturale.Quando utilizzi l’Assistente IA per creare un pubblico, l’Assistente AI elabora un piano basato sul prompt e lo esegue nel browser utilizzando l’automazione basata su IA.

Ad esempio, se chiedi all’Assistente IA &quot;Crea un pubblico federato di clienti che vivono nel Regno Unito utilizzando lo schema CUSTOMERS_Table&quot;, l’Assistente IA definisce il piano che sarà adottato per creare il pubblico, inclusi i passaggi per passare alla pagina Composizioni federate, il modo in cui l’agente crea la composizione e il salvataggio del pubblico una volta completata.

![Viene visualizzata una domanda e una risposta di esempio.](/help/start/assets/ai-assistant/ask-create.png)

Se il piano è accurato, puoi selezionare **[!UICONTROL Esegui]** per consentire all’agente di eseguire l’automazione. L’agente, all’interno del browser, esegue in modo autonomo i passaggi necessari per creare la composizione richiesta nell’interfaccia utente di Composizione di pubblico federato. Puoi interrompere l’automazione in un qualsiasi momento selezionando **[!UICONTROL Interrompi]**.

![Il piano è stato eseguito e l’agente esegue il piano in modo autonomo.](/help/start/assets/ai-assistant/execute-plan.png)

Attualmente, la funzionalità di creazione del pubblico supporta le seguenti funzioni aggiuntive:

- Modulo di pianificazione
   - Puoi creare composizioni federate che vengono eseguite in base a una pianificazione ricorrente. I valori supportati includono **Una volta** e **Giornaliera**.
- Deduplica
   - Puoi deduplicare i record di dati federati durante la riconciliazione dei dati

## Passaggi successivi

Per ulteriori informazioni sull’Assistente IA, inclusi esempi di obiettivi che puoi raggiungere con l’Assistente IA e per scoprire il funzionamento dell’Assistente IA, leggi la [Panoramica dell’Assistente IA](https://experienceleague.adobe.com/it/docs/experience-platform/ai-assistant/home){target="_blank"}.

Per un elenco completo delle domande sugli Insight operativi che puoi porre per la Composizione di pubblico federato, leggi la [sezione sugli insight operativi](https://experienceleague.adobe.com/it/docs/experience-platform/ai-assistant/home#operational-insights){target="_blank"}.
