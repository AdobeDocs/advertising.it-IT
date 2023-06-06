---
title: Impostazioni feed report foglio di calcolo
description: Scopri le impostazioni per i feed di fogli di calcolo.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '492'
ht-degree: 0%

---

# Impostazioni feed report foglio di calcolo

| Campo | Descrizione |
|---|---|
| [!UICONTROL Feed Name] | Un nome per il feed del foglio di calcolo. |
| [!UICONTROL Report Template] | Il modello di report che specifica i dati del report richiesti; seleziona quello utilizzato per creare il [!DNL Excel] modello. Sono elencati tutti i modelli di report di base.<br><br><b>Nota:</b> Se modifichi il modello di rapporto utilizzato per il rapporto o aggiorni le colonne nel modello, devi creare e caricare un nuovo [!DNL Excel] modello. |
| [!UICONTROL Excel Template] | Il formato speciale [!DNL Excel] modello creato in formato .XLSX, applicato ai dati specificati nel modello di report. Specificare il file da caricare immettendo il percorso completo e il nome del file oppure facendo clic su <b>[!UICONTROL Browse]</b> per individuare il file sul dispositivo o sulla rete. |
| [!UICONTROL Back Fill From] | La data di inizio per la quale i dati esistenti sul [!UICONTROL RAW] viene aggiornata e viene rappresentato da un numero di giorni nel passato. Immetti un valore massimo di 90 giorni; il valore predefinito è sette (7) giorni.<br><br>Ad esempio, se il valore è 7 e oggi è 7 marzo, i dati esistenti sul [!UICONTROL RAW] viene aggiornata la scheda che inizia con 1 marzo (fino alla data di fine specificata da [!UICONTROL Back Fill Until] parametro ). Le righe di dati esistenti per le date precedenti al 1° marzo non vengono eliminate, ma non vengono aggiornate. |
| [!UICONTROL Back Fill Until] | La data di fine per la quale i dati esistenti sul [!UICONTROL RAW] viene aggiornata e viene rappresentato da un numero di giorni nel passato. Il valore predefinito è un (1) giorno.<br><br>Ad esempio, se questo valore è 1 e oggi è 7 marzo, i dati esistenti sul [!UICONTROL RAW] viene aggiornata fino al 6 marzo (e a partire dalla data di inizio specificata da [!UICONTROL Back Fill From] parametro ). Se questo valore è 1, il [!UICONTROL Back Fill Until] 7, e oggi è il 7 marzo, quindi i dati esistenti sul [!UICONTROL RAW] La scheda viene aggiornata dal 1° marzo al 6 marzo. In entrambi gli esempi, le righe di dati esistenti per le date successive al 6 marzo non vengono eliminate, ma non vengono aggiornate. |
| [!UICONTROL Email Recipients] | Indirizzi e-mail a cui inviare notifiche ogni volta che il report viene aggiornato o ogni volta che il report viene eseguito quando il modello include una pianificazione. Per impostazione predefinita, viene immesso l’indirizzo dell’account utente. Per specificare più indirizzi, separali con virgole, spazi o nuove righe. |
| [!UICONTROL Schedule Time] | L’ora in cui i feed del foglio di calcolo vengono aggiornati: alle 08:00 o a qualsiasi ora tra le 10:00 e le 23:00 nel fuso orario dell’inserzionista. Il valore predefinito per i nuovi feed di fogli di calcolo è 10:00.<br><br><b>Nota:</b> Per motivi di prestazioni, non è possibile aggiornare i feed dei fogli di calcolo alle 09:00 quando vengono generati altri rapporti. |
| [!UICONTROL Email Notification] | (Quando si specificano i destinatari e-mail) Cosa includere nelle notifiche e-mail a qualsiasi indirizzo specificato:<ul><li><i>Allega feed</i> — Per inviare una copia del report completato in formato XLSX. Se il file supera i 10 MB, la notifica non include un allegato.</li><li><i>Solo notifica</i> (impostazione predefinita) - Per inviare solo una notifica del completamento o del fallimento del report, con un collegamento al report.</li></ul> |

>[!MORELIKETHIS]
>
>* [Informazioni sui feed di report dei fogli di calcolo](spreadsheet-feed-about.md)
>* [Creare un feed di report per fogli di calcolo](spreadsheet-feed-create.md)
>* [Creare un [!DNL Excel] modello per un feed di report per fogli di calcolo](spreadsheet-feed-create-excel-template.md)
>* [Modifica impostazioni feed report foglio di calcolo](spreadsheet-feed-edit.md)
>* [Visualizzare o salvare un file di feed di report del foglio di calcolo](spreadsheet-feed-view-or-save.md)
>* [Aggiorna manualmente i feed dei rapporti del foglio di calcolo](spreadsheet-feed-refresh.md)
>* [Eliminare i feed dei report del foglio di calcolo](spreadsheet-feed-delete.md)

