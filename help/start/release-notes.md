---
title: Novità nella composizione di pubblico federato di Experience Platform
description: Aggiornamenti e note sulla versione più recenti
exl-id: d4dcaf31-93cd-4a4e-888a-cf1bbdc4ca03
source-git-commit: 59d7d112421e0ff207ce76122593a111ad9c6cc7
workflow-type: tm+mt
source-wordcount: '1542'
ht-degree: 92%

---

# Note sulla versione {#rn-new}

[!DNL Federated Audience Composition] offre continuamente nuove funzioni, miglioramenti alle funzioni esistenti e correzioni di bug. In queste note sulla versione, tutte le modifiche sono consolidate. [!DNL Federated Audience Composition] è stato sviluppato in modalità nativa su [!DNL Adobe Experience Platform] e ne eredita le innovazioni e i miglioramenti più recenti. Ulteriori informazioni su queste modifiche sono disponibili nelle [Note sulla versione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=it){target="_blank"}.

## Versione del 25 luglio {#fac-25-7}

### Nuove funzionalità {#fac-25-07-feature}

<table>
<thead>
<tr>
<th><strong>Nuovo connettore - Oracle</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Il connettore Oracle è ora disponibile per l’utilizzo con Federated Audience Composition.</p>
<p>Puoi utilizzare il connettore Oracle per casi di utilizzo relativi alla creazione e all’arricchimento di tipi di pubblico.</p>
<p>Per ulteriori informazioni sulla connessione Oracle, leggere la <a href="../connections/home.md#create">panoramica delle connessioni</a>.</p>
</br>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Avvisi composizione</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi attivare gli avvisi per informazioni sulle esecuzioni riuscite e non riuscite della composizione</p>
<p>Per ulteriori informazioni sulla sottoscrizione alle notifiche per le esecuzioni della composizione, leggere la <a href="../compositions/start-monitor-composition.md#alerts">guida di avvio e monitoraggio della composizione</a>.</p>
</br>
</td>
</tr>
</tbody>
</table>

### Miglioramenti {#fac-25-07-improvements}

Questa versione include i seguenti miglioramenti:

* **Lunghezza caratteri server aumentata**

  Durante la configurazione dei database federati, è ora possibile utilizzare fino a 255 caratteri, anziché gli 80 caratteri precedenti.

## Versione di giugno 2025 {#fac-25-6}

### Miglioramenti {#fac-25-06-improvements}

Questa versione include i seguenti miglioramenti:

* **Disponibilità generale per la clientela Healthcare Shield di Adobe**

  La funzione Composizione di pubblico federato sarà disponibile per la clientela Healthcare Shield di Adobe per i casi d’uso di creazione di pubblico, arricchimento e arricchimento del profilo entro la fine di giugno.

  Ulteriori informazioni sulla privacy e la sicurezza in Composizione di pubblico federato sono disponibili nella [guida alla governance, privacy e sicurezza dei dati](/help/governance-privacy-security/home.md).

* **Controllo degli accessi a livello di oggetto**

  La funzione Composizione di pubblico federato ora supporta il controllo degli accessi a livello di oggetto per applicare le etichette di accesso alle composizioni specificate.

  Ulteriori informazioni sull’utilizzo delle etichette di accesso a livello di oggetto sono disponibili nella [guida alle composizioni](/help/compositions/gs-compositions.md).

* **Ruoli predefiniti**

  Ora è possibile utilizzare uno dei ruoli predefiniti per gestire le autorizzazioni utente per l’accesso a Composizione di pubblico federato.

  Ulteriori informazioni sui ruoli predefiniti sono disponibili nella [guida all’accesso alla composizione di pubblico federato](/help/governance-privacy-security/access-control.md).

* **Aggiornamenti incrementali nei casi d’uso dell’arricchimento del profilo**

  L’attività Salva profili ora supporta gli aggiornamenti incrementali. Con gli aggiornamenti incrementali, puoi eseguire query e aggiornare dati incrementali durante l’arricchimento dei profili con dati provenienti da data warehouse di dati esterni.

  Ulteriori informazioni sull’utilizzo dell’attività di salvataggio dei profili sono disponibili nella [guida all’attività di salvataggio dei profili](/help/compositions/activities/save-profiles.md).

