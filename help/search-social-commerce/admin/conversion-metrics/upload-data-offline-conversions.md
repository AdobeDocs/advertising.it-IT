---
title: Carica dati di conversione offline per conversioni avanzate
description: Scopri come caricare dati di conversione offline di prime parti da mappare su  [!DNL Google Ads] conversioni avanzate per lead e  [!DNL Microsoft Advertising] conversioni avanzate.
feature: Conversions
exl-id: 5c5dfbb8-3b17-4973-8012-fc7f0e97e33b
TQID: https://experienceleague.adobe.com/Hfmc5VCw9682cYmOQIcoy1Yy6InkoSmE18qqILbD2oI
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: ab69d6b27b86f6e4d9da6be3cd0245d6116469d3
workflow-type: tm+mt
source-wordcount: 792
ht-degree: 0%

---

# Carica dati di conversione offline per conversioni avanzate

Solo *[!DNL Google Ads]e [!DNL Microsoft Advertising] account*

Puoi caricare i dati di conversione offline di prime parti, inclusi indirizzi e-mail con hash e numeri di telefono, per eseguire il mapping alle [[!DNL Google Ads] conversioni avanzate esistenti per lead](/help/search-social-commerce/admin/conversion-metrics/conversion-action-google.md) e [[!DNL Microsoft Advertising] conversioni avanzate](https://help.ads.microsoft.com/#apex/ads/en/60178). Tutti i dati caricati vengono sincronizzati in tempo reale con la rete di annunci.

## Caricare dati per conversioni avanzate

1. Nel menu principale fare clic su **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Admin] >[!UICONTROL Conversions]** e quindi sulla scheda **[!UICONTROL Upload]**.

1. Seleziona la rete di annunci e quindi l’account.

