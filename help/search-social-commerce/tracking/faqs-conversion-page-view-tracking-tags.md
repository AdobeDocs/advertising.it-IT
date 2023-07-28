---
title: Domande frequenti sulla conversione degli Adobi Advertising e sui tag di tracciamento della visualizzazione della pagina
description: Vedi un confronto tra i tag di conversione Adobe Advertising e di tracciamento della visualizzazione della pagina.
exl-id: 5eb414a7-2f96-47de-b157-a17851653206
feature: Search Tracking
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '318'
ht-degree: 0%

---

# Domande frequenti sulla conversione degli Adobi Advertising e sui tag di tracciamento della visualizzazione della pagina

Di seguito sono riportati alcuni Adobi Advertising di tag di tracciamento della conversione e di tag di tracciamento della visualizzazione della pagina.

| | Tag JS con ECID | Tag JS versione 3 | Tag JS versione 2 | Tag immagine |
| ---- | ---- | ---- | ---- | ---- |
| Può essere utilizzato nella stessa pagina web di un’altra versione JS | — | — | — | n/d |
| Consente l’utilizzo di più tag con gli stessi ID utente inserzionista sulla stessa pagina web | Sì | Sì | Sì | — |
| Consente di utilizzare più tag con ID utente diversi per gli inserzionisti sulla stessa pagina Web | Sì | Sì | No | No |
| Utilizzato dall’estensione Adobi Advertising per Adobe Experience Platform e compatibile con altri tag generati utilizzando Experienci Platform | Sì | Sì | — | — |
| Consente tutte le conversioni provenienti da [!DNL Apple Safari] e [!DNL Mozilla Firefox] da tracciare se utilizzato con il tag di mappatura della conversione JavaScript Adobi Advertising | Sì | Sì | Sì | — |

<!-- add link to page on conversion mapping tag above? -->

>[!NOTE]
>
>* Tutte le nuove implementazioni utilizzano JavaScript versione 3.
>* Il tag JavaScript con ECID utilizza [Servizio Adobe Experience Cloud ID (ECID)](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html) nonché i precedenti ef_id e gsurferid per misurare le conversioni. Questo tag più recente crea [cookie s_ecid di Experience Cloud di prime parti](https://experienceleague.adobe.com/docs/core-services/interface/administration/ec-cookies/cookies-first-party.html) e offre una maggiore integrazione con altri prodotti di Experience Cloud.
>* Utilizza i tag JavaScript versione 2 solo quando sono già implementati nelle pagine web dell’inserzionista.
>* La best practice prevede l’utilizzo di tag JavaScript invece di tag immagine, a meno che il sito non disponga di criteri che ne impediscano l’utilizzo.
>* I tag JavaScript sono necessari per gli inserzionisti che desiderano eseguire il targeting dei tipi di pubblico creati in Adobe Experience Cloud, creati in Adobe Audience Manager o pubblicati in Adobe Experience Cloud da Audienci Manager o Adobe Analytics.

>[!MORELIKETHIS]
>
>* [Informazioni sui tag di tracciamento delle conversioni di Adobe Advertising](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [Genera un tag di conversione Adobe Advertising](/help/search-social-commerce/tools/conversion-tag-generate.md)
>* [Formato dei tag di tracciamento della conversione JavaScript versione 3](/help/search-social-commerce/tracking/format-conversion-tag-jsv3.md)
>* [Formato dei tag di tracciamento della conversione JavaScript versione 2](/help/search-social-commerce/tracking/format-conversion-tag-jsv2.md)
>* [Formato dei tag di tracciamento conversione immagine](/help/search-social-commerce/tracking/format-conversion-tag-image.md)

<!-- add if I keep the file:  
>* The Adobe Advertising JavaScript conversion mapping tag
-->
