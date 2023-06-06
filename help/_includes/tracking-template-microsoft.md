---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 0%

---
# Campo Modello di tracciamento per entità Microsoft Advertising

<!-- Search CRUD and bulk edit of Microsoft entity settings -->

**[!UICONTROL Tracking Template]:** (Facoltativo) Il modello di tracciamento o l’URL di tracciamento, che specifica tutti i reindirizzamenti e i parametri di tracciamento dei domini di destinazione e incorpora anche l’URL finale/della pagina di destinazione in un parametro. Esempio: `{lpurl}?source={network}&id=5` o `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5` per includere un reindirizzamento.

Ad Adobe, il tracciamento della conversione di Advertising, applicato quando le impostazioni della campagna includono &quot;[!UICONTROL EF Redirect]&quot; e &quot;[!UICONTROL Auto Upload],&quot; Search, Social e Commerce aggiunge automaticamente il prefisso al proprio codice di reindirizzamento e di tracciamento quando si salva il record.

* Per i parametri supportati per incorporare l’URL finale, vedi [[!DNL Microsoft Advertising] documentazione sui parametri per indicare l’URL finale](https://help.ads.microsoft.com/#apex/3/en/56799).

* Facoltativamente, puoi includere i parametri URL ed eventuali parametri personalizzati definiti per la campagna, separati da e commerciali (&amp;), ad esempio {lpurl}?matchtype={matchtype}&amp;device={device}.

* Facoltativamente, puoi aggiungere reindirizzamenti e tracciamento di terze parti.

<!-- Some entities may need additional/different notes. Try to keep this applicable to all MS entities. -->

>[!NOTE]
>
>* Il modello di tracciamento al livello più granulare sostituisce i valori a tutti i livelli superiori. Ad esempio, se entrambe le impostazioni account e parola chiave includono un valore, tale valore viene applicato.
>* Puoi aggiornare i modelli di tracciamento a qualsiasi livello senza inviare nuovamente gli annunci per l’approvazione.

