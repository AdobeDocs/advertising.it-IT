---
title: Casi d’uso
description: Scopri i casi d’uso per la condivisione dei dati multimediali di Advertising DSP con Audience Manager
feature: Integration with Adobe Audience Manager
exl-id: 1d961799-b8be-499a-8db6-b59762d96bf1
source-git-commit: 7f35b3f3b33ed320ac186d219cbd0f826666bb3b
workflow-type: tm+mt
source-wordcount: '730'
ht-degree: 0%

---

# Casi d’uso per l’acquisizione dei dati sull’esposizione multimediale in Adobe Audience Manager

*Inserzionisti con solo Advertising DSP*

*Inserzionisti con una sola integrazione Adobe Advertising-Adobe Audience Manager*

Di seguito sono riportati alcuni modi in cui puoi trarre vantaggio dall&#39;acquisizione dei dati di esposizione multimediale di Advertising DSP <!-- ad impression data? --> in Audience Manager.

## Gestione di frequenza e attualità

L’acquisizione dei dati sulle impression in Audience Manager ti consente di migliorare la gestione della frequenza creando segmenti di utenti che sono stati esposti a un particolare annuncio o campagna. Puoi utilizzare questi segmenti per il targeting degli annunci se desideri aumentare la frequenza oppure per la soppressione degli annunci se desideri limitare la frequenza.

Inoltre, con l&#39;Audience Manager [!DNL Segment Builder], puoi applicare [controlli di recency e frequenza](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/segments/recency-and-frequency.html?lang=it) a qualsiasi [caratteristiche basate su regole](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/traits/trait-builder/create-onboarded-rule-based-traits.html?lang=it) che contiene segnali actionable. Ciò ti consente, ad esempio, di limitare il numero di volte in cui un utente riceve una particolare creatività all’interno di una campagna multimediale. Leggi &quot;[Eliminazione immediata tra dispositivi](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/profile-merge-rules/instant-cross-device-suppression.html?lang=it)&quot; per scoprire come eseguire questa operazione.<!-- The AM pulled this paragraph verbatim from AEM doc; I change only a word or two. -->

## Messaggistica sequenziale

Acquisendo i dati delle impression, puoi creare un segmento di utenti che sono stati esposti a una campagna o a un annuncio e utilizzare questo segmento per la messaggistica o l’eliminazione sequenziale. È possibile, ad esempio, eseguire il retargeting degli utenti che hanno visto il contenuto creativo `123` ma non hanno fatto clic né convertito mostrando loro il contenuto creativo `456`.

Per eseguire l&#39;Audience Manager seguente, eseguire la procedura seguente:<!-- The AM pulled this example/procedure verbatim from AEM doc; I changed only a word or two. -->

1. Crea una caratteristica per acquisire gli utenti che hanno visto la creatività.

   Ad esempio, per denominare la caratteristica `Creative Trait 123`, utilizza la seguente regola di caratteristica:

   ```
   d_creative == 123 AND d_event == imp
   ```

1. Crea una caratteristica per acquisire gli utenti che fanno clic o si convertono.

   Ad esempio, per denominare questa caratteristica `Click and Converter`, utilizza la seguente regola di caratteristica:

   ```
   d_event == click OR d_event=conv
   ```

1. Crea un segmento denominato `Retarget Users` da compilare con gli utenti che hanno visto il contenuto creativo `123` ma non hanno fatto clic o non hanno convertito. Utilizza la seguente regola di caratteristiche:

   ```
   Creative Trait 123 AND NOT Click and Converter
   ```

1. Mappare il segmento `Retarget Users` su una destinazione ed eseguire il targeting degli utenti nella destinazione con `456` creativo.

## [!DNL Adobe Audience Analytics] e dati esposizione campagna

Una volta che i dati di impression e clic della campagna sono disponibili in Audience Manager, puoi creare caratteristiche e segmenti di utenti che sono stati esposti a, o hanno interagito con, una determinata campagna o tattica. Con un&#39;integrazione [[!DNL Audience Analytics] integration](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html?lang=it), i segmenti di Audience Manager possono essere sincronizzati con [!DNL Analytics] per ulteriori analisi. I potenziali casi d’uso includono:

