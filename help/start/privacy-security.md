---
title: Privacy e sicurezza nella Federated Audience Composition
description: Scopri in che modo Federated Audience Composition si occupa della privacy e della sicurezza dei dati utente, incluse funzioni quali governance dei dati, applicazione del consenso, controllo degli accessi, crittografia dei dati e conformità alla privacy.
source-git-commit: b505a4f0ac9ac7350e2879f4f54f93a69b73f96c
workflow-type: tm+mt
source-wordcount: '1085'
ht-degree: 1%

---


# Privacy e sicurezza nella Federated Audience Composition

Federated Audience Composition rispetta numerose pratiche di sicurezza per proteggere i dati durante l’elaborazione.

## Privacy Service {#privacy}

Federated Audience Composition fornisce i dati federati che Adobe Experience Platform e Adobe Journey Optimizer possono utilizzare. Tuttavia, Federated Audience Composition **non** memorizza i dati dei clienti da uno qualsiasi dei data warehouse. Di conseguenza, puoi utilizzare Adobe Experience Platform Privacy Service per rispettare le richieste dell’interessato e di cancellazione dei dati.

Ad esempio, quando crei un pubblico utilizzando il blocco dell’attività di salvataggio nell’area di lavoro della composizione, il pubblico risultante viene memorizzato nel data lake in Experience Platform come pubblico esterno. Questo pubblico esterno è contrassegnato con il relativo campo di identità e spazio dei nomi di identità. Di conseguenza, puoi utilizzare Privacy Service per accedere e rimuovere tali profili con un pubblico esterno.

In alternativa, dopo aver creato un arricchimento del profilo utilizzando l’attività salva profilo nell’area di lavoro della composizione, l’arricchimento risultante viene memorizzato in Experience Platform come schema abilitato per il profilo e set di dati abilitati per il profilo. Questi dati di arricchimento sono contrassegnati con un campo di identità e uno spazio dei nomi di identità. Di conseguenza, puoi utilizzare Privacy Service per accedere a questi profili e pulirli.

