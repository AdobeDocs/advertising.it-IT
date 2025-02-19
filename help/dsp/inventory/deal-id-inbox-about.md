---
title: Informazioni su [!UICONTROL Deal ID Inbox]
description: Scopri la funzione [!UICONTROL Deal ID inbox], che ti consente di accettare offerte private già negoziate con gli editori il [!DNL FreeWheel], [!DNL Google Authorized Buyers] (precedentemente noto come [!DNL AdX]), and [!DNL Magnite DV+] (precedentemente [!DNL Rubicon]).
feature: DSP Private Inventory, DSP Deal IDs
exl-id: a1ba7de0-d6b4-4e22-8615-3e62d2ffdf5c
source-git-commit: 394a281c9b9d7eeab939f4c58508ec1f34eba67c
workflow-type: tm+mt
source-wordcount: '491'
ht-degree: 0%

---

# Informazioni su [!UICONTROL Deal ID Inbox]

Advertising DSP [!UICONTROL Deal ID inbox] consente di impostare rapidamente le offerte importate da DSP dagli editori tramite piattaforme lato fornitura (SSP) in modo da non dover impostare ogni offerta manualmente. È possibile accettare le offerte di inventario privato garantite e non garantite già negoziate con gli editori il [!DNL FreeWheel], [!DNL Google Authorized Buyers] (precedentemente noto come [!DNL AdX]) e [!DNL Magnite DV+] (precedentemente [!DNL Rubicon]) da [!UICONTROL Deal ID inbox].

>[!NOTE]
>
>Advertising DSP è il primo DSP a integrarsi con l&#39;API [!DNL FreeWheel].

In [!UICONTROL Deal ID inbox], puoi visualizzare i dettagli dell&#39;offerta così come vengono visualizzati dall&#39;editore, velocizzare la configurazione dell&#39;offerta ed evitare errori di immissione manuale.

<!-- 
Accepting a deal automatically pre-populates a new Deal ID record with details from the publisher, and you need to enter only the publisher [always? or just in some cases?], the media type, who can access the deal, and any attribute labels to apply to the deal so it's easy to find. [Are labels a dimension you can report on?]

For each available deal, you can review the deal details sent directly from the publisher. Some deals are grouped as proposals (packages), and you can see the individual deal details by reviewing the deal.

You can accept any available deal or move an incorrect deal to the Ignored Deals tab. You can also un-ignore deals, which moves them back to the New Deals tab so you can potentially accept them.

For each deal, you can select one publisher and one media type (Desktop Video, Mobile Video, Connected TV, Display, or Audio), and you can share the deal with specific advertisers and with all advertisers for a specific account.
 -->

DSP aggiorna automaticamente tutti i dettagli dell&#39;offerta ogni giorno alle 4:30 EST. Inoltre aggiorna tutte le [!DNL FreeWheel] offerte e aggiorna le offerte esistenti da [!DNL Google] e [!DNL Magnite DV+] ogni ora. Puoi anche aggiornare manualmente i dettagli dell’offerta per inserire nuove offerte in qualsiasi momento.

<!-- MC: I'm not sure where I got the following. Is this currently true? -->

>[!NOTE]
>
>Per le offerte garantite programmatiche tramite [!DNL Google Authorized Buyers], devi fornire almeno il 90% del budget oppure il tuo account perde l&#39;accesso alle offerte di [!DNL Google] in [!UICONTROL Deal ID inbox].

## Implementazione di [!UICONTROL Deal ID Inbox]

Per ricevere le offerte in [!UICONTROL Deal ID inbox], gli account del provider di servizi condivisi devono mappare l&#39;account DSP dell&#39;organizzazione all&#39;account del provider di servizi condivisi. DSP può condividere i nomi dei conti dell&#39;organizzazione con i provider di servizi condivisi pertinenti. Contatta il team del tuo account Adobe per istruzioni.

Durante le negoziazioni, chiedi all&#39;editore di inviare l&#39;affare al tuo acquirente invece che all&#39;account DSP principale. L&#39;identificativo dell&#39;operazione può essere un nome o un ID, a seconda della SSP.

## Azioni da intraprendere sulle offerte

* **Rivedi le offerte** per verificare che il provider di servizi condivisi abbia inviato l&#39;editore corretto, le date del volo, CPM e altri dettagli dell&#39;offerta. Se l&#39;editore ha commesso un errore, contattali al di fuori di DSP in modo che possano correggere e inviare nuovamente l&#39;affare.

* **Accetta le offerte** dopo la revisione e non verranno più visualizzate in [!UICONTROL Deal ID inbox]. Le offerte accettate sono elencate in [!UICONTROL Inventory] > [!UICONTROL Deals] e sono pronte per il targeting nei posizionamenti degli inserzionisti.

* **Ignora offerte** non necessarie o non richieste. Le offerte ignorate vengono spostate nella scheda [!UICONTROL Ignored Deals] all&#39;interno di [!UICONTROL Deal ID inbox], che funge da archivio. DSP non avvisa i provider di servizi condivisi e gli editori quando si ignora un&#39;offerta.

* **Modifica dettagli per offerte già accettate** da [!UICONTROL Inventory] > [!UICONTROL Deals] (non in [!UICONTROL Deal ID inbox]). Analogamente, quando gli editori inviano modifiche alle offerte, gli inserzionisti sono responsabili dell&#39;implementazione di tali modifiche in [!UICONTROL Inventory] > [!UICONTROL Deals] perché [!UICONTROL Deal ID inbox] non sincronizza le modifiche dai provider di servizi condivisi dopo la configurazione delle offerte.

## Quali tipi di offerte non possono essere accettate?

Quando un&#39;offerta non include l&#39;icona ![Accetta](/help/dsp/assets/accept.png) o un pulsante [!UICONTROL Accept], non puoi accettarla da [!UICONTROL Deal ID inbox]. È invece possibile [creare manualmente i dettagli dell&#39;ID offerta](/help/dsp/inventory/deal-id-create.md).

Non puoi accettare i seguenti tipi di offerte:

* [!DNL Google] offerte che non sono in USD.

* [!DNL Magnite DV+] offerte che non sono in USD

* [!DNL FreeWheel] offerte che non sono nella valuta del tuo account.

* Offerte con data di fine precedente a oggi.

* [!DNL Magnite DV+] vecchie offerte etichettate come &quot;più tipi di file multimediali&quot;.

I dettagli dell’offerta includono il motivo per cui l’offerta non è disponibile per l’accettazione.

>[!MORELIKETHIS]
>
>* [Accetta un&#39;offerta nella casella in entrata dell&#39;ID offerta](deal-id-inbox-accept.md)
>* [Panoramica delle funzionalità di inventario](inventory-overview.md)
