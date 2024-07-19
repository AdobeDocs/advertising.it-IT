---
title: Informazioni su [!UICONTROL Simple Ad Serving]
description: Scopri le offerte di [!UICONTROL Simple Ad Serving] utilizzando i pixel di tracciamento degli eventi.
feature: DSP Simple Ad Serving
exl-id: 327a2c93-d729-42e1-856f-f0e05efab7ca
source-git-commit: 7e614ecb517515217d812926f61ca10437820efd
workflow-type: tm+mt
source-wordcount: '227'
ht-degree: 0%

---

# Informazioni su [!UICONTROL Simple Ad Serving]

[!UICONTROL Simple Ad Serving] fornisce recapito e reporting garantiti e non decisi di annunci per un editore specificato e un singolo tipo di annuncio utilizzando un singolo posizionamento dedicato. Utilizza [!DNL Simple Ad Serving] quando il tuo editore non può eseguire la tua offerta tramite gli ID offerta. Il targeting, l’andamento del budget, il limite di budget e il limite di frequenza sono gestiti dall’editore. Esegui queste offerte tramite pixel di tracciamento degli eventi.

Con [!UICONTROL Simple Ad Serving], ogni annuncio viene servito direttamente dall&#39;editore (server del sito) e l&#39;DSP fornisce un pixel di tracciamento degli eventi da inviare all&#39;editore, che deve implementare il pixel e il traffico degli annunci DSP. A seconda del tipo di inventario, i pixel dell’evento misurano gli eventi di impression, click-through e riproduzione di video.

Sono disponibili i seguenti tipi di annunci:

* pre-roll standard del desktop
* pre-roll standard per tablet e dispositivi mobili
* pre-roll standard TV collegato
* visualizzare
* audio

È possibile creare un&#39;offerta [!UICONTROL Simple Ad Serving] nella visualizzazione [!UICONTROL Inventory] > [!UICONTROL Deals]. DSP genera automaticamente un posizionamento con il sottotipo &quot;[!DNL Simple ad serving]&quot; per l&#39;annuncio. Il posizionamento esegue il targeting dell’offerta ma non consente un targeting aggiuntivo, un budget o un limite di frequenza. È possibile modificare solo alcune impostazioni dell&#39;offerta, ad esempio il nome dell&#39;offerta, il CPM, le impression e le date del volo.<!-- If you need multiple tracking tags for a [!UICONTROL Simple Ad Serving] deal, create a duplicate deal. -->

I posizionamenti di [!UICONTROL Simple Ad Serving] non sono conformi ai fondi utilizzabili dell&#39;account o ai budget della campagna e del pacchetto. Tuttavia, la spesa viene tracciata e conteggiata in base a tali budget. Anche quando il CPM è pari a $0, i dati dell’evento vengono sempre tracciati.

>[!MORELIKETHIS]
>
>* [Crea un&#39;offerta [!UICONTROL Simple Ad Serving]](simple-deal-create.md)
>* [Modifica impostazioni offerte [!UICONTROL Simple Ad Serving]](simple-deal-edit.md)
>* Impostazioni [[!UICONTROL Simple Ad Serving]](simple-deal-settings.md)
>* [Visualizza un report dettagliato per un&#39;offerta](/help/dsp/inventory/deal-view-report.md)

<!-- add back when reimplemented:
>* [View Event-Tracking Pixels for a [!UICONTROL Simple Ad Serving] Deal](simple-deal-show-pixels.md)
-->
