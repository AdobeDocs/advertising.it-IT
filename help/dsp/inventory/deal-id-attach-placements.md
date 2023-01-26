---
title: Specificare posizionamenti e annunci per un'offerta privata
description: Scopri come utilizzare un’offerta privata con posizionamenti e annunci aggiuntivi.
feature: DSP Private Inventory, DSP Deal IDs, DSP Programmatic Guaranteed Deals
exl-id: 669cadcf-021b-4129-95d5-3d24af4a4b88
source-git-commit: 7055a9b9d3a68ef2f690e146128d6946e713586a
workflow-type: tm+mt
source-wordcount: '283'
ht-degree: 1%

---

# Specificare posizionamenti e annunci per un&#39;offerta privata

Per le offerte non garantite, puoi specificare l&#39;offerta come target di inventario per i nuovi posizionamenti dal [!UICONTROL Placements] visualizza.

Per le offerte a livello di programmazione garantite (PG), puoi creare posizionamenti con annunci specifici dal [!UICONTROL Deals] visualizza.

È inoltre possibile [allegare nuovi annunci ai posizionamenti esistenti](/help/dsp/campaign-management/ads/ad-attach-to-placement.md) associati a PG e a operazioni non garantite in qualsiasi momento.

## Specificare un&#39;operazione non garantita come destinazione di inventario per un posizionamento

* [Crea un posizionamento dal [!UICONTROL Placements] visualizzare](/help/dsp/campaign-management/placements/placement-create.md). In [!UICONTROL Inventory Targeting] seleziona l&#39;offerta privata.

## Allega posizionamenti e annunci a un accordo PG

1. Nel menu principale, fai clic su **[!UICONTROL Inventory]> [!UICONTROL Deals].**

1. Nella riga dell&#39;offerta, fai clic su  **[!UICONTROL ...]>[!UICONTROL Attach New Placement]**.

1. In [!UICONTROL Ad & Campaign Selection] seleziona gli annunci da utilizzare per il posizionamento:

       1. Seleziona l’inserzionista, la campagna e il tipo di annuncio. Facoltativamente, seleziona uno stato di annuncio in base al quale filtrare gli annunci.
       
       1. Dall’elenco degli annunci disponibili, seleziona la casella di controllo accanto a ciascun annuncio che verrà utilizzato per l’offerta.
       
       1. Clic **[!UICONTROL Apply]**.
   
   1. Nella schermata delle impostazioni di posizionamento:

      1. Immettere il nome del posizionamento.

      1. (Facoltativo) Modifica il [impostazioni di posizionamento](/help/dsp/campaign-management/placements/placement-settings.md), compresa la sovrascrittura dell&#39;offerta predefinita, compilata automaticamente con il valore CPM dell&#39;operazione; modifica dell’intervallo di date; o allegando altri annunci.

      L&#39;offerta viene automaticamente indirizzata nella sezione Destinazioni di inventario . Tutte le altre opzioni di targeting non sono applicabili.

      1. Clic **[!UICONTROL Create placement]**.


Il posizionamento inizierà a essere eseguito dopo che l’editore avrà attivato il tuo ID offerta PG.

>[!NOTE]
>
> Non devi inviare il tag dell’offerta all’editore per la verifica.

>[!MORELIKETHIS]
>
>* [Informazioni su Inventario privato](private-inventory-about.md)
>* [Elenco di posizionamenti e annunci per un&#39;offerta privata](/help/dsp/inventory/private-deal-view-placements.md)
>* [Creare manualmente i dettagli dell’ID offerta](deal-id-create.md)
>* [Impostazioni ID offerta manuale](deal-id-settings.md)
>* [Imposta un accordo garantito programmatico](programmatic-guaranteed-set-up.md)

