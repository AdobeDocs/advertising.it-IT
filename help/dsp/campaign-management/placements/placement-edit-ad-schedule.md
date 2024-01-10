---
title: Modifica gli Schedules per i Posizionamenti
description: Scopri come modificare le pianificazioni degli annunci per gli annunci allegati ai posizionamenti.
feature: DSP Placements
exl-id: 4c981d57-032f-4cde-858a-e9ac2bf2e6f2
source-git-commit: d993ffe4a7dceed36ecbae85642e82de271432cd
workflow-type: tm+mt
source-wordcount: '470'
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

1. Apri il file scaricato, modifica le informazioni sul volo in base alle esigenze e salva il file aggiornato:

   * Per aggiungere un volo, specifica le date del volo per ogni riga di annuncio da includere nel volo utilizzando **[!UICONTROL Flight N Start Date]** e **[!UICONTROL Flight N End Date]** colonne. Utilizza il formato AAAA-MM-GG per ogni data.

     Ad esempio, per gli annunci del primo volo, inserisci i valori nel campo [!UICONTROL Flight 1 Start Date] e [!UICONTROL Flight 1 End Date] campi. Se le righe dell’annuncio non sono già incluse nel file, inserisci le informazioni richieste nelle nuove righe.

     Tutti gli annunci con campi di data di volo vuoti vengono trattati come annunci non partecipanti.

   * Per ruotare gli annunci di un volo in modo uniforme, immetti &quot;**[!UICONTROL Even]**&quot; nella relativa **[!UICONTROL Flight N Weight]** campi (come [!UICONTROL Flight 1 Weight]).

   * Per ruotare gli annunci di un volo in modo non uniforme, immettere il peso relativo di cui ruotare ogni annuncio, come percentuale, nel relativo **[!UICONTROL Flight N Weight]** campi (come [!UICONTROL Flight 1 Weight]).

     I pesi totali per ciascun volo devono essere pari a 100.

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
>* [Modificare un posizionamento](placement-edit.md)
>* [Visualizzare il log delle modifiche per un posizionamento](placement-change-log.md)
>* [Impostazioni di posizionamento](placement-settings.md)
