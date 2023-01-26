---
title: Casi d'uso
description: Scopri i casi d’uso per condividere i dati multimediali DSP pubblicità con Audience Manager
feature: Integration with Adobe Audience Manager
exl-id: 1d961799-b8be-499a-8db6-b59762d96bf1
source-git-commit: 7e614ecb517515217d812926f61ca10437820efd
workflow-type: tm+mt
source-wordcount: '791'
ht-degree: 0%

---

# Casi d’uso per l’acquisizione di dati sull’esposizione dei contenuti multimediali in Adobe Audience Manager

*Advertising DSP solo*

*Inserzionisti con una sola integrazione Advertising-Adobe Audience Manager di Adobe*

Di seguito sono riportati alcuni modi in cui è possibile trarre vantaggio dall&#39;acquisizione dei dati di esposizione DSP media pubblicitari <!-- ad impression data? --> Audience Manager.

## Gestione di recency e frequenza

L’acquisizione dei dati sulle impression in Audience Manager consente di migliorare la gestione delle frequenze creando segmenti di utenti che sono stati esposti a un particolare annuncio o campagna. Puoi utilizzare questi segmenti per il targeting degli annunci se desideri aumentare la frequenza o per la soppressione degli annunci se desideri limitare la frequenza.

Inoltre, con Audience Manager [!DNL Segment Builder], puoi applicare [controlli di attualità e di frequenza](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/segments/recency-and-frequency.html) a qualsiasi [caratteristiche basate su regole](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/traits/trait-builder/create-onboarded-rule-based-traits.html) che contengono segnali actionable. Questo consente, ad esempio, di limitare il numero di volte in cui un utente riceve una particolare creatività all’interno di una campagna multimediale. Leggi &quot;[Soppressione immediata su diversi dispositivi](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/profile-merge-rules/instant-cross-device-suppression.html)&quot; per imparare come fare questo.<!-- The AM pulled this paragraph verbatim from AEM doc; I change only a word or two. -->

## Messaggistica sequenziale

Acquisendo i dati sulle impression, puoi creare un segmento di utenti esposti a una campagna o a un annuncio e utilizzare questo segmento per la messaggistica o la soppressione sequenziali. Ad esempio, puoi eseguire il retargeting degli utenti che hanno visualizzato contenuti creativi `123` ma non hanno fatto clic o convertito mostrando loro creativo `456`.

Per eseguire questo esempio in Audience Manager, segui questi passaggi:<!-- The AM pulled this example/procedure verbatim from AEM doc; I changed only a word or two. -->

1. Crea una caratteristica per catturare gli utenti che hanno visto il creativo.

   Ad esempio, per denominare la caratteristica `Creative Trait 123`, utilizza la seguente regola di caratteristiche:

   `d_creative == 123 AND d_event == imp`

1. Crea una caratteristica per acquisire gli utenti che fanno clic o convertono.

   Ad esempio, per denominare questa caratteristica `Click and Converter`, utilizza la seguente regola di caratteristiche:

   `d_event == click OR d_event=conv`

1. Creare un segmento denominato `Retarget Users` per popolarsi con gli utenti che hanno visto creativo `123` ma non ha fatto clic o convertito. Utilizza la seguente regola di caratteristiche:

   `Creative Trait 123 AND NOT Click and Converter`

1. Mappare il segmento `Retarget Users` a una destinazione e rivolgiti agli utenti della destinazione con elementi creativi `456`.

## [!DNL Adobe Audience Analytics] e i dati di esposizione alla campagna

Una volta disponibili, ad Audience Manager, le impression della campagna e i dati di clic, puoi creare caratteristiche e segmenti di utenti che sono stati esposti o con cui hanno interagito una determinata campagna o tattica. Con un [[!DNL Audience Analytics] integrazione](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html), i segmenti di Audience Manager possono essere sincronizzati con [!DNL Analytics] per ulteriori analisi. I casi d’uso potenziali includono:

