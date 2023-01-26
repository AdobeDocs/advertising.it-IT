---
title: Soluzioni multi-dispositivo
description: Ulteriori informazioni sulle funzioni multi-dispositivo.
feature: DSP Introduction
exl-id: d21917ef-5cac-46f8-8222-099667797683
source-git-commit: 7e614ecb517515217d812926f61ca10437820efd
workflow-type: tm+mt
source-wordcount: '999'
ht-degree: 0%

---

# Soluzioni multi-dispositivo

Integrazione di Advertising DSP con [!DNL LiveRamp] consente di estendere il pubblico a tutti i dispositivi noti di una persona, non solo ai dispositivi tracciati dal tuo marchio. L’integrazione fornisce inoltre il limite di frequenza e la misurazione dell’attribuzione su tutti i dispositivi.

Quando utilizzi un grafico dei dispositivi basato su persone supportato, puoi:

* Fai corrispondere i tipi di pubblico tra canali e dispositivi per distribuire annunci a persone e famiglie anziché a dispositivi.
* Equilibrare l&#39;esposizione comprendendo e limitando la frequenza tra gli individui.
* Strategie di test che espongono e convertono i tipi di pubblico tra canali o dispositivi.

## Vantaggi [!DNL LiveRamp] Device Graph

* Fornisce un pool di dati deterministici, inclusi i dati dei clienti offline

* Fornisce una copertura uniforme tra ID cookie e ID dispositivo mobile

* Include i dati provenienti principalmente dagli Stati Uniti

* È gratuito per il limite di frequenza e la misurazione dell’attribuzione

* Prezzi a $0,35 CPM per impression estese (impression consegnate esclusivamente utilizzando il [!DNL LiveRamp] grafico dei dispositivi anziché su dispositivi presenti nei segmenti di pubblico target)

   Il tasso si riflette sulla carta del tasso del tuo account.

## Gestione delle frequenze basata sulle persone

La gestione della frequenza basata sulle persone consente di specificare limiti di frequenza a livello di persona, anziché a livello di dispositivo, per un vero controllo dell&#39;esposizione ai supporti.

### Attivare la gestione della frequenza basata sulle persone

* **Campagne:** Quando crei una nuova campagna, puoi specificare un [!UICONTROL Cross-Device Level] impostazione. Abilita &quot;[!UICONTROL Same Device]&quot; -> &quot;[!UICONTROL People],&quot; e seleziona un grafico dei dispositivi. Il grafico dei dispositivi specificato viene utilizzato sia per il targeting tra dispositivi a livello di posizionamento che per la gestione delle frequenze basate sulle persone a livello di campagna, pacchetto e posizionamento. I limiti di frequenza si applicano a tutti i dispositivi noti di una persona.

Per ulteriori informazioni, consulta [Impostazioni di Campaign](/help/dsp/campaign-management/campaigns/campaign-settings.md).

Una volta salvata una campagna, non è possibile modificarne la [!UICONTROL Cross Device Level] impostazione.

* **Pacchetti:**  Facoltativamente, puoi impostare limiti di frequenza aggiuntivi a livello di pacchetto. DSP rispettare il limite di frequenza più rigoroso nella gerarchia delle campagne.

* **Posizionamenti:** Facoltativamente, puoi impostare limiti di frequenza aggiuntivi a livello di posizionamento. DSP rispettare il limite di frequenza più rigoroso nella gerarchia delle campagne.

## Targeting basato su persone

Il targeting basato sulle persone consente di trovare clienti su desktop e dispositivi mobili.

### Attivare Il Targeting Basato Sulle Persone

* **Campagne:** Quando crei una nuova campagna, puoi specificare un [!UICONTROL Cross-Device Level] impostazione. Abilita &quot;[!UICONTROL Same Device]&quot; -> &quot;[!UICONTROL People],&quot; e seleziona un grafico dei dispositivi. Il grafico dei dispositivi specificato viene utilizzato sia per il targeting tra dispositivi a livello di posizionamento che per la gestione delle frequenze basate sulle persone.

Per ulteriori informazioni, consulta [Impostazioni di Campaign](/help/dsp/campaign-management/campaigns/campaign-settings.md).

* **Posizionamenti:** Quando selezioni target di pubblico per un posizionamento in una campagna con un grafico dei dispositivi specifico, un [!UICONTROL Cross-Device Targeting] l’opzione ti consente di estendere il targeting su tutti i dispositivi noti di una persona (in base al grafico dei dispositivi specificato nelle impostazioni della campagna), anche sui dispositivi che non si trovano nei segmenti specificati.

### Impostazione di rapporti per il targeting basato sulle persone

Nei rapporti personalizzati puoi includere le metriche seguenti:

* **Impressioni estese:** (Nel [!UICONTROL Build Your Report] sezione [!UICONTROL Metrics] > [!UICONTROL Std. Metrics]) Il volume di impression incrementali fornite sfruttando un grafico dei dispositivi (e non trovato nei segmenti di pubblico originali). Questa metrica viene utilizzata anche per calcolare le tariffe applicabili associate all’utilizzo di un grafico dei dispositivi di terze parti.

   Per determinare il costo delle impression estese durante un periodo di tempo, esegui un rapporto personalizzato che include [!UICONTROL Extended Impressions] , quindi moltiplica il numero totale di impression estese per $ 0,00035 ($0,35/1000 impression).

   Il costo aggregato è incluso anche nel [!UICONTROL Billable Other Net Spend] colonna (sotto [!UICONTROL Metrics] > [!UICONTROL Spend]), anche se tale metrica include anche altre tariffe per le campagne che potresti aver aggiunto.

