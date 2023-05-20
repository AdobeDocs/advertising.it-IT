---
title: Informazioni su [!UICONTROL Simple Ad Serving]
description: Informazioni su [!UICONTROL Simple Ad Serving] tratta utilizzando pixel di tracciamento degli eventi.
feature: DSP Simple Ad Serving
exl-id: 327a2c93-d729-42e1-856f-f0e05efab7ca
source-git-commit: 7e614ecb517515217d812926f61ca10437820efd
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 0%

---

# Informazioni su [!UICONTROL Simple Ad Serving]

[!UICONTROL Simple Ad Serving] fornisce recapito e reporting di annunci garantiti e non decisi per un editore specificato e un singolo tipo di annuncio utilizzando un singolo posizionamento dedicato. Utilizzare [!DNL Simple Ad Serving] quando l’editore non può eseguire l’offerta tramite gli ID offerta. Il targeting, l’andamento del budget, il limite di budget e il limite di frequenza sono gestiti dall’editore. Esegui queste offerte tramite pixel di tracciamento degli eventi.

Con [!UICONTROL Simple Ad Serving], ogni annuncio viene servito direttamente dall’editore (server del sito) e l’DSP fornisce un pixel di tracciamento degli eventi da inviare all’editore, che deve implementare il pixel e inviare il traffico agli annunci dell’DSP. A seconda del tipo di inventario, i pixel dell’evento misurano gli eventi di impression, click-through e riproduzione di video.

Sono disponibili i seguenti tipi di annunci:

* pre-roll standard del desktop
* pre-roll standard per tablet e dispositivi mobili
* pre-roll standard TV collegato
* visualizzare
* audio

Puoi creare una [!UICONTROL Simple Ad Serving] trattare in [!UICONTROL Inventory] > [!UICONTROL Deals] visualizzazione. L’DSP genera automaticamente un posizionamento con il sottotipo &quot;[!DNL Simple ad serving]&quot; per l’annuncio. Il posizionamento esegue il targeting dell’offerta ma non consente un targeting aggiuntivo, un budget o un limite di frequenza. Puoi modificare solo alcune impostazioni dell’offerta, ad esempio il nome, il CPM, le impression e le date dei voli.<!-- If you need multiple tracking tags for a [!UICONTROL Simple Ad Serving] deal, create a duplicate deal. -->

[!UICONTROL Simple Ad Serving] i posizionamenti non sono conformi ai fondi utilizzabili dell’account o ai budget per campagne e pacchetti. Tuttavia, la spesa viene tracciata e conteggiata in base a tali budget. Anche quando il CPM è pari a $0, i dati dell’evento vengono sempre tracciati.

>[!MORELIKETHIS]
>
>* [Creare un [!UICONTROL Simple Ad Serving] Offerta](simple-deal-create.md)
>* [Modifica [!UICONTROL Simple Ad Serving] Impostazioni offerta](simple-deal-edit.md)
>* [[!UICONTROL Simple Ad Serving] Impostazioni](simple-deal-settings.md)
>* [Visualizzare un rapporto dettagliato per un&#39;offerta](/help/dsp/inventory/deal-view-report.md)


<!-- add back when reimplemented:
>* [View Event-Tracking Pixels for a [!UICONTROL Simple Ad Serving] Deal](simple-deal-show-pixels.md)
-->