* **Analisi di interazione tra DSP e [!DNL Adobe Advertising Search] annunci:** Lo standard [[!DNL Analytics for Advertising] integrazione](/help/integrations/analytics/overview.md) non fornisce informazioni approfondite sull&#39;interazione tra DSP e [!DNL [!DNL Search]] perché entrambi i canali utilizzano AMO ID che seguono le regole di attribuzione AMO ID, per le quali un clic di ricerca sostituisce una visualizzazione view-through. Creando un segmento di esposizione DSP in Audience Manager, puoi utilizzare [!DNL Audience Analytics] per analizzare l’interazione tra DSP e [!DNL] [!DNL Search]] annunci in [!DNL Analytics].

* **Analisi di frequenza:** Puoi creare segmenti in Audience Manager in base al numero di volte in cui un utente è stato esposto a un particolare annuncio o campagna. Puoi quindi analizzare i diversi segmenti di esposizione in Analytics per vedere come cambia il comportamento dell’utente a seconda del numero di esposizioni DSP.

## [!DNL Audience Optimization Reports]

Puoi sfruttare [Audience Manager [!DNL Audience Optimization Reports]](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-reports.html) per identificare potenziali opportunità di prestazioni per i segmenti nelle campagne. Questi rapporti combinano le impression della campagna, i dati di clic e conversione con le metriche dei segmenti per informare le ottimizzazioni incentrate sui segmenti e un efficace mix di canali.

### Tipi di rapporti Audience Optimization rilevanti

| Rapporto | Descrizione |
| ------ | ----------- |
| [[!UICONTROL Segment Performance] Rapporto](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/segment-performance.html) | Confronta segmenti mappati e non mappati per impression e tassi di conversione. |
| [[!UICONTROL Trend Analysis and Volume Analysis] Rapporti]9https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/trend-analysis-volume-analysis.html) | Restituisci dati su impression, tassi di click-through e conversioni per un’ampia gamma di dimensioni pubblicitarie. |
| [[!UICONTROL Optimal Frequency] Rapporto](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/optimal-frequency.html) | Consente di scoprire l’equilibrio ottimale tra il numero di impression e di conversioni servite. Consente di regolare il numero di impression da visualizzare prima di iniziare a vedere i ritorni decrescenti. |
| [[!UICONTROL Unique User Reach] Rapporto](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/unique-user-reach.html) | Grafico a bolle, in cui ogni bolla viene ridimensionata in proporzione diretta al numero di utenti univoci per la dimensione selezionata. |

### Considerazioni

* Se [!DNL Audience Optimization Reports] gli utenti dispongono di controlli di accesso basati sul ruolo (RBAC), quindi [!DNL Adobe Customer Care] deve configurare una mappatura tra l’ID inserzionista e il codice di integrazione dell’origine dati Audience Manager dell’organizzazione. Gli utenti amministratori possono quindi fornire diritti RBAC a utenti diversi.

* Rapporti di conversione in [!DNL Audience Optimization Reports] richiede una certa configurazione da parte dell&#39;utente finale. Gli utenti devono compilare i file di metadati.

* [!DNL Audience Optimization Reports] non supporta le modifiche ai metadati della campagna (ad esempio il nome della campagna o il nome del posizionamento).

* I clic sugli annunci di ricerca sono inclusi in [!DNL Audience Optimization Reports] solo quando sono correlate alle impression. In altre parole, i clic di ricerca vengono trattati come conversioni successive alle impression. Di conseguenza, molti clic di ricerca potrebbero non essere inclusi in [!DNL Audience Optimization Reports].

>[!MORELIKETHIS]
>
>* [Panoramica sull’invio DSP dati di esposizione a contenuti multimediali a Adobe Audience Manager](overview.md)
>* [Raccogliere dati di clic e impression da campagne pubblicitarie DSP](collect.md)