## Versione di maggio 2025 {#fac-25-5}

### Nuove funzionalità {#fac-25-05-feature}

<table>
<thead>
<tr>
<th><strong>Vista area di lavoro modello dati - Disponibilità generale</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Il modello dati con vista area di lavoro è ora disponibile per tutta la clientela.</p>
<p>La vista area di lavoro per la sezione Modelli dati migliora l’esperienza consentendo la visualizzazione dei modelli di dati e dei relativi collegamenti in un layout dell’area di lavoro, insieme alla vista a tabella esistente. </p>
<p>Per ulteriori informazioni sulla vista area di lavoro, consulta la <a href="../data-management/gs-models.md">panoramica sui modelli di dati</a>.</p>
</br>
</td>
</tr>
</tbody>
</table>

### Miglioramenti {#fac-25-5-improvements}

Questa versione include i seguenti miglioramenti:

* **Controllo degli accessi basato sul ruolo**

  A partire dalla versione di maggio, [!DNL Federated Audience Composition] supporta le nuove autorizzazioni granulari per il controllo degli accessi. Gli utenti possono assegnare tali autorizzazioni ai ruoli utente per un accesso più preciso alla [!DNL Federated Audience Composition].

  Per ulteriori informazioni sulle nuove autorizzazioni, consulta la [guida all’accesso alla Composizione di pubblico federato](/help/governance-privacy-security/access-control.md).

## Versione di aprile 2025 {#fac-25-4}

### Nuove funzionalità {#fac-25-04-feature}

