---
title: Gestisci [!DNL ChatGPT Ads] campagne pubblicitarie conversazionali
description: Scopri come creare e gestire [!DNL ChatGPT Ads] campagne, gruppi di annunci e annunci tramite chat card, una funzione beta che inserisce gli annunci all'interno delle conversazioni dell'assistente AI.
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
    internal-label: Demand Side Platform
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: cb25ab04e8fef5d00935e5325a897b1de97e2674
workflow-type: tm+mt
source-wordcount: '1188'
ht-degree: 0%
---
# Gestisci [!DNL ChatGPT Ads] campagne pubblicitarie di conversazione, gruppi di annunci e annunci

*funzionalità Beta*

Gestisci [!DNL ChatGPT Ads] campagne, gruppi di annunci e annunci tramite chat in un [account di annunci conversational](account-manage.md).

L&#39;utilizzo di [!DNL ChatGPT Ads] alla fine del mese viene fatturato con le altre fatture. Per domande sulla fatturazione, contatta il team del tuo account Adobe.

## Visualizzazione [!UICONTROL Conversational Ads Beta] > [!UICONTROL Campaigns] {#campaign-views-about}

La visualizzazione [!UICONTROL Conversational Ads Beta] > [!UICONTROL Campaigns] include tre schede: [!UICONTROL Campaigns], [!UICONTROL Ad Groups] e [!UICONTROL Ads]. Ogni scheda elenca le campagne, i gruppi di annunci o gli annunci per l’account selezionato, insieme ai dati sulle prestazioni per l’intervallo di date selezionato. I dati sulle prestazioni a livello di campagna, gruppo di annunci e annuncio includono [!UICONTROL Impressions], [!UICONTROL Clicks], [!UICONTROL Spend], [!UICONTROL CTR], [!UICONTROL Avg CPC] e [!UICONTROL Avg CPM].

>[!NOTE]
>
>* Le organizzazioni configurate per visualizzare i valori delle imposte nelle visualizzazioni dei rapporti non potranno visualizzarli per [!DNL ChatGPT Ads]. Calcola manualmente i valori delle imposte.

### Azioni disponibili

