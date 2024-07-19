---
source-git-commit: a59b477a6f8a616851d85bf89b58434d4d56cd83
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 0%

---
# Visualizzare i campi Percorso 1 e Percorso 2 in alcune impostazioni degli annunci

**[!UICONTROL Display Path 1]**, **[!UICONTROL Display Path 2]:** (Facoltativo) Testo aggiunto all&#39;URL di visualizzazione che viene estratto automaticamente dall&#39;URL finale. Ogni percorso è preceduto nell&#39;URL da una barra (`/`). Un percorso non può contenere una barra (`/`) o caratteri di nuova riga (`\n`). La lunghezza massima per ogni percorso è di 15 caratteri o 7 caratteri a doppio byte.

Per inserire un ad customizer, utilizzare i formati seguenti, dove `Default text` è un valore facoltativo da inserire quando il file di feed non include un valore valido:

* [!DNL Google Ads]: `{CUSTOMIZER.AdCustomizerName:Default text}, such as {CUSTOMIZER.Discount:10%}`

* [!DNL Microsoft Advertising]: `{CUSTOMIZER.Attribute name:Default text}, such as {CUSTOMIZER.Discount:10%}`

Ad esempio, se [!UICONTROL Display Path 1] è &quot;offerte&quot; e [!UICONTROL Display Path 2] è &quot;locale&quot;, l&#39;URL di visualizzazione sarà `<display URL>/deals/local`, ad esempio www.example.com/deals/local.