<table>
<thead>
<tr>
<th><strong>Vista area di lavoro modello dati (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La vista area di lavoro per la sezione Modelli dati migliora l’esperienza consentendo la visualizzazione dei modelli di dati e dei relativi collegamenti in un layout dell’area di lavoro, insieme alla vista a tabella esistente. </p>
<p>La vista area di lavoro del modello dati è attualmente disponibile in versione Beta solo per alcuni utenti.</p>
<p>Per ulteriori informazioni, consulta la <a href="../data-management/gs-models.md">documentazione dettagliata</a>.</p>
</br>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Supporto dell’Assistente IA per la conoscenza del prodotto</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>L’Assistente IA è una funzione dell’interfaccia utente che consente di accedere e comprendere i concetti di Adobe e ottenere insight operativi per l’ambiente specifico. È disponibile in diversi prodotti Adobe Experience Cloud, tra cui la composizione di pubblico federato.</p>
<p>Per ulteriori informazioni, consulta la <a href="../start/ai-assistant.md">documentazione dettagliata</a>.</p>
</br>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Attività Salva i profili</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p> La composizione di pubblico federato ora supporta il caso d’uso dell’arricchimento dei profili, consentendo alla clientela di migliorare i profili Experience Platform esistenti con i dati dei propri data warehouse esterni.
</p>
<p>Per ulteriori informazioni, consulta la <a href="../compositions/activities/save-profiles.md">documentazione dettagliata</a>.</p>
</br>
</td>
</tr>
</tbody>
</table>

### Miglioramenti {#fac-25-4-improvements}

Questa versione include i miglioramenti indicati di seguito.

* **Nome del modello dati**

  Dal menu Tipi di pubblico, la scheda **Composizioni federate** mostra ora il nome del modello dati invece dell’ID, migliorando la chiarezza e l’usabilità complessiva.

* **Pubblico**

  Il menu Tipi di pubblico ora mostra il nome o l’etichetta del modello dati selezionato quando un utente seleziona un modello dati senza tipi di pubblico associati.

* **Esportazione di tipi di pubblico di grandi dimensioni**

  La composizione di pubblico federato ora supporta l’esportazione di tipi di pubblico di grandi dimensioni, anche con file di dimensioni superiori a 1 GB.

* **Attività Salva pubblico**

  È stata aggiunta una nota all’attività **Salva pubblico**, che ricorda agli utenti di collaborare con un amministratore dati per applicare etichette di governance ai nuovi schemi e set di dati creati durante la creazione e l’arricchimento del pubblico.
  [Ulteriori informazioni sulle etichette di utilizzo dei dati](https://experienceleague.adobe.com/it/docs/experience-platform/data-governance/labels/user-guide)

### Compatibilità {#fac-25-4-compat}

* **Connessione protetta ad Amazon Redshift**

  Con questa nuova versione, la composizione di pubblico federato supporta connessioni protette di collegamento privato a database Amazon Redshift. [Ulteriori informazioni](../connections/home.md#amazon-redshift)

* **Google BigQuery**

  Con questa nuova versione, la composizione di pubblico federato supporta connessioni VPN sicure per i database Google BigQuery. [Ulteriori informazioni](../connections/home.md#google-bigquery)

## Versione di marzo 2025 {#fac-25-3}

### Miglioramenti {#fac-25-3-improvements}

Questa versione include i miglioramenti indicati di seguito.

* **Autorizzazioni di Composizione di pubblico federato**

  A partire dalla versione di marzo, [!DNL Federated Audience Composition] inizierà ad applicare l’accesso alle interfacce **Gestione dati federati** e **Composizioni federate** a chi è stata concessa l’autorizzazione **Gestisci dati federati**.

  Per continuare ad accedere all’interfaccia utente di [!DNL Federated Audience Composition], contattata il tuo amministratore per richeidere che questa autorizzazione venga aggiunta al tuo ruolo.

  Per informazioni su come assegnare questa autorizzazione, consulta la [documentazione dettagliata](/help/governance-privacy-security/access-control.md).

### Compatibilità {#fac-25-3-compat}

* **Connessione Databricks**

  Con questa nuova versione, la funzionalità Composizione di pubblico federato ora supporta la connettività con collegamento privato per le connessioni a database Databricks.
Ciò include connessioni sicure ai database Databricks ospitati su Amazon Web Services (AWS) tramite collegamento privato e a quelli ospitati su Microsoft Azure tramite VPN. [Ulteriori informazioni](../connections/home.md#databricks)

* **Supporto per clienti di CDP B2B**

  La funzionalità Composizione di pubblico federato è ora disponibile per la clientela di Customer Data Platform (CDP) Business-to-Business (B2B) per i casi d’uso con pubblico basato su persone.

* **Connessione protetta Snowflake**

  Con questa nuova versione, la funzionalità Composizione di pubblico federato supporta connessioni sicure con collegamento privato a database Snowflake ospitati in Microsoft Azure. [Ulteriori informazioni](../connections/home.md#snowflake)

## Versione di febbraio 2025 {#fac-25-2}

Questa versione include i cambiamenti elencati di seguito.

* **Supporto di Microsoft Fabric**

  È ora possibile stabilire connessioni ai database Microsoft Fabric tramite la Composizione di pubblico federato. [Ulteriori informazioni](../connections/home.md)

* **Supporto di Amazon Redshift Spectrum**

  Amazon Redshift Spectrum è ora supportato per le connessioni al database Amazon Redshift. [Ulteriori informazioni](../connections/home.md#amazon-redshift)

* **Esperienza di creazione schema avanzata**

  Il processo di creazione degli schemi è stato migliorato tramite un’interfaccia utente aggiornata, progettata per navigare in modo più intuitivo e facile. Questi miglioramenti offrono ai professionisti dei dati un modo più semplice ed efficiente per sviluppare modelli di dati. [Ulteriori informazioni](../customer/schemas.md)

* **Supporto per l’arricchimento del pubblico per Databricks**

  È ora possibile utilizzare Databricks nel flusso Leggi pubblico, abilitando l’attività per i database Databricks e consentendone l’impostazione come nuova destinazione. [Ulteriori informazioni](../connections/destinations.md)

## Versione di novembre 2024 {#fac-24-11}

### Miglioramenti {#fac-24-11-improvements}

Questa versione include il miglioramento indicato di seguito.

* **Elenco consentiti indirizzo IP**

  Ora durante l’aggiunta di un database federato nell’interfaccia utente di Adobe Experience Platform, è possibile visualizzare direttamente gli indirizzi IP associati alle istanze della composizione di pubblico federato. Questo consente di copiare e autorizzare facilmente tali IP per la connessione al database, al fine di migliorare la sicurezza e la flessibilità. [Ulteriori informazioni](../connections/home.md)

## Versione di ottobre 2024 {#fac-24-10}

>[!AVAILABILITY]
>
>Precedentemente disponibile per un set di organizzazioni (LA), la Composizione di pubblico federato di Adobe Experience Platform è ora disponibile per tutti gli utenti (GA). Questa funzionalità viene attivata in base all’offerta ed è visibile solo con le autorizzazioni associate. [Ulteriori informazioni](access-prerequisites.md)

### Compatibilità {#fac-24-10-compat}

Con questa nuova versione, la composizione di pubblico federato è ora compatibile con i sistemi elencati di seguito.

* **Supporto Databricks**

  È ora possibile stabilire connessioni ai database Databricks tramite la composizione di pubblico federato. [Ulteriori informazioni](../connections/home.md#databricks)

* **Supporto per l’accesso sicuro a Snowflake tramite AWS PrivateLink**

  È ora supportato l’accesso sicuro al data warehouse esterno di Snowflake tramite collegamento privato. Il tuo account di Snowflake deve essere ospitato su Amazon Web Services (AWS) e situato nella stessa area geografica dell’ambiente di composizione di pubblico federato. Contatta il tuo rappresentante Adobe per assistenza nella configurazione dell’accesso sicuro all’account Snowflake. [Ulteriori informazioni](../connections/home.md#snowflake)

* **Supporto serverless Amazon Redshift**

  Con questa nuova versione, la composizione di pubblico federato supporta [Amazon Redshift serverless](https://aws.amazon.com/it/redshift/redshift-serverless/){target="_blank"}.

### Miglioramenti {#fac-24-10-improvements}

Questa versione include i miglioramenti elencati di seguito.

* **Aggiornare schemi esistenti**

  Quando una colonna viene creata, modificata o eliminata in un database federato, è ora possibile rilevare e applicare le modifiche facendo clic sul pulsante **[!UICONTROL Aggiorna schema]** nello schema corrispondente. [Ulteriori informazioni](../customer/schemas.md#schema-refresh)

* **Associare un modello dati a una nuova composizione**

  Quando viene creata una composizione, è ora possibile selezionare il modello dati da associare. Con questa nuova opzione, la configurazione delle attività è più semplice in quanto sono disponibili solo le tabelle del modello dati associato. [Ulteriori informazioni](../compositions/create-composition.md)

## Versione di luglio 2024 - Composizione di pubblico federato (LA) {#fac-la}

La composizione di pubblico federato offre alle aziende un accesso flessibile ed esteso ai data warehouse aziendali per comporre tipi di pubblico utilizzando set di dati aziendali critici e fornire esperienze immediate e avviate dal brand. Con questo nuovo approccio, in qualità di utente di [Real-time Customer Data Platform di Adobe](https://experienceleague.adobe.com/it/docs/experience-platform/segmentation/home){target="_blank"} e/o [Adobe Journey Optimizer](https://experienceleague.adobe.com/it/docs/journey-optimizer/using/ajo-home){target="_blank"}, puoi raccogliere i dati di pubblico federato direttamente dal data warehouse esistente per arricchire i tipi di pubblico di Adobe Experience Platform in un unico sistema.

La composizione di pubblico federato affronta le crescenti richieste del mercato per le aziende che necessitano flessibilità per comporre i tipi di pubblico con set di dati warehouse. Questo consente alle aziende di ridurre lo spostamento dei dati, rendendo al tempo stesso disponibili ai team di marketing i dati critici sul pubblico per soddisfare i requisiti dei casi d’uso e fornire esperienze personalizzate.

Ulteriori informazioni sulle funzionalità della composizione di pubblico federato sono disponibili in [questa pagina](get-started.md) e nelle [domande frequenti](faq.md).

Per informazioni dettagliate sui prerequisiti per accedere alle composizioni di pubblico federato e ai guardrail attuali, consulta [questa pagina](access-prerequisites.md).
