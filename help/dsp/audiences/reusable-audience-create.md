---
title: Creare un pubblico riutilizzabile
description: Scopri come creare un pubblico riutilizzabile costituito da segmenti di pubblico e altri tipi di pubblico salvati.
feature: DSP Audiences
exl-id: 5f4a0abb-c285-4452-a6c3-a91d5281df9b
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '485'
ht-degree: 0%

---

# Creare un pubblico riutilizzabile

<!-- "Saved audience" is used in UI (where?), but "saved" is a state, not a type. "Reusable audience" sounds better in a description. "Audience template" isn't right, either, since it implies you can edit it on the fly to create a new, different audience. Some other term? -->

Puoi salvare e gestire i tipi di pubblico riutilizzabili, ovvero gruppi di segmenti di pubblico e anche altri tipi di pubblico salvati, che puoi utilizzare come target o esclusioni per più posizionamenti.

1. Nel menu principale, fai clic su **[!UICONTROL Audiences]** > **[!UICONTROL All Audiences]**.

1. Sopra la tabella dati, fai clic su **[!UICONTROL Create]**.

1. Inserisci un valore univoco **[!UICONTROL Audience Name]**.

1. (Facoltativo) Deseleziona l’opzione per **[!UICONTROL Share with all advertisers in my account]**.

   Quando condividi un pubblico, questo diventa disponibile come target o come esclusione per tutti gli inserzionisti all’interno dell’account. Tuttavia, i singoli segmenti nel pubblico sono disponibili solo per gli utenti a cui i segmenti sono condivisi. Ad esempio, se condividi un pubblico contenente segmenti di Adobe Analytics con un inserzionista che non è mappato allo stesso [!DNL Analytics] , il segmento non viene visualizzato in anteprima nel pubblico per l’inserzionista in questione. Solo i segmenti disponibili per l’inserzionista vengono visualizzati in anteprima nel pubblico.

1. Clic **[!UICONTROL Save]**.

1. Creare il pubblico:

   >[!NOTE]
   >
   >Man mano che crei il pubblico, [dati sulle dimensioni del pubblico](audience-about.md) viene aggiornato nel pannello di destra

   * Per creare manualmente la logica del segmento, utilizza i segmenti disponibili nel [[!UICONTROL Third Party Segments], [!UICONTROL First Party Segments], [!UICONTROL Adobe Segments], [!UICONTROL Custom Segments], e [!UICONTROL Saved Audiences] schede](audience-settings.md), eseguire le operazioni seguenti.

      * Per aggiungere il primo segmento, individualo nel pannello a sinistra e seleziona la casella di controllo accanto al nome del segmento.

      * Per aggiungere un segmento a un gruppo di segmenti esistente:

         1. Fai clic sul gruppo di segmenti nel pannello di destra.

         1. (Facoltativo) Modifica la logica del gruppo in *[!UICONTROL Include Any]*, *[!UICONTROL Include All]*, o *[!UICONTROL Exclude All]*, in base alle esigenze.

            *[!UICONTROL Exclude All]* non è disponibile per il primo gruppo di segmenti. Per un pubblico che include solo esclusioni, crea questo pubblico come *[!UICONTROL Include Any]* e quindi, all’interno di un posizionamento, seleziona quel pubblico dal menu Tipi di pubblico esclusi.

         1. Individua il nuovo segmento nel pannello a sinistra e seleziona la casella di controllo accanto al nome del segmento.

            Il gruppo di segmenti viene aggiornato automaticamente con il nuovo segmento.

      * Per aggiungere un nuovo gruppo di segmenti:

         1. Clic **[!UICONTROL + New Group]** nel pannello a destra.

         1. (Facoltativo) Modifica la logica tra il gruppo precedente e quello nuovo in *[!UICONTROL And]* o *[!UICONTROL Or]*, in base alle esigenze.

         1. Individuate i segmenti per il nuovo gruppo nel pannello a sinistra e selezionate le caselle di controllo accanto ai nomi dei segmenti.

         1. (Facoltativo) Modifica la logica del gruppo in *[!UICONTROL Include Any]*, *[!UICONTROL Include All]*, o *[!UICONTROL Exclude All]*, in base alle esigenze.

   * Per utilizzare la logica dei segmenti da un pubblico esistente:

      1. Copia la logica del segmento dal pubblico esistente in uno dei seguenti modi:

         * Nella vista Tutti i tipi di pubblico, posiziona il cursore sulla riga del pubblico e fai clic su **[!UICONTROL More]** > **[!UICONTROL Copy to Clipboard]**.

         * Nelle impostazioni per il pubblico esistente, nella parte superiore del pannello logica del segmento, fai clic su **[!UICONTROL More]** > **[!UICONTROL Copy to Clipboard]**.

         * In un editor di testo, crea manualmente la logica del segmento utilizzando ID segmento alfanumerici e [Sintassi boolean](audience-segment-logic-syntax.md)e copiarlo negli Appunti.

      1. Clic **[!UICONTROL paste in an audience rule to begin building]**, incolla la logica del segmento esistente nel campo di input, quindi fai clic su **[!UICONTROL Apply]**.

         >[!NOTE]
         >
         >Se il pubblico include già una logica di segmento, l’operazione Incolla nella logica Nuovo segmento sovrascrive la logica esistente.

1. Clic **[!UICONTROL Create]**.

>[!MORELIKETHIS]
>
>* [Informazioni su Gestione dell&#39;audience](audience-about.md)
>* [Impostazioni pubblico](audience-settings.md)
>* [Sintassi della logica dei segmenti di pubblico](audience-segment-logic-syntax.md)
>* [Provider di dati di terze parti disponibili](third-party-data-providers.md)
>* [Creare e implementare un segmento personalizzato](custom-segment-create.md)
>* [Creare e implementare un [!UICONTROL CCPA Opt-Out-of-Sale] Segmento](ccpa-opt-out-segment-create.md)
>* [Impostazioni di posizionamento](/help/dsp/campaign-management/placements/placement-settings.md)
