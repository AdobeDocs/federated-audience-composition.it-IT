---
title: Privacy e sicurezza nella composizione di pubblico federato
description: Scopri in che modo la composizione di pubblico federato affronta la privacy e la sicurezza dei dati utente, incluse funzioni quali governance dei dati, applicazione del consenso, controllo degli accessi, crittografia dei dati e rispetto delle normative sulla privacy.
exl-id: 677e26e7-1294-4f62-a5ce-17b65e84c65e
source-git-commit: 8076a7851d0cd5cd84a7c48c6f1783b452864903
workflow-type: ht
source-wordcount: '1085'
ht-degree: 100%

---

# Privacy e sicurezza nella composizione di pubblico federato

La composizione di pubblico federato rispetta numerose pratiche di sicurezza per proteggere i dati durante l’elaborazione.

## Privacy Service {#privacy}

La composizione di pubblico federato fornisce i dati federati che Adobe Experience Platform e Adobe Journey Optimizer possono utilizzare. Tuttavia, la composizione di pubblico federato **non** memorizza i dati della clientela provenienti da uno qualsiasi dei data warehouse. Di conseguenza, puoi utilizzare Privacy Service di Adobe Experience Platform per rispettare le richieste della persona interessata e di eliminazione dei dati.

Ad esempio, quando crei un pubblico utilizzando il blocco dell’attività Salva nell’area di lavoro della composizione, il pubblico risultante viene archiviato nel data lake di Experience Platform come pubblico esterno. Questo pubblico esterno è contrassegnato con il relativo campo di identità e lo spazio dei nomi identità. Di conseguenza, puoi utilizzare Privacy Service per accedere e rimuovere tali profili con un pubblico esterno.

In alternativa, dopo aver creato un arricchimento del profilo utilizzando l’attività Salva profilo nell’area di lavoro della composizione, l’arricchimento risultante viene memorizzato in Experience Platform come schema e set di dati abilitati per il profilo. Questi dati di arricchimento sono contrassegnati con un campo di identità e uno spazio dei nomi identità. Di conseguenza, puoi utilizzare Privacy Service per accedere a questi profili e pulirli.

Per ulteriori informazioni su Privacy Service, consulta la [panoramica su Privacy Service](https://experienceleague.adobe.com/it/docs/experience-platform/privacy/home){target="_blank"}.

### Richieste di privacy {#privacy-requests}

In Privacy Service, puoi creare e gestire singole richieste di privacy di accesso ed eliminazione dei dati della clientela dalla composizione di pubblico federato. Privacy Service fornisce sia un’[interfaccia utente](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html?lang=it){target="_blank"} che un’[API RESTful](https://experienceleague.adobe.com/it/docs/experience-platform/privacy/api/overview){target="_blank"} per aiutarti a gestire le richieste di accesso ai dati della clientela.

Per ulteriori informazioni sulla creazione e sulla gestione delle richieste di privacy, consulta i [processi relativi alla privacy nella guida all’interfaccia utente di Privacy Service](https://experienceleague.adobe.com/it/docs/experience-platform/privacy/ui/user-guide){target="_blank"}.

## Applicazione dei criteri di consenso {#consent}

La composizione di pubblico federato, tramite Experience Platform, offre strumenti che consentono di automatizzare l’applicazione del consenso, garantendo l’attivazione di tipi di pubblico in base al consenso fornito alla clientela.

Ad esempio, quando crei un pubblico utilizzando il blocco dell’attività Salva nell’area di lavoro della composizione, il pubblico risultante viene archiviato nel data lake di Experience Platform come pubblico esterno. Experience Platform supporta automaticamente la convalida del consenso durante l’attivazione. Per ulteriori informazioni, consulta le [Domande frequenti sul Servizio di segmentazione](https://experienceleague.adobe.com/it/docs/experience-platform/segmentation/faq#consent){target="_blank"}.

In alternativa, dopo aver creato un arricchimento del profilo utilizzando l’attività Salva profilo nell’area di lavoro della composizione, l’arricchimento risultante viene archiviato in Experience Platform come schema e set di dati abilitati per il profilo. Per i profili esistenti, gli attributi di consenso disponibili vengono rispettati automaticamente durante l’attivazione. Per i nuovi profili, gli attributi di consenso forniti durante l’acquisizione del profilo vengono rispettati automaticamente durante l’attivazione. Per ulteriori informazioni sull’applicazione dei consensi ai profili, consulta la [guida sul gruppo di campi consensi e preferenze](https://experienceleague.adobe.com/it/docs/experience-platform/xdm/field-groups/profile/consents){target="_blank"}.

Per ulteriori informazioni sull’applicazione dei consensi, consulta la [guida all’interfaccia utente della gestione dei criteri](https://experienceleague.adobe.com/it/docs/experience-platform/data-governance/policies/user-guide#consent-policy){target="_blank"}.

## Ciclo di vita dei dati {#data-lifecycle}

Poiché la composizione di pubblico federato **non** memorizza dati della clientela provenienti da uno qualsiasi dei data warehouse, puoi utilizzare Experience Platform per gestire il ciclo di vita dei dati. Grazie alla gestione avanzata del ciclo di vita dei dati, puoi gestire il ciclo di vita dei dati sia a livello di set di dati che a livello di record.

Ad esempio, quando crei un pubblico utilizzando il blocco dell’attività Salva nell’area di lavoro della composizione, il pubblico risultante viene archiviato nel data lake in Experience Platform come pubblico esterno. Poiché questi dati **non** sono memorizzati nella composizione di pubblico federato, i dati del pubblico e i set di dati corrispondenti vengono eliminati automaticamente quando il pubblico viene eliminato in Audience Portal.

In alternativa, dopo aver creato un arricchimento del profilo utilizzando l’attività Salva profilo nell’area di lavoro della composizione, l’arricchimento risultante viene archiviato in Experience Platform come schema e set di dati abilitati per il profilo. Di conseguenza, puoi utilizzare il ciclo di vita dei dati per accedere ai profili e pulirli.

Per ulteriori informazioni sull’utilizzo del ciclo di vita dei dati, consulta la [panoramica sul ciclo di vita dei dati](https://experienceleague.adobe.com/it/docs/experience-platform/data-lifecycle/home){target="_blank"}.

## Etichette di utilizzo dei dati {#data-usage-labels}

Le etichette di utilizzo dei dati ti consentono di classificare i set di dati e campi in base ai criteri di governance applicabili a tali dati. Dopo aver creato un pubblico utilizzando le composizioni, puoi applicare le etichette dei dati appropriate allo schema risultante per garantire che rispetti le restrizioni di utilizzo richieste.

Per ulteriori informazioni sull’utilizzo delle etichette dei dati, consulta la [panoramica sulle etichette di utilizzo dei dati](https://experienceleague.adobe.com/it/docs/experience-platform/data-governance/labels/overview){target="_blank"}.

## Crittografia {#encryption}

La composizione del pubblico flessibile fornisce la crittografia attraverso la crittografia dei dati a riposo, la crittografia dei dati in transito e le chiavi gestite dalla clientela.

I dati a riposo si riferiscono ai dati della clientela utilizzati nella composizione di pubblico federato. I dati vengono crittografati dal provider del servizio cloud e utilizzati nella composizione di pubblico federato in forma crittografata.

I dati in transito si riferiscono ai dati della clientela durante lo spostamento da un componente all’altro nella composizione di pubblico federato. I dati vengono mantenuti crittografati in tutti i componenti della composizione di pubblico federato che utilizzano TLS 1.3 tramite HTTPS.

Per ulteriori informazioni su come Adobe gestisce la crittografia dei dati, consulta la guida sulla [crittografia dei dati in Experience Platform](https://experienceleague.adobe.com/it/docs/experience-platform/landing/governance-privacy-security/encryption){target="_blank"}.

### Chiavi gestite dalla clientela {#customer-managed-keys}

Le chiavi gestite dalla clientela consentono di controllare i dati, utilizzando le proprie chiavi di crittografia per crittografare i dati. Poiché la composizione di pubblico federato **non** archivia i dati della clientela, puoi utilizzare le chiavi gestite dalla clientela direttamente sui tipi di pubblico e sugli arricchimenti risultanti, poiché verranno archiviati nel data lake su Experience Platform.

Per ulteriori informazioni sulle chiavi gestite dalla clientela, consulta la [guida alle chiavi gestite dalla clientela](https://experienceleague.adobe.com/it/docs/experience-platform/landing/governance-privacy-security/customer-managed-keys/overview){target="_blank"}.

## Registro di controllo {#audit-log}

Tutte le operazioni di creazione, lettura, aggiornamento ed eliminazione eseguite nella composizione di pubblico federato vengono registrate nell’audit trail. Puoi utilizzare il registro di controllo per tracciare queste azioni, applicare la responsabilità e supportare i controlli di conformità.

Per ulteriori informazioni, consulta la [panoramica sull’audit trail](/help/admin/audit-trail.md){target="_blank"}.

## Controllo degli accessi {#access-control}

Puoi controllare l’accesso alla composizione di pubblico federato sia a livello di campo che di ruolo. Puoi utilizzare questi controlli di accesso per applicare i criteri di governance dei dati, limitare l’esposizione delle informazioni sensibili e allineare l’accesso alle responsabilità degli utenti.

Per ulteriori informazioni sul controllo degli accessi alla composizione di pubblico federato, consulta la [guida all’accesso alla composizione di pubblico federato](/help/start/feature-access.md){target="_blank"}.

## Localizzazione dei dati {#data-localization}

La composizione di pubblico federato **non** archivia i dati della clientela. Di conseguenza, devi assicurarti di collegare **solo** i database esterni con l’area geografica corrispondente della sandbox per mantenere i dati nella stessa area. Se connetti il database di un’area geografica diversa a una sandbox, Adobe **non** è responsabile della localizzazione dei dati.

## Passaggi successivi {#next-steps}

Dopo aver letto questa guida, avrai una migliore comprensione delle funzioni di privacy e sicurezza utilizzate per la composizione di pubblico federato, tra cui governance dei dati, conformità alla privacy, applicazione del consenso, gestione del ciclo di vita dei dati e controllo degli accessi.
