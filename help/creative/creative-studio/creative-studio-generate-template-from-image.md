---
title: Generare un modello di annuncio da un’immagine utilizzando AI
description: Scopri come utilizzare l’intelligenza artificiale in Creative Studio per convertire un’immagine pubblicitaria statica esistente in un modello di annuncio modificabile.
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: d0d9f2ed-c163-44e1-97a1-4ace121416b8
    internal-label: Creative
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: adc2fdc93f06b5459c19b08306d1e30ce00e7028
workflow-type: tm+mt
source-wordcount: '399'
ht-degree: 0%
---
# Generare un modello di annuncio da un’immagine utilizzando AI

*funzionalità Beta*

Utilizzare AI in [!UICONTROL Creative Studio] per convertire un&#39;immagine annuncio di visualizzazione statica esistente in un modello di annuncio di visualizzazione modificabile. Rivedi il modello generato, richiedi le modifiche utilizzando il linguaggio naturale e apri l’editor modelli per apportare modifiche manuali e salvare il modello.

## Prima di iniziare

È necessario un annuncio immagine statico esistente in una libreria Creative. Questo flusso di lavoro seleziona gli annunci dalle librerie; non carica una nuova immagine direttamente nella finestra di dialogo di generazione.

## Generare e rivedere il modello {#template-generate}

1. Nel menu principale, fare clic su **[!UICONTROL Creative Studio]**.

1. Fare clic sulla scheda **[!UICONTROL Templates]**.

1. (Facoltativo) Seleziona un inserzionista dall&#39;elenco degli inserzionisti nella parte superiore della pagina per visualizzarne le librerie.

1. Nella casella **[!UICONTROL Use AI to Generate a New Display Ad Template]** fare clic su **[!UICONTROL Generate]**.

1. Nella finestra di dialogo **[!UICONTROL Generate New Ad Template]**, seleziona **[!UICONTROL Generate from Existing Standard Ad Image]** se non è già selezionato.

1. Selezionare la libreria contenente l&#39;annuncio immagine dall&#39;elenco **[!UICONTROL Ad Library]**.

1. Posizionare il cursore sulla scheda dell&#39;annuncio immagine e fare clic su **[!UICONTROL Use this Standard Ad]**.

   La generazione inizia automaticamente, utilizzando la larghezza e l’altezza dell’annuncio selezionato.

1. Attendere il termine della generazione, quindi esaminare l&#39;anteprima del modello e il pannello **[!UICONTROL Layers]**, se disponibile.

   Controlla il testo, le immagini e il layout prima di utilizzare il modello. I livelli mostrati qui sono per la revisione; apporta modifiche manuali nell&#39;editor modelli.

1. (Facoltativo) Richiedi modifiche al modello generato:

   1. Nel campo **[!UICONTROL Ask the AI for any changes]**, descrivere le modifiche desiderate. Immettere ad esempio `Change the headline to "Limited Time Offer" and the button text to "Shop Now"`.

   1. Fare clic su **[!UICONTROL Regenerate]**.

   1. Rivedi l’anteprima aggiornata. Ripetere l&#39;operazione in base alle esigenze.

1. Quando si è pronti per continuare, fare clic su **[!UICONTROL Use this Ad Template]**.

   Il modello generato si apre nell’editor di modelli di visualizzazione.

## Modifica e salva il modello {#template-save}

1. Nell&#39;editor modelli, esaminare gli elementi generati e apportare le modifiche rimanenti utilizzando i [controlli dell&#39;editor modelli](creative-studio-manage-templates.md#template-controls).

1. Fare clic su **[!UICONTROL Save]**.

1. Nella finestra di dialogo **[!UICONTROL Update Template]**, immettere o aggiornare **[!UICONTROL Template name]**, selezionare **[!UICONTROL Advertiser]** e facoltativamente aggiungere tag.

1. Fare clic su **[!UICONTROL Update]** per salvare il modello e tornare alla visualizzazione **[!UICONTROL Templates]**.

   Per salvare una copia separata, fare clic su **[!UICONTROL Save As New]**.

Puoi quindi utilizzare il modello per [generare varianti di annunci](creative-studio-manage-templates.md#ad-variations-generate).

## Se non è possibile generare un modello {#troubleshooting}

* **Non sono elencate librerie o annunci di immagini:** Controlla l&#39;inserzionista selezionato e **[!UICONTROL Ad Library]**. Se la libreria non dispone di immagini pubblicitarie standard, seleziona un’altra libreria contenente un annuncio immagine statico esistente.

* **Generazione non riuscita o impossibile convertire l&#39;immagine:** Rivedi il messaggio visualizzato, fai clic su **[!UICONTROL Back to library]** e seleziona un annuncio immagine da riprovare.

>[!MORELIKETHIS]
>
>* [Gestione dei modelli di annunci in Creative Studio](creative-studio-manage-templates.md)
>* [Gestione di annunci standard in Creative Studio](creative-studio-manage-standard-ads.md)