---
title: '[!UICONTROL Simple Ad Serving] Impostazioni offerta'
description: Scopri le impostazioni disponibili per [!UICONTROL Simple Ad Serving] offerte.
feature: DSP Simple Ad Serving
exl-id: 20e23182-d3d0-457f-a821-0ad4770a138d
source-git-commit: 14f78b89dea8cc680756232c6116975c652feee5
workflow-type: tm+mt
source-wordcount: '467'
ht-degree: 0%

---

# [!UICONTROL Simple Ad Serving] Impostazioni offerta

## Nuovo [!UICONTROL Simple Ad Serving] Offerte

### [!UICONTROL Select Ad Source]

| Parametro | Descrizione |
|-----------|-------------|
| **[!UICONTROL Serving Type]** | Il tipo di supporto per questa offerta: *[!UICONTROL Video],* *[!UICONTROL Display],* o *[!UICONTROL Audio].* |
| **[!UICONTROL Publisher Site Served On]** | Nome dell&#39;editore che sta vendendo questo inventario. Cercare un editore immettendo almeno i primi due caratteri nel nome. Per aggiungere un editore non presente nell’elenco, contatta il team del tuo account di Adobe. |
| **[!UICONTROL Advertiser]** | Un singolo inserzionista nell’account che può accedere a questa offerta. Seleziona anche la campagna e (facoltativamente) il pacchetto in cui è disponibile l’offerta. |
| **[!UICONTROL Media Quality Assessment?]** | (Alcuni utenti) Consente di eseguire l’annuncio su un altro DSP per la verifica di terze parti. <!-- Who can select this? It's disabled for me. Need to see if there are additional fields when this is enabled. --> |
| **[!UICONTROL Ad Source]** | L’unica opzione è *[!UICONTROL Site Serve (Event Pixels)]*. |
| **[!UICONTROL Ad Creation]** | (Solo nuove offerte) Se:<ul><li>*[!UICONTROL Create New]:* Per creare un annuncio per questa offerta.</li><li>*[!UICONTROL Select Ads]:* Per utilizzare un annuncio esistente per questa offerta.</li></ul> |
| **[!UICONTROL Ad Type]** | Il tipo di annuncio per questa offerta. Se desideri creare annunci per l’offerta, includi le dimensioni o la durata dell’annuncio, come richiesto. Le opzioni disponibili variano in base al tipo di supporto. |

{style="table-layout:auto"}

### [!UICONTROL Select Ad(s)]

(Quando utilizzi annunci esistenti) Gli annunci da includere nell’offerta. Seleziona la casella di controllo accanto a ogni annuncio da includere.

### [!UICONTROL Select & Upload [Media Type]]

(Solo per nuovi annunci) Screens per creare un nuovo [annuncio di terze parti](/help/dsp/campaign-management/ads/ad-create-multiple.md).

### [!UICONTROL Feed Details]

