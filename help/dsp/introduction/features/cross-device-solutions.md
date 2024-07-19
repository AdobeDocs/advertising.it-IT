---
title: Soluzioni multi-dispositivo
description: Ulteriori informazioni sulle funzioni multi-dispositivo.
feature: DSP Introduction
exl-id: d21917ef-5cac-46f8-8222-099667797683
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '1000'
ht-degree: 0%

---

# Soluzioni multi-dispositivo

L&#39;integrazione di Advertising DSP con [!DNL LiveRamp] ti consente di estendere il pubblico a tutti i dispositivi noti di una persona, non solo ai dispositivi tracciati dal tuo marchio. L’integrazione fornisce anche il limite di frequenza e la misurazione dell’attribuzione su tutti i dispositivi.

Quando utilizzi un grafico dei dispositivi basato sulle persone supportato, puoi:

* Abbina i tipi di pubblico su canali e dispositivi per distribuire annunci a persone e famiglie, anziché a dispositivi.
* Equilibrio ed esposizione attraverso la comprensione e la limitazione della frequenza tra i singoli individui.
* Strategie di test che espongono e convertono i tipi di pubblico tra canali o dispositivi.

## Vantaggi del grafico dei dispositivi [!DNL LiveRamp]

* Fornisce un pool di dati deterministici, inclusi i dati dei clienti offline

* Fornisce copertura uniforme tra ID cookie e ID dispositivo mobile

* Include dati provenienti prevalentemente dagli Stati Uniti

* È gratuito per la misurazione della quota limite e dell’attribuzione

* Prezzo di 0,35 CPM per le impression estese (impression distribuite esclusivamente utilizzando il grafico dei dispositivi [!DNL LiveRamp] anziché sui dispositivi presenti nei segmenti di pubblico di destinazione)

  La tariffa si riflette sulla scheda della tariffa del tuo account.

## Gestione della frequenza basata sulle persone

La gestione della frequenza basata sulle persone consente di specificare i limiti di frequenza a livello di persona, anziché a livello di dispositivo, per un controllo efficace dell&#39;esposizione dei supporti.

### Attiva gestione frequenza basata sulle persone

* **Campagne:** Quando si crea una nuova campagna, è possibile specificare un&#39;impostazione [!UICONTROL Cross-Device Level]. Abilitare &quot;[!UICONTROL Same Device]&quot; -> &quot;[!UICONTROL People]&quot; e selezionare un grafico dei dispositivi. Il grafico dei dispositivi specificato viene utilizzato sia per il targeting tra dispositivi a livello di posizionamento che per la gestione della frequenza basata sulle persone a livello di campagna, pacchetto e posizionamento. I limiti di frequenza si applicano a tutti i dispositivi noti di una persona.

Per ulteriori informazioni, vedere [Impostazioni campagna](/help/dsp/campaign-management/campaigns/campaign-settings.md).

Una volta salvata una campagna, non puoi modificarne l&#39;impostazione [!UICONTROL Cross Device Level].

* **Pacchetti:** Facoltativamente è possibile impostare limiti di frequenza aggiuntivi a livello di pacchetto. L’DSP rispetta il limite di frequenza più severo nella gerarchia delle campagne.

* **Posizionamenti:** Facoltativamente puoi impostare limiti di frequenza aggiuntivi a livello di posizionamento. L’DSP rispetta il limite di frequenza più severo nella gerarchia delle campagne.

## Targeting basato su persone

Il targeting basato sulle persone consente di trovare i clienti su desktop e dispositivi mobili.

### Attiva targeting basato sulle persone

* **Campagne:** Quando si crea una nuova campagna, è possibile specificare un&#39;impostazione [!UICONTROL Cross-Device Level]. Abilitare &quot;[!UICONTROL Same Device]&quot; -> &quot;[!UICONTROL People]&quot; e selezionare un grafico dei dispositivi. Il grafico dei dispositivi specificato viene utilizzato sia per il targeting tra dispositivi a livello di posizionamento che per la gestione della frequenza basata sulle persone.

Per ulteriori informazioni, vedere [Impostazioni campagna](/help/dsp/campaign-management/campaigns/campaign-settings.md).

* **Posizionamenti:** quando selezioni i target di pubblico per un posizionamento in una campagna con un grafico dei dispositivi specificato, un&#39;opzione [!UICONTROL Cross-Device Targeting] ti consente di estendere il targeting su tutti i dispositivi noti di una persona (in base al grafico dei dispositivi specificato nelle impostazioni della campagna), anche su dispositivi che non si trovano nei segmenti specificati.

### Configurare la generazione di rapporti per il targeting basato sulle persone

Puoi includere le metriche seguenti nei rapporti personalizzati:

