---
title: Novità nella composizione di pubblico federato di Experience Platform
description: Aggiornamenti e note sulla versione più recenti
hide: true
hidefromtoc: true
exl-id: 23ea1a5d-a0e4-4f47-b0f8-56009bbc0a4a
source-git-commit: 5972479c87a757eb09ce74535e26427f5410f254
workflow-type: tm+mt
source-wordcount: '802'
ht-degree: 90%

---

# Note sulla versione {#rn-new}

[!DNL Federated Audience Composition] offre continuamente nuove funzioni, miglioramenti alle funzioni esistenti e correzioni di bug. In queste note sulla versione, tutte le modifiche sono consolidate. [!DNL Federated Audience Composition] è stato sviluppato in modalità nativa su [!DNL Adobe Experience Platform] e ne eredita le innovazioni e i miglioramenti più recenti. Ulteriori informazioni su queste modifiche sono disponibili nelle [Note sulla versione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=it){target="_blank"}.

## Versione di marzo 2025 {#fac-25-3}

### Miglioramenti {#fac-25-3-improvements}

Questa versione include i miglioramenti indicati di seguito.

* **Autorizzazioni di Composizione di pubblico federato**

  A partire dalla versione di marzo, [!DNL Federated Audience Composition] inizierà ad applicare l’accesso alle interfacce **Gestione dati federati** e **Composizioni federate** a chi è stata concessa l’autorizzazione **Gestisci dati federati**.

  Per continuare ad accedere all’interfaccia utente di [!DNL Federated Audience Composition], contattata il tuo amministratore per richeidere che questa autorizzazione venga aggiunta al tuo ruolo.

  Per informazioni su come assegnare questa autorizzazione, consulta la [documentazione dettagliata](feature-access.md).

<!--
* **Data model Canvas view**

    The Canvas view for the Data Models section improves the experience by enabling the visualization of data models and their links in a canvas layout, alongside the existing tabular view. [Learn more](../data-management/gs-models.md)


* **AI Assistant**

    The AI Assistant is a user interface feature designed to help you navigate and understand Adobe concepts and get operational insights for your specific environment. It is available in several products across Adobe Experience Cloud, including Federated Audience Composition. [Learn more](ai-assistant.md)
-->

### Compatibilità {#fac-25-3-compat}

* **Connessione Databricks**

  Con questa nuova versione, la funzionalità Composizione di pubblico federato ora supporta la connettività con collegamento privato per le connessioni a database Databricks.
Consente inoltre connessioni sicure ai database Databricks ospitati su Amazon Web Services (AWS). [Ulteriori informazioni](../connections/federated-db.md#databricks)

* **Supporto per clienti di CDP B2B**

  La funzionalità Composizione di pubblico federato è ora disponibile per la clientela di Customer Data Platform (CDP) Business-to-Business (B2B) per i casi d’uso con pubblico basato su persone.

* **Connessione protetta Snowflake**

  Con questa nuova versione, la funzionalità Composizione di pubblico federato supporta connessioni sicure con collegamento privato a database Snowflake ospitati in Microsoft Azure. [Ulteriori informazioni](../connections/federated-db.md#snowflake)

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
>Precedentemente disponibile per un set di organizzazioni (LA), la Composizione di pubblico federato di Adobe Experience Platform è ora disponibile per tutti gli utenti (GA). Questa funzionalità viene attivata in base all’offerta ed è visibile solo con le autorizzazioni associate. [Ulteriori informazioni](access-prerequisites.md)
>

### Compatibilità {#fac-24-10-compat}

Con questa nuova versione, la composizione di pubblico federato è ora compatibile con i sistemi elencati di seguito.

* **Supporto Databricks**

  È ora possibile stabilire connessioni ai database Databricks tramite la composizione di pubblico federato. [Ulteriori informazioni](../connections/federated-db.md#databricks)

* **Supporto per l’accesso sicuro a Snowflake tramite AWS PrivateLink**

  È ora supportato l’accesso sicuro al data warehouse esterno di Snowflake tramite collegamento privato. Il tuo account di Snowflake deve essere ospitato su Amazon Web Services (AWS) e situato nella stessa area geografica dell’ambiente di composizione di pubblico federato. Contatta il tuo rappresentante Adobe per assistenza nella configurazione dell’accesso sicuro all’account Snowflake. [Ulteriori informazioni](../connections/federated-db.md#snowflake)

* **Supporto serverless Amazon Redshift**

  Con questa nuova versione, Federated Audience Composition supporta [Amazon Redshift Serverless](https://aws.amazon.com/it/redshift/redshift-serverless/){target="_blank"}.

### Miglioramenti {#fac-24-10-improvements}

Questa versione include i miglioramenti elencati di seguito.

* **Aggiornare schemi esistenti**

  Quando una colonna viene creata, modificata o eliminata in un database federato, è ora possibile rilevare e applicare le modifiche facendo clic sul pulsante **[!UICONTROL Aggiorna schema]** nello schema corrispondente. [Ulteriori informazioni](../customer/schemas.md#schema-refresh)

* **Associare un modello dati a una nuova composizione**

  Quando viene creata una composizione, è ora possibile selezionare il modello dati da associare. Con questa nuova opzione, la configurazione delle attività è più semplice in quanto sono disponibili solo le tabelle del modello dati associato. [Ulteriori informazioni](../compositions/create-composition.md)

## Versione di luglio 2024 - Composizione di pubblico federato (LA) {#fac-la}

La composizione di pubblico federato offre alle aziende un accesso flessibile ed esteso ai data warehouse aziendali per comporre tipi di pubblico utilizzando set di dati aziendali critici e fornire esperienze immediate e avviate dal brand. Con questo nuovo approccio, in qualità di utente di [Adobe Real-Time Customer Data Platform](https://experienceleague.adobe.com/it/docs/experience-platform/segmentation/home){target="_blank"} e/o [Adobe Journey Optimizer](https://experienceleague.adobe.com/it/docs/journey-optimizer/using/ajo-home){target="_blank"}, puoi federare i dati del pubblico direttamente dal data warehouse esistente per arricchire i tipi di pubblico di Adobe Experience Platform in un unico sistema.

La composizione di pubblico federato affronta le crescenti richieste del mercato per le aziende che necessitano flessibilità per comporre i tipi di pubblico con set di dati warehouse. Questo consente alle aziende di ridurre lo spostamento dei dati, rendendo al tempo stesso disponibili ai team di marketing i dati critici sul pubblico per soddisfare i requisiti dei casi d’uso e fornire esperienze personalizzate.

Ulteriori informazioni sulle funzionalità di Federated Audience Composition in [questa pagina](get-started.md) e nelle [domande frequenti](faq.md).

Per informazioni dettagliate sui prerequisiti per accedere alle composizioni di pubblico federato e ai guardrail attuali, consulta [questa pagina](access-prerequisites.md).
