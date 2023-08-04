---
title: Crea manualmente dettagli ID offerta
description: Scopri come inserire manualmente i dettagli di un ID offerta.
feature: DSP Private Inventory, DSP Deal IDs
exl-id: 20a57919-c68f-4c9d-a8e1-f49484f74655
source-git-commit: 60676d8ef022d2ed61467d7254405695d5f106b3
workflow-type: tm+mt
source-wordcount: '431'
ht-degree: 0%

---

# Crea manualmente dettagli ID offerta

1. Nel menu principale, fai clic su **[!UICONTROL Inventory]** > **[!UICONTROL Deals].**

1. Sopra la tabella dati, fai clic su **[!UICONTROL Create]** e quindi selezionare **[!UICONTROL Deal ID]**.

1. Inserisci il [impostazioni di offerta](deal-id-settings.md):

   1. In [!UICONTROL Deal ID basics] , specifica i dettagli dell&#39;offerta e gli inserzionisti che possono accedere all&#39;offerta. Per le offerte garantite, devi inoltre specificare le date di volo pianificate e il numero stimato di impression, solo a scopo di tracciamento.

      Puoi tenere traccia della velocità delle offerte garantite includendo la colonna &quot;Velocità impression PG&quot; nella vista Inventario > Offerte.

   1. (Solo per utenti amministratori; facoltativo) In [!UICONTROL Technical] , modificare le impostazioni predefinite in base alle esigenze.

   1. Clic **[!UICONTROL Save]**.

1. (Solo offerte garantite) Seleziona gli annunci da utilizzare per l’offerta (o il pixel 1x1 per gli annunci gestiti dall’editore) e crea un posizionamento programmatico garantito (PG) predefinito.

   I posizionamenti PG predefiniti garantiscono che l&#39;offerta restituisca sempre un&#39;offerta per ogni richiesta di offerta. Se non crei un posizionamento PG predefinito, tutti i posizionamenti mirati all’offerta non inviano offerte a meno che non siano impostati correttamente. Dovreste sempre creare un posizionamento PG predefinito. In [!UICONTROL Placements] visualizzazione, i posizionamenti PG predefiniti hanno un [!UICONTROL Sub-type] valore colonna di &quot;[!UICONTROL PG Default].&quot;

   Facoltativamente, puoi utilizzare l’offerta come obiettivo di magazzino in posizionamenti aggiuntivi, ma è necessario impostarla correttamente per fare offerte.

   1. In [!UICONTROL Ad & Campaign Selection] , seleziona gli annunci che verranno utilizzati per l’offerta:

      1. Seleziona l’inserzionista, la campagna e il tipo di annuncio. Facoltativamente, seleziona uno stato dell’annuncio in base al quale filtrare gli annunci.

      1. Dall’elenco degli annunci disponibili, seleziona la casella di controllo accanto a ogni annuncio da utilizzare per l’offerta.

      1. Per gli annunci gestiti dall’editore, viene applicato automaticamente un pixel di tracciamento 1x1 dopo la selezione dell’inserzionista e della campagna.

      1. Clic **[!UICONTROL Apply]**.

   1. Nella schermata delle impostazioni di posizionamento:

      1. Immettete il nome del posizionamento.

      1. (Facoltativo) Modifica il [impostazioni di posizionamento](/help/dsp/campaign-management/placements/placement-settings.md), inclusa la sovrascrittura dell’offerta predefinita, che viene compilata automaticamente con il valore CPM dell’offerta, la modifica dell’intervallo di date o l’aggiunta di altri annunci.

      L’offerta viene impostata automaticamente come destinazione nella sezione Oggetti di inventario. Tutte le altre opzioni di targeting non sono applicabili.

      1. Clic **[!UICONTROL Create placement]**.

Dopo aver creato l&#39;offerta, è possibile utilizzarla come destinazione di magazzino per più posizionamenti.

>[!NOTE]
>
> Non è necessario inviare il tag dell’offerta all’editore per la verifica.

>[!TIP]
>
>* In [!UICONTROL Inventory] > [!UICONTROL Deals] visualizza, il [!UICONTROL Pacing & Budget] Questa colonna mostra il ritmo dell’offerta fino alla data di volo e all’obiettivo di impression specificati.
>
>* Se la consegna è al di sotto o al di sopra del ritmo, contatta l’editore per regolare il volume inviato tramite l’offerta.

>[!MORELIKETHIS]
>
>* [Impostazioni ID offerta manuale](deal-id-settings.md)
>* [Imposta un&#39;offerta programmatica garantita](programmatic-guaranteed-set-up.md)
>* [Inviare un annuncio per un&#39;offerta programmatica garantita con [!DNL FreeWheel]](freewheel-submit.md)
>* [Informazioni sulle offerte garantite programmatiche](programmatic-guaranteed-about.md)
<!-- >* [Specify Placements and Ads for a Private Deal](deal-id-attach-placements.md)-->