* **Impression estese:** (nella sezione [!UICONTROL Build Your Report] in [!UICONTROL Metrics] > [!UICONTROL Std. Metrics]) il volume di impression incrementali distribuite sfruttando un grafico dei dispositivi (e non trovate all&#39;interno dei segmenti di pubblico originali). Questa metrica viene utilizzata anche per calcolare le tariffe applicabili associate all’utilizzo di un grafico dei dispositivi di terze parti.

  Per determinare il costo delle impression estese durante un periodo di tempo, esegui un rapporto personalizzato che includa la colonna [!UICONTROL Extended Impressions], quindi moltiplica il numero totale di impression estese per $0,00035 (0,35/1000 impression).

  Il costo aggregato è incluso anche nella colonna [!UICONTROL Billable Other Net Spend] (in [!UICONTROL Metrics] > [!UICONTROL Spend]), sebbene tale metrica includa anche altre commissioni della campagna eventualmente aggiunte.

* **Grafico dispositivo:** (nella sezione [!UICONTROL Build Your Report] in [!UICONTROL Dimensions] > [!UICONTROL Campaign]) Il grafico dei dispositivi selezionato per una campagna, un pacchetto o un posizionamento particolare.

## Misurazione dell’attribuzione basata sulle persone

*Inserzionisti con solo tracciamento conversione Adobe Advertising*

Con l’attribuzione basata sulle persone, puoi attribuire le conversioni che hanno avuto luogo su un dispositivo diverso da quello su cui si è verificata l’esposizione multimediale. La misurazione dell&#39;attribuzione basata sulle persone è disponibile in DSP, [!DNL Adobe Advertising Creative] e [!DNL Adobe Advertising Search, Social, & Commerce] per gli inserzionisti che hanno implementato pixel di conversione Adobi Advertising sui loro siti.

### Abilita misurazione attribuzione basata su persone

Se desideri attivare la misurazione dell’attribuzione tra dispositivi, contatta il team dell’account di Adobe.

### Impostare i rapporti di conversione per l&#39;attribuzione della conversione tra dispositivi

#### Impostazioni dei rapporti di conversione

Quando un grafo di dispositivi è abilitato per la misurazione dell&#39;attribuzione, il rapporto [!UICONTROL Conversion] include un&#39;impostazione [!UICONTROL Cross-Device Breakout] che consente di includere fino a tre colonne separate per ogni metrica di conversione, tra cui:

* &lt;*Conversione*>[!UICONTROL (tp)]: include le conversioni totali (persone totali), che includono sia le conversioni dello stesso dispositivo che le conversioni tra dispositivi (se applicabili). Nel report, &quot;[!UICONTROL (tp)]&quot; viene aggiunto al nome della metrica di conversione, al tipo di regola e ai tipi di conversione nel percorso di conversione (ad esempio, &quot;Responses(le)(tl)(tp)).

* &lt;*Conversione*>[!UICONTROL (sd)]: (facoltativo) include solo le conversioni per le quali è stato tracciato un solo dispositivo nel percorso di conversione. Nel report, &quot;[!UICONTROL (sd)]&quot; viene aggiunto al nome della metrica di conversione, al tipo di regola e ai tipi di conversione nel percorso di conversione (ad esempio, &quot;Responses(le)(tl)(sd)).

* &lt;*Conversione*>[!UICONTROL (xd)]: (facoltativo) include solo le conversioni per le quali è stato tracciato più di un dispositivo nel percorso di conversione. Nel report, &quot;[!UICONTROL (xd)]&quot; viene aggiunto al nome della metrica di conversione, al tipo di regola e ai tipi di conversione nel percorso di conversione (ad esempio, &quot;Responses(le)(tl)(xd)).

#### Come interpretare il rapporto di conversione

Ordinare la percentuale di conversioni totali tra dispositivi ([!UICONTROL (xd)]/[!UICONTROL (tl)]) da alto a basso per capire cosa determina conversioni tra dispositivi superiori alla media. Puoi utilizzarlo per informare la tua strategia creativa o di targeting in modo da abbinare la messaggistica e incanalare gli investimenti al comportamento degli utenti.

* Pacchetti: scopri quali pacchetti generano il maggior numero di conversioni totali e quali hanno una percentuale elevata di conversioni tra dispositivi diversi. Questo può aiutarti a capire dove concentrarti sulla spesa.

* Posizionamenti: confronta le prestazioni e l’attribuzione del posizionamento (ad esempio, un annuncio web per dispositivi mobili può determinare conversioni su desktop). Senza un grafico dei dispositivi per l’attribuzione, potresti perdere l’impatto di un posizionamento web mobile sulle conversioni desktop o potrebbe essere nascosto se la maggior parte degli utenti si converte su desktop e non su web mobile.

* Annunci: scopri quali annunci favoriscono conversioni più elevate e quantificane il valore e l’impatto sia sui browser web che sugli ambienti delle app mobili.

* Siti: ottimizzare i siti su più siti anziché escluderli completamente manualmente. Se un sito web guida conversioni tra dispositivi, puoi vedere su quali dispositivi si verifica questo comportamento.

* Offerte: migliora l’ottimizzazione manuale verificando quali offerte di inventario forniscono conversioni tra dispositivi diversi e quindi decidendo se espandere il targeting per includere più dispositivi e canali in tali offerte.

>[!MORELIKETHIS]
>
>* [Impostazioni report](/help/dsp/reports/report-settings.md)
>* [Impostazioni campagna](/help/dsp/campaign-management/campaigns/campaign-settings.md)
>* [Impostazioni pacchetto](/help/dsp/campaign-management/packages/package-settings.md)
>* [Impostazioni posizionamento](/help/dsp/campaign-management/placements/placement-settings.md)
