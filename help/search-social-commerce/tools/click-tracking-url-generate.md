---
title: Generare un URL di tracciamento dei clic
description: Scopri come generare manualmente un URL di tracciamento dei clic per Search, Social e Commerce.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '469'
ht-degree: 0%

---

# Generare un URL di tracciamento dei clic di Search, Social &amp; Commerce utilizzando lo strumento URL di tracciamento

*Per gli inserzionisti con solo il tracciamento delle conversioni Adobe Advertising*

Per informazioni su quando è necessario generare e implementare manualmente un URL di tracciamento dei clic, consulta &quot;[Quando e come generare URL di tracciamento dei clic](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md).&quot;

>[!NOTE]
>
>Questa funzione non implementa il modello di tracciamento o l’URL di destinazione nell’account annuncio rilevante.

1. Nel menu principale, fai clic su **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Tracking URL]**.

1. Seleziona l’account di rete dell’annuncio dall’elenco.

   ([!DNL Google Ads] parole chiave; testo, installazione di app mobili e annunci di ricerca dinamica; posizionamenti; sitelink e gruppi di prodotti) Vengono visualizzati i tag di tracciamento per il campo del modello di tracciamento. Non includono parametri di accodamento a livello di account. Passare al passaggio 4.

   Per tutti gli altri tipi di tag, inserisci le informazioni necessarie per generare un tag.

1. Se necessario, genera un tag:

   1. Specifica le pagine di destinazione, con collegamenti a siti web o nomi di prodotti se richiesto, in uno dei seguenti modi:

      * Specificare un file contenente le informazioni immettendo il percorso completo e il nome del file oppure facendo clic su **[!UICONTROL Browse]** per individuare il file sul dispositivo o sulla rete. Il file deve essere un file di testo delimitato da tabulazioni con un elemento per riga nel seguente formato:

         * (Creative, annunci standard) `**landing_page**`

            dove `landing_page` è un URL di pagina di destinazione o un URL di base valido.

            Esempio: http://www.example.com/travel.html

         * ([!DNL Microsoft® Advertising] sitelink) `sitelink <tab> ** <tab> landing_page`

            dove `sitelink` è il nome del sitelink e `landing_page` è un URL di pagina di destinazione o un URL di base valido.

            Esempio: `Careers <tab> ** <tab> http://www.example.com/careers.html`

            Il file può includere fino a 10.000 righe.

         * ([!DNL Google Merchant Center] gruppi di prodotti e [Microsoft® Advertising] annunci di prodotti) `product name <tab> ** <tab> landing_page`

            dove `product name` è il nome del prodotto e `landing_page` è un URL di pagina di destinazione o un URL di base valido.

            Esempio: `Acme PR208 <tab> ** <tab> http://www.example.com/travel.html`

            Il file può includere fino a 10.000 righe.
      * Nel campo di immissione immettere un elemento per riga nel formato seguente:

         * (Creative, annunci standard) `landing_page`

            dove `landing_page` è un URL di pagina di destinazione o un URL di base valido.

            Esempio: http://www.example.com/travel.html

         * ([!DNL Microsoft® Advertising] sitelink) `sitelink**landing_page`

            dove `sitelink` è il nome del sitelink e `landing_page` è un URL di pagina di destinazione o un URL di base valido.

            Esempio: `Careers**http://www.example.com/careers.html`

         * ([!DNL Google Merchant Center] gruppi di prodotti e [!DNL Microsoft® Advertising] annunci di prodotti) `product name**landing_page`

            dove `product name` è il nome del prodotto e `landing_page` è un URL di pagina di destinazione o un URL di base valido.

            Esempio: Acme PR208**http://www.example.com/travel.html
   1. Clic **[!UICONTROL Generate Tracking URLs]**.



1. (Facoltativo) Copia gli URL (che iniziano con &quot;http&quot; o &quot;https&quot;) dalla schermata o dalla pagina di output e implementali nell’account di ricerca o social.

Per i conti con URL di destinazione, inserisci i valori nel [!UICONTROL Base URL] campi.

Per i conti con URL finali, inserisci il valore su schermo nell’appropriato [!UICONTROL Tracking Template] campo. È necessario aggiungere un parametro per l’URL finale dopo il `&url=` parametro (ad esempio `{lpurl}`). Per [!DNL Yahoo! Japan Ads] account, utilizza il parametro `{lpurl}`. Per un elenco di [!DNL Google Ads] e [!DNL Microsoft® Advertising] parametri per indicare gli URL finali nei modelli di tracciamento, vedi [[!DNL Google Ads] documentazione](https://support.google.com/google-ads/answer/6305348) (vedi i parametri &quot;Solo modello di tracciamento&quot; nella sezione &quot;Parametri ValueTrack disponibili&quot;) e il [[!DNL Microsoft® Advertising] documentazione](https://help.ads.microsoft.com/#apex/3/en/56799/2).

>[!MORELIKETHIS]
>
>* [Informazioni sugli strumenti per creare e decodificare i tag di tracciamento](tracking-tools-about.md)
>* [Quando e come generare URL di tracciamento dei clic](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md)
>* [Decodificare un URL di tracciamento dei clic di Search, Social &amp; Commerce](click-tracking-url-decode.md)

