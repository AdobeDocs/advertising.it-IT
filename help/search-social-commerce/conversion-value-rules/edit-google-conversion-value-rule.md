---
title: 'Modifica una regola del valore di conversione  [!DNL Google Ads] '
description: Scopri come modificare le  [!DNL Google Ads] regole del valore di conversione.
source-git-commit: efb4b80337b36b3b631898ca9ed66e99227468f1
workflow-type: tm+mt
source-wordcount: '259'
ht-degree: 0%

---

# Modifica una regola del valore di conversione [!DNL Google Ads]

Puoi modificare una regola del valore di conversione in account/campagne per i quali le conversioni vengono tracciate a livello di singolo account o inferiore. Non è possibile modificare una regola per un account con conversioni tra account diversi che vengono tracciate a livello di account principale.

1. Nel menu principale, fare clic su **[!UICONTROL Goals]>[!UICONTROL Conversion Value Rules]**.

   Per impostazione predefinita, la scheda **[!UICONTROL Campaign]** è selezionata per mostrare tutte le regole a livello di campagna.

1. (Facoltativo) Per visualizzare tutte le regole a livello di account, fare clic sulla scheda **[!UICONTROL Account]**.

1. Selezionare la casella di controllo accanto alla regola.

1. Nella barra degli strumenti delle azioni in blocco,

   * Per attivare (abilitare) le regole in pausa, fare clic su (/help/search-social-commerce/assets/edit-new.png &quot;Modifica&quot;).

1. Modifica le [impostazioni della regola di conversione](google-conversion-value-rule-settings.md).

   Non è possibile modificare i tipi di condizione per una regola esistente, ma è possibile modificare le condizioni e le regolazioni dei valori.

   Devi configurare una condizione primaria e una regolazione del valore. Facoltativamente, puoi configurare una condizione secondaria.

   **Nota:** se si aggiunge una condizione secondaria, questa deve essere dello stesso tipo di condizione delle altre regole nell&#39;account. Ad esempio, se la regola 1 altre regole nel conto hanno la condizione secondaria &quot;Ubicazione&quot;, quando le altre regole includono una condizione secondaria, la condizione secondaria deve essere &quot;Ubicazione&quot;. Quando si include una condizione secondaria, la condizione secondaria viene unita alla condizione principale utilizzando l&#39;operatore booleano ALL, in modo che entrambe le condizioni debbano essere soddisfatte per avviare una regolazione del valore.

1. Fare clic su **[!UICONTROL Review and Save]** per rivedere le impostazioni.

1. Fare clic su **[!UICONTROL Save]**.

>[!MORELIKETHIS]
>
>* [Informazioni su [!DNL Google Ads] regole del valore di conversione](about-google-conversion-value-rules.md)
>* [Crea una [!DNL Google Ads] regola del valore di conversione](create-google-conversion-value-rule.md)
>* [Modifica lo stato di una  [!DNL Google Ads] regola del valore di conversione](change-the-status-of-google-conversion-value-rule.md)
>* [[!DNL Google Ads] impostazioni regola del valore di conversione](google-conversion-value-rule-settings.md)

