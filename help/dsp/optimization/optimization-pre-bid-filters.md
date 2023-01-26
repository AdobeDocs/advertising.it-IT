---
title: Filtri di pre-offerta a livello di posizionamento e modalità di utilizzo
description: Fai riferimento ai filtri pre-bid a livello di posizionamento disponibili e scopri come utilizzarli.
feature: DSP Optimization
exl-id: c699e970-84ca-429b-8062-81804e6c9f21
source-git-commit: 1c13874967ec4ad264e5fa6a5e0dfeb6120f53cc
workflow-type: tm+mt
source-wordcount: '448'
ht-degree: 0%

---

# Filtri di pre-offerta a livello di posizionamento e modalità di utilizzo

| Filtro pre-offerta | Descrizione | Quando utilizzare questo filtro |
| ---------------| ----------- | ---------------------- |
| [!UICONTROL Click Through Rate] | Imposta una soglia di previsione minima per la probabilità che un&#39;asta si traduca in un click-through. Ad esempio, se imposti la soglia su 0,1%, non invierai un’offerta su un’asta a meno che la probabilità prevista di un clic non sia maggiore o uguale a 0,1%.<br><br><b>Nota:</b> I filtri vengono applicati prima degli obiettivi di ottimizzazione. Di conseguenza, filtri molto rigidi possono impedire la spesa. | Da utilizzare quando si dispone di un obiettivo KPI minimo per il CTR (click-through rate) e non si desidera spendere il budget quando il CTR è al di sotto della soglia. Questo filtro può essere piuttosto restrittivo, quindi è importante stabilire obiettivi realistici. A seconda di altre restrizioni al posizionamento, un obiettivo dello 0,03-07% è generalmente un buon punto di partenza. Puoi ottimizzarlo a livello di sito in base alle esigenze per migliorare le metriche.<br><br>Se l&#39;obiettivo è quello di raggiungere un CTR minimo e il miglior CPM possibile, allora la configurazione consigliata è quella di combinare un [!UICONTROL Click Through Rate] filtro con obiettivo di ottimizzazione &quot;[!UICONTROL Lowest CPM].&quot; Se il tuo obiettivo è un CPM massimo senza nessun reale vantaggio per il superamento, e un CTR minimo, allora accoppiare un [!UICONTROL Click Through Rate] filtro con obiettivo di ottimizzazione &quot;[!UICONTROL Always Max Bid + Highest CTR]&quot; può essere più appropriato. |
| [!UICONTROL 100% Completion Rate] | Imposta un tasso di completamento minimo richiesto che deve essere soddisfatto prima di fare un&#39;offerta su un&#39;impression. | Utilizza questo filtro quando l’obiettivo principale della campagna sono i tassi di completamento. Fattore in altri parametri di targeting, ma 65% è la percentuale iniziale consigliata. |
| [!UICONTROL Player Size - Adobe] | Imposta la dimensione minima richiesta del lettore, utilizzando i dati di DSP. Farai un&#39;offerta su un&#39;impression quando il [!UICONTROL Player Size] è soddisfatta la soglia. | Utilizza per assicurarti di fornire l&#39;inventario del lettore full-episode utilizzando i dati di DSP. |
| [!UICONTROL Player Size 3rdParty (Moat/IAS)] | Imposta la dimensione minima richiesta per il lettore, utilizzando i dati di [!DNL Moat] o [!DNL Integral Ad Science] ([!DNL IAS]). Farai un&#39;offerta su un&#39;impression quando il [!UICONTROL Player Size] è soddisfatta la soglia. | Utilizza per assicurarti di fornire un inventario completo del lettore a episodio utilizzando la piattaforma [!DNL Moat] o [!DNL IAS] dati.<br><br><b>Nota:</b> Usa questo filtro solo quando la campagna è configurata per l’utilizzo [!DNL Moat] o [!DNL IAS] dati. |
| [!UICONTROL Viewability Adobe (MRC or [!DNL GroupM])] | Imposta una percentuale minima di visualizzabilità richiesta, utilizzando DSP numeri e misure di visualizzabilità. Puoi fare un’offerta su un’impression quando viene soddisfatta la soglia specificata.<br><br><b>Note:</b><ul><li>Se la campagna è [!UICONTROL Viewability Sensitivity] l&#39;impostazione è &quot;[!UICONTROL Standard (50% of ad in view for 2 consecutive seconds)],&quot; quindi il [!DNL Media Rating Council] (MRC) Lo standard di misurazione della visualizzabilità viene utilizzato per la campagna. Se la [!UICONTROL Viewability Sensitivity] l&#39;impostazione è &quot;[!UICONTROL Strict (100% of ad in view & audio on for 50% duration)],&quot; quindi il [!DNL GroupM] per la campagna viene utilizzato lo standard di misurazione della visualizzabilità.</li><li>Le definizioni di misurazione di Adobe differiscono da quelle di terze parti, pertanto potrebbero esserci lievi discrepanze con i dati di terze parti.</li></ul> | La best practice consigliata consiste nell’abbinare l’obiettivo di ottimizzazione e le impostazioni di filtro pre-offerta a quelle della campagna [!UICONTROL Viewability Sensitivity] impostazione. |

{style=&quot;table-layout:auto&quot;}

>[!MORELIKETHIS]
>
>* [Ottimizzazione DSP campagne](optimization-how-dsp-optimizes-campaigns.md)
>* [Impostazioni pacchetto](/help/dsp/campaign-management/packages/package-settings.md)
>* [Impostazioni di posizionamento](/help/dsp/campaign-management/placements/placement-settings.md)
>* [Impostazioni di Campaign](/help/dsp/campaign-management/campaigns/campaign-settings.md)
>* [Obiettivi di ottimizzazione e come utilizzarli](optimization-goals.md)