* **Analisi dell&#39;interazione tra DSP e [!DNL Advertising Search, Social, & Commerce] annunci:** L&#39;integrazione [[!DNL Analytics for Advertising] standard](/help/integrations/analytics/overview.md) non fornisce informazioni sull&#39;interazione tra DSP e [!DNL Search, Social, & Commerce] perché entrambi i canali utilizzano AMO ID che seguono le regole di attribuzione AMO ID, per cui un clic di ricerca sostituisce una visualizzazione view-through. Creando un segmento di esposizione DSP in Audience Manager, puoi utilizzare [!DNL Audience Analytics] per analizzare l&#39;interazione tra DSP e [!DNL Search, Social, & Commerce] annunci in [!DNL Analytics].

* **Analisi di frequenza:** Puoi creare segmenti in Audience Manager in base al numero di volte in cui un utente è stato esposto a un particolare annuncio o campagna. Puoi quindi analizzare i diversi segmenti di esposizione in Analytics per vedere come cambia il comportamento dell’utente in base al numero di esposizioni all’DSP.

## [!DNL Audience Optimization Reports]

Puoi sfruttare [l&#39;Audience Manager [!DNL Audience Optimization Reports]](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-reports.html?lang=it) per identificare potenziali opportunità di prestazioni per i segmenti nelle campagne. Questi rapporti combinano i dati di impression, clic e conversione di una campagna con le metriche del segmento per fornire ottimizzazioni incentrate sul segmento e un mix di canali efficace.

### Tipi di rapporti sugli Audienci Optimization rilevanti

| Report | Descrizione |
| ------ | ----------- |
| Report [[!UICONTROL Segment Performance]](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/segment-performance.html?lang=it) | Confronta i segmenti mappati e non mappati per impression e tassi di conversione. |
| [[!UICONTROL Trend Analysis and Volume Analysis] report]9https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/trend-analysis-volume-analysis.html) | Restituisci dati su impression, tassi di click-through e conversioni per una vasta gamma di dimensioni pubblicitarie. |
| Report [[!UICONTROL Optimal Frequency]](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/optimal-frequency.html?lang=it) | Consente di scoprire l’equilibrio ottimale tra il numero di impression e di conversioni servite. Consente di regolare il numero di impression da visualizzare prima di iniziare a vedere rendimenti in diminuzione. |
| Report [[!UICONTROL Unique User Reach]](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/unique-user-reach.html?lang=it) | Un grafico a bolle, in cui ogni bolla viene ridimensionata in proporzione diretta al numero di utenti univoci per la dimensione selezionata. |

### Considerazioni

* Se [!DNL Audience Optimization Reports] utenti dispongono di controlli di accesso basati sul ruolo (RBAC), [!DNL Adobe Customer Care] deve configurare un mapping tra l&#39;ID inserzionista e il codice di integrazione dell&#39;origine dati di Audience Manager dell&#39;organizzazione. Gli utenti amministratori possono quindi fornire i diritti RBAC a utenti diversi.

* Il reporting delle conversioni in [!DNL Audience Optimization Reports] richiede alcune impostazioni da parte dell&#39;utente finale. Gli utenti devono compilare i file di metadati.

* [!DNL Audience Optimization Reports] non supporta le modifiche ai metadati della campagna (ad esempio il nome della campagna o del posizionamento).

* I clic sugli annunci di ricerca sono inclusi in [!DNL Audience Optimization Reports] solo quando sono correlati alle impression. In altre parole, i clic di ricerca vengono trattati come conversioni successive alle impression. Di conseguenza, molti clic di ricerca potrebbero non essere inclusi in [!DNL Audience Optimization Reports].

>[!MORELIKETHIS]
>
>* [Panoramica sull&#39;invio di dati sull&#39;esposizione multimediale DSP a Adobe Audience Manager](overview.md)
>* [Raccogli dati di clic e impression dalle campagne Advertising DSP](collect.md)
