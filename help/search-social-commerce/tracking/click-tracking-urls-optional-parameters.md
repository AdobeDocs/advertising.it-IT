---
title: Parametri di tracciamento facoltativi per gli URL di tracciamento dei clic
description: Scopri i parametri di tracciamento facoltativi per Search, Social e Commerce e i parametri di tracciamento specifici per la rete di annunci che puoi aggiungere agli URL di tracciamento dei clic.
source-git-commit: a24b51405bef1e73ed57b1cb9d012bdfbda9cdec
workflow-type: tm+mt
source-wordcount: '1219'
ht-degree: 0%

---

# Parametri di tracciamento facoltativi per gli URL di tracciamento dei clic

*Google Ads, Microsoft Advertising e Yahoo! Solo account Giappone*

Invece di utilizzare solo i parametri di tracciamento standard per un URL finale o un URL di destinazione, puoi aggiungere altri parametri per tracciare dati specifici per un account di rete di annunci. Puoi aggiungere qualsiasi combinazione dei seguenti parametri nelle impostazioni dell’account o della campagna:

* Puoi aggiungere qualsiasi stringa di testo statica come parametro negli URL di base dell’account o della campagna.

* Adobe Puoi aggiungere parametri specifici per la rete di annunci e annunci pubblicitari negli URL di base dell’account o della campagna per tenere traccia di più dati:

   * I parametri Adobe Advertising sono semistatici. Adobe Advertising inserisce un valore di dati quando carica l’URL di base nella rete di annunci. Ad esempio, quando aggiungi `campaign={ef_campaign}` all’URL di base, Adobe Advertising sostituisce `{ef_campaign}` con il nome effettivo della campagna (ad esempio &quot;Back-to-school-Campaign&quot;) quando carica l’URL.

     **Nota:** Una volta inseriti i valori, questi rimangono statici. Se sposti una parola chiave o un annuncio in un gruppo di annunci diverso o sposti il gruppo di annunci in una campagna diversa, allora  {ef_adgroup} o {ef_campaign} Il parametro non viene aggiornato automaticamente, pertanto devi generare manualmente un nuovo URL di destinazione o URL di base (finale).

   * I parametri specifici della rete di annunci sono dinamici e il motore di ricerca inserisce un valore di dati quando l’utente fa clic su un annuncio. Ad esempio, quando aggiungi `{param1}` all&#39;URL di base, l&#39;ad network lo sostituisce con l&#39;effettivo {param1} valore quando un utente finale fa clic sull’annuncio.

>[!NOTE]
>
>* Separa più parametri con virgole o e commerciali (`&`).
>* I seguenti parametri non fanno distinzione tra maiuscole e minuscole.
>* Nell’URL di destinazione o nell’URL di base (finale) generato, i caratteri speciali nei parametri aggiunti vengono sostituiti come segue:
>  * `=` viene sostituito con `%3D`
>  * `?` viene sostituito con `%26`
>  * uno spazio vuoto viene sostituito con `%2B`
>  Ad esempio, quando aggiungi il parametro `campaign={ef_campaign}` all’URL di base http://www.example.com per una parola chiave, l’URL di base per tale parola chiave viene generato come `http://www.example.com/campaign%3D{ef_campaign}`.

## Parametri di tracciamento statico per Search, Social e Commerce

Puoi utilizzare i seguenti parametri per gli account su qualsiasi rete di annunci e combinarli con i parametri per una rete di annunci specifica, in base alle esigenze. Alcuni di questi parametri duplicano i parametri che vengono aggiunti automaticamente per specifiche reti di annunci quando il metodo di tracciamento dell’account è &quot;[!UICONTROL EF Direct].&quot;

Tutti i seguenti parametri devono essere specificati come coppia chiave-valore; è possibile includere più parametri per una coppia valore. Ad esempio, per inserire il nome della campagna, utilizza `<your_parameter_name>={ef_campaign}`, ad esempio `campaign={ef_campaign}`. Per inserire il tipo di corrispondenza utilizzando i nomi dei tipi di corrispondenza specificati, utilizzare `<your_parameter_name>={ef_mt_broad:<value>}{ef_mt_exact:<value>}{ef_mt_phrase:<value>}`, ad esempio `matchtype={ef_mt_broad:<b>}{ef_mt_exact:<e>}{ef_mt_phrase:<p>}`. I tipi di corrispondenza non applicabili non vengono visualizzati nell’URL risultante.

