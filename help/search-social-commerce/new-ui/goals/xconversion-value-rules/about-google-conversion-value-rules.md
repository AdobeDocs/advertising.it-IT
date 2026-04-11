---
title: Informazioni sulle  [!DNL Google Ads] regole del valore di conversione
description: Scopri come visualizzare e gestire le regole del valore di conversione  [!DNL Google Ads]  in Search, Social e Commerce.
source-git-commit: e15d34f3f32a8565735e53f1ce40e71008dbb4d9
workflow-type: tm+mt
source-wordcount: '454'
ht-degree: 0%

---

# Informazioni sulle regole del valore di conversione [!DNL Google Ads]

Cerca, Social e Commerce sincronizzano automaticamente le [regole del valore di conversione](https://support.google.com/google-ads/answer/10518330) dai tuoi account [!DNL Google Ads]. Le regole del valore di conversione ti consentono di regolare i valori degli eventi di conversione in base alle informazioni dell’utente, tra cui il tipo di dispositivo, la posizione e il segmento di pubblico. Con Google Smart Bidding puoi utilizzare le regole per le offerte basate sul valore nelle campagne di ricerca, visualizzazione, acquisto e prestazione massima. Per le campagne con strategie di offerta Maximize Conversions (Massimizza conversioni) e Target ROAS, gli algoritmi [!DNL Google Ads] inizieranno a preferire le conversioni con un valore più alto.

Le regole dei valori di conversione a livello di campagna sostituiscono le regole a livello di conto. Quando una conversione soddisfa più regole del valore di conversione, viene applicata solo una delle regole. Di solito viene applicata la regola più specifica, ma consulta la [[!DNL Google Ads] documentazione sulle priorità per i diversi tipi di condizioni della regola](https://support.google.com/google-ads/answer/10520348).

## Visualizzazione e funzionalità di [!UICONTROL Conversion Value Rules]

Tutte le regole create nell&#39;interfaccia [!DNL Google Ads] vengono sincronizzate entro 24 ore e sono disponibili nella visualizzazione [!UICONTROL Goals] > [!UICONTROL Conversion Value Rules]. Alcuni account possono gestire le regole del valore di conversione:

* Nei conti per i quali vengono tracciate le conversioni a livello del singolo account o della campagna, puoi creare, modificare e modificare lo stato delle regole a livello di account e di campagna.

  Gli account possono essere collegati agli account manager [!DNL Google Ads], ma non possono utilizzare il tracciamento delle conversioni tra account diversi (le cui conversioni vengono tracciate in tutti gli account dell&#39;account manager).

* Negli account che utilizzano il tracciamento delle conversioni tra account, le regole a livello di account e di campagna vengono ereditate dall’account manager e sono di sola lettura.

## Regole del valore di conversione con i portfolio Search, Social e Commerce

Quando l&#39;account dell&#39;inserzionista è configurato per caricare gli obiettivi Search, Social e Commerce in [!DNL Google Ads] e si include una campagna che utilizza una regola del valore di conversione in un portfolio con un obiettivo, [!DNL Google Ads] applica la regola del valore di conversione al valore di conversione originale specificato nell&#39;obiettivo. Di conseguenza, i dati di conversione in Search, Social e Commerce sono diversi da quelli in [!DNL Google Ads].

Ad esempio, supponiamo che l’obiettivo utilizzi una singola metrica di conversione &quot;Lead&quot; e dia alle conversioni da dispositivi mobili un peso di 10 e alle conversioni da dispositivi non mobili un peso di 10. Search, Social e Commerce contano un evento da entrambi i tipi di dispositivi come una (1) conversione e attribuiscono il valore di conversione come 10. Tuttavia, supponiamo che una campagna in tale portfolio utilizzi una regola del valore di conversione &quot;Se il dispositivo è mobile, moltiplicalo per 2&quot;. Quando viene tracciato un evento di lead mobili per tale campagna, [!DNL Google Ads] attribuisce anche il conteggio di conversione come uno (1) ma il valore di conversione come (10 x 2) = 20.

Per ulteriori informazioni sulle regole, inclusi i valori di conversione originali prima dell&#39;applicazione delle regole, vedere il report delle regole del valore di conversione [in [!DNL Google Ads]](https://support.google.com/google-ads/answer/10519848).

>[!MORELIKETHIS]
>
>* [Crea una [!DNL Google Ads] regola del valore di conversione](create-google-conversion-value-rule.md)
>* [Modifica una [!DNL Google Ads] regola del valore di conversione](edit-google-conversion-value-rule.md)
>* [Modifica lo stato di una  [!DNL Google Ads] regola del valore di conversione](change-the-status-of-google-conversion-value-rule.md)
>* [[!DNL Google Ads] impostazioni regola del valore di conversione](google-conversion-value-rule-settings.md)

