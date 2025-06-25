---
title: Generare un report di base o un report avanzato
description: Scopri come generare un rapporto di base o avanzato personalizzato.
exl-id: 529a35f5-517f-4bde-b752-c0afc6346f4b
feature: Search Reports, Search Basic Reports, Search Advanced Reports
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '391'
ht-degree: 0%

---

# Generare un report di base o un report avanzato

1. Nel menu principale, fare clic su **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Insights & Reports] >[!UICONTROL Reports]**.

1. Nella barra degli strumenti sopra la tabella dati fare clic su **[!UICONTROL Create Report]**, tenere premuto il cursore su **[!UICONTROL Basic Reports]** o **[!UICONTROL Advanced Reports]** e quindi fare clic sul tipo di report [](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-about.md).

1. (Facoltativo) Nella finestra [!UICONTROL Report Settings], modifica le [impostazioni report](basic-advanced-report-settings.md) predefinite:

   1. (Facoltativo) Inserire un nome personalizzato per il rapporto e per il modello (se si salva il rapporto come modello).

   1. (Facoltativo) Per salvare le impostazioni del report come modello, selezionare la casella di controllo accanto a **[!UICONTROL Save as template]**.

   1. (Facoltativo) Nella scheda **[!UICONTROL Basic Settings]**, selezionare un modello di report esistente da utilizzare o modificare le impostazioni di base predefinite per il report.

   1. (Facoltativo) Fare clic su **[!UICONTROL Columns tab]** e modificare le colonne predefinite nel report.

      Per impostazione predefinita, tutti i dati monetari nei rapporti vengono visualizzati nel formato del dollaro statunitense (ad esempio 1.000,00). Per visualizzare il valore nel formato di valuta corretto (ma senza simboli di valuta nei formati CSV e TSV), aggiungere la colonna &quot;[!UICONTROL Currency]&quot; al rapporto. Se il report include dati per conti con valute diverse, tutti i valori monetari &quot;[!UICONTROL Total]&quot; sono la somma di tutti i numeri nella colonna, indipendentemente dalla valuta.

   1. (Facoltativo; solo [!UICONTROL Campaign Report], [!UICONTROL Ad Group Report], [!UICONTROL Ad Variation Report], [!UICONTROL Keyword Report] e [!UICONTROL Label Classification Report]) Fare clic sulla scheda **[!UICONTROL Classifications]** e limitare i risultati del report in modo che includano solo classificazioni di etichette specifiche.

   1. (Facoltativo) Fare clic sulla scheda **[!UICONTROL Advanced Filters]** e modificare le opzioni avanzate predefinite.

   1. (Facoltativo) Fare clic sulla scheda **[!UICONTROL Attribution]** e modificare la regola di attribuzione predefinita.

   1. (Facoltativo) Fare clic sulla scheda **[!UICONTROL Scheduling and Delivery]** e modificare le opzioni di pianificazione e consegna predefinite.

1. (Facoltativo se disponibile) Per visualizzare in anteprima le prime 50 righe del report, fare clic su **[!UICONTROL Preview]**. Al termine, fare clic su **[!UICONTROL Back]** per tornare alla pagina delle impostazioni del report.

   >[!NOTE]
   >
   >Il pulsante Anteprima è disponibile per tutti i report di base e avanzati ad eccezione di [!UICONTROL Campaign Hourly Report], [!UICONTROL Ad Variation Report], [!UICONTROL Keyword Report], [!UICONTROL Domain Referral Report] e [!UICONTROL Transaction Report].

1. Fare clic su **[!UICONTROL Create]**.

Se non è stata specificata una pianificazione, il report viene eseguito immediatamente; in caso contrario, viene eseguito in base alla pianificazione specificata. Il nome del report viene aggiunto alla visualizzazione [[!UICONTROL Latest Reports]](/help/search-social-commerce/reports/report-about.md). Se il report è stato salvato come modello, verrà aggiunto anche alla visualizzazione [[!UICONTROL Templates]](/help/search-social-commerce/reports/report-about.md). Una volta completato il report, il file è disponibile per l&#39;apertura o il salvataggio; i modelli sono disponibili immediatamente.

Se hai immesso indirizzi e-mail per la notifica, ogni destinatario riceve una notifica quando il processo di report viene completato o non riesce, in base alle [impostazioni di notifica configurate](/help/search-social-commerce/notifications/notification-edit.md) dell&#39;utente per i report.

>[!MORELIKETHIS]
>
>* [Informazioni sui report di base e avanzati](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-about.md)
>* [Impostazioni di base e avanzate del report](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-settings.md)
>* [Colonne report per report di base e avanzati](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-columns.md)
>* [Elimina report](/help/search-social-commerce/reports/management/report-delete.md)
