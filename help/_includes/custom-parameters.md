---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 0%

---
# Campo Parametri personalizzati nelle impostazioni delle campagne GGL e MS, nelle impostazioni dei gruppi di annunci MS e nelle impostazioni degli annunci multimediali e reattivi di MS

**[!UICONTROL Custom Parameters]:** (Facoltativo; applicabile solo alle campagne per il pubblico di [!DNL Microsoft Advertising]) Coppie nome e valore per un massimo di tre parametri personalizzati. La lunghezza massima per i nomi è di 16 caratteri alfanumerici; la lunghezza massima per i valori è di 200 caratteri, inclusi i parametri incorporati.

Puoi includere i nomi dei parametri personalizzati nei modelli di tracciamento per l’entità e le relative entità secondarie. Quando un utente fa clic su un annuncio rilevante, la rete di annunci sostituisce il nome del parametro con il valore del parametro definito. Ad esempio, se crei un parametro cliente `{_color}=red` e il modello di tracciamento include `http://tracker.example.com/?color={_color}&u={lpurl}`, nel parametro del colore viene inserito &quot;rosso&quot; quando l’utente fa clic su un annuncio.

Parametri personalizzati nel gruppo di annunci o ([!DNL Microsoft Advertising] solo) ad level override dei parametri personalizzati a livello di campagna con lo stesso nome.
