---
title: Informazioni sulla gestione degli annunci in Advertising DSP
description: Informazioni sulla gestione degli annunci.
feature: DSP Ads
exl-id: 41dbe28e-a476-4601-a3d8-a9111eae3f6b
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '733'
ht-degree: 0%

---

# Informazioni sulla gestione degli annunci in Advertising DSP

<!-- add "The Ads View (Dashboard?)" section -->

L’DSP supporta la distribuzione degli annunci tramite tag di terze parti per la gestione degli annunci (ad esempio Google, Flashtalk o Sizmek) per vari tipi di annunci e il caricamento diretto delle risorse per gli annunci display nativi. Puoi caricare tag di terze parti singolarmente o in blocco. I caricamenti in blocco utilizzano fogli di tag partner o un modello di tag in blocco.

<!-- The bulk upload feature requires you to either a) upload DoubleClick and Flashtalking tag sheets or b) download a template, input your tags into the template, and then re-upload the template. -->
<!-- need a list of all supported third-party ad servers; see file in future-tbd folder -->

Una volta configurati gli annunci, allega ogni annuncio a un posizionamento, che include i parametri di targeting (come geotargeting, pubblico, dispositivo e targeting di inventario) che controllano il modo in cui la campagna consegna. Puoi allegare un singolo annuncio a uno o più posizionamenti.

## Tipi di annunci disponibili {#ad-types}

Tutti i seguenti tipi di annunci sono disponibili nell’DSP. Per le specifiche complete per ogni tipo di annuncio, consulta le [Specifiche annuncio](ad-specs.md).

* **Annunci audio (solo di terze parti)**: gli annunci audio vengono riprodotti tra contenuti di siti di editori digitali e possono essere eseguiti come file audio autonomi o con banner correlati. L’audio è ideale per promuovere la brand awareness e coinvolgere il pubblico in movimento. Gli indicatori di prestazioni chiave per l&#39;audio includono [!UICONTROL Completion Rate] e [!UICONTROL Cost per Completion].

* **Annunci visualizzati (solo di terze parti)**: gli annunci visualizzati sono immagini animate o statiche visualizzate nei browser Web o nelle app. Facendo clic sull’unità pubblicitaria, l’utente viene indirizzato a un sito o a un microsito con marchio. La visualizzazione è ideale per promuovere CPM efficienti, aumentare l’associazione dei messaggi, aggiungere ulteriori punti di contatto per marchi o prodotti e indirizzare gli utenti verso il basso nel funnel di acquisto. Gli indicatori di prestazioni chiave per la visualizzazione includono [!UICONTROL Clicks], [!UICONTROL Cost per Click], [!UICONTROL Conversions] e [!UICONTROL Cost per Conversion]. L&#39;DSP supporta un&#39;ampia varietà di banner pubblicitari.

* **Annunci per dispositivi mobili (solo di terze parti)**: gli annunci per dispositivi mobili possono essere in formato video pre-roll (VAST, MRAID) o di visualizzazione standard. Il video mobile pre-roll può essere riprodotto automaticamente o con un clic per essere riprodotto ed è meglio utilizzato per raggiungere gli spettatori attraverso gli schermi. La visualizzazione standard per dispositivi mobili è un’immagine statica visualizzata nei browser web o nelle app mobili ed è ideale per integrare gli acquisti di video digitali, promuovere l’associazione dei messaggi e aggiungere ulteriori punti di contatto di branding o prodotti. Gli annunci per dispositivi mobili possono anche funzionare come rilevamenti a schermo intero o come interstiziali mobili, ovvero annunci mobili a schermo intero e ad alto impatto che vengono utilizzati meglio per sviluppare la brand awareness per il pubblico mobile e stimolare le conversioni.

* **Annunci visualizzati nativi (solo di prime parti)**: gli annunci nativi sono supportati nel formato di visualizzazione standard. Gli annunci nativi includono un titolo e/o un titolo, una descrizione, un logo e un’immagine. Gli elementi dell’annuncio vengono combinati e renderizzati in modo da corrispondere allo stile di pagina dell’editore, affinché l’annuncio si fonda con il contenuto organico dell’editore e aumenti il coinvolgimento. Nativa è ideale per la brand awareness e per indirizzare la visualizzazione del pubblico e i tassi di coinvolgimento con la pubblicità intuitiva. Gli indicatori di prestazioni chiave includono [!UICONTROL Clicks], [!UICONTROL Cost Per Click], [!UICONTROL Conversions] e [!UICONTROL Cost Per Conversion].

* **Annunci pre-roll (solo di terze parti)**: gli annunci pre-roll (VAST e VPAID) vengono visualizzati prima dei contenuti video premium e forniscono un&#39;esperienza di visualizzazione coinvolgente e coinvolgente. I video pre-roll possono essere interattivi, contenere funzioni rich media e includere sovrapposizioni, rollover e chiamate all’azione. Gli indicatori di prestazioni chiave per gli annunci video pre-roll includono [!UICONTROL Video Completion Rate] e [!UICONTROL Viewability Rate].

* **Annunci TV connessi (solo di terze parti)**: gli annunci TV connessi vengono visualizzati prima e durante i contenuti video TV premium. Tutti gli inventari TV collegati vengono eseguiti su dispositivi TV, il che significa che il video viene riprodotto automaticamente in un ambiente a schermo intero e snello che gli spettatori non possono saltare. Connected TV è il formato video digitale più simile agli spot televisivi. Gli indicatori di prestazioni chiave per la TV connessa includono [!UICONTROL Completion Rate].

* **Annunci video universali (solo di terze parti)**: gli annunci video universali consentono di eseguire il targeting dell&#39;inventario video dagli ambienti desktop, mobile e TV connessi per l&#39;inventario VPAID e VAST utilizzando un unico posizionamento video. Combinano tutte le funzionalità della TV collegata, degli annunci pre-roll e pre-roll mobili e vengono visualizzati prima e durante i contenuti video. Gli indicatori di prestazioni chiave per il video universale includono [!UICONTROL Completion Rate] e [!UICONTROL Viewability Rate].

  Gli annunci video universali possono essere collegati solo ai posizionamenti video universali.

  Per ulteriori informazioni sugli annunci video universali, consulta &quot;[Domande frequenti sul video universale](/help/dsp/campaign-management/faq-universal-video.md)&quot;.

## Approvazioni di annunci DSP

Quando crei un annuncio, l’DSP lo esamina per individuare le categorie sensibili, fai clic su Funzionalità URL e visualizza l’anteprima del rendering.

Inizialmente, la colonna [!UICONTROL Status] dell&#39;annuncio mostra un punto rosso. Il processo di revisione richiede normalmente 24-48 ore. Un annuncio interrotto, tuttavia, potrebbe avere uno stato in sospeso per più di 48 ore, pertanto hai il tempo di correggere gli errori prima che l’annuncio venga rifiutato. Gli annunci rifiutati includono un motivo del rifiuto.

Quando l’DSP approva un annuncio, la colonna Stato dell’annuncio mostra un punto verde.

![indicatore di approvazione in [!UICONTROL Status] colonna](/help/dsp/assets/ad-approval-status.png)

>[!NOTE]
>
>Il tuo annuncio può essere servito solo se sia l&#39;DSP che la SSP hanno approvato il contenuto creativo. Ciascuna SSP ha i propri requisiti e la propria procedura di approvazione.

>[!MORELIKETHIS]
>
>* [Crea un annuncio singolo](ad-create.md)
>* [Creazione di più annunci di terze parti](ad-create-multiple.md)
>* [Specifiche annuncio](ad-specs.md)
