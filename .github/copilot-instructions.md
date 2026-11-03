---
source-git-commit: d8ce0aecffcf6b85aa6c41e2520efbf564806098
workflow-type: tm+mt
source-wordcount: '2814'
ht-degree: 2%
---
# Documentazione di Adobe Experience Platform: istruzioni del copilota

Questo archivio (`experience-platform.en`) è la documentazione pubblica di Adobe Experience Platform.
Ogni elemento di contenuto che crei, modifichi o rivedi DEVE seguire le regole riportate di seguito.

## Non restringere o ridefinire le richieste

Rispondi alla richiesta che è stata fatta, non più piccola. Non aggiornare una richiesta
più piccolo di quanto fosse e non restituire un lavoro parziale descritto come completato.
Ogni riga in questo archivio può essere corretta indipendentemente da chi o cosa l’abbia scritta o quando: &quot;preesistente&quot;,
&quot;non fa parte di questa differenza&quot; e &quot;non rientra nell’ambito di applicazione&quot; non sono motivi per lasciare una violazione indeterminata.
Quando ti viene chiesto di correggere le violazioni, correggili tutte, indipendentemente dalla loro età. Se qualcosa blocca davvero
il lavoro, dire esattamente ciò che è stato annullato e quello che è rimasto annullato, e fermarsi.

## &#x200B;1. Voce, tono e stile

### Scrittura incentrata sull&#39;utente

Centra l’utente, non la funzione. Scrivere ciò che l&#39;utente può **fare**, non ciò che la funzione fa.

- Usa la seconda persona (&quot;tu&quot;) e l&#39;umore imperativo per le istruzioni.
- Usa &quot;tu&quot; quando parli al pubblico di se stessi, non di &quot;utenti&quot;. &quot;Utenti&quot; è
accettabile quando si fa riferimento a un ruolo (ad esempio, un amministratore che gestisce gli utenti).
- Evita &quot;La funzione X consente di...&quot; o &quot;La funzione X consente di...&quot;. Inserisci l’utente come
soggetto o usa umore imperativo.
  - Scorretto: &quot;L’API server può essere utilizzata sui server&quot;. Corretto: &quot;Utilizzare l&#39;API server sui server&quot;.
  - Scorretto: &quot;I campi calcolati consentono la creazione di valori...&quot; Scorretto: &quot;Utilizzare campi calcolati
    per creare valori...&quot;
- Faccia attenzione all&#39;uso eccessivo di &quot;tu puoi&quot;. Va bene, ma può creare frasi ripetitive o peggiori.
- Utilizza &quot;seleziona&quot; per scegliere le opzioni da un elenco o evidenziare il testo. Usa &quot;click&quot; solo per
azioni esplicite del mouse. Evita di denominare il tipo di controllo (pulsante, collegamento) se non necessario per
disambiguazione.
- Utilizzare &quot;Apri&quot; / &quot;Chiudi&quot; per le applicazioni e le principali finestre o pannelli.
- Utilizza &quot;Lascia&quot; per uscire da un sito o da un’esperienza (ad esempio, &quot;Lascia Report Builder&quot;).
- Utilizza &quot;vai a&quot; o &quot;passa a&quot; per la navigazione.
- Utilizzare &quot;Riproduci video&quot; e non &quot;Guarda video&quot;.
- Utilizzare &quot;Visualizza&quot;, &quot;Mostra&quot; o &quot;Vai a tutti&quot; e non &quot;Vedi tutti&quot;.
- Utilizzare &quot;accesso&quot; / &quot;disconnessione&quot;, non &quot;accesso&quot; / &quot;disconnessione&quot;.
- Evita di usare &quot;al fine di&quot;. Utilizza invece &quot;per&quot;.
- Evita di utilizzare. Utilizza invece &quot;use&quot;.
- Evita aggettivi vaghi come &quot;veloce&quot; o &quot;facile&quot;. Sii preciso: &quot;Questo processo richiede di solito
5 minuti.&quot;
- Evita avverbi deboli: molto, estremamente, incredibilmente.

### Struttura frase e paragrafo

