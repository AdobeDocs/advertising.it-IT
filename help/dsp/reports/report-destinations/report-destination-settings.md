---
title: Impostazioni di destinazione del rapporto
description: Vedi i dettagli richiesti per le destinazioni dei rapporti, per tipo di destinazione.
feature: DSP Custom Reports
exl-id: 1437ceea-111a-4c2e-a439-037b3a35865c
TQID: https://experienceleague.adobe.com/VB5UY9vm147LQJMKKyGOlhZdNcq6mVDYTT0Ef4RcwVs
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2:
  - id: cc3b7f3c-58f0-4ba4-b808-391002930fd4
  - id: e8b92199-d82f-4b20-9fc3-ffe694f93ce5
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 267
ht-degree: 0%

---

# Impostazioni di destinazione del rapporto

I dettagli richiesti per le destinazioni dei rapporti non e-mail variano a seconda del tipo di destinazione.

>[!NOTE]
>
> Puoi anche inviare i rapporti personalizzati ai destinatari e-mail, che non richiedono una destinazione di rapporto salvata. Nelle impostazioni del rapporto puoi specificare i destinatari e-mail anziché le destinazioni salvate.

## [!UICONTROL S3]

**[!UICONTROL Name]:** Nome per identificare la destinazione.

**[!UICONTROL S3 Bucket URL]:** Percorso completo della cartella nel bucket [!DNL Amazon Simple Storage Service] (S3) in cui viene caricato il report. Esempio: `s3://dsp_account/reports`

**[!UICONTROL Access Key ID]:** ID della chiave di accesso al bucket ([!DNL Amazon S3]) (fornito da [!DNL Amazon]).

**[!UICONTROL Secret Access Key]:** Chiave di accesso segreta al bucket ([!DNL Amazon S3]) (fornita da [!DNL Amazon]).

## [!UICONTROL FTP]

**[!UICONTROL Name]:** Nome per identificare la destinazione.

**[!UICONTROL Server]:** Il nome host per il server.

**[!UICONTROL Port]:** Numero di porta da utilizzare nel server. Il valore predefinito è *[!UICONTROL 21]*.

**[!UICONTROL Username]:** Nome utente per accedere al server.

**[!UICONTROL Password]:** La password per accedere al server.

**[!UICONTROL Path (Optional)]:** Il percorso del server in cui vengono caricati i file.

## [!UICONTROL SFTP]

**[!UICONTROL Name]:** Nome per identificare la destinazione.

**[!UICONTROL Server]:** Il nome host per il server.

**[!UICONTROL Port]:** Numero di porta da utilizzare nel server. Il valore predefinito è *[!UICONTROL 21]*.

**[!UICONTROL Username]:** Nome utente per accedere al server.

**[!UICONTROL Password]:** La password per accedere al server.

**[!UICONTROL Path (Optional)]:** Il percorso del server in cui vengono caricati i file.

## [!UICONTROL FTP SSL]

**[!UICONTROL Name]:** Nome per identificare la destinazione.

**[!UICONTROL Server]:** Il nome host per il server.

**[!UICONTROL Port]:** Numero di porta da utilizzare nel server. Il valore predefinito è *[!UICONTROL 21]*.

**[!UICONTROL Username]:** Nome utente per accedere al server.

**[!UICONTROL Password]:** La password per accedere al server.

**[!UICONTROL Path (Optional)]:** Il percorso del server in cui vengono caricati i file.

>[!MORELIKETHIS]
>
>* [Informazioni sulle destinazioni dei report](/help/dsp/reports/report-destinations/report-destination-about.md)
>* [Creare una destinazione di report](/help/dsp/reports/report-destinations/report-destination-create.md)
>* [Modifica un [!UICONTROL Report Destination]](/help/dsp/reports/report-destinations/report-destination-edit.md)
>* [Eliminare una destinazione di report](/help/dsp/reports/report-destinations/report-destination-delete.md)
