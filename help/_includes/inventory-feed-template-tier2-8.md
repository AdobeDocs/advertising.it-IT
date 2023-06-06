---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 0%

---
# Campi Livello 2 - Livello 8 nei modelli di annunci commerciali

**[!UICONTROL Tier  2 - Tier 8]:** (Quando si aggiungono livelli di gruppi di prodotti) Un tipo di attributo di prodotto in base al quale eseguire il targeting dei prodotti e i criteri di idoneità per il tipo di attributo selezionato (ad esempio, Brand=Acme o Condition=New). I valori vengono applicati gerarchicamente per determinare i prodotti idonei. Selezionare un tipo di attributo e inserire i criteri di idoneità. I caratteri non consentiti includono: `[ ] < > >>` (due segni &quot;maggiore di&quot; consecutivi), utilizzati per designare i nomi di colonna nel modello, i nomi dei modificatori nel modello e i separatori di livello nel [!UICONTROL Parent Product Grouping] colonna nei bulksheet.

Puoi includere fino a otto livelli di gruppi di prodotti, tra cui &quot;[!UICONTROL All Products]&quot; (Livello 1). Ogni livello può includere più gruppi di prodotti, ma devono appartenere allo stesso tipo di attributo (ad esempio &quot;Condizione&quot;).

>[!NOTE]
>
>* ([!DNL Google Ads] solo) I valori possibili per [!UICONTROL Channel] sono &quot;[!UICONTROL Local]&quot; o &quot;[!UICONTROL Online],&quot; e i possibili valori per [!UICONTROL ChannelExclusivity] sono &quot;[!UICONTROL SingleChannel]&quot; e &quot;[!UICONTROL MultiChannel].&quot;
>* Quando crei un gruppo di prodotti di secondo livello (figlio) per un gruppo di annunci dal [!UICONTROL Product Groups] scheda in [!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] view, un altro gruppo di prodotti, denominato &quot;[!UICONTROL Everything Else],&quot; viene creato automaticamente utilizzando l’offerta di gruppo di annunci predefinita. Tuttavia, è possibile utilizzare i modelli di feed inventario &quot;[!UICONTROL Everything Else]&quot;I gruppi di prodotti sono esclusi.
>* Se si includono più livelli e non è disponibile alcun valore per il livello finale (quello con il numero più alto), come gruppo di prodotti che è possibile fare offerte viene utilizzato il livello immediatamente superiore. Ad esempio, se includi cinque livelli e non è disponibile alcun valore per il livello 5, il livello 4 viene utilizzato come gruppo di prodotti (unità) che è possibile fare offerte. Tuttavia, se non è disponibile alcun valore per un livello intermedio, la riga viene ignorata. Ad esempio, se si includono cinque livelli e il livello 5 ha un valore ma il livello 4 non lo ha, la riga 4 viene ignorata.

