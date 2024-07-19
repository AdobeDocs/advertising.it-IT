---
title: Nozioni di base di  [!DNL Marketing Channels]
description: Scopri le informazioni chiave su [!DNL Analytics Marketing Channels] che [!DNL Analytics for Advertising] gli utenti dovrebbero comprendere.
feature: Integration with Adobe Analytics
exl-id: de02dff5-86ce-41e8-89c6-3c11f6375b77
source-git-commit: 29b49e8fa54580d7cdd62f9a10fd2616def4694b
workflow-type: tm+mt
source-wordcount: '548'
ht-degree: 0%

---

# Nozioni di base di [!DNL Analytics Marketing Channels]

In questa pagina sono illustrate le informazioni chiave su [!DNL Analytics Marketing Channels] che [!DNL Analytics for Advertising] utenti devono comprendere.

Per la documentazione completa su [!DNL Marketing Channels], vedere &quot;[Introduzione a [!DNL Marketing Channels]](https://experienceleague.adobe.com/docs/analytics/components/marketing-channels/c-getting-started-mchannel.html).&quot;

## Panoramica di [!DNL Marketing Channels]

[!DNL Marketing Channels] sono funzionalità chiave di Adobe Analytics. I rapporti di [!DNL Marketing Channels] mostrano come i clienti arrivano al tuo sito web tramite l&#39;intervallo di reporting e come ogni canale influisce sui ricavi o sul comportamento in loco.

Prendi in considerazione l’esempio seguente di un percorso di visite incrociate. Ogni visita al sito web è indicata dal canale di marketing da cui il visitatore è entrato. La prima visita, denominata anche Canale di primo contatto, è l’E-mail. La visualizzazione durante la seconda visita è un canale partecipante e la ricerca naturale è considerata il canale di ultimo contatto. Se utilizzi [!UICONTROL Last Touch Attribution] entro [!UICONTROL Attribution IQ], la ricerca naturale riceverà il merito completo per l&#39;evento di conversione da $ 250. Utilizzando il servizio ID di Experience Cloud, puoi collegare queste visite individuali per mostrare un percorso per un singolo visitatore.

![Esempio di percorso di conversione tra visite in canali di marketing](/help/integrations/assets/a4adc-mc-sample-journey.png)

Utilizzando [!UICONTROL Marketing Channels] Regole di elaborazione, puoi creare set di logica per determinare i canali che generano il traffico e per tenere traccia di ciascun canale quando gli utenti arrivano sul tuo sito. Ad esempio, il canale [!UICONTROL Email] sarebbe indicato da un codice di tracciamento univoco generato al momento del clic che, una volta registrato da Adobe Analytics, classificherebbe la visita come proveniente da una campagna di marketing e-mail.

## Regole di elaborazione e impostazione dei canali di marketing

Ogni volta che un utente accede a un sito web, lo fa tramite un URL su cui fa clic o che digita direttamente nella barra degli indirizzi. Quando l&#39;utente accede al sito Web, [!DNL Analytics] tiene traccia delle informazioni che possono essere utilizzate per determinare il canale che ha guidato la visita.

Spesso, gli addetti al marketing accodano i codici di tracciamento dei parametri delle stringhe di query agli URL del canale per monitorare l’impatto del canale sul sito. È possibile configurare [!DNL Marketing Channels] regole di elaborazione per l&#39;ascolto di parametri e valori di tracciamento specifici per determinare il canale senza alcun tracciamento aggiuntivo. Ad esempio, se tutti gli URL della campagna e-mail seguono il formato `www.adobe.com?cid=email…` (dove l&#39;URL contiene il parametro della stringa di query e il valore `cid=email`), puoi creare una regola per ascoltare questo codice di tracciamento e bucket la visita nel canale [!UICONTROL Email].

Gli altri canali non dispongono di percorsi URL tracciabili e richiedono un’ulteriore logica per l’identificazione. Ad esempio, [!UICONTROL Earned Social], in cui un utente fa clic su un collegamento condiviso organicamente da un altro utente su un social network, è un canale importante da monitorare. Tuttavia, l’addetto marketing non ha modo di aggiungere all’URL condiviso un codice di tracciamento dei parametri della stringa di query. In questo caso, puoi creare una regola di elaborazione per ascoltare il dominio di riferimento dei social network di interesse e l’assenza di codici di tracciamento a pagamento per determinare il canale. Le visite che soddisfano questi requisiti vengono quindi registrate come Earned Social (Guadagni sociali) nel rapporto Marketing Channels (Canali di marketing).

Adobe consiglia di collaborare con il team di analisi per creare un set completo di [!DNL Marketing Channels] regole di elaborazione per tenere traccia di tutti i canali pertinenti alla tua azienda. In questo modo puoi creare rapporti di attribuzione efficaci.

Per capire come Adobe Advertising può contribuire ai segnali necessari per la creazione di canali di marketing personalizzati, consulta &quot;[Utilizzo degli ID di Advertising per la creazione di  [!DNL Marketing Channels] Regole](mc-ids.md).&quot;

>[!MORELIKETHIS]
>
>* [Utilizzo degli ID Adobe Advertising per la creazione [!DNL Marketing Channels] Regole di elaborazione](mc-ids.md)
>* [Perché i dati del canale possono variare tra Adobe Advertising e [!DNL Marketing Channels]](mc-data-variances.md)
>* [Utilizzo di [!DNL Analytics Marketing Channels] con dati Adobe Advertising](mc-ac-data.md)
>* [Video: utilizzo di [!DNL Marketing Channels] per Adobe Advertising di reporting](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-reporting-a4adc.html)
>* [Panoramica di [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)