<!-- * [Refresh information about your campaigns](#refresh) -- Add topic below. -->

* [Crea](#campaign-create) o [modifica](#campaign-edit) una campagna

* [Crea](#ad-group-create) o [modifica](#ad-group-edit) un gruppo di annunci per una campagna esistente

* [Crea](#ad-create) o [modifica](#ad-edit) un annuncio per un gruppo di annunci esistente

* [Attivare o sospendere una campagna, un gruppo di annunci o un annuncio](#pause-activate)

* [Archiviare una campagna, un gruppo di annunci o un annuncio](#archive)

* [Espandere campagne in gruppi di annunci e annunci](#drill-down)

* [Aggiorna la campagna, il gruppo di annunci o l’elenco di annunci](#refresh)

## Campagne

### Crea una campagna pubblicitaria conversazionale [!DNL ChatGPT Ads] {#campaign-create}

Quando crei una campagna, puoi facoltativamente crearne il primo gruppo di annunci e l’annuncio. Ogni passaggio crea l&#39;entità non appena si fa clic su **[!UICONTROL Next]**, quindi non è possibile tornare a un passaggio precedente. Se è necessario modificare qualcosa in un secondo momento, modificarlo dopo la chiusura della procedura guidata.

1. Nel menu principale, fare clic su **[!UICONTROL Conversational Ads Beta]**.

1. Nel sottomenu fare clic sulla scheda **[!UICONTROL Campaigns]**.

1. In alto a destra, seleziona un inserzionista e un account [!DNL ChatGPT Ads].

1. In alto a destra, fare clic su **[!UICONTROL Create]>[!UICONTROL Campaign]**.

1. Specifica le [impostazioni campagna](#campaign-settings).

1. Fare clic su **[!UICONTROL Next]** per salvare le impostazioni della campagna.

1. Effettua una delle seguenti operazioni:

   * Se non desideri creare un gruppo di annunci per la campagna, fai clic su **[!UICONTROL Close]**.

     >[!TIP]
     >
     >Per creare un gruppo di annunci o un annuncio in un secondo momento, vedi &quot;[Creare un gruppo di annunci](#ad-group-create)&quot; o &quot;[Creare un annuncio](#ad-create).&quot;

   * (Facoltativo) Crea un gruppo di annunci:

     1. Specifica le [impostazioni del gruppo di annunci](#ad-group-settings).

     1. Fare clic su **[!UICONTROL Next]** per salvare le impostazioni del gruppo di annunci.

     1. (Facoltativo) Se non desideri creare un annuncio per la campagna, fai clic su **[!UICONTROL Close]**.

   * (Facoltativo dopo aver creato un gruppo di annunci) Crea un annuncio:

     1. Specifica le [impostazioni annuncio](#ad-settings).

     1. Fare clic su **[!UICONTROL Create ad]**.

### Modifica impostazioni campagna pubblicitaria conversazionale [!DNL ChatGPT Ads] {#campaign-edit}

1. Nel menu principale, fare clic su **[!UICONTROL Conversational Ads Beta]**.

1. Nel sottomenu a sinistra, fare clic su **[!UICONTROL Campaigns]**.

1. In alto a destra, seleziona un inserzionista e un account [!DNL ChatGPT Ads].

1. (Se necessario) Sopra la tabella dati, fare clic sulla scheda **[!UICONTROL Campaigns]**.

1. Posizionare il cursore sulla riga e fare clic su **[!UICONTROL ...]>[!UICONTROL Edit]**.

1. Modifica le [impostazioni campagna](#campaign-settings), [impostazioni gruppo annunci](#ad-group-settings) e [impostazioni annunci](#ad-settings).

1. Fare clic su **[!UICONTROL Save]**.

### [!DNL ChatGPT Ads] impostazioni campagna pubblicitaria conversazionale {#campaign-settings}

**[!UICONTROL Campaign name]:** Nome univoco per la campagna. Il nome deve contenere almeno tre caratteri.

**[!UICONTROL Campaign type]:** (sola lettura) *Standard* è l&#39;unico tipo disponibile.

**[!UICONTROL Objective]:** La metrica su cui focalizzare la campagna: *Raggiungi* o *Clic*. L’obiettivo determina il tipo di offerta per i gruppi di annunci della campagna.

**[!UICONTROL Locations]:** (facoltativo) una o più posizioni specifiche di destinazione. Per eseguire il targeting di tutte le posizioni, lascia vuota questa impostazione. Per specificare una posizione specifica, immettere almeno due lettere da visualizzare in un punto qualsiasi del nome, quindi fare clic sul nome all&#39;interno dei risultati della ricerca.

**[!UICONTROL Budget type]:** *Budget giornaliero* o *Budget durata*.

**[!UICONTROL Budget]:** Il budget per il tipo di budget specificato. Il valore deve essere maggiore di zero (0).

**[!UICONTROL Start date]:** La data di inizio della campagna, nel fuso orario dell&#39;account.

**[!UICONTROL Set an end date]:** (facoltativo) consente di specificare una data di fine per la campagna. Quando si seleziona questa opzione, specificare **[!UICONTROL End date]**.

## Gruppi di annunci

### Crea un gruppo di annunci [!DNL ChatGPT Ads] per una campagna esistente {#ad-group-create}

1. Nel menu principale, fare clic su **[!UICONTROL Conversational Ads Beta]**.

1. Nel sottomenu fare clic sulla scheda **[!UICONTROL Campaigns]**.

1. In alto a destra, seleziona un inserzionista e un account [!DNL ChatGPT Ads].

1. In alto a destra, fare clic su **[!UICONTROL Create]>[!UICONTROL Ad Group]**.

1. Specifica le [impostazioni del gruppo di annunci](#ad-group-settings), inclusa la campagna principale.

1. Fare clic su **[!UICONTROL Create ad group]**.

## Modifica un gruppo di annunci [!DNL ChatGPT Ads] {#ad-group-edit}

1. Nel menu principale, fare clic su **[!UICONTROL Conversational Ads Beta]**.

1. Nel sottomenu a sinistra, fare clic su **[!UICONTROL Campaigns]**.

1. In alto a destra, seleziona un inserzionista e un account [!DNL ChatGPT Ads].

1. Sopra la tabella dati, fare clic sulla scheda **[!UICONTROL Ad Groups]**.

1. Posizionare il cursore sulla riga e fare clic su **[!UICONTROL ...]>[!UICONTROL Edit]**.

1. Modifica le impostazioni del [gruppo di annunci](#ad-group-settings).

1. Fare clic su **[!UICONTROL Save]**.

### Impostazioni gruppo di annunci [!DNL ChatGPT Ads] {#ad-group-settings}

**[!UICONTROL Parent campaign]:** (Solo gruppi di annunci per campagne esistenti) La campagna a cui appartiene il gruppo di annunci.

**[!UICONTROL Ad group name]:** Nome univoco per il gruppo di annunci. Il nome deve contenere almeno tre caratteri.

**[!UICONTROL Maximum CPC bid]** o **[!UICONTROL Maximum CPM bid]:** L&#39;importo massimo che pagherai per ogni clic o per 1.000 impression. Il valore deve essere maggiore di zero (0). L&#39;obiettivo della campagna determina il campo dell&#39;offerta: *Le campagne Clic* mostrano **[!UICONTROL Maximum CPC bid]** e le campagne *Raggiungi* mostrano **[!UICONTROL Maximum CPM bid]**.

>[!TIP]
>
>Le offerte più alte possono aggiudicarsi più aste.

**[!UICONTROL Context hints]:** (Facoltativo) Una descrizione delle conversazioni, degli argomenti o delle parole chiave per cui i prodotti o i servizi sono rilevanti. Questi suggerimenti guidano la corrispondenza, ma non sono regole di targeting di corrispondenza esatta.

## Annunci

### Crea un annuncio scheda chat [!DNL ChatGPT Ads] per un gruppo di annunci esistente {#ad-create}

1. Nel menu principale, fare clic su **[!UICONTROL Conversational Ads Beta]**.

1. Nel sottomenu fare clic sulla scheda **[!UICONTROL Campaigns]**.

1. In alto a destra, seleziona un inserzionista e un account [!DNL ChatGPT Ads].

1. In alto a destra, fare clic su **[!UICONTROL Create]>[!UICONTROL Ad]**.

1. Specifica le [impostazioni annuncio](#ad-settings), inclusi la campagna principale e il gruppo di annunci.

1. Fare clic su **[!UICONTROL Create ad]**.

## Modifica un annuncio scheda chat di [!DNL ChatGPT Ads] {#ad-edit}

1. Nel menu principale, fare clic su **[!UICONTROL Conversational Ads Beta]**.

1. Nel sottomenu a sinistra, fare clic su **[!UICONTROL Campaigns]**.

1. In alto a destra, seleziona un inserzionista e un account [!DNL ChatGPT Ads].

1. Sopra la tabella dati, fare clic sulla scheda **[!UICONTROL Ads]**.

1. Posizionare il cursore sulla riga e fare clic su **[!UICONTROL ...]>[!UICONTROL Edit]**.

1. Modifica le impostazioni di [ad](#ad-settings).

1. Fare clic su **[!UICONTROL Save]**.

### Impostazioni annuncio scheda chat di [!DNL ChatGPT Ads] {#ad-settings}

**[!UICONTROL Parent campaign]** e **[!UICONTROL Parent ad group]:** (solo annunci nei gruppi di annunci esistenti) La campagna e il gruppo di annunci a cui appartiene l&#39;annuncio.

**[!UICONTROL Ad name]:** Nome univoco per l&#39;annuncio. Il nome deve contenere almeno tre caratteri.

**[!UICONTROL Ad URL (Link)]:** URL della pagina di destinazione, a partire da `http://` o `https://`.

**[!UICONTROL Title (headline)]:** Il titolo dell&#39;annuncio. Il titolo deve contenere tra 3 e 50 caratteri. **Nota:** in alcuni tipi di posizionamento il titolo potrebbe essere troncato.

**[!UICONTROL Description]:** Il corpo del testo dell&#39;annuncio. La descrizione deve contenere tra 3 e 100 caratteri.

**[!UICONTROL Ad image]:** immagine JPG o PNG da includere nell&#39;annuncio. Per caricare un&#39;immagine, fare clic su (nuovi annunci) **[!UICONTROL Upload image (PNG/JPG)]** o **[!UICONTROL Change image]**, quindi individuare e selezionare un file nel dispositivo o nella rete.

**[!UICONTROL Preview]:** Anteprima dell&#39;annuncio, in base alle impostazioni dell&#39;annuncio.

## Attiva o sospende una campagna, un gruppo di annunci o un annuncio di [!DNL ChatGPT Ads] {#pause-activate}

1. Nel menu principale, fare clic su **[!UICONTROL Conversational Ads Beta]**.

1. Nel sottomenu a sinistra, fare clic su **[!UICONTROL Campaigns]**.

1. In alto a destra, seleziona un inserzionista e un account [!DNL ChatGPT Ads].

1. Nella scheda **[!UICONTROL Campaigns]**, **[!UICONTROL Ad Groups]** o **[!UICONTROL Ads]** trovare la riga.

1. Nella colonna **[!UICONTROL Active]** eseguire una delle operazioni seguenti:

   * Per attivare un elemento in pausa, attiva l’interruttore (a destra).

   * Per mettere in pausa un elemento attivo, disattivare l&#39;interruttore (a sinistra).

## Archivia una campagna, un gruppo di annunci o un annuncio di [!DNL ChatGPT Ads] {#archive}

L&#39;archiviazione rimuove definitivamente la campagna, il gruppo di annunci o l&#39;annuncio dalle visualizzazioni [!UICONTROL Conversational Ads].

1. Nel menu principale, fare clic su **[!UICONTROL Conversational Ads Beta]**.

1. Nel sottomenu a sinistra, fare clic su **[!UICONTROL Campaigns]**.

1. In alto a destra, seleziona un inserzionista e un account [!DNL ChatGPT Ads].

1. Nella scheda **[!UICONTROL Campaigns]**, **[!UICONTROL Ad Groups]** o **[!UICONTROL Ads]**, posizionare il cursore sulla riga e fare clic su **[!UICONTROL ...]>[!UICONTROL Archive]**.

## Espandere da [!DNL ChatGPT Ads] campagne a gruppi di annunci e annunci {#drill-down}

* Fare clic su una riga della campagna per visualizzare solo i gruppi di annunci nella scheda **[!UICONTROL Ad Groups]** oppure fare clic su una riga del gruppo di annunci per visualizzare solo gli annunci nella scheda **[!UICONTROL Ads]**.

Per rimuovere il filtro e visualizzare tutte le righe nella visualizzazione, fare clic su **X** nel filtro sopra la tabella dati.

## Aggiorna la campagna, il gruppo di annunci o l’elenco di annunci {#refresh}

Visualizza nuovamente l’elenco di campagne, gruppi di annunci o annunci quando altri utenti possono aver apportato modifiche o aggiunte.

1. Nel menu principale, fare clic su **[!UICONTROL Conversational Ads Beta]**.

1. Nella visualizzazione **[!UICONTROL Campaigns]**, **[!UICONTROL Ad Groups]** o **[!UICONTROL Ads]**, fare clic su **[!UICONTROL Refresh]** sopra la tabella dati.

>[!MORELIKETHIS]
>
>* [Gestione account di annunci conversazionali](account-manage.md)
