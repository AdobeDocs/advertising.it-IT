---
title: Generare un URL di tracciamento dei clic
description: Scopri come generare manualmente un URL di tracciamento dei clic per Search, Social e Commerce.
exl-id: 43a36869-146a-4c5f-b4f2-eddfb856480b
feature: Search Tools, Search Tracking
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '458'
ht-degree: 0%

---

# Generare un URL di tracciamento dei clic per Search, Social e Commerce utilizzando lo strumento URL di tracciamento

*Inserzionisti con solo monitoraggio delle conversioni di Adobe Advertising*

Per informazioni su quando è necessario generare e implementare manualmente un URL di tracciamento dei clic, vedi &quot;[Quando e come generare URL di tracciamento dei clic](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md).&quot;

>[!NOTE]
>
>Questa funzione non implementa il modello di tracciamento o l’URL di destinazione nell’account annuncio rilevante.

1. Nel menu principale, fare clic su **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Tools] >[!UICONTROL Tracking URL]**.

1. Seleziona l’account di rete dell’annuncio dall’elenco.

   ([!DNL Google Ads] parole chiave; testo, installazione app mobile e annunci di ricerca dinamica; posizionamenti; sitelink e gruppi di prodotti) Vengono visualizzati i tag di tracciamento per il campo del modello di tracciamento. Non includono parametri di accodamento a livello di account. Passare al passaggio 4.

   Per tutti gli altri tipi di tag, inserisci le informazioni necessarie per generare un tag.

1. Se necessario, genera un tag:

   1. Specifica le pagine di destinazione, con collegamenti a siti web o nomi di prodotti se richiesto, in uno dei seguenti modi:

      * Specificare un file contenente le informazioni immettendo il percorso completo e il nome del file oppure facendo clic su **[!UICONTROL Browse]** per individuare il file nel dispositivo o nella rete. Il file deve essere un file di testo delimitato da tabulazioni con un elemento per riga nel seguente formato:

         * (Creative, annunci standard) `**landing_page**`

           dove `landing_page` è un URL valido della pagina di destinazione o di base.

           Esempio: http://www.example.com/travel.html

         * ([!DNL Microsoft Advertising] sitelink) `sitelink <tab> ** <tab> landing_page`

           dove `sitelink` è il nome del sitelink e `landing_page` è un URL di pagina di destinazione o un URL di base valido.

           Esempio: `Careers <tab> ** <tab> http://www.example.com/careers.html`

           Il file può includere fino a 10.000 righe.

         * ([!DNL Google Merchant Center] gruppi di prodotti e [!DNL Microsoft Advertising] annunci di prodotto) `product name <tab> ** <tab> landing_page`

           dove `product name` è il nome del prodotto e `landing_page` è un URL di pagina di destinazione o un URL di base valido.

           Esempio: `Acme PR208 <tab> ** <tab> http://www.example.com/travel.html`

           Il file può includere fino a 10.000 righe.

      * Nel campo di immissione immettere un elemento per riga nel formato seguente:

         * (Creative, annunci standard) `landing_page`

           dove `landing_page` è un URL valido della pagina di destinazione o di base.

           Esempio: http://www.example.com/travel.html

         * ([!DNL Microsoft Advertising] sitelink) `sitelink**landing_page`

           dove `sitelink` è il nome del sitelink e `landing_page` è un URL di pagina di destinazione o un URL di base valido.

           Esempio: `Careers**http://www.example.com/careers.html`

         * ([!DNL Google Merchant Center] gruppi di prodotti e [!DNL Microsoft Advertising] annunci di prodotto) `product name**landing_page`

           dove `product name` è il nome del prodotto e `landing_page` è un URL di pagina di destinazione o un URL di base valido.

           Esempio: Acme PR208**http://www.example.com/travel.html

   1. Fare clic su **[!UICONTROL Generate Tracking URLs]**.

1. (Facoltativo) Copia gli URL (che iniziano con &quot;http&quot; o &quot;https&quot;) dalla schermata o dalla pagina di output e implementali nell’account di ricerca o social.

Per gli account con URL di destinazione, immettere i valori nei campi [!UICONTROL Base URL] appropriati.

Per gli account con URL finali, immettere il valore visualizzato sullo schermo nel campo [!UICONTROL Tracking Template] appropriato. Aggiungere un parametro per l&#39;URL finale dopo il parametro `&url=` (ad esempio `{lpurl}`). Per gli account [!DNL Yahoo! Japan Ads], utilizzare il parametro `{lpurl}`. Per un elenco dei parametri [!DNL Google Ads] e [!DNL Microsoft Advertising] per indicare gli URL finali nei modelli di tracciamento, consulta la [[!DNL Google Ads] documentazione](https://support.google.com/google-ads/answer/6305348) (vedi i parametri &quot;Solo modello di tracciamento&quot; nella sezione &quot;Parametri [!DNL ValueTrack] disponibili&quot;) e la [[!DNL Microsoft Advertising] documentazione](https://help.ads.microsoft.com/#apex/3/en/56799/2).

>[!MORELIKETHIS]
>
>* [Informazioni sugli strumenti per creare e decodificare i tag di tracciamento](tracking-tools-about.md)
>* [Quando e come generare gli URL di tracciamento dei clic](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md)
>* [Decodificare un URL di tracciamento dei clic di Ricerca, Social e Commerce](click-tracking-url-decode.md)
