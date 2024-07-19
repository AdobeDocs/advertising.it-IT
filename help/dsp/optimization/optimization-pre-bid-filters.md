---
title: Filtri pre-offerta a livello di posizionamento e come utilizzarli
description: Fai riferimento ai filtri pre-offerta a livello di posizionamento disponibili e scopri come utilizzarli.
feature: DSP Optimization
exl-id: 34a15666-7ca2-416d-9064-8638ca81e5b3
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '452'
ht-degree: 0%

---

# Filtri pre-offerta a livello di posizionamento e come utilizzarli

| Filtro pre-offerta | Descrizione | Quando utilizzare questo filtro |
| ---------------| ----------- | ---------------------- |
| [!UICONTROL Click Through Rate] | Imposta una soglia minima di previsione per la probabilità che un&#39;asta possa dar luogo a un click-through. Ad esempio, se imposti la soglia allo 0,1%, fai un&#39;offerta per le aste solo quando la probabilità prevista di un clic è maggiore o uguale allo 0,1%.<br><br><b>Nota:</b> i filtri vengono applicati prima degli obiettivi di ottimizzazione. Di conseguenza, filtri molto rigidi possono evitare la spesa. | Utilizzare quando si dispone di un obiettivo KPI minimo per il tasso di click-through (CTR) e non si desidera spendere il budget quando il CTR è inferiore alla soglia. Questo filtro può essere piuttosto restrittivo, quindi è importante fissare obiettivi realistici. A seconda di altre restrizioni sul posizionamento, un obiettivo di 0,03-0,07% è generalmente un buon punto di partenza. Puoi ottimizzarlo a livello di sito in base alle esigenze per migliorare le metriche.<br><br>Se l&#39;obiettivo è quello di ottenere un CTR minimo e il CPM migliore possibile, è consigliabile combinare un filtro [!UICONTROL Click Through Rate] con l&#39;obiettivo di ottimizzazione &quot;[!UICONTROL Lowest CPM]&quot;.&quot; Se l&#39;obiettivo è un CPM massimo senza vantaggi reali per il superamento dei limiti e un CTR minimo, potrebbe essere più appropriato associare un filtro [!UICONTROL Click Through Rate] all&#39;obiettivo di ottimizzazione &quot;[!UICONTROL Always Max Bid + Highest CTR]&quot;. |
| [!UICONTROL 100% Completion Rate] | Imposta la percentuale di completamento minima richiesta che deve essere soddisfatta prima di fare un&#39;offerta per un&#39;impression. | Utilizza questo filtro quando l’obiettivo principale della campagna è la percentuale di completamento. Fattore in altri parametri di targeting, ma il 65% è la percentuale iniziale consigliata. |
| [!UICONTROL Player Size - Adobe] | Imposta la dimensione minima del lettore richiesta, utilizzando i dati dell&#39;DSP. Puoi fare un&#39;offerta per un&#39;impression quando viene raggiunta la soglia di [!UICONTROL Player Size]. | Utilizza per assicurarti di eseguire la consegna dell’inventario completo dei lettori di episodi utilizzando i dati provenienti dall’DSP. |
| [!UICONTROL Player Size 3rdParty (Moat/IAS)] | Imposta la dimensione minima del lettore richiesta, utilizzando i dati di [!DNL Moat] o [!DNL Integral Ad Science] ([!DNL IAS]). Puoi fare un&#39;offerta per un&#39;impression quando viene raggiunta la soglia di [!UICONTROL Player Size]. | Utilizza per assicurarti di eseguire la consegna dell&#39;inventario completo degli episodi del lettore utilizzando dati [!DNL Moat] o [!DNL IAS] a livello di piattaforma.<br><br><b>Nota:</b> utilizzare questo filtro solo quando la campagna è configurata per l&#39;utilizzo di dati [!DNL Moat] o [!DNL IAS]. |
| [!UICONTROL Viewability Adobe (MRC or [!DNL GroupM])] | Imposta la percentuale minima di visualizzabilità richiesta, utilizzando i numeri e le misurazioni di visualizzabilità DSP. Puoi fare un&#39;offerta per un&#39;impression quando viene raggiunta la soglia specificata.<br><br><b>Note:</b><ul><li>Se l&#39;impostazione [!UICONTROL Viewability Sensitivity] della campagna è &quot;[!UICONTROL Standard (50% of ad in view for 2 consecutive seconds)]&quot;, per la campagna viene utilizzato lo standard di misurazione della visualizzabilità [!DNL Media Rating Council] (MRC). Se l&#39;impostazione [!UICONTROL Viewability Sensitivity] è &quot;[!UICONTROL Strict (100% of ad in view & audio on for 50% duration)]&quot;, per la campagna viene utilizzato lo standard di misurazione della visualizzabilità [!DNL GroupM].</li><li>Le definizioni di misura di Adobe differiscono dalle definizioni di terze parti, pertanto potrebbero esserci lievi discrepanze con i dati di terze parti.</li></ul> | La best practice prevede di abbinare l&#39;obiettivo di ottimizzazione ed eventuali impostazioni del filtro pre-offerta all&#39;impostazione [!UICONTROL Viewability Sensitivity] della campagna. |

{style="table-layout:auto"}

>[!MORELIKETHIS]
>
>* [Come DSP Ottimizza Le Campagne](optimization-how-dsp-optimizes-campaigns.md)
>* [Impostazioni pacchetto](/help/dsp/campaign-management/packages/package-settings.md)
>* [Impostazioni posizionamento](/help/dsp/campaign-management/placements/placement-settings.md)
>* [Impostazioni campagna](/help/dsp/campaign-management/campaigns/campaign-settings.md)
>* [Obiettivi di ottimizzazione e modalità di utilizzo](optimization-goals.md)
