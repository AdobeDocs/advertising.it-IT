---
title: Gestire i modelli di feed
description: Scopri come gestire i modelli di feed.
feature: Creative Dynamic Creatives
source-git-commit: 0d7a7ab23173a061961c4b5c66ace5b69a746e86
workflow-type: tm+mt
source-wordcount: '404'
ht-degree: 0%

---

# Gestire i modelli di feed

<!-- I have a "Retail" feed template that was created by rkarthik@adobe. Ask product if this is available to all clients or just internal.  -->

<!-- We have a finite set of supported fields on the backend. I need to include that info in an appendix. -->

I modelli di feed associano i campi nei file di feed o nei cataloghi con i campi nel backend di Advertising Creative. Gli annunci HTML5 dinamici, ma non gli annunci HTML5 statici, richiedono un modello di feed per creare annunci dinamici.

Puoi utilizzare un modello di feed con più modelli di annunci.

## Creare un modello di feed

1. Nel menu principale, fare clic su **[!UICONTROL Creative]** > **[!UICONTROL Feeds]**.

1. Fare clic sulla scheda **[!UICONTROL Templates]**.

1. In alto a destra, fare clic su **[!UICONTROL Create]** > **[!UICONTROL Template]**.

1. Specificare le [impostazioni del modello di feed](#feed-template-settings).

1. Fare clic su **[!UICONTROL Save]**.

## Modificare un modello di feed

**Nota:** è possibile modificare solo i modelli di feed creati.

1. Nel menu principale, fare clic su **[!UICONTROL Creative]** > **[!UICONTROL Feeds]**.

1. Fare clic sulla scheda **[!UICONTROL Templates]**.

1. Posizionare il cursore sulla riga del modello e fare clic su **[!UICONTROL Duplicate]**.

1. Modifica le [impostazioni del modello di feed](#feed-template-settings) in base alle esigenze.

1. Fare clic su **[!UICONTROL Save]**.

## Visualizzare un modello di feed

1. Nel menu principale, fare clic su **[!UICONTROL Creative]** > **[!UICONTROL Feeds]**.

1. Fare clic sulla scheda **[!UICONTROL Templates]**.

1. Posizionare il cursore sulla riga del modello e fare clic su **[!UICONTROL View]**.

## Duplicare un modello di feed

1. Nel menu principale, fare clic su **[!UICONTROL Creative]** > **[!UICONTROL Feeds]**.

1. Fare clic sulla scheda **[!UICONTROL Templates]**.

1. Posizionare il cursore sulla riga del modello e fare clic su **[!UICONTROL Duplicate]**.

1. Nella schermata [!UICONTROL Duplicate Template], immettere un **[!UICONTROL Template Name]** univoco. Se stai duplicando un modello creato da un altro utente, seleziona **[!UICONTROL Advertiser]**. Se necessario, modifica altre [impostazioni del modello di feed](#feed-template-settings).

1. Fare clic su **[!UICONTROL Save]**.

## Scaricare un modello di feed

I modelli di feed scaricati sono in formato foglio di calcolo Microsoft Excel (XLSX) compresso.

1. Nel menu principale, fare clic su **[!UICONTROL Creative]** > **[!UICONTROL Feeds]**.

1. Fare clic sulla scheda **[!UICONTROL Templates]**.

1. Posizionare il cursore sulla riga del modello e fare clic su **[!UICONTROL Download]**.

   Il file viene scaricato in base alla normale procedura del browser.

## Impostazioni del modello di feed {#feed-template-settings}

### [!UICONTROL General] impostazioni

**[!UICONTROL Template Name]:** Nome di modello univoco per l&#39;inserzionista specificato.

**[!UICONTROL Advertiser]:** Inserzionista che può utilizzare il modello.

**[!UICONTROL Description]:** (facoltativo) informazioni utili per chiunque utilizzi il modello di feed.

### [!UICONTROL Field Mapping] impostazioni

Mappa ciascun campo nel file di feed su un campo nel backend di Advertising Creative. Per un elenco dei campi back-end e dei relativi attributi obbligatori, vedere &quot;[Campi disponibili per i file di feed di annunci dinamici](/help/creative/appendix-available-feed-fields.md)&quot;.<!-- Check w/product: What is displayed where in the UI/reports and published ads? -->

Almeno un campo del file di feed deve essere contrassegnato come &quot;[!UICONTROL Is Unique]&quot;. Per aggiungere un mapping di campi, fare clic su **[!UICONTROL +]**. Per rimuovere l&#39;ultimo mapping di campi, fare clic su **[!UICONTROL +]**.

**[!UICONTROL Field Name]:** Il campo nel file di feed.

**[!UICONTROL Description]:** (facoltativo) informazioni utili per chiunque utilizzi il modello di feed.

**[!UICONTROL Is Unique]:** indica che il campo è un ID univoco (chiave). Almeno un campo per modello di feed deve essere univoco. Per selezionare questa opzione, fare clic sul pulsante per spostarla a destra.<!-- **Note: The unique identifier is different from the feed "trigger" in experience settings. -->

**[!UICONTROL Backend Field]:** Il campo [&#x200B; nel backend di Advertising Creative](/help/creative/appendix-available-feed-fields.md) mappato a [!UICONTROL Field Name] specificato nel file di feed.

>[!MORELIKETHIS]
>
>* [Flussi di lavoro per annunci dinamici](/help/creative/introduction/workflow-dynamic-ads.md)
>* [Gestione file risorse](/help/creative/feeds/asset-manage.md)
>* [Gestisci cataloghi](/help/creative/feeds/catalog-manage.md)
>* [Monitora lo stato dei processi di elaborazione catalogo](/help/creative/feeds/job-status-track.md)
>* [Gestisci modelli di annunci dinamici](/help/creative/ad-templates/ad-template-manage.md)
>* [Aggiungere elementi creativi dinamici a una libreria creativa](/help/creative/creative-libraries/creative-add-dynamic.md)
