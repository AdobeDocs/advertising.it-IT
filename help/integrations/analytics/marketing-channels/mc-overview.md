---
title: Nozioni di base di  [!DNL Marketing Channels]
description: Scopri le informazioni chiave su [!DNL Analytics Marketing Channels] che [!DNL Analytics for Advertising] gli utenti dovrebbero comprendere.
feature: Integration with Adobe Analytics
exl-id: de02dff5-86ce-41e8-89c6-3c11f6375b77
TQID: https://experienceleague.adobe.com/NJ4LPss-g-J06PuvdCaUktHPyP7MARdJK84-D8gnwAk
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: beb7a3c1-66ab-4786-b879-7621375b3c40
source-git-commit: 7845129ba6566c1aaaf160cc6f9ad33bf1731f75
workflow-type: tm+mt
source-wordcount: 561
ht-degree: 0%

---

# Nozioni di base di [!DNL Analytics Marketing Channels]

In questa pagina sono illustrate le informazioni chiave su [!DNL Analytics Marketing Channels] che [!DNL Analytics for Advertising] utenti devono comprendere.

Per la documentazione completa su [!DNL Marketing Channels], vedere &quot;[Introduzione a [!DNL Marketing Channels]](https://experienceleague.adobe.com/en/docs/analytics/components/marketing-channels/c-getting-started-mchannel).&quot;

## Panoramica di [!DNL Marketing Channels]

[!DNL Marketing Channels] sono funzionalità chiave di Adobe Analytics. I rapporti di [!DNL Marketing Channels] mostrano come i clienti arrivano al tuo sito web tramite l&#39;intervallo di reporting e come ogni canale influisce sui ricavi o sul comportamento in loco.

Prendi in considerazione l’esempio seguente di un percorso di visite incrociate. Ogni visita al sito web è indicata dal canale di marketing da cui il visitatore è entrato. La prima visita, denominata anche Canale di primo contatto, è l’E-mail. La visualizzazione durante la seconda visita è un canale partecipante e la ricerca naturale è considerata il canale di ultimo contatto. Se utilizzi [!UICONTROL Last Touch Attribution] entro [!UICONTROL Attribution IQ], la ricerca naturale riceve il merito completo per l&#39;evento di conversione da $ 250. Utilizzando il servizio Adobe CX Enterprise ID, puoi collegare queste visite individuali per mostrare un percorso per un singolo visitatore.

![Esempio di percorso di conversione tra visite in canali di marketing](/help/integrations/assets/a4adc-mc-sample-journey.png)

Utilizzando le regole di elaborazione di [!UICONTROL Marketing Channels], puoi creare set di logica per determinare i canali che generano il traffico e per tenere traccia di ciascun canale mentre gli utenti arrivano sul tuo sito. Ad esempio, il canale [!UICONTROL Email] è indicato da un codice di tracciamento univoco generato al momento del clic che, quando registrato da Adobe Analytics, classifica la visita come proveniente da una campagna di marketing e-mail.

## Regole di elaborazione e impostazione dei canali di marketing

Ogni volta che un utente accede a un sito web, lo fa tramite un URL su cui fa clic o che digita direttamente nella barra degli indirizzi. Quando l&#39;utente accede al sito Web, [!DNL Analytics] tiene traccia delle informazioni che possono essere utilizzate per determinare il canale che ha guidato la visita.

Spesso, gli addetti al marketing accodano i codici di tracciamento dei parametri delle stringhe di query agli URL del canale per monitorare l’impatto del canale sul sito. È possibile configurare [!DNL Marketing Channels] regole di elaborazione per l&#39;ascolto di parametri e valori di tracciamento specifici per determinare il canale senza alcun tracciamento aggiuntivo. Ad esempio, se tutti gli URL della campagna e-mail seguono il formato `www.adobe.com?cid=email…` (dove l&#39;URL contiene il parametro della stringa di query e il valore `cid=email`), puoi creare una regola per ascoltare questo codice di tracciamento e bucket la visita nel canale [!UICONTROL Email].

Other channels don&#39;t have trackable URL paths and need further logic for identification. For example, [!UICONTROL Earned Social], in which a user clicks a link that another user shared organically on a social network, is an important channel to track. However, the marketer has no way to append a query string parameter tracking code to the URL that&#39;s shared. In this case, you could create a processing rule to listen for the referring domain of social networks of interest and the absence of paid tracking codes to determine the channel. The visits that meet these requirements then would be tracked as Earned Social within the Marketing Channels report.

Adobe recommends working with your [!DNL Analytics] team to build a comprehensive set of [!DNL Marketing Channels] processing rules that track all pertinent channels. Doing so allows you to create powerful attribution reporting.

To understand how Adobe Advertising can contribute to the signals necessary to create custom marketing channels, see &quot;[Using Adobe Advertising IDs to create [!DNL Marketing Channels] processing rules](mc-ids.md).&quot;

>[!MORELIKETHIS]
>
>* [Using Adobe Advertising IDs to create [!DNL Marketing Channels] processing rules](mc-ids.md)
>* [Why channel data can vary between Adobe Advertising and [!DNL Marketing Channels]](mc-data-variances.md)
>* [Using [!DNL Analytics Marketing Channels] with Adobe Advertising data](mc-ac-data.md)
>* [Video: Using [!DNL Marketing Channels] for Adobe Advertising reporting](https://experienceleague.adobe.com/en/docs/advertising-learn/tutorials/analytics/analytics-reporting-a4adc)
>* [Panoramica di [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)
