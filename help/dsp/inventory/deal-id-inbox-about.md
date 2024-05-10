---
title: Informazioni su [!UICONTROL Deal ID Inbox]
description: Scopri di più su [!UICONTROL Deal ID inbox] , che ti consente di accettare offerte private su cui hai già negoziato con gli editori [!DNL FreeWheel], [!DNL Google Authorized Buyers] (precedentemente noto come [!DNL AdX]), and [!DNL Magnite DV+] (in precedenza [!DNL Rubicon]).
feature: DSP Private Inventory, DSP Deal IDs
exl-id: a1ba7de0-d6b4-4e22-8615-3e62d2ffdf5c
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '491'
ht-degree: 0%

---

# Informazioni su [!UICONTROL Deal ID Inbox]

Advertising DSP [!UICONTROL Deal ID inbox] consente di impostare rapidamente le offerte che DSP ha importato dagli editori tramite piattaforme lato offerta (SSP) in modo da non dover impostare ogni offerta manualmente. Puoi accettare le offerte di inventario privato garantite e non garantite già negoziate con gli editori su [!DNL FreeWheel], [!DNL Google Authorized Buyers] (precedentemente noto come [!DNL AdX]), e [!DNL Magnite DV+] (in precedenza [!DNL Rubicon]) dalla [!UICONTROL Deal ID inbox].

>[!NOTE]
>
>Advertising DSP è il primo DSP a integrarsi con [!DNL FreeWheel] API.

In [!UICONTROL Deal ID inbox], puoi visualizzare i dettagli dell’offerta nel modo in cui vengono visualizzati dall’editore, velocizzare la configurazione dell’offerta ed evitare errori di immissione manuali.

<!-- 
Accepting a deal automatically pre-populates a new Deal ID record with details from the publisher, and you need to enter only the publisher [always? or just in some cases?], the media type, who can access the deal, and any attribute labels to apply to the deal so it's easy to find. [Are labels a dimension you can report on?]

For each available deal, you can review the deal details sent directly from the publisher. Some deals are grouped as proposals (packages), and you can see the individual deal details by reviewing the deal.

You can accept any available deal or move an incorrect deal to the Ignored Deals tab. You can also un-ignore deals, which moves them back to the New Deals tab so you can potentially accept them.

For each deal, you can select one publisher and one media type (Desktop Video, Mobile Video, Connected TV, Display, or Audio), and you can share the deal with specific advertisers and with all advertisers for a specific account.
 -->

L&#39;DSP aggiorna automaticamente tutti i dettagli dell&#39;operazione ogni giorno alle 4:30 EST. Inoltre aggiorna tutti [!DNL FreeWheel] offerte e aggiornamenti offerte esistenti da [!DNL Google] e [!DNL Magnite DV+] ogni ora. Puoi anche aggiornare manualmente i dettagli dell’offerta per inserire nuove offerte in qualsiasi momento.

<!-- MC: I'm not sure where I got the following. Is this currently true? -->
>[!NOTE]
>
>Per offerte garantite programmatiche tramite [!DNL Google Authorized Buyers], è necessario fornire almeno il 90% del budget o il tuo account perde l&#39;accesso a [!DNL Google] offerte in [!UICONTROL Deal ID inbox].

## Implementazione di [!UICONTROL Deal ID Inbox]

Per ricevere le offerte nel [!UICONTROL Deal ID inbox], gli account del provider di servizi condivisi devono mappare l&#39;account DSP dell&#39;organizzazione all&#39;account del provider di servizi condivisi. L&#39;DSP può condividere i nomi dei conti dell&#39;organizzazione con i provider di servizi condivisi interessati. Per istruzioni, contatta il team del tuo account di Adobe.

Durante le negoziazioni, chiedi all&#39;editore di inviare l&#39;affare al tuo acquirente invece che all&#39;account DSP principale. L&#39;identificativo dell&#39;operazione può essere un nome o un ID, a seconda della SSP.

## Azioni da intraprendere sulle offerte

* **Rivedi offerte** per verificare che il provider di servizi condivisi abbia inviato l&#39;editore corretto, le date del volo, il CPM e altri dettagli sull&#39;operazione. Se l&#39;editore ha commesso un errore, contattali al di fuori dell&#39;DSP in modo che possano correggere e inviare nuovamente l&#39;affare.

* **Accetta offerte** dopo la revisione e non vengono più visualizzati nel [!UICONTROL Deal ID inbox]. Le offerte accettate sono elencate in [!UICONTROL Inventory] > [!UICONTROL Deals] e sono pronti a eseguire il targeting all’interno dei posizionamenti degli inserzionisti.

* **Ignora offerte** che non sono necessari o non sono sollecitati. Le offerte ignorate vengono spostate in [!UICONTROL Ignored Deals] all&#39;interno del [!UICONTROL Deal ID inbox], che funge da archivio. L’DSP non avvisa i provider di servizi condivisi e gli editori quando si ignora un accordo.

* **Modifica i dettagli delle offerte già accettate** da [!UICONTROL Inventory] > [!UICONTROL Deals] (non in [!UICONTROL Deal ID inbox]). Analogamente, quando gli editori inviano modifiche alle offerte, gli inserzionisti sono responsabili dell’implementazione di tali modifiche in [!UICONTROL Inventory] > [!UICONTROL Deals] perché [!UICONTROL Deal ID inbox] non sincronizza le modifiche dai provider di servizi condivisi dopo la configurazione delle offerte.

## Quali tipi di offerte non possono essere accettate?

Quando un&#39;inserzione non include un ![Accetta](/help/dsp/assets/accept.png) o un [!UICONTROL Accept] , non è possibile accettarlo dal [!UICONTROL Deal ID inbox]. Invece, puoi [creare manualmente i dettagli dell’ID offerta](/help/dsp/inventory/deal-id-create.md).

Non puoi accettare i seguenti tipi di offerte:

* [!DNL Google] offerte che non sono in USD.

* [!DNL Magnite DV+] offerte che non sono in USD

* [!DNL FreeWheel] offerte che non sono nella valuta del tuo account.

* Offerte con data di fine precedente a oggi.

* Vecchio [!DNL Magnite DV+] offerte etichettate come &quot;tipi di media multipli&quot;.

I dettagli dell’offerta includono il motivo per cui l’offerta non è disponibile per l’accettazione.

>[!MORELIKETHIS]
>
>* [Accetta un&#39;offerta nella casella in entrata dell&#39;ID offerta](deal-id-inbox-accept.md)
>* [Panoramica delle funzioni di magazzino](inventory-overview.md)
