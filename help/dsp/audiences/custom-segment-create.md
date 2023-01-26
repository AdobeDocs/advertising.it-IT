---
title: Creare e implementare un segmento personalizzato
description: Scopri come creare e implementare un segmento personalizzato per tenere traccia degli utenti esposti agli annunci o agli utenti che visitano le tue pagine web.
feature: DSP Segments
exl-id: 691903e2-773e-4205-837e-822f435f57a7
source-git-commit: 1c13874967ec4ad264e5fa6a5e0dfeb6120f53cc
workflow-type: tm+mt
source-wordcount: '342'
ht-degree: 0%

---

# Creare e implementare un segmento personalizzato

Puoi raccogliere i tuoi dati di pubblico di prime parti creando e implementando un segmento di DSP personalizzato. Puoi utilizzare il segmento per tenere traccia di a) utenti esposti agli annunci da dispositivi desktop, mobili e CTV e b) utenti che visitano specifiche pagine web. In seguito puoi effettuare il retargeting degli utenti nel segmento con annunci aggiuntivi o impedire agli utenti nel segmento di ricevere annunci aggiuntivi.

>[!NOTE]
>
>Per tenere traccia degli ID degli utenti dalle richieste di rifiuto del consumatore sul tuo sito web, in base al California Consumer Privacy Act (CCPA), crea un [Segmento di rifiuto del CCPA](ccpa-opt-out-segment-create.md).

1. Crea il segmento:

   1. Nel menu principale, fai clic su **[!UICONTROL Audiences]>[!UICONTROL Segments]**.

   1. Sopra la tabella dati, fai clic su **[!UICONTROL Create]**.

   1. Immettere un valore univoco **[!UICONTROL Segment Name]**.

   1. Per **[!UICONTROL Segment Type]**, seleziona *[!UICONTROL Custom]*.

   1. Inserisci il **[!UICONTROL Segment Window]**, che è il numero di giorni in cui il cookie di un utente rimane nel segmento.

      La finestra predefinita è 45 giorni. Immettere un valore compreso tra 1 e 365.

   1. Clic **[!UICONTROL Save]**.

1. Copia e implementa i tag per tenere traccia del segmento, in base alle esigenze:

   1. Torna a **[!UICONTROL Audiences]>[!UICONTROL Segments]**.

   2. Posiziona il cursore sulla riga del segmento e fai clic su **[!UICONTROL Get Pixel]**.

      * Per tenere traccia dei visitatori desktop e mobili su una pagina web:

         1. Copia il tag di tracciamento della visualizzazione della pagina, che è etichettato &quot;[!UICONTROL Desktop or mobile websites].&quot;

         1. Fornisci il tag all’inserzionista o al contatto del sito web per la distribuzione.

            Il reparto IT dell&#39;inserzionista o un altro gruppo potrebbe dover pianificare o essere informato sulla distribuzione dei tag.
      * Per tenere traccia degli utenti esposti a un’unità pubblicitaria su dispositivi desktop, mobili o CTV:

         1. Copia il tag di tracciamento delle impression, che è etichettato &quot;[!UICONTROL Desktop or mobile ads].&quot;


1. Aggiungi il tag al [!UICONTROL Pixel] scheda per ogni annuncio rilevante o [!UICONTROL Event Pixels] della sezione [[!UICONTROL Tracking] impostazioni per ogni posizionamento pertinente](/help/dsp/campaign-management/placements/placement-settings.md#placement-tracking).

Una volta implementato un tag di tracciamento, puoi utilizzare il segmento nei target o nelle esclusioni del pubblico per qualsiasi posizionamento.

>[!TIP]
>
>Tieni traccia delle dimensioni del segmento quando gli utenti vengono tracciati.

>[!MORELIKETHIS]
>
>* [Informazioni sulla gestione dell&#39;audience](audience-about.md)
>* [Modifica informazioni segmento](segment-edit.md)
>* [Eliminare un segmento](segment-delete.md)
>* [Visualizzare i pixel di tracciamento per un segmento](segment-view-pixels.md)
>* [Condividere o interrompere la condivisione di un segmento](segment-share.md)
>* [Creare e implementare un [!UICONTROL CCPA Opt-Out-of-Sale] Segmento](ccpa-opt-out-segment-create.md)
>* [Creare un pubblico riutilizzabile](reusable-audience-create.md)
>* [Fornitori di dati di terze parti disponibili](third-party-data-providers.md)
>* [Impostazioni di posizionamento](/help/dsp/campaign-management/placements/placement-settings.md)

