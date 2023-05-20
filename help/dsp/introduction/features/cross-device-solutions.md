---
title: Soluzioni multi-dispositivo
description: Ulteriori informazioni sulle funzioni multi-dispositivo.
feature: DSP Introduction
exl-id: d21917ef-5cac-46f8-8222-099667797683
source-git-commit: 7f35b3f3b33ed320ac186d219cbd0f826666bb3b
workflow-type: tm+mt
source-wordcount: '1000'
ht-degree: 0%

---

# Soluzioni multi-dispositivo

L’integrazione Advertising DSP con [!DNL LiveRamp] consente di estendere il pubblico a tutti i dispositivi noti di una persona, non solo ai dispositivi tracciati dal tuo marchio. L’integrazione fornisce anche il limite di frequenza e la misurazione dell’attribuzione su tutti i dispositivi.

Quando utilizzi un grafico dei dispositivi basato sulle persone supportato, puoi:

* Abbina i tipi di pubblico su canali e dispositivi per distribuire annunci a persone e famiglie, anziché a dispositivi.
* Equilibrio ed esposizione attraverso la comprensione e la limitazione della frequenza tra i singoli individui.
* Strategie di test che espongono e convertono i tipi di pubblico tra canali o dispositivi.

## Vantaggi della [!DNL LiveRamp] Device Graph

* Fornisce un pool di dati deterministici, inclusi i dati dei clienti offline

* Fornisce copertura uniforme tra ID cookie e ID dispositivo mobile

* Include dati provenienti prevalentemente dagli Stati Uniti

* È gratuito per la misurazione della quota limite e dell’attribuzione

