---
title: Visualizzare i siti, gli annunci, la frequenza e i dettagli di inventario per un posizionamento
description: Scopri come visualizzare i siti target, gli annunci, la frequenza e i dati di inventario per un posizionamento.
feature: DSP Placements
exl-id: b58b442c-2fb8-4a78-9be9-d85aa83136e2
source-git-commit: 0f022babeab6c044949760cedc103323eb0cc950
workflow-type: tm+mt
source-wordcount: '658'
ht-degree: 0%

---

# Visualizzare i siti, gli annunci, la frequenza e i dettagli di inventario per un posizionamento

Per ogni posizionamento, puoi [aprire una (visualizzazione dettagli [!UICONTROL Inspector])](placement-details-view.md), che elenca tutti i siti target, gli annunci e le offerte in un posizionamento. Include anche i dati di frequenza per il posizionamento. Facoltativamente, puoi esportare i dati da qualsiasi scheda.

![Ispettore posizionamento](/help/dsp/assets/placement-inspector.png)

## Informazioni nel posizionamento [!UICONTROL Inspector] {#placement-inspector}

* **[!UICONTROL Sites]:** Tutti i siti in cui il posizionamento ha avuto impression.

  La scheda [!UICONTROL Sites] include le funzionalità di ricerca e filtro, le stesse opzioni di visualizzazione delle colonne standard e personalizzate disponibili nella pagina principale e un pulsante [!UICONTROL Exclude] in ogni riga per escludere rapidamente un sito dal posizionamento.

* **[!UICONTROL Ads]:** tutti gli annunci nel posizionamento.

  La scheda [!UICONTROL Ads] include le funzionalità di ricerca e filtro, le stesse opzioni di visualizzazione delle colonne standard e personalizzate disponibili nella pagina principale e i pulsanti di azione rapida in ogni riga, ad esempio [!UICONTROL View Ad Approvals].

* **[!UICONTROL Frequency]:** dati per ogni livello di frequenza annuncio per il posizionamento, inclusi:
   * il livello di frequenza dell’annuncio (ad esempio &quot;1&quot; per tutte le istanze in cui gli utenti hanno visto un annuncio una volta)
   * numero univoco stimato di dispositivi/browser o persone (a seconda del [!UICONTROL Cross Device Level] specificato per la campagna) che hanno ricevuto impression al livello di frequenza specificato
   * il numero stimato di impression al livello di frequenza specificato
   * la frequenza media stimata per il livello di frequenza specificato. Questo valore è uguale a (Impression stimate)/(Valori univoci stimati).

* **[!UICONTROL Inventory]:** Informazioni su tutte le offerte target del posizionamento.

  La scheda [!UICONTROL Inventory] consente di risolvere rapidamente i problemi visualizzando le statistiche sulle prestazioni, ad esempio [!UICONTROL Auctions], [!UICONTROL Bids] e [!UICONTROL Win Rate]. La scheda include le funzionalità di ricerca e filtro, le stesse opzioni di visualizzazione colonne standard e personalizzate disponibili nella pagina principale e i pulsanti di azione rapida in ogni riga, inclusi [!UICONTROL Edit], [!UICONTROL View Report] e [[!UICONTROL Auction Insights] per ulteriori informazioni sulla risoluzione dei problemi](/help/dsp/inventory/private-deal-auction-insights.md).

## Apri [!UICONTROL Placement Inspector] {#inspector-open}

1. Apri la vista posizionamenti per la campagna o il pacchetto principale:

   * Visualizza tutti i posizionamenti all’interno della campagna principale:

      1. Nel menu principale, fare clic su **[!UICONTROL Campaigns]**.

      1. Fai clic sul nome della campagna.

      1. Fare clic sulla scheda **[!UICONTROL Placements]**.

   * Visualizza tutti i posizionamenti all’interno del pacchetto principale:

      1. Nel menu principale, fare clic su **[!UICONTROL Campaigns]**.

      1. Fai clic sul nome della campagna.

      1. Fare clic sulla scheda **[!UICONTROL Packages]**.

      1. Fare clic sul nome del pacchetto padre.

1. Tenere premuto il cursore sulla riga di posizionamento e fare clic su **[!UICONTROL ...]** > **[!UICONTROL Analyze]** > **[!UICONTROL Inspector]**.

1. (Facoltativo) [Modifica la vista a colonne](campaign-data-views-manage.md#column-view-change) in base alle esigenze per visualizzare le metriche richieste.

1. (Facoltativo) Per esportare i dati in qualsiasi scheda, fare clic su ![Altro](/help/search-social-commerce/assets/more.png "Altro") in alto a destra, quindi fare clic su **[!UICONTROL Export]**.

   I dati vengono salvati nella cartella di download predefinita del browser come rapporto in formato XLSM.

## Rimuovere un annuncio da un posizionamento da [!UICONTROL Placement Inspector] {#remove-ads-placement-inspector}

1. [Apri [!UICONTROL Placement Inspector]](#inspector-open).

1. Fare clic sulla scheda **[!UICONTROL Ads]**.

1. Accanto al nome dell&#39;annuncio, fare clic su **[!UICONTROL ...]** > **[!UICONTROL Detach]**.

## Risoluzione dei problemi di inventario

| Problema | Possibile causa | Azioni da intraprendere |
| -----------| ---------- | ---------- |
| [!UICONTROL Zero Auctions] | L&#39;editore non ha iniziato a inviare richieste di offerta. | Contatta l’editore per attivare l’offerta. |
| | L’offerta è stata impostata in modo errato, ad esempio inserendo un ID offerta esterno errato. | Conferma i dettagli dell’offerta e modifica l’offerta. |
| [!UICONTROL Auctions but no Bids] | Il targeting del posizionamento non corrisponde alle richieste di offerta in arrivo per l’offerta. <br><br> Ad esempio, un posizionamento potrebbe essere indirizzato a un&#39;area geografica non idonea per l&#39;operazione. | Modifica le destinazioni di posizionamento in base alle esigenze per evitare incongruenze di targeting. |
| | Il posizionamento non ha un annuncio attivo con il tipo di file multimediale richiesto per l’offerta. | Crea e allega al posizionamento un annuncio con il tipo di file multimediale corretto. |
| | Il posizionamento non dispone di un budget adeguato. | Aumenta il budget di posizionamento per consentire le offerte sulle richieste in arrivo. |
| | Le date del volo di posizionamento non si sovrappongono alle date di consegna delle impression per l’offerta. | Modifica le date di volo del posizionamento in base alle esigenze. |
| [!UICONTROL Low Win Rate] | L&#39;offerta massima del posizionamento (minima o fissa) è inferiore al minimo richiesto dalla trattativa. | Aumentare il valore di [!UICONTROL Max Bid] del posizionamento in base alle esigenze. |
| | Il posizionamento utilizza filtri pre-offerta che limitano le offerte. | Abbassa le soglie dei filtri pre-offerta per consentire un maggior numero di offerte. |
| | Il targeting del pubblico per il posizionamento è troppo restrittivo. | Verifica se le destinazioni del pubblico specificato hanno un numero sufficiente di utenti attivi e, se possibile, espandi il pubblico. |

>[!MORELIKETHIS]
>
>* [Tipi di rapporti sulle prestazioni nelle visualizzazioni di gestione delle campagne](campaign-reports-about.md)
>* [Gestione Delle Visualizzazioni Dati Della Campagna](campaign-data-views-manage.md)
