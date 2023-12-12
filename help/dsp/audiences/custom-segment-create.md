---
title: Creare e implementare un segmento personalizzato
description: Scopri come creare e implementare un segmento personalizzato per tenere traccia degli utenti esposti agli annunci o degli utenti che visitano le tue pagine web.
feature: DSP Segments
exl-id: 3190fd78-18d2-4da3-920b-d4171e693c03
source-git-commit: 67b59f4f066d25f323620b83b5a0cb49beb3ee04
workflow-type: tm+mt
source-wordcount: '343'
ht-degree: 0%

---

# Creare e implementare un segmento personalizzato

Puoi raccogliere i tuoi dati sul pubblico di prime parti creando e implementando un segmento DSP personalizzato. Puoi utilizzare il segmento per monitorare a) gli utenti esposti agli annunci da desktop e dispositivi mobili e b) gli utenti che visitano specifiche pagine web. In seguito, puoi eseguire il retargeting degli utenti del segmento con annunci aggiuntivi o impedire agli utenti del segmento di ricevere annunci aggiuntivi.

>[!NOTE]
>
>Per tenere traccia degli ID degli utenti dalle richieste di rifiuto del consumatore sul sito web, in base al California Consumer Privacy Act (CCPA), crea un’ [Segmento di rinuncia CCPA](ccpa-opt-out-segment-create.md).

1. Crea il segmento:

   1. Nel menu principale, fai clic su **[!UICONTROL Audiences]** > **[!UICONTROL Segments]**.

   1. Sopra la tabella dati, fai clic su **[!UICONTROL Create]**.

   1. Inserisci un valore univoco **[!UICONTROL Segment Name]**.

   1. Per **[!UICONTROL Segment Type]**, seleziona *[!UICONTROL Custom]*.

   1. Inserisci il **[!UICONTROL Segment Window]**, che è il numero di giorni in cui il cookie di un utente rimane nel segmento.

      La finestra predefinita è di 45 giorni. Immettere un valore compreso tra uno (1) e 365.

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
