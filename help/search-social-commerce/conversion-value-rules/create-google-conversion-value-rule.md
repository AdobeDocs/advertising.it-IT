---
title: 'Crea una regola del valore di conversione  [!DNL Google Ads] '
description: Scopri come creare  [!DNL Google Ads] regole del valore di conversione.
source-git-commit: efb4b80337b36b3b631898ca9ed66e99227468f1
workflow-type: tm+mt
source-wordcount: '445'
ht-degree: 0%

---

# Crea una regola del valore di conversione [!DNL Google Ads]

È possibile creare regole del valore di conversione a livello di account e di campagna in [!DNL Google Ads] account per i quali vengono tracciate le conversioni a livello di singolo account o inferiore. Non è possibile creare regole per i conti con conversioni tra conti diversi che vengono tracciati a livello di conto principale.

Ogni regola include fino a due condizioni, nonché l’adeguamento del valore di conversione da applicare quando le condizioni vengono soddisfatte. Tutte le regole in un account devono utilizzare lo stesso tipo di condizioni primarie e (facoltative) secondarie. Ad esempio, se la regola 1 include la condizione primaria &quot;Pubblico&quot; e la condizione secondaria &quot;Posizione&quot;, tutte le altre regole nell’account devono avere la condizione principale &quot;Pubblico&quot;. Quando le altre regole includono una condizione secondaria, deve essere &quot;Posizione&quot;.

Puoi creare più regole a livello di campagna per ogni campagna. Tuttavia, [!DNL Google Ads] non consente ancora di creare nuove regole a livello di account al di fuori dell&#39;editor [!DNL Google Ads] quando esiste già una regola a livello di account. Per creare regole aggiuntive a livello di account, accedere direttamente a [!DNL Google Ads] e utilizzare l&#39;editor [!DNL Google Ads].

**Nota:** le regole del valore di conversione a livello di campagna hanno la precedenza sulle regole a livello di account e a una conversione è possibile applicare una sola regola. Per ulteriori informazioni, vedere [come [!DNL Google Ads] determina quale regola viene applicata a una conversione quando questa soddisfa le condizioni per più regole](https://support.google.com/google-ads/answer/10520348).

1. Nel menu principale, fare clic su **[!UICONTROL Goals]>[!UICONTROL Conversion Value Rules]**.

   Per impostazione predefinita, la scheda **[!UICONTROL Campaign]** è selezionata per mostrare tutte le regole a livello di campagna.

1. (Facoltativo) Per creare una regola a livello di account, fare clic sulla scheda **[!UICONTROL Account]**.

1. Nella barra degli strumenti, fai clic su ![Crea](/help/search-social-commerce/assets/add.png "Crea").<!-- Upload newer icon -->

1. Seleziona la rete di annunci e l’account. Per le regole a livello di campagna, seleziona anche la campagna. Quindi fare clic su **[!UICONTROL Next]**.

1. Configura le [impostazioni della regola di conversione](google-conversion-value-rule-settings.md).

   Devi configurare una condizione primaria e una regolazione del valore. Facoltativamente, puoi configurare una condizione secondaria.

   All’interno di una condizione, più destinazioni o esclusioni vengono unite utilizzando l’operatore booleano OR, in modo che possa essere soddisfatta qualsiasi opzione per avviare una regolazione del valore. Quando si include una condizione secondaria, la condizione secondaria viene unita alla condizione principale utilizzando l&#39;operatore booleano ALL, in modo che entrambe le condizioni debbano essere soddisfatte per avviare una regolazione del valore. Esempio: se \[Location is Algeria OR Tunisia\] AND \[Device is Mobile OR Tablet\], aggiungere 1.5.

   **Nota:** tutte le regole in un account devono utilizzare lo stesso tipo di condizioni primarie e (facoltative) secondarie. Ad esempio, se la regola 1 include la condizione primaria &quot;Pubblico&quot; e la condizione secondaria &quot;Posizione&quot;, tutte le altre regole nell’account devono avere la condizione principale &quot;Pubblico&quot;. Quando le altre regole includono una condizione secondaria, deve essere &quot;Posizione&quot;.

1. Fare clic su **[!UICONTROL Review and Save]** per rivedere le impostazioni.

1. Fare clic su **[!UICONTROL Save]**.

>[!MORELIKETHIS]
>
>* [Informazioni su [!DNL Google Ads] regole del valore di conversione](about-google-conversion-value-rules.md)
>* [Modifica una [!DNL Google Ads] regola del valore di conversione](edit-google-conversion-value-rule.md)
>* [Modifica lo stato di una  [!DNL Google Ads] regola del valore di conversione](change-the-status-of-google-conversion-value-rule.md)
>* [[!DNL Google Ads] impostazioni regola del valore di conversione](google-conversion-value-rule-settings.md)

