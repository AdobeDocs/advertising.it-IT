---
title: Informazioni sugli account di rete degli annunci
description: Scopri di più sugli account di rete di annunci in Search, Social e Commerce.
exl-id: fca469f1-502c-415a-897d-03b6e6ba34e8
feature: Search Campaign Management
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '417'
ht-degree: 0%

---

# Informazioni sugli account di rete degli annunci

*Solo i ruoli utente Responsabile account agenzia, Responsabile account Adobe e Amministratore*

Search, Social e Commerce possono tracciare qualsiasi account dell’inserzionista sulle reti pubblicitarie supportate. Per abilitare il tracciamento di un account, è necessario creare un record account corrispondente. Devi impostare i dettagli dell’account per qualsiasi tipo di account, indipendentemente dal fatto che Search, Social e Commerce si sincronizzino con esso o ottimizzino offerte e budget sui suoi annunci.

## Account sincronizzati tramite API

*[!DNL Baidu], [!DNL Google Ads], [!DNL Microsoft Advertising] (in precedenza [!DNL Bing Ads]), [!DNL Yahoo! Display Network], [!DNL Yahoo! Japan Ads], e [!DNL Yandex] account*

Sincronizzazioni di Search, Social e Commerce (*sincronizza*) con account di rete di annunci supportati per monitorare, creare rapporti e visualizzare le prestazioni degli annunci. Per tutte le reti pubblicitarie ad eccezione di [!DNL Yahoo! Display Network], puoi facoltativamente gestire le campagne per il tuo account in Search, Social e Commerce; [!DNL Yahoo! Display Network], le campagne sono di sola lettura. Per tutte le reti di annunci, puoi consentire la funzionalità di ottimizzazione delle offerte sugli annunci negli account gestiti aggiungendole ai portfolio.

Per abilitare la sincronizzazione di un account, il record account deve contenere le credenziali di accesso all&#39;account ed essere abilitato (attivo).

Durante la sincronizzazione, Search, Social e Commerce richiama le strutture di campagna dell’inserzionista e le entità di campagna supportate, inclusa la maggior parte degli attributi gestiti o segnalati in Search, Social e Commerce. Non include i dati di clic, né le offerte e i modificatori di offerte immessi al di fuori di Search, Social e Commerce, che vengono raccolti separatamente. Search, Social e Commerce si sincronizzano automaticamente con gli account della tua rete di annunci una volta al giorno e anche ogni volta che rileva una nuova campagna su una delle tue reti di annunci. Inoltre, invia immediatamente alla rete di annunci tutte le modifiche apportate ai dati della campagna da Search, Social e Commerce. Se necessario, è possibile richiedere una sincronizzazione manuale.

Per ulteriori informazioni sulla creazione e la modifica di campagne sincronizzate, consulta il capitolo su &quot;Campaign Management&quot;.

## Account di solo tracciamento

*[!DNL Naver]Account*

Le campagne di tracciamento ti consentono di tracciare, creare rapporti e visualizzare le prestazioni per gli annunci acquistati direttamente dalla rete di annunci. Search, Social e Commerce non sincronizzano i dati con la rete di annunci, non fanno offerte per l’account e non forniscono alcun tipo di ottimizzazione o simulazione.

Per consentire a Search, Social e Commerce di attribuire le conversioni ai clic, imposta le opzioni di tracciamento nel record account e abilita il record account. Puoi quindi utilizzare i bulksheet per generare URL di tracciamento per annunci e parole chiave e aggiungere manualmente gli URL di tracciamento all’interno di [!DNL Naver] ad manager.

Ulteriori informazioni su [!DNL Naver] campagne di solo tracciamento, consulta &quot;[Implementare [!DNL Naver] account di solo tracciamento](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md).&quot;

>[!MORELIKETHIS]
>
>* [Gestire gli account di rete degli annunci](ad-network-account-manage.md)
>* [Gestisci account centro esercenti](merchant-account-manage.md)
>* [Aggiorna il codice di tracciamento s\_kwcid per un [!DNL Google Ads] account](update-skwcid-google.md)
