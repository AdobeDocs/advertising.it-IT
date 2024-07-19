---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 0%

---
# Campo Descrizioni annunci nelle impostazioni degli annunci RSA

**[!UICONTROL Ad Descriptions]:** almeno due e fino a quattro descrizioni di annunci con puntini di posizione facoltativi. La rete di annunci visualizza annunci con un massimo di due descrizioni; immetti almeno due. La lunghezza massima per ogni descrizione è di 90 caratteri, incluso qualsiasi testo dinamico (come i valori delle parole chiave e delle personalizzazioni di annunci).

Per inserire un ad customizer, utilizzare i formati seguenti, dove `Default text` è un valore facoltativo da inserire quando il file di feed non include un valore valido:

* [!DNL Google Ads]: `{CUSTOMIZER.AdCustomizerName:Default text}, such as {CUSTOMIZER.Discount:10%}`

* [!DNL Microsoft Advertising]: `{CUSTOMIZER.Attribute name:Default text}, such as {CUSTOMIZER.Discount:10%}`

Per fissare una descrizione a una posizione specifica, selezionare l&#39;opzione di fissaggio, ad esempio &quot;[!UICONTROL Pinned at position 1]&quot;. Per ogni posizione deve essere disponibile almeno una descrizione. Se si fissano più descrizioni alla stessa posizione, l&#39;annuncio finale include sempre una di queste descrizioni nella posizione specificata. Le descrizioni fissate alla posizione 2 potrebbero non essere visualizzate con l’annuncio.

Per aggiungere una descrizione aggiuntiva, fare clic su **[!UICONTROL + Add]**.
