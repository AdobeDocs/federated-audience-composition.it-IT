---
title: Note sulla versione di Federated Audience Composition
description: Ultimi aggiornamenti e note sulla versione per Federated Audience Composition.
exl-id: d4dcaf31-93cd-4a4e-888a-cf1bbdc4ca03
source-git-commit: e82f1c237927af983a32c848cb9d45d84f9cf3fe
workflow-type: tm+mt
source-wordcount: '1279'
ht-degree: 95%

---

# Note sulla versione {#rn-new}

[!DNL Federated Audience Composition] offre continuamente nuove funzioni, miglioramenti alle funzioni esistenti e correzioni di bug. In queste note sulla versione, tutte le modifiche sono consolidate. [!DNL Federated Audience Composition] è stato sviluppato in modalità nativa su [!DNL Adobe Experience Platform] e ne eredita le innovazioni e i miglioramenti più recenti. Ulteriori informazioni su queste modifiche sono disponibili nelle [Note sulla versione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=it){target="_blank"}.

## Versione di ottobre 2025 {#fac-25-10}

### Nuove funzionalità {#fac-25-10-feature}

<!-- 
<table>
<thead>
<tr>
<th><strong>Availability for Adobe Experience Platform customers on Amazon Web Services (AWS)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now use Federated Audience Composition if your Experience Platform instance is on AWS.</p>
<p>For more information about Experience Platform on AWS, please read the <a href="https://experienceleague.adobe.com/en/docs/experience-platform/landing/multi-cloud">multi-cloud overview</a>.</p>
</br>
</td>
</tr>
</tbody>
</table> 
-->

<table>
<thead>
<tr>
<th><strong>Autenticazione OAuth per Google BigQuery e Snowflake</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi connetterti a Google BigQuery e Snowflake mediante OAuth.</p>
<p>Per ulteriori informazioni sulla creazione delle connessioni, consulta la <a href="../connections/home.md#create">panoramica delle connessioni</a>.</p>
</br>
</td>
</tr>
</tbody>
</table>

## Versione di agosto 2025 {#fac-25-8}

### Nuove funzionalità {#fac-25-08-feature}

<table>
<thead>
<tr>
<th><strong>Supporto della chiave composita nell’individuazione dello schema</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi combinare le colonne per creare una chiave composita per lo schema.</p>
<p>Per ulteriori informazioni, consulta la <a href="../data-modelling/schemas.md#create">panoramica sugli schemi</a>.</p>
</br>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Aggiunta di più unioni in un collegamento per i modelli</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi aggiungere più unioni in un unico collegamento per i modelli.</p>
<p>Per ulteriori informazioni sui modelli, consulta la <a href="../data-modelling/models.md#create">panoramica sui modelli</a>.</p>
</br>
</td>
</tr>
</tbody>
</table>

### Miglioramenti {#fac-25-8-improvements}

Questa versione include i seguenti miglioramenti:

* **È stata aggiunta la funzione `StringAgg`**

  Ora puoi sfruttare la funzione `StringAgg` per i database Amazon Redshift Spectrum quando utilizzi l’editor di espressioni.

* Funzione **`Replace`**

  La descrizione e la sintassi della funzione `Replace` sono state chiarite all’interno della documentazione.

### Compatibilità {#fac-25-8-compatibility}

* **Database Azure Synapse**

  Ora puoi connetterti in modo sicuro ai database Azure Synapse con PrivateLink o VPN. Per ulteriori informazioni, contatta l’Assistenza clienti di Adobe.

* **Database Oracle**

  Ora puoi connetterti in modo sicuro ai database di Oracle. Per ulteriori informazioni, contatta l’Assistenza clienti di Adobe.

Per ulteriori informazioni sui database supportati nella composizione di pubblico federato, consulta la [panoramica sulle connessioni](../connections/home.md).

## Versione di luglio 2025 {#fac-25-7}

### Nuove funzionalità {#fac-25-07-feature}

<table>
<thead>
<tr>
<th><strong>Nuovo connettore: Oracle</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Il connettore Oracle è ora disponibile per l’utilizzo con la composizione di pubblico federato.</p>
<p>Puoi utilizzare il connettore Oracle per casi d’uso relativi alla creazione e all’arricchimento di un pubblico.</p>
<p>Per ulteriori informazioni sulla connessione Oracle, consulta la <a href="../connections/home.md#create">panoramica delle connessioni</a>.</p>
</br>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Avvisi sulla composizione</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi iscriverti agli avvisi per informazioni sulle esecuzioni riuscite e non riuscite della composizione</p>
<p>Per ulteriori informazioni sulla sottoscrizione alle notifiche per le esecuzioni della composizione, leggere la <a href="../compositions/create-composition.md#alerts">creazione di una guida alla composizione</a>.</p>
</br>
</td>
</tr>
</tbody>
</table>

