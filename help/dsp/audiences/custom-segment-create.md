---
title: Creare e implementare un segmento personalizzato
description: Scopri come creare e implementare un segmento personalizzato per tenere traccia degli utenti esposti agli annunci o degli utenti che visitano le tue pagine web.
feature: DSP Segments
exl-id: 3190fd78-18d2-4da3-920b-d4171e693c03
source-git-commit: fcce2b2ba7ab9717e83b05ddf8f22399f6b2e28e
workflow-type: tm+mt
source-wordcount: '651'
ht-degree: 0%

---

# Creare e implementare un segmento personalizzato

Puoi raccogliere i tuoi dati sul pubblico di prime parti creando e implementando un segmento DSP personalizzato. Puoi utilizzare il segmento per monitorare a) gli utenti esposti agli annunci da desktop e dispositivi mobili e b) gli utenti che visitano specifiche pagine web. In seguito, puoi eseguire il retargeting degli utenti del segmento con annunci aggiuntivi o impedire agli utenti del segmento di ricevere annunci aggiuntivi.

>[!NOTE]
>
>Per tenere traccia degli ID degli utenti dalle richieste di rifiuto del consumatore sul sito web, in base al California Consumer Privacy Act (CCPA), crea un’ [Segmento di rinuncia CCPA](ccpa-opt-out-segment-create.md).

## Prerequisiti per i segmenti per tenere traccia degli ID ID5

*Funzione beta*

* Prima di generare un segmento per tenere traccia degli utenti associati agli ID5, devi firmare un accordo con [!DNL ID5] e ottieni l’ID partner della tua organizzazione. Per istruzioni, contatta il team del tuo account di Adobe.

