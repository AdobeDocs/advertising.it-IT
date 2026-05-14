---
title: Carica dati di conversione offline per conversioni avanzate
description: Scopri come caricare dati di conversione offline di prime parti da mappare su  [!DNL Google Ads] conversioni avanzate per lead e  [!DNL Microsoft Advertising] conversioni avanzate.
feature: Conversions
source-git-commit: 3272a0d3e5766a22c2ff761b84f1774cafe153bd
workflow-type: tm+mt
source-wordcount: '901'
ht-degree: 0%

---

# Carica dati di conversione offline per conversioni avanzate

<!-- Renamed file to start with "conversions-"-->

<!-- Added procedure in new UI, which isn't available to all yet -->

Solo *[!DNL Google Ads]e [!DNL Microsoft Advertising] account*

Puoi caricare i dati di conversione offline di prime parti, inclusi indirizzi e-mail con hash e numeri di telefono, per eseguire il mapping alle [[!DNL Google Ads] conversioni avanzate esistenti per lead](/help/search-social-commerce/admin/conversion-metrics/conversion-action-google.md) e [[!DNL Microsoft Advertising] conversioni avanzate](https://help.ads.microsoft.com/#apex/ads/en/60178). Tutti i dati caricati vengono sincronizzati in tempo reale con la rete di annunci.

## (Nuova interfaccia) Caricare dati per conversioni avanzate

*funzionalità Beta*

1. Nel menu principale, fare clic su **[!UICONTROL Goals]>[!UICONTROL Conversions]**.

1. Sopra la tabella dati, fare clic su **[!UICONTROL Set up Conversion]**.

1. Specifica le impostazioni di caricamento dati:

   1. Nella scheda [!UICONTROL Basic Details]:

      1. Selezionare [!UICONTROL Setup Method] *[!UICONTROL Data Upload]*.

      1. Selezionare [!UICONTROL Platform]: *[!UICONTROL Google]* o *[!UICONTROL Microsoft]*.

      1. Fare clic su **[!UICONTROL Next]**.

   1. Nella scheda [!UICONTROL Configure]:

      1. (Facoltativo) Per scaricare un modello con tutti i [campi dati obbligatori](#enhanced-conversions-leads-data) in formato [!DNL Microsoft Excel], fare clic su **[!UICONTROL Download Template]**, quindi scaricare il file in base alla normale procedura del browser.

         È possibile modificare il file in modo da includere i dati e salvare le modifiche, quindi caricare il file nell&#39;account di rete specificato.

      1. Seleziona l’account di rete dell’annuncio su cui verranno caricati i dati.

      1. Nella casella [!UICONTROL Upload Conversion File] eseguire una delle operazioni seguenti:

         * Trascina un file nella casella.

         * Fare clic su **[!UICONTROL Browse File]**, quindi selezionare un file da caricare dal dispositivo o dalla rete.

   1. Fare clic su **[!UICONTROL Review and Save]** per rivedere le impostazioni.

   1. Fare clic su **[!UICONTROL Upload]**.

## (Interfaccia precedente) Caricamento di dati per conversioni avanzate

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
| [!UICONTROL Email] | L’indirizzo e-mail dell’utente, al quale deve essere applicato l’hashing utilizzando l’algoritmo SHA-256. Ogni riga deve includere un valore [!UICONTROL Email] o [!UICONTROL Phone Number]. |
| [!UICONTROL Phone Number] | Il numero di telefono dell’utente, che deve essere sottoposto a hashing utilizzando l’algoritmo SHA-256. Deve includere un codice paese e può contenere trattini e altri simboli. Ogni riga deve includere un valore [!UICONTROL Email] o [!UICONTROL Phone Number]. |
| [!UICONTROL Conversion Name] | (Obbligatorio) Nome dell’azione di conversione. |
| [!UICONTROL Conversion Time] | (Obbligatorio) Ora in cui si è verificato l&#39;evento di conversione in un formato di ora [supportato](https://support.google.com/google-ads/answer/7014069#prepare_data). Se non includi l&#39;ID del fuso orario dell&#39;account nella riga `Parameters:TimeZone=insert_timezone` sopra la tabella di dati, includi il fuso orario per ogni riga utilizzando a\) il formato [ID fuso orario supportato](https://developers.google.com/google-ads/api/data/codes-formats#timezone_ids) o b\) l&#39;offset GMT, come indicato da + o - e la differenza di ora a 4 cifre (ad esempio -0500 per New York, +0100 per Berlino o +0000 per l&#39;ora di Greenwich). |
| [!UICONTROL Conversion Value] | (Obbligatorio) Il valore di conversione numerico. |
| [!UICONTROL Conversion Currency] | Codice valuta per l’evento di conversione. |
| [!UICONTROL Ad User Data] | (Applicabile per i dati relativi agli utenti dello Spazio economico europeo (SEE) o del Regno Unito (UK)) Indica se è stato fornito il consenso dell&#39;utente per l&#39;invio dei dati utente a [!DNL Google] a scopo di personalizzazione degli annunci. I valori possono includere `Granted`, `Denied` o \[null\] (inviato a [!DNL Google Ads] come `Unspecified`). **Nota:** [!DNL Google Ads] al momento non impone il consenso per le conversioni avanzate per i lead, ma potrebbe farlo in futuro. |
| [!UICONTROL Ad Personalization] | (Applicabile ai dati relativi agli utenti dello Spazio economico europeo (SEE) o del Regno Unito (UK)) Indica se l&#39;utente ha acconsentito all&#39;invio dei dati utente a [!DNL Google] a scopo pubblicitario. I valori possono includere `Granted`, `Denied` o \[null\] (inviato a [!DNL Google Ads] come `Unspecified`). **Nota:** [!DNL Google Ads] al momento non impone il consenso per le conversioni avanzate per i lead, ma potrebbe farlo in futuro. |

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
