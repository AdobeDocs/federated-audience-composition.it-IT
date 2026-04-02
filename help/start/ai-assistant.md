---
title: Panoramica dell’Assistente AI
description: Scopri come utilizzare AI Assistant, tra cui conoscenze di prodotto, informazioni operative e creazione di composizioni di pubblico federato.
exl-id: f7493a57-e42d-43f9-b20a-1b9b90477a74
source-git-commit: 226679a38d0ad17726fd743f5df3b74879a2dd32
workflow-type: tm+mt
source-wordcount: '651'
ht-degree: 15%

---

# Panoramica dell’Assistente AI {#ai-assistant}

L’Assistente IA è una funzione dell’interfaccia utente progettata per aiutarti ad accedere e comprendere i concetti di Adobe. Puoi utilizzare l’Assistente ai per comprendere meglio i casi di utilizzo della conoscenza del prodotto in diversi prodotti in Adobe Experience Cloud, inclusa la Federated Audience Composition.

>[!CAUTION]
>
>Prima di poter utilizzare l’Assistente IA, devi accettare le linee guida per l’utente sull’intelligenza artificiale generativa di Adobe Experience Cloud. Ulteriori informazioni sul contratto nella panoramica dell&#39;[Assistente IA (legacy)](https://experienceleague.adobe.com/it/docs/experience-platform/ai-assistant/home){target="_blank"}.

Nella composizione di pubblico federato, puoi accedere alla conoscenza del prodotto per scoprire i concetti di Adobe riguardanti i vari aspetti del processo. L&#39;Assistente AI supporta quattro tipi di casi d&#39;uso: **Individuazione aperta** (esplora i concetti del prodotto in base alla documentazione di Experience League), **Apprendimento mirato e risoluzione dei problemi** (fai domande su caratteristiche o funzionalità specifiche), **Informazioni operative** (fai domande sui tuoi oggetti in Federated Audience Composition) e **Creazione di composizioni di pubblico federato**.

## Accesso {#access}

Per accedere all&#39;Assistente AI, seleziona ![l&#39;icona Assistente AI](/help/start/assets/ai-assistant/icon.png) nella barra superiore. L’Assistente IA viene visualizzato nella sezione a destra dello schermo. È possibile selezionare ![Testo alternativo immagine immersione](assets/do-not-localize/Smock_FullScreen_18_N.svg "l&#39;icona Espandi") per espandere la finestra dell&#39;Assistente AI.

![L&#39;icona Assistente IA è evidenziata e mostra come accedere all&#39;Assistente AI.](/help/start/assets/ai-assistant/access.png)

## Utilizzo dell’Assistente AI {#using}

Dopo aver aperto l’Assistente AI, inserisci la domanda nel campo nella parte inferiore dello schermo e premi Invio. Viene visualizzata la risposta alla domanda. Puoi utilizzare il pollice verso l’alto o il pollice verso il basso per valutare la risposta.

![Nell&#39;Assistente di IA viene visualizzata una domanda e una risposta di esempio.](/help/start/assets/ai-assistant/sample-question-answer.png)

## Domande di esempio {#sample-questions}

Le query seguenti mostrano i tipi di domande disponibili che è possibile porre all’Assistente IA:

| Tipo di query | Domanda di esempio |
| ---------- | --------------- |
| Rilevamento aperto | <ul><li>Che cos’è la composizione di pubblico federato?</li></ul> |
| Apprendimento mirato | <ul><li>Come configurare un account di database federato di Snowflake?</li><li>Come si crea una composizione federata?</li></ul> |
| Insight operativi | <ul><li>Quanti database federati sono presenti nella sandbox?</li><li>Quanti schemi ho creato negli ultimi 30 giorni?</li></ul> |
| Creazione di una composizione di pubblico federato | <ul><li>Crea un pubblico federato di clienti che vivono nel Regno Unito.</li></ul> |

Inoltre, puoi utilizzare l’Assistente IA per creare autonomamente una composizione di pubblico federato.

## Creazione di un pubblico {#create-audience}

È possibile utilizzare l’Assistente AI per creare una composizione di pubblico federato utilizzando prompt in linguaggio naturale. Quando utilizzi l’Assistente AI per creare un pubblico, l’Assistente AI genera un piano basato sul prompt e lo esegue nel browser utilizzando l’automazione basata sull’intelligenza artificiale.

Ad esempio, se chiedi ad AI Assistant di &quot;Creare un pubblico federato di clienti che vivono nel Regno Unito utilizzando lo schema CUSTOMERS_Table&quot;, AI Assistant definirà il piano che intraprenderà per creare il pubblico, inclusi i passaggi per passare alla pagina Composizioni federate, il modo in cui l’agente creerà la composizione e il salvataggio del pubblico una volta completata.

![Viene visualizzata una domanda e una risposta di esempio.](/help/start/assets/ai-assistant/ask-create.png)

Se il piano è accurato, è possibile selezionare **[!UICONTROL Esegui]** per consentire all&#39;agente di eseguire l&#39;automazione. L’agente, all’interno del browser, esegue in modo autonomo i passaggi necessari per creare la composizione richiesta nell’interfaccia utente di Federated Audience Composition. Se in un qualsiasi momento si desidera interrompere l&#39;automazione, selezionare **[!UICONTROL Interrompi]**.

![Il piano è stato eseguito e l&#39;agente esegue il piano in modo autonomo.](/help/start/assets/ai-assistant/execute-plan.png)

Attualmente, l’abilità di creazione del pubblico supporta le seguenti funzioni aggiuntive:

- Modulo di pianificazione
   - Puoi creare composizioni federate che vengono eseguite su una pianificazione ricorrente. I valori supportati includono **Una volta** e **Ogni giorno**.
- Deduplica
   - Puoi deduplicare i record di dati federati durante la riconciliazione dei dati

## Passaggi successivi

Per ulteriori informazioni sull&#39;Assistente di intelligenza artificiale, inclusi gli obiettivi che è possibile raggiungere con l&#39;Assistente di intelligenza artificiale e le modalità di funzionamento dell&#39;Assistente di intelligenza artificiale, leggere la [panoramica dell&#39;Assistente di intelligenza artificiale](https://experienceleague.adobe.com/it/docs/experience-platform/ai-assistant/home){target="_blank"}.

Per un elenco completo delle domande su Operational Insight da porre per Federated Audience Composition, leggi la [sezione approfondimenti operativi](https://experienceleague.adobe.com/en/docs/experience-platform/ai-assistant/home#operational-insights){target="_blank"}.
