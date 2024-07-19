---
source-git-commit: 92bf7768be91e75f029e1577c7f4e7e790c5a934
workflow-type: tm+mt
source-wordcount: '532'
ht-degree: 0%

---
# Snippet

## Campo Modello di tracciamento per entità Google Ads {#tracking-template-google}

<!-- Duplicated from include file because one file has multiple occurrences, which ExL doesn't support. -->

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

## Campo modello di tracciamento per [!DNL Microsoft Advertising] entità {#tracking-template-microsoft}

<!-- Search CRUD and bulk edit of Microsoft entity settings -->

**[!UICONTROL Tracking Template]:** (Facoltativo) Il modello di tracciamento o l&#39;URL di tracciamento, che specifica tutti i reindirizzamenti del dominio di destinazione e i parametri di tracciamento e incorpora anche l&#39;URL della pagina finale/di destinazione in un parametro. Esempio: `{lpurl}?source={network}&id=5` o `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5` per includere un reindirizzamento.

Ad Adobe Advertising, il tracciamento della conversione, che viene applicato quando le impostazioni della campagna includono &quot;[!UICONTROL EF Redirect]&quot; e &quot;[!UICONTROL Auto Upload]&quot;, Search, Social e Commerce prefissano automaticamente il proprio codice di reindirizzamento e tracciamento quando si salva il record.

* Per i parametri supportati per incorporare l&#39;URL finale, vedere la [[!DNL Microsoft Advertising] documentazione sui parametri per indicare l&#39;URL finale](https://help.ads.microsoft.com/#apex/3/en/56799).

* È possibile includere facoltativamente i parametri URL ed eventuali parametri personalizzati definiti per la campagna, separati da e commerciali (&amp;), ad esempio {lpurl}?matchtype={matchtype}&amp;device={device}.

* Facoltativamente, puoi aggiungere reindirizzamenti e tracciamento di terze parti.

<!-- Some entities may need additional/different notes. Try to keep this applicable to all MS entities. -->

>[!NOTE]
>
>* Il modello di tracciamento al livello più granulare sostituisce i valori a tutti i livelli superiori. Ad esempio, se entrambe le impostazioni account e parola chiave includono un valore, tale valore viene applicato.
>* Puoi aggiornare i modelli di tracciamento a qualsiasi livello senza inviare nuovamente gli annunci per l’approvazione.

## Testo e modello: nota che spiega come inserire un parametro dinamico {#inventory-feed-template-insert-dynamic-parameter}

Per inserire un nome di colonna o un gruppo di modificatori come parametro dinamico, fare clic nel campo di input e quindi fare clic su un nome di colonna nell&#39;elenco delle colonne o su un nome di [modificatore](/help/search-social-commerce/campaign-management/inventory-feeds/modifiers-manage.md) nell&#39;elenco dei modificatori. Per inserire la variabile [!DNL Param1] o [!DNL Param2], immettere il valore `{param1:default text}` o `{param2:default text}`, dove &quot;testo predefinito&quot; è il testo utilizzato se la colonna dei parametri nel file di feed è vuota per una riga di annuncio.

## Modello di annuncio testuale: nota che spiega come inserire un ad customizer {#inventory-feed-template-insert-ad-customizer}

Per inserire un ad customizer, utilizzare i formati seguenti, dove `Default text` è un valore facoltativo da inserire quando il file di feed non include un valore valido:

* [!DNL Google Ads]: `{CUSTOMIZER.AdCustomizerName:Default text}`, ad esempio `{CUSTOMIZER.Discount:10%}`

* [!DNL Microsoft Advertising]: `{CUSTOMIZER.Attribute name:Default text}`, ad esempio `{CUSTOMIZER.Discount:10%}`