- Target non più di 20 parole per frase (massimo 35). Un pensiero per frase.
- Paragrafi: massimo 125 parole, idealmente 100 o meno. Max 4-5 frasi. Nessuna parete di testo.
- Usa la voce attiva. Evita costruzioni passive e nominalizzazioni (ad es., &quot;crea&quot; non
creazione).
- Utilizza una semplice struttura soggetto-verbo-oggetto.
- Evita soggetti falsi (&quot;È...&quot;, &quot;Ci sono...&quot;).
- Utilizza la stessa parola in modo coerente. Non ruotare i sinonimi.
- Nessun esempio di umorismo, gergo, gergo o cultura specifica (localizzare bene).
- Utilizza la virgola di Oxford negli elenchi di tre o più elementi.
- Scrivi i numeri interi da zero a nove; utilizza le cifre per i numeri da 10 in poi.
- Nessun punto e virgola. Utilizza invece un punto e una nuova frase.
- NON usare trattini lunghi, trattini lunghi o trattini in prosa. Riformula invece. I trattini sono
sono consentite solo negli aggettivi composti visualizzati nell’interfaccia utente, nei nomi dei file e nel codice.
- NON utilizzare regole orizzontali (`---` o `***`). Non sono supportati in Experience League.

### Scannabilità

- I lettori devono comprendere l’ambito dell’articolo solo da titolo, intestazioni e didascalie.
- Max 2-5 sottosezioni per sezione.
- Target 7 passaggi per attività; 10 è il massimo pratico. Suddividere le procedure più lunghe in sottoattività.
- Max 8 elementi per elenco puntato.
- Utilizzare le tabelle per semplificare la scansione degli elenchi di termini/definizioni.
- Il contenuto deve essere inferiore al grado 10 in un test di leggibilità (dopo aver rimosso i sostantivi corretti)
e titoli).

### Scrittura per individuazione IA

- Inserire i termini chiave (nomi di prodotto, nomi di funzionalità, attività) nel corpo del testo e nel testo del collegamento, non solo
in immagini o tabelle complesse.
- Scrivi titoli e primi paragrafi chiari e autonomi.
- Mantieni le frasi brevi e dirette.
- Utilizza formati strutturati (passaggi numerati, punti elenco brevi, intestazioni in stile definizione) per
procedure e confronti.
- Includi sinonimi o termini alternativi al primo utilizzo (ad esempio, &quot;ECID (Experience Cloud ID)&quot;).
- Mantieni i campi dei metadati (titolo, descrizione, tag delle funzioni) completi e precisi.

## &#x200B;2. Tag di localizzazione (applica sempre)

La traduzione automatica viene eseguita automaticamente a ogni commit in main.

### `[!DNL Product Name]`: non localizzare

Applica a nomi di prodotto Adobe (`[!DNL Analytics]`, `[!DNL Target]`, `[!DNL Campaign]`,
`[!DNL Experience Platform]`), nomi di prodotti di terze parti (`[!DNL Mozilla Firefox]`,
`[!DNL Workfront]`), nomi funzionali che potrebbero confondere la traduzione (`[!DNL Pass]`,
`[!DNL Campaign]`) e operatori booleani utilizzati come termini logici (`[!DNL AND]`, `[!DNL OR]`).

NON applicare a URL, nomi di file, nomi di directory, blocchi di codice, acronimi o termini già
nel database Do Not Translate.

Nel testo del collegamento, rimuovere le parentesi: `[Adobe](https://www.adobe.com/it)`, non
`[[!DNL Adobe]](https://www.adobe.com/it)`.

### `[!UICONTROL Label]`: controlli dell&#39;interfaccia utente

Obbligatorio per ogni elemento dell’interfaccia utente cliccabile nei passaggi della procedura e sui nomi delle funzioni,
elementi di navigazione, nomi di pagina, opzioni, campi e schede come mostrato nell’interfaccia.

- Grassetto nei passaggi e nella navigazione: `Select **[!UICONTROL Destinations]** from the left navigation.`
- Il corsivo è accettabile nel testo concettuale (senza passaggi) per maggiore chiarezza.
- Nelle tabelle di HTML: utilizzare `<span class="uicontrol">term</span>` anziché &grave;&grave;.
- Nel testo del collegamento: rimuovi le parentesi quadre.
- Le maiuscole devono corrispondere esattamente all’interfaccia.
- NON si applica ai termini generici utilizzati concettualmente (&quot;segmento&quot;, &quot;metrica&quot;, &quot;campagna&quot;) a meno che
con riferimento all’elemento dell’interfaccia utente, a frasi lunghe, blocchi di codice, acronimi o descrizioni di icone
(se disponibile, usa il nome del passaggio del mouse o della descrizione comando dell’icona).