| Parametro | Descrizione |
| ---- | ---- |
| <code>{custom_code}</code> | Per inserire nell’URL di tracciamento i dati della colonna &quot;Parametro URL personalizzato&quot; in un file bulksheet caricato. {custom_code} può essere utilizzato solo alla fine del valore di una o più coppie chiave-valore nell’URL di tracciamento. Esempi:  <code>a={custom_code}</code>; <code>a={ef_campaignid}{custom_code}</code>; <code>a={ef_campaignid}{custom_code}&amp;b={custom_code}</code><br><br><b>Nota:</b> Per inserire il valore personalizzato dal file bulksheet all’URL di tracciamento, carica il file bulksheet utilizzando l’opzione &quot;Genera URL di tracciamento&quot;. Per ulteriori informazioni sull&#39;utilizzo dei file bulksheet, vedere &quot;[Informazioni sulla gestione dei dati della campagna tramite bulksheet](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).&quot; |
| <code>{ef_uniqueid}</code> | Per inserire l&#39;ID univoco creato da Adobe Advertising. Aggiunto automaticamente quando il metodo di tracciamento è &quot;EF Redirect&quot;. |
| <code>{ef_userid}</code> | Per inserire l&#39;ID utente univoco che Adobe Advertising assegna all&#39;inserzionista. |
| <code>{ef_sid}</code> | Per inserire l’ID numerico assegnato da Search, Social &amp; Commerce alla rete di annunci: <i>[!UICONTROL 3]</i> per [!DNL Google Ads], <i>[!UICONTROL 10]</i> per [!DNL Microsoft® Advertising], <i>[!UICONTROL 45]</i> per [!DNL Meta], <i>[!UICONTROL 86]</i> per [!DNL Yahoo! Display Network], <i>[!UICONTROL 87]</i> per [!DNL Naver], <i>[!UICONTROL 88]</i> per [!DNL Baidu], <i>[!UICONTROL 90]</i> per [!DNL Yandex], <i>[!UICONTROL 94]</i> per [!DNL Yahoo! Japan Ads], <i>[!UICONTROL 105]</i> per [!DNL Yahoo Native] (obsoleto), oppure <i>[!UICONTROL 106]</i> per [!DNL Pinterest] (obsoleto). |
| <code>{ef_searchengine}</code> | Per inserire il nome della rete di annunci. |
| <code>{ef_campaign}</code> | Per inserire il nome della campagna. |
| <code>{ef_campaignid}</code> | Per inserire l’ID della campagna. <b>Nota:</b> L’ID di una nuova campagna viene creato solo dopo che questa è stata pubblicata sulla rete di annunci. Se l’account utilizza le opzioni &quot;EF Redirect&quot; (Reindirizzamento EF) e &quot;AutoUpload&quot; (Caricamento automatico), Adobe Advertising inserisce automaticamente l’ID della campagna negli URL di destinazione o negli URL finali pertinenti il giorno successivo. Se l’account non utilizza le opzioni &quot;EF Redirect&quot; (Reindirizzamento EF) e &quot;Auto Upload&quot; (Caricamento automatico) e desideri inserire l’ID della campagna negli URL di destinazione o negli URL finali pertinenti, devi creare la campagna; scaricare un file di bulksheet per la nuova campagna, utilizzando l’opzione &quot;Generate Tracking URLs;&quot; (Genera URL di tracciamento), quindi pubblicare il file nella rete di annunci. |
| <code>{ef_adgroup}</code> | Per inserire il nome del gruppo di annunci. |
| <code>{ef_adgroupid}</code> | Per inserire l’ID del gruppo di annunci. <b>Nota:</b> L’ID di un nuovo gruppo di annunci viene creato solo dopo che il gruppo è stato pubblicato sulla rete di annunci. Se l’account utilizza le opzioni &quot;EF Redirect&quot; (Reindirizzamento EF) e &quot;AutoUpload&quot; (Caricamento automatico), Adobe Advertising inserisce automaticamente l’ID del gruppo di annunci negli URL di destinazione o negli URL finali pertinenti il giorno successivo. Se l’account non utilizza le opzioni &quot;EF Redirect&quot; (Reindirizzamento EF) e &quot;Auto Upload&quot; (Caricamento automatico) e desideri inserire l’ID del gruppo di annunci negli URL di destinazione o negli URL finali pertinenti, devi creare il gruppo di annunci; scaricare un file bulksheet per il nuovo gruppo di annunci, utilizzando l’opzione &quot;Generate Tracking URLs;&quot; (Genera URL di tracciamento) e quindi pubblicare il file nella rete di annunci. |
| <code>{ef_keyword}</code> | Per inserire la parola chiave. |
| <code>{ef_keywordid}</code> | Per inserire l&#39;ID della parola chiave. <b>Nota:</b> L’ID di una nuova parola chiave viene creato solo dopo che questa è stata pubblicata sulla rete dell’annuncio. Se l’account utilizza le opzioni &quot;EF Redirect&quot; e &quot;Auto Upload&quot; (Caricamento automatico), Adobe Advertising inserisce automaticamente l’ID della parola chiave negli URL di destinazione o negli URL finali pertinenti il giorno successivo. Se l&#39;account non utilizza le opzioni &quot;EF Redirect&quot; e &quot;Auto Upload&quot; e desideri inserire l&#39;ID della parola chiave negli URL di destinazione o negli URL finali pertinenti, devi creare la parola chiave; scaricare un file bulksheet per la nuova parola chiave, utilizzando l&#39;opzione &quot;Generate Tracking URL;&quot; (Genera URL di tracciamento) e quindi pubblicare il file nella rete dell&#39;annuncio. |
| <code>{ef_matchtype}</code> | Per inserire il tipo di corrispondenza della parola chiave come &quot;Broad&quot;, &quot;Exact&quot; o &quot;Phrase&quot;. Incluso automaticamente per Google Ads e Microsoft Advertising con il metodo di tracciamento &quot;EF Redirect&quot;. |
| <code>{ef_adid}</code> | Per inserire l’ID dell’annuncio. <b>Nota:</b> L’ID di un nuovo annuncio viene creato solo dopo che l’annuncio è stato pubblicato sulla rete di annunci. Se l’account utilizza le opzioni &quot;EF Redirect&quot; (Reindirizzamento EF) e &quot;Auto Upload&quot; (Caricamento automatico), Adobe Advertising inserisce automaticamente l’ID dell’annuncio negli URL di destinazione o negli URL finali pertinenti il giorno successivo. Se l’account non utilizza le opzioni &quot;EF Redirect&quot; e &quot;Auto Upload&quot; e desideri inserire l’ID dell’annuncio negli URL di destinazione pertinenti o negli URL finali, devi creare l’annuncio; scaricare un file bulksheet per il nuovo annuncio, utilizzando l’opzione &quot;Generate Tracking URLs;&quot; (Genera URL di tracciamento) e quindi pubblicare il file nella rete dell’annuncio. |

