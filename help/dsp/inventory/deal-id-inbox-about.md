---
title: Informazioni sul [!UICONTROL Deal ID Inbox]
description: Scopri le [!UICONTROL Deal ID inbox] che ti consente di accettare offerte private già negoziate con gli editori su [!DNL FreeWheel], [!DNL Google Authorized Buyers] (precedentemente noto come [!DNL AdX]), and [!DNL Magnite DV+] (in precedenza [!DNL Rubicon]).
feature: DSP Private Inventory, DSP Deal IDs
exl-id: a1ba7de0-d6b4-4e22-8615-3e62d2ffdf5c
source-git-commit: 7e614ecb517515217d812926f61ca10437820efd
workflow-type: tm+mt
source-wordcount: '490'
ht-degree: 0%

---

# Informazioni sul [!UICONTROL Deal ID Inbox]

La DSP pubblicitaria [!UICONTROL Deal ID inbox] consente di impostare rapidamente le offerte che DSP importate dagli editori tramite le piattaforme lato fornitura (SSP), in modo da non dover impostare manualmente ciascuna offerta. Puoi accettare le offerte di inventario privato garantite e non garantite su cui hai già negoziato con gli editori [!DNL FreeWheel], [!DNL Google Authorized Buyers] (precedentemente noto come [!DNL AdX]) e [!DNL Magnite DV+] (in precedenza [!DNL Rubicon]) dal [!UICONTROL Deal ID inbox].

>[!NOTE]
>
>La DSP pubblicitaria è la prima DSP da integrare con [!DNL FreeWheel] API.

In [!UICONTROL Deal ID inbox], puoi visualizzare i dettagli dell’offerta come li vede il tuo editore, velocizzare la configurazione dell’offerta ed evitare errori di inserimento manuale.

<!-- 
Accepting a deal automatically pre-populates a new Deal ID record with details from the publisher, and you need to enter only the publisher [always? or just in some cases?], the media type, who can access the deal, and any attribute labels to apply to the deal so it's easy to find. [Are labels a dimension you can report on?]

For each available deal, you can review the deal details sent directly from the publisher. Some deals are grouped as proposals (packages), and you can see the individual deal details by reviewing the deal.
   
You can accept any available deal or move an incorrect deal to the Ignored Deals tab. You can also un-ignore deals, which moves them back to the New Deals tab so you can potentially accept them.

For each deal, you can select one publisher and one media type (Desktop Video, Mobile Video, Connected TV, Display, or Audio), and you can share the deal with specific advertisers and with all advertisers for a specific account.
 -->

DSP automaticamente aggiorna tutti i dettagli dell&#39;offerta ogni giorno alle 4:30 EST. Rinnova anche tutto [!DNL FreeWheel] offerte e aggiornamenti di offerte esistenti da [!DNL Google] e [!DNL Magnite DV+] ogni ora. Puoi anche aggiornare manualmente i dettagli dell&#39;offerta per popolare le nuove offerte in qualsiasi momento.

<!-- MC: I'm not sure where I got the following. Is this currently true? -->
>[!NOTE]
>
>Per offerte programmatiche garantite tramite [!DNL Google Authorized Buyers], devi consegnare almeno il 90% del tuo budget o il tuo account perderà l&#39;accesso a [!DNL Google] le [!UICONTROL Deal ID inbox].

## Implementazione [!UICONTROL Deal ID Inbox]

Per ricevere le tue offerte in [!UICONTROL Deal ID inbox], gli account SSP devono mappare l’account DSP della tua organizzazione sull’account SSP. DSP condividerà i nomi dei conti dell&#39;organizzazione con le relative SSP. Contatta il tuo [!DNL Adobe] per le istruzioni.

Durante le negoziazioni di accordo, di&#39; all&#39;editore di inviare l&#39;offerta al tuo acquirente invece che all&#39;account DSP padre. L&#39;identificatore dell&#39;offerta può essere un nome o un ID, a seconda della SSP.

## Azioni che puoi intraprendere sulle tue offerte

* **Offerte di revisione** per verificare che la SSP abbia inviato l’editore corretto, le date di volo, il CPM e altri dettagli sull’offerta. Se l&#39;editore ha commesso un errore, contattaci al di fuori di DSP in modo che possano correggere e reinviare l&#39;offerta.

* **Accetta offerte** dopo la revisione, e non verranno più visualizzati nella [!UICONTROL Deal ID inbox]. Le offerte accettate sono elencate in [!UICONTROL Inventory] > [!UICONTROL Deals] e sono pronti per essere utilizzati nei posizionamenti degli inserzionisti.

* **Ignora offerte** non sono necessarie o non sono richieste. Le offerte ignorate vengono spostate nel [!UICONTROL Ignored Deals] nella scheda [!UICONTROL Deal ID inbox], che funge da archivio. DSP avvisa gli SSP e gli editori quando ignori un&#39;offerta.

* **Modificare i dettagli per le offerte già accettate** da [!UICONTROL Inventory] > [!UICONTROL Deals] (non nel [!UICONTROL Deal ID inbox]). Allo stesso modo, quando gli editori inviano modifiche alle offerte, gli inserzionisti sono responsabili dell&#39;implementazione di tali modifiche in [!UICONTROL Inventory] > [!UICONTROL Deals] perché [!UICONTROL Deal ID inbox] non sincronizza le modifiche dai SSP dopo l&#39;impostazione delle offerte.

## Quali tipi di offerte non possono essere accettate?

Quando un elenco di offerte non include un ![Accetta](/help/dsp/assets/accept.png) icona o [!UICONTROL Accept] non puoi accettarlo dal [!UICONTROL Deal ID inbox]. Invece, puoi [creare manualmente i dettagli dell&#39;ID offerta](/help/dsp/inventory/deal-id-create.md).

Non puoi accettare i seguenti tipi di offerte:

* [!DNL Google] offerte che non sono in USD.

* [!DNL Magnite DV+] offerte che non sono in USD

* [!DNL FreeWheel] offerte che non sono nella valuta del tuo account.

* Offerte che hanno una data di fine prima di oggi.

* Antico [!DNL Magnite DV+] offerte etichettate come &quot;tipi di media multipli&quot;.

I dettagli dell&#39;offerta includono il motivo per cui l&#39;offerta non è disponibile per l&#39;accettazione.

>[!MORELIKETHIS]
>
>* [Accettare un accordo nella casella in entrata dell’ID offerta](deal-id-inbox-accept.md)
>* [Panoramica delle funzionalità di inventario](inventory-overview.md)

