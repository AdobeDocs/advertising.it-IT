---
title: Casi d’uso
description: Scopri i casi d’uso per condividere i dati multimediali dell’DSP di Advertising con Audience Manager
feature: Integration with Adobe Audience Manager
exl-id: 1d961799-b8be-499a-8db6-b59762d96bf1
source-git-commit: 7f35b3f3b33ed320ac186d219cbd0f826666bb3b
workflow-type: tm+mt
source-wordcount: '789'
ht-degree: 0%

---

# Casi d’uso per l’acquisizione dei dati sull’esposizione multimediale in Adobe Audience Manager

*Inserzionisti solo con Advertising DSP*

*Inserzionisti con un Adobe di integrazione Advertising-Adobe Audience Manager Only*

Di seguito sono riportati alcuni modi in cui puoi trarre vantaggio dall’acquisizione dei dati di esposizione multimediale di Advertising DSP <!-- ad impression data? --> in Audience Manager.

## Gestione di frequenza e attualità

L’acquisizione dei dati sulle impression in Audience Manager ti consente di migliorare la gestione della frequenza creando segmenti di utenti che sono stati esposti a un particolare annuncio o campagna. Puoi utilizzare questi segmenti per il targeting degli annunci se desideri aumentare la frequenza oppure per la soppressione degli annunci se desideri limitare la frequenza.

Inoltre, con Audience Manager [!DNL Segment Builder], puoi applicare [controlli di attualità e frequenza](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/segments/recency-and-frequency.html) a qualsiasi [caratteristiche basate su regole](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/traits/trait-builder/create-onboarded-rule-based-traits.html) che contengono segnali utilizzabili. Ciò ti consente, ad esempio, di limitare il numero di volte in cui un utente riceve una particolare creatività all’interno di una campagna multimediale. Leggi &quot;[Soppressione immediata su diversi dispositivi](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/profile-merge-rules/instant-cross-device-suppression.html)&quot; per scoprire come eseguire questa operazione.<!-- The AM pulled this paragraph verbatim from AEM doc; I change only a word or two. -->

## Messaggistica sequenziale

Acquisendo i dati delle impression, puoi creare un segmento di utenti che sono stati esposti a una campagna o a un annuncio e utilizzare questo segmento per la messaggistica o l’eliminazione sequenziale. Ad esempio, puoi eseguire il retargeting degli utenti che hanno visto contenuti creativi `123` ma non ha fatto clic o convertito mostrando loro la creatività `456`.

Per eseguire questo Audience Manager in, segui questi passaggi:<!-- The AM pulled this example/procedure verbatim from AEM doc; I changed only a word or two. -->

1. Crea una caratteristica per acquisire gli utenti che hanno visto la creatività.

   Ad esempio, per denominare la caratteristica `Creative Trait 123`, utilizza la seguente regola di caratteristiche:

   ```
   d_creative == 123 AND d_event == imp
   ```

1. Crea una caratteristica per acquisire gli utenti che fanno clic o si convertono.

   Ad esempio, per denominare questa caratteristica `Click and Converter`, utilizza la seguente regola di caratteristiche:

   ```
   d_event == click OR d_event=conv
   ```

1. Crea un segmento denominato `Retarget Users` per popolare con gli utenti che hanno visto creativo `123` ma non ha fatto clic o convertito. Utilizza la seguente regola di caratteristiche:

   ```
   Creative Trait 123 AND NOT Click and Converter
   ```

1. Mappare il segmento `Retarget Users` a una destinazione e rivolgiti agli utenti nella destinazione con creativi `456`.

## [!DNL Adobe Audience Analytics] e i dati di esposizione alla campagna

Una volta che i dati di impression e clic della campagna sono disponibili in Audience Manager, puoi creare caratteristiche e segmenti di utenti che sono stati esposti a, o hanno interagito con, una determinata campagna o tattica. Con un [[!DNL Audience Analytics] integrazione](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html), i segmenti di Audience Manager possono essere sincronizzati con [!DNL Analytics] per ulteriori analisi. I potenziali casi d’uso includono:

