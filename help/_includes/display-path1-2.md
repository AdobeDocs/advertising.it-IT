---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 0%

---
# Visualizzare i campi Percorso 1 e Percorso 2 in alcune impostazioni degli annunci

**[!UICONTROL Display Path 1]**, **[!UICONTROL Display Path 2]:** (Facoltativo) Testo aggiunto all&#39;URL di visualizzazione che viene estratto automaticamente dall&#39;URL finale. Ogni percorso è preceduto nell’URL da una barra (`/`). Un percorso non può contenere una barra (`/`) o nuova riga (`\n`) caratteri. La lunghezza massima per ogni percorso è di 15 caratteri o 7 caratteri a doppio byte.

Per inserire un ad customizer, usa i seguenti formati, dove `Default text` è un valore facoltativo da inserire quando il file di feed non include un valore valido:

* [!DNL Google Ads]: `{CUSTOMIZER.AdCustomizerName:Default text}, such as {CUSTOMIZER.Discount:10%}`

* [!DNL Microsoft Advertising]: `{CUSTOMIZER.Attribute name:Default text}, such as {CUSTOMIZER.Discount:10%}`

Ad esempio, se il percorso di visualizzazione 1 è &quot;offerte&quot; e il percorso di visualizzazione 2 è &quot;locale&quot;, l’URL di visualizzazione sarà `<display URL>/deals/local`, ad esempio www.example.com/deals/local.
