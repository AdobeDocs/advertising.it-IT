---
title: (Nuova interfaccia) Convalida delle pagine di destinazione in file bulksheet
description: Scopri come convalidare gli URL di destinazione in un file di bulksheet per un singolo account nella nuova interfaccia utente di Search, Social e Commerce.
feature: Search Bulksheets
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
subfeature_v2:
  - id: e58024d1-d6da-420c-80af-6be211808316
  - id: f3d33161-c519-436e-bbbd-730ba428736b
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: f916f47a40729ff39ac1456e3b3ad93e1045e9a9
workflow-type: tm+mt
source-wordcount: 585
ht-degree: 0%

---

# (Nuova interfaccia) Convalida delle pagine di destinazione in file bulksheet

*Account con solo URL di destinazione*

Puoi convalidare le pagine di destinazione in tutti gli URL di destinazione in un file di bulksheet a account singolo. Puoi specificare qualsiasi frase e URL che indichi una pagina non valida e, facoltativamente, segnalare i reindirizzamenti della pagina di destinazione come errori. Search, Social e Commerce verificano le condizioni specificate e le pagine di destinazione mancanti (con conseguente errore HTTP 404 o &quot;Non trovato&quot;).

Quando vengono rilevati errori, in Ricerca, Social e Commerce viene creato un file di errore bulksheet che include tutte le righe del bulksheet originale e messaggi di errore per tutte le righe con pagine di destinazione non valide. Gli errori sono riportati nella colonna [!UICONTROL EF Errors]. Convenzione nome file: `<bulksheet name>__lpv_errors.<extension used for the bulksheet>`.

Successivamente puoi scaricare il file, correggere gli errori e caricare il file corretto, quindi pubblicare il file corretto sull’account di rete dell’annuncio.

>[!NOTE]
>
>* Questa funzione non convalida i valori nella colonna URL di base/URL finale.
>* È possibile pubblicare i file di bulksheet durante la convalida o anche in caso di errori.

>[!IMPORTANT]
>
>Il supporto per i caratteri non ASCII nella convalida della pagina di destinazione è stato temporaneamente sospeso. Se gli URL della pagina di destinazione contengono caratteri non ASCII, contatta il supporto tecnico per assistenza.

1. Nel menu principale, fare clic su **[!UICONTROL Setup]** \> **[!UICONTROL Bulksheets]**.

1. Selezionare la casella di controllo accanto a ogni file da convalidare.

   >[!NOTE]
   >
   >È possibile convalidare solo i bulksheet EF a account singolo che non sono attualmente in corso. Se si seleziona un bulksheet con più conti o un bulksheet attualmente in fase di elaborazione, tali file vengono esclusi.

1. Nella barra delle azioni fare clic su **[!UICONTROL Validate URLs]**.

1. Nella finestra di dialogo immettere le informazioni nei campi, quindi fare clic su **[!UICONTROL Apply]**:

   **[!UICONTROL Enter case-sensitive text or phrases that indicate an invalid page (one per line):]** Testo nel corpo di una pagina di destinazione che indica che la pagina non è valida. Per specificare più valori, immetterli su righe separate.

   **[!UICONTROL Enter invalid landing pages (one per line):]** URL di pagine non valide come pagine di destinazione. Per specificare più valori, immetterli su righe separate.

   **[!UICONTROL User Agent:]** Identificazione dell&#39;agente di convalida della pagina di destinazione nel server Web in cui si trova la pagina di destinazione. Il valore predefinito è `default`, che attribuisce le visualizzazioni dell&#39;agente a un utente anonimo [!DNL Mozilla Firefox]. Se il server Web blocca le richieste di [!DNL Mozilla Firefox] utenti anonimi, immettere il nome di un agente diverso. Ad esempio, per [!DNL Googlebot], immettere `Googlebot/2.1;+http://www.google.com/bot.html`.

   **[!UICONTROL Report redirects as errors]:** Quando una pagina di destinazione viene reindirizzata a un&#39;altra pagina (ad esempio, se la pagina di destinazione risulta mancante e il sito visualizza una pagina sostitutiva), la colonna [!UICONTROL EF Errors] nel file di errore della pagina di destinazione indica l&#39;URL a cui viene reindirizzata la pagina di destinazione.

Quando l&#39;attività inizia, viene aggiunta una nuova riga alla visualizzazione [!UICONTROL Bulksheets]. Quando le notifiche e-mail per i bulksheet sono abilitate per [&#x200B; in [!UICONTROL Notification Center]](/help/search-social-commerce/new-ui/notifications/notification-manage.md), al momento della creazione del file viene inviata una notifica e-mail con un collegamento al file. A seconda della quantità di dati compilati, la notifica e-mail potrebbe richiedere alcuni minuti o più. Puoi scaricare il file per modificarlo e quindi ricaricarlo per la pubblicazione, oppure puoi pubblicare il file così com’è.

>[!NOTE]
>
>* La convalida dei file di grandi dimensioni richiede più tempo.
>* I file di bulksheet per più campagne possono contenere fino a 500.000 righe di dati. Se si generano dati per più campagne e i dati combinati sono costituiti da più di 500.000 righe, i dati vengono suddivisi per campagna in due o più file denominati `<bulksheet name>_1.tsv`, `<bulksheet name>_2.tsv` e così via.

>[!MORELIKETHIS]
>
>* [(Nuova interfaccia) Informazioni sulla gestione dei dati della campagna tramite bulksheet](about.md)
>* [(Nuova interfaccia) Carica un bulksheet o un file di errore corretto](upload.md)
>* [(Nuova interfaccia) Pubblica i bulksheet o correggi i file di errore](post.md)
>* [(Nuova interfaccia) Elimina i bulksheet caricati e i file di errore](delete.md)
>* [(Nuova interfaccia) Interruzione di un processo bulksheet in corso](stop-job.md)
