---
title: Creare più annunci di terze parti
description: Scopri come creare più annunci di terze parti contemporaneamente.
feature: DSP Ads
exl-id: be7c1cc4-3c17-4e37-aae7-c8601d2222a0
source-git-commit: 4b9cc5956d573b346eacdf71a8ea490c162b4660
workflow-type: tm+mt
source-wordcount: '390'
ht-degree: 0%

---

# Creare più annunci di terze parti

Puoi creare fino a 500 annunci di terze parti alla volta caricando tag che puntano a risorse creative ospitate su server di annunci di terze parti. È possibile includere pixel di tracciamento per gli annunci.<!-- The bulksheet template for other ad servers says you can include 200. Which is it: 200 or 500? -->

È possibile caricare [!DNL DoubleClick] e [!DNL Flashtalking] fogli di tag o un file popolato manualmente utilizzando il modello fornito.

>[!TIP]
>
> La best practice prevede l’utilizzo di annunci di terze parti gestiti in modo sicuro tramite HTTPS. Gli URL serviti tramite HTTPS iniziano con &quot;https&quot;.

1. Nel menu principale, fare clic su **[!UICONTROL Campaigns]**.

1. Fai clic sul nome della campagna in cui includere l’annuncio.

1. Sopra la tabella dati, fare clic su **[!UICONTROL Create]**. Nella sezione Tipi di annunci del menu, fare clic su **[!UICONTROL Bulk upload ads]**.

1. Selezionare il server di annunci in cui è ospitato l&#39;annuncio: *[!UICONTROL DoubleClick]*, *[!UICONTROL Flashtalking]* o *[!UICONTROL Other]*.

1. ([!DNL DoubleClick] e [!DNL Flashtalking] annunci) Seleziona il tipo di tag da utilizzare per ogni risorsa video e ogni risorsa di visualizzazione. Le opzioni disponibili variano a seconda del server di annunci.

1. (Annunci su tutti i server di annunci eccetto [!DNL DoubleClick] e [!DNL Flashtalking]) Fare clic su **[!UICONTROL Download this template]** per scaricare un modello in formato foglio di calcolo [!DNL Microsoft Excel] (XLSX), che è possibile compilare con dati di annunci e salvare localmente. Le colonne richieste includono [!UICONTROL Ad Name], [!UICONTROL VAST/VPAID URL or Ad Tag] e [!UICONTROL Ad Types].

1. Fare clic su **[!UICONTROL Upload]** e selezionare un file in formato xlsx o xls dal dispositivo o dalla rete.

   Per [!DNL DoubleClick] e [!DNL Flashtalking] annunci, carica fogli tag non modificati dal server di annunci. Per gli altri server di annunci, utilizza il modello scaricato nel passaggio 3.

1. Al termine del caricamento, fare clic su **[!UICONTROL Start Building Ads]**.

1. Rivedi i dettagli e lo stato di ciascun annuncio:

   1. (Annunci video universali con tag [!DNL Google] o [!DNL Flashtalking]) Fare clic sul campo **[!UICONTROL Ad Type]** e selezionare **[!UICONTROL Universal Video]**.

   1. (Annunci video universali) Per ogni nuovo annuncio, fai clic su ![modifica](/help/dsp/assets/edit.png), seleziona il [formato video applicabile](/help/dsp/campaign-management/ads/ad-settings-universal-video.md), quindi fai clic su **Salva**.

   1. Rivedi lo stato di ciascun annuncio, in base ai controlli di convalida sul tag caricato.

   1. (Facoltativo) Effettua una delle seguenti operazioni per ciascun annuncio:

      * Per visualizzare l&#39;anteprima di un annuncio, fare clic su ![riproduci](/help/dsp/assets/play.png) nella riga dell&#39;annuncio.

      * Per modificare i dettagli dell&#39;annuncio, fare clic su ![modifica](/help/dsp/assets/edit.png), modificare i dettagli, quindi fare clic su **Salva**.

      * Per rimuovere un annuncio, fare clic su **[!UICONTROL X]** nella riga annuncio.

1. Fai clic su **[!UICONTROL Create *N *annuncio/i]**.

1. Effettuare una delle seguenti operazioni:

   * Fare clic su **[!UICONTROL Done]**.

   * (Se un annuncio viene rifiutato; facoltativo) Per modificare il record dell’annuncio e inviare nuovamente l’annuncio per la revisione:

      1. Fai clic sul nome dell’annuncio.

      1. Modifica le impostazioni dell’annuncio.

      1. Fare clic su **[!UICONTROL Save & submit for review]**.

>[!NOTE]
>
>Gli annunci video universali possono essere collegati solo ai posizionamenti video universali.

>[!MORELIKETHIS]
>
>* [Informazioni Sulla Gestione Degli Annunci](ad-about.md)
>* [Specifiche annuncio](ad-specs.md)
>* [Crea un annuncio singolo](ad-create.md)
>* [Video: come caricare in blocco tag di annunci di terze parti](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/dsp/bulk-upload-third-party-ad-tags.html)
>* [Domande frequenti sul video universale](/help/dsp/campaign-management/faq-universal-video.md)
