---
title: Visualizzare i siti, gli annunci, la frequenza e i dettagli di inventario per un posizionamento
description: Scopri come visualizzare i siti target, gli annunci, la frequenza e i dati di inventario per un posizionamento.
feature: DSP Placements
exl-id: b58b442c-2fb8-4a78-9be9-d85aa83136e2
source-git-commit: 1ac58da2d538cc682161ebc944a0412ad4a8af17
workflow-type: tm+mt
source-wordcount: '685'
ht-degree: 0%

---

# Visualizzare i siti, gli annunci, la frequenza e i dettagli di inventario per un posizionamento

Per ogni posizionamento, puoi [apri una (visualizzazione dettagli) [!UICONTROL Inspector])](placement-details-view.md), che elenca tutti i siti di destinazione, gli annunci e le offerte in un posizionamento. Include anche i dati di frequenza per il posizionamento. Facoltativamente, puoi esportare i dati da qualsiasi scheda.

![posizionamento Ispettore](/help/dsp/assets/placement-inspector.png)

## Informazioni nel posizionamento [!UICONTROL Inspector] {#placement-inspector}

* **[!UICONTROL Sites]:** Tutti i siti su cui il posizionamento ha avuto impressioni.

  Il [!UICONTROL Sites] Questa scheda include le funzioni di ricerca e filtro, le stesse opzioni di visualizzazione delle colonne standard e personalizzate disponibili nella pagina principale e una [!UICONTROL Exclude] in ogni riga, in modo da poter escludere rapidamente un sito dal posizionamento.

* **[!UICONTROL Ads]:** Tutti gli annunci nel posizionamento.

  Il [!UICONTROL Ads] Questa scheda include le funzioni di ricerca e filtro, le stesse opzioni di visualizzazione delle colonne standard e personalizzate disponibili nella pagina principale e i pulsanti di azione rapida in ogni riga, ad esempio [!UICONTROL Pause] (in modo da poter mettere in pausa rapidamente un annuncio).

* **[!UICONTROL Frequency]:** Dati per ciascun livello di frequenza dell’annuncio per il posizionamento, tra cui:
   * il livello di frequenza dell’annuncio (ad esempio &quot;1&quot; per tutte le istanze in cui gli utenti hanno visto un annuncio una volta)
   * il numero univoco stimato di dispositivi/browser o persone (a seconda del [!UICONTROL Cross Device Level] per la campagna) che ha ricevuto impression al livello di frequenza specificato
   * il numero stimato di impression al livello di frequenza specificato
   * la frequenza media stimata per il livello di frequenza specificato. Questo valore è uguale a (Impression stimate)/(Valori univoci stimati).

* **[!UICONTROL Inventory]:** Informazioni su tutte le offerte target del posizionamento.

  Il [!UICONTROL Inventory] consente di risolvere rapidamente i problemi visualizzando le statistiche sulle prestazioni, ad esempio [!UICONTROL Auctions], [!UICONTROL Bids], e [!UICONTROL Win Rate]. La scheda include le funzioni di ricerca e filtro, le stesse opzioni di visualizzazione delle colonne standard e personalizzate disponibili nella pagina principale e i pulsanti di azione rapida in ogni riga, tra cui [!UICONTROL Edit], [!UICONTROL View Report], e [[!UICONTROL Auction Insights] per ulteriori informazioni sulla risoluzione dei problemi](/help/dsp/inventory/private-deal-auction-insights.md).

## Apri [!UICONTROL Placement Inspector]

1. Apri la vista posizionamenti per la campagna o il pacchetto principale:

   * Visualizza tutti i posizionamenti all’interno della campagna principale:

      1. Nel menu principale, fai clic su **[!UICONTROL Campaigns]**.

      1. Fai clic sul nome della campagna.

      1. Fai clic su **[!UICONTROL Placements]** scheda.

   * Visualizza tutti i posizionamenti all’interno del pacchetto principale:

      1. Nel menu principale, fai clic su **[!UICONTROL Campaigns]**.

      1. Fai clic sul nome della campagna.

      1. Fai clic su **[!UICONTROL Packages]** scheda.

      1. Fare clic sul nome del pacchetto padre.

1. Tenete premuto il cursore sulla riga di posizionamento e fate clic su **[!UICONTROL More]** e quindi fare clic su un&#39;opzione:

   * Per visualizzare tutti i siti di destinazione del posizionamento, fate clic su **[!UICONTROL Sites]**.

   * Per visualizzare tutti gli annunci nel posizionamento, fai clic su **[!UICONTROL Ads]**.

   * Per visualizzare i dati di frequenza per il posizionamento, fate clic su **[!UICONTROL Frequency]**.

   * Per visualizzare tutte le offerte con targeting di posizionamento, fai clic su **[!UICONTROL Inventory]**.

1. (Facoltativo) [Modificare la vista a colonne](campaign-data-views-manage.md#column-view-change) in base alle esigenze, per visualizzare le metriche richieste.

1. (Facoltativo) Per esportare i dati in una scheda qualsiasi, fai clic su ![Altro](/help/search-social-commerce/assets/more.png "Altro") in alto a destra, quindi fai clic su **[!UICONTROL Export]**.

   I dati vengono salvati nella cartella di download predefinita del browser come rapporto in formato XLSM.

## Risoluzione dei problemi di inventario

| Problema | Possibile causa | Azioni da intraprendere |
| -----------| ---------- | ---------- |
| [!UICONTROL Zero Auctions] | L&#39;editore non ha iniziato a inviare richieste di offerta. | Contatta l’editore per attivare l’offerta. |
| | L’offerta è stata impostata in modo errato, ad esempio inserendo un ID offerta esterno errato. | Conferma i dettagli dell’offerta e modifica l’offerta. |
| [!UICONTROL Auctions but no Bids] | Il targeting del posizionamento non corrisponde alle richieste di offerta in arrivo per l’offerta. <br><br> Ad esempio, un posizionamento potrebbe essere indirizzato a una geografia che non è idonea per l’operazione. | Modifica le destinazioni di posizionamento in base alle esigenze per evitare incongruenze di targeting. |
| | Il posizionamento non ha un annuncio attivo con il tipo di file multimediale richiesto per l’offerta. | Crea e allega al posizionamento un annuncio con il tipo di file multimediale corretto. |
| | Il posizionamento non dispone di un budget adeguato. | Aumenta il budget di posizionamento per consentire le offerte sulle richieste in arrivo. |
| | Le date del volo di posizionamento non si sovrappongono alle date di consegna delle impression per l’offerta. | Modifica le date di volo del posizionamento in base alle esigenze. |
| [!UICONTROL Low Win Rate] | L&#39;offerta massima del posizionamento (minima o fissa) è inferiore al minimo richiesto dalla trattativa. | Aumentare il [!UICONTROL Max Bid] secondo necessità. |
| | Il posizionamento utilizza filtri pre-offerta che limitano le offerte. | Abbassa le soglie dei filtri pre-offerta per consentire un maggior numero di offerte. |
| | Il targeting del pubblico per il posizionamento è troppo restrittivo. | Verifica se le destinazioni del pubblico specificato hanno un numero sufficiente di utenti attivi e, se possibile, espandi il pubblico. |

>[!MORELIKETHIS]
>
>* [Tipi di rapporti sulle prestazioni nelle visualizzazioni di Campaign Management](campaign-reports-about.md)
>* [Gestire le visualizzazioni dati della campagna](campaign-data-views-manage.md)
