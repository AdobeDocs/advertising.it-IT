---
title: Informazioni sulla gestione degli annunci in Advertising DSP
description: Scopri la gestione degli annunci.
feature: DSP Ads
exl-id: 41dbe28e-a476-4601-a3d8-a9111eae3f6b
source-git-commit: 7e614ecb517515217d812926f61ca10437820efd
workflow-type: tm+mt
source-wordcount: '722'
ht-degree: 0%

---

# Informazioni sulla gestione degli annunci in Advertising DSP

<!-- add "The Ads View (Dashboard?)" section -->

DSP supporta la consegna di annunci tramite tag di terze parti per il serving di annunci (come Google, Flashtalk o Sizmek) per vari tipi di annunci e il caricamento di risorse dirette per gli annunci display nativi. Puoi caricare tag di terze parti singolarmente o in blocco. I caricamenti in blocco utilizzano i fogli dei tag partner o un modello di tag in blocco.

<!-- The bulk upload feature requires you to either a) upload DoubleClick and Flashtalking tag sheets or b) download a template, input your tags into the template, and then re-upload the template. -->
<!-- need a list of all supported third-party ad servers; see file in future-tbd folder -->

Una volta configurati i tuoi annunci, dovrai allegare ogni annuncio a un posizionamento, che include i parametri di targeting (come geo, pubblico, dispositivo e targeting di inventario) che controlleranno la distribuzione della campagna. Puoi allegare un singolo annuncio a uno o più posizionamenti.

## Tipi di annunci disponibili {#ad-types}

Sono disponibili in DSP tutti i seguenti tipi di annunci. Per le specifiche complete per ogni tipo di annuncio, vedi [Specifiche degli annunci](ad-specs.md).

* **Annunci audio (solo di terze parti)**: Gli annunci audio vengono riprodotti tra i contenuti dei siti di pubblicazione digitale e possono essere eseguiti autonomamente come file audio o insieme a banner correlati. L&#39;audio viene utilizzato al meglio per promuovere la brand awareness e coinvolgere il pubblico on-the-go. Gli indicatori prestazioni chiave per l&#39;audio includono [!UICONTROL Completion Rate] e [!UICONTROL Cost per Completion].

* **Annunci visualizzati (solo di terze parti)**: Gli annunci display sono immagini animate o statiche visualizzate nei browser web o nelle app. Facendo clic sull’unità pubblicitaria l’utente passa a un sito o a un microsito di marca. La visualizzazione è più utilizzata per promuovere CPM efficienti, aumentare l’associazione dei messaggi, aggiungere punti di contatto aggiuntivi di marchi o prodotti e indirizzare gli utenti verso il basso nel funnel di acquisto. Tra gli indicatori chiave di performance per la visualizzazione [!UICONTROL Clicks], [!UICONTROL Cost per Click], [!UICONTROL Conversions]e [!UICONTROL Cost per Conversion]. DSP supporta un&#39;ampia varietà di banner di visualizzazione e dimensioni degli annunci.

* **Annunci mobili (solo di terze parti)**: Gli annunci mobili possono essere in formato video pre-roll (VAST, MRAID) o standard. I video mobili pre-roll possono essere riprodotti automaticamente o fare clic per la riproduzione ed è meglio utilizzato per raggiungere gli spettatori attraverso gli schermi. La visualizzazione standard per dispositivi mobili è un’immagine statica visualizzata sui browser web per dispositivi mobili o nelle app ed è meglio utilizzata per integrare acquisti di video digitali, favorire l’associazione dei messaggi e aggiungere punti di contatto di branding o prodotti aggiuntivi. Gli annunci mobili possono anche funzionare come acquisti a schermo intero o come interstiziali mobili, che sono annunci mobili a schermo intero ad alto impatto e sono utilizzati al meglio per sviluppare la brand awareness per il pubblico mobile e favorire le conversioni.

* **Annunci di visualizzazione nativi (solo di prime parti)**: Gli annunci nativi sono supportati nel formato di visualizzazione standard. Gli annunci nativi includono un titolo e/o un titolo, una descrizione, un logo e un’immagine. Gli elementi dell&#39;annuncio vengono combinati ed eseguiti in modo da corrispondere allo stile di pagina dell&#39;editore in modo che l&#39;annuncio si fonde con il contenuto organico dell&#39;editore e generi un maggiore coinvolgimento. Native viene utilizzato al meglio per la brand awareness e per promuovere la visualizzazione del pubblico e i tassi di coinvolgimento con pubblicità favorevole ai visualizzatori. Gli indicatori chiave di performance includono: [!UICONTROL Clicks], [!UICONTROL Cost Per Click], [!UICONTROL Conversions]e [!UICONTROL Cost Per Conversion].

* **Annunci pre-roll (solo di terze parti)**: Gli annunci pre-roll (VAST e VPAID) vengono visualizzati prima dei contenuti video premium e forniscono un’esperienza di visualizzazione coinvolgente e coinvolgente. I video pre-roll possono essere interattivi, contenere funzioni rich media e includere sovrapposizioni, rollover e chiamate all’azione. Gli indicatori prestazioni chiave per gli annunci video pre-roll includono [!UICONTROL Video Completion Rate] e [!UICONTROL Viewability Rate].

* **Annunci TV collegati (solo di terze parti)**: Gli annunci TV collegati vengono visualizzati prima e durante i contenuti video TV premium. Tutto l&#39;inventario televisivo collegato viene eseguito su dispositivi TV, il che significa che il video viene riprodotto automaticamente in un ambiente snello e a schermo intero che gli spettatori non possono saltare. La TV collegata è il formato video digitale più simile alle pubblicità televisive. Gli indicatori prestazioni chiave per la TV connessa includono [!UICONTROL Completion Rate].

* **Annunci video universali (solo di terze parti)**: Gli annunci Universal Video combinano tutte le funzionalità di Annunci pre-roll e mobili pre-roll (VAST e VPAID) in uno e vengono mostrati prima e durante il contenuto video. L’annuncio video universale può essere utilizzato quando si esegue il targeting dell’inventario video da ambienti Desktop, Mobile e Connected TV, evitando così la necessità di creare più annunci video. Gli indicatori prestazioni chiave per il video universale includono [!UICONTROL Completion Rate] e [!UICONTROL Viewability Rate].

## Approvazioni annunci DSP

Quando crei un annuncio, DSP lo rivede per categorie sensibili, fai clic su Funzionalità URL e visualizza in anteprima il rendering.

Inizialmente, verrà visualizzato un punto rosso nel [!UICONTROL Status] colonna. Il processo di revisione richiede normalmente 24-48 ore. Un annuncio interrotto, tuttavia, potrebbe avere uno stato in sospeso per più di 48 ore, quindi hai tempo per correggere gli errori prima che l’annuncio venga rifiutato. Gli annunci rifiutati includono un motivo del rifiuto.

Quando DSP approvato un annuncio, viene visualizzato un punto verde nella colonna Stato .

![indicatore di omologazione in [!UICONTROL Status] column](/help/dsp/assets/ad-approval-status.png)

>[!NOTE]
>
>Il tuo annuncio verrà servito solo se sia DSP che la SSP hanno approvato il contenuto creativo. Ogni SSP ha i propri requisiti e procedure di approvazione.

>[!MORELIKETHIS]
>
>* [Creare un singolo annuncio](ad-create.md)
>* [Creare più annunci di terze parti](ad-create-multiple.md)
>* [Specifiche degli annunci](ad-specs.md)

