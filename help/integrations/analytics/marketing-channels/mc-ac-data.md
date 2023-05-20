---
title: Utilizzo di [!DNL Marketing Channels] con i dati pubblicitari di Adobe
description: Scopri come utilizzare i dati di Adobe Advertising in [!DNL Analytics Marketing Channels].
feature: Integration with Adobe Analytics
exl-id: 522c7f01-1138-477d-8018-36030caab55e
source-git-commit: 7e614ecb517515217d812926f61ca10437820efd
workflow-type: tm+mt
source-wordcount: '708'
ht-degree: 0%

---

# Utilizzo di [!DNL Analytics Marketing Channels] con i dati pubblicitari di Adobe

*Inserzionisti con un Adobe di integrazione Advertising-Adobe Analytics Only*

Utilizzando sia Adobe Advertising che [!DNL Analytics Marketing Channels] rapporti, puoi ottenere informazioni utili su come i contenuti multimediali digitali influenzano l’attività del sito.

<!-- from video: By using Marketing Channels with your Adobe Advertising data, you can get a more holistic view of how your advertising efforts are affecting site behavior. In particular, you can see the value of your view-through and click-through data, and how your advertising assists or is assisted by other channels. -->

L’illustrazione seguente mostra come Adobe Advertising e [!DNL Marketing Channels] tenere traccia delle singole visite che compongono il percorso di un visitatore. Adobe di rapporti sulla pubblicità in [!DNL Analytics] sono limitati solo alla pubblicità a pagamento tramite display, search, social e commerce channel trafficata attraverso Adobe Advertising, utilizzando l’AMO ID. Tuttavia, [!DNL Marketing Channels] tiene traccia di tutti i canali configurati in [!DNL Marketing Channels] Regole di elaborazione.

![Come Adobe la pubblicità e [!DNL Marketing Channels] tenere traccia delle singole visite nel percorso di un visitatore](/help/integrations/assets/a4adc-mc-sample-journey2.png)

Nella prima visita, l’utente è entrato nel sito web tramite una campagna e-mail, ha eseguito dieci visualizzazioni di pagina e poi se ne è andato. Nella seconda visita, l’utente è entrato nel sito tramite un annuncio pubblicitario, ha eseguito dieci visualizzazioni di pagina e poi se n’è andato. Nella terza visita, l’utente è entrato nel sito tramite ricerca naturale, ha eseguito cinque visualizzazioni di pagina, ha eseguito una conversione da 250 $ e ha lasciato. Notate la differenza nel tracciamento tra [!DNL Marketing Channels] e pubblicità Adobe. L’unico canale che Adobe Advertising traccia in questo percorso è [!UICONTROL Display]. Adobe Advertising tiene traccia della [!UICONTROL Display] visita del canale e attribuisce i dati del coinvolgimento successivo (come le visualizzazioni di pagina) e le conversioni all’influenza dell’annuncio pubblicitario. [!DNL Marketing Channels], dall&#39;altro, offre una visione completa di tutti i canali.

Poiché l’AMO ID persiste nel percorso del visitatore, puoi utilizzare i dati AMO ID per vedere in che modo la pubblicità Adobe influisce su altri canali di marketing. AMO ID [persiste per 60 giorni per impostazione predefinita](/help/integrations/analytics/overview.md), ma puoi configurare la persistenza in base alle esigenze.

## Come combinare i dati dei canali pubblicitari e di marketing Adobi per analizzare le prestazioni dei contenuti multimediali

Entro [!DNL Analytics], puoi combinare i dati pubblicitari a pagamento persistenti di Adobe Advertising e la [!DNL Marketing Channels] dati completi sulle visite per analizzare meglio le prestazioni multimediali in modo da influenzare meglio il percorso dei clienti.

L’analisi seguente utilizza i dati di Adobe Advertising per mostrare diverse versioni del modo in cui un annuncio pubblicitario influisce sulla conversione del sito. Tutte e tre le colonne utilizzano le stesse metriche di conversione, ma ogni colonna racconta una storia diversa:

* La colonna 1 esamina i dati AMO ID che rimangono costanti nel percorso del visitatore. La colonna 1 indica che 641 avvii di applicazioni sono stati collegati a un Adobe di annunci pubblicitari tramite un evento view-through o click-through. Questa visualizzazione non considera altri [!DNL Marketing Channels] attribuzione in considerazione.

* In [!DNL Marketing Channels] Tuttavia, il set di dati 641 Applications Starts è attribuito ad altri canali di marketing. Le ultime due colonne prendono 641 Applications Starts e limitano i dati a [!UICONTROL Display Click-Through] e [!UICONTROL Display View-Through] canali, mostrando le conversioni che si verificano in un modello di attribuzione ultimo contatto.

![esempio di come una visualizzazione annuncio influisce sulla conversione del sito](/help/integrations/assets/a4adc-mc-display-impact.png)

Puoi portare questa analisi un passo avanti. Puoi scomporre ulteriormente la riga Adobe Advertising per canale di marketing per vedere dove le conversioni di Adobe Advertising sono attribuite al numero 641 di avvii delle applicazioni. Già sai che cinque di queste conversioni sono attribuite a un click-through con visualizzazione dell’ultimo contatto e 19 a un view-through con visualizzazione dell’ultimo contatto. Rimangono ancora 617 avvii di applicazioni attribuiti ad altri canali di marketing. Puoi trascinare e rilasciare la dimensione Last Touch Channel (Canale di ultimo contatto) sopra la voce Advertising DSP per visualizzare l’attribuzione del canale per il resto di Applications Starts (Avvio applicazioni) e mostrare l’impatto cross-channel del canale di visualizzazione.

![come aggiungere la dimensione Canale di ultimo contatto](/help/integrations/assets/a4adc-mc-display-impact-ltc.png)

Ora puoi vedere come vengono attribuiti gli altri avvii delle applicazioni. All’e-mail viene assegnato il merito per 357 avvii delle applicazioni di ultimo contatto per i quali è persistito un AMO ID. Utilizzando questo tipo di analisi, puoi vedere l’impatto che gli annunci display di Adobe Advertising hanno avuto su tutti i canali. Con un solo set di dati e modello di attribuzione, questo tipo di informazioni non sarebbe disponibile.

![esempio dell’impatto cross-channel dei canali di visualizzazione](/help/integrations/assets/a4adc-mc-display-impact-x-channel.png)

Puoi migliorare ulteriormente l’analisi utilizzando un grafico a stack impostato su &quot;Sovrapposizione 100%&quot; per mostrare i dati con tendenze nel tempo. Questa visualizzazione consente di monitorare più facilmente quali canali di marketing di ultimo contatto sono più fortemente interessati dalle campagne di marketing display.

![esempio dell’impatto cross-channel con tendenze dei canali di visualizzazione](/help/integrations/assets/a4adc-mc-display-impact-x-channel-trend.png)

>[!MORELIKETHIS]
>
>* [Nozioni di base di [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [Utilizzo degli ID Adobe Advertising per la creazione [!DNL Marketing Channels] Regole di elaborazione](mc-ids.md)
>* [Perché i dati dei canali possono variare tra la pubblicità Adobe e [!DNL Marketing Channels]](mc-data-variances.md)
>* [Video: Utilizzo [!DNL Marketing Channels] ad Adobe Advertising Reporting](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-reporting-a4adc.html)
>* [Panoramica di [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)