* **Analisi dell’interazione tra DSP e [!DNL Advertising Search, Social, & Commerce] annunci:** Lo standard [[!DNL Analytics for Advertising] integrazione](/help/integrations/analytics/overview.md) non fornisce informazioni sull’interazione tra DSP e [!DNL Search, Social, & Commerce] perché entrambi i canali utilizzano AMO ID che seguono le regole di attribuzione AMO ID, per cui un clic di ricerca sostituisce una visualizzazione view-through. Creando un segmento di esposizione dell’DSP in Audience Manager, puoi utilizzare [!DNL Audience Analytics] analizzare l’interazione tra DSP e [!DNL Search, Social, & Commerce] annunci in [!DNL Analytics].

* **Analisi della frequenza:** Puoi creare segmenti in Audience Manager in base al numero di volte in cui un utente è stato esposto a un particolare annuncio o campagna. Puoi quindi analizzare i diversi segmenti di esposizione in Analytics per vedere come cambia il comportamento dell’utente in base al numero di esposizioni all’DSP.

## [!DNL Audience Optimization Reports]

Puoi sfruttare [Audience Manager [!DNL Audience Optimization Reports]](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-reports.html) identificare potenziali opportunità di prestazioni per segmenti nelle campagne. Questi rapporti combinano i dati di impression, clic e conversione di una campagna con le metriche del segmento per fornire ottimizzazioni incentrate sul segmento e un mix di canali efficace.

### Tipi di rapporti sugli Audienci Optimization rilevanti

| Report | Descrizione |
| ------ | ----------- |
| [[!UICONTROL Segment Performance] Report](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/segment-performance.html) | Confronta i segmenti mappati e non mappati per impression e tassi di conversione. |
| [[!UICONTROL Trend Analysis and Volume Analysis] Report]9https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/trend-analysis-volume-analysis.html) | Restituisci dati su impression, tassi di click-through e conversioni per una vasta gamma di dimensioni pubblicitarie. |
| [[!UICONTROL Optimal Frequency] Report](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/optimal-frequency.html) | Consente di scoprire l’equilibrio ottimale tra il numero di impression e di conversioni servite. Consente di regolare il numero di impression da visualizzare prima di iniziare a vedere rendimenti in diminuzione. |
| [[!UICONTROL Unique User Reach] Report](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/unique-user-reach.html) | Un grafico a bolle, in cui ogni bolla viene ridimensionata in proporzione diretta al numero di utenti univoci per la dimensione selezionata. |

### Considerazioni

* Se [!DNL Audience Optimization Reports] gli utenti dispongono di controlli di accesso basati sul ruolo (RBAC), quindi [!DNL Adobe Customer Care] deve configurare una mappatura tra l’ID inserzionista e il codice di integrazione dell’origine dati di Audience Manager dell’organizzazione. Gli utenti amministratori possono quindi fornire i diritti RBAC a utenti diversi.

* Reporting sulle conversioni in [!DNL Audience Optimization Reports] richiede alcune impostazioni da parte dell’utente finale. Gli utenti devono compilare i file di metadati.

* [!DNL Audience Optimization Reports] non supporta le modifiche ai metadati della campagna (come il nome della campagna o del posizionamento).

* I clic sugli annunci di ricerca sono inclusi in [!DNL Audience Optimization Reports] solo quando sono correlati con le impression. In altre parole, i clic di ricerca vengono trattati come conversioni successive alle impression. Di conseguenza, molti clic di ricerca potrebbero non essere inclusi in [!DNL Audience Optimization Reports].

>[!MORELIKETHIS]
>
>* [Panoramica dell’invio dei dati sull’esposizione ai contenuti multimediali dell’DSP a Adobe Audience Manager](overview.md)
>* [Raccogliere dati di clic e impression dalle campagne Advertising DSP](collect.md)

