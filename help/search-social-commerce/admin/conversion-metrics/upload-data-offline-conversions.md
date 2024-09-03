---
title: Carica dati di conversione offline per conversioni avanzate
description: Scopri come caricare dati di conversione offline di prime parti da mappare su  [!DNL Google Ads] conversioni avanzate per i lead.
feature: Conversions
source-git-commit: c3cb1549adeb7b621c1b426c53da9bb09eddcbdc
workflow-type: tm+mt
source-wordcount: '510'
ht-degree: 0%

---

# Carica dati di conversione offline per conversioni avanzate

Solo *[!DNL Google Ads]account*

<!-- Tweak metadata title/description and heading -->

Puoi caricare i dati di conversione offline di prime parti, inclusi indirizzi e-mail con hash e numeri di telefono, per eseguire il mapping alle [[!DNL Google Ads] conversioni avanzate esistenti per i lead](/help/search-social-commerce/admin/conversion-metrics/conversion-action-google.md). Tutti i dati caricati vengono sincronizzati in tempo reale in [!DNL Google Ads].

## Carica dati per [!DNL Google Ads] conversioni avanzate per lead

1. Nel menu principale fare clic su **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Conversions]** e quindi sulla scheda **[!UICONTROL Upload]**.

1. Seleziona la rete di annunci e quindi l’account.

1. (Facoltativo) Per scaricare un modello con tutti i [campi dati obbligatori](#enhanced-conversions-leads-data) in formato [!DNL Microsoft Excel], fare clic su **[!UICONTROL View Template]**, quindi scaricare il file in base alla normale procedura del browser.

   Puoi modificare il file in modo da includere i dati e salvare le modifiche, quindi caricare il file nel passaggio successivo.

1. Fare clic su **[!UICONTROL Choose File]**, quindi selezionare un file da caricare dal dispositivo o dalla rete.

## Dati richiesti per i file caricati {#enhanced-conversions-leads-data}

### Dati sopra la tabella

`Parameters:TimeZone=insert_timezone`

Immettere il fuso orario dell&#39;account in questa posizione o nella colonna &quot;[!UICONTROL Conversion Time]&quot; per ogni riga. Utilizzare a) il formato ID del fuso orario [supportato](https://developers.google.com/google-ads/api/data/codes-formats#timezone_ids) o b) l&#39;offset GMT, come indicato da + o - e la differenza di ora a 4 cifre (ad esempio -0500 per New York).

### Colonne e valori della tabella

| Colonna | Descrizione |
| ------ | ----------- |
| E-mail | L’indirizzo e-mail dell’utente, al quale deve essere applicato l’hashing utilizzando l’algoritmo SHA-256. Ogni riga deve includere un valore E-mail o Numero di telefono. |
| Numero di telefono | Il numero di telefono dell’utente, che deve essere sottoposto a hashing utilizzando l’algoritmo SHA-256. Deve includere un codice paese e può contenere trattini e altri simboli. Ogni riga deve includere un valore E-mail o Numero di telefono. |
| Nome conversione | (Obbligatorio) Nome dell’azione di conversione. |
| Tempo di conversione | (Obbligatorio) Ora in cui si è verificato l&#39;evento di conversione in un formato di ora [supportato](https://support.google.com/google-ads/answer/7014069#prepare_data). Se non includi l&#39;ID del fuso orario dell&#39;account nella riga `Parameters:TimeZone=insert_timezone` al di sopra della tabella di dati, includi il fuso orario per ogni riga utilizzando a) il formato ID [fuso orario supportato](https://developers.google.com/google-ads/api/data/codes-formats#timezone_ids) o b) l&#39;offset GMT, come indicato da + o - e la differenza orario di 4 cifre (ad esempio -0500 per New York). |
| Valore di conversione | (Obbligatorio) Il valore di conversione numerico. |
| Valuta di conversione | Codice valuta per l’evento di conversione. |
| Aggiungi dati utente | (Applicabile per i dati relativi agli utenti dello Spazio economico europeo (SEE) o del Regno Unito (UK)) Indica se è stato fornito il consenso dell&#39;utente per l&#39;invio dei dati utente a [!DNL Google] a scopo di personalizzazione degli annunci. I valori possono includere `Granted`, `Denied` o \[null\] (inviato a [!DNL Google Ads] come `Unspecified`). **Nota:** [!DNL Google Ads] al momento non impone il consenso per le conversioni avanzate per i lead, ma potrebbe farlo in futuro. |
| Ad Personalization | (Applicabile ai dati relativi agli utenti dello Spazio economico europeo (SEE) o del Regno Unito (UK)) Indica se l&#39;utente ha acconsentito all&#39;invio dei dati utente a [!DNL Google] a scopo pubblicitario. I valori possono includere `Granted`, `Denied` o \[null\] (inviato a [!DNL Google Ads] come `Unspecified`). **Nota:** [!DNL Google Ads] al momento non impone il consenso per le conversioni avanzate per i lead, ma potrebbe farlo in futuro. |

>[!MORELIKETHIS]
>
>* [Crea un&#39;azione di conversione per  [!DNL Google Ads] conversione avanzata per lead](/help/search-social-commerce/admin/conversion-metrics/conversion-action-google.md)
>* [Implementa [!DNL Google Ads] conversioni avanzate per lead](/help/search-social-commerce/campaign-management/special-workflows/google-enhanced-conversions-leads.md)
>* [Carica metriche di conversione tracciate da ricerca, social e Commerce in [!DNL Google Ads]](/help/search-social-commerce/tools/conversion-metrics-upload-to-google.md)