## Parametri di tracciamento dinamico di Google Ads

Consulta [https://support.google.com/google-ads/answer/2375447](https://support.google.com/google-ads/answer/2375447).

## Parametri di tracciamento dinamico di Microsoft Advertising

Consulta [https://help.bingads.microsoft.com/#apex/3/en/51091/2](https://help.bingads.microsoft.com/#apex/3/en/51091/2).

## Parametri di tracciamento dinamico nativi Yahoo

Consulta [https://developer.yahoo.com/nativeandsearch/guide/resources/dynamic-parameters](https://developer.yahoo.com/nativeandsearch/guide/resources/dynamic-parameters).

## Yahoo! Parametri di tracciamento dinamico di Japan Ads

Consulta [https://ads-help.yahoo-net.jp/s/article/H000044463?language=en_US](https://ads-help.yahoo-net.jp/s/article/H000044463?language=en_US).

## Parametri di tracciamento dinamico Yandex

Consulta [https://yandex.com/support/direct/statistics/url-tags.html](https://yandex.com/support/direct/statistics/url-tags.html).

>[!MORELIKETHIS]
>
>* [Informazioni sui formati degli URL di tracciamento dei clic per il servizio di tracciamento delle conversioni di Adobe Advertising](/help/search-social-commerce/tracking/formats-click-tracking-about.md)
