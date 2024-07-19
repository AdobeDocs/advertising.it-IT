---
title: Utilizzo di  [!DNL Marketing Channels]  con dati Adobe Advertising
description: Scopri come utilizzare i dati Adobe Advertising in [!DNL Analytics Marketing Channels].
feature: Integration with Adobe Analytics
exl-id: 522c7f01-1138-477d-8018-36030caab55e
source-git-commit: 7e614ecb517515217d812926f61ca10437820efd
workflow-type: tm+mt
source-wordcount: '713'
ht-degree: 0%

---

# Utilizzo di [!DNL Analytics Marketing Channels] con dati Adobe Advertising

*Inserzionisti con una sola integrazione Adobe Advertising-Adobe Analytics*

Utilizzando i report Adobe Advertising e [!DNL Analytics Marketing Channels], puoi ottenere informazioni utili su come i contenuti multimediali digitali influenzano l&#39;attività del sito.

<!-- from video: By using Marketing Channels with your Adobe Advertising data, you can get a more holistic view of how your advertising efforts are affecting site behavior. In particular, you can see the value of your view-through and click-through data, and how your advertising assists or is assisted by other channels. -->

Nella figura seguente viene illustrato come Adobe Advertising e [!DNL Marketing Channels] tengono traccia delle singole visite che costituiscono il percorso di un visitatore. I report Adobe Advertising in [!DNL Analytics] sono limitati solo alla pubblicità a pagamento tramite display, search, social e commerce channel, che viene trafficata attraverso Adobe Advertising, utilizzando l’AMO ID. Tuttavia, [!DNL Marketing Channels] tiene traccia di tutti i canali configurati nelle regole di elaborazione [!DNL Marketing Channels].

![Come Adobe Advertising e [!DNL Marketing Channels] tengono traccia delle singole visite nel percorso di un visitatore](/help/integrations/assets/a4adc-mc-sample-journey2.png)

Nella prima visita, l’utente è entrato nel sito web tramite una campagna e-mail, ha eseguito dieci visualizzazioni di pagina e poi se ne è andato. Nella seconda visita, l’utente è entrato nel sito tramite un annuncio pubblicitario, ha eseguito dieci visualizzazioni di pagina e poi se n’è andato. Nella terza visita, l’utente è entrato nel sito tramite ricerca naturale, ha eseguito cinque visualizzazioni di pagina, ha eseguito una conversione da 250 $ e ha lasciato. Si noti la differenza nel tracciamento tra [!DNL Marketing Channels] e Adobe Advertising. L&#39;unico canale che l&#39;Adobe Advertising traccia in questo percorso è [!UICONTROL Display]. L&#39;Adobe Advertising tiene traccia della visita al canale [!UICONTROL Display] e attribuisce i dati di coinvolgimento successivi (come le visualizzazioni di pagina) e le conversioni all&#39;influenza dell&#39;annuncio pubblicitario. [!DNL Marketing Channels], invece, offre una visualizzazione completa di tutti i canali.

Poiché l’AMO ID persiste nel percorso del visitatore, puoi utilizzare i dati AMO ID per vedere in che modo Adobe Advertising influenza altri canali di marketing. L&#39;AMO ID [ persiste per 60 giorni per impostazione predefinita](/help/integrations/analytics/overview.md), ma puoi configurare la persistenza in base alle esigenze.

## Come combinare i dati dei canali di Adobe Advertising e marketing per analizzare le prestazioni dei contenuti multimediali

In [!DNL Analytics], puoi combinare l&#39;Adobe Advertising dei dati persistenti della pubblicità a pagamento e i dati completi sulle visite di [!DNL Marketing Channels] per analizzare meglio le prestazioni multimediali in modo da influenzare meglio il percorso dei clienti.

L’analisi seguente utilizza i dati dell’Adobe Advertising per mostrare versioni diverse di come un annuncio pubblicitario visualizzato influisce sulla conversione del sito. Tutte e tre le colonne utilizzano le stesse metriche di conversione, ma ogni colonna racconta una storia diversa:

* La colonna 1 esamina i dati AMO ID che rimangono costanti nel percorso del visitatore. La colonna 1 indica che 641 avvii di applicazioni sono stati, in un determinato punto, collegati a un Adobe Advertising pubblicitario, tramite un evento view-through o click-through. Questa visualizzazione non prende in considerazione nessun&#39;altra attribuzione [!DNL Marketing Channels].

* Nel set di dati [!DNL Marketing Channels], tuttavia, gli avvii di 641 applicazioni sono attribuiti ad altri canali di marketing. Le ultime due colonne prendono 641 Applicazioni avviate e limitano i dati ai canali [!UICONTROL Display Click-Through] e [!UICONTROL Display View-Through], mostrando le conversioni che si verificano in un modello di attribuzione ultimo contatto.

![esempio di come un annuncio visualizzato influisce sulla conversione del sito](/help/integrations/assets/a4adc-mc-display-impact.png)

Puoi portare questa analisi un passo avanti. Puoi scomporre ulteriormente la riga dell’Adobe Advertising per canale di marketing per vedere dove le conversioni dell’Adobe Advertising sono attribuite all’avvio di 641 applicazioni. Già sai che cinque di queste conversioni sono attribuite a un click-through con visualizzazione dell’ultimo contatto e 19 a un view-through con visualizzazione dell’ultimo contatto. Rimangono ancora 617 avvii di applicazioni attribuiti ad altri canali di marketing. Puoi trascinare e rilasciare la dimensione Last Touch Channel (Canale di ultimo contatto) sopra la voce di riga Advertising DSP per visualizzare l’attribuzione del canale per il resto degli avvii delle applicazioni e mostrare l’impatto cross-channel del canale di visualizzazione.

![come aggiungere la dimensione Canale di ultimo contatto](/help/integrations/assets/a4adc-mc-display-impact-ltc.png)

Ora puoi vedere come vengono attribuiti gli altri avvii delle applicazioni. All’e-mail viene assegnato il merito per 357 avvii delle applicazioni di ultimo contatto per i quali è persistito un AMO ID. Utilizzando questo tipo di analisi, puoi vedere l’impatto degli annunci display di Adobe Advertising su tutti i canali. Con un solo set di dati e modello di attribuzione, questo tipo di informazioni non sarebbe disponibile.

![esempio dell&#39;impatto cross-channel dei canali di visualizzazione](/help/integrations/assets/a4adc-mc-display-impact-x-channel.png)

Puoi migliorare ulteriormente l’analisi utilizzando un grafico a stack impostato su &quot;Sovrapposizione 100%&quot; per mostrare i dati con tendenze nel tempo. Questa visualizzazione consente di monitorare più facilmente quali canali di marketing di ultimo contatto sono più fortemente interessati dalle campagne di marketing display.

![esempio dell&#39;impatto multicanale con tendenze dei canali di visualizzazione](/help/integrations/assets/a4adc-mc-display-impact-x-channel-trend.png)

>[!MORELIKETHIS]
>
>* [Nozioni di base di [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [Utilizzo degli ID Adobe Advertising per la creazione [!DNL Marketing Channels] Regole di elaborazione](mc-ids.md)
>* [Perché i dati del canale possono variare tra Adobe Advertising e [!DNL Marketing Channels]](mc-data-variances.md)
>* [Video: utilizzo di [!DNL Marketing Channels] per Adobe Advertising di reporting](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-reporting-a4adc.html)
>* [Panoramica di [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)
