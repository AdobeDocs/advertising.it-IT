---
title: Informazioni sugli account di rete degli annunci
description: Scopri gli account di rete di annunci in Search, Social e Commerce.
exl-id: cb3e650d-721f-48ec-ada3-50bdd7c0375b
feature: Search Campaign Management
source-git-commit: b2d578d0e15e647a57353dbfbde666b5e72d79f2
workflow-type: tm+mt
source-wordcount: '418'
ht-degree: 0%

---

# Informazioni sugli account di rete degli annunci

*Solo i ruoli di account manager agenzia, manager account Adobe e amministratore*

Search, Social e Commerce possono tenere traccia degli account di un inserzionista sulle reti di annunci supportate. Per abilitare il tracciamento di un account, è necessario creare un record account corrispondente. Devi impostare i dettagli dell’account per qualsiasi tipo di account, indipendentemente dal fatto che Search, Social e Commerce si sincronizzino con esso o ottimizzino offerte e budget sui suoi annunci.

## Account sincronizzati tramite API

*[!DNL Google Ads], [!DNL Microsoft Advertising] (in precedenza [!DNL Bing Ads]), [!DNL Yahoo! Display Network], [!DNL Yahoo! Japan Ads], [!DNL Yandex] e [!DNL Baidu] account esistenti*

Search, Social e Commerce sincronizzano (*syncs*) con account di rete di annunci supportati in modo da poter tenere traccia degli annunci, creare rapporti e visualizzare le prestazioni. Per tutte le reti di annunci eccetto [!DNL Yahoo! Display Network], è possibile gestire facoltativamente le campagne per il proprio account in Search, Social e Commerce; [!DNL Yahoo! Display Network], le campagne sono di sola lettura. Per tutte le reti di annunci, puoi consentire la funzionalità di ottimizzazione delle offerte sugli annunci negli account gestiti aggiungendole ai portfolio.

Per abilitare la sincronizzazione di un account, il record account deve contenere le credenziali di accesso all&#39;account ed essere abilitato (attivo).

Durante la sincronizzazione, Search, Social e Commerce richiama le strutture di campagna dell’inserzionista e le entità di campagna supportate, inclusa la maggior parte degli attributi gestiti o segnalati in Search, Social e Commerce. Non include i dati sui clic, né le offerte e i modificatori di offerte immessi all’esterno di Search, Social e Commerce, che vengono raccolti separatamente. Search, Social e Commerce si sincronizzano automaticamente con gli account della rete di annunci una volta al giorno e ogni volta che rileva una nuova campagna su una delle reti di annunci. Inoltre, invia immediatamente alla rete di annunci tutte le modifiche apportate ai dati della campagna dall’interno di Search, Social e Commerce. Se necessario, è possibile richiedere una sincronizzazione manuale.

Per ulteriori informazioni sulla creazione e la modifica di campagne sincronizzate, consulta il capitolo su &quot;Campaign Management&quot;.

## Account di solo tracciamento

*[!DNL Naver]account*

Le campagne di tracciamento ti consentono di tracciare, creare rapporti e visualizzare le prestazioni per gli annunci acquistati direttamente dalla rete di annunci. Search, Social e Commerce non sincronizzano i dati con la rete di annunci, non fanno offerte per l’account e non forniscono alcun tipo di ottimizzazione o simulazione.

Per consentire a Search, Social e Commerce di attribuire le conversioni ai clic, imposta le opzioni di tracciamento nel record account e abilita il record account. È quindi possibile utilizzare i bulksheet per generare gli URL di tracciamento per gli annunci e le parole chiave e aggiungere manualmente gli URL di tracciamento all&#39;interno dell&#39;Ad Manager [!DNL Naver].

Per ulteriori informazioni sulle [!DNL Naver] campagne di sola verifica, vedere &quot;[Implementare [!DNL Naver] account di sola verifica](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md).&quot;

>[!MORELIKETHIS]
>
>* [Gestione account di rete pubblicitaria](ad-network-account-manage.md)
>* [Gestione account centro esercenti](merchant-account-manage.md)
>* [Aggiorna il codice di tracciamento AMO ID per un [!DNL Google Ads] account](update-amo-id-google.md)
