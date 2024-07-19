---
title: Invia un annuncio per un'offerta PG a [!DNL FreeWheel]
description: Scopri come richiedere l'approvazione per un annuncio per un accordo programmatico garantito con un editore su [!DNL Freewheel].
feature: DSP Private Inventory, DSP Deal IDs
exl-id: 18d91f0c-4a27-4e40-b762-6c5e97e9a21a
source-git-commit: 14f78b89dea8cc680756232c6116975c652feee5
workflow-type: tm+mt
source-wordcount: '240'
ht-degree: 0%

---

# Invia un annuncio per un&#39;offerta programmatica garantita a [!DNL Freewheel]

*Account con solo l&#39;autorizzazione Programmatica garantita [!DNL FreeWheel]*

Dopo aver [accettato un&#39;offerta programmatica garantita con un editore su FreeWheel](#programmatic-guaranteed-set-up.md#pg-setup-deal-id-inbox), inclusa la selezione di un annuncio e la creazione del posizionamento predefinito programmatico garantito da utilizzare per l&#39;offerta, è necessario inviare l&#39;annuncio a [!DNL Freewheel] per l&#39;approvazione.

>[!PREREQUISITES]
>
>Rivolgiti al team dell&#39;account Adobe per assicurarti che l&#39;account [!DNL DSP] disponga dell&#39;autorizzazione per utilizzare il flusso di lavoro programmatico garantito di [!DNL FreeWheel].

1. Copia la chiave dell&#39;annuncio utilizzato con l&#39;offerta [!DNL Freewheel]:

   1. Fai clic sul nome della campagna.

   1. Nel sottomenu fare clic su **[!UICONTROL Ads]**.

   1. Fai clic su **[!UICONTROL ...]** > **[!UICONTROL Edit]** accanto al nome dell&#39;annuncio.

   1. Una volta aperte le impostazioni dell’annuncio, copia la chiave alfanumerica nell’URL visualizzato nella barra degli indirizzi del browser.

      Ad esempio, nell&#39;URL seguente, la chiave annuncio è `3NtNC5ZbaGZtqbei8jD3`

      ```
      https://advertising.adobe.com/configurator/ad/3NtNC5ZbaGZtqbei8jD3?referrer=/playtime/ads
      ```

1. Invia l&#39;annuncio a [!DNL Freewheel]:

   1. Effettuare una delle seguenti operazioni:

      * Accanto al nome dell&#39;annuncio, fare clic su **[!UICONTROL ...]** > **[!UICONTROL submit to FreeWheel]**.

      * Nel menu principale, fare clic su **[!UICONTROL Inventory]** > **[!UICONTROL Deals]**. Nella riga dell&#39;offerta fare clic su ![Menu Opzioni](/help/dsp/assets/options-menu.png) > **[!UICONTROL submit to FreeWheel]**.

   1. Verificare l&#39;ID offerta, immettere il **[!UICONTROL Ad Key]** copiato nel passaggio 1, quindi fare clic su **[!UICONTROL Submit]**.

   L’annuncio deve essere inviato e approvato prima di essere eseguito.

1. [Verifica lo stato di invio dell&#39;annuncio](freewheel-check-status.md).

>[!MORELIKETHIS]
>
>* [Panoramica sulla configurazione di offerte garantite a livello di programmazione in [!DNL Freewheel]](freewheel-overview.md)
>* [Accetta un&#39;offerta nella casella in entrata dell&#39;ID offerta](deal-id-inbox-accept.md)
>* [Verifica lo stato degli annunci per [!DNL FreeWheel] Offerte garantite a livello di programmazione](freewheel-check-status.md)
>* [Codici di errore per [!DNL Freewheel] Invii di annunci](freewheel-error-codes.md)
