---
audience: end-user
title: Panoramica delle attività
description: Scopri le diverse attività e transizioni disponibili per l’utilizzo in Federated Audience Composition.
source-git-commit: 8e6bd50191afa2bdeb420186d9eb65347f063bb9
workflow-type: tm+mt
source-wordcount: '4662'
ht-degree: 33%

---

# Panoramica delle attività

In Federated Audience Composition, puoi aggiungere attività e transizioni che aiutano a definire il pubblico.

## Attività {#activities}

Le attività ti consentono di definire i componenti all’interno del pubblico.

Esistono **due** tipi diversi di attività da utilizzare in Federated Audience Composition: attività di targeting e attività di controllo del flusso.

### Attività di targeting {#targeting}

Le attività di targeting ti consentono di definire cosa costituisce il pubblico per la composizione.

#### Crea pubblico {#build-audience}

>[!CONTEXTUALHELP]
>id="dc_orchestration_build_audience_audienceselector"
>title="Pubblico"
>abstract="Seleziona il pubblico."

L&#39;attività **Genera pubblico** ti consente di definire la popolazione target per la composizione. Puoi selezionare un pubblico esistente o utilizzare il query modeler per definire una query personalizzata.

+++ Dettagli configurazione

Dopo aver aggiunto l&#39;attività **Genera pubblico** all&#39;area di lavoro della composizione, assegna un nome al pubblico. Ora puoi specificare se desideri creare un pubblico o utilizzarne uno esistente.

>[!BEGINTABS]

>[!TAB Crea nuovo pubblico]

Dopo aver selezionato **Crea pubblico**, scegli lo **schema** per il pubblico. Lo schema consente di definire la popolazione target dell’operazione, ad esempio destinatari, beneficiari del contratto, operatori o abbonati. Per impostazione predefinita, lo schema viene selezionato dai destinatari.

![](./assets/activities/build-audience-create.png)

Dopo aver scelto uno schema, seleziona **Continua**. Ora puoi definire la definizione del pubblico all’interno di Query Modeler. Per ulteriori informazioni sull&#39;utilizzo di Query Modeler, leggere la [Panoramica di Query Modeler](../query/home.md).

>[!TAB Utilizza pubblico esistente]

Dopo aver selezionato **Read audience**, scegli **Continua**.

![](./assets/activities/build-audience-read.png)

Ora puoi selezionare il pubblico da utilizzare per la composizione.

>[!ENDTABS]

Dopo aver selezionato le opzioni, puoi scegliere di **generare una transizione in uscita**. Selezionando questa opzione puoi aggiungere una transizione in uscita che verrà attivata alla fine dell’esecuzione dell’attività se la popolazione del pubblico è vuota.

+++

#### Modificare l’origine dati {#change-data-source}

L&#39;attività **Modifica origine dati** consente di modificare l&#39;origine dati utilizzata dalla composizione.

+++ Dettagli configurazione

Dopo aver aggiunto l&#39;attività **Modifica origine dati** all&#39;area di lavoro della composizione, è possibile definire l&#39;origine dati che verrà utilizzata per la composizione.