### `[!DONOTLOCALIZE]`: escludi intere sezioni

```markdown
>[!DONOTLOCALIZE]
>
>Content that must not be translated.
```

Non è necessario all’interno di blocchi di codice; per impostazione predefinita non sono localizzati.

### Dove è possibile e non è possibile utilizzare i tag

- Può essere utilizzato in: paragrafi, elenchi, intestazioni, tabelle, badge, testo alternativo e metadati.
- Non può essere utilizzato in: blocchi di codice, acronimi.
- Se un campo di metadati inizia con un tag `[!DNL]` o &grave;&grave;, racchiudere l&#39;intero campo
valore tra virgolette o convalida non riuscita.

## &#x200B;3. Terminologia e branding

### Nomi di prodotto

Utilizza sempre questi moduli esatti. Includi &quot;Adobe&quot; come primo riferimento in una guida. NON precedere
i nomi dei prodotti con &quot;il&quot;, a meno che il nome ufficiale non lo includa.

| Corretto | NON usare MAI |
|---|---|
| Adobe Experience Platform | AEP, AXP, Adobe XP, Adobe Cloud Platform |
| Experience Platform (riferimento secondario) | Platform (da sola, a meno che il contesto non sia univoco) |
| Adobe Real-Time CDP | RTCDP, ARTCDP |
| Real-Time CDP (secondario) | Real-time CDP (&quot;t&quot; minuscola) |
| Adobe Real-Time Customer Data Platform | — |
| Profilo cliente in tempo reale | Profilo cliente in tempo reale, Profilo unificato |
| Adobe Journey Optimizer | AJO |
| Adobe Customer Journey Analytics | CJA |
| Customer Journey Analytics (secondario) | — |
| Adobe Real-Time CDP Collaboration | RTCDP Collaboration, RTCDP Collab, Collab |
| Connessioni Adobe Real-Time CDP | Connessioni RTCDP, Connessioni AEP, Connessioni (da sole) |
| Adobe Experience Platform Edge Network | Platform Edge Network, Platform Edge, Adobe Experience Edge |
| Tag (nome prodotto) | Launch (obsoleto) |
| Gestione delle decisioni | Offer Decisioning (solo parentesi: &quot;precedentemente Offer Decisioning&quot;) |
| flusso di dati (una parola, lettere minuscole) | datastreaming, configurazione edge |
| Analysis Workspace | analysis workspace, workspace, Workspace |
| Adobe AI | Sensei (obsoleto) |
| Adobe GenAI | — |
| Adobe GenStudio for Performance Marketing | — |

- &quot;Real-Time&quot; utilizza sempre la R maiuscola e la T maiuscola quando fanno parte del nome di un prodotto.
- &quot;Edizioni&quot; è in minuscolo genericamente; &quot;Edizione&quot; è in maiuscolo come parte di un’edizione di prodotto
nome (ad esempio, &quot;Adobe Real-Time CDP B2C Edition&quot;).
- NON abbreviare i nomi dei prodotti nella documentazione rivolta all’utente (nessun AEP, CJA, AJO, RTCDP).
Eccezioni limitate: gli acronimi possono apparire tra parentesi al primo utilizzo per SEO, o nel sommario
voci, metadati di descrizione e intestazioni per cui la lunghezza rappresenta un problema.
- Uso delle maiuscole in Analytics: i nomi dei pannelli sono minuscoli (vuoto, attribuzione, sperimentazione,
figura libera; eccezione: &quot;area di lavoro Percorso&quot;). I nomi delle visualizzazioni sono in minuscolo (barra, ciambella,
istogramma, linea, mappa ad albero, testo).

### Terminologia funzionale e concettuale

