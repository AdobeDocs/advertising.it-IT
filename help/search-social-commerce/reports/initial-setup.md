---
title: Le attività di configurazione iniziali per i rapporti
description: Scopri come rendere le metriche disponibili nei rapporti e come automatizzare i rapporti.
exl-id: c2e76c63-ddb8-4762-8628-30cf3f54b8fd
feature: Search Reports
source-git-commit: 724b4ff772fa7d6dc0640d35a968d664707ceae6
workflow-type: tm+mt
source-wordcount: '336'
ht-degree: 0%

---

# Le attività di configurazione iniziali per i rapporti

I nuovi utenti devono eseguire le seguenti attività di configurazione iniziale:

* Rendi le metriche di conversione di cui Adobe Advertising tiene traccia per un inserzionista [disponibili per i rapporti e altre visualizzazioni](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-edit-available.md) e, facoltativamente, [rinomina una delle metriche di conversione](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-edit-display-name.md) visualizzate nelle intestazioni di colonna per migliorarne la leggibilità.

  Le proprietà delle transazioni non sono disponibili per i rapporti, a meno che non vengano rese specificamente disponibili.

  Se in seguito inizierai a tenere traccia di una nuova metrica di conversione, dovrai ripetere questa attività.

* (Facoltativo) Generazione automatica dei rapporti:

   * Se si desidera generare regolarmente i dati del report per un incremento di tempo specifico, ad esempio [!UICONTROL Campaign Report] per l&#39;ultima settimana o gli ultimi 30 giorni, è possibile impostare [modelli di report](/help/search-social-commerce/reports/automation/templates/template-about.md) e pianificarne l&#39;esecuzione giornaliera o in un giorno specifico della settimana o del mese. Ogni volta che è pianificata l’esecuzione del rapporto, viene generato un nuovo rapporto. È possibile notificare gli indirizzi di posta elettronica di specifici utenti di Search, Social e Commerce al completamento del report, in base alle [impostazioni di notifica configurate in [!UICONTROL Notification Center]](/help/search-social-commerce/notifications/notification-about.md).

   * Se si desidera visualizzare i dati aggiornati dei report giornalieri in un foglio di calcolo personalizzato, con o senza tabelle pivot e colonne aggiuntive, è necessario eseguire ulteriori calcoli, è possibile impostare un [feed di fogli di calcolo](/help/search-social-commerce/reports/automation/spreadsheet-feeds/spreadsheet-feed-about.md) giornaliero. I feed dei fogli di calcolo vengono aggiornati quotidianamente con i dati sulle prestazioni più recenti e continuano a conservare i dati per le date precedenti. Per configurare i feed del foglio di calcolo, è innanzitutto necessario creare un modello di foglio di calcolo personalizzato in [!DNL Microsoft Excel]. È possibile notificare gli indirizzi di posta elettronica di specifici utenti di Search, Social e Commerce quando è disponibile un file di feed, in base alle [impostazioni di notifica configurate in [!UICONTROL Notification Center]](/help/search-social-commerce/notifications/notification-about.md).

   * Se desideri ricevere report di base e avanzati in una posizione FTP, puoi impostare l&#39;accesso [FTP ai report di base e avanzati](/help/search-social-commerce/reports/automation/ftp-reports.md) richiedendo un account FTP e configurando i modelli di report utilizzando una convenzione di denominazione specifica.

>[!MORELIKETHIS]
>
>* [Informazioni sui report](report-about.md)
>* [Dati utilizzati per i report](data-used-for-reports.md)
