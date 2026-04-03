---
title: Invia un annuncio per un'offerta PG a  [!DNL FreeWheel]
description: Scopri come richiedere l'approvazione per un annuncio per un accordo programmatico garantito con un editore su [!DNL FreeWheel].
feature: DSP Private Inventory, DSP Deal IDs
exl-id: 18d91f0c-4a27-4e40-b762-6c5e97e9a21a
TQID: https://experienceleague.adobe.com/f6Cu6mG77YOjwshI4xVbkLSkykAhqXonfSMg5ynDK5g
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2:
  - id: ac506c20-96f2-48f6-9096-77706e336bda
  - id: fae3ff5f-9a75-4de1-a100-c90dd8268528
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 237
ht-degree: 0%

---

# Invia un annuncio per un&#39;offerta programmatica garantita a [!DNL FreeWheel]

*Account con solo l&#39;autorizzazione Programmatica garantita [!DNL FreeWheel]*

Dopo aver [accettato un&#39;offerta programmatica garantita con un editore su FreeWheel](#programmatic-guaranteed-set-up.md#pg-setup-deal-id-inbox), inclusa la selezione di un annuncio e la creazione del posizionamento predefinito programmatico garantito da utilizzare per l&#39;offerta, è necessario inviare l&#39;annuncio a [!DNL FreeWheel] per l&#39;approvazione.

>[!PREREQUISITES]
>
>Rivolgiti al team del tuo account Adobe per assicurarti che l&#39;account [!DNL DSP] disponga dell&#39;autorizzazione per utilizzare il flusso di lavoro programmatico garantito di [!DNL FreeWheel].

1. Copia la chiave dell&#39;annuncio utilizzato con l&#39;offerta [!DNL FreeWheel]:

   1. Fai clic sul nome della campagna.

   1. Nel sottomenu fare clic su **[!UICONTROL Ads]**.

   1. Fai clic su **[!UICONTROL ...]** > **[!UICONTROL Edit]** accanto al nome dell&#39;annuncio.

   1. Una volta aperte le impostazioni dell’annuncio, copia la chiave alfanumerica nell’URL visualizzato nella barra degli indirizzi del browser.

      Ad esempio, nell&#39;URL seguente, la chiave annuncio è `3NtNC5ZbaGZtqbei8jD3`

      ```
      https://advertising.adobe.com/configurator/ad/3NtNC5ZbaGZtqbei8jD3?referrer=/playtime/ads
      ```

1. Invia l&#39;annuncio a [!DNL FreeWheel]:

   1. Effettuare una delle seguenti operazioni:

      * Accanto al nome dell&#39;annuncio, fare clic su **[!UICONTROL ...]** > **[!UICONTROL submit to FreeWheel]**.

      * Nel menu principale, fare clic su **[!UICONTROL Inventory]** > **[!UICONTROL Deals]**. Nella riga dell&#39;offerta fare clic su ![Menu Opzioni](/help/dsp/assets/options-menu.png) > **[!UICONTROL submit to FreeWheel]**.

   1. Verificare l&#39;ID offerta, immettere il **[!UICONTROL Ad Key]** copiato nel passaggio 1, quindi fare clic su **[!UICONTROL Submit]**.

   L’annuncio deve essere inviato e approvato prima di essere eseguito.

1. [Verifica lo stato di invio dell&#39;annuncio](freewheel-check-status.md).

>[!MORELIKETHIS]
>
>* [Panoramica sulla configurazione di offerte programmatiche garantite in [!DNL FreeWheel]](freewheel-overview.md)
>* [Accetta un&#39;offerta in [!UICONTROL Deal ID Inbox]](deal-id-inbox-accept.md)
>* [Verifica lo stato degli annunci per un&#39;offerta [!DNL FreeWheel] PG](freewheel-check-status.md)
>* [Codici di errore per [!DNL FreeWheel] invii di annunci](freewheel-error-codes.md)
