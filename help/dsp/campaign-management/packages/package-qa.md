---
title: Rivedere e modificare le impostazioni dei pacchetti utilizzando i bulksheet
description: Scopri come rivedere e modificare le impostazioni dei pacchetti chiave in blocco utilizzando i fogli di calcolo.
feature: DSP Packages
exl-id: bf52de27-db48-40e2-bb55-a2c27a1924ad
source-git-commit: fa4cee46135c85849daa7faa4059c77fc753c2c8
workflow-type: tm+mt
source-wordcount: '1184'
ht-degree: 0%

---

# Rivedere e modificare le impostazioni dei pacchetti utilizzando i bulksheet

È possibile scaricare le impostazioni per uno o più pacchetti in formato XLSX ([!DNL Microsoft Excel] spreadsheet) per la revisione. Il foglio di calcolo include una scheda separata con le informazioni sul volo.

Per aggiornare più impostazioni contemporaneamente, è possibile effettuare una delle seguenti operazioni:

* Apporta le modifiche necessarie per selezionare i campi, salvare il file e caricare nuovamente il file di bulksheet modificato in DSP.

* Per apportare modifiche ad altri pacchetti e alle impostazioni per qualsiasi posizionamento o annuncio, scarica un modello di bulksheet vuoto che includa schede per ogni tipo di componente della campagna, immetti o incolla le impostazioni nuove o aggiornate nel file di modello, quindi carica il file per apportare le modifiche. Per istruzioni, consulta &quot;[Rivedere e modificare le impostazioni dei componenti di Campaign utilizzando i bulksheet](/help/dsp/campaign-management/campaign-components-review-edit.md).&quot;

I campi modificabili includono la maggior parte delle impostazioni normalmente modificabili.

>[!TIP]
>
>Per modificare rapidamente più campi per uno o più pacchetti, vedere &quot;[Modifica pacchetti](/help/dsp/campaign-management/packages/package-edit.md)&quot;.

## Scaricare le impostazioni per tutti i pacchetti in una campagna

Quando scarichi le impostazioni per tutti i pacchetti di una campagna, il foglio di calcolo include schede separate per le impostazioni del pacchetto e per le informazioni sul volo. Facoltativamente, puoi includere le impostazioni per i posizionamenti e gli annunci associati ai pacchetti; vengono incluse schede aggiuntive per le impostazioni di posizionamento e annunci.

1. Nel menu principale, fare clic su **[!UICONTROL Campaigns]**.

1. Fai clic sul nome della campagna.

1. In alto a destra, fare clic su **[!UICONTROL ...]** > **[!UICONTROL Download QA sheet]**.

1. Nella finestra di dialogo [!UICONTROL QA Sheet Download] deselezionare i componenti di Campaign di cui si desidera escludere le impostazioni dal file scaricato e quindi fare clic su **[!UICONTROL Download]**.

Per impostazione predefinita, sono selezionate le impostazioni per tutti i posizionamenti e gli annunci associati ai pacchetti.

Un messaggio di notifica indica quando il file è disponibile per il download.

1. Per scaricare il file, effettuare una delle seguenti operazioni:

   * Nel messaggio di notifica, fare clic su **[!UICONTROL Download].**

   * Nella parte destra della barra dei menu superiore, fai clic su ![Processi](/help/dsp/assets/downloads.png). Fare clic su **[!UICONTROL Download]** accanto al processo.

     Il file viene salvato nella cartella Download del browser. Per un elenco delle colonne incluse, vedere &quot;[Colonne di posizionamento nei fogli di calcolo scaricati/caricati](#qa-sheet-columns)&quot;.

>[!NOTE]
>
>Non puoi modificare e ricaricare i fogli di controllo qualità a livello di campagna. Per apportare modifiche alle impostazioni del componente Campaign in questi file, scarica un modello di bulksheet separato, immetti o incolla righe dal foglio di controllo qualità nel modello di bulksheet e salva il file, quindi carica il bulksheet popolato. Per istruzioni, consulta &quot;[Rivedere e modificare le impostazioni dei componenti di Campaign utilizzando i bulksheet](/help/dsp/campaign-management/campaign-components-review-edit.md).&quot;

## Impostazioni di download per uno o più pacchetti

Quando si scaricano le impostazioni per pacchetti specifici, il file del bulksheet include schede separate per le impostazioni del pacchetto e per le informazioni sul volo e il file è modificabile.

1. Nel menu principale, fare clic su **[!UICONTROL Campaigns]**.

1. Fai clic sul nome della campagna.

1. Nel sottomenu fare clic su **[!UICONTROL Packages]**.

1. Nella barra degli strumenti Azioni in blocco fare clic su **[!UICONTROL ...]** > **[!UICONTROL Download Bulksheet]**.

   Un messaggio di notifica indica quando il file bulksheet è disponibile per il download.

1. Per scaricare il bulksheet, effettuare una delle seguenti operazioni:

   * Nel messaggio di notifica, fare clic su **[!UICONTROL Download].**

   * Nella parte destra della barra dei menu superiore, fai clic su ![Processi](/help/dsp/assets/downloads.png). Fare clic su **[!UICONTROL Download]** accanto al processo.

     Il file viene salvato nella cartella Download del browser. Per un elenco delle colonne incluse, vedere &quot;[Colonne di posizionamento nei fogli di calcolo scaricati/caricati](#qa-sheet-columns)&quot;.

<!-- I don't think I need this here

## Download a Bulksheet Template {#download-template}

You can optionally download a blank bulksheet template that includes tabs for each type of campaign component. You can later add rows to any tab on the template and [upload the edited file](##upload-bulksheet-package) to make changes. 

1. Click the name of the campaign.

1.  In the upper right, click **[!UICONTROL ...]** > **[!UICONTROL Download Bulksheet]**.

   The file is saved to the browser's Downloads folder. See "[Placement Columns in Downloaded/Uploaded Spreadsheets](#qa-sheet-columns)" for a list of the included columns.

-->

## Caricare un bulksheet con le impostazioni del pacchetto {#upload-bulksheet-package}

Puoi caricare le impostazioni dei pacchetti, inclusi i posizionamenti e gli annunci associati ai pacchetti, in un file bulksheet.

1. Nel menu principale, fare clic su **[!UICONTROL Campaigns]**.

1. Fai clic sul nome della campagna.

1. In alto a destra, fare clic su **[!UICONTROL ...]** > **[!UICONTROL Upload Bulksheet]**.

1. Nella finestra di dialogo [!UICONTROL Upload Bulksheet]:

   1. Trascinare e rilasciare un file nella casella oppure fare clic all&#39;interno della casella per selezionare un file dal dispositivo o dalla rete.

   1. Fare clic su **[!UICONTROL Upload]**.

1. (Facoltativo) Per verificare che gli aggiornamenti siano stati elaborati, fai clic su ![Processi](/help/dsp/assets/downloads.png) a destra della barra dei menu superiore.

## Colonne delle impostazioni dei pacchetti nei fogli di calcolo scaricati/caricati{#qa-sheet-columns-packages}

>[!TIP]
>
> In un foglio di calcolo scaricato, tutte le colonne modificabili sono evidenziate in blu.

### Scheda [!UICONTROL Package]

| Sezione | Colonna | Descrizione | Modificabile? |
|---------|--------|-------------|-----------|
| [!UICONTROL Basic details] | [!UICONTROL Package ID] | ID numerico del pacchetto. | — |
| [!UICONTROL Basic details] | [!UICONTROL Package Name] | Nome del pacchetto. | Sì |
| [!UICONTROL Basic details] | [!UICONTROL Status] | Stato del pacchetto: *[!UICONTROL active]* o *[!UICONTROL inactive]*. | Sì |
| [!UICONTROL Basic details] | [!UICONTROL Description] | Descrizione facoltativa del pacchetto. | Sì |
| [!UICONTROL Basic details] | [!UICONTROL 3rd-party fees - CPM] | Tariffa statica di terze parti da registrare come costo non fatturabile per 1000 impression, se applicabile. | Sì |
| [!UICONTROL Basic details] | [!UICONTROL 3rd-party fees - description] | Una descrizione facoltativa della tariffa della commissione di terzi, se applicabile. | Sì |
| [!UICONTROL Goals & Budget] | [!UICONTROL Package Start Date] | Data di inizio del pacchetto. | Sì |
| [!UICONTROL Goals & Budget] | [!UICONTROL Package End Date] | Data di fine del pacchetto. | Sì |
| [!UICONTROL Goals & Budget] | [!UICONTROL Pacing Level] | Livello al quale posizionare e limitare i posizionamenti nel pacchetto: *[!UICONTROL Package]* o *[!UICONTROL Placement]*. | — |
| [!UICONTROL Goals & Budget] | [!UICONTROL Budget] | Il budget del pacchetto. | Sì |
| [!UICONTROL Goals & Budget] | [!UICONTROL Budget Interval] | Intervallo di budget: &lt;i[!UICONTROL >Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]* o *[!UICONTROL All Time]*. | Sì |
| [!UICONTROL Goals & Budget] | [!UICONTROL Interval Cap] | Limite facoltativo dell&#39;intervallo di budget. | Sì |
| [!UICONTROL Goals & Budget] | [!UICONTROL Interval Cap Period] | Intervallo per il limite dell&#39;intervallo di budget facoltativo: &lt;i[!UICONTROL >Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]* o *[!UICONTROL All Time]*. | Sì |
| [!UICONTROL Goals & Budget] | [!UICONTROL Optimization Goal] | Obiettivo del pacchetto. | Sì |
| [!UICONTROL Goals & Budget] | [!UICONTROL Optimization Target] | Il valore target dell’obiettivo. | Sì |
| [!UICONTROL Goals & Budget] | [!UICONTROL Custom Goal Name] | (Pacchetti con solo gli obiettivi di ottimizzazione &quot;[!UICONTROL Highest Return on Ad Spend]&quot; e &quot;[!UICONTROL Lowest Cost per Acquisition]&quot;)Un [obiettivo personalizzato](/help/dsp/optimization/custom-goal.md) che include gli eventi di conversione o ricavi utilizzati per calcolare la metrica CPA o ROAS. | Sì |
| [!UICONTROL Goals & Budget] | [!UICONTROL Conversion Metric Name] | (Facoltativo; solo pacchetti con gli obiettivi di ottimizzazione &quot;[!UICONTROL Highest Return on Ad Spend]&quot; e &quot;[!UICONTROL Lowest Cost per Acquisition]&quot;) L&#39;evento di conversione finale o l&#39;importo di evento di ricavo/vendita da utilizzare per calcolare il ritorno sulla spesa pubblicitaria o il costo per acquisizione. | Sì |
| [!UICONTROL Goals & Budget] | [!UICONTROL Package Goal Type] | (Solo pacchetti con obiettivi di ottimizzazione personalizzati) Scopo del pacchetto, che consente di determinare come ottimizzare il pacchetto: *[!UICONTROL Prospecting]*, *[!UICONTROL Retargeting]* o *[!UICONTROL Other]*. | Sì |
| [!UICONTROL Goals & Budget] | [!UICONTROL Linked Package id for learning carryover] | (Solo pacchetti con obiettivi di ottimizzazione personalizzati) ID del pacchetto per un altro pacchetto i cui dati storici vengono utilizzati come input per l’ottimizzazione del pacchetto. | Sì |
| [!UICONTROL Goals & Budget] | [!UICONTROL Linked Package Name for learning carryover] | (Solo pacchetti con obiettivi di ottimizzazione personalizzati) Un altro pacchetto i cui dati storici vengono utilizzati come input per l’ottimizzazione del pacchetto. | — |
| [!UICONTROL Goals & Budget] | [!UICONTROL Pace on] | Indica se il pacchetto sta avanzando verso *[!UICONTROL budget]* o *[!UICONTROL primary_goal]* (per le impression). | — |
| [!UICONTROL Goals & Budget] | [!UICONTROL Primary Goal Amount] | (Quando distribuisci il pacchetto sulle impression) Il numero target di impression durante l’intervallo di tempo specificato. | Sì |
| [!UICONTROL Goals & Budget] | [!UICONTROL Primary Goal Interval] | (Quando distribuisci il pacchetto sulle impression) L’intervallo di tempo per il numero target di impression. | Sì |
| [!UICONTROL Goals & Budget] | [!UICONTROL Flight Pacing] | Strategia di andamento del volo per il pacchetto: *[!UICONTROL Even]*, *[!UICONTROL slightly ahead]*, *[!UICONTROL frontload]* o *[!UICONTROL aggressive frontload]*. | Sì |
| [!UICONTROL Goals & Budget] | [!UICONTROL Intraday Pacing] | Strategia di velocità infragiornaliera per il pacchetto: *[!UICONTROL Even]* o *[!UICONTROL ASAP]*. | Sì |
| [!UICONTROL Goals & Budget] | [!UICONTROL Frequency Cap] | Il limite di frequenza primario per il pacchetto durante il [!UICONTROL Frequency Cap Interval] specificato. | Sì |
| [!UICONTROL Goals & Budget] | [!UICONTROL Frequency Cap Interval] | Intervallo per il limite di frequenza primario: *[!UICONTROL Day]*, *[!UICONTROL Week]* o *[!UICONTROL Month]*. | Sì |
| [!UICONTROL Goals & Budget] | [!UICONTROL Frequency Cap Interval Value] | Il numero di settimane, giorni, ore o minuti a cui si applica l&#39;elemento primario [!UICONTROL Frequency Cap]. Ad esempio, se il limite principale è di 12 impression al mese, il valore qui sarà `12`. | Sì |
| [!UICONTROL Goals & Budget] | [!UICONTROL Secondary Frequency Cap] | Limite di frequenza secondario per il pacchetto durante il [!UICONTROL Secondary Frequency Cap Interval] specificato | Sì |
| [!UICONTROL Goals & Budget] | [!UICONTROL Secondary Frequency Cap Interval] | Tipo di intervallo per il limite di frequenza secondario: *[!UICONTROL Week]*, *[!UICONTROL Day]*, *[!UICONTROL Hour]* o *[!UICONTROL Minute]*. Il numero applicabile di settimane, giorni, ore o minuti è indicato da [!UICONTROL Secondary Frequency Cap Interval Value]. | Sì |
| [!UICONTROL Goals & Budget] | [!UICONTROL Secondary Frequency Cap Interval Value] | Il numero di settimane, giorni, ore o minuti a cui si applica [!UICONTROL Secondary Frequency Cap]. Ad esempio, se il limite secondario è di tre impression per sei ore, il valore qui sarà `6`. | Sì |
| [!UICONTROL Custom Flights] | [!UICONTROL Activate Custom Flights] | Indica se creare o meno voli non uniformi per il pacchetto *T* (true) o *F* (false). Una volta attivato il riflesso personalizzato e salvato il pacchetto, non è possibile disattivare il riflesso personalizzato né modificare la data di inizio del pacchetto. | — |
| [!UICONTROL Custom Flights] | [!UICONTROL Automatic Budget Rollover] | (Disponibile solo quando l&#39;opzione [!UICONTROL Activate Custom Flighting] è abilitata) Indica se aggiungere o meno automaticamente i budget rimanenti del volo precedente al budget esistente per il volo successivo: *T* (true) o *F* (false). | Sì |
| [!UICONTROL Error] | [!UICONTROL Error] | Eventuali errori rilevanti. | — |

### Scheda [!UICONTROL Package_Flights] {#qa-sheet-columns-package-flights}

| Sezione | Colonna | Descrizione | Modificabile? |
|---------|--------|-------------|-----------|
| [!UICONTROL Flight Details] | [!UICONTROL Package ID] | ID numerico del pacchetto. | — |
| [!UICONTROL Flight details] | [!UICONTROL Flight ID] | ID numerico del volo. | — |
| [!UICONTROL Flight details] | [!UICONTROL Flight Start Date] | La prima data del volo. | Sì |
| [!UICONTROL Flight details] | [!UICONTROL Flight End Date] | La data finale del volo. | Sì |
| [!UICONTROL Flight details] | [!UICONTROL Flight Budget] | L’obiettivo di spesa target per il volo. | Sì |
| [!UICONTROL Flight details] | [!UICONTROL Rollover] | (Pacchetti esistenti senza l&#39;opzione &quot;[!UICONTROL Automatically rollover remaining flight budget to next flight]&quot; abilitata) Un importo di budget potenzialmente non speso da aggiungere al volo successivo. | Sì |

>[!MORELIKETHIS]
>
>* [Verifica e modifica le impostazioni dei componenti della campagna tramite bulksheet](/help/dsp/campaign-management/campaign-components-review-edit.md)
>* [Modifica pacchetti](/help/dsp/campaign-management/packages/package-edit.md)
>* [Impostazioni pacchetto](/help/dsp/campaign-management/packages/package-settings.md)
