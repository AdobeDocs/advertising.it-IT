---
title: Informazioni sull’automazione della gestione degli annunci tramite i feed di inventario
description: Scopri il flusso di lavoro per gestire automaticamente la struttura dei conti e distribuire annunci dinamici in base ai dati sull’inventario di prodotti o servizi.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '413'
ht-degree: 0%

---

# Flusso di lavoro per la gestione dei dati della campagna tramite i feed di inventario

*[!DNL Google Ads], [!DNL Microsoft® Advertising], [!DNL Yahoo! Japan Ads] (solo azioni di eliminazione), e [!DNL Yandex] solo account*

Inizialmente, eseguire il test di almeno un file di feed o un account, quindi automatizzare completamente il processo o continuare a controllarlo in ogni passaggio:

1. (Facoltativo) Contatta il team dell’account Adobe per impostare una directory FTP per il deposito dei file di dati.

   Se si utilizza la directory FTP, il servizio di feed verifica la presenza di nuovi file ogni due ore.

   In caso contrario, puoi caricare manualmente i file nel [!UICONTROL Advanced (ACM)] visualizzazione.

1. Imposta [parametri per l’elaborazione dei dati di feed](feed-settings-manage.md#feed-data-settings).

   Se utilizzi l’FTP, non inviare automaticamente i dati alle reti di annunci inizialmente. Dopo aver verificato l’output del primo file e aver ottenuto i risultati desiderati, puoi modificare le impostazioni.

1. Caricare un file di dati nella directory FTP, [caricare manualmente un file di dati](feed-files-manage.md) nel [!UICONTROL Advanced (ACM) view], o [abilitare l&#39;accesso a un account Google o Microsoft® merchant center](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md).

Per caricare manualmente i file, puoi attendere finché non crei un modello che utilizza il file di dati.

1. (Facoltativo) Crea gruppi di [modificatori](modifiers-manage.md) da utilizzare come variabili in vari campi di dati nei modelli di dati dei feed.

1. [Creare uno o più modelli](ad-templates/ad-template-manage.md) che utilizzano le colonne di dati per creare campagne, gruppi di annunci, parole chiave e/o copie di annunci per un account di rete di annunci specifico.

1. [Propagazione dei dati di feed tramite i modelli](feed-data-propagate.md), che sostituisce i nomi delle colonne nel modello con i dati nel file o nel conto. A seconda delle opzioni del modello, Cerca, Social e Commerce crea una nuova struttura di account (campagne, gruppi di annunci, parole chiave) per gli annunci utilizzando le impostazioni predefinite oppure mappa gli annunci alla struttura di account esistente.

1. (Facoltativo) [Anteprima dell’output](propagated-data-view.md) nel [!UICONTROL Advanced (ACM)] e, se lo si desidera, visualizzare un riepilogo delle modifiche apportate ai dati [!UICONTROL Propagations] scheda.

1. [Pubblica i dati](propagated-data-post.md) ai pertinenti account di rete pubblicitaria.

1. (Se per caricare i dati utilizzi l’FTP o un account del centro commerciale, facoltativo) Dopo aver convalidato l’output del primo file di feed, [modificare i parametri](feed-settings-manage.md#feed-data-settings) per propagare automaticamente i dati successivi tramite i modelli associati e inviarli alle reti di annunci pertinenti.

1. (Quando disponi di nuovi file di dati) Se necessario, carica nuovi file, propaga i dati tramite modelli e invia i dati alla rete di annunci pertinente. Facoltativamente, puoi propagare e pubblicare i dati in un unico passaggio.

>[!MORELIKETHIS]
>
>* [Informazioni sull’automazione della gestione degli annunci tramite i feed di inventario](inventory-feeds-about.md)
>* [Quando vengono creati o eliminati i componenti del conto dai feed di inventario?](when-are-components-created-deleted.md)

