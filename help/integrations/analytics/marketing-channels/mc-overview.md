---
title: Nozioni fondamentali di [!DNL Marketing Channels]
description: Informazioni chiave [!DNL Analytics Marketing Channels] che [!DNL Analytics for Advertising] gli utenti devono comprendere.
feature: Integration with Adobe Analytics
exl-id: de02dff5-86ce-41e8-89c6-3c11f6375b77
source-git-commit: 7e614ecb517515217d812926f61ca10437820efd
workflow-type: tm+mt
source-wordcount: '568'
ht-degree: 0%

---

# Nozioni fondamentali di [!DNL Analytics Marketing Channels]

*Inserzionisti con una sola integrazione Advertising-Adobe Analytics di Adobe*

Questa pagina spiega le informazioni chiave su [!DNL Analytics Marketing Channels] che [!DNL Analytics for Advertising] gli utenti devono capire.

Per la documentazione completa su [!DNL Marketing Channels], vedi &quot;[Introduzione a [!DNL Marketing Channels]](https://experienceleague.adobe.com/docs/analytics/components/marketing-channels/c-getting-started-mchannel.html).&quot;

## Panoramica [!DNL Marketing Channels]

[!DNL Marketing Channels] sono una funzionalità chiave di Adobe Analytics. [!DNL Marketing Channels] i rapporti mostrano come i clienti arrivano al tuo sito web tramite l’intervallo di reporting e come ogni canale influisce sui ricavi o sul comportamento sul sito.

Prendi in considerazione l’esempio seguente di un percorso di visite incrociate. Ogni visita al sito web è indicata dal canale di marketing da cui il visitatore è entrato. La prima visita, nota anche come Canale primo contatto, è E-mail. La visualizzazione alla seconda visita è un canale partecipante e la ricerca naturale è considerata il canale ultimo contatto. Se utilizzi [!UICONTROL Last Touch Attribution] entro [!UICONTROL Attribution IQ], la funzione Ricerca naturale riceverà un credito completo per l’evento di conversione da $ 250. Utilizzando il servizio Experience Cloud ID, puoi collegare le singole visite per mostrare un percorso per un singolo visitatore.

![Esempio di percorso di conversione cross-visit in canali di marketing](/help/integrations/assets/a4adc-mc-sample-journey.png)

Utilizzando [!UICONTROL Marketing Channels] Regole di elaborazione, puoi creare set di logiche per determinare i canali che guidano il traffico e per monitorare ogni canale quando gli utenti arrivano al tuo sito. Ad esempio, il [!UICONTROL Email] il canale è indicato da un codice di tracciamento univoco generato al momento del clic che, se registrato da Adobe Analytics, classifica la visita come proveniente da una campagna di marketing e-mail.

## Regole di elaborazione e modalità di impostazione dei canali di marketing

Ogni volta che un utente accede a un sito web, lo fa tramite un URL che ha fatto clic o digitato direttamente nella barra degli indirizzi. Quando l’utente accede al sito web, [!DNL Analytics] tiene traccia delle informazioni che possono essere utilizzate per determinare il canale che ha guidato la visita.

Spesso, gli addetti al marketing aggiungono codici di tracciamento dei parametri della stringa di query agli URL dei canali per aiutare a tracciare l&#39;impatto del canale sul loro sito. Puoi configurare [!DNL Marketing Channels] regole di elaborazione per ascoltare parametri e valori di tracciamento specifici per determinare il canale senza alcun ulteriore tracciamento. Ad esempio, se tutti gli URL della campagna e-mail seguono il formato `www.adobe.com?cid=email…` (dove l’URL contiene il parametro e il valore della stringa di query `cid=email`), quindi puoi creare una regola per ascoltare questo codice di tracciamento e per seccare la visita in [!UICONTROL Email] canale.

Altri canali non dispongono di percorsi URL tracciabili e necessitano di ulteriori logiche per l’identificazione. Ad esempio: [!UICONTROL Earned Social], in cui un utente fa clic su un collegamento che un altro utente ha condiviso organicamente su un social network, è un canale importante da monitorare. Tuttavia, l’addetto al marketing non ha modo di aggiungere un codice di tracciamento dei parametri della stringa di query all’URL condiviso. In questo caso, puoi creare una regola di elaborazione per ascoltare il dominio di riferimento delle reti sociali di interesse e l&#39;assenza di codici di tracciamento a pagamento per determinare il canale. Le visite che soddisfano questi requisiti vengono quindi tracciate come Social guadagnato nel rapporto Canali di marketing .

Adobe consiglia di collaborare con il team di analytics per creare un set completo di [!DNL Marketing Channels] regole di elaborazione per tenere traccia di tutti i canali pertinenti alla tua azienda. In questo modo puoi creare potenti rapporti di attribuzione.

Per capire in che modo Adobe Advertising può contribuire ai segnali necessari per creare canali di marketing personalizzati, vedi &quot;[Utilizzo degli ID pubblicitari per creare [!DNL Marketing Channels] Regole](mc-ids.md).&quot;

>[!MORELIKETHIS]
>
>* [Utilizzo degli ID pubblicitari di Adobe per creare [!DNL Marketing Channels] Regole di elaborazione](mc-ids.md)
>* [Perché i dati del canale possono variare tra la pubblicità Adobe e [!DNL Marketing Channels]](mc-data-variances.md)
>* [Utilizzo [!DNL Analytics Marketing Channels] con i dati pubblicitari di Adobe](mc-ac-data.md)
>* [Video: Utilizzo [!DNL Marketing Channels] ad Adobe Advertising Reporting](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-reporting-a4adc.html)
>* [Panoramica [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)

