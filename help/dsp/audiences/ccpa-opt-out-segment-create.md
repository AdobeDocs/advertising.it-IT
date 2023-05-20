---
title: Creare e implementare un segmento di rifiuto del CCPA
description: Scopri come creare e implementare un segmento per tenere traccia degli ID degli utenti dalle richieste di rifiuto da parte dei consumatori.
feature: CCPA, DSP Segments
exl-id: 0623c52e-02ea-4e06-bc54-8abb7a87765a
source-git-commit: 1a98b3ba7c37a768825e9e48db7d847f12daa9a0
workflow-type: tm+mt
source-wordcount: '417'
ht-degree: 0%

---

# Creare e implementare un segmento di rifiuto del CCPA

Puoi creare un segmento per tenere traccia degli ID degli utenti dalle richieste di rifiuto del consumatore sul tuo sito web, in base al California Consumer Privacy Act (CCPA). Gli utenti rimangono nei segmenti di rifiuto del CCPA per un tempo indefinito.

Una volta implementato il tag pixel del segmento, Adobe Advertising inizierà a raccogliere un pool di ID per conto dell’inserzionista.

>[!NOTE]
>
>* Per informazioni su come comunicare le richieste di rifiuto del CCPA ad Adobe Advertising tramite l’API Adobe Experience Platform Privacy Service, consulta [https://experienceleague.adobe.com/docs/advertising/privacy/ccpa/ccpa-opt-out-of-sale.html](https://experienceleague.adobe.com/docs/advertising/privacy/ccpa/ccpa-opt-out-of-sale.html).
>* Per tenere traccia degli utenti che visitano le pagine Web per scopi non correlati al tracciamento di eventi di rifiuto del CCPA, nonché degli utenti esposti agli annunci da dispositivi desktop, mobili e CTV, creare un [segmento personalizzato](/help/dsp/audiences/custom-segment-create.md).


1. Crea il segmento:

   1. Nel menu principale, fai clic su **Tipi di pubblico > Segmenti**.

   1. Sopra la tabella dati, fai clic su **[!UICONTROL Create]**.

   1. Inserisci un valore univoco **[!UICONTROL Segment Name]**.

      Nome segmento consigliato: &quot;&lt;*Nome inserzionista*> - Rinuncia CCPA&quot; (ad esempio &quot;Acme - Rinuncia CCPA&quot;)

   1. Per [!UICONTROL Segment Type], seleziona **[!UICONTROL CCPA Opt-out of sale]**.

   1. Clic **[!UICONTROL Save]**.

1. Copia e implementa un tag pixel per tenere traccia del segmento:

   1. Torna a **[!UICONTROL Audiences]** > **[!UICONTROL Segments]**.

   1. Nella riga del segmento, posiziona il cursore sul nuovo segmento e fai clic su **[!UICONTROL Get pixel]**.

   1. Copia il pixel dell&#39;immagine (iniziando con `<img src="https://rtd-tm.everesttech.net"`) per raccogliere gli ID utente dei visitatori desktop e mobili in una pagina web.

   1. Fornisci il tag all’inserzionista o al contatto del sito web per la distribuzione utilizzando il meccanismo utilizzato dall’azienda per tenere traccia delle richieste di rifiuto del CCPA (ad esempio, utilizzando una piattaforma di gestione dei consensi).

      Il reparto IT dell’inserzionista o un altro gruppo potrebbe dover pianificare la distribuzione dei tag o esserne informato.

      Una volta implementato il pixel, Adobe Advertising inizierà a raccogliere un pool di ID per conto dell’inserzionista.

      Anche se la scelta e la logica di implementazione dipendono dall’inserzionista, ecco un esempio di come un inserzionista potrebbe attivare il pixel:

      1. Un consumatore arriva sulla homepage dell’inserzionista.
      1. Il consumatore trova e fa clic sul pulsante &quot;CCPA opt out of sale&quot; dell’inserzionista.
      1. Al consumatore viene presentato un elenco dei prestatori di servizi con cui l&#39;inserzionista lavora.
      1. Il consumatore seleziona la casella per rinunciare alla vendita di dati ad Adobe Advertising.

         Questa azione attiva il pixel per attivare e raccogliere l’ID cookie del consumatore all’interno del specificato &quot;[!UICONTROL CCPA Opt-out of sale]&quot;.

>[!MORELIKETHIS]
>
>* [Adobe di supporto per la pubblicità per il California Consumer Privacy Act: supporto per la rinuncia del consumatore](/help/privacy/ccpa/ccpa-opt-out-of-sale.md)
>* [Informazioni su [!UICONTROL CCPA Opt-out-of-Sale] Segmenti e rapporti](ccpa-opt-out-about.md)
>* [Recuperare i rapporti sulla rinuncia del consumatore](ccpa-opt-out-segment-report-retrieve.md)
>* [Creare e implementare un segmento personalizzato](custom-segment-create.md)
>* [Informazioni su Gestione dell&#39;audience](audience-about.md)

