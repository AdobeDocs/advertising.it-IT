---
title: Utilizzo [!DNL Marketing Channels] con i dati pubblicitari di Adobe
description: Scopri come utilizzare i dati pubblicitari di Adobe in [!DNL Analytics Marketing Channels].
feature: Integration with Adobe Analytics
exl-id: c9403a03-58aa-4633-bb97-51afc30843ad
source-git-commit: 1c13874967ec4ad264e5fa6a5e0dfeb6120f53cc
workflow-type: tm+mt
source-wordcount: '708'
ht-degree: 0%

---

# Utilizzo [!DNL Analytics Marketing Channels] con i dati pubblicitari di Adobe

*Inserzionisti con una sola integrazione Advertising-Adobe Analytics di Adobe*

Utilizzando sia Adobe Advertising che [!DNL Analytics Marketing Channels] , puoi ottenere informazioni utili su come i contenuti multimediali digitali influenzano l’attività del sito.

<!-- from video: By using Marketing Channels with your Adobe Advertising data, you can get a more holistic view of how your advertising efforts are affecting site behavior. In particular, you can see the value of your view-through and click-through data, and how your advertising assists or is assisted by other channels. -->

La figura seguente illustra come Adobe Advertising e [!DNL Marketing Channels] tiene traccia delle singole visite che compongono il percorso di un visitatore. Report pubblicitari di Adobe in [!DNL Analytics] sono limitati solo alla visualizzazione a pagamento, alla ricerca, ai canali social e di e-commerce pubblicizzati trafficati tramite Adobe Advertising, utilizzando l’AMO ID. Tuttavia, [!DNL Marketing Channels] tiene traccia di tutti i canali configurati nel [!DNL Marketing Channels] Regole di elaborazione.

![Come Adobe Advertising e [!DNL Marketing Channels] tenere traccia delle singole visite nel percorso di un visitatore](/help/integrations/assets/a4adc-mc-sample-journey2.png)

Nella prima visita, l’utente è entrato nel sito web tramite una campagna e-mail, ha eseguito dieci visualizzazioni di pagina e poi è partito. Nella seconda visita, l’utente è entrato nel sito tramite un annuncio pubblicitario, ha eseguito dieci visualizzazioni di pagina e poi è partito. Nella terza visita, l’utente è entrato nel sito tramite ricerca naturale, ha eseguito cinque visualizzazioni di pagina, ha eseguito una conversione da $ 250 e la sinistra. Osserva la differenza nel tracciamento tra [!DNL Marketing Channels] e Adobe Advertising. L&#39;unico canale che Adobe Advertising tiene traccia in questo percorso è [!UICONTROL Display]. Adobe Advertising tiene traccia dei [!UICONTROL Display] visita del canale e attribuisce i dati di coinvolgimento successivi (come le visualizzazioni di pagina) e le conversioni di nuovo all&#39;influenza di quell&#39;annuncio. [!DNL Marketing Channels]d&#39;altra parte, offre una visione completa di tutti i canali.

Poiché l’AMO ID persiste attraverso il percorso del visitatore, puoi utilizzare i dati AMO ID per vedere in che modo Adobe Advertising influenza altri canali di marketing. AMO ID [persiste per 60 giorni per impostazione predefinita](/help/integrations/analytics/overview.md), ma puoi configurare la persistenza in base alle esigenze.

## Come combinare i dati di Adobe Advertising e Marketing Channels per analizzare le prestazioni dei file multimediali

Within [!DNL Analytics], è possibile combinare l&#39;Adobe Pubblicità persistente dati pubblicitari a pagamento e il [!DNL Marketing Channels] dati completi sulle visite per analizzare meglio le prestazioni dei contenuti multimediali in modo da poter influenzare meglio il percorso dei clienti.

L’analisi seguente utilizza i dati pubblicitari di Adobe per mostrare diverse versioni di come un annuncio pubblicitario influisce sulla conversione del sito. Tutte e tre le colonne utilizzano le stesse metriche di conversione, ma ogni colonna presenta una storia diversa:

* La colonna 1 esamina i dati AMO ID persistenti nel percorso del visitatore. La colonna 1 indica che 641 Applicazioni Starts erano, a un certo punto, collegate a un annuncio pubblicitario Adobe, tramite un evento view-through o click-through. Questa visualizzazione non ne ha altre [!DNL Marketing Channels] attribuzione in considerazione.

* In [!DNL Marketing Channels] set di dati, tuttavia, le 641 Applicazioni Starts sono attribuite ad altri canali di marketing. Le ultime due colonne prendono le 641 applicazioni Starts e limitano i dati al [!UICONTROL Display Click-Through] e [!UICONTROL Display View-Through] , che mostra le conversioni che si verificano in un modello di attribuzione ultimo contatto.

![esempio di impatto di un annuncio visualizzato sulla conversione del sito](/help/integrations/assets/a4adc-mc-display-impact.png)

Puoi fare un ulteriore passo avanti per questa analisi. Puoi suddividere ulteriormente la riga Pubblicità Adobe per canale di marketing per vedere dove le conversioni Pubblicitario Adobe sono attribuite alle 641 Applicazioni Starts. È già noto che cinque di queste conversioni sono attribuite a un ultimo click-through di visualizzazione touch e 19 sono attribuite a un ultimo display view-through. Ciò lascia ancora 617 applicazioni iniziali attribuite ad altri canali di marketing. Puoi trascinare e rilasciare la dimensione Last Touch Channel sopra l’elemento della riga Advertising DSP per visualizzare l’attribuzione del canale per il resto delle applicazioni Starts e mostrare l’impatto cross-channel del canale Display.

![come aggiungere la dimensione Last Touch Channel](/help/integrations/assets/a4adc-mc-display-impact-ltc.png)

Ora puoi vedere come vengono attribuiti gli avvii delle applicazioni rimanenti. All’e-mail viene assegnato un credito per 357 applicazioni di ultimo contatto Starts per i quali un AMO ID è persistito. Utilizzando questo tipo di analisi, puoi vedere l’impatto degli annunci display di Adobe Advertising su tutti i canali. Con un solo set di dati e un modello di attribuzione, questo tipo di informazioni non sarebbe disponibile.

![esempio dell&#39;impatto cross-channel dei canali di visualizzazione](/help/integrations/assets/a4adc-mc-display-impact-x-channel.png)

Puoi migliorare ulteriormente l’analisi utilizzando un grafico Stack impostato su &quot;100% impilato&quot; per mostrare i dati con tendenze nel tempo. Questa visualizzazione facilita il monitoraggio degli ultimi canali di marketing touch maggiormente interessati dalle campagne di marketing display.

![esempio dell&#39;impatto cross-channel con tendenze dei canali di visualizzazione](/help/integrations/assets/a4adc-mc-display-impact-x-channel-trend.png)

>[!MORELIKETHIS]
>
>* [Nozioni fondamentali di [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [Utilizzo degli ID pubblicitari di Adobe per creare [!DNL Marketing Channels] Regole di elaborazione](mc-ids.md)
>* [Perché i dati del canale possono variare tra la pubblicità Adobe e [!DNL Marketing Channels]](mc-data-variances.md)
>* [Video: Utilizzo [!DNL Marketing Channels] ad Adobe Advertising Reporting](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-reporting-a4adc.html)
>* [Panoramica [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)

