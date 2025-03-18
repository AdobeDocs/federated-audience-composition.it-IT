---
title: Novità nella composizione di pubblico federato di Experience Platform
description: Aggiornamenti e note sulla versione più recenti
hide: true
hidefromtoc: true
source-git-commit: 59959bf01321d8062d345e1ec89538e5904a03cd
workflow-type: tm+mt
source-wordcount: '857'
ht-degree: 68%

---

# Note sulla versione {#rn-new}

[!DNL Federated Audience Composition] offre continuamente nuove funzioni, miglioramenti alle funzioni esistenti e correzioni di bug. In queste note sulla versione, tutte le modifiche sono consolidate. [!DNL Federated Audience Composition] è stato sviluppato in modalità nativa su [!DNL Adobe Experience Platform] e ne eredita le innovazioni e i miglioramenti più recenti. Ulteriori informazioni su queste modifiche nelle [Note sulla versione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=it){target="_blank"}.

## Versione di marzo 2025 {#fac-25-3}

### Miglioramenti {#fac-25-3-improvements}

Questa versione include i miglioramenti riportati di seguito.

* **Autorizzazioni di Federated Audience Composition**

  A partire dalla versione di marzo, [!DNL Federated Audience Composition] inizierà ad applicare l&#39;accesso di **Federated data management** e **Federated Compositions** alle interfacce utente a cui è stata concessa l&#39;autorizzazione **Manage Federated Data**.

  Si consiglia agli utenti di contattare gli amministratori per aggiungere questa autorizzazione al loro ruolo per continuare ad accedere all&#39;interfaccia utente [!DNL Federated Audience Composition].

  Per informazioni su come assegnare questa autorizzazione, consulta la [documentazione dettagliata](feature-access.md).

* **Visualizzazione area di lavoro modello dati**

  La visualizzazione Area di lavoro per la sezione Modelli di dati migliora l’esperienza consentendo la visualizzazione dei modelli di dati e dei relativi collegamenti in un layout di area di lavoro, insieme alla visualizzazione tabulare esistente. [Ulteriori informazioni](../data-management/gs-models.md)

* **Esportazione pubblico**

  Federated Audience Composition ora supporta l’esportazione di tipi di pubblico di grandi dimensioni, gestendo file di dimensioni fino a 20 GB.

### Compatibilità {#fac-25-3-compat}

* **Connessione a database**

  Con questa nuova versione, Federated Audience Composition ora supporta la connettività di collegamento privato per le connessioni al database Databricks.
Consente inoltre connessioni sicure ai database Database ospitati su Amazon Web Services (AWS) e Azure. [Ulteriori informazioni](../connections/federated-db.md#databricks)

* **Supporto per clienti CDP B2B**

  La Federated Audience Composition è ora disponibile per i clienti di Business-to-Business (B2B) Customer Data Platform (CDP) per i casi di utilizzo di pubblico basati sulle persone.

* **Connessione protetta Snowflake**

  Con questa nuova versione, Federated Audience Composition supporta connessioni sicure di collegamenti privati ai database di Snowflake in hosting su Azure. [Ulteriori informazioni](../connections/federated-db.md#snowflake)

## Versione di febbraio 2025 {#fac-25-2}

Questa versione include i cambiamenti elencati di seguito.

* **Supporto di Microsoft Fabric**

  È ora possibile stabilire connessioni ai database Microsoft Fabric tramite la Composizione di pubblico federato. [Ulteriori informazioni](../connections/federated-db.md)

* **Supporto di Amazon Redshift Spectrum**

  Amazon Redshift Spectrum è ora supportato per le connessioni al database Amazon Redshift. [Ulteriori informazioni](../connections/federated-db.md#amazon-redshift)

* **Esperienza di creazione schema avanzata**

  Il processo di creazione degli schemi è stato migliorato tramite un’interfaccia utente aggiornata, progettata per navigare in modo più intuitivo e facile. Questi miglioramenti offrono ai professionisti dei dati un modo più semplice ed efficiente per sviluppare modelli di dati. [Ulteriori informazioni](../customer/schemas.md)

* **Supporto per l’arricchimento del pubblico per Databricks**

  È ora possibile utilizzare Databricks nel flusso Leggi pubblico, abilitando l’attività per i database Databricks e consentendone l’impostazione come nuova destinazione. [Ulteriori informazioni](../connections/destinations.md)

## Versione di novembre 2024 {#fac-24-11}

### Miglioramenti {#fac-24-11-improvements}

Questa versione include il miglioramento indicato di seguito.

* **Elenco consentiti indirizzo IP**

  Ora durante l’aggiunta di un database federato nell’interfaccia utente di Adobe Experience Platform, è possibile visualizzare direttamente gli indirizzi IP associati alle istanze della composizione di pubblico federato. Questo consente di copiare e autorizzare facilmente tali IP per la connessione al database, al fine di migliorare la sicurezza e la flessibilità. [Ulteriori informazioni](../connections/connections.md)

## Versione di ottobre 2024 {#fac-24-10}

>[!AVAILABILITY]
>
>Precedentemente disponibile per un set di organizzazioni (LA), la Composizione di pubblico federato di Adobe Experience Platform è ora disponibile per tutti gli utenti (GA). Questa funzionalità viene attivata in base all’offerta e visibile solo con le autorizzazioni associate. [Ulteriori informazioni](access-prerequisites.md)
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

Federated Audience Composition offre alle aziende un accesso flessibile e esteso ai data warehouse aziendali per comporre il pubblico utilizzando set di dati aziendali critici e fornire esperienze immediate e avviate dal marchio. Con questo nuovo approccio, in qualità di utente di [Adobe Real-time Customer Data Platform](https://experienceleague.adobe.com/it/docs/experience-platform/segmentation/home){target="_blank"} e/o [Adobe Journey Optimizer](https://experienceleague.adobe.com/it/docs/journey-optimizer/using/ajo-home){target="_blank"}, puoi raccogliere i set di dati direttamente dal data warehouse esistente per arricchire i tipi di pubblico di Adobe Experience Platform in un unico sistema.

La Federated Audience Composition soddisfa le crescenti richieste del mercato per le aziende che necessitano della flessibilità per comporre i tipi di pubblico con set di dati di magazzino. Questo consente alle aziende di ridurre lo spostamento dei dati, rendendo al tempo stesso disponibili ai team di marketing i dati critici sul pubblico per soddisfare i requisiti dei casi d’uso e fornire esperienze personalizzate.

Ulteriori informazioni sulle funzionalità della composizione di pubblico federato sono disponibili in [questa pagina](get-started.md) e nelle [domande frequenti](faq.md).

Per informazioni dettagliate sui prerequisiti per accedere alle composizioni di pubblico federato e ai guardrail attuali, consulta [questa pagina](access-prerequisites.md).


