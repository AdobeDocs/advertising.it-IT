---
title: Impostazioni di destinazione del rapporto
description: Vedi i dettagli richiesti per le destinazioni dei rapporti, in base al tipo di destinazione.
feature: DSP Custom Reports
exl-id: 1437ceea-111a-4c2e-a439-037b3a35865c
source-git-commit: 7e614ecb517515217d812926f61ca10437820efd
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 0%

---

# Impostazioni di destinazione del rapporto

I dettagli richiesti per le destinazioni di rapporti non-mail variano a seconda del tipo di destinazione.

>[!NOTE]
>
> Puoi anche inviare rapporti personalizzati ai destinatari e-mail, che non richiedono una destinazione del rapporto salvata. Puoi specificare i destinatari e-mail, anziché le destinazioni salvate, nelle impostazioni del rapporto.

## [!UICONTROL S3]

**[!UICONTROL Name]:** Un nome per identificare la destinazione.

**[!UICONTROL S3 Bucket URL]:** Percorso completo della cartella sul [!DNL Amazon Simple Storage Service] (S3) bucket in cui verrà caricato il rapporto. Esempio: `s3://dsp_account/reports`

**[!UICONTROL Access Key ID]:** ID chiave di accesso al[!DNL Amazon S3]) bucket (fornito da [!DNL Amazon]).

**[!UICONTROL Secret Access Key]:** Chiave di accesso segreto per ([!DNL Amazon S3]) bucket (fornito da [!DNL Amazon]).

## [!UICONTROL FTP]

**[!UICONTROL Name]:** Un nome per identificare la destinazione.

**[!UICONTROL Server]:** Nome host del server.

**[!UICONTROL Port]:** Numero di porta da utilizzare sul server. Il valore predefinito è *[!UICONTROL 21]*.

**[!UICONTROL Username]:** Nome utente da accedere al server.

**[!UICONTROL Password]:** La password per accedere al server.

**[!UICONTROL Path (Optional)]:** Percorso del server in cui verranno caricati i file.

## [!UICONTROL SFTP]

**[!UICONTROL Name]:** Un nome per identificare la destinazione.

**[!UICONTROL Server]:** Nome host del server.

**[!UICONTROL Port]:** Numero di porta da utilizzare sul server. Il valore predefinito è *[!UICONTROL 21]*.

**[!UICONTROL Username]:** Nome utente da accedere al server.

**[!UICONTROL Password]:** La password per accedere al server.

**[!UICONTROL Path (Optional)]:** Percorso del server in cui verranno caricati i file.

## [!UICONTROL FTP SSL]

**[!UICONTROL Name]:** Un nome per identificare la destinazione.

**[!UICONTROL Server]:** Nome host del server.

**[!UICONTROL Port]:** Numero di porta da utilizzare sul server. Il valore predefinito è *[!UICONTROL 21]*.

**[!UICONTROL Username]:** Nome utente da accedere al server.

**[!UICONTROL Password]:** La password per accedere al server.

**[!UICONTROL Path (Optional)]:** Percorso del server in cui verranno caricati i file.

>[!MORELIKETHIS]
>
>* [Informazioni [!UICONTROL Report Destinations]](/help/dsp/reports/report-destinations/report-destination-about.md)
>* [Crea un [!UICONTROL Report Destination]](/help/dsp/reports/report-destinations/report-destination-create.md)
>* [Modificare un [!UICONTROL Report Destination]](/help/dsp/reports/report-destinations/report-destination-edit.md)
>* [Eliminare un [!UICONTROL Report Destination]](/help/dsp/reports/report-destinations/report-destination-delete.md)

