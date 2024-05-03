---
title: Modifica gli Schedules per i Posizionamenti
description: Scopri come modificare le pianificazioni degli annunci per gli annunci allegati ai posizionamenti.
feature: DSP Placements
exl-id: 4c981d57-032f-4cde-858a-e9ac2bf2e6f2
source-git-commit: ae1a58bd0aed430cd2914146dfb2850bc8125025
workflow-type: tm+mt
source-wordcount: '439'
ht-degree: 0%

---

# Modifica gli Schedules per i Posizionamenti

## Modificare gli Schedules degli annunci per uno o più posizionamenti

Puoi modificare le date dei voli programmati e la rotazione degli annunci per gli annunci associati a più posizionamenti utilizzando un’ [!DNL Microsoft Excel] foglio di calcolo. Ogni annuncio può essere attivo durante più voli.

1. Nel menu principale, fai clic su **[!UICONTROL Campaigns]**.

1. Fai clic sul nome della campagna.

1. Nel sottomenu, fai clic su **[!UICONTROL Placements]**.

1. Seleziona la casella di controllo accanto a ciascun posizionamento di cui desideri scaricare i dati dell’annuncio.

1. Nella barra degli strumenti Azioni in blocco, fai clic su **[!UICONTROL ...]** > **[!UICONTROL Download Custom Ad Schedule Sheet]**.

1. Quando il file è disponibile, fai clic su **[!UICONTROL Download]** nella notifica nella parte superiore della pagina del browser per scaricare un file del foglio di lavoro (in formato XLSX) in base alla normale procedura del browser.

   ![Scarica notifica pronta](/help/dsp/assets/download-ready.png "Scarica notifica pronta")

1. Apri il file scaricato, modifica i campi delle informazioni sul volo per ogni riga dell’annuncio da includere nel volo e salva il file aggiornato:

   * **[!UICONTROL Flight N Start Date]** / **[!UICONTROL Flight N End Date]** (ad esempio [!UICONTROL Flight 1 Start Date] e [!UICONTROL Flight 1 End Date]): prima e ultima data del volo. Utilizza il formato AAAA-MM-GG per ogni data. Tutti gli annunci con campi di data di volo vuoti vengono trattati come annunci non partecipanti.

   * **[!UICONTROL Flight N Weight]** (ad esempio [!UICONTROL Flight 1 Weight]): come ruotare gli annunci per un volo. Immetti un valore:

      * Per ruotare gli annunci di un volo in modo uniforme, immetti `[!UICONTROL Even]`.

      * Per ruotare gli annunci di un volo in modo non uniforme, immettere il peso relativo in base al quale ruotare ogni annuncio, come percentuale (ad esempio `40` 40%). Il peso totale del volo deve essere pari a 100.

1. Carica il modello di pianificazione modificato:

   1. Selezionare la casella di controllo accanto a ogni posizionamento applicabile.

   1. Nella barra degli strumenti Azioni in blocco, fai clic su **[!UICONTROL ...]** > **[!UICONTROL Upload Custom Ad Schedule Sheet]** e specificare il file da caricare.

## Modificare la pianificazione degli annunci per un singolo posizionamento

<!-- Some placements don't have this option. Clarify which placement types aren't eligible -- just simple ad serving placements (PG ones seem okay)? And anything else? -->

Puoi modificare le date dei voli programmati e la rotazione degli annunci per gli annunci allegati a un posizionamento. Ogni annuncio può essere attivo durante più voli.

1. Nel menu principale, fai clic su **[!UICONTROL Campaigns]**.

1. Fai clic sul nome della campagna.

1. Nel sottomenu, fai clic su **[!UICONTROL Placements]**.

1. Accanto al nome del posizionamento, fate clic su  **[!UICONTROL ...]** > **[!UICONTROL Ad schedule]**.

1. Effettua una delle seguenti operazioni:

   * Per aggiungere un volo, fai clic su **[!UICONTROL Add Flight]** e quindi specificare la data di inizio e la data di fine.

   * Per aggiungere un volo esistente a un annuncio, fai clic su **[!UICONTROL +]** nella riga annuncio per la colonna volo.

   * Per rimuovere un volo esistente da un annuncio, fai clic su **[!UICONTROL x]** nella riga annuncio per la colonna volo.

      * (Quando più annunci hanno lo stesso volo) Per ruotare gli annunci in modo non uniforme, fai clic su **[!UICONTROL Even Rotation]** nelle informazioni sul volo, quindi immettere il peso relativo in base al quale ruotare ogni annuncio, come percentuale.

        Il peso totale deve essere uguale a 100.

1. In alto a destra, fai clic su **[!UICONTROL Continue]**.

1. Rivedi i dettagli del volo, quindi fai clic su **[!UICONTROL Save & Finish]**.

>[!MORELIKETHIS]
>
>* [Informazioni sulla gestione del posizionamento](placement-about.md)
>* [Modifica posizionamenti](placement-edit.md)
>* [Visualizzare il log delle modifiche per un posizionamento](placement-change-log.md)
>* [Impostazioni di posizionamento](placement-settings.md)
