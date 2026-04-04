---
title: Specificare posizionamenti e annunci per un’offerta privata
description: Scopri come utilizzare un’offerta privata con posizionamenti e annunci aggiuntivi.
feature: DSP Private Inventory, DSP Deal IDs, DSP Programmatic Guaranteed Deals
exl-id: 09119471-429d-413e-8033-e29e1558abb0
TQID: https://experienceleague.adobe.com/ZCFqnc6cQLEqahDoElttE7DzeZCR3IRx2lkyyb3BPMs
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2:
  - id: ac506c20-96f2-48f6-9096-77706e336bda
  - id: fae3ff5f-9a75-4de1-a100-c90dd8268528
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 3b9845e85cd91cdece195593b43cbaf851368f9e
workflow-type: tm+mt
source-wordcount: 275
ht-degree: 0%

---

# Specificare posizionamenti e annunci per un’offerta privata

Per le offerte non garantite, è possibile specificare l&#39;offerta come destinazione di magazzino per i nuovi posizionamenti dalla visualizzazione [!UICONTROL Placements].

Per offerte programmatiche garantite (PG), puoi creare posizionamenti con annunci specifici dalla visualizzazione [!UICONTROL Deals].

Puoi anche [allegare annunci ai posizionamenti](/help/dsp/campaign-management/ads/ad-attach-to-placement.md) associati a offerte PG e non garantite in qualsiasi momento.

## Specificare un&#39;offerta non garantita come destinazione di magazzino per un posizionamento

* [Crea un posizionamento dalla visualizzazione [!UICONTROL Placements]](/help/dsp/campaign-management/placements/placement-create.md). Nelle impostazioni [!UICONTROL Inventory Targeting], seleziona l&#39;offerta privata.

## Allega posizionamenti e annunci a un&#39;offerta PG

1. Nel menu principale, fare clic su **[!UICONTROL Inventory]** > **[!UICONTROL Deals].**

1. Nella riga dell&#39;offerta, fare clic su **[!UICONTROL ...]** > **[!UICONTROL Attach New Placement]**.

1. Nelle impostazioni [!UICONTROL Ad & Campaign Selection], seleziona gli annunci da utilizzare per il posizionamento:

   1. Seleziona l’inserzionista, la campagna e il tipo di annuncio. Facoltativamente, seleziona uno stato dell’annuncio in base al quale filtrare gli annunci.

   1. Dall’elenco degli annunci disponibili, seleziona la casella di controllo accanto a ogni annuncio da utilizzare per l’offerta.

   1. Fare clic su **[!UICONTROL Apply]**.

1. Nella schermata delle impostazioni di posizionamento:

   1. Immettete il nome del posizionamento.

   1. (Facoltativo) Modifica le [impostazioni di posizionamento](/help/dsp/campaign-management/placements/placement-settings.md), inclusa la sovrascrittura dell&#39;offerta predefinita, che viene automaticamente compilata con il valore CPM dell&#39;offerta, la modifica dell&#39;intervallo di date o l&#39;aggiunta di altri annunci.

      L’offerta viene impostata automaticamente come destinazione nella sezione Oggetti di inventario. Tutte le altre opzioni di targeting non sono applicabili.

   1. Fare clic su **[!UICONTROL Create placement]**.

Il posizionamento inizia a essere eseguito dopo che l’editore ha attivato l’ID offerta PG.

>[!NOTE]
>
> Non è necessario inviare il tag dell’offerta all’editore per la verifica.

>[!MORELIKETHIS]
>
>* [Informazioni sull&#39;inventario privato](private-inventory-about.md)
>* [Elencare posizionamenti e annunci per un&#39;offerta privata](/help/dsp/inventory/private-deal-view-placements.md)
>* [Creare manualmente i dettagli dell&#39;ID offerta](deal-id-create.md)
>* [Impostazioni ID offerta manuale](deal-id-settings.md)
>* [Imposta un&#39;offerta programmatica garantita](programmatic-guaranteed-set-up.md)