![L&#39;opzione dell&#39;origine dati è evidenziata nell&#39;area di lavoro Federated Audience Composition.](./assets/activities/configure.png){zoomable="yes"}{width="70%"}

| Origine | Descrizione |
| ------ | ----------- |
| Account esterno FDA | Un database cloud esterno connesso a Federated Audience Composition. |

Dopo aver selezionato **[!UICONTROL l&#39;account esterno FDA]**, puoi scegliere con quale account esterno connetterti.

![Viene visualizzato il popover con le opzioni dell&#39;account esterno.](./assets/activities/fda-external-account.png){zoomable="yes"}{width="70%"}

+++

#### Cambia dimensione {#change-dimension}

>[!CONTEXTUALHELP]
>id="dc_orchestration_dimension_complement"
>title="Generare un complemento"
>abstract="Puoi generare una transizione in uscita aggiuntiva con la popolazione rimanente, che è stata esclusa come duplicato. A tale scopo, attiva l’opzione **[!UICONTROL Genera complemento]**"

>[!CONTEXTUALHELP]
>id="dc_orchestration_change_dimension"
>title="Attività Cambia dimensione"
>abstract="Questa attività consente di modificare lo schema, noto anche come dimensione targeting durante la creazione di un pubblico. Sposta l’asse in base al modello di dati e alla schema di input. Ad esempio, puoi passare dallo schema “contratti” allo schema “clienti”."

L&#39;attività **Modifica dimensione** consente di modificare lo schema (noto anche come dimensione di targeting) della composizione.

+++ Dettagli configurazione

Dopo aver aggiunto l&#39;attività **Modifica dimensione** all&#39;area di lavoro della composizione, puoi definire un nuovo schema che sostituirà quello precedente. Durante questa modifica dello schema, tutti i record verranno conservati.

![](./assets/activities/change-dimension.png)

Dopo aver eseguito la composizione, i risultati verranno aggiornati.

+++

#### Combina {#combine}

>[!CONTEXTUALHELP]
>id="dc_orchestration_combine"
>title="Attività Combina"
>abstract="L’attività **Combina** consente di eseguire la segmentazione sulla popolazione in entrata. Puoi quindi combinare più popolazioni, escluderne una parte o mantenere i dati comuni a più target."

>[!CONTEXTUALHELP]
>id="dc_orchestration_intersection_merging_options"
>title="Opzioni di unione per Intersezione"
>abstract="L’attività **Intersezione** consente di mantenere solo gli elementi comuni alle diverse popolazioni in entrata all’interno dell’attività. Nella sezione **Set da unire**, seleziona tutte le attività precedenti che desideri unire."

>[!CONTEXTUALHELP]
>id="dc_orchestration_exclusion_merging_options"
>title="Opzioni di unione per Esclusione"
>abstract="La **esclusione** ti consente di escludere elementi da una popolazione in base a determinati criteri. Nella sezione **Set da unire**, seleziona tutte le attività precedenti che desideri unire."

>[!CONTEXTUALHELP]
>id="dc_orchestration_combine_options"
>title="Selezionare il tipo di segmentazione"
>abstract="Seleziona la modalità di combinazione dei tipi di pubblico: unione, intersezione o esclusione."

>[!CONTEXTUALHELP]
>id="dc_orchestration_intersection_reconciliation_options"
>title="Opzioni di riconciliazione dell’intersezione"
>abstract="Seleziona il tipo di riconciliazione per definire la modalità di gestione dei duplicati."

>[!CONTEXTUALHELP]
>id="dc_orchestration_combine_reconciliation"
>title="Opzioni di riconciliazione"
>abstract="Seleziona il **Tipo di riconciliazione** per definire la modalità di gestione dei duplicati."

>[!CONTEXTUALHELP]
>id="dc_orchestration_exclusion_options"
>title="Regole di esclusione"
>abstract="Se necessario, è possibile elaborare le tabelle in entrata. In effetti per escludere un target da un altro schema, noto anche come dimensione targeting, tale target deve essere restituito nello stesso schema del target principale. A tale scopo, selezionare **Aggiungi una regola** nella sezione E **regole di esclusione** e specificare le condizioni per la modifica dello schema. La riconciliazione dei dati viene eseguita tramite un attributo o un’unione."

>[!CONTEXTUALHELP]
>id="dc_orchestration_combine_sets"
>title="Selezionare i set da combinare"
>abstract="Nella sezione **Set da unire**, dalle transizioni in entrata, seleziona **Set primario**. Questo è il set da cui gli elementi sono esclusi. Gli altri set confrontano gli elementi prima che vengano esclusi dal set primario."

>[!CONTEXTUALHELP]
>id="dc_orchestration_combine_exclusion"
>title="Regole di esclusione"
>abstract="Se necessario, è possibile elaborare le tabelle in entrata. In effetti per escludere un target da un altro schema, noto anche come dimensione targeting, tale target deve essere restituito nello stesso schema del target principale. A tale scopo, selezionare **Aggiungi una regola** nella sezione **Regole di esclusione** e specificare le condizioni per la modifica dello schema. La riconciliazione dei dati viene eseguita tramite un attributo o un’unione."

>[!CONTEXTUALHELP]
>id="dc_orchestration_combine_complement"
>title="Complemento generato da combinazione"
>abstract="Attiva l’opzione **Genera complemento** per elaborare la popolazione rimanente in una transizione aggiuntiva."

>[!NOTE]
>
>L&#39;attività **Combine** **must** deve essere inserita dopo un&#39;altra attività e **impossibile** all&#39;inizio della composizione.

L&#39;attività **Combina** ti consente di unire più tipi di pubblico in vari modi: un&#39;unione, un&#39;intersezione o un&#39;esclusione.

- **Unione**: un&#39;unione combina i diversi tipi di pubblico in un unico pubblico. Equivale a un&#39;operazione OR.
- **Intersezione**: un&#39;intersezione combina i diversi tipi di pubblico in un unico pubblico mantenendo solo il contenuto **condiviso**. Equivale a un&#39;operazione AND.
- **Esclusione**: un&#39;esclusione combina i diversi tipi di pubblico in un unico pubblico senza le regole di esclusione specificate. Equivale a un&#39;operazione XOR.

+++ Dettagli configurazione

Dopo aver aggiunto più attività per formare almeno **due** rami diversi, aggiungi l&#39;attività **Combina** alla fine di uno dei rami. Ora puoi scegliere una delle opzioni di combinazione: Unione, Intersezione o Esclusione.

![](./assets/activities/combine.png)

>[!BEGINTABS]

>[!TAB Unione]

![](./assets/activities/combine-union.png)

Se selezioni **Unione**, dovrai scegliere il **tipo di riconciliazione** per l&#39;attività di combinazione. Il tipo di riconciliazione consente di definire la modalità di gestione delle voci duplicate.

- **Solo chiavi**: se selezioni **Solo chiavi** manterrà **un elemento** quando più elementi hanno la stessa chiave. Puoi utilizzare questa opzione solo se le popolazioni in arrivo sono omogenee.
- **Selezione di colonne**: la selezione di **Selezione di colonne** consente di definire un elenco di colonne alle quali viene applicata la riconciliazione dei dati. È possibile selezionare il set principale di dati contenente i dati di origine, seguito dalle colonne da utilizzare per il join.

>[!TAB Intersezione]

![](./assets/activities/combine-intersection.png)

Se selezioni **Intersection**, dovrai scegliere il **Tipo di riconciliazione** per l&#39;attività di combinazione. Il tipo di riconciliazione consente di definire la modalità di gestione delle voci duplicate.

- **Solo chiavi**: se selezioni **Solo chiavi** manterrà **un elemento** quando più elementi hanno la stessa chiave. Puoi utilizzare questa opzione solo se le popolazioni in arrivo sono omogenee.
- **Selezione di colonne**: la selezione di **Selezione di colonne** consente di definire un elenco di colonne alle quali viene applicata la riconciliazione dei dati.

Dopo aver configurato il tipo di riconciliazione, puoi anche selezionare l&#39;opzione **Genera complemento**. La generazione di un complemento elabora il gruppo rimanente e contiene i dati **non** inclusi nell&#39;intersezione. All’attività verrà aggiunta un’ulteriore transizione in uscita.

>[!TAB Exclusion]

![](./assets/activities/combine-exclusion.png)

Se selezioni **Esclusione**, dovrai selezionare il **Set principale** dalle transizioni in entrata. Rappresenta i set da cui gli elementi verranno esclusi.

Dopo aver scelto il set principale, puoi impostare le **regole di esclusione**. È possibile selezionare **Corrispondenza per attributo** o **Partecipa**.

Dopo aver configurato le regole di esclusione, puoi anche selezionare l&#39;opzione **Genera complemento**. La generazione di un complemento elabora la popolazione rimanente e contiene i dati **non** inclusi nell&#39;esclusione. All’attività verrà aggiunta un’ulteriore transizione in uscita.

+++

#### Deduplica {#deduplication}

>[!CONTEXTUALHELP]
>id="dc_orchestration_deduplication_fields"
>title="Campi per identificare i duplicati"
>abstract="Nella sezione **[!UICONTROL Campi per identificare i duplicati]**, selezionare il pulsante **[!UICONTROL Aggiungi attributo]** per specificare i campi per i quali i valori identici consentono l&#39;identificazione dei duplicati, ad esempio: indirizzo e-mail, nome, cognome e così via. L’ordine dei campi consente di specificare quali elaborare per primi."

>[!CONTEXTUALHELP]
>id="dc_orchestration_deduplication"
>title="Attività Deduplica"
>abstract="L’attività **Deduplica** consente di eliminare i duplicati nei risultati delle attività in entrata. Viene utilizzato principalmente dopo le attività di targeting e prima delle attività che consentono l’utilizzo di dati mirati."

>[!CONTEXTUALHELP]
>id="dc_orchestration_deduplication_complement"
>title="Generare un complemento"
>abstract="Puoi generare una transizione in uscita aggiuntiva con la popolazione rimanente, che è stata esclusa come duplicato. A tale scopo, attiva l’opzione **[!UICONTROL Genera complemento]**"

>[!CONTEXTUALHELP]
>id="dc_orchestration_deduplication_settings"
>title="Impostazioni di deduplica"
>abstract="Per eliminare i duplicati nei dati in arrivo, definisci il metodo di deduplica nei campi seguenti. Per impostazione predefinita, viene mantenuto un solo record. Devi anche selezionare la modalità di deduplica in base a un’espressione o a un attributo. Per impostazione predefinita, il record da escludere dai duplicati viene selezionato in modo casuale."

L&#39;attività **Deduplication** rimuove eventuali risultati duplicati all&#39;interno del pubblico.

+++ Dettagli configurazione

>[!NOTE]
>
>Se hai più transizioni in entrata, devi innanzitutto selezionare il **set principale** dal menu a discesa.

Dopo aver aggiunto un&#39;attività di **deduplicazione**, puoi scegliere i campi per identificare i duplicati. Seleziona **Aggiungi attributo** per identificare i campi in cui possono verificarsi duplicati.

![](./assets/activities/deduplication.png)

Dopo aver identificato i campi, puoi configurare le impostazioni di deduplicazione.

| Impostazione | Descrizione |
| ------- | ----------- |
| Duplicati da mantenere | Numero di record duplicati da mantenere. Se il valore è impostato su 0, verranno conservati **tutti** record duplicati. |
| Metodo di deduplicazione | Metodo per rimuovere i record duplicati. <ul><li>**Selezione casuale**: il record rimosso è scelto in modo casuale.</li><li>**Utilizzo di un&#39;espressione**: il record rimosso è basato sull&#39;espressione inviata. Puoi ordinare in ordine crescente o decrescente, a seconda dei valori che desideri rimuovere.</li><li>**Valori non vuoti**: il record rimosso è basato sull&#39;espressione inviata. I record in cui l’espressione non ha un valore verranno rimossi.</li><li>**Segue un elenco di valori**: il record rimosso è basato sul campo o sull&#39;espressione inviati. È possibile ordinare i valori rimanenti in modo casuale, in ordine crescente o decrescente.</li></ul> |

È inoltre possibile selezionare l&#39;opzione **Genera complemento**. La generazione di un complemento elabora la popolazione rimanente e contiene i dati **non** inclusi nella deduplicazione. All’attività verrà aggiunta un’ulteriore transizione in uscita.

+++

#### Arricchimento {#enrichment}

>[!CONTEXTUALHELP]
>id="dc_orchestration_enrichment"
>title="Attività Arricchimento"
>abstract="L’attività di **Arricchimento** consente di migliorare i dati mirati con informazioni aggiuntive provenienti dal database. Viene comunemente utilizzata in una composizione dopo le attività di segmentazione."

>[!CONTEXTUALHELP]
>id="dc_orchestration_enrichment_data"
>title="Attività Arricchimento"
>abstract="Una volta aggiunti i dati di arricchimento alla composizione, questi possono essere utilizzati nelle attività aggiunte dopo quella **Arricchimento** per segmentare i profili in gruppi distinti in base a comportamenti, preferenze e scelte."

>[!CONTEXTUALHELP]
>id="dc_orchestration_enrichment_simplejoin"
>title="Definizione dei collegamenti"
>abstract="Creare un collegamento tra i dati della tabella di lavoro e il database federato."

>[!CONTEXTUALHELP]
>id="dc_orchestration_enrichment_reconciliation"
>title="Riconciliazione dell’arricchimento"
>abstract="Impostare i parametri di riconciliazione."

>[!CONTEXTUALHELP]
>id="dc_targetdata_personalization_enrichmentdata"
>title="Dati di arricchimento"
>abstract="Seleziona i dati da utilizzare per arricchire la composizione. Puoi selezionare due tipi di dati di arricchimento: un attributo di arricchimento singolo dallo schema, noto anche come dimensione targeting, oppure un collegamento della raccolta, che è un collegamento con cardinalità 1-N tra le tabelle."

L&#39;attività **Enrichment** ti consente di migliorare la composizione aggiungendo dati aggiuntivi dal database federato.

Se hai configurato una connessione alla destinazione Federated Audience Composition, puoi utilizzare l’attività Enrichment per arricchire i dati in arrivo da Adobe Experience Platform con gli attributi del database esterno. [Scopri come arricchire il pubblico di Adobe Experience Platform con dati esterni](../connections/destinations.md)

+++ Dettagli configurazione

>[!NOTE]
>
>Se hai più transizioni in entrata, devi innanzitutto selezionare il **set principale** dal menu a discesa.

Dopo aver aggiunto l&#39;attività **Enrichment** alla composizione, è possibile selezionare **Aggiungi dati di arricchimento** per scegliere l&#39;attributo da utilizzare per arricchire la composizione. È possibile selezionare **Modifica espressione** per generare un&#39;espressione avanzata per selezionare l&#39;attributo.

![](./assets/activities/enrichment.png)

+++

#### Riconciliazione {#reconciliation}

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation"
>title="Attività di riconciliazione"
>abstract="L’attività **Riconciliazione** consente di definire il collegamento tra i dati nel database e quelli in una tabella di lavoro."

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation_field"
>title="Campo di selezione riconciliazione"
>abstract="Campo di selezione riconciliazione"

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation_condition"
>title="Condizione di creazione riconciliazione"
>abstract="Condizione di creazione riconciliazione"

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation_complement"
>title="Complemento generato da riconciliazione"
>abstract="Complemento generato da riconciliazione"

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation_targeting"
>title="Schema"
>abstract="Seleziona il nuovo schema da applicare ai dati. Uno schema, noto anche come dimensione targeting, consente di definire la popolazione di destinazione: destinatari, abbonati all’app, operatori, iscritti, ecc. Per impostazione predefinita, è selezionato lo schema corrente della composizione."

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation_rules"
>title="Regole di riconciliazione"
>abstract="Seleziona le regole di riconciliazione da utilizzare per la deduplica. Per utilizzare gli attributi, seleziona l’opzione **Attributi semplici** e scegli i campi di origine e di destinazione. Per creare una condizione di riconciliazione personalizzata utilizzando query modeler, seleziona l’opzione **Condizioni di riconciliazione avanzate**."

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation_targeting_selection"
>title="Selezionare una dimensione targeting"
>abstract="Seleziona lo schema, noto anche come dimensione targeting, per i dati in entrata da riconciliare."

>[!CONTEXTUALHELP]
>id="dc_orchestration_keep_unreconciled_data"
>title="Mantenere i dati non riconciliati"
>abstract="Per impostazione predefinita, i dati non riconciliati vengono conservati nella transizione in uscita e sono disponibili nella tabella di lavoro per utilizzi futuri. Per rimuovere i dati non riconciliati, disattiva l’opzione **Mantieni i dati non riconciliati**."

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation_attribute"
>title="Attributo di riconciliazione"
>abstract="Seleziona l’attributo da utilizzare per riconciliare i dati e conferma."

>[!NOTE]
>
>Per impostazione predefinita, i dati non riconciliati vengono mantenuti nella transizione in uscita e sono disponibili nella tabella di lavoro per utilizzi futuri. Se **non** desidera utilizzare dati riconciliati, disattivare l&#39;opzione **Mantieni dati non riconciliati**.

L&#39;attività **Reconciliation** consente di definire il collegamento tra i dati del database federato e i dati di una tabella di lavoro.

+++ Dettagli configurazione

Dopo aver aggiunto l&#39;attività **Riconciliazione** alla composizione, è possibile scegliere lo schema da utilizzare per la riconciliazione.

Dopo aver scelto lo schema, devi impostare le regole di riconciliazione. Puoi scegliere tra **Attributi semplici** o **Condizioni di riconciliazione avanzate**.

>[!BEGINTABS]

>[!TAB Attributi semplici]

Dopo aver scelto **Attributi semplici**, seleziona **Aggiungi regola**. Ora puoi impostare la riconciliazione aggiungendo i campi **Source** e **Destination**. Il campo **Destinazione** corrisponde ai campi dello schema selezionato.

![](./assets/activities/reconciliation-rules.png)

I dati vengono riconciliati quando l’origine e la destinazione sono uguali. È possibile aggiungere altri criteri di riconciliazione selezionando **Aggiungi regola**. Se sono specificate più condizioni di join, **tutte** devono essere verificate in modo che i dati possano essere collegati tra loro.

>[!TAB Condizioni di riconciliazione avanzate]

Dopo aver scelto **Condizioni di riconciliazione avanzate**, seleziona **Crea condizioni**. Ora puoi creare una condizione di riconciliazione personalizzata utilizzando Query Modeler. Per ulteriori informazioni sull&#39;utilizzo di Query Modeler, leggere la [Panoramica di Query Modeler](../query/home.md)

![](./assets/activities/reconciliation-advanced.png)

>[!ENDTABS]

Puoi anche filtrare i dati riconciliati. Selezionare **Crea filtro** per creare una condizione personalizzata utilizzando Query Modeler. Per ulteriori informazioni sull&#39;utilizzo di Query Modeler, leggere la [Panoramica di Query Modeler](../query/home.md)

+++

#### Salva pubblico {#save-audience}

>[!CONTEXTUALHELP]
>id="dc_orchestration_save_audience"
>title="Salva un pubblico"
>abstract="Utilizza questa attività per creare un pubblico nuovo dalla popolazione calcolata a monte nella composizione. I tipi di pubblico creati vengono aggiunti all’elenco dei tipi di pubblico e sono disponibili tramite il menu **Tipi di pubblico**."

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveaudience_outbound"
>title="Genera transizione in uscita"
>abstract="Utilizza questa opzione se desideri aggiungere una transizione dopo l’attività **Salva pubblico**."

>[!CONTEXTUALHELP]
>id="dc_orchestration_save_audience_primary_identity"
>title="Campo dell’identità primaria"
>abstract="Seleziona l’identità primaria da utilizzare per i profili."
>additional-url="https://experienceleague.adobe.com/it/docs/experience-platform/xdm/ui/fields/identity#define-a-identity-field" text="Ulteriori informazioni nella documentazione di Experience Platform"

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveaudience_namespace"
>title="Spazio dei nomi identità"
>abstract="Selezionare lo spazio dei nomi da utilizzare per i profili."
>additional-url="https://experienceleague.adobe.com/it/docs/experience-platform/identity/features/namespaces" text="Ulteriori informazioni nella documentazione di Experience Platform"

>[!IMPORTANT]
>
>Se la sandbox utilizza un criterio di unione **precedenza set di dati**, contatta l’Assistenza clienti Adobe per aggiungere il set di dati `Halos UPS` al criterio di unione.
>
>Per ulteriori informazioni sui criteri di unione, consulta la [panoramica sui criteri di unione](https://experienceleague.adobe.com/it/docs/experience-platform/profile/merge-policies/overview).

L&#39;attività **Save audience** consente di creare un pubblico in base alla composizione. Una volta creato il pubblico, puoi utilizzarlo all’interno di Audience Portal in Adobe Experience Platform. Per ulteriori informazioni sull&#39;utilizzo dei tipi di pubblico con Federated Audience Composition, consulta la [panoramica sui tipi di pubblico](../start/audiences.md). Per ulteriori informazioni sui tipi di pubblico in Experience Platform, consulta la [Panoramica di Audience Portal](https://experienceleague.adobe.com/it/docs/experience-platform/segmentation/ui/audience-portal){target="_blank"}.

+++ Dettagli configurazione

>[!IMPORTANT]
>
>Il nome del pubblico **deve** essere univoco nella sandbox corrente e non può avere lo stesso nome di un pubblico esistente.

Dopo aver aggiunto l&#39;attività **Salva pubblico** alla composizione, puoi specificare il nome del pubblico appena creato.

![](./assets/activities/save-audience.png){zoomable="yes" width="30%"}

Ora puoi specificare le mappature per selezionare i campi da trasferire al pubblico appena creato. Seleziona **Aggiungi mappatura pubblico** e scegli i campi del pubblico di origine e di destinazione, ripetendo il numero di volte necessario.

Dopo aver aggiunto le mappature, puoi selezionare l’identità principale e lo spazio dei nomi per identificare i profili target nel database. Il campo di identità principale viene utilizzato per identificare i profili, mentre lo spazio dei nomi dell’identità funge da chiave per identificare l’identità.

Inoltre, puoi impostare la scadenza dei dati per il pubblico. La scadenza dei dati determina il numero di giorni dopo i quali scadrà l’iscrizione al pubblico. La scadenza dei dati può essere compresa tra 1 e 90 giorni. Per impostazione predefinita, questo valore è impostato su 30.

+++

#### Dividi {#split}

>[!CONTEXTUALHELP]
>id="dc_orchestration_split"
>title="Attività Dividi"
>abstract="L’attività **Dividi** consente di segmentare le popolazioni in ingresso in più sottoinsiemi in base a criteri di selezione diversi, ad esempio le regole di filtro o le dimensioni della popolazione."

>[!CONTEXTUALHELP]
>id="dc_orchestration_split_segments"
>title="Segmenti per attività Dividi"
>abstract="Aggiungi tutti i sottoinsiemi desiderati per segmentare la popolazione in ingresso.<br/></br>Quando viene eseguita l’attività **Dividi**, la popolazione viene segmentata tra i diversi sottoinsiemi nell’ordine in cui vengono aggiunti all’attività. Prima di avviare la composizione, assicurati di aver ordinato i sottoinsiemi nell’ordine più adatto alle tue esigenze utilizzando i pulsanti freccia."

>[!CONTEXTUALHELP]
>id="dc_orchestration_split_filter"
>title="Filtro attività Dividi"
>abstract="Per applicare una condizione di filtro al sottoinsieme, selezionare **[!UICONTROL Crea filtro]** e configurare la regola di filtro desiderata utilizzando il modellatore di query. Ad esempio, includi i profili della popolazione in ingresso il cui indirizzo e-mail esiste nel database."

>[!CONTEXTUALHELP]
>id="dc_orchestration_split_limit"
>title="Limite attività Dividi"
>abstract="Per limitare il numero di profili selezionati dal sottoinsieme, attiva l’opzione **[!UICONTROL Abilita limite]** e specifica il numero o le percentuali della popolazione da includere."

>[!CONTEXTUALHELP]
>id="dc_orchestration_split_sorting"
>title="Ordinamento attività Dividi"
>abstract="Quando imposti un limite di popolazione per un sottoinsieme, puoi classificare i profili selezionati in base a un attributo di profilo specifico, in ordine crescente o decrescente. A tale scopo, attiva l’opzione **Abilita ordinamento**. Ad esempio, puoi limitare un sottoinsieme in modo da includere solo i primi 50 profili con l’importo di acquisto più alto."

>[!CONTEXTUALHELP]
>id="dc_orchestration_split_complement"
>title="Complemento generato da suddivisione"
>abstract="Dopo aver configurato tutti i sottoinsiemi, puoi selezionare la popolazione rimanente che non corrisponde a nessuno dei sottoinsiemi e includerli in un’ulteriore transizione in uscita. A tale scopo, attiva l’opzione **Genera complemento**."

>[!CONTEXTUALHELP]
>id="dc_orchestration_split_generatesubsets"
>title="Generare tutti i sottoinsiemi nella stessa tabella"
>abstract="Attiva questa opzione per raggruppare tutti i sottoinsiemi in una singola transizione di output."

>[!CONTEXTUALHELP]
>id="dc_orchestration_split_emptytransition"
>title="Ignora transizione vuota"
>abstract="Attiva l’opzione **[!UICONTROL Ignora transizione vuota]** per disabilitare la transizione di output per questo sottoinsieme se la popolazione in ingresso è vuota."

>[!CONTEXTUALHELP]
>id="dc_orchestration_split_enable_overlapping"
>title="Abilita sovrapposizione popolazioni di output"
>abstract="L’opzione **[!UICONTROL Abilita sovrapposizione popolazioni di output]** consente di gestire le popolazioni appartenenti a diversi sottoinsiemi. Quando questa opzione non è selezionata, l’attività Dividi si assicura che un destinatario non possa essere presente in diverse transizioni di output, anche se soddisfa i criteri di diversi sottoinsiemi. Saranno nella destinazione della prima scheda con i criteri corrispondenti. Quando questa opzione è selezionata, i destinatari possono essere in più sottoinsiemi se soddisfano i rispettivi criteri di filtro. "

L&#39;attività **Split** separa il gruppo in ingresso in più parti, a seconda dei criteri specificati.

+++ Dettagli configurazione

>[!IMPORTANT]
>
>Quando l&#39;attività **Split** viene eseguita, il gruppo è separato tra i diversi sottoinsiemi nell&#39;**ordine in cui vengono aggiunti**. Ad esempio, se il primo sottoinsieme divide il 70% della popolazione iniziale, il sottoinsieme successivo applicherà i propri criteri di selezione al restante 30%.
>
>Prima di eseguire la composizione, assicuratevi di aver ordinato i sottoinsiemi nell&#39;ordine in cui desiderate eseguire le suddivisioni.

Dopo aver aggiunto l&#39;attività **Dividi** alla composizione, ora puoi determinare come impostare il pubblico in modo secondario. Seleziona **Aggiungi segmento** per creare i tuoi diversi percorsi di diramazione.

Ora puoi fornire dettagli per ciascuno di questi percorsi secondari. Puoi assegnare un nome al percorso secondario e le condizioni del filtro. Per creare una condizione di filtro, selezionare **Crea filtro** e configurare la regola di filtro utilizzando Query Modeler. Per ulteriori informazioni sull&#39;utilizzo di Query Modeler, leggere la [Panoramica di Query Modeler](../query/home.md).

Dopo aver creato la condizione di filtro, puoi applicare le seguenti regole aggiuntive:

- **Abilita limite**: limita il numero di profili che possono essere suddivisi nel sottoinsieme. Puoi impostarlo come numero o come percentuale della popolazione.
   - Se abiliti un limite, puoi anche classificare i profili selezionati in base a un attributo di profilo specifico. Attiva **Abilita ordinamento** e puoi ordinare gli attributi in ordine crescente o decrescente.
- **Salta transizione vuota**: disabilita la transizione se il gruppo in ingresso è vuoto.

Ora che i sottoinsiemi sono stati configurati, puoi impostare alcune opzioni aggiuntive.

| Opzioni | Descrizione |
| ------- | ----------- |
| **Genera complemento** | Crea una transizione in uscita contenente il gruppo rimanente. |
| **Abilita la sovrapposizione delle popolazioni di output** | Se attivato, il destinatario **non può** essere presente in più transizioni in uscita e **solo** sarà presente nella prima transizione in uscita. Se disabilitato, il destinatario **può** comparire in più transizioni in uscita. |
| **Genera tutti i sottoinsiemi nella stessa tabella** | Raggruppa tutti i sottoinsiemi in un&#39;unica transizione in uscita. |

+++

### Attività di controllo del flusso {#flow-control}

Le attività di controllo del flusso consentono di definire l&#39;organizzazione e il coordinamento della composizione.

#### E unisci {#and-join}

>[!CONTEXTUALHELP]
>id="dc_orchestration_and-join"
>title="Attività AND-join"
>abstract="L’attività **AND-join** consente di sincronizzare più rami di esecuzione di una composizione. Viene attivata al termine di tutte le attività precedenti. Questo consente di verificare che alcune attività siano state completate prima di continuare a eseguire la composizione."

L&#39;attività **AND-join** consente di combinare più rami di una composizione. Questa attività viene attivata solo dopo che sono state attivate **tutte** le transizioni in entrata.

+++ Dettagli configurazione

Dopo aver aggiunto più attività per formare almeno due rami diversi, puoi aggiungere l&#39;attività **AND-join** alla fine di qualsiasi ramo.

![](./assets/activities/and-join.png)

Nella sezione **Opzioni di unione** puoi selezionare tutte le attività che desideri sincronizzare. Inoltre, puoi scegliere quale transizione in entrata mantenere nel menu a discesa **Set principale**.

+++

#### Fine {#end}

L&#39;attività **End** contrassegna graficamente la fine della composizione e non ha alcun impatto funzionale.

#### Fork {#fork}

>[!CONTEXTUALHELP]
>id="dc_orchestration_fork"
>title="Attività Fork"
>abstract="L’attività **Fork** consente di creare transizioni in uscita per avviare più attività contemporaneamente."

>[!CONTEXTUALHELP]
>id="dc_orchestration_fork_transitions"
>title="Transizioni delle attività Fork"
>abstract="Per impostazione predefinita, vengono create due transizioni con attività **Fork**. Seleziona il pulsante **Aggiungi transizione** per definire una transizione in uscita aggiuntiva e immetti la relativa etichetta."

L&#39;attività **Fork** consente di creare più transizioni in uscita che avviano contemporaneamente più attività.

+++ Dettagli configurazione

Dopo aver aggiunto l&#39;attività **Fork** alla composizione, vengono generate automaticamente due transizioni in uscita. Puoi assegnare un nome a queste transizioni in uscita. Inoltre, puoi selezionare **Aggiungi transizione** per aggiungere un&#39;altra transizione in uscita.

![](./assets/activities/fork.png)

+++

#### Modulo di pianificazione {#scheduler}

>[!CONTEXTUALHELP]
>id="dc_orchestration_scheduler"
>title="Attività del modulo di pianificazione"
>abstract="L’attività **Modulo di pianificazione** consente di pianificare quando viene avviata una composizione del pubblico. Questa attività deve essere considerata come un avvio pianificato. Può essere utilizzata solo come prima attività di una composizione."

>[!CONTEXTUALHELP]
>id="dc_orchestration_schedule_validity"
>title="Validità del modulo di pianificazione"
>abstract="È possibile definire un periodo di validità per il modulo di pianificazione. Può essere permanente (impostazione predefinita) o valido fino a una data specifica."

>[!CONTEXTUALHELP]
>id="dc_orchestration_schedule_options"
>title="Opzioni del modulo di pianificazione"
>abstract="Definisci la frequenza del modulo di pianificazione. Può essere eseguito in un determinato momento, una o più volte al giorno, alla settimana o al mese."

L&#39;attività **Scheduler** consente di pianificare quando avviare l&#39;esecuzione della composizione. **devi** utilizzarlo come prima attività della composizione.

+++ Dettagli configurazione

Dopo aver aggiunto l&#39;attività **Scheduler** alla composizione, è possibile impostare la **frequenza di esecuzione** per la composizione. Le opzioni includono **Una volta**, **Ogni giorno**, **Più volte al giorno**, **Ogni settimana** e **Ogni mese**.

>[!BEGINTABS]

>[!TAB Una volta]

>[!NOTE]
>
>L&#39;ora è impostata su UTC.

Se selezioni **Una volta**, la composizione viene eseguita una sola volta. Potete selezionare la data e l&#39;ora di esecuzione della composizione.

>[!TAB Giornaliero]

Se selezioni **Giornaliero**, la composizione viene eseguita una volta al giorno. Tuttavia, puoi scegliere il giorno del mese in cui viene eseguita la composizione nella sezione **Giorno del mese**. I valori possibili includono **Ogni giorno**, **Nei giorni della settimana**, **Durante un periodo selezionato** e **Giorni selezionati della settimana**.

| Giorno del mese | Descrizione |
| ---------------- | ----------- |
| Ogni giorno | La composizione viene eseguita ogni giorno. |
| Nei giorni della settimana | La composizione viene eseguita ogni giorno feriale. |
| Durante un periodo selezionato | La composizione viene eseguita ogni giorno per tutto il periodo selezionato. È possibile impostare la durata del periodo di ricorrenza e la data di inizio del periodo. |
| Giorni della settimana selezionati | La composizione viene eseguita ogni giorno della settimana selezionata. |

Dopo aver scelto il giorno del mese in cui eseguire la pianificazione, puoi selezionare **Anteprima orari di lancio** per controllare la pianificazione delle prossime dieci esecuzioni della composizione.

>[!TAB Più volte al giorno]

Se selezioni **Più volte al giorno**, la composizione viene eseguita più volte al giorno. Potete scegliere se la composizione viene eseguita in orari specifici al giorno o periodicamente a orari prestabiliti.

Se selezioni **Ore selezionate**, puoi scegliere le ore specifiche in cui verrà eseguita la composizione. Se si seleziona **Periodico**, è possibile scegliere la frequenza di esecuzione della composizione in ore o minuti e tra le ore di esecuzione. Tutte le ore sono in UTC.

Dopo aver selezionato le ore, puoi scegliere la frequenza con cui eseguire l&#39;esecuzione nella sezione **Giorno del mese**.

| Giorno del mese | Descrizione |
| ---------------- | ----------- |
| Ogni giorno della settimana | La composizione viene eseguita ogni giorno. |
| In alcuni giorni della settimana | La composizione viene eseguita ogni giorno della settimana selezionata. |

Dopo aver scelto il giorno del mese in cui eseguire la pianificazione, puoi selezionare **Anteprima orari di lancio** per controllare la pianificazione delle prossime dieci esecuzioni della composizione.

>[!TAB Settimanale]

Se si seleziona **Settimanale**, la composizione viene eseguita con la frequenza settimanale impostata. Se imposti la frequenza settimanale su un numero maggiore di 1, puoi anche scegliere la data da cui inizia l’esecuzione.

Dopo aver scelto la frequenza di valutazione, puoi scegliere la frequenza con cui eseguire l&#39;esecuzione nella sezione **Giorno del mese**.

| Giorno del mese | Descrizione |
| ---------------- | ----------- |
| Ogni giorno della settimana | La composizione viene eseguita ogni giorno. |
| In alcuni giorni della settimana | La composizione viene eseguita ogni giorno della settimana selezionata. |

Dopo aver scelto il giorno del mese in cui eseguire la pianificazione, puoi selezionare **Anteprima orari di lancio** per controllare la pianificazione delle prossime dieci esecuzioni della composizione.

>[!TAB Mensile]

Se si seleziona **Mensile**, la composizione viene eseguita sulla frequenza mensile impostata. Puoi impostarlo su ogni mese o su determinati mesi.

Dopo aver scelto la frequenza mensile, puoi scegliere il **giorno del mese** in cui viene eseguita l&#39;esecuzione.

| Giorno del mese | Descrizione |
| ---------------- | ----------- |
| Ogni giorno | La composizione viene eseguita ogni giorno. |
| Nei giorni della settimana | La composizione viene eseguita ogni giorno feriale. |
| Durante un periodo selezionato | La composizione viene eseguita ogni giorno per tutto il periodo selezionato. È possibile impostare la durata del periodo di ricorrenza e la data di inizio del periodo. |
| Giorni della settimana selezionati | La composizione viene eseguita ogni giorno della settimana selezionata. |

Una volta impostato il **giorno del mese**, puoi scegliere l&#39;ora di inizio. Tutte le ore sono in UTC.

>[!ENDTABS]

Dopo aver selezionato la frequenza di esecuzione, puoi scegliere il **Periodo di validità** della pianificazione.

| Periodo di validità | Descrizione |
| --------------- | ----------- |
| **Permanente (senza scadenza)** | La composizione non scadrà mai. |
| **Periodo di validità** | La composizione verrà eseguita tra le date specificate. |

+++

#### Attendi {#wait}

>[!CONTEXTUALHELP]
>id="dc_orchestration_wait"
>title="Attività Attendi"
>abstract="L’attività **Attendi** viene utilizzata per ritardare la transizione da un’attività a un’altra."

L&#39;attività **Wait** sospende l&#39;esecuzione della composizione per il periodo di tempo specificato.

+++ Dettagli configurazione

Dopo aver aggiunto l&#39;attività **Attendi** alla composizione, puoi impostarla come **Durata** o **Ora fissa**.

![](./assets/activities/wait.png)

Se selezioni durata, puoi impostare il periodo di tempo da attendere. Questo periodo di tempo può essere espresso in secondi, minuti, ore o giorni.

Se selezionate l&#39;ora fissa, potete impostare la composizione in modo che attenda la data e l&#39;ora specificate. L&#39;ora è impostata sul **fuso orario locale**.

+++

## Transizioni {#transitions}

Nelle composizioni, le transizioni mostrano come i dati vengono trasportati da un’attività all’altra. Le transizioni memorizzano i dati in una tabella di lavoro temporanea. Se selezioni la transizione, puoi visualizzare le seguenti informazioni:

- **Anteprima schema**: è possibile selezionare questa opzione per visualizzare lo schema per la tabella di lavoro.
- **Risultati anteprima**: è possibile selezionare questa opzione per visualizzare i dati trasportati nella transizione selezionata. Questa opzione è disponibile solo se è abilitato **Mantieni il risultato delle popolazioni provvisorie tra due esecuzioni**.

![](assets/transition-preview.png)

## Passaggi successivi {#next-steps}

Dopo aver letto questa guida, avrai una migliore comprensione delle attività e delle transizioni che puoi utilizzare all’interno di una composizione. Per ulteriori informazioni sulle composizioni in generale, leggere la [panoramica sulla composizione](./create-composition.md).