Per ulteriori informazioni su Privacy Service, leggere la [panoramica di Privacy Service](https://experienceleague.adobe.com/it/docs/experience-platform/privacy/home){target="_blank"}.

### Richieste di privacy {#privacy-requests}

In Privacy Service, puoi creare e gestire singole richieste di privacy per accedere e cancellare i dati dei clienti da Federated Audience Composition. Privacy Service fornisce sia un&#39;interfaccia utente [&#128279;](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html?lang=it)1&rbrace; che un&#39;API [RESTful](https://experienceleague.adobe.com/it/docs/experience-platform/privacy/api/overview){target="_blank"} per aiutarti a gestire le richieste di dati dei clienti.{target="_blank"}

Per ulteriori informazioni sulla creazione e la gestione delle richieste di accesso a dati personali, leggere i [processi relativi alla privacy nella guida dell&#39;interfaccia utente di Privacy Service](https://experienceleague.adobe.com/it/docs/experience-platform/privacy/ui/user-guide){target="_blank"}.

## Applicazione dei criteri di consenso {#consent}

Federated Audience Composition, tramite Experience Platform, offre strumenti che consentono di automatizzare l’applicazione del consenso, garantendo l’attivazione di tipi di pubblico in base al consenso fornito ai clienti.

Ad esempio, quando crei un pubblico utilizzando il blocco dell’attività di salvataggio nell’area di lavoro della composizione, il pubblico risultante viene memorizzato nel data lake in Experience Platform come pubblico esterno. Experience Platform supporta automaticamente la convalida del consenso durante l’attivazione. Per ulteriori informazioni, leggere le [Domande frequenti sul servizio di segmentazione](https://experienceleague.adobe.com/it/docs/experience-platform/segmentation/faq#consent){target="_blank"}.

In alternativa, dopo aver creato un arricchimento del profilo utilizzando l’attività salva profilo nell’area di lavoro della composizione, l’arricchimento risultante viene memorizzato in Experience Platform come schema abilitato per il profilo e set di dati abilitato per il profilo. Per i profili esistenti, gli attributi di consenso disponibili vengono rispettati automaticamente durante l’attivazione. Per i nuovi profili, gli attributi di consenso forniti durante l’acquisizione del profilo vengono rispettati automaticamente durante l’attivazione. Per ulteriori informazioni sull&#39;applicazione dei consensi ai profili, leggere la [guida del gruppo di campi consensi e preferenze](https://experienceleague.adobe.com/it/docs/experience-platform/xdm/field-groups/profile/consents){target="_blank"}.

Per ulteriori informazioni sull&#39;applicazione dei consensi, leggere la [guida all&#39;interfaccia utente per la gestione dei criteri](https://experienceleague.adobe.com/it/docs/experience-platform/data-governance/policies/user-guide#consent-policy){target="_blank"}.

## Ciclo di vita dei dati {#data-lifecycle}

Poiché Federated Audience Composition **non** memorizza i dati dei clienti da uno qualsiasi dei data warehouse, puoi utilizzare Experience Platform per gestire il ciclo di vita dei dati. Grazie a Advanced Data Lifecycle Management è possibile gestire il ciclo di vita dei dati sia a livello di set di dati che a livello di record.

Ad esempio, quando crei un pubblico utilizzando il blocco dell’attività di salvataggio nell’area di lavoro della composizione, il pubblico risultante viene memorizzato nel data lake in Experience Platform come pubblico esterno. Poiché questi dati sono **non** memorizzati in Federated Audience Composition, i dati del pubblico e i set di dati corrispondenti vengono eliminati automaticamente quando il pubblico viene eliminato in Audience Portal.

In alternativa, dopo aver creato un arricchimento del profilo utilizzando l’attività salva profilo nell’area di lavoro della composizione, l’arricchimento risultante viene memorizzato in Experience Platform come schema abilitato per il profilo e set di dati abilitato per il profilo. Di conseguenza, puoi eseguire il ciclo di vita dei dati per accedere ai profili e pulirli.

Per ulteriori informazioni sull&#39;utilizzo del ciclo di vita dei dati, leggere la [Panoramica del ciclo di vita dei dati](https://experienceleague.adobe.com/it/docs/experience-platform/data-lifecycle/home){target="_blank"}.

## Etichette di utilizzo dei dati {#data-usage-labels}

Le etichette di utilizzo dei dati ti consentono di categorizzare set di dati e campi in base ai criteri di governance applicabili a tali dati. Dopo aver creato un pubblico utilizzando le composizioni, puoi applicare le etichette dati appropriate allo schema risultante per garantire che rispetti le restrizioni di utilizzo richieste.

Per ulteriori informazioni sull&#39;utilizzo delle etichette dati, leggere la [panoramica delle etichette di utilizzo dati](https://experienceleague.adobe.com/it/docs/experience-platform/data-governance/labels/overview){target="_blank"}.

## Crittografia {#encryption}

La composizione flessibile del pubblico fornisce la crittografia attraverso la crittografia dei dati a riposo, la crittografia dei dati in transito e le chiavi gestite dal cliente.

I dati inattivi si riferiscono ai dati dei clienti utilizzati in Federated Audience Composition. I dati vengono crittografati dal provider del servizio cloud e utilizzati in Federated Audience Composition nella sua forma crittografata.

I dati in transito si riferiscono ai dati dei clienti durante lo spostamento da un componente all’altro in Federated Audience Composition. I dati vengono mantenuti crittografati in tutti i componenti Federated Audience Composition che utilizzano TLS 1.3 tramite HTTPS.

Per ulteriori informazioni su come Adobe gestisce la crittografia dei dati, leggere la guida sulla crittografia dei dati [in Experience Platform](https://experienceleague.adobe.com/it/docs/experience-platform/landing/governance-privacy-security/encryption){target="_blank"}.

### Chiavi gestite dal cliente {#customer-managed-keys}

Le chiavi gestite dal cliente consentono di controllare i dati, utilizzando le proprie chiavi di crittografia per crittografare i dati. Poiché Federated Audience Composition **non** memorizza i dati del cliente, puoi utilizzare le chiavi gestite dal cliente direttamente sui tipi di pubblico e sugli arricchimenti risultanti, poiché verranno memorizzati nel data lake su Experience Platform.

Per ulteriori informazioni sulle chiavi gestite dal cliente, leggere la [guida alle chiavi gestite dal cliente](https://experienceleague.adobe.com/it/docs/experience-platform/landing/governance-privacy-security/customer-managed-keys/overview){target="_blank"}.

## Registro di audit {#audit-log}

Tutte le operazioni di creazione, lettura, aggiornamento ed eliminazione eseguite in Federated Audience Composition vengono registrate nell’audit trail. Puoi utilizzare questo registro di audit per tenere traccia di queste azioni, applicare la responsabilità e supportare i controlli di conformità.

Per ulteriori informazioni, leggere la [Panoramica di Audit Trail](/help/admin/audit-trail.md){target="_blank"}.

## Controllo degli accessi {#access-control}

Puoi controllare l’accesso a Federated Audience Composition sia a livello di campo che di ruolo. Puoi utilizzare questi controlli di accesso per applicare i criteri di governance dei dati, limitare l’esposizione delle informazioni sensibili e allineare l’accesso alle responsabilità degli utenti.

Per ulteriori informazioni sul controllo degli accessi in Federated Audience Composition, leggere la [Guida all&#39;accesso in Federated Audience Composition](/help/start/feature-access.md){target="_blank"}.

## Localizzazione dei dati {#data-localization}

La Composizione del pubblico federato **non** memorizza i dati dei clienti. Di conseguenza, devi assicurarti di **solo** collegare i database esterni con l&#39;area sandbox corrispondente per mantenere i dati nella stessa area. Se connetti il database di un&#39;area diversa a una sandbox, Adobe è **non** responsabile della localizzazione dei dati.

## Passaggi successivi {#next-steps}

Dopo aver letto questa guida, avrai una migliore comprensione delle funzioni di privacy e sicurezza utilizzate per Federated Audience Composition, tra cui governance dei dati, conformità alla privacy, applicazione del consenso, gestione del ciclo di vita dei dati e controllo degli accessi.
