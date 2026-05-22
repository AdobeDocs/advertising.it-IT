---
title: Importa segmenti di prime parti da [!DNL AdFixus]
description: Scopri come importare  [!DNL AdFixus] segmenti di prime parti costituiti da [!DNL AdFixus] ID universali in DSP.
feature: DSP Audiences
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2:
  - id: fef5c122-6482-4d17-a8ce-4e70b906f1f4
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
source-git-commit: 79f0b3872a0d5d3765093ce83cc8f1c284a8255c
workflow-type: tm+mt
source-wordcount: 448
ht-degree: 0%

---

# Importa segmenti di prime parti da [!DNL AdFixus]

*Applicabile solo agli inserzionisti in Australia*

Utilizza l&#39;integrazione di Advertising DSP con [!DNL AdFixus] per importare gli ID universali [!DNL AdFixus] con mappature dei segmenti per pubblicità mirata. [!DNL AdFixus] Gli ID sono disponibili solo in Australia. DSP non modifica gli ID [!DNL AdFixus] in altri tipi di ID, né converte altri tipi di ID in ID [!DNL AdFixus]. DSP non addebita alcuna tariffa per l&#39;importazione degli ID.

Dopo aver importato i segmenti [!DNL AdFixus] in DSP, puoi indirizzare i posizionamenti agli ID [!DNL AdFixus] e a segmenti di prime parti specifici da [!DNL AdFixus]. Puoi anche aggiungere [!DNL AdFixus] segmenti a tipi di pubblico riutilizzabili. I dettagli di qualsiasi segmento includono il conteggio degli ID [!DNL AdFixus] applicabili.

Puoi visualizzare le impression, i clic, la frequenza e altre metriche per gli utenti con ID [!DNL AdFixus] nei rapporti personalizzati. Gli inserzionisti con [!DNL Analytics for Advertising] possono anche visualizzare i dati view-through per [!DNL AdFixus] ID da Adobe Analytics, nonché i dati da Adobe Analytics in DSP.

1. Utilizza [!DNL AdFixus] per convertire i dati di prime parti della tua organizzazione in segmenti con [!DNL AdFixus] ID.

   È necessario un account separato con [!DNL AdFixus] e una chiave di licenza attiva. Sarà inoltre necessario implementare il codice specifico di [!DNL AdFixus] per le proprietà e i domini del sito Web. Lavora direttamente con [!DNL AdFixus] per generare segmenti con ID.

1. (Inserzionisti con [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)) Configura il tracciamento per la misurazione [!DNL Analytics]:

   1. (Se non lo hai già fatto) Completa tutti i [prerequisiti per l&#39;implementazione [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) e l&#39;[AMO ID e EF ID negli URL di tracciamento](/help/integrations/analytics/ids.md).

   1. Distribuisci il codice specifico di [!DNL AdFixus] nelle tue pagine Web in modo che corrisponda alle conversioni dagli ID di [!DNL AdFixus] nei browser Web per desktop e dispositivi mobili (ma non nelle app mobili) alle view-through.

1. Importa i segmenti [!DNL AdFixus] di prime parti:

   1. [Crea un&#39;origine di pubblico](source-manage.md) di [!UICONTROL Type] **[!UICONTROL AdFixus ID]**. È necessario accettare i termini del contratto di assistenza.

      Le impostazioni di origine includono una chiave di origine generata automaticamente.

   1. Condividi la chiave di origine con il tuo team [!DNL AdFixus] in modo che possa inviare in streaming i segmenti richiesti a DSP.

1. Verifica nella sezione [!UICONTROL First Party Segments] della libreria del pubblico (disponibile quando crei o modifichi un pubblico da [!UICONTROL Audiences] > [!UICONTROL All Audiences] o all&#39;interno delle impostazioni di posizionamento) che il segmento sia popolato. Confrontare il numero di ID [!DNL AdFixus] con il numero di ID utente in [!DNL AdFixus].

   I segmenti sono disponibili in DSP non appena vengono creati.

I segmenti vengono aggiornati e sono disponibili per il targeting ogni tre ore, anche se il conteggio mostrato in DSP viene aggiornato ogni 24 ore. **Nota:** l&#39;inclusione in un segmento scade dopo un periodo di scadenza specificato, configurato in [!DNL AdFixus]. Aggiorna i segmenti inviandoli di nuovo da [!DNL AdFixus] prima della scadenza.

>[!MORELIKETHIS]
>
>* [Informazioni sulle origini del pubblico di prime parti](/help/dsp/audiences/sources/source-about.md)
>* [Gestisci origini pubblico per attivare il pubblico con ID universale](source-manage.md)
>* [Connessione Adobe Advertising DSP](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html?lang=it)
>* Adobe Experience Platform [Panoramica del catalogo delle destinazioni](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/overview.html?lang=it)
>* [Supporto per l&#39;attivazione degli ID universali](/help/dsp/audiences/universal-ids.md)
>* [Informazioni su Gestione dell&#39;audience](/help/dsp/audiences/audience-about.md)
