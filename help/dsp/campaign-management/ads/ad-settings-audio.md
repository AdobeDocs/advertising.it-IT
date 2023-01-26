---
title: Impostazioni annuncio audio
description: Consulta le descrizioni delle impostazioni di annunci disponibili per gli annunci audio.
feature: DSP Ads
exl-id: 746b6f40-ff59-4bbe-bfc0-3579d4461e4a
source-git-commit: 1c13874967ec4ad264e5fa6a5e0dfeb6120f53cc
workflow-type: tm+mt
source-wordcount: '382'
ht-degree: 0%

---

# Impostazioni annuncio audio

## [!UICONTROL Insert Ad Tag]

*Solo nuovi annunci*

**[!UICONTROL URL]**: URL del tag VAST.

**[!UICONTROL Title]**: Un nome per il file, che verrà utilizzato nel [!UICONTROL Ads] visualizza e report.

>[!TIP]
>
> Per verificare la validità di un tag VAST, incollalo in un browser e premi il pulsante **[!UICONTROL Enter]** chiave. Se il tag è valido, verrà visualizzato un file XML che include `<VAST>` vicino alla cima.

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:** (Sola lettura) Il tipo di annuncio che stai creando, che corrisponde al tipo di posizionamento a cui l’annuncio può essere allegato. Per impostazione predefinita *[!UICONTROL Audio]*.

**[!UICONTROL Ad Name]:** Nome dell&#39;annuncio. Il titolo della risorsa viene utilizzato per impostazione predefinita, ma puoi modificarlo.

>[!TIP]
>
> Utilizza un nome che sarà facile trovare quando alleghi l’annuncio a un posizionamento, nella [!UICONTROL Ads] e nei rapporti. Ad esempio, descrivi il tipo di unità e alcuni attributi chiave (ad esempio, Anteprima del prodotto in vacanza): 30 sec Audio&quot;).

**[!UICONTROL Ad Duration]:** Lunghezza del file audio. Viene automaticamente impostato come [!UICONTROL 15] o [!UICONTROL 30], a seconda dell’unità pubblicitaria selezionata.

Questo campo può essere visualizzato o meno, a seconda delle autorizzazioni dell&#39;account.

**[!UICONTROL VAST Tag]:** (Annunci che utilizzano solo tag VAST) Un URL per una fonte di annunci di terze parti. Assicurati che il tag VAST includa solo file multimediali audio.

**[!UICONTROL Final VAST Tag]:** (Annunci che utilizzano solo tag VAST) L’URL per la fonte di annunci di terze parti con i necessari [Macro per il tracciamento DSP pubblicità](/help/dsp/campaign-management/macros.md) se del caso.

**[!UICONTROL Select Rate]:** (Solo utenti autorizzati) Un tasso pre-negoziato fatturato tramite Adobe, o uno dei tassi negoziati e per i quali verrà fatturato tramite il fornitore. Per aggiungere un tasso, contatta il tuo [!DNL Adobe] team di account.

### Pixel

Tutti i pixel di tracciamento degli eventi esistenti per il posizionamento vengono automaticamente collegati. Puoi scollegare i pixel esistenti e creare nuovi pixel in base alle tue esigenze di tracciamento per il singolo annuncio.

Le seguenti impostazioni si applicano a ogni pixel creato o modificato.

**[!UICONTROL Integration Event]:** L&#39;evento che attiva il pixel da attivare. Per questo tipo di annuncio, utilizza i pixel che attivano *[!UICONTROL Impression]* o *[!UICONTROL Click-through]*.

**[!UICONTROL Pixel Type]:** Se il pixel è un *[!UICONTROL IMG UR]L* (file immagine da 1 pixel), *[!UICONTROL HTML]* oppure *[!UICONTROL JavaScript URL]*.

**[!UICONTROL Pixel URL or Code]:** L&#39;URL dell&#39;immagine pixel, nel formato appropriato per il tipo di pixel specificato.

**[!UICONTROL Pixel Name]:** Nome del pixel. Utilizza un nome che ti aiuti a identificare facilmente il pixel.

**[!UICONTROL Pixel Provider]:** Provider di pixel: *[!UICONTROL None]*, *[!UICONTROL Nielsen]* oppure *[!UICONTROL Comscore]*.

>[!MORELIKETHIS]
>
>* [Informazioni sulla gestione degli annunci](ad-about.md)
>* [Creare un singolo annuncio](ad-create.md)
>* [Elencare i posizionamenti associati a un annuncio](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [Specifiche degli annunci](ad-specs.md)
>* [Macro DSP](/help/dsp/campaign-management/macros.md)

