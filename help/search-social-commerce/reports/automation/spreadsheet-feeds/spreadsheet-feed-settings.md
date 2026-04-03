---
title: Impostazioni feed report foglio di calcolo
description: Scopri le impostazioni per i feed di fogli di calcolo.
exl-id: 88836c15-81fe-4fe7-8321-2c984b4dcb5d
feature: Search Reports
TQID: https://experienceleague.adobe.com/4JPflN5lVXkNf2nWszh-LznW2xNaMkQMGPOxo6Ac2WU
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 513
ht-degree: 0%

---

# Impostazioni feed report foglio di calcolo

| Campo | Descrizione |
|---|---|
| [!UICONTROL Feed Name] | Un nome per il feed del foglio di calcolo. |
| [!UICONTROL Report Template] | Il modello di report che specifica i dati del report richiesti; selezionare quello utilizzato per creare il modello [!DNL Excel]. Sono elencati tutti i modelli di report di base.<br><br><b>Nota:</b> se si modifica il modello di report utilizzato per il report o si aggiornano le colonne nel modello, è necessario creare e caricare un nuovo modello [!DNL Excel]. |
| [!UICONTROL Excel Template] | Il modello [!DNL Excel] appositamente formattato creato in formato .XLSX, che viene applicato ai dati specificati nel modello di report. Specificare il file da caricare immettendo il percorso completo e il nome del file oppure facendo clic su <b>[!UICONTROL Browse]</b> per individuare il file nel dispositivo o nella rete. |
| [!UICONTROL Back Fill From] | Data di inizio per la quale vengono aggiornati i dati esistenti nella scheda [!UICONTROL RAW], rappresentata da un numero di giorni nel passato. Immetti un valore massimo di 90 giorni; il valore predefinito è sette (7) giorni.<br><br>Ad esempio, se il valore è 7 e oggi è 7 marzo, i dati esistenti nella scheda [!UICONTROL RAW] a partire dal 1 marzo verranno aggiornati (fino alla data di fine specificata dal parametro [!UICONTROL Back Fill Until]). Le righe di dati esistenti per le date precedenti al 1° marzo non vengono eliminate, ma non vengono aggiornate. |
| [!UICONTROL Back Fill Until] | Data di fine per la quale i dati esistenti nella scheda [!UICONTROL RAW] vengono aggiornati, rappresentata da un numero di giorni nel passato. Il valore predefinito è un (1) giorno.<br><br>Ad esempio, se il valore è 1 e oggi è 7 marzo, i dati esistenti nella scheda [!UICONTROL RAW] verranno aggiornati fino al 6 marzo e a partire dalla data di inizio specificata dal parametro [!UICONTROL Back Fill From]. Se questo valore è 1, il parametro [!UICONTROL Back Fill Until] è 7 e oggi è 7 marzo, i dati esistenti nella scheda [!UICONTROL RAW] vengono aggiornati dal 1° marzo al 6 marzo. In entrambi gli esempi, le righe di dati esistenti per le date successive al 6 marzo non vengono eliminate, ma non vengono aggiornate. |
| [!UICONTROL Email Recipients] | Indirizzi e-mail a cui inviare notifiche ogni volta che il report viene aggiornato o ogni volta che il report viene eseguito quando il modello include una pianificazione. Per impostazione predefinita, viene immesso l’indirizzo dell’account utente. Per specificare più indirizzi, separali con virgole, spazi o nuove righe. |
| [!UICONTROL Schedule Time] | L’ora in cui i feed del foglio di calcolo vengono aggiornati: alle ore 08:00 o a qualsiasi ora tra le ore 10:00 e 23:00 nel fuso orario dell’inserzionista. Il valore predefinito per i nuovi feed di fogli di calcolo è 10:00.<br><br><b>Nota:</b> per motivi di prestazioni, non è possibile aggiornare i feed dei fogli di calcolo a 09:00, quando vengono generati altri report. |
| [!UICONTROL Email Notification] | (Quando si specificano i destinatari e-mail) Cosa includere nelle notifiche e-mail a qualsiasi indirizzo specificato:<ul><li><i>Allega feed</i> — Per inviare una copia del report completato in formato XLSX. Se il file supera i 10 MB, la notifica non include un allegato.</li><li><i>Solo notifica</i> (impostazione predefinita): per inviare solo una notifica del completamento o dell&#39;errore del report, con un collegamento al report.</li></ul> |

>[!MORELIKETHIS]
>
>* [Informazioni sui feed di report del foglio di calcolo](spreadsheet-feed-about.md)
>* [Creare un feed di report per fogli di calcolo](spreadsheet-feed-create.md)
>* [Creare un  [!DNL Excel] modello per un feed di report di foglio di calcolo](spreadsheet-feed-create-excel-template.md)
>* [Modifica impostazioni feed report foglio di calcolo](spreadsheet-feed-edit.md)
>* [Visualizzare o salvare un file di feed di report del foglio di calcolo](spreadsheet-feed-view-or-save.md)
>* [Aggiorna manualmente i feed dei report del foglio di calcolo](spreadsheet-feed-refresh.md)
>* [Elimina feed report foglio di calcolo](spreadsheet-feed-delete.md)
