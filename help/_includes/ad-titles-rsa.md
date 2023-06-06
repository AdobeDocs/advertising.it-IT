---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 0%

---
# Campo Titoli annuncio nelle impostazioni annuncio RSA

**[!UICONTROL Ad Titles]:** Almeno tre e fino a quindici titoli di annunci (titoli), con pin di posizione opzionali. La rete di annunci visualizza annunci con un massimo di tre titoli; immetti almeno tre titoli. La lunghezza massima per ogni titolo è di 30 caratteri, incluso qualsiasi testo dinamico (come i valori delle parole chiave e delle personalizzazioni di annunci).

Per inserire un ad customizer, usa i seguenti formati, dove `Default text` è un valore facoltativo da inserire quando il file di feed non include un valore valido:

* [!DNL Google Ads]: `{CUSTOMIZER.AdCustomizerName:Default text}, such as {CUSTOMIZER.Discount:10%}`

* [!DNL Microsoft Advertising]: `{CUSTOMIZER.Attribute name:Default text}, such as {CUSTOMIZER.Discount:10%}`

Per fissare un titolo a una posizione specifica, seleziona l’opzione pin (ad esempio &quot;[!UICONTROL Pinned at position 1]&quot;). Per ogni posizione deve essere disponibile almeno un titolo. Se si fissano più titoli nella stessa posizione, l&#39;annuncio finale includerà sempre uno di questi titoli nella posizione specificata. I titoli fissati alla posizione 3 potrebbero non essere visualizzati con l’annuncio.

Per aggiungere un titolo aggiuntivo, fai clic su **[!UICONTROL + Add]**.
