---
title: Esportare e implementare un tag di esperienza annuncio per un’esperienza live
description: Scopri come esportare un tag esperienza annuncio e, facoltativamente, caricarlo in una campagna Advertising DSP.
feature: Creative Experiences
source-git-commit: fc2cd07944026badc0722c1449aa9aaf2c94bfd7
workflow-type: tm+mt
source-wordcount: '525'
ht-degree: 0%

---

# Esportare e implementare un tag di esperienza annuncio per un’esperienza live

*Versione beta chiusa*

Quando un tag annuncio per una dimensione creativa specifica è disponibile per un&#39;esperienza [live](experience-about.md#experience-statuses), puoi generare e copiare il tag nei formati JavaScript e iframe per l&#39;implementazione su Advertising DSP o altro DSP. I tag per l&#39;DSP includono tutte le macro necessarie per l&#39;DSP.

Gli inserzionisti con Advertising DSP possono facoltativamente caricare tag direttamente in una campagna Advertising DSP come annunci.

>[!NOTE]
>
>* Quando crei un&#39;esperienza con il targeting della struttura decisionale, [!DNL Creative] crea automaticamente un tag annuncio per ogni dimensione creativa applicabile.
>* Quando crei un&#39;esperienza senza il targeting della struttura decisionale, devi [creare manualmente un tag annuncio](experience-tag-create-manually.md) per ogni dimensione creativa applicabile.
>* I tag esperienza sono dinamici. Non è necessario aggiornare i tag se si modifica un’esperienza.

## Esportare un tag annuncio per un’esperienza con targeting della struttura decisionale

1. Nel menu principale, fare clic su **[!UICONTROL Creative]** > **[!UICONTROL Experiences]**.

1. Eseguire una delle operazioni seguenti:<!-- I see multiselect, but it's not actually working for me as of 2/3 so I don't know how exporting multiple tags works.-->

   * Nella vista a schede, fai clic su **[!UICONTROL ...]** accanto al nome dell&#39;esperienza e quindi su **[!UICONTROL Tag Manager]**.

   * Nella visualizzazione per tabella, posizionare il cursore sulla riga, fare clic su **[!UICONTROL More]** e quindi su **[!UICONTROL Tag Manager]**

1. Posizionare il cursore sulla riga relativa al tag annuncio applicabile e fare clic su ![Esporta tag annuncio](/help/creative/assets/export.png "Esporta tag annuncio") **[!UICONTROL Export ad tags]** o **[!UICONTROL ... More] > **[!UICONTROL Export ad tags]**.

<!-- Tag Manager has only a list view, but no card view, as of 2/2. -->

1. (Facoltativo) Nella scheda [!UICONTROL Macros], specificare fino a cinque macro personalizzate da includere nel tag. Per ogni macro da includere:

   1. Selezionare una casella di controllo.<!-- Explain more -->

   1. Immettere la macro personalizzata.<!-- Explain more -->

1. Fare clic su **[!UICONTROL Next]** in alto a destra o su **[!UICONTROL Generate ad tags]** nel menu a sinistra.

1. Selezionare il tipo di tag: ** *JavaScript<!-- sic -->* ** o ** *IFRAME* ** <!-- sic -->.

1. Nell&#39;elenco [!UICONTROL Destinations], seleziona la posizione in cui verranno creati gli annunci per l&#39;esperienza.

   * *Adobe Advertising:* Per gli annunci che creerai in Advertising DSP.

   * *Generico:* per gli annunci che creerai in un altro DSP. **Nota:** potrebbe essere necessario includere manualmente ulteriori macro in base alle esigenze.

1. Fare clic su **[!UICONTROL Generate tags]**.

1. Copia o scarica i tag:

   * Per copiare un tag per una singola dimensione di annuncio, espandi la riga del tag, tieni il cursore sopra la riga e fai clic su ![Copia](/help/creative/assets/copy.png "Copia") **[!UICONTROL Copy]**.<!-- why diff than "Copy to clipboard icon used to copy macros for creatives? -->

   * Per scaricare tutti i tag generati come file nel percorso di download predefinito del browser, fai clic su ![Scarica tag](/help/creative/assets/download.png "Scarica tag").

   Puoi aprire il file in un editor di testo per copiare ogni tag. Per i tag di JavaScript, il tag è racchiuso tra `<script></script>` e `<noscript></noscript>` tag. Per i tag iframe, il tag è racchiuso tra `<iframe></iframe>` tag.

1. Implementare i tag per il DSP pertinente:

   * Per DSP diverso da Advertising DSP, fornisci i tag a chiunque creerà gli annunci all’interno dell’DSP.

   * Per Advertising DSP:

      1. Fare clic su **[!UICONTROL Next]** in alto a destra o su **[!UICONTROL DSP link]** nel menu a sinistra.

      1. Seleziona la campagna per la quale diventerà disponibile il tag dell’annuncio.

      1. Fare clic su **[!UICONTROL Assign Tags]**.

         DSP apre alla visualizzazione [!UICONTROL Ads] per la campagna selezionata.

      1. Nella visualizzazione [!UICONTROL Create ads], esaminare i tag dell&#39;annuncio, selezionare ogni tag per il quale si desidera creare un annuncio e quindi fare clic su **[!UICONTROL Create]**.

         La visualizzazione [!UICONTROL Ads] ora include i nuovi annunci, che hanno gli stessi nomi dei tag annuncio in [!DNL Creative]. Puoi [allegare gli annunci a qualsiasi posizionamento](/help/dsp/campaign-management/ads/ad-attach-to-placement.md) nella campagna.

<!-- no way to get back to the Creative Tag Manager -- you have to click back through the main menu -->

<!-- Add this info, with descriptions:

## Ad tag formats

### JavaScript

### Iframe

-->

>[!MORELIKETHIS]
>
>* [Creare manualmente un tag annuncio per una dimensione creativa applicabile](experience-tag-create-manually.md)
>* [Assegna creatività a un tag annuncio per esperienze senza targeting](experience-tag-assign-creatives.md)
>* [Rinominare un tag annuncio](experience-tag-rename.md)
