---
title: Creare più annunci di terze parti
description: Scopri come creare più annunci di terze parti contemporaneamente.
feature: DSP Ads
exl-id: be7c1cc4-3c17-4e37-aae7-c8601d2222a0
source-git-commit: 5139e6022cd5f5f11046d8f38bd0f1db91464928
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Creare più annunci di terze parti

Puoi creare fino a 500 annunci di terze parti alla volta caricando tag che puntano a risorse creative ospitate su server di annunci di terze parti. Puoi includere i pixel di tracciamento per gli annunci.<!-- The bulksheet template for other ad servers says you can include 200. Which is it: 200 or 500? -->

Puoi caricare uno dei due [!DNL DoubleClick] e [!DNL Flashtalking] assegnare tag ai fogli o a un file compilato manualmente utilizzando il modello fornito.

>[!TIP]
>
> La best practice prevede l’utilizzo di annunci di terze parti che vengono serviti in modo sicuro utilizzando HTTPS. Gli URL serviti con HTTPS iniziano con &quot;https&quot;.

1. Nel menu principale, fai clic su **[!UICONTROL Campaigns]**.

1. Fai clic sul nome della campagna in cui l’annuncio verrà incluso.

1. Sopra la tabella dati, fai clic su **[!UICONTROL Create]**. Nella sezione Tipi di annunci del menu , fai clic su **[!UICONTROL Bulk upload ads]**.

1. Seleziona il server di annunci in cui è ospitato l’annuncio: *[!UICONTROL DoubleClick]*, *[!UICONTROL Flashtalking]* oppure *[!UICONTROL Other]*.

1. ([!DNL DoubleClick] e [!DNL Flashtalking] annunci) Seleziona il tipo di tag da utilizzare per ogni risorsa video e per ogni risorsa visualizzata. Le opzioni disponibili variano a seconda del server di annunci.

1. (Annunci su tutti i server di annunci eccetto [!DNL DoubleClick] e [!DNL Flashtalking]) Fai clic su **[!UICONTROL Download this template]** per scaricare un modello in [!DNL Microsoft Excel] formato foglio di calcolo (XLSX), che può essere compilato con i dati degli annunci e salvato localmente. Le colonne richieste includono [!UICONTROL Ad Name], [!UICONTROL VAST/VPAID URL or Ad Tag]e [!UICONTROL Ad Types].

1. Fai clic su **[!UICONTROL Upload]** e selezionare un file in formato .xlsx o .xls dal dispositivo o dalla rete.

   Per [!DNL DoubleClick] e [!DNL Flashtalking] annunci, carica fogli tag non modificati dal server annunci. Per altri server di annunci, utilizza il modello scaricato al passaggio 3.

1. Al termine del caricamento, fai clic su **[!UICONTROL Start Building Ads]**.

1. Rivedi i dettagli e lo stato di ciascun annuncio:

   1. (Annunci video universali con [!DNL Google] o [!DNL Flashtalking] tag) Fai clic sul pulsante **[!UICONTROL Ad Type]** campo e seleziona **[!UICONTROL Universal Video]**.

   1. (Annunci video universali) Per ogni nuovo annuncio, fai clic su ![modifica](/help/dsp/assets/edit.png), seleziona [formato video applicabile](/help/dsp/campaign-management/ads/ad-settings-universal-video.md), quindi fai clic su **Salva**.

   1. Rivedi lo stato di ciascun annuncio, basato sui controlli di convalida sul tag caricato.

   1. (Facoltativo) Effettua una delle seguenti operazioni per ogni annuncio:

      * Per visualizzare in anteprima un annuncio, fai clic su ![play](/help/dsp/assets/play.png) nella riga annuncio.

      * Per modificare i dettagli dell’annuncio, fai clic su ![modifica](/help/dsp/assets/edit.png), modifica i dettagli e fai clic su **Salva**.

      * Per rimuovere un annuncio, fai clic su **[!UICONTROL X]** nella riga annuncio.

1. Fai clic su **[!UICONTROL Create *N *Annunci]**.

1. Effettua una delle seguenti operazioni:

   * Clic **[!UICONTROL Done]**.

   * (In caso di rifiuto di un annuncio; facoltativo) Per modificare il record dell&#39;annuncio e inviare nuovamente l&#39;annuncio per la revisione:

      1. Fai clic sul nome dell’annuncio.

      1. Modifica le impostazioni dell’annuncio.

      1. Clic **[!UICONTROL Save & submit for review]**.

>[!NOTE]
>
>Gli annunci video universali possono essere allegati solo a posizionamenti video universali.

>[!MORELIKETHIS]
>
>* [Informazioni sulla gestione degli annunci](ad-about.md)
>* [Specifiche degli annunci](ad-specs.md)
>* [Creare un singolo annuncio](ad-create.md)
>* [Video: Come caricare in blocco tag di annunci di terze parti](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/dsp/bulk-upload-third-party-ad-tags.html)
>* [Domande frequenti sui video universali](/help/dsp/campaign-management/faq-universal-video.md)

