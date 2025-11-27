---
title: Carica dati di conversione offline per conversioni avanzate
description: Scopri come caricare dati di conversione offline di prime parti da mappare su  [!DNL Google Ads] conversioni avanzate per lead e  [!DNL Microsoft Advertising] conversioni avanzate.
feature: Conversions
exl-id: 5c5dfbb8-3b17-4973-8012-fc7f0e97e33b
source-git-commit: 3ab2e38f6a2f70c03504363575b13dc0dc730282
workflow-type: tm+mt
source-wordcount: '785'
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

Immettere il fuso orario dell&#39;account in questa posizione o nella colonna &quot;[!UICONTROL Conversion Time]&quot; per ogni riga. Utilizzare a\) ([!DNL Google Ads only]) il formato [ID fuso orario supportato](https://developers.google.com/google-ads/api/data/codes-formats#timezone_ids) o b\) per l&#39;offset GMT, come indicato da + o - e dalla differenza di ora a 4 cifre (ad esempio -0500 per New York, +0100 per Berlino o +0000 per l&#39;ora di Greenwich).

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

Per ulteriori istruzioni sull&#39;utilizzo del modello, vedere [https://help.ads.microsoft.com/#apex/3/56852](https://help.ads.microsoft.com/#apex/3/56852).

| Colonna | Descrizione |
| ------ | ----------- |
| Nome conversione | (Obbligatorio) Nome dell’obiettivo di conversione. |
| Tempo di conversione | (Obbligatorio) L’ora in cui si è verificato l’evento di conversione. Se non includi l’ID del fuso orario dell’account nella riga `Parameters:TimeZone=insert_timezone` sopra la tabella di dati, includi il fuso orario per ogni riga utilizzando l’offset GMT, come indicato da + o - e la differenza di orario di 4 cifre (ad esempio -0500 per New York, +0100 per Berlino o +0000 per Greenwich Mean Time). Per un elenco dei fusi orari per le varie città, vedere [https://learn.microsoft.com/en-us/advertising/guides/time-zones](https://learn.microsoft.com/en-us/advertising/guides/time-zones), ma assicurarsi di utilizzare il formato specificato in questo campo anziché quello nell&#39;elenco dei fusi orari. |
| Valore di conversione | (Obbligatorio) Il valore di conversione numerico. |
| Valuta di conversione | Codice valuta per l’evento di conversione. |
| ID clic Microsoft | Identificatore di clic [!DNL Microsoft] univoco associato (MSCLKID). Questo campo può essere vuoto per le conversioni offline avanzate. |
| Indirizzo e-mail con hash | L’indirizzo e-mail dell’utente, al quale deve essere applicato l’hashing utilizzando l’algoritmo SHA-256. Per conversioni offline avanzate, ogni riga deve includere un valore Indirizzo e-mail con hash o un valore Numero di telefono con hash. |
| Numero di telefono con hash | Il numero di telefono dell’utente, che deve essere sottoposto a hashing utilizzando l’algoritmo SHA-256. Deve includere un codice paese e può contenere trattini e altri simboli. Per conversioni offline avanzate, ogni riga deve includere un valore Indirizzo e-mail con hash o un valore Numero di telefono con hash. |

>[!MORELIKETHIS]
>
>* [Implementa [!DNL Google Ads] conversioni avanzate per lead](/help/search-social-commerce/campaign-management/special-workflows/google-enhanced-conversions-leads.md)
>* [Implementa [!DNL Microsoft Advertising] conversioni offline avanzate](/help/search-social-commerce/campaign-management/special-workflows/microsoft-enhanced-conversions.md)
>* [([!DNL Google Ads only]) Crea un&#39;azione di conversione per una conversione  [!DNL Google Ads] avanzata per lead](/help/search-social-commerce/admin/conversion-metrics/conversion-action-google.md)
>* [Carica metriche di conversione tracciate da ricerca, social e Commerce in [!DNL Google Ads]](/help/search-social-commerce/tools/conversion-metrics-upload-to-google.md)