* **Device Graph:** (Nel [!UICONTROL Build Your Report] sezione [!UICONTROL Dimensions] > [!UICONTROL Campaign]) Grafico del dispositivo selezionato per una determinata campagna, pacchetto o posizionamento.

## Misurazione dell’attribuzione basata sulle persone

*Inserzionisti con solo tracciamento della conversione pubblicitaria di Adobe*

Con l’attribuzione basata sulle persone, puoi attribuire conversioni che hanno avuto luogo su un dispositivo diverso da quello sul quale si è verificata l’esposizione dei contenuti multimediali. La misurazione dell’attribuzione basata sulle persone è disponibile in DSP, [!DNL Adobe Advertising Creative]e [!DNL Adobe Advertising Search] per gli inserzionisti che hanno implementato i pixel di conversione della pubblicità Adobe sui loro siti.

### Abilitare la misurazione dell’attribuzione basata sulle persone

Per attivare la misurazione di attribuzione tra dispositivi, contatta il tuo [!DNL Adobe] team di account.

### Configurare i rapporti di conversione per l’attribuzione della conversione tra dispositivi

#### Impostazioni dei rapporti di conversione

Quando un grafico dei dispositivi è abilitato per la misurazione dell’attribuzione, la funzione [!UICONTROL Conversion] Il rapporto include [!UICONTROL Cross-Device Breakout] , che consente di includere fino a tre colonne separate per ogni metrica di conversione, tra cui:

* &lt;*Conversione*>[!UICONTROL (tp)]: Include le conversioni totali (persone totali), che includono sia le conversioni con lo stesso dispositivo che le conversioni tra dispositivi (se applicabili). Nel rapporto, &quot;[!UICONTROL (tp)]&quot; viene aggiunto al nome della metrica di conversione, al tipo di regola e ai tipi di conversione nel percorso di conversione (ad esempio, &quot;Responses(le)(tl)(tp))).

* &lt;*Conversione*>[!UICONTROL (sd)]: (Facoltativo) Include solo le conversioni per le quali è stato tracciato un solo dispositivo nel percorso di conversione. Nel rapporto, &quot;[!UICONTROL (sd)]&quot; viene aggiunto al nome della metrica di conversione, al tipo di regola e ai tipi di conversione nel percorso di conversione (ad esempio, &quot;Responses(le)(tl)(sd))).

* &lt;*Conversione*>[!UICONTROL (xd)]: (Facoltativo) Include solo le conversioni per le quali più di un dispositivo è stato tracciato nel percorso di conversione. Nel rapporto, &quot;[!UICONTROL (xd)]&quot; viene aggiunto al nome della metrica di conversione, al tipo di regola e ai tipi di conversione nel percorso di conversione (ad esempio, &quot;Responses(le)(tl)(xd))).

#### Come interpretare il rapporto di conversione

Se ordini la percentuale di conversioni totali che sono tra dispositivi ([!UICONTROL (xd)]/[!UICONTROL (tl)]) dall&#39;alto al basso, capirai cosa sta causando conversioni tra dispositivi superiori alla media. Puoi utilizzarlo per informare la tua strategia creativa o di targeting in modo da abbinare messaggistica e investimenti di canale al comportamento degli utenti.

* Pacchetti - Scopri quali pacchetti generano le conversioni più totali e quali hanno un&#39;alta percentuale di conversioni tra dispositivi. Questo può aiutarti a capire dove concentrare la spesa.

* Posizionamenti : confronta le prestazioni di posizionamento e l’attribuzione (ad esempio, un annuncio web per dispositivi mobili può stimolare le conversioni su desktop). Senza un grafico dei dispositivi per l’attribuzione, potresti perdere l’impatto di un posizionamento web per dispositivi mobili sulle conversioni desktop, o potrebbe essere sepolto se la maggior parte degli utenti si converte su desktop e non su web per dispositivi mobili.

* Annunci: scopri quali annunci determinano conversioni più elevate e quantificane il loro valore e impatto sia nei browser web che negli ambienti delle app mobili.

* Siti: ottimizza i siti invece di escluderli manualmente completamente. Se un sito web genera conversioni tra dispositivi, puoi vedere su quali dispositivi si verifica questo comportamento.

* Offerte: migliora l’ottimizzazione manuale verificando quali offerte di inventario forniscono conversioni tra dispositivi e decidendo se espandere il targeting per includere più dispositivi e canali in tali offerte.

>[!MORELIKETHIS]
>
>* [Impostazioni dei rapporti](/help/dsp/reports/report-settings.md)
>* [Impostazioni di Campaign](/help/dsp/campaign-management/campaigns/campaign-settings.md)
>* [Impostazioni pacchetto](/help/dsp/campaign-management/packages/package-settings.md)
>* [Impostazioni di posizionamento](/help/dsp/campaign-management/placements/placement-settings.md)

