---
title: Le attività di configurazione iniziali per i rapporti
description: Scopri come rendere le metriche disponibili nei rapporti e come automatizzare i rapporti.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '331'
ht-degree: 0%

---

# Le attività di configurazione iniziali per i rapporti

I nuovi utenti devono eseguire le seguenti attività di configurazione iniziale:

* Rendi le proprietà della transazione di cui Adobe Advertising tiene traccia per un inserzionista [disponibile per rapporti e altre visualizzazioni](/help/search-social-commerce/admin/transaction-properties/transaction-property-edit-available.md), e facoltativamente [rinominare uno dei nomi di proprietà](/help/search-social-commerce/admin/transaction-properties/transaction-property-edit-display-name.md) che vengono visualizzate nelle intestazioni di colonna per migliorarne la leggibilità.

   Le proprietà delle transazioni non sono disponibili per i rapporti, a meno che non vengano rese specificamente disponibili.

   Se in seguito si inizia a tenere traccia di una nuova proprietà di transazione, sarà necessario ripetere l&#39;attività.

* (Facoltativo) Generazione automatica dei rapporti:

   * Se desideri generare regolarmente i dati del rapporto per un incremento di tempo specifico, ad esempio [!UICONTROL Campaign Report] nell&#39;ultima settimana o negli ultimi 30 giorni, puoi impostare [modelli di rapporto](/help/search-social-commerce/reports/automation/templates/template-about.md) e pianificarle in modo che vengano eseguite ogni giorno o in un giorno specifico della settimana o del mese. Ogni volta che è pianificata l’esecuzione del rapporto, viene generato un nuovo rapporto. È possibile notificare gli indirizzi e-mail di specifici utenti di Search, Social e Commerce quando il report viene completato, in base al [impostazioni di notifica configurate in [!UICONTROL Notification Center]](/help/search-social-commerce/notifications/notification-about.md).

   * Se si desidera visualizzare i dati dei report giornalieri aggiornati in un foglio di calcolo personalizzato, con o senza tabelle pivot e colonne aggiuntive necessarie per eseguire ulteriori calcoli, è possibile impostare un&#39;opzione giornaliera [feed foglio di calcolo](/help/search-social-commerce/reports/automation/spreadsheet-feeds/spreadsheet-feed-about.md). I feed dei fogli di calcolo vengono aggiornati quotidianamente con i dati sulle prestazioni più recenti e continuano a conservare i dati per le date precedenti. Per configurare i feed dei fogli di calcolo, devi prima creare un modello di foglio di calcolo personalizzato in [!DNL Microsoft Excel]. È possibile notificare gli indirizzi e-mail di specifici utenti di Search, Social e Commerce quando un file di feed è disponibile, in base al [impostazioni di notifica configurate in [!UICONTROL Notification Center]](/help/search-social-commerce/notifications/notification-about.md).

   * Se desideri ricevere report di base e avanzati in una posizione FTP, puoi impostare [Accesso FTP ai report di base e avanzati](/help/search-social-commerce/reports/automation/ftp-reports.md) richiedendo un account FTP e configurando modelli di rapporto utilizzando una convenzione di denominazione specifica.

>[!MORELIKETHIS]
>
>* [Informazioni sui report](report-about.md)
>* [Dati utilizzati per i rapporti](data-used-for-reports.md)