| Corretto | NON usi |
|---|---|
| inoltro eventi | inoltro lato server, Launch Server Side |
| INSERISCO NELL&#39;ELENCO CONSENTITI DI | whitelist |
| INSERISCO NELL&#39;ELENCO BLOCCATI DI / | blacklist |
| principale/replica OPPURE primario/secondario (server) | master/slave |
| principale (ramo GitHub) | principale |
| hacker etico | hacker con cappello bianco |
| remarketing | retargeting |
| gruppo di campi | mixin (obsoleto), estensioni, mixin |
| scadenza automatica dei dati | TTL, time-to-live, scadenza |
| sandbox non di produzione | staging (come nome di ambiente) |
| definizione del segmento | segmento (solo, quando significa la definizione) |
| ID (maiuscole sempre) | Id |
| acquisizione/acquisizione/acquisizione | onboarding (per aggiungere dati a Platform) |
| set di dati/set di dati | File di dati, file di set di dati |
| controllo degli accessi | autorizzazioni (per la funzione Platform) |
| widget | scheda metrica (obsoleto) |
| variabile segnaposto | variabile fittizia |
| non disponibile / bloccato / disattivato / disattivato | disattivato |
| verifica di coerenza | controllo di integrità |
| incorporato | nativo (come sinonimo di integrato) |
| priorità alta | unghie obbligatorie |
| legacy | clausola di salvaguardia |
| principale/principale/sorgente | master (come descrittore) |

### Termini solo interni: NON utilizzare MAI in documenti rivolti al pubblico

| Termine interno | Utilizza invece |
|---|---|
| AEP | Adobe Experience Platform |
| PALMO | gestione sandbox/controllo degli accessi |
| BIOME | environment |
| Idrato/idratazione | crea/popola |
| Profilo unificato | Profilo cliente in tempo reale |
| Staging (ambiente) | sandbox non di produzione |
| DTM | Tag |
| Tenant | Organizzazione IMS |
| CRUD | crea, leggi, aggiorna ed elimina (scrivi) |
| Sifone, BSO, Ethos | nomi di codice interni, mai esterni |
| Luppolo | termine interno RGPD/controllo degli accessi |
| Ritmo | termine pubblicitario non rivolto all&#39;utente |
| Pipeline | termine dell’infrastruttura Adobe interna |

## &#x200B;4. Linguaggio inclusivo e accessibilità

### Principi linguistici inclusivi

- Utilizza termini indipendenti dal genere: &quot;rappresentante commerciale&quot; non &quot;venditore&quot;, &quot;moderatore&quot; non &quot;presidente&quot;.
- Preferisci la seconda persona (&quot;tu&quot;) per evitare i pronomi di genere.
- Utilizza singolarmente &quot;loro&quot; per una persona il cui genere è sconosciuto. NON usi lui/lei o lui/i.
- Includere nomi di culture non bianche in esempi (ad esempio, Ayesha, Ibrahim, Vignesh, Quynh).
NON usare solo nomi culturalmente bianchi.
- NON confondere il sesso (maschile/femminile) con il sesso (uomo/donna).
- Capitalizzare le nazionalità, i popoli, le razze (diverse da &quot;bianchi&quot;, secondo lo Stylebook di AP), e le tribù.
- Usa il linguaggio personalizzato: &quot;persone che usano la tecnologia per l&#39;accessibilità&quot;, non &quot;disabili&quot;.
- Evita eufemismi come &quot;diversamente abili&quot;. Evita di usare i descrittori come sostantivi: &quot;il cieco&quot;
&quot;il sordo&quot;.
- Evita termini che riflettano identità/appropriazione culturale: spirito animale, sherpa, fiacca wow,
guru, ninja, tribù.

### Terminologia non inclusiva da evitare

| Utilizzo di | Non |
|---|---|
| INSERISCO NELL&#39;ELENCO CONSENTITI / ELENCO BLOCCATI DI / DI | whitelist/blacklist |
| principale/replica OPPURE principale/secondario | master/slave |
| principale (ramo Git) | principale |
| priorità alta | unghie obbligatorie |
| variabile segnaposto | variabile fittizia |
| non disponibile / bloccato / disattivato / disattivato | disattivato |
| verifica di coerenza | controllo di integrità |
| incorporato | nativo (come sinonimo) |
| autorità/esperto | guru/ninja |
| membri del gruppo | membri della tua tribù |
| riunione | Pow wow / Circolare i carri |
| modello di ruolo / spirito affine | spirito animale |
| guida | Sherpa |
| legacy | clausola di salvaguardia |
| impresa inutile | marcia della morte |
| ridicolo/incompetente/imprevedibile | stupido / zoppo / pazzo |
| hacker etico/non etico | hacker cappello bianco / cappello nero |
| Riproduci video | Guarda il video |
| Visualizza/Mostra/Vai a tutti | Vedi tutto |

