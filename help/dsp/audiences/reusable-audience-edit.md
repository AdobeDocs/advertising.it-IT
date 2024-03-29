---
title: Modificare un pubblico riutilizzabile
description: Scopri come modificare un pubblico riutilizzabile.
feature: DSP Audiences
exl-id: 4de6b9a4-2907-474d-92bf-83686a1f0b31
source-git-commit: 443f8907644bf3e480626e14713e8abb9bfca284
workflow-type: tm+mt
source-wordcount: '421'
ht-degree: 0%

---

# Modificare un pubblico riutilizzabile

Quando modifichi un pubblico utilizzato in qualsiasi posizionamento o altro pubblico riutilizzabile, le modifiche vengono immediatamente applicate a tali posizionamenti e tipi di pubblico.<!-- verify -->

1. Nel menu principale, fai clic su **[!UICONTROL Audiences]** > **[!UICONTROL All audiences]**.

1. Posiziona il cursore sulla riga del pubblico e fai clic su **[!UICONTROL Edit]**.

1. Modifica le impostazioni del pubblico in uno dei seguenti modi:

   >[!NOTE]
   >
   >Se modifichi la logica del segmento di pubblico, vengono [dati sulle dimensioni del pubblico](audience-about.md) viene aggiornato nel pannello di destra.

   * (Facoltativo) Per modificare **[!UICONTROL Audience Name]** click ![Modifica](/help/dsp/assets/edit.png) accanto al nome del pubblico, inserisci un nome univoco per il pubblico, quindi fai clic su **[!UICONTROL Apply]**.

   * (Facoltativo) Per modificare manualmente la logica dei segmenti, utilizza i segmenti disponibili nel [[!UICONTROL Third Party Segments], [!UICONTROL First Party Segments], [!UICONTROL Adobe Segments], [!UICONTROL Custom Segments], e [!UICONTROL Saved Audiences] schede](audience-settings.md), eseguire le operazioni seguenti.

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





1. Clic **[!UICONTROL Save]**.

1. Nel messaggio di conferma, fai clic su **[!UICONTROL Continue]**.

>[!MORELIKETHIS]
>
>* [Informazioni su Gestione dell&#39;audience](audience-about.md)
>* [Creare un pubblico riutilizzabile](reusable-audience-create.md)
>* [Duplicare un pubblico riutilizzabile](reusable-audience-duplicate.md)
>* [Visualizzare dettagli su un pubblico riutilizzabile](reusable-audience-view-details.md)
>* [Condividere un pubblico riutilizzabile](reusable-audience-share.md)
>* [Esportare un pubblico riutilizzabile](reusable-audience-export.md)
>* [Copiare negli Appunti la chiave del segmento di un pubblico riutilizzabile](reusable-audience-clipboard.md)
>* [Eliminare un pubblico riutilizzabile](reusable-audience-delete.md)
>* [Impostazioni pubblico](audience-settings.md)
>* [Sintassi della logica dei segmenti di pubblico](audience-segment-logic-syntax.md)
>* [Provider di dati di terze parti disponibili](third-party-data-providers.md)

