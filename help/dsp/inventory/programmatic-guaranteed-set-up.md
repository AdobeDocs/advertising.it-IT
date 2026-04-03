---
title: Imposta un'offerta programmatica garantita
description: Scopri come impostare un’offerta programmatica garantita (PG) negoziata con un editore.
feature: DSP Private Inventory, DSP Deal IDs, DSP Programmatic Guaranteed Deals
exl-id: d962942f-c248-4b48-97bd-baa2df3a519e
TQID: https://experienceleague.adobe.com/z7kz7dnCjgCGmlgDlFvbZXTn8d9-OMEunv-Sm-k6TzY
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2:
  - id: ac506c20-96f2-48f6-9096-77706e336bda
  - id: fae3ff5f-9a75-4de1-a100-c90dd8268528
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 452
ht-degree: 0%

---

# Imposta un&#39;offerta programmatica garantita

*[Solo piattaforme lato fornitura supportate](programmatic-guaranteed-about.md)*

Dopo aver negoziato un&#39;offerta programmatica garantita (PG) con un editore supportato, è possibile impostare l&#39;offerta in DSP utilizzando [!DNL Deal ID Inbox] o immettendo manualmente i dettagli dell&#39;offerta.

>[!NOTE]
>
> Per le offerte PG, l’editore gestisce l’andamento del budget, i limiti di budget e il targeting. Tutti i provider di servizi condivisi che consentono PG tramite DSP confermano che l&#39;editore può impostare limiti di budget.
>
> L&#39;impostazione di offerte programmatiche garantite con gli editori su [!DNL FreeWheel] richiede autorizzazioni e passaggi aggiuntivi. Per ulteriori informazioni, vedere &quot;[Panoramica sulla configurazione di offerte programmatiche garantite in [!DNL FreeWheel]](freewheel-overview.md)&quot;.

## Imposta un&#39;offerta programmatica garantita utilizzando [!DNL Deal ID Inbox] {#pg-setup-deal-id-inbox}

Il metodo seguente è la procedura preferita per [!DNL FreeWheel], [!DNL Google Authorized Buyers] e [!DNL Magnite DV+].

1. [Accetta l&#39;offerta](deal-id-inbox-accept.md).

1. Dopo aver salvato l’offerta, seleziona gli annunci (o pixel di tracciamento 1x1 per gli annunci gestiti dall’editore) da utilizzare per l’offerta e crea un posizionamento predefinito programmatico garantito (PG), come richiesto.

   La creazione di un posizionamento PG predefinito per l’offerta è obbligatoria per consegnare il 100% del tuo acquisto. Questo tipo di posizionamento non ha un targeting, pertanto DSP può restituire un’offerta a ogni richiesta di offerta dell’editore.

   * Se accetti una singola offerta, verrai automaticamente reindirizzato al flusso di lavoro di creazione del posizionamento predefinito PG.

     Tutte le [!DNL FreeWheel] offerte sono proposte come un&#39;unica offerta.

   * Se accetti una proposta con più ID offerta PG, identifica ciascun posizionamento PG predefinito da creare. Dopo aver creato tutti i posizionamenti richiesti, il pulsante Continua è attivato.

1. (Facoltativo) Eseguire il targeting dell&#39;offerta PG in posizionamenti aggiuntivi PG o non PG facendo clic sul ![menu Opzioni](/help/dsp/assets/options-menu.png) **>[!UICONTROL Attach new placement]**.

   Un’offerta può essere indirizzata a più posizionamenti che supportano qualsiasi combinazione di tipi di contenuti multimediali (come TV connessa, desktop e audio).

## Imposta manualmente un’offerta programmatica garantita

Utilizzare questo metodo per tutte le altre SSP.

1. [Imposta manualmente i dettagli dell&#39;ID offerta](deal-id-create.md).

1. Dopo aver salvato l’offerta, seleziona gli annunci (o pixel di tracciamento 1x1 per gli annunci gestiti dall’editore) da utilizzare per l’offerta e crea un posizionamento PG predefinito, come richiesto.

   La creazione di un posizionamento PG predefinito per l’offerta è obbligatoria per consegnare il 100% del tuo acquisto. Questo tipo di posizionamento non ha un targeting, pertanto DSP può restituire un’offerta a ogni richiesta di offerta dell’editore.

1. (Facoltativo) Eseguire il targeting dell&#39;offerta PG in posizionamenti aggiuntivi PG o non PG facendo clic sul ![menu Opzioni](/help/dsp/assets/options-menu.png) **>[!UICONTROL Attach new placement]**.

   Un’offerta può essere indirizzata a più posizionamenti che supportano qualsiasi combinazione di tipi di contenuti multimediali (come TV connessa, desktop e audio).

>[!MORELIKETHIS]
>
>* [Informazioni sulle offerte garantite programmatiche](programmatic-guaranteed-about.md)
>* [Suggerimenti per la negoziazione di un&#39;offerta programmatica garantita](/help/dsp/inventory/programmatic-guaranteed-tips.md)
>* [Invia un annuncio per un&#39;offerta programmatica garantita con [!DNL FreeWheel]](freewheel-submit.md)
>* [Accetta un&#39;offerta in [!UICONTROL Deal ID Inbox]](deal-id-inbox-accept.md)
>* [Creare manualmente i dettagli dell&#39;ID offerta](deal-id-create.md)
>* [Partner SSP](ssp-partners.md)
>* [Panoramica delle funzionalità di inventario in Advertising DSP](inventory-overview.md)
