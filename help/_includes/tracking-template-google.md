---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '244'
ht-degree: 0%

---
# Campo Modello di tracciamento per entità Google Ads

<!-- Search CRUD and bulk edit of Google entity settings -->

**[!UICONTROL Tracking Template]:** (Facoltativo) Il modello di tracciamento o l’URL di tracciamento, che specifica tutti i reindirizzamenti e i parametri di tracciamento dei domini di fuori destinazione e incorpora anche l’URL finale/della pagina di destinazione in un [!DNL ValueTrack] parametro. Esempio: `{lpurl}?source={network}&id=5` o `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5` per includere un reindirizzamento.

Ad Adobe, il tracciamento della conversione di Advertising, applicato quando le impostazioni della campagna includono &quot;[!UICONTROL EF Redirect]&quot; e &quot;[!UICONTROL Auto Upload],&quot; Search, Social e Commerce aggiunge automaticamente il prefisso al proprio codice di reindirizzamento e di tracciamento quando si salva il record.

* Per i parametri supportati per incorporare l’URL finale, vedi [[!DNL Google Ads] documentation for the supported [!DNL ValueTrack] formati](https://support.google.com/google-ads/answer/6305348). (Andare ai parametri &quot;Solo modello di tracciamento&quot; nella sezione &quot;Parametri ValueTrack disponibili&quot;).

* Facoltativamente, puoi includere i parametri URL ed eventuali parametri personalizzati definiti per la campagna, separati da e commerciali (&amp;), ad esempio {lpurl}?matchtype={matchtype}&amp;device={device}.

* Facoltativamente, puoi aggiungere reindirizzamenti e tracciamento di terze parti.

>[!NOTE]
>
>* Evita l&#39;uso di macro, che non sono sostituite dai clic provenienti da origini che abilitano il tracciamento parallelo. Se l’inserzionista deve utilizzare delle macro, il Team dell’account Adobe deve collaborare con l’Assistenza clienti o con il team di implementazione per aggiungerle.
>* Il modello di tracciamento al livello più granulare sostituisce i valori a tutti i livelli superiori. Ad esempio, se entrambe le impostazioni account e parola chiave includono un valore, tale valore viene applicato.
>* Se aggiorni un modello di tracciamento a livello di annuncio, sitelink o parola chiave, gli annunci pertinenti vengono nuovamente inviati per la revisione. Puoi aggiornare i modelli di tracciamento a livello di account, campagna o gruppo di annunci senza inviare nuovamente gli annunci per l’approvazione.

