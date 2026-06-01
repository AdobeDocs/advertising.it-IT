---
title: (Nuova interfaccia) Le attività di configurazione iniziali per i rapporti
description: Scopri come rendere le metriche disponibili nei rapporti e come automatizzare i rapporti.
feature: Search Reports
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
subfeature_v2:
  - id: e246c273-d720-4ece-b29b-7aaba7d50169
source-git-commit: 18f4c5afafd63a6ae9421bf80b4e5b5fd424ed86
workflow-type: tm+mt
source-wordcount: 357
ht-degree: 0%

---

# (Nuova interfaccia) Le attività di configurazione iniziali per i rapporti

I nuovi utenti devono eseguire le seguenti attività di configurazione iniziale:

* Rendi le metriche di conversione che Adobe Advertising sta tracciando per un inserzionista disponibili per i rapporti e altre visualizzazioni e, facoltativamente, rinomina una qualsiasi delle metriche di conversione visualizzate nelle intestazioni di colonna per migliorarne la leggibilità. Consulta &quot;[Gestire e visualizzare i dati sulle prestazioni per le metriche di conversione di un inserzionista](/help/search-social-commerce/new-ui/goals/conversions/conversion-metrics-manage.md).&quot;

  Le proprietà delle transazioni non sono disponibili per i rapporti, a meno che non vengano rese specificamente disponibili.

  Se in seguito inizierai a tenere traccia di una nuova metrica di conversione, dovrai ripetere questa attività.

* (Facoltativo) Generazione automatica dei rapporti:

   * Se si desidera generare regolarmente i dati del report per un incremento di tempo specifico, ad esempio [!UICONTROL Campaign Report] per l&#39;ultima settimana o gli ultimi 30 giorni, è possibile impostare [modelli di report](report-templates-manage.md) e pianificarne l&#39;esecuzione giornaliera o in un giorno specifico della settimana o del mese. Ogni volta che è pianificata l’esecuzione del rapporto, viene generato un nuovo rapporto. È possibile notificare gli indirizzi di posta elettronica di specifici utenti di Search, Social e Commerce quando il report viene completato, in base alle [impostazioni di notifica configurate in [!UICONTROL Notification Center]][Manage custom alerts]&#x200B;(/help/search-social-commerce/new-ui/notifications-manage.md).

   * Se si desidera visualizzare i dati aggiornati dei report giornalieri in un foglio di calcolo personalizzato, con o senza tabelle pivot e colonne aggiuntive, è necessario eseguire ulteriori calcoli, è possibile impostare un [feed di fogli di calcolo](/help/search-social-commerce/reports/automation/spreadsheet-feeds/spreadsheet-feed-about.md) giornaliero. I feed dei fogli di calcolo vengono aggiornati quotidianamente con i dati sulle prestazioni più recenti e continuano a conservare i dati per le date precedenti. Per configurare i feed del foglio di calcolo, è innanzitutto necessario creare un modello di foglio di calcolo personalizzato in [!DNL Microsoft Excel]. È possibile notificare gli indirizzi di posta elettronica di specifici utenti di Search, Social e Commerce quando è disponibile un file di feed, in base alle [impostazioni di notifica configurate in [!UICONTROL Notification Center]](/help/search-social-commerce/new-ui/notifications-manage.md).

   * Se desideri ricevere report di base e avanzati in una posizione FTP, puoi impostare l&#39;accesso [FTP ai report di base e avanzati](/help/search-social-commerce/new-ui/reports/ftp-reports.md) richiedendo un account FTP e configurando i modelli di report utilizzando una convenzione di denominazione specifica.

>[!MORELIKETHIS]
>
>* [Informazioni sui report](report-about.md)
>* [Dati utilizzati per i report](data-used-for-reports.md)
