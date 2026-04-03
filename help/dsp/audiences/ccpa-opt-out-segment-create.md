---
title: Creare e implementare un segmento di rifiuto del CCPA
description: Scopri come creare e implementare un segmento per tenere traccia degli ID degli utenti dalle richieste di rifiuto da parte dei consumatori.
feature: CCPA, DSP Segments
exl-id: 0623c52e-02ea-4e06-bc54-8abb7a87765a
TQID: https://experienceleague.adobe.com/NYXgnUkEw4uSilL8LO8qlRPp5AVAjXeXNS0pVeIZl3Y
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2:
  - id: c193c532-b70e-4556-bde7-857186cbe140
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 405
ht-degree: 0%

---

# Creare e implementare un segmento di rifiuto del CCPA

Puoi creare un segmento per tenere traccia degli ID degli utenti dalle richieste di rifiuto del consumatore sul tuo sito web, in base al California Consumer Privacy Act (CCPA). Gli utenti rimangono nei segmenti di rifiuto del CCPA per un tempo indefinito.

Una volta implementato il tag pixel del segmento, Adobe Advertising inizia a raccogliere un pool di ID per conto dell’inserzionista.

>[!NOTE]
>
>* Per informazioni su come comunicare le richieste di rifiuto del CCPA ad Adobe Advertising tramite l&#39;API Adobe Experience Platform Privacy Service, vedere [https://experienceleague.adobe.com/docs/advertising/privacy/ccpa/ccpa-opt-out-of-sale.html](https://experienceleague.adobe.com/docs/advertising/privacy/ccpa/ccpa-opt-out-of-sale.html).
>* Per tenere traccia degli utenti che visitano le pagine Web per scopi non correlati al tracciamento di eventi di rifiuto del CCPA, nonché degli utenti esposti agli annunci da dispositivi desktop, mobili e CTV, creare un [segmento personalizzato](/help/dsp/audiences/custom-segment-create.md).

1. Crea il segmento:

   1. Nel menu principale, fai clic su **Tipi di pubblico > Segmenti**.

   1. Sopra la tabella dati, fare clic su **[!UICONTROL Create]**.

   1. Immettere un **[!UICONTROL Segment Name]** univoco.

      Nome segmento consigliato: &quot;&lt;*Nome inserzionista*> - Rinuncia CCPA&quot; (ad esempio &quot;Acme - Rinuncia CCPA&quot;)

   1. Per [!UICONTROL Segment Type], selezionare **[!UICONTROL CCPA Opt-out of sale]**.

   1. Fare clic su **[!UICONTROL Save]**.

1. Copia e implementa un tag pixel per tenere traccia del segmento:

   1. Torna a **[!UICONTROL Audiences]** > **[!UICONTROL Segments]**.

   1. Nella riga del segmento, posizionare il cursore sul nuovo segmento e fare clic su **[!UICONTROL Get pixel]**.

   1. Copiare il pixel dell&#39;immagine (a partire da `<img src="https://rtd-tm.everesttech.net"`) per raccogliere gli ID utente dei visitatori del desktop e del dispositivo mobile in una pagina Web.

   1. Fornisci il tag all’inserzionista o al contatto del sito web per la distribuzione utilizzando il meccanismo utilizzato dall’azienda per tenere traccia delle richieste di rifiuto del CCPA (ad esempio, utilizzando una piattaforma di gestione dei consensi).

      Il reparto IT dell’inserzionista o un altro gruppo potrebbe dover pianificare la distribuzione dei tag o esserne informato.

      Una volta implementato il pixel, Adobe Advertising inizia a raccogliere un pool di ID per conto dell’inserzionista.

      Anche se la scelta e la logica di implementazione dipendono dall’inserzionista, ecco un esempio di come un inserzionista potrebbe attivare il pixel:

      1. Un consumatore arriva sulla homepage dell’inserzionista.
      1. Il consumatore trova e fa clic sul pulsante &quot;CCPA opt out of sale&quot; dell’inserzionista.
      1. Al consumatore viene presentato un elenco dei prestatori di servizi con cui l&#39;inserzionista lavora.
      1. Il consumatore seleziona la casella per rinunciare alla vendita di dati ad Adobe Advertising.

         Questa azione attiva il pixel per attivare e raccogliere l&#39;ID cookie del consumatore all&#39;interno del segmento &quot;[!UICONTROL CCPA Opt-out of sale]&quot; specificato.

>[!MORELIKETHIS]
>
>* [Supporto di Adobe Advertising per il California Consumer Privacy Act: supporto per la rinuncia del consumatore](/help/privacy/ccpa/ccpa-opt-out-of-sale.md)
>* [Informazioni su [!UICONTROL CCPA Opt-out-of-Sale] segmenti e report](ccpa-opt-out-about.md)
>* [Recupera report di rifiuto del consumatore](ccpa-opt-out-segment-report-retrieve.md)
>* [Creare e implementare un segmento personalizzato](custom-segment-create.md)
>* [Informazioni su Gestione dell&#39;audience](audience-about.md)
