---
title: Crea un'offerta [!UICONTROL Simple Ad Serving]
description: Scopri come creare un pixel di tracciamento per un'offerta [!UICONTROL Simple Ad Serving].
feature: DSP Simple Ad Serving
exl-id: 77d5dabd-1a0d-4dce-8a9a-8d54a637e15d
source-git-commit: 443f8907644bf3e480626e14713e8abb9bfca284
workflow-type: tm+mt
source-wordcount: '386'
ht-degree: 0%

---

# Crea un&#39;offerta [!UICONTROL Simple Ad Serving]

1. Nel menu principale, fare clic su **[!UICONTROL Inventory]** > **[!UICONTROL Deals].**

1. Sopra la tabella dati, fare clic su **[!UICONTROL Create]**, quindi selezionare **[!UICONTROL Simple Ad Serving]**.

1. Immetti le [impostazioni di offerta](simple-deal-settings.md):

   1. Nella sezione [!UICONTROL Select Ad Source] specificare le informazioni relative all&#39;editore, all&#39;inserzionista e alla campagna e al tipo di annuncio, quindi fare clic su **[!UICONTROL Next]**.

   1. Nella sezione [!UICONTROL Select Ad(s)], specifica un annuncio da utilizzare come proxy in DSP:

      1. Effettuare una delle seguenti operazioni:

         * Per gli annunci esistenti, seleziona gli annunci da utilizzare.

         * Per i nuovi annunci, crea un proxy [annuncio di terze parti](/help/dsp/campaign-management/ads/ad-create-multiple.md).

      >[!NOTE]
      > L’DSP non distribuisce gli annunci specificati. L’editore distribuisce l’annuncio.

      1. Fare clic su **[!UICONTROL Next]**.

   1. In Dettagli feed, modificare i dettagli del feed, quindi fare clic su **[!UICONTROL Next]**.

      DSP genera automaticamente un posizionamento, denominato &quot;SAS Placement - &lt;*deal name*>&quot;, per l&#39;annuncio. Nel posizionamento, l&#39;offerta viene automaticamente indirizzata nella sezione [!UICONTROL Inventory Targets]. Tutte le altre opzioni di targeting non sono applicabili.

1. Invia i pixel di tracciamento degli eventi all’editore per l’implementazione in uno dei seguenti modi:

   * (Facoltativo) Dalla schermata [!UICONTROL Activate Tag with Publisher], invia il tag offerta all&#39;editore.

     Al termine dei passaggi precedenti, DSP genera un messaggio e-mail che puoi inviare all’editore. Il messaggio include i dettagli dell’offerta, un collegamento da cui recuperare il tag dell’offerta e un codice di autorizzazione per il collegamento.

      1. Rivedi i dettagli dell’offerta, quindi effettua una delle seguenti operazioni:

         * Per incollare le informazioni in un messaggio di posta elettronica in un&#39;applicazione di posta elettronica sul dispositivo, fare clic su **[!UICONTROL Email & Done]** e selezionare l&#39;applicazione di posta elettronica. Il campo [!UICONTROL CC:] è precompilato con un indirizzo di supporto [!DNL Adobe]. Puoi quindi inviare il messaggio al contatto appropriato per l’editore.

         * Per copiare le informazioni negli Appunti, fare clic su **[!UICONTROL Copy Email].** È quindi possibile incollare manualmente il contenuto in un messaggio di posta elettronica e inviarlo al contatto appropriato per l&#39;editore. È necessario includere una copia (CC:) in `publisher-support-global@adobe.com`. Al termine della copia del messaggio, fare clic su **[!UICONTROL Email & Done]**.

      1. (Se necessario) Rivolgiti all’editore per verificare se il tag include le macro appropriate in modo che il tag funzioni con l’ad server dell’editore.

   * (Facoltativo) Invia manualmente i pixel di tracciamento degli eventi all’editore:

      1. Nella riga dell&#39;offerta all&#39;interno della visualizzazione [!UICONTROL Deals], fare clic sul ![menu Opzioni](/help/dsp/assets/options-menu.png) **>[!UICONTROL show pixel]**.

         I pixel dell&#39;evento includono un pixel [!UICONTROL Clickthrough] e un pixel [!UICONTROL Impression]. Gli annunci video e audio includono anche pixel evento per quartile completato (da [!UICONTROL 25% Complete] a [!UICONTROL 100% Complete]).

      1. Copia i pixel di tracciamento degli eventi e forniscili al tuo editore.

>[!MORELIKETHIS]
>
>* [Informazioni su [!UICONTROL Simple Ad Serving]](simple-deal-about.md)
>* Impostazioni [[!UICONTROL Simple Ad Serving]](simple-deal-settings.md)
>* [Visualizza un report dettagliato per un&#39;offerta](/help/dsp/inventory/deal-view-report.md)

<!-- add back when reimplemented:
>* [View Event-Tracking Pixels for a [!UICONTROL Simple Ad Serving] Deal](simple-deal-show-pixels.md)
-->