### Accessibilità: descrizione dell’interfaccia utente

NON descrivere gli elementi dell&#39;interfaccia utente in base al colore o alla posizione dello schermo. Utilizzo cronologico, non spaziale,
lingua:

| Utilizzo di | Non |
|---|---|
| Primo, Successivo, Finale | Sopra, sotto |
| Nella barra dei menu | A sinistra |
| Prima/Dopo | Nella parte superiore/inferiore dello schermo |

Descrivere le operazioni e non l&#39;aspetto dei controlli:

| Utilizzo di | Non |
|---|---|
| Seleziona ricerca | Fare clic sull&#39;icona della lente di ingrandimento |
| Modifica | Icona della matita |
| Attivato/Disattivato | Commuta/commuta/attiva |
| Menu | Cassetto laterale |
| Immetti l’e-mail | Digita il tuo indirizzo email |
| Salva | Pulsante Salva |
| Annulla | Chiudi |

NON usare il solo colore per trasmettere le informazioni. Associare sempre il colore al testo o alla forma.

### Accessibilità: testo alternativo, collegamenti e video

- **Testo alt**: descrive ciò che viene visualizzato nell&#39;immagine, non solo il nome della schermata. Usa come completato
frasi, parole intere (gli assistenti vocali scrivono abbreviazioni) e includono testo rilevante
dall&#39;immagine. Le immagini che trasmettono informazioni indipendenti dal testo circostante DEVONO avere
testo alternativo.
- **Collegamenti**: non utilizzare mai &quot;fai clic qui&quot; o &quot;collega&quot; come testo di collegamento. Rendi la destinazione chiara da
solo il testo del collegamento.
- **Video**: NON deve essere riprodotto automaticamente. Fornisci sempre un testo alternativo, una trascrizione o un collegamento a
istruzioni scritte. Includi sottotitoli significativi.

## &#x200B;5. Nozioni di base sulla sintassi Markdown

### Frontmatter (obbligatorio per ogni file)

```yaml
---
title: Title Case Title Here
description: Learn how to... or Learn about... (150-160 chars, sentence case).
---
```

- NON aggiungere `exl-id` durante la creazione di una nuova pagina. Viene generato automaticamente al momento della pubblicazione
tempo. Conserva solo i campi `exl-id` che esistono già nelle pagine esistenti.
- Titolo: maiuscole/minuscole, massimo 60 caratteri, nessuna barra verticale o nome prodotto (aggiunto automaticamente).
I titoli dei concetti sono frasi sostantive; i titoli delle attività sono frasi verbali.
- Descrizione: maiuscole/minuscole, da 150 a 160 caratteri. La prima frase riassume; la seconda è una
call to action. NON iniziare con il nome del prodotto o copiare il primo paragrafo letteralmente.

### Intestazioni

- `#` = H1 (uno per pagina, prima riga dopo il frontmatter). `##`, `###` per le sottosezioni. Mai
salta i livelli.
- Massimo 5 parole, massimo 69 caratteri. Riga vuota prima e dopo ogni intestazione.
- Ogni intestazione deve essere seguita dal corpo del testo; non sovrapporre mai le intestazioni o inserire un elenco/tabella/nota
direttamente sotto un titolo.
- Frase. Le intestazioni del concetto sono frasi sostantive; le intestazioni delle attività sono verbi imperativi
(evitare i gerundi).
- Nessun titolo astratto di una singola parola (&quot;Panoramica&quot;, &quot;Introduzione&quot;) senza descrivere l’argomento.
- ID di ancoraggio personalizzati: `## Section title {#section-id}` (lettere minuscole, trattini).

### Collegamenti, immagini e codice

- I riferimenti incrociati interni utilizzano percorsi relativi alla radice: `[text](/help/path/to/file.md)`.
I collegamenti esterni utilizzano `https://` URL assoluti.
- Non utilizzare mai &quot;fai clic qui&quot; o &quot;collega&quot; come testo di collegamento. Evita URL non elaborati nel corpo del testo.
- Testo alternativo: `![alt text](path/to/image.png)`. Frasi intere, senza &quot;Questa immagine mostra...&quot;.
- Schermate: solo tema chiaro, nessun dato cliente, nessuna interfaccia utente di terze parti, nessuna immagine del codice.
- I blocchi di codice delimitati utilizzano tre apici retroversi con un identificatore di lingua. I blocchi di codice non sono
localizzato (non è necessario inserire DNL/UICONTROL).
- Video: `>[!VIDEO](url?quality=12&learn=on)`. Non eseguire mai la riproduzione automatica; fornisci sempre una trascrizione
o scritta alternativa.

