---
title: Creare e implementare un segmento di rifiuto del CCPA
description: Scopri come creare e implementare un segmento per tenere traccia degli ID degli utenti dalle richieste di rinuncia del consumatore.
feature: CCPA, DSP Segments
exl-id: 0623c52e-02ea-4e06-bc54-8abb7a87765a
source-git-commit: 1a98b3ba7c37a768825e9e48db7d847f12daa9a0
workflow-type: tm+mt
source-wordcount: '417'
ht-degree: 0%

---

# Creare e implementare un segmento di rifiuto del CCPA

Puoi creare un segmento per tenere traccia degli ID degli utenti dalle richieste di rifiuto del consenso del consumatore sul tuo sito web, in base al California Consumer Privacy Act (CCPA). Gli utenti rimangono a tempo indefinito nei segmenti di rifiuto del CCPA.

Una volta implementato il tag pixel del segmento, Adobe Advertising inizierà a raccogliere un pool di ID per conto dell’inserzionista.

>[!NOTE]
>
>* Per informazioni su come comunicare le richieste di rifiuto del CCPA ad Adobe Advertising utilizzando l’API Adobe Experience Platform Privacy Service, vedi [https://experienceleague.adobe.com/docs/advertising/privacy/ccpa/ccpa-opt-out-of-sale.html](https://experienceleague.adobe.com/docs/advertising/privacy/ccpa/ccpa-opt-out-of-sale.html).
>* Per tenere traccia degli utenti che visitano le pagine web per scopi non correlati al tracciamento degli eventi di rifiuto del CCPA, nonché degli utenti esposti agli annunci da dispositivi desktop, mobili e CTV, crea un [segmento personalizzato](/help/dsp/audiences/custom-segment-create.md).


1. Crea il segmento:

   1. Nel menu principale, fai clic su **Tipi di pubblico > Segmenti**.

   1. Sopra la tabella dati, fai clic su **[!UICONTROL Create]**.

   1. Immettere un valore univoco **[!UICONTROL Segment Name]**.

      Nome del segmento consigliato: &quot;&lt;*Nome inserzionista*> - Rinuncia CCPA per la vendita (ad esempio &quot;Acme - CCPA Opt Out of Sale&quot;)

   1. Per [!UICONTROL Segment Type], seleziona **[!UICONTROL CCPA Opt-out of sale]**.

   1. Clic **[!UICONTROL Save]**.

1. Copia e implementa un tag pixel per tracciare il segmento:

   1. Torna a **[!UICONTROL Audiences]** > **[!UICONTROL Segments]**.

   1. Nella riga del segmento, tieni premuto il cursore sul nuovo segmento e fai clic su **[!UICONTROL Get pixel]**.

   1. Copia il pixel dell’immagine (a partire da `<img src="https://rtd-tm.everesttech.net"`) per raccogliere gli ID utente dei visitatori desktop e mobili in una pagina web.

   1. Fornisci il tag all’inserzionista o al contatto del sito web per la distribuzione utilizzando il meccanismo utilizzato dall’azienda per monitorare le richieste di rifiuto del CCPA (ad esempio utilizzando una piattaforma di gestione del consenso).

      Il reparto IT dell&#39;inserzionista o un altro gruppo potrebbe dover pianificare o essere informato sulla distribuzione dei tag.

      Una volta implementato il pixel, Adobe Advertising inizierà a raccogliere un pool di ID per conto dell’inserzionista.

      Anche se la scelta e la logica di implementazione dipendono dall’inserzionista, ecco un esempio di come un inserzionista potrebbe attivare il pixel:

      1. Un consumatore arriva sulla homepage dell&#39;inserzionista.
      1. Il consumatore trova e clicca sul pulsante &quot;CCPA opt out of sale&quot; dell’inserzionista.
      1. Al consumatore viene presentato un elenco di fornitori di servizi con i quali lavora l&#39;inserzionista.
      1. Il consumatore seleziona la casella per rinunciare alla vendita di dati ad Adobe Advertising.

         Questa azione attiva il pixel da attivare e per raccogliere l’ID cookie del consumatore all’interno del &quot;[!UICONTROL CCPA Opt-out of sale]&quot; segmento.

>[!MORELIKETHIS]
>
>* [Adobe di supporto per la pubblicità per il California Consumer Privacy Act: Supporto per rinuncia del consumatore](/help/privacy/ccpa/ccpa-opt-out-of-sale.md)
>* [Informazioni [!UICONTROL CCPA Opt-out-of-Sale] Segmenti e rapporti](ccpa-opt-out-about.md)
>* [Recuperare i rapporti di rinuncia del consumatore](ccpa-opt-out-segment-report-retrieve.md)
>* [Creare e implementare un segmento personalizzato](custom-segment-create.md)
>* [Informazioni sulla gestione dell&#39;audience](audience-about.md)

