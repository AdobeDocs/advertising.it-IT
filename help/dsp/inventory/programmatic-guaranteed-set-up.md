---
title: Imposta un'offerta programmatica garantita
description: Scopri come impostare un’offerta programmatica garantita (PG) negoziata con un editore.
feature: DSP Private Inventory, DSP Deal IDs, DSP Programmatic Guaranteed Deals
exl-id: d962942f-c248-4b48-97bd-baa2df3a519e
source-git-commit: b1a772acbd9b934f2b4679d1111d56e1059e0cca
workflow-type: tm+mt
source-wordcount: '456'
ht-degree: 0%

---

# Imposta un&#39;offerta programmatica garantita

*[Solo piattaforme lato fornitura supportate](programmatic-guaranteed-about.md)*

Dopo aver negoziato un accordo programmatico garantito (PG) con un editore supportato, puoi impostare l’accordo in ambito DSP utilizzando [!DNL Deal ID inbox] oppure inserendo manualmente i dettagli dell&#39;offerta.

>[!NOTE]
>
> Per le offerte PG, l’editore gestisce l’andamento del budget, i limiti di budget e il targeting. Tutti i provider di servizi condivisi che consentono PG tramite DSP confermano che l’editore può impostare limiti di budget.
>
> Impostazione di offerte garantite programmatiche con editori su [!DNL FreeWheel] richiede autorizzazioni e passaggi aggiuntivi. Consulta &quot;[Panoramica dell’impostazione di offerte programmatiche garantite in [!DNL FreeWheel]](freewheel-overview.md)&quot; per ulteriori informazioni.

## Imposta un&#39;offerta programmatica garantita utilizzando [!DNL Deal ID Inbox] {#pg-setup-deal-id-inbox}

La procedura preferita per [!DNL FreeWheel], [!DNL Google Authorized Buyers], e [!DNL Magnite DV+].

1. [Accetta l&#39;offerta](deal-id-inbox-accept.md).

1. Dopo aver salvato l’offerta, seleziona gli annunci (o pixel di tracciamento 1x1 per gli annunci gestiti dall’editore) che verranno utilizzati per l’offerta e crea un posizionamento predefinito programmatico garantito (PG), come richiesto.

   La creazione di un posizionamento PG predefinito per l’offerta è obbligatoria per consegnare il 100% del tuo acquisto. Questo tipo di posizionamento non ha un targeting, pertanto l’DSP può restituire un’offerta per ogni richiesta di offerta dell’editore.

   * Se accetti una singola offerta, verrai automaticamente reindirizzato al flusso di lavoro di creazione del posizionamento predefinito PG.

     Tutti [!DNL FreeWheel] Le offerte sono proposte come un&#39;unica offerta.

   * Se accetti una proposta con più ID offerta PG, identifica ciascun posizionamento PG predefinito da creare. Dopo aver creato tutti i posizionamenti richiesti, il pulsante Continua è attivato.

1. (Facoltativo) Esegui il targeting dell’offerta PG in posizionamenti aggiuntivi PG o non PG facendo clic su ![Menu Opzioni](/help/dsp/assets/options-menu.png) **>[!UICONTROL Attach new placement]**.

   Un’offerta può essere indirizzata a più posizionamenti che supportano qualsiasi combinazione di tipi di contenuti multimediali (come TV connessa, desktop e audio).

## Imposta manualmente un accordo programmatico garantito

Utilizzare questo metodo per tutte le altre SSP.

1. [Imposta manualmente i dettagli dell’ID offerta](deal-id-create.md).

1. Dopo aver salvato l’offerta, seleziona gli annunci (o pixel di tracciamento 1x1 per gli annunci gestiti dall’editore) che verranno utilizzati per l’offerta e crea un posizionamento PG predefinito, come richiesto.

   La creazione di un posizionamento PG predefinito per l’offerta è obbligatoria per consegnare il 100% del tuo acquisto. Questo tipo di posizionamento non ha un targeting, pertanto l’DSP può restituire un’offerta per ogni richiesta di offerta dell’editore.

1. (Facoltativo) Esegui il targeting dell’offerta PG in posizionamenti aggiuntivi PG o non PG facendo clic su ![Menu Opzioni](/help/dsp/assets/options-menu.png) **>[!UICONTROL Attach new placement]**.

   Un’offerta può essere indirizzata a più posizionamenti che supportano qualsiasi combinazione di tipi di contenuti multimediali (come TV connessa, desktop e audio).

>[!MORELIKETHIS]
>
>* [Informazioni sulle offerte garantite programmatiche](programmatic-guaranteed-about.md)
>* [Suggerimenti per negoziare un accordo programmatico garantito](/help/dsp/inventory/programmatic-guaranteed-tips.md)
>* [Inviare un annuncio per un&#39;offerta programmatica garantita con [!DNL FreeWheel]](freewheel-submit.md)
>* [Accetta un&#39;offerta nella casella in entrata dell&#39;ID offerta](deal-id-inbox-accept.md)
>* [Crea manualmente dettagli ID offerta](deal-id-create.md)
>* [Partner SSP](ssp-partners.md)
>* [Panoramica delle funzioni di magazzino](inventory-overview.md)
