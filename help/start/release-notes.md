---
title: Novità nella composizione di pubblico federato di Experience Platform
description: Aggiornamenti e note sulla versione più recenti
exl-id: d4dcaf31-93cd-4a4e-888a-cf1bbdc4ca03
source-git-commit: 81ac7595196aeff30f1d09d66779ca4392f7bb19
workflow-type: tm+mt
source-wordcount: '590'
ht-degree: 88%

---

# Note sulla versione {#rn-new}

[!DNL Federated Audience Composition] offre continuamente nuove funzioni, miglioramenti alle funzioni esistenti e correzioni di bug. In queste note sulla versione, tutte le modifiche sono consolidate. [!DNL Federated Audience Composition] è stato sviluppato in modalità nativa su [!DNL Adobe Experience Platform] e ne eredita le innovazioni e i miglioramenti più recenti. Ulteriori informazioni su queste modifiche nelle [Note sulla versione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=it){target="_blank"}.


## Aggiornamento del 25 febbraio {#fac-25-01}

A partire dalla versione di marzo, [!DNL Federated Audience Composition] inizierà ad applicare l&#39;accesso di **Federated data management** e **Federated Compositions** alle interfacce utente a cui è stata concessa l&#39;autorizzazione **Manage Federated Data**.

Si consiglia agli utenti di contattare gli amministratori per aggiungere questa autorizzazione al loro ruolo per continuare ad accedere all&#39;interfaccia utente [!DNL Federated Audience Composition].

Per informazioni su come assegnare questa autorizzazione, consulta la [documentazione dettagliata](feature-access.md).

## Versione di novembre 2024 {#fac-24-11}

### Miglioramenti {#fac-24-11-improvements}

Questa versione include il miglioramento indicato di seguito.

* **Elenco consentiti indirizzo IP**

  Ora durante l’aggiunta di un database federato nell’interfaccia utente di Adobe Experience Platform, è possibile visualizzare direttamente gli indirizzi IP associati alle istanze della composizione di pubblico federato. Questo consente di copiare e autorizzare facilmente tali IP per la connessione al database, al fine di migliorare la sicurezza e la flessibilità. [Ulteriori informazioni](../connections/connections.md)

## Versione di ottobre 2024 {#fac-24-10}

>[!AVAILABILITY]
>
>Precedentemente disponibile per un set di organizzazioni (LA), la Composizione di pubblico federato di Adobe Experience Platform è ora disponibile per tutti gli utenti (GA). Questo componente aggiuntivo viene attivato in base all’offerta ed è visibile solo con le autorizzazioni associate. [Ulteriori informazioni](access-prerequisites.md)
>

### Compatibilità {#fac-24-10-compat}

Con questa nuova versione, la composizione di pubblico federato è ora compatibile con i sistemi elencati di seguito.

* **Supporto Databricks**

  È ora possibile stabilire connessioni ai database Databricks tramite la composizione di pubblico federato. [Ulteriori informazioni](../connections/federated-db.md#databricks)

* **Supporto per l’accesso sicuro a Snowflake tramite AWS PrivateLink**

  È ora supportato l’accesso sicuro al data warehouse esterno di Snowflake tramite collegamento privato. Il tuo account di Snowflake deve essere ospitato su Amazon Web Services (AWS) e situato nella stessa area geografica dell’ambiente di composizione di pubblico federato. Contatta il tuo rappresentante Adobe per assistenza nella configurazione dell’accesso sicuro all’account Snowflake. [Ulteriori informazioni](../connections/federated-db.md#snowflake)

* **Supporto serverless Amazon Redshift**

  Con questa nuova versione, la composizione di pubblico federato supporta [Amazon Redshift serverless](https://aws.amazon.com/it/redshift/redshift-serverless/){target="_blank"}.

### Miglioramenti {#fac-24-10-improvements}

Questa versione include i miglioramenti elencati di seguito.

* **Aggiornare schemi esistenti**

  Quando una colonna viene creata, modificata o eliminata in un database federato, è ora possibile rilevare e applicare le modifiche facendo clic sul pulsante **[!UICONTROL Aggiorna schema]** nello schema corrispondente. [Ulteriori informazioni](../customer/schemas.md#schema-refresh)

* **Associare un modello dati a una nuova composizione**

  Quando viene creata una composizione, è ora possibile selezionare il modello dati da associare. Con questa nuova opzione, la configurazione delle attività è più semplice in quanto sono disponibili solo le tabelle del modello dati associato. [Ulteriori informazioni](../compositions/create-composition.md)

## Versione di luglio 2024 - Composizione di pubblico federato (LA) {#fac-la}

La composizione di pubblico federato è una funzionalità aggiuntiva che offre alle aziende un accesso flessibile e ampio ai data warehouse aziendali per comporre il pubblico utilizzando set di dati aziendali critici ed esperienze immediate e avviate dal marchio. Con questo nuovo approccio, in qualità di utente di [Adobe Real-time Customer Data Platform](https://experienceleague.adobe.com/it/docs/experience-platform/segmentation/home){target="_blank"} e/o [Adobe Journey Optimizer](https://experienceleague.adobe.com/it/docs/journey-optimizer/using/ajo-home){target="_blank"}, puoi raccogliere i set di dati direttamente dal data warehouse esistente per arricchire i tipi di pubblico di Adobe Experience Platform in un unico sistema.

La composizione di pubblico federato affronta le crescenti richieste del mercato per le aziende che necessitano della flessibilità per comporre i tipi di pubblico con set di dati warehouse. Questo consente alle aziende di ridurre lo spostamento dei dati, rendendo al tempo stesso disponibili ai team di marketing i dati critici sul pubblico per soddisfare i requisiti dei casi d’uso e fornire esperienze personalizzate. 

Ulteriori informazioni sulle funzionalità della composizione di pubblico federato sono disponibili in [questa pagina](get-started.md) e nelle [domande frequenti](faq.md).

Per informazioni dettagliate sui prerequisiti per accedere alle composizioni di pubblico federato e ai guardrail attuali, consulta [questa pagina](access-prerequisites.md).