### Miglioramenti {#fac-25-07-improvements}

Questa versione include i seguenti miglioramenti:

* **Lunghezza caratteri del server aumentata**

  Durante la configurazione dei database federati, è ora possibile utilizzare fino a 255 caratteri, anziché gli 80 caratteri precedenti.

## Versione di giugno 2025 {#fac-25-6}

### Miglioramenti {#fac-25-06-improvements}

Questa versione include i seguenti miglioramenti:

* **Disponibilità generale per la clientela Healthcare Shield di Adobe**

  La funzione Composizione di pubblico federato sarà disponibile per la clientela Healthcare Shield di Adobe per i casi d’uso di creazione di pubblico, arricchimento e arricchimento del profilo entro la fine di giugno.

  Ulteriori informazioni sulla privacy e la sicurezza in Composizione di pubblico federato sono disponibili nella [guida alla governance, privacy e sicurezza dei dati](/help/governance-privacy-security/home.md).

* **Controllo degli accessi a livello di oggetto**

  La funzione Composizione di pubblico federato ora supporta il controllo degli accessi a livello di oggetto per applicare le etichette di accesso alle composizioni specificate.

  Ulteriori informazioni sull’utilizzo delle etichette di accesso a livello di oggetto sono disponibili nella [guida alle composizioni](/help/compositions/home.md).

* **Ruoli predefiniti**

  Ora è possibile utilizzare uno dei ruoli predefiniti per gestire le autorizzazioni utente per l’accesso a Composizione di pubblico federato.

  Ulteriori informazioni sui ruoli predefiniti sono disponibili nella [guida all’accesso alla composizione di pubblico federato](/help/governance-privacy-security/access-control.md).

* **Aggiornamenti incrementali nei casi d’uso dell’arricchimento del profilo**

  L’attività Salva profili ora supporta gli aggiornamenti incrementali. Con gli aggiornamenti incrementali, puoi eseguire query e aggiornare dati incrementali durante l’arricchimento dei profili con dati provenienti da data warehouse di dati esterni.

  Ulteriori informazioni sull&#39;utilizzo dell&#39;attività di salvataggio dei profili sono disponibili nella sezione [salva profilo della guida attività](/help/compositions/activities.md#save-profiles).

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
<p>Per ulteriori informazioni sulla vista area di lavoro, consulta la <a href="../data-modelling/models.md">panoramica sui modelli di dati</a>.</p>
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
<p>Per ulteriori informazioni, consulta la <a href="../data-modelling/models.md">documentazione dettagliata</a>.</p>
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
<p>L’Assistente IA è una funzione dell’interfaccia utente che consente di accedere e comprendere i concetti di Adobe e ottenere insight operativi per l’ambiente specifico. È disponibile in diversi prodotti Adobe Experience Cloud, tra cui Composizione di pubblico federato.</p>
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
<p>Per ulteriori informazioni, consulta la <a href="../compositions/activities.md#save-profiles">documentazione dettagliata</a>.</p>
</br>
</td>
</tr>
</tbody>
</table>

### Miglioramenti {#fac-25-4-improvements}

Questa versione include i seguenti miglioramenti:

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

Questa versione include i seguenti miglioramenti:

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

Questa versione include le seguenti modifiche:

* **Supporto di Microsoft Fabric**

  È ora possibile stabilire connessioni ai database Microsoft Fabric tramite la Composizione di pubblico federato. [Ulteriori informazioni](../connections/home.md)

* **Supporto di Amazon Redshift Spectrum**

  Amazon Redshift Spectrum è ora supportato per le connessioni al database Amazon Redshift. [Ulteriori informazioni](../connections/home.md#amazon-redshift)

* **Esperienza di creazione schema avanzata**

  Il processo di creazione degli schemi è stato migliorato tramite un’interfaccia utente aggiornata, progettata per navigare in modo più intuitivo e facile. Questi miglioramenti offrono ai professionisti dei dati un modo più semplice ed efficiente per sviluppare modelli di dati. [Ulteriori informazioni](../data-modelling/schemas.md)

* **Supporto per l’arricchimento del pubblico per Databricks**

  È ora possibile utilizzare Databricks nel flusso Leggi pubblico, abilitando l’attività per i database Databricks e consentendone l’impostazione come nuova destinazione. [Ulteriori informazioni](../connections/destinations.md)
