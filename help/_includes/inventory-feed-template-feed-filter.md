---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 0%

---
# Modello di annuncio testuale - Filtro feed

**\[Filtro feed\]:** Quali righe del file di feed propagare:

* *[!UICONTROL Propagate all rows found in feed:]* (Impostazione predefinita) Per propagare i dati per tutte le righe.

* *[!UICONTROL Propagate rows that meet certain conditions:]* Per propagare i dati solo per le righe che soddisfano fino a dieci condizioni specificate. Specifica i filtri da applicare:

   1. Seleziona l’operazione booleana da utilizzare per tutti i filtri:  **[!UICONTROL AND]** o **[!UICONTROL OR]**.

   1. Selezionare un nome di colonna dal primo menu, selezionare un operatore dal secondo menu, quindi immettere i valori applicabili o lasciare vuoto il campo di input per propagare i dati per le righe senza condizioni.

   L’elenco delle colonne include tutte le colonne disponibili nel feed.

   Gli operatori disponibili includono *[!UICONTROL contains]*, *[!UICONTROL does not contain]*, *[!UICONTROL =]*, *[!UICONTROL <>]* (non è uguale a), *[!UICONTROL in]*, *[!UICONTROL not in]*, *[!UICONTROL less than]*, e *[!UICONTROL greater than]*. Quando selezioni l’operatore &quot;[!UICONTROL in],&quot; è possibile immettere un elenco di valori separati da virgole; se un record corrisponde a uno qualsiasi dei valori specificati, i dati vengono propagati per tali righe. Per tutti gli altri operatori, immettere un solo valore. I valori non fanno distinzione tra maiuscole e minuscole.

   Ad esempio, se hai selezionato la colonna &quot;product_type&quot; e desideri restituire solo le righe per i nomi di prodotto contenenti &quot;shoes&quot;, seleziona &quot;**[!UICONTROL contains]**&quot; ed entra `shoes` nel campo di input.

   1. Per applicare fino a nove filtri aggiuntivi, fai clic su **[!UICONTROL Add Condition]**, quindi specificare il filtro aggiuntivo per il passaggio 2.