| Parametro | Descrizione |
|-----------|-------------|
| **[!UICONTROL Media CPM]** | Il costo per 1000 impression (CPM), come riportato nella scheda tariffaria del contratto. Contatta il team dell’account Adobe per questo valore. <br><br>Specifica anche la valuta per l’offerta. Tutti gli utenti possono selezionare USD o, se la SSP supporta valute aggiuntive, la valuta per il conto DSP. |
| **[!UICONTROL Third Party Billed Fees]** | (Facoltativo) Una commissione statica di terze parti da tracciare come costo non fatturabile e la valuta per l’operazione.<br><br>Tutti gli utenti possono selezionare USD o, se la SSP supporta valute aggiuntive, la valuta per il conto DSP. **NOTA:** Le tariffe fatturabili vengono riportate nel [!UICONTROL Net CPM] metrica. |
| **[!UICONTROL Third Party Fee Description]** | (Facoltativo) Una descrizione delle tariffe di terze parti. |
| **[!UICONTROL Flight Dates]** | Le date di inizio e fine del traffico che utilizza questa offerta. Le date del volo devono essere incluse nelle date del volo della campagna. I tag annuncio restituiscono una risposta solo durante il volo specificato.<br><br> La best practice per creare una semplice campagna pubblicitaria separata con una durata di un anno e per creare pixel di tracciamento al suo interno. |
| **[!UICONTROL Impressions]** | (Facoltativo) Il numero stimato di impression che si prevede di eseguire utilizzando questa offerta. Questo valore viene utilizzato solo a scopo di tracciamento e per contrassegnare quando gli obiettivi di consegna vengono raggiunti; l’editore controlla la consegna effettiva degli annunci. La best practice prevede di inserire un numero elevato di impression per mantenere il tag attivo in DSP in modo che possa essere rinnovato o esteso, se necessario. |
| **[!UICONTROL Deal Name]** | Il nome dell’offerta. Inserisci un nome o seleziona *[!UICONTROL Auto Generate Deal Name]* per consentire all’DSP di generare un nome basato sui dettagli dell’operazione.<br><br>Esempio di nome generato automaticamente: `Campaign-desktop_video_preroll_15-24Kitchen-$10_USD-jdoe-SAS` |
| **[!UICONTROL Attached Ads]** | (Sola lettura) Gli annunci che fanno parte dell’offerta. Per modificare un annuncio, fai clic sul nome dell’annuncio. Per rimuovere un annuncio dall’offerta, fai clic su **[!UICONTROL X]** accanto al nome dell’annuncio. |

{style="table-layout:auto"}

<!-- 
## Existing Simple Ad Serving Deals

Changes aren't applied retroactively.
-->

<!-- completely different settings layout, so need a separate section for them -->

<!-- From Abhinav: Editable fields are Name, Start & End date, Impressions & CPM. Changes are not applied retroactively.

But I see:

| Parameter | Description |
|-----------|-------------|

| **[!UICONTROL Are you using Deal ID?] | (Read-only) Whether the deal was set up as a [!UICONTROL Deal ID] (*[!DNL Yes]*)  or a [!UICONTROL Simple Ad Serving] deal (*[!DNL No]*). |
| **[!UICONTROL Inventory Type] | (Read-only) The inventory type for the deal. |
| **[!UICONTROL Feed Name] | The name of the [!UICONTROL Simple Ad Serving] deal. |
| **[!UICONTROL Publisher Ad Server] | (Read-only)  |
| **[!UICONTROL Publisher maximum ad length] | The maximum length of the ad, per the publisher. |
| **[!UICONTROL Publisher minimum ad length] | The minimum length of the ad, per the publisher. |
| **[!UICONTROL Fill Type] | (Read-only)  |
| **[!UICONTROL Contracted CPM] | This field is required if billing through TubeMogul, but enter your CPM in this field to track your actual spend. |
| **[!UICONTROL 3rd party technology CPM] | (Optional)  |
| **[!UICONTROL Planned Flight Dates] | The beginning and end dates for the deal flight. These dates don't control ad delivery but are used to track delivery pacing. **THIS IS CONTRARY TO WHAT THE NEW DEAL SETTINGS ABOVE, FROM ABHINAV, SAY**> |
| **[!UICONTROL Target Impressions] | (Optional) The estimated number of impressions you expect to run using this deal. This value is used for tracking purposes only and to flag when delivery goals are met; the publisher controls actual ad delivery. The best practice is to enter a high number of impressions to keep the tag active within DSP so it can be renewed or extended if needed. |
 -->

>[!MORELIKETHIS]
>
>* [Informazioni su [!UICONTROL Simple Ad Serving]](simple-deal-about.md)
>* [Creare un [!UICONTROL Simple Ad Serving] Offerta](simple-deal-create.md)
>* [Modifica [!UICONTROL Simple Ad Serving] Impostazioni offerta](simple-deal-edit.md)
>* [Visualizzare un rapporto dettagliato per un&#39;offerta](/help/dsp/inventory/deal-view-report.md)


<!-- add back when reimplemented:
>* [View Event-Tracking Pixels for a [!UICONTROL Simple Ad Serving] Deal](simple-deal-show-pixels.md)
-->
