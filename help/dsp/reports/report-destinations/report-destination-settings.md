---
title: Impostazioni destinazione report
description: Vedi i dettagli richiesti per le destinazioni dei rapporti, per tipo di destinazione.
feature: DSP Custom Reports
exl-id: 1437ceea-111a-4c2e-a439-037b3a35865c
source-git-commit: 26a4451fb09f2a42ac60ba123ddf0cf38323312d
workflow-type: tm+mt
source-wordcount: '261'
ht-degree: 0%

---

# Impostazioni destinazione report

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
>* [Informazioni su [!UICONTROL Report Destinations]](/help/dsp/reports/report-destinations/report-destination-about.md)
>* [Crea un [!UICONTROL Report Destination]](/help/dsp/reports/report-destinations/report-destination-create.md)
>* [Modifica un [!UICONTROL Report Destination]](/help/dsp/reports/report-destinations/report-destination-edit.md)
>* [Elimina [!UICONTROL Report Destination]](/help/dsp/reports/report-destinations/report-destination-delete.md)
