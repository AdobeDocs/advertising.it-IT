---
source-git-commit: 38d6d70d03c12aab1a7caee6e589a2fdeaf78ad4
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 0%

---
# Campo Modello di tracciamento per entità Microsoft Advertising

<!-- Search CRUD and bulk edit of Microsoft entity settings -->

**[!UICONTROL Tracking Template]:** (Facoltativo; non disponibile per tutte le entità) Il modello di tracciamento o l&#39;URL di tracciamento, che specifica tutti i reindirizzamenti del dominio di destinazione e i parametri di tracciamento e incorpora anche l&#39;URL della pagina finale/di destinazione in un parametro. Esempio: `{lpurl}?source={network}&id=5` o `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5` per includere un reindirizzamento.

Ad Adobe Advertising, il tracciamento della conversione, che viene applicato quando le impostazioni della campagna includono &quot;[!UICONTROL EF Redirect]&quot; e &quot;[!UICONTROL Auto Upload]&quot;, Search, Social e Commerce prefissano automaticamente il proprio codice di reindirizzamento e tracciamento quando si salva il record.

* Per i parametri supportati per incorporare l&#39;URL finale, vedere la [[!DNL Microsoft Advertising] documentazione sui parametri per indicare l&#39;URL finale](https://help.ads.microsoft.com/#apex/3/en/56799).

* È possibile includere facoltativamente i parametri URL ed eventuali parametri personalizzati definiti per la campagna, separati da e commerciali (&amp;), ad esempio {lpurl}?matchtype={matchtype}&amp;device={device}.

* Facoltativamente, puoi aggiungere reindirizzamenti e tracciamento di terze parti.

<!-- Some entities may need additional/different notes. Try to keep this applicable to all MS entities. -->

>[!NOTE]
>
>* Il modello di tracciamento al livello più granulare sostituisce i valori a tutti i livelli superiori. Ad esempio, se entrambe le impostazioni account e parola chiave includono un valore, tale valore viene applicato.
>* Puoi aggiornare i modelli di tracciamento a qualsiasi livello senza inviare nuovamente gli annunci per l’approvazione.