* Per la misurazione in Adobe Analytics, è necessario:

   1. Completa tutto [prerequisiti per l&#39;implementazione [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) e [AMO ID e EF ID negli URL di tracciamento](/help/integrations/analytics/ids.md).

   1. Aggiungi il seguente parametro alle tue pagine web prima o all’interno del [Codice JavaScript richiesto per [!DNL Analytics for Advertising]](/help/integrations/analytics/javascript.md) — in un punto qualsiasi prima dell&#39;inizializzazione dell&#39;ultimo servizio eventi.

      ```window.id5PartnerId=Your_ID5_PartnerID;```

      Esempio:

      ```
      <script src="https://www.everestjs.net/static/le/last-event-tag-latest.min.js">
      <script>
        window.id5PartnerId=Your_ID5_PartnerID;
             if("undefined" != typeof AdCloudEvent)
                 AdCloudEvent('IMS ORG Id','rsid');
      </script>
      ```

## Creare e implementare un segmento personalizzato

1. Crea il segmento:

   1. Nel menu principale, fai clic su **[!UICONTROL Audiences]** > **[!UICONTROL Segments]**.

   1. Sopra la tabella dati, fai clic su **[!UICONTROL Create]**.

   1. Inserisci un valore univoco **[!UICONTROL Segment Name]**.

   1. Per **[!UICONTROL Segment Type]**, seleziona *[!UICONTROL Custom]*.

   1. Inserisci il **[!UICONTROL Lookback Window]**, che è il numero di giorni in cui il cookie di un utente rimane nel segmento.

      La finestra predefinita è di 45 giorni. Immettere un valore compreso tra uno (1) e 365.

   1. Clic **[!UICONTROL Advanced]** per espandere le impostazioni avanzate e quindi selezionare i tipi di identificatori utente di cui il tag segmento terrà traccia:

      * *[!UICONTROL Cookies]:* (Impostazione predefinita) Il tag del segmento tiene traccia dei cookie.

      * [!UICONTROL Universal IDs (Beta)]:

         * *[!UICONTROL ID5]:* Il tag del segmento verrà tracciato [!DNL ID5] ID. Non viene applicata alcuna tariffa per le impression consegnate agli ID universali.

        **[!UICONTROL Terms of Service]:** I termini del contratto di servizio per l&#39;utilizzo degli ID universali. Prima di poter utilizzare gli ID universali per un nuovo tipo di ID, è necessario che tu o un altro utente con l’account DSP accetti una volta i termini. Per i clienti con contratti di assistenza gestiti, il team dell’account Adobe otterrà il consenso e accetterà i termini per conto della tua organizzazione. Per leggere i termini, fai clic su **>**. Per accettare i termini, scorri fino alla parte inferiore dei termini e fai clic su **[!UICONTROL Accept]**.

   1. Clic **[!UICONTROL Save]**.

1. Copia e implementa i tag per tenere traccia del segmento, in base alle esigenze:

   1. Torna a **[!UICONTROL Audiences]** > **[!UICONTROL Segments]**.

   1. Tenere premuto il cursore sulla riga del segmento e fare clic su **[!UICONTROL Get Pixel]**.

      * Per tenere traccia dei visitatori desktop e mobili in una pagina Web:

         1. Copia il tag di tracciamento della visualizzazione della pagina, che è etichettato &quot;[!UICONTROL Desktop or mobile websites].&quot;

         1. Fornisci il tag all’inserzionista o al contatto del sito web per la distribuzione.

            Il reparto IT dell’inserzionista o un altro gruppo potrebbe dover pianificare la distribuzione dei tag o esserne informato.

      * Per tenere traccia degli utenti esposti a un’unità pubblicitaria su dispositivi desktop o mobili:

         1. Copia il tag di tracciamento delle impression, etichettato come &quot;[!UICONTROL Desktop or mobile ads].&quot;

   1. (Tag per i segmenti che tengono traccia di [!DNL ID5] ID per i visitatori desktop e mobili di una pagina web) Nel tag copiato, sostituisci `ID5_PARTNER_ID` con l’ID partner che [!DNL ID5] assegnati alla tua organizzazione.

   Ad esempio, se l’ID partner ID5 è `abcde` e il tag del segmento generato è

   ```<script src="https://playtime.tubemogul.com/ud/prod/universal_ids/segment.js?sid=012345&id5pid=ID5_PARTNER_ID"></script><img src="https://rtd-tm.everesttech.net/upi/?sid=012345&cs=1" />```

   quindi sostituisci `ID5_PARTNER_ID` con `abcde` all’interno del tag per ottenere quanto segue:

   ```<script src="https://playtime.tubemogul.com/ud/prod/universal_ids/segment.js?sid=012345&id5pid=abcde"></script><img src="https://rtd-tm.everesttech.net/upi/?sid=012345&cs=1" />```

   L&#39;organizzazione ha ricevuto l&#39;ID partner quando ha firmato un accordo con [!DNL ID5]. Se non conosci il tuo ID partner, contatta il team del tuo account Adobe.

   Questo passaggio non è necessario per tenere traccia dei tag [!DNL ID5] ID per gli utenti esposti a un’unità pubblicitaria su dispositivi desktop o mobili.

1. Aggiungi il tag al [!UICONTROL Pixel] per ogni annuncio pertinente o per [!UICONTROL Event Pixels] sezione del [[!UICONTROL Tracking] impostazioni per ogni posizionamento pertinente](/help/dsp/campaign-management/placements/placement-settings.md#placement-tracking).

Una volta implementato un tag di tracciamento, puoi utilizzare il segmento nei target o nelle esclusioni del pubblico per qualsiasi posizionamento.

>[!TIP]
>
>Tieni traccia delle dimensioni del segmento durante la registrazione degli utenti.

>[!MORELIKETHIS]
>
>* [Informazioni su Gestione dell&#39;audience](audience-about.md)
>* [Modifica informazioni segmento](segment-edit.md)
>* [Eliminare un segmento](segment-delete.md)
>* [Visualizzare i pixel di tracciamento per un segmento](segment-view-pixels.md)
>* [Condividere o interrompere la condivisione di un segmento](segment-share.md)
>* [Creare e implementare un [!UICONTROL CCPA Opt-Out-of-Sale] Segmento](ccpa-opt-out-segment-create.md)
>* [Creare un pubblico riutilizzabile](reusable-audience-create.md)
>* [Provider di dati di terze parti disponibili](third-party-data-providers.md)
>* [Impostazioni di posizionamento](/help/dsp/campaign-management/placements/placement-settings.md)
