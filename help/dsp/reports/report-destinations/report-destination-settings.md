---
title: Impostazioni destinazione report
description: Vedi i dettagli richiesti per le destinazioni dei rapporti, per tipo di destinazione.
feature: DSP Custom Reports
exl-id: 1437ceea-111a-4c2e-a439-037b3a35865c
source-git-commit: 7e614ecb517515217d812926f61ca10437820efd
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 0%

---

# Impostazioni destinazione report

I dettagli richiesti per le destinazioni dei rapporti non e-mail variano a seconda del tipo di destinazione.

>[!NOTE]
>
> Puoi anche inviare i rapporti personalizzati ai destinatari e-mail, che non richiedono una destinazione di rapporto salvata. Nelle impostazioni del rapporto puoi specificare i destinatari e-mail anziché le destinazioni salvate.

## [!UICONTROL S3]

**[!UICONTROL Name]:** Un nome per identificare la destinazione.

**[!UICONTROL S3 Bucket URL]:** Percorso completo della cartella sul [!DNL Amazon Simple Storage Service] (S3) bucket in cui verrà caricato il rapporto. Esempio: `s3://dsp_account/reports`

**[!UICONTROL Access Key ID]:** L’ID della chiave di accesso a ([!DNL Amazon S3]) bucket (fornito da [!DNL Amazon]).

**[!UICONTROL Secret Access Key]:** Chiave di accesso segreta a ([!DNL Amazon S3]) bucket (fornito da [!DNL Amazon]).

## [!UICONTROL FTP]

**[!UICONTROL Name]:** Un nome per identificare la destinazione.

**[!UICONTROL Server]:** Il nome host del server.

**[!UICONTROL Port]:** Numero di porta da utilizzare sul server. Il valore predefinito è *[!UICONTROL 21]*.

**[!UICONTROL Username]:** Nome utente per accedere al server.

**[!UICONTROL Password]:** Password per accedere al server.

**[!UICONTROL Path (Optional)]:** Percorso del server in cui verranno caricati i file.

## [!UICONTROL SFTP]

**[!UICONTROL Name]:** Un nome per identificare la destinazione.

**[!UICONTROL Server]:** Il nome host del server.

**[!UICONTROL Port]:** Numero di porta da utilizzare sul server. Il valore predefinito è *[!UICONTROL 21]*.

**[!UICONTROL Username]:** Nome utente per accedere al server.

**[!UICONTROL Password]:** Password per accedere al server.

**[!UICONTROL Path (Optional)]:** Percorso del server in cui verranno caricati i file.

## [!UICONTROL FTP SSL]

**[!UICONTROL Name]:** Un nome per identificare la destinazione.

**[!UICONTROL Server]:** Il nome host del server.

**[!UICONTROL Port]:** Numero di porta da utilizzare sul server. Il valore predefinito è *[!UICONTROL 21]*.

**[!UICONTROL Username]:** Nome utente per accedere al server.

**[!UICONTROL Password]:** Password per accedere al server.

**[!UICONTROL Path (Optional)]:** Percorso del server in cui verranno caricati i file.

>[!MORELIKETHIS]
>
>* [Informazioni su [!UICONTROL Report Destinations]](/help/dsp/reports/report-destinations/report-destination-about.md)
>* [Creare un [!UICONTROL Report Destination]](/help/dsp/reports/report-destinations/report-destination-create.md)
>* [Modifica un [!UICONTROL Report Destination]](/help/dsp/reports/report-destinations/report-destination-edit.md)
>* [Eliminare un [!UICONTROL Report Destination]](/help/dsp/reports/report-destinations/report-destination-delete.md)