* Prezzo di 0,35 $ CPM per le impression estese (impression fornite esclusivamente utilizzando il [!DNL LiveRamp] grafico dei dispositivi (anziché sui dispositivi trovati all’interno dei segmenti di pubblico target)

   La tariffa si riflette sulla scheda della tariffa del tuo account.

## Gestione della frequenza basata sulle persone

La gestione della frequenza basata sulle persone consente di specificare i limiti di frequenza a livello di persona, anziché a livello di dispositivo, per un controllo efficace dell&#39;esposizione dei supporti.

### Attiva gestione frequenza basata sulle persone

* **Campagne:** Quando crei una nuova campagna, puoi specificare una [!UICONTROL Cross-Device Level] impostazione. Abilita &quot;[!UICONTROL Same Device]&quot; -> &quot;[!UICONTROL People],&quot; e seleziona un grafico dei dispositivi. Il grafico dei dispositivi specificato viene utilizzato sia per il targeting tra dispositivi a livello di posizionamento che per la gestione della frequenza basata sulle persone a livello di campagna, pacchetto e posizionamento. I limiti di frequenza si applicano a tutti i dispositivi noti di una persona.

Per ulteriori informazioni, consulta [Impostazioni campagna](/help/dsp/campaign-management/campaigns/campaign-settings.md).

Una volta salvata una campagna, non puoi modificarne le [!UICONTROL Cross Device Level] impostazione.

* **Pacchetti:**  Facoltativamente, puoi impostare limiti di frequenza aggiuntivi a livello di pacchetto. L’DSP rispetterà il limite di frequenza più rigoroso nella gerarchia della campagna.

* **Posizionamenti:** Facoltativamente, è possibile impostare limiti di frequenza aggiuntivi a livello di posizionamento. L’DSP rispetterà il limite di frequenza più rigoroso nella gerarchia della campagna.

## Targeting basato su persone

Il targeting basato sulle persone consente di trovare i clienti su desktop e dispositivi mobili.

### Attiva targeting basato sulle persone

* **Campagne:** Quando crei una nuova campagna, puoi specificare una [!UICONTROL Cross-Device Level] impostazione. Abilita &quot;[!UICONTROL Same Device]&quot; -> &quot;[!UICONTROL People],&quot; e seleziona un grafico dei dispositivi. Il grafico dei dispositivi specificato viene utilizzato sia per il targeting tra dispositivi a livello di posizionamento che per la gestione della frequenza basata sulle persone.

Per ulteriori informazioni, consulta [Impostazioni campagna](/help/dsp/campaign-management/campaigns/campaign-settings.md).

* **Posizionamenti:** Quando selezioni i target di pubblico per un posizionamento in una campagna con un grafico dei dispositivi specificato, viene [!UICONTROL Cross-Device Targeting] Questa opzione ti consente di estendere il targeting su tutti i dispositivi noti di una persona (in base al grafico dei dispositivi specificato nelle impostazioni della campagna), anche su quelli che non si trovano nei segmenti specificati.

### Configurare la generazione di rapporti per il targeting basato sulle persone

Puoi includere le metriche seguenti nei rapporti personalizzati:

* **Impression estese:** (nel [!UICONTROL Build Your Report] sezione in [!UICONTROL Metrics] > [!UICONTROL Std. Metrics]) Il volume di impression incrementali fornite sfruttando un grafico dei dispositivi (e non trovate all’interno dei segmenti di pubblico originali). Questa metrica viene utilizzata anche per calcolare le tariffe applicabili associate all’utilizzo di un grafico dei dispositivi di terze parti.

   Per determinare il costo delle impression estese in un determinato periodo di tempo, esegui un rapporto personalizzato che includa [!UICONTROL Extended Impressions] e quindi moltiplica il numero totale di impression estese per $0,00035 (0,35/1000 impression).

   Il costo aggregato è incluso anche nel [!UICONTROL Billable Other Net Spend] colonna (sotto [!UICONTROL Metrics] > [!UICONTROL Spend]), anche se tale metrica include anche altre tariffe della campagna che potresti aver aggiunto.

* **Device Graph (Grafico dispositivo):** (nel [!UICONTROL Build Your Report] sezione in [!UICONTROL Dimensions] > [!UICONTROL Campaign]) Il grafico dei dispositivi selezionato per una particolare campagna, pacchetto o posizionamento.

## Misurazione dell’attribuzione basata sulle persone

*Per gli inserzionisti che utilizzano solo il tracciamento della conversione di annunci Adobe*

Con l’attribuzione basata sulle persone, puoi attribuire le conversioni che hanno avuto luogo su un dispositivo diverso da quello su cui si è verificata l’esposizione multimediale. La misurazione dell’attribuzione basata sulle persone è disponibile in tutta l’DSP, [!DNL Adobe Advertising Creative], e [!DNL Adobe Advertising Search, Social, & Commerce] per gli inserzionisti che hanno implementato pixel di conversione di Adobe Advertising sui loro siti.

### Abilita misurazione attribuzione basata su persone

Se desideri attivare la misurazione dell’attribuzione tra dispositivi, contatta il team dell’account di Adobe.

### Impostare i rapporti di conversione per l&#39;attribuzione della conversione tra dispositivi

#### Impostazioni dei rapporti di conversione

Quando un grafico dei dispositivi è abilitato per la misurazione dell’attribuzione, il [!UICONTROL Conversion] Il rapporto include una [!UICONTROL Cross-Device Breakout] che ti consente di includere fino a tre colonne separate per ogni metrica di conversione, tra cui:

* &lt;*Conversione*>[!UICONTROL (tp)]: include le conversioni totali (persone totali), che includono sia le conversioni con lo stesso dispositivo che quelle tra dispositivi (se applicabile). Nel rapporto, &quot;[!UICONTROL (tp)]&quot; viene aggiunto al nome della metrica di conversione, al tipo di regola e ai tipi di conversione nel percorso di conversione (ad esempio, &quot;Responses(le)(tl)(tp)).

* &lt;*Conversione*>[!UICONTROL (sd)]: (Facoltativo) Include solo le conversioni per le quali è stato tracciato un solo dispositivo nel percorso di conversione. Nel rapporto, &quot;[!UICONTROL (sd)]&quot; viene aggiunto al nome della metrica di conversione, al tipo di regola e ai tipi di conversione nel percorso di conversione (ad esempio, &quot;Responses(le)(tl)(sd)).

* &lt;*Conversione*>[!UICONTROL (xd)]: (Facoltativo) Include solo le conversioni per le quali è stato tracciato più di un dispositivo nel percorso di conversione. Nel rapporto, &quot;[!UICONTROL (xd)]&quot; viene aggiunto al nome della metrica di conversione, al tipo di regola e ai tipi di conversione nel percorso di conversione (ad esempio, &quot;Responses(le)(tl)(xd)).

#### Come interpretare il rapporto di conversione

Se ordini la percentuale del totale delle conversioni tra dispositivi diversi ([!UICONTROL (xd)]/[!UICONTROL (tl)]) dall&#39;alto al basso, capirai cosa determina conversioni tra dispositivi superiori alla media. Puoi utilizzarlo per informare la tua strategia creativa o di targeting in modo da abbinare la messaggistica e incanalare gli investimenti al comportamento degli utenti.

* Pacchetti: scopri quali pacchetti generano la maggior parte delle conversioni totali e quali hanno una percentuale elevata di conversioni tra dispositivi diversi. Questo può aiutarti a capire dove concentrarti sulla spesa.

* Posizionamenti: confronta le prestazioni e l’attribuzione del posizionamento (ad esempio, un annuncio web per dispositivi mobili può determinare conversioni su desktop). Senza un grafico dei dispositivi per l’attribuzione, potresti perdere l’impatto di un posizionamento web mobile sulle conversioni desktop o potrebbe essere nascosto se la maggior parte degli utenti si converte su desktop e non su web mobile.

* Annunci: scopri quali annunci favoriscono conversioni più elevate e quantificane il valore e l’impatto sia sui browser web che sugli ambienti delle app mobili.

* Siti: ottimizza i siti su più siti anziché escluderli completamente manualmente. Se un sito web guida conversioni tra dispositivi, puoi vedere su quali dispositivi si verifica questo comportamento.

* Offerte: migliora l’ottimizzazione manuale verificando quali offerte di inventario forniscono conversioni tra dispositivi diversi e quindi decidendo se espandere il targeting per includere più dispositivi e canali in tali offerte.

>[!MORELIKETHIS]
>
>* [Impostazioni dei rapporti](/help/dsp/reports/report-settings.md)
>* [Impostazioni campagna](/help/dsp/campaign-management/campaigns/campaign-settings.md)
>* [Impostazioni pacchetto](/help/dsp/campaign-management/packages/package-settings.md)
>* [Impostazioni di posizionamento](/help/dsp/campaign-management/placements/placement-settings.md)

