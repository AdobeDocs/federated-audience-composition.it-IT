---
title: Novità nella composizione di pubblico federato di Experience Platform
description: Ultimi aggiornamenti e note sulla versione
badge: label="Disponibilità limitata" type="Informative"
exl-id: d4dcaf31-93cd-4a4e-888a-cf1bbdc4ca03
source-git-commit: 61a70f9de0a6cf171a2ff1128b57ae6206be842c
workflow-type: tm+mt
source-wordcount: '442'
ht-degree: 53%

---

# Note sulla versione {#rn-new}

[!DNL Federated Audience Composition] offre continuamente nuove funzioni, miglioramenti alle funzioni esistenti e correzioni di bug. Tutte le modifiche sono consolidate in queste note sulla versione. [!DNL Federated Audience Composition] è stato sviluppato in modalità nativa su [!DNL Adobe Experience Platform] e ne eredita le innovazioni e i miglioramenti più recenti. Ulteriori informazioni su queste modifiche nelle [Note sulla versione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=it){target="_blank"}.

## Versione di ottobre 2024 {#fac-24-10}

### Compatibilità {#fac-24-10-compat}

Con questa nuova versione, Federated Audience Composition è ora compatibile con i sistemi elencati di seguito.

* **Supporto di database**

  È ora possibile stabilire connessioni ai database delle banche dati tramite Federated Audience Composition. [Ulteriori informazioni](../connections/federated-db.md#databricks)

* **Supporto per l&#39;accesso sicuro al Snowflake tramite AWS PrivateLink**

  È ora supportato l’accesso sicuro al data warehouse di Snowflake esterno tramite collegamento privato. Il tuo account di Snowflake deve essere ospitato su Amazon Web Services (AWS) e si trova nella stessa area dell’ambiente Federated Audience Composition. Contatta il tuo rappresentante Adobe per assistenza nella configurazione dell’accesso sicuro al tuo account di Snowflake. [Ulteriori informazioni](../connections/federated-db.md#snowflake)

* **Supporto Amazon Redshift Serverless**

  Con questa nuova versione, Federated Audience Composition supporta [Amazon Redshift Serverless](https://aws.amazon.com/redshift/redshift-serverless/){target="_blank"}.

### Miglioramenti {#fac-24-10-improvements}

Questa versione include i miglioramenti elencati di seguito.

* **Aggiorna schemi esistenti**

  Quando una colonna viene creata, modificata o eliminata in un database federato, è ora possibile rilevare e applicare le modifiche facendo clic sul pulsante **[!UICONTROL Aggiorna schema]** nello schema corrispondente. [Ulteriori informazioni](../customer/schemas.md#schema-refresh)

* **Associare un modello dati a una nuova composizione**

  Durante la creazione di una composizione, è ora possibile selezionare il modello dati da associare. Con questa nuova opzione, la configurazione delle attività è più semplice in quanto sono disponibili solo tabelle del modello dati associato. [Ulteriori informazioni](../compositions/create-composition.md)

## Versione del 24 luglio - Federated Audience Composition (LA) {#fac-la}

>[!AVAILABILITY]
>
>La composizione di pubblico federato è attualmente disponibile solo per un set di organizzazioni (disponibilità limitata).
>

La composizione di pubblico federato è una funzionalità aggiuntiva che offre alle aziende un accesso flessibile e ampio ai data warehouse aziendali per comporre il pubblico utilizzando set di dati aziendali critici ed esperienze immediate e avviate dal marchio. Con questo nuovo approccio, in qualità di utente di [Adobe Real-time Customer Data Platform](https://experienceleague.adobe.com/it/docs/experience-platform/segmentation/home){target="_blank"} e/o [Adobe Journey Optimizer](https://experienceleague.adobe.com/it/docs/journey-optimizer/using/ajo-home){target="_blank"}, puoi raccogliere i set di dati direttamente dal data warehouse esistente per arricchire i tipi di pubblico di Adobe Experience Platform in un unico sistema.

La composizione di pubblico federato affronta le crescenti richieste del mercato per le aziende che necessitano della flessibilità per comporre i tipi di pubblico con set di dati warehouse. Questo consente alle aziende di ridurre lo spostamento dei dati, rendendo al tempo stesso disponibili ai team di marketing i dati critici sul pubblico per soddisfare i requisiti dei casi d’uso e fornire esperienze personalizzate. 

Ulteriori informazioni sulle funzionalità della composizione di pubblico federato sono disponibili in [questa pagina](get-started.md) e nelle [domande frequenti](faq.md).

Per informazioni dettagliate sui prerequisiti per accedere alle composizioni di pubblico federato e ai guardrail attuali, consulta [questa pagina](access-prerequisites.md).