### Ammonizioni

```markdown
>[!NOTE]
>
>Note content here.
```

Una riga `>` vuota deve separare la riga del tag dal contenuto; ogni riga di continuazione inizia
con `>`. NON inserire `[!NOTE]` immediatamente dopo un blocco `[!CONTEXTUALHELP]`.

### Messaggi popover della Guida contestuali (`[!CONTEXTUALHELP]`)

`[!CONTEXTUALHELP]` blocca le descrizioni comandi di feed popopover che ingegnerizzano i cavi nell&#39;esperienza
Interfaccia utente di Platform. Risiedono nella documentazione ma vengono riprodotti come finestre a comparsa interne al prodotto tramite un feed JSON
generato in fase di generazione della build.

```markdown
## Configure file names {#configure-file-names}

>[!CONTEXTUALHELP]
>id="platform_destinations_activate_filename"
>title="Configure file name"
>abstract="For file-based destinations, a unique file name is generated per segment. Use the file name editor to create and edit a unique file name or keep the default name."
>additional-url="https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/activate-batch-profile-destinations.html?lang=it#file-names" text="Learn more in documentation"
```

Campi obbligatori: `id`, `title`, `abstract`. Tutto il resto è facoltativo.

**Posizionamento:**
- Il blocco deve seguire direttamente un&#39;intestazione (`#`, `##` o `###`) con un&#39;intestazione esplicita
ID ancoraggio (ad esempio, `### Section title {#section-id}`). Nessun paragrafo o altro contenuto tra
l’intestazione e il blocco, oppure la finestra a comparsa non verrà riprodotta.
- Più blocchi `[!CONTEXTUALHELP]` possono apparire consecutivamente nella stessa sezione (ad esempio,
uno per campo).
- NON inserire un blocco `[!NOTE]` subito dopo un blocco `[!CONTEXTUALHELP]`. Si rompe
rendering su Experience League (limitazione nota della piattaforma).

**Sintassi ID:**
- Formato: `id="platform_<yourarea>_<workflow>_<uiitem>"`, ad esempio
  `id="platform_destinations_activate_deduplicationkey"`.
- Gli ID possono contenere lettere maiuscole.
- Gli ID devono essere univoci in tutto il set di documenti (selezionati al momento della compilazione). Lo stesso ID può essere riutilizzato
su più posizioni dell’interfaccia utente per progettazione, che produce contenuti popover identici in
ogni punto. È previsto.

**Collegamenti all&#39;interno di un popover, utilizzare `additional-url`, non HTML in linea:**
- Per aggiungere un collegamento, utilizzare una riga separata: `>additional-url="URL" text="Link text"`. NON incorporare
  `<a href="...">` o markdown `[text](url)` all&#39;interno della stringa `abstract` a questo scopo.
- Il valore `additional-url` DEVE includere `.html` nel percorso, altrimenti il collegamento non verrà visualizzato in
interfaccia utente (ad esempio, `https://experienceleague.adobe.com/docs/experience-platform/path/to/page.html#anchor`,
non il più recente modulo `/en/docs/...` senza estensione utilizzato nei collegamenti corpo-testo altrove).
- Massimo due `additional-url` righe per blocco.
- Un primo collegamento viene generato automaticamente dall’intestazione della sezione durante la generazione Jenkins. Tu
non aggiungerlo manualmente e non puoi rinominarlo.

**Altra sintassi supportata:**
- Il campo `abstract` supporta HTML/markdown di base per enfasi e struttura: `<b>`,
  `<br>`, `<ul><li>`, `**bold**`.
- I collegamenti video sono supportati tramite lo stesso meccanismo `additional-url`/`text`, che punta a un
URL video diretto o URL YouTube.

**Nota flusso di lavoro:** quando si invia un nuovo ID popover all&#39;interfaccia utente/team tecnico (in genere tramite un
Jira ticket), fornisci anche un URL di fallback (preferisci un goURL, se presente, per quella pagina) e
il percorso dell’interfaccia utente. Questo fallback è separato da `additional-url` utilizzato nella documentazione
markdown.

### Elenchi e tabelle

- Utilizza `*` o `-` in modo coerente all&#39;interno di un articolo; non combinare.
- Gli elenchi numerati utilizzano `1.` per ogni elemento. Le procedure in un unico passaggio utilizzano un punto elenco, non `1.`.
- Nessuna casella di controllo per l&#39;elenco di attività in stile GitHub (`- [ ]`). Non supportato in Experience League.
- Racchiudere elenchi e tabelle con linee vuote. Mantieni le voci elenco in parallelo dal punto di vista grammaticale.

### Denominazione di file e cartelle

- Nomi di file Markdown: in minuscolo con trattini, senza lettere maiuscole/trattini bassi/punti/spazi.
- Usare slug descrittivi (`create-calculated-metric.md`), non nomi nudi come `overview.md`.
- Le immagini vengono inserite in una sottocartella `assets/`; le immagini che non devono essere localizzate vengono inserite
  `do-not-localize/`.

## &#x200B;6. Convenzioni struttura e sommario

- Tre tipi di contenuto separati: **Concetto** (cosa/perché, intestazioni sostantive), **Attività**
(come, titoli imperativi, sempre preceduti da un concetto), **Riferimento** (campi,
tabelle).
- Passaggi: ogni è una singola frase completa che inizia con un verbo o con l&#39;obiettivo. Target 7
passaggi per attività, massimo 10; suddividere procedure più lunghe in sottoattività.
- TOC.md: voci di maiuscole/minuscole della frase, ID di ancoraggio validi su ogni intestazione di sezione, nessun duplicato
voci di file, nessun commento dell&#39;elenco intermedio.
- Nascondi una pagina dalla navigazione con `{hide-from-toc}` in `TOC.md` (non frontmatter). Nascondi
da motori di ricerca con `hide: true` in frontmatter.
- Denominazione ramo: nessun prefisso del nome utente. Utilizza il numero del biglietto Jira e una barra del titolo
(e.g., `PLAT-12345-Update-Guardrail-Limits`). Assegna allo stesso modo il nome della filiale e il titolo della PR.

## &#x200B;7. Controllo ortografia e punteggiatura

- Inglese americano: colore, riconoscere, licenza, mentre, scadenza, metro, tra
(non colore, riconoscimento, licenza, mentre, scadenza, contatore, tra).
- Riserva le virgolette per le persone tra virgolette; non citare le stringhe dell’interfaccia utente (utilizza il grassetto +
  &grave;&grave;).
- Usa il corsivo per i termini utilizzati come termini (*profilo*, non &quot;profilo&quot;). Utilizzare gli apici retroversi per il codice,
parametri, nomi di file e testo digitato.
- Grassetto solo per gli elementi dell&#39;interfaccia utente nelle procedure (con &grave;&grave;) e i termini chiave all&#39;inizio
introduzione.
- Non ci sono punti e virgola, non ci sono trattini/trattini in prosa, né regole orizzontali (vedere paragrafo 1).

## &#x200B;8. Controlla elenco di controllo

Prima di terminare qualsiasi modifica, verifica quanto segue:

- Voce focalizzata sull&#39;utente, voce attiva, seconda persona, nessun &quot;ti permette di&quot;/&quot;ti consente di&quot;
- Frasi ≤20 parole, paragrafi ≤125 parole
- Titoli: maiuscole/minuscole, ≤5 parole/69 caratteri, seguiti da corpo del testo, nessun livello saltato
- Correggere i nomi e i moduli dei prodotti; nessun termine obsoleto, solo interno o non inclusivo
- &grave;&grave; su ogni elemento dell&#39;interfaccia utente nei passaggi; `[!DNL]` su ogni nome di prodotto/terze parti
- Nessun tag all’interno di blocchi di codice; campi di metadati con tag racchiusi tra virgolette
- Correzione della sintassi di ammonizione; marcatori di elenco coerenti; nessun elenco di attività; nessuna regola orizzontale
- Il testo alternativo è descrittivo e completo; nessun &quot;click here&quot;; nessun linguaggio spaziale/direzionale
- Nessun colore utilizzato da solo per trasmettere le informazioni; i video non vengono riprodotti automaticamente
- Presenza frontmatter richiesta; collegamenti interni relativi alla radice; nomi file con sillabazione minuscola