1. (Facoltativo) Per scaricare un modello con tutti i [campi dati obbligatori](#enhanced-conversions-leads-data) in formato [!DNL Microsoft Excel], fare clic su **[!UICONTROL View Template]**, quindi scaricare il file in base alla normale procedura del browser.

   Puoi modificare il file in modo da includere i dati e salvare le modifiche, quindi caricare il file nel passaggio successivo.

1. Fare clic su **[!UICONTROL Choose File]**, quindi selezionare un file da caricare dal dispositivo o dalla rete.

## Dati richiesti per i file caricati {#enhanced-conversions-leads-data}

### Dati sopra la tabella

`Parameters:TimeZone=insert_timezone`

Immettere il fuso orario dell&#39;account in questa posizione o nella colonna &quot;[!UICONTROL Conversion Time]&quot; per ogni riga. Utilizza a\) ([!DNL solo [!DNL Google Ads]]) il formato [ID fuso orario supportato](https://developers.google.com/google-ads/api/data/codes-formats#timezone_ids) o b\) l&#39;offset GMT, come indicato da + o - e la differenza di ora a 4 cifre (ad esempio -0500 per New York, +0100 per Berlino o +0000 per l&#39;ora di Greenwich).

### Colonne e valori della tabella per [!DNL Google Ads]

| Colonna | Descrizione |
| ------ | ----------- |
| E-mail | L’indirizzo e-mail dell’utente, al quale deve essere applicato l’hashing utilizzando l’algoritmo SHA-256. Ogni riga deve includere un valore E-mail o Numero di telefono. |
| Numero di telefono | Il numero di telefono dell’utente, che deve essere sottoposto a hashing utilizzando l’algoritmo SHA-256. Deve includere un codice paese e può contenere trattini e altri simboli. Ogni riga deve includere un valore E-mail o Numero di telefono. |
| Nome conversione | (Obbligatorio) Nome dell’azione di conversione. |
| Tempo di conversione | (Obbligatorio) Ora in cui si è verificato l&#39;evento di conversione in un formato di ora [supportato](https://support.google.com/google-ads/answer/7014069#prepare_data). Se non includi l&#39;ID del fuso orario dell&#39;account nella riga `Parameters:TimeZone=insert_timezone` sopra la tabella di dati, includi il fuso orario per ogni riga utilizzando a\) il formato [ID fuso orario supportato](https://developers.google.com/google-ads/api/data/codes-formats#timezone_ids) o b\) l&#39;offset GMT, come indicato da + o - e la differenza di ora a 4 cifre (ad esempio -0500 per New York, +0100 per Berlino o +0000 per l&#39;ora di Greenwich). |
| Valore di conversione | (Obbligatorio) Il valore di conversione numerico. |
| Valuta di conversione | Codice valuta per l’evento di conversione. |
| Aggiungi dati utente | (Applicabile per i dati relativi agli utenti dello Spazio economico europeo (SEE) o del Regno Unito (UK)) Indica se è stato fornito il consenso dell&#39;utente per l&#39;invio dei dati utente a [!DNL Google] a scopo di personalizzazione degli annunci. I valori possono includere `Granted`, `Denied` o \[null\] (inviato a [!DNL Google Ads] come `Unspecified`). **Nota:** [!DNL Google Ads] al momento non impone il consenso per le conversioni avanzate per i lead, ma potrebbe farlo in futuro. |
| Ad Personalization | (Applicabile ai dati relativi agli utenti dello Spazio economico europeo (SEE) o del Regno Unito (UK)) Indica se l&#39;utente ha acconsentito all&#39;invio dei dati utente a [!DNL Google] a scopo pubblicitario. I valori possono includere `Granted`, `Denied` o \[null\] (inviato a [!DNL Google Ads] come `Unspecified`). **Nota:** [!DNL Google Ads] al momento non impone il consenso per le conversioni avanzate per i lead, ma potrebbe farlo in futuro. |

### Colonne e valori della tabella per [!DNL Microsoft Advertising]

Per ulteriori istruzioni sulla formattazione e sull&#39;hashing dei dati, vedere la documentazione di [!DNL Microsoft Ads] su [Conversioni avanzate](https://help.ads.microsoft.com/#apex/ads/60178).

| Colonna | Descrizione |
| ------ | ----------- |
| [!UICONTROL Email] | L’indirizzo e-mail dell’utente, al quale deve essere applicato l’hashing utilizzando l’algoritmo SHA-256. Ogni riga deve includere un valore [!UICONTROL Email] o [!UICONTROL Phone Number]. |
| [!UICONTROL Phone Number] | Il numero di telefono dell’utente, che deve essere sottoposto a hashing utilizzando l’algoritmo SHA-256. Deve includere un codice paese e può contenere trattini e altri simboli. Per le conversioni offline avanzate, ogni riga deve includere un valore [!UICONTROL Email] o un valore [!UICONTROL Phone Number]. |
| [!UICONTROL Conversion Name] | (Obbligatorio) Nome dell’azione di conversione. |
| [!UICONTROL Conversion Time] | (Obbligatorio) L’ora in cui si è verificato l’evento di conversione. Se non includi l’ID del fuso orario dell’account nella riga `Parameters:TimeZone=insert_timezone` sopra la tabella di dati, includi il fuso orario per ogni riga utilizzando l’offset GMT, come indicato da + o - e la differenza di orario di 4 cifre (ad esempio -0500 per New York, +0100 per Berlino o +0000 per Greenwich Mean Time). Per un elenco dei fusi orari per le varie città, vedere [https://learn.microsoft.com/en-us/advertising/guides/time-zones](https://learn.microsoft.com/en-us/advertising/guides/time-zones), ma assicurarsi di utilizzare il formato specificato in questo campo anziché quello nell&#39;elenco dei fusi orari. |
| [!UICONTROL Conversion Value] | (Obbligatorio) Il valore di conversione numerico. |
| [!UICONTROL Conversion Currency] | Codice valuta per l’evento di conversione. |

>[!MORELIKETHIS]
>
>* [Implementa [!DNL Google Ads] conversioni avanzate per lead](/help/search-social-commerce/campaign-management/special-workflows/google-enhanced-conversions-leads.md)
>* [Implementa [!DNL Microsoft Advertising] conversioni offline avanzate](/help/search-social-commerce/campaign-management/special-workflows/microsoft-enhanced-conversions.md)
>* [Crea un&#39;azione di conversione per  [!DNL Google Ads] conversione avanzata per lead](/help/search-social-commerce/admin/conversion-metrics/conversion-action-google.md)
>* [Carica metriche di conversione tracciate da ricerca, social e Commerce in [!DNL Google Ads]](/help/search-social-commerce/tools/conversion-metrics-upload-to-google.md)
