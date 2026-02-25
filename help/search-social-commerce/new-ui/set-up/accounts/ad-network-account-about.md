---
title: (Nuova interfaccia) Informazioni sugli account di rete di annunci
description: Scopri gli account di rete degli annunci nella nuova interfaccia utente di Search, Social e Commerce.
feature: Search Campaign Management
source-git-commit: e62eb730ec88a37cbe34e35d7b9bf99e0d4fd41d
workflow-type: tm+mt
source-wordcount: '518'
ht-degree: 0%

---

# (Nuova interfaccia) Informazioni sugli account di rete di annunci

Search, Social e Commerce possono tenere traccia degli account di un inserzionista sulle reti di annunci supportate. Per abilitare il tracciamento di un account, è necessario creare un record account corrispondente. Devi impostare i dettagli dell’account per qualsiasi tipo di account, indipendentemente dal fatto che Search, Social e Commerce si sincronizzino con esso o ottimizzino offerte e budget sui suoi annunci.

## Account sincronizzati tramite API

*[!DNL Google Ads], [!DNL Microsoft Advertising] (in precedenza [!DNL Bing Ads]), [!DNL Yahoo! Display Network], [!DNL Yahoo! Japan Ads], [!DNL Yandex] e [!DNL Baidu] account esistenti*

Search, Social e Commerce sincronizzano (*syncs*) con account di rete di annunci supportati in modo da poter tenere traccia degli annunci, creare rapporti e visualizzare le prestazioni. Per tutte le reti di annunci eccetto [!DNL Yahoo! Display Network], è possibile gestire facoltativamente le campagne per il proprio account in Search, Social e Commerce; [!DNL Yahoo! Display Network], le campagne sono di sola lettura. Per tutte le reti di annunci, puoi consentire la funzionalità di ottimizzazione per ottimizzare le offerte, il budget delle campagne e i target della strategia di offerta delle campagne per le campagne negli account gestiti, aggiungendo le campagne ai portfolio.

Per abilitare la sincronizzazione di un account, il record account deve contenere le credenziali di accesso all&#39;account ed essere abilitato (attivo).

Durante la sincronizzazione, Search, Social e Commerce richiama le strutture di campagna dell’inserzionista e le entità di campagna supportate, inclusa la maggior parte degli attributi gestiti o segnalati in Search, Social e Commerce. Non include i dati sui clic, né le offerte e i modificatori di offerte immessi all’esterno di Search, Social e Commerce, che vengono raccolti separatamente. Search, Social e Commerce si sincronizzano automaticamente con gli account della rete di annunci una volta al giorno e ogni volta che rileva una nuova campagna su una delle reti di annunci. Inoltre, invia immediatamente alla rete di annunci tutte le modifiche apportate ai dati della campagna dall’interno di Search, Social e Commerce. Se necessario, è possibile richiedere una sincronizzazione manuale.

Per ulteriori informazioni sulla creazione e la modifica di campagne sincronizzate, consulta il capitolo su &quot;Gestione delle campagne&quot;.

## Account per i quali si caricano manualmente i dati

Per le reti di annunci online per le quali Search, Social e Commerce non forniscono supporto API, puoi caricare contenuti della campagna e dati di costo, clic e conversione offline per un account per eseguire report e simulazioni delle prestazioni. Search, Social e Commerce non sincronizzano i dati con la rete di annunci, forniscono offerte automatizzate né forniscono alcun tipo di ottimizzazione, ma consentono di semplificare le informazioni cross-channel e identificare opportunità per l’ottimizzazione manuale.

## Account di solo tracciamento basati su modelli

*Disponibile solo per gli account [!DNL Naver] esistenti*

Le campagne di tracciamento ti consentono di tracciare, creare rapporti e visualizzare le prestazioni per gli annunci acquistati direttamente dalla rete di annunci. Search, Social e Commerce non sincronizzano i dati con la rete di annunci, non forniscono offerte automatizzate né forniscono alcun tipo di ottimizzazione o simulazione.

Per consentire a Search, Social e Commerce di attribuire le conversioni ai clic, imposta le opzioni di tracciamento nel record account e abilita il record account. È quindi possibile utilizzare i bulksheet per generare gli URL di tracciamento per gli annunci e le parole chiave e aggiungere manualmente gli URL di tracciamento all&#39;interno dell&#39;Ad Manager [!DNL Naver].

Non puoi impostare nuovi account [!DNL Naver] in Search, Social e Commerce. Per ulteriori informazioni sulle [!DNL Naver] campagne di sola verifica, vedere &quot;[Implementare [!DNL Naver] account di sola verifica](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md).&quot;

>[!MORELIKETHIS]
>
>* [Gestire gli account di rete tramite la connessione API](/help/search-social-commerce/new-ui/set-up/accounts/api-accounts/api-account-manage.md)
>* [Gestire gli account di rete degli annunci per il caricamento dei dati](/help/search-social-commerce/new-ui/set-up/accounts/data-upload-accounts/data-upload-account-manage.md)
>* [Gestisci [!DNL Naver] account solo per il tracciamento](/help/search-social-commerce/new-ui/set-up/accounts/template-account-manage.md)
>* [Implementa [!DNL Naver] account di sola verifica](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md)
>* [Gestione account centro esercenti](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md)
