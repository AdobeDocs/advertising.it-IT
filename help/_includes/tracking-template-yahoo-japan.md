---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 0%

---
# Campo modello di tracciamento per Yahoo! Entità Japan Ads

<!-- Search CRUD and bulk edit of Yahoo! Japan Ads entity settings -->

**[!UICONTROL Tracking Template]:** (Facoltativo) Il modello di tracciamento o l’URL di tracciamento, che specifica tutti i reindirizzamenti e i parametri di tracciamento dei domini di destinazione e incorpora anche l’URL finale/della pagina di destinazione in un parametro. Usa il parametro `!{lpurl}` per indicare l’URL della pagina di destinazione. Esempio: `{lpurl}?source={network}&id=5` o `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5` per includere un reindirizzamento.

Facoltativamente, puoi aggiungere reindirizzamenti e tracciamento di terze parti.

Ad Adobe, il tracciamento della conversione di Advertising, applicato quando le impostazioni della campagna includono &quot;[!UICONTROL EF Redirect]&quot; e &quot;[!UICONTROL Auto Upload],&quot; Search, Social e Commerce aggiunge automaticamente il prefisso al proprio codice di reindirizzamento e di tracciamento quando si salva il record.

>[!NOTE]
>
>* Il modello di tracciamento al livello più granulare sostituisce i valori a tutti i livelli superiori. Ad esempio, se entrambe le impostazioni account e parola chiave includono un valore, tale valore viene applicato.
>* Puoi aggiornare i modelli di tracciamento a qualsiasi livello senza inviare nuovamente gli annunci per l’approvazione.

