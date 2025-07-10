---
title: Esportare e implementare un tag di esperienza annuncio per un’esperienza live
description: Scopri come esportare un tag esperienza annuncio e, facoltativamente, caricarlo in una campagna Advertising DSP.
feature: Creative Experiences
exl-id: 4ae05142-8319-4329-96d7-f87d77f02745
source-git-commit: 45b2dad83aa626ea30e7553df7caaf5e7f53b3e1
workflow-type: tm+mt
source-wordcount: '602'
ht-degree: 0%

---

# Esportare e implementare un tag di esperienza annuncio per un’esperienza live

*Versione beta chiusa*

Quando un tag annuncio per una dimensione creativa specifica è disponibile per un&#39;esperienza [live](experience-about.md#experience-statuses), puoi generare e copiare il tag nei formati JavaScript e iframe per l&#39;implementazione su Advertising DSP o altre DSP. I tag per DSP includono tutte le macro necessarie per DSP.

Gli inserzionisti con Advertising DSP possono facoltativamente caricare tag direttamente in una campagna Advertising DSP come annunci con tipo di annuncio &quot;visualizzazione standard&quot;.

>[!NOTE]
>
>* Quando crei un&#39;esperienza con il targeting della struttura decisionale, [!DNL Creative] crea automaticamente un tag annuncio per ogni dimensione creativa applicabile.
>* Quando crei un&#39;esperienza senza il targeting della struttura decisionale, devi [creare manualmente un tag annuncio](experience-tag-create-manually.md) per ogni dimensione creativa applicabile.
>* I tag esperienza sono dinamici. Non è necessario aggiornare i tag se si modifica un’esperienza.
>* Assicurati che le campagne in cui implementerai un’esperienza pubblicitaria includano un targeting compatibile con l’esperienza. Il comportamento di targeting gerarchico può variare a seconda di DSP. In Advertising DSP, il targeting a livello di annuncio viene applicato a livello di posizionamento (non al suo posto).

1. Nel menu principale, fare clic su **[!UICONTROL Creative]** > **[!UICONTROL Experiences]**.

1. Eseguire una delle operazioni seguenti:<!-- I see multiselect, but it's not actually working for me as of 2/3 so I don't know how exporting multiple tags works.-->

   * Nella vista a schede, fai clic su **[!UICONTROL ...]** accanto al nome dell&#39;esperienza e quindi su **[!UICONTROL Tag Manager]**.

   * Nella visualizzazione per tabella, posizionare il cursore sulla riga, fare clic su **[!UICONTROL More]** e quindi su **[!UICONTROL Tag Manager]**.

1. Posizionare il cursore sulla riga relativa al tag annuncio applicabile e fare clic su ![Esporta tag annuncio](/help/creative/assets/export.png "Esporta tag annuncio") **[!UICONTROL Export ad tags]** o **[!UICONTROL ... More] > &#x200B;** [!UICONTROL Export ad tags]**.

>[!NOTE]
>
>Per esperienze annuncio video standard, attendi che la colonna [!UICONTROL Tag Status] mostri &quot;[!UICONTROL Ready]&quot;, che indica che tutti i video nell&#39;esperienza sono stati transcodificati. Tutti i creativi video vengono automaticamente transcodificati da DSP, ma è possibile [applicare una transcodifica specifica per l&#39;editore](experience-tag-video-transcoding.md) a qualsiasi tag esperienza annuncio video.

<!-- Tag Manager has only a list view, but no card view, as of 2/2. -->

1. (Facoltativo) Nella scheda [!UICONTROL Macros], specificare fino a cinque macro personalizzate da includere nel tag. Per ogni macro da includere:

   1. Selezionare una casella di controllo.<!-- Explain more -->

   1. Immettere la macro personalizzata.<!-- Explain more -->

1. Fare clic su **[!UICONTROL Next]** in alto a destra o su **[!UICONTROL Generate ad tags]** nel menu a sinistra.

1. Selezionare il tipo di tag: ** *JavaScript<!-- sic -->* **&#x200B; o &#x200B;** *IFRAME* ** <!-- sic -->.

1. Nell&#39;elenco [!UICONTROL Destinations], seleziona la posizione in cui creare gli annunci per l&#39;esperienza.

   * *Generico:* per gli annunci che creerai in altre DSP. **Nota:** potrebbe essere necessario includere manualmente [ulteriori macro](/help/creative/creative-macros.md) in base alle esigenze.

   * *Adobe AdCloud:* per annunci che creerai in Advertising DSP.

   * *Google CM360:* Per gli annunci che creerai in [!DNL Google Campaign Manager 360]. **Nota:** potrebbe essere necessario includere manualmente [ulteriori macro](/help/creative/creative-macros.md) in base alle esigenze.

1. Fare clic su **[!UICONTROL Generate tags]**.

1. Copia o scarica i tag:

   * Per copiare un tag per una singola dimensione di annuncio, espandi la riga del tag, tieni il cursore sopra la riga e fai clic su ![Copia](/help/creative/assets/copy.png "Copia") **[!UICONTROL Copy]**.<!-- why diff than "Copy to clipboard icon used to copy macros for creatives? -->

   * Per scaricare tutti i tag generati come file nel percorso di download predefinito del browser, fai clic su ![Scarica tag](/help/creative/assets/download.png "Scarica tag").

   Puoi aprire il file in un editor di testo per copiare ogni tag. Per i tag di JavaScript, il tag è racchiuso tra `<script></script>` e `<noscript></noscript>` tag. Per i tag iframe, il tag è racchiuso tra `<iframe></iframe>` tag.

1. Implementare i tag per il DSP pertinente:

   * Per le DSP diverse da Advertising DSP, fornisci i tag a chiunque creerà gli annunci all’interno di DSP.

   * Per Advertising DSP:

      1. Fare clic su **[!UICONTROL Next]** in alto a destra o su **[!UICONTROL DSP link]** nel menu a sinistra.

      1. Seleziona la campagna in cui desideri caricare il tag dell’annuncio.

      1. Fare clic su **[!UICONTROL Assign Tags]**.

         DSP apre la visualizzazione [!UICONTROL Ads] per la campagna selezionata.

      1. Nella visualizzazione [!UICONTROL Create ads], esaminare i tag dell&#39;annuncio, selezionare ogni tag per il quale si desidera creare un annuncio e quindi fare clic su **[!UICONTROL Create]**.

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
>* [Personalizzare le opzioni di transcodifica per un tag esperienza annuncio video](experience-tag-video-transcoding.md)
