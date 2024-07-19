---
source-git-commit: a59b477a6f8a616851d85bf89b58434d4d56cd83
workflow-type: tm+mt
source-wordcount: '244'
ht-degree: 0%

---
# Campo Modello di tracciamento per entità Google Ads

<!-- Search CRUD and bulk edit of Google entity settings -->

**[!UICONTROL Tracking Template]:** (Facoltativo) Il modello di tracciamento o l&#39;URL di tracciamento, che specifica tutti i reindirizzamenti del dominio di destinazione e i parametri di tracciamento e incorpora anche l&#39;URL della pagina di destinazione/finale in un parametro [!DNL ValueTrack]. Esempio: `{lpurl}?source={network}&id=5` o `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5` per includere un reindirizzamento.

Ad Adobe Advertising, il tracciamento della conversione, che viene applicato quando le impostazioni della campagna includono &quot;[!UICONTROL EF Redirect]&quot; e &quot;[!UICONTROL Auto Upload]&quot;, Search, Social e Commerce prefissano automaticamente il proprio codice di reindirizzamento e tracciamento quando si salva il record.

* Per i parametri supportati per incorporare l&#39;URL finale, consulta la [[!DNL Google Ads] documentazione dei  [!DNL ValueTrack] formati](https://support.google.com/google-ads/answer/6305348) supportati. (Andare ai parametri &quot;Solo modello di tracciamento&quot; nella sezione &quot;Parametri [!DNL ValueTrack] disponibili&quot;).

* È possibile includere facoltativamente i parametri URL ed eventuali parametri personalizzati definiti per la campagna, separati da e commerciali (&amp;), ad esempio {lpurl}?matchtype={matchtype}&amp;device={device}.

* Facoltativamente, puoi aggiungere reindirizzamenti e tracciamento di terze parti.

>[!NOTE]
>
>* Evita l&#39;uso di macro, che non sono sostituite dai clic provenienti da origini che abilitano il tracciamento parallelo. Se l’inserzionista deve utilizzare delle macro, il Team dell’account Adobe deve collaborare con l’Assistenza clienti o con il team di implementazione per aggiungerle.
>* Il modello di tracciamento al livello più granulare sostituisce i valori a tutti i livelli superiori. Ad esempio, se entrambe le impostazioni account e parola chiave includono un valore, tale valore viene applicato.
>* Se aggiorni un modello di tracciamento a livello di annuncio, sitelink o parola chiave, gli annunci pertinenti vengono nuovamente inviati per la revisione. Puoi aggiornare i modelli di tracciamento a livello di account, campagna o gruppo di annunci senza inviare nuovamente gli annunci per l’approvazione.
