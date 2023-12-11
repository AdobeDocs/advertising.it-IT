---
title: Nozioni di base di [!DNL Marketing Channels]
description: Scopri le informazioni chiave su [!DNL Analytics Marketing Channels] che [!DNL Analytics for Advertising] Gli utenti dovrebbero capire.
feature: Integration with Adobe Analytics
exl-id: de02dff5-86ce-41e8-89c6-3c11f6375b77
source-git-commit: 29b49e8fa54580d7cdd62f9a10fd2616def4694b
workflow-type: tm+mt
source-wordcount: '548'
ht-degree: 0%

---

# Nozioni di base di [!DNL Analytics Marketing Channels]

Questa pagina spiega le informazioni chiave su [!DNL Analytics Marketing Channels] che [!DNL Analytics for Advertising] gli utenti devono capire.

Per la documentazione completa su [!DNL Marketing Channels], vedere &quot;[Introduzione a [!DNL Marketing Channels]](https://experienceleague.adobe.com/docs/analytics/components/marketing-channels/c-getting-started-mchannel.html).&quot;

## Panoramica di [!DNL Marketing Channels]

[!DNL Marketing Channels] sono una funzione chiave di Adobe Analytics. [!DNL Marketing Channels] i rapporti mostrano come i clienti arrivano al tuo sito web attraverso il periodo definito per la generazione del rapporto e come ogni canale influisce sui ricavi o sul comportamento nel sito.

Prendi in considerazione l’esempio seguente di un percorso di visite incrociate. Ogni visita al sito web è indicata dal canale di marketing da cui il visitatore è entrato. La prima visita, denominata anche Canale di primo contatto, è l’E-mail. La visualizzazione durante la seconda visita è un canale partecipante e la ricerca naturale è considerata il canale di ultimo contatto. Se usa [!UICONTROL Last Touch Attribution] entro [!UICONTROL Attribution IQ], alla ricerca naturale verrebbe attribuito il merito completo per l’evento di conversione da 250 $. Utilizzando il servizio ID di Experience Cloud, puoi collegare queste visite individuali per mostrare un percorso per un singolo visitatore.

![Esempio di percorso di conversione tra visite in canali di marketing](/help/integrations/assets/a4adc-mc-sample-journey.png)

Utilizzando [!UICONTROL Marketing Channels] Regole di elaborazione, puoi creare set di logica per determinare i canali che determinano il traffico e per monitorare ciascun canale mentre gli utenti arrivano sul tuo sito. Ad esempio, il [!UICONTROL Email] il canale sarebbe indicato da un codice di tracciamento univoco generato al momento del clic che, se registrato da Adobe Analytics, categorizzerebbe la visita come proveniente da una campagna di marketing e-mail.

## Regole di elaborazione e impostazione dei canali di marketing

Ogni volta che un utente accede a un sito web, lo fa tramite un URL su cui fa clic o che digita direttamente nella barra degli indirizzi. Quando l’utente accede al sito web, [!DNL Analytics] tiene traccia delle informazioni che possono essere utilizzate per determinare il canale che ha guidato la visita.

Spesso, gli addetti al marketing accodano i codici di tracciamento dei parametri delle stringhe di query agli URL del canale per monitorare l’impatto del canale sul sito. Puoi configurare [!DNL Marketing Channels] regole di elaborazione per ascoltare parametri e valori di tracciamento specifici e determinare il canale senza alcun tracciamento aggiuntivo. Ad esempio, se tutti gli URL della campagna e-mail seguono il formato `www.adobe.com?cid=email…` (dove l’URL contiene il parametro e il valore della stringa di query) `cid=email`), quindi puoi creare una regola per ascoltare questo codice di tracciamento e archiviare la visita nel [!UICONTROL Email] canale.

Gli altri canali non dispongono di percorsi URL tracciabili e richiedono un’ulteriore logica per l’identificazione. Ad esempio: [!UICONTROL Earned Social], in cui un utente fa clic su un collegamento condiviso organicamente da un altro utente su un social network, è un canale importante da monitorare. Tuttavia, l’addetto marketing non ha modo di aggiungere all’URL condiviso un codice di tracciamento dei parametri della stringa di query. In questo caso, puoi creare una regola di elaborazione per ascoltare il dominio di riferimento dei social network di interesse e l’assenza di codici di tracciamento a pagamento per determinare il canale. Le visite che soddisfano questi requisiti vengono quindi registrate come Earned Social (Guadagni sociali) nel rapporto Marketing Channels (Canali di marketing).

Adobe consiglia di collaborare con il team di analisi per creare un set completo di [!DNL Marketing Channels] regole di elaborazione per tenere traccia di tutti i canali pertinenti alla tua azienda. In questo modo puoi creare rapporti di attribuzione efficaci.

Per scoprire come Adobi Advertising può contribuire ai segnali necessari per la creazione di canali di marketing personalizzati, consulta la sezione &quot;[Utilizzo degli ID pubblicitari per creare [!DNL Marketing Channels] Regole](mc-ids.md).&quot;

>[!MORELIKETHIS]
>
>* [Utilizzo degli ID Adobi Advertising per la creazione [!DNL Marketing Channels] Regole di elaborazione](mc-ids.md)
>* [Perché i dati del canale possono variare tra Adobe Advertising e [!DNL Marketing Channels]](mc-data-variances.md)
>* [Utilizzo di [!DNL Analytics Marketing Channels] con dati Adobi Advertising](mc-ac-data.md)
>* [Video: Utilizzo [!DNL Marketing Channels] ad Adobe Advertising Reporting](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-reporting-a4adc.html)
>* [Panoramica di [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)
