---
title: Informazioni [!UICONTROL Simple Ad Serving]
description: Scopri [!UICONTROL Simple Ad Serving] tratta utilizzando i pixel di tracciamento degli eventi.
feature: DSP Simple Ad Serving
exl-id: d65d1d8e-4d10-4d1d-86d3-f4457c29ae8d
source-git-commit: 1c13874967ec4ad264e5fa6a5e0dfeb6120f53cc
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 0%

---

# Informazioni [!UICONTROL Simple Ad Serving]

[!UICONTROL Simple Ad Serving] fornisce ad delivery e reporting garantiti e non decisionati per uno specifico editore e un singolo tipo di annuncio utilizzando un unico posizionamento dedicato. Utilizzo [!DNL Simple Ad Serving] quando l’editore non può eseguire l’offerta tramite gli ID offerta. L’editore gestisce tutte le funzioni di targeting, pacing del budget, limitazione e limitazione della frequenza. Esegui queste offerte tramite pixel di tracciamento eventi.

Con [!UICONTROL Simple Ad Serving], ogni annuncio viene servito direttamente dall&#39;editore (server del sito) e DSP fornisce un pixel di tracciamento degli eventi da inviare all&#39;editore, che deve implementare il pixel e il traffico degli annunci DSP. A seconda del tipo di inventario, i pixel dell’evento misurano gli eventi di impression, click-through e video riprodotti.

Sono disponibili i seguenti tipi di annunci:

* pre-roll standard desktop
* pre-roll standard per tablet e dispositivi mobili
* pre-roll standard TV collegato
* display
* audio

Puoi creare una [!UICONTROL Simple Ad Serving] l&#39;accordo [!UICONTROL Inventory] > [!UICONTROL Deals] visualizza. DSP genera automaticamente un posizionamento con il sottotipo &quot;[!DNL Simple ad serving]&quot; per l&#39;annuncio. Il posizionamento esegue il targeting dell’offerta ma non consente ulteriori operazioni di targeting, budget o limiti di frequenza. Puoi modificare solo alcune delle impostazioni dell’offerta, ad esempio il nome dell’offerta, CPM, impression e date del volo.<!-- If you need multiple tracking tags for a [!UICONTROL Simple Ad Serving] deal, create a duplicate deal. -->

[!UICONTROL Simple Ad Serving] i posizionamenti non sono conformi ai fondi utilizzabili del conto o ai budget per campagne e pacchetti. Tuttavia, la spesa viene monitorata e conteggiata verso tali budget. Anche quando il CPM è pari a $0, i dati dell’evento vengono sempre tracciati.

>[!MORELIKETHIS]
>
>* [Crea un [!UICONTROL Simple Ad Serving] Offerta](simple-deal-create.md)
>* [Modifica [!UICONTROL Simple Ad Serving] Impostazioni offerte](simple-deal-edit.md)
>* [[!UICONTROL Simple Ad Serving] Impostazioni](simple-deal-settings.md)
>* [Visualizzare un rapporto dettagliato di un&#39;offerta](/help/dsp/inventory/deal-view-report.md)


<!-- add back when reimplemented:
>* [View Event-Tracking Pixels for a [!UICONTROL Simple Ad Serving] Deal](simple-deal-show-pixels.md)
-->
