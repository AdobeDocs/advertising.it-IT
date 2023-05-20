---
title: Creare un [!UICONTROL Simple Ad Serving] Offerta
description: Scopri come creare un pixel di tracciamento per un [!UICONTROL Simple Ad Serving] affare.
feature: DSP Simple Ad Serving
exl-id: 77d5dabd-1a0d-4dce-8a9a-8d54a637e15d
source-git-commit: 443f8907644bf3e480626e14713e8abb9bfca284
workflow-type: tm+mt
source-wordcount: '386'
ht-degree: 0%

---

# Creare un [!UICONTROL Simple Ad Serving] Offerta

1. Nel menu principale, fai clic su **[!UICONTROL Inventory]** > **[!UICONTROL Deals].**

1. Sopra la tabella dati, fai clic su **[!UICONTROL Create]**, quindi selezionare **[!UICONTROL Simple Ad Serving]**.

1. Inserisci il [impostazioni di offerta](simple-deal-settings.md):

   1. In [!UICONTROL Select Ad Source] , specificare informazioni sull&#39;editore, l&#39;inserzionista e la campagna e il tipo di annuncio, quindi fare clic su **[!UICONTROL Next]**.

   1. In [!UICONTROL Select Ad(s)] , specifica un annuncio da utilizzare come proxy nell’DSP:

      1. Effettuare una delle seguenti operazioni:

         * Per gli annunci esistenti, seleziona gli annunci da utilizzare.

         * Per i nuovi annunci, crea un proxy [annuncio di terze parti](/help/dsp/campaign-management/ads/ad-create-multiple.md).
      >[!NOTE]
      > L’DSP non distribuisce gli annunci specificati. L’editore distribuisce l’annuncio.

      1. Clic **[!UICONTROL Next]**.
   1. In Dettagli feed, modifica i dettagli del feed, quindi fai clic su **[!UICONTROL Next]**.

      DSP genera automaticamente un posizionamento denominato &quot;SAS Placement - &lt;*nome offerta*>,&quot; per l’annuncio. Nel posizionamento, l’offerta viene automaticamente indirizzata nel [!UICONTROL Inventory Targets] sezione. Tutte le altre opzioni di targeting non sono applicabili.



1. Invia i pixel di tracciamento degli eventi all’editore per l’implementazione in uno dei seguenti modi:

   * (Facoltativo) Da [!UICONTROL Activate Tag with Publisher] , invia il tag dell&#39;offerta all&#39;editore.

      Al termine dei passaggi precedenti, DSP genera un messaggio e-mail che puoi inviare all’editore. Il messaggio include i dettagli dell’offerta, un collegamento da cui recuperare il tag dell’offerta e un codice di autorizzazione per il collegamento.

      1. Rivedi i dettagli dell’offerta, quindi effettua una delle seguenti operazioni:

         * Per incollare le informazioni in un messaggio e-mail in un’applicazione e-mail sul dispositivo, fai clic su **[!UICONTROL Email & Done]** e seleziona l’applicazione e-mail. Il [!UICONTROL CC:] il campo è precompilato con [!DNL Adobe] indirizzo di supporto. Puoi quindi inviare il messaggio al contatto appropriato per l’editore.

         * Per copiare le informazioni negli Appunti, fare clic su **[!UICONTROL Copy Email].** Puoi quindi incollare manualmente il contenuto in un messaggio e-mail e inviarlo al contatto appropriato per l’editore. Devi includere una copia (CC:) in `publisher-support-global@adobe.com`. Al termine della copia del messaggio, fai clic su **[!UICONTROL Email & Done]**.
      1. (Se necessario) Rivolgiti all’editore per verificare se il tag include le macro appropriate in modo che il tag funzioni con l’ad server dell’editore.
   * (Facoltativo) Invia manualmente i pixel di tracciamento degli eventi all’editore:

      1. Nella riga dell’offerta all’interno del [!UICONTROL Deals] visualizza, fai clic su ![Menu Opzioni](/help/dsp/assets/options-menu.png) **>[!UICONTROL show pixel]**.

         I pixel dell’evento includono [!UICONTROL Clickthrough] pixel e un [!UICONTROL Impression] pixel. Gli annunci video e audio includono anche pixel evento per quartile completato (da [!UICONTROL 25% Complete] a [!UICONTROL 100% Complete]).

      1. Copia i pixel di tracciamento degli eventi e forniscili al tuo editore.



>[!MORELIKETHIS]
>
>* [Informazioni su [!UICONTROL Simple Ad Serving]](simple-deal-about.md)
>* [[!UICONTROL Simple Ad Serving] Impostazioni](simple-deal-settings.md)
>* [Visualizzare un rapporto dettagliato per un&#39;offerta](/help/dsp/inventory/deal-view-report.md)


<!-- add back when reimplemented:
>* [View Event-Tracking Pixels for a [!UICONTROL Simple Ad Serving] Deal](simple-deal-show-pixels.md)
-->
