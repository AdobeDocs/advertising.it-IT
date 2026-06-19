---
source-git-commit: 47de92fd6d4b1d481380a58f75ec4735d95fca73
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 0%

---
# Campo modello di tracciamento per [!DNL LY Ads] entità

<!-- Search CRUD and bulk edit of LY Ads entity settings -->

**[!UICONTROL Tracking Template]:** (Facoltativo) Il modello di tracciamento o l&#39;URL di tracciamento, che specifica tutti i reindirizzamenti del dominio di destinazione e i parametri di tracciamento e incorpora anche l&#39;URL della pagina finale/di destinazione in un parametro. Utilizzare il parametro `!{lpurl}` per indicare l&#39;URL della pagina di destinazione. Esempio: `{lpurl}?source={network}&id=5` o `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5` per includere un reindirizzamento.

Facoltativamente, puoi aggiungere reindirizzamenti e tracciamento di terze parti.

Per il tracciamento delle conversioni di Adobe Advertising, applicato quando le impostazioni della campagna includono &quot;[!UICONTROL EF Redirect]&quot; e &quot;[!UICONTROL Auto Upload]&quot;, Search, Social e Commerce prefissano automaticamente il proprio codice di reindirizzamento e tracciamento quando si salva il record.

>[!NOTE]
>
>* Il modello di tracciamento al livello più granulare sostituisce i valori a tutti i livelli superiori. Ad esempio, se entrambe le impostazioni account e parola chiave includono un valore, tale valore viene applicato.
>* Puoi aggiornare i modelli di tracciamento a qualsiasi livello senza inviare nuovamente gli annunci per l’approvazione.
