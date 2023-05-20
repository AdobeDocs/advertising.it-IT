---
title: Filtri pre-offerta a livello di posizionamento e come utilizzarli
description: Fai riferimento ai filtri pre-offerta a livello di posizionamento disponibili e scopri come utilizzarli.
feature: DSP Optimization
exl-id: 34a15666-7ca2-416d-9064-8638ca81e5b3
source-git-commit: 7e614ecb517515217d812926f61ca10437820efd
workflow-type: tm+mt
source-wordcount: '445'
ht-degree: 0%

---

# Filtri pre-offerta a livello di posizionamento e come utilizzarli

| Filtro pre-offerta | Descrizione | Quando utilizzare questo filtro |
| ---------------| ----------- | ---------------------- |
| [!UICONTROL Click Through Rate] | Imposta una soglia minima di previsione per la probabilità che un&#39;asta dia luogo a un click-through. Ad esempio, se imposti la soglia allo 0,1%, non invierai un&#39;offerta per un&#39;asta a meno che la probabilità prevista di un clic non sia maggiore o uguale allo 0,1%.<br><br><b>Nota:</b> I filtri vengono applicati prima degli obiettivi di ottimizzazione. Di conseguenza, filtri molto rigidi possono evitare la spesa. | Utilizzare quando si dispone di un obiettivo KPI minimo per il tasso di click-through (CTR) e non si desidera spendere il budget quando il CTR è inferiore alla soglia. Questo filtro può essere piuttosto restrittivo, quindi è importante fissare obiettivi realistici. A seconda di altre restrizioni sul posizionamento, un obiettivo di 0,03-0,07% è generalmente un buon punto di partenza. Puoi ottimizzarlo a livello di sito in base alle esigenze per migliorare le metriche.<br><br>Se il tuo obiettivo è quello di ottenere un CTR minimo e il CPM migliore possibile, allora la configurazione consigliata è quella di combinare [!UICONTROL Click Through Rate] filtrare con l’obiettivo di ottimizzazione &quot;[!UICONTROL Lowest CPM].&quot; Se il tuo obiettivo è un CPM massimo senza vantaggi reali per il superamento del limite e un CTR minimo, allora associando un [!UICONTROL Click Through Rate] filtrare con l’obiettivo di ottimizzazione &quot;[!UICONTROL Always Max Bid + Highest CTR]&quot; può essere più appropriato. |
| [!UICONTROL 100% Completion Rate] | Imposta la percentuale di completamento minima richiesta che deve essere soddisfatta prima di fare un&#39;offerta per un&#39;impression. | Utilizza questo filtro quando l’obiettivo principale della campagna è la percentuale di completamento. Fattore in altri parametri di targeting, ma il 65% è la percentuale iniziale consigliata. |
| [!UICONTROL Player Size - Adobe] | Imposta la dimensione minima del lettore richiesta, utilizzando i dati dell&#39;DSP. Farai un&#39;offerta per un&#39;impression quando [!UICONTROL Player Size] soglia è raggiunta. | Utilizza per assicurarti di eseguire la consegna dell’inventario completo dei lettori di episodi utilizzando i dati provenienti dall’DSP. |
| [!UICONTROL Player Size 3rdParty (Moat/IAS)] | Imposta la dimensione minima del lettore richiesta, utilizzando i dati di [!DNL Moat] o [!DNL Integral Ad Science] ([!DNL IAS]). Farai un&#39;offerta per un&#39;impression quando [!UICONTROL Player Size] soglia è raggiunta. | Utilizza per assicurarti di eseguire la consegna dell’inventario completo dei lettori di episodi utilizzando a livello di piattaforma [!DNL Moat] o [!DNL IAS] dati.<br><br><b>Nota:</b> Usa questo filtro solo quando la campagna è configurata per l’utilizzo [!DNL Moat] o [!DNL IAS] dati. |
| [!UICONTROL Viewability Adobe (MRC or [!DNL GroupM])] | Imposta la percentuale minima di visualizzabilità richiesta, utilizzando i numeri e le misurazioni di visualizzabilità DSP. Farai un&#39;offerta per un&#39;impression quando viene raggiunta la soglia specificata.<br><br><b>Note:</b><ul><li>Se la campagna [!UICONTROL Viewability Sensitivity] l&#39;impostazione è &quot;[!UICONTROL Standard (50% of ad in view for 2 consecutive seconds)],&quot; quindi il [!DNL Media Rating Council] (MRC) per la campagna viene utilizzato lo standard di misurazione della visualizzabilità. Se il [!UICONTROL Viewability Sensitivity] l&#39;impostazione è &quot;[!UICONTROL Strict (100% of ad in view & audio on for 50% duration)],&quot; quindi il [!DNL GroupM] per la campagna viene utilizzato lo standard di misurazione della visualizzabilità.</li><li>Le definizioni di misura di Adobe differiscono dalle definizioni di terze parti, pertanto potrebbero esserci lievi discrepanze con i dati di terze parti.</li></ul> | La best practice prevede di abbinare l’obiettivo di ottimizzazione ed eventuali impostazioni di filtro pre-offerta a quelle della campagna [!UICONTROL Viewability Sensitivity] impostazione. |

{style="table-layout:auto"}

>[!MORELIKETHIS]
>
>* [Come l’DSP ottimizza le campagne](optimization-how-dsp-optimizes-campaigns.md)
>* [Impostazioni pacchetto](/help/dsp/campaign-management/packages/package-settings.md)
>* [Impostazioni di posizionamento](/help/dsp/campaign-management/placements/placement-settings.md)
>* [Impostazioni campagna](/help/dsp/campaign-management/campaigns/campaign-settings.md)
>* [Obiettivi di ottimizzazione e modalità di utilizzo](optimization-goals.md)

