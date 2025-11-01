---
source-git-commit: 73c9cc7134360e073fc466dda3733cfc9bac8786
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 0%

---
# Modello di annuncio testuale - Filtro feed

**\[Filtro feed\]:** Quali righe nel file di feed propagare:

* *[!UICONTROL Propagate all rows found in feed:]* (impostazione predefinita) Per propagare i dati per tutte le righe.

* *[!UICONTROL Propagate rows that meet certain conditions:]* Per propagare i dati solo per le righe che soddisfano fino a dieci condizioni specificate. Specifica i filtri da applicare:

   1. Selezionare l&#39;operazione booleana da utilizzare per tutti i filtri: **[!UICONTROL AND]** o **[!UICONTROL OR]**.

   1. Selezionare un nome di colonna dal primo menu, selezionare un operatore dal secondo menu, quindi immettere i valori applicabili o lasciare vuoto il campo di input per propagare i dati per le righe senza condizioni.

  L’elenco delle colonne include tutte le colonne disponibili nel feed.

  Gli operatori disponibili includono *[!UICONTROL contains]*, *[!UICONTROL does not contain]*, *[!UICONTROL =]*, *[!UICONTROL <>]* (non è uguale a), *[!UICONTROL in]*, *[!UICONTROL not in]*, *[!UICONTROL less than]* e *[!UICONTROL greater than]*. Quando si seleziona l&#39;operatore &quot;[!UICONTROL in]&quot;, è possibile immettere un elenco di valori separati da virgole. Se un record corrisponde a uno dei valori specificati, i dati vengono propagati per tali righe. Per tutti gli altri operatori, immettere un solo valore. I valori non fanno distinzione tra maiuscole e minuscole.

  Ad esempio, se si seleziona la colonna &quot;product_type&quot; e si desidera restituire solo le righe per i nomi di prodotto contenenti &quot;shoes&quot;, selezionare &quot;**[!UICONTROL contains]**&quot; e immettere `shoes` nel campo di input.

   1. (Per applicare fino a nove filtri aggiuntivi) Per ogni filtro aggiuntivo, fare clic su **[!UICONTROL Add Condition]** e quindi specificare il filtro aggiuntivo per il passaggio 2.
