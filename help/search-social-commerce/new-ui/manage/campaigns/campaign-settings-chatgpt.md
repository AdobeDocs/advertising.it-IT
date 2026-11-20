---
title: '[!DNL ChatGPT Ads] impostazioni campagna'
description: Fai riferimento alle impostazioni per [!DNL ChatGPT Ads] campagne.
feature: Search Campaign Management
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
    internal-label: Search, Social, & Commerce
subfeature_v2:
  - id: f3d33161-c519-436e-bbbd-730ba428736b
    internal-label: Campaign management
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: 6aa2e40903fd8652c0ac744e3cd4f68c5e74fd48
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 0%
---
# [!DNL ChatGPT Ads] impostazioni campagna

*Gli annunci in [!DNL ChatGPT] sono una funzionalità pilota di[!DNL OpenAI]*

## Scheda [!UICONTROL Basic Settings]

*Solo nuove campagne*

**[!UICONTROL Network]:** La rete di annunci.

**[!UICONTROL Account]:** L&#39;account di rete dell&#39;annuncio.

**[!UICONTROL Campaign Type]:** Dove inserire gli annunci: l&#39;unica opzione è *[!UICONTROL Standard]* per visualizzare gli annunci in [!DNL ChatGPT].

## Scheda [!UICONTROL Campaign Details]

**[!UICONTROL Campaign Name]:** Nome di campagna univoco all&#39;interno dell&#39;account.

**[!UICONTROL Status]:** Lo stato di visualizzazione della campagna: *Attivo* o *In pausa*. Il valore predefinito per le nuove campagne pubblicitarie è *Attivo*.

**[!UICONTROL Objective]:** Obiettivo della campagna: *[!UICONTROL Reach]*, *[!UICONTROL Clicks]* o *[!UICONTROL Conversions]*. L&#39;obiettivo determina le [opzioni di offerta per gruppi di annunci](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings-chatgpt.md) disponibili: l&#39;offerta CPC di destinazione è supportata per i clic e l&#39;offerta CPA di destinazione è supportata per le conversioni. Le offerte CPC di Target e CPA di Target non sono disponibili per le campagne REACH.

**[!UICONTROL Billing event]:** (Nuove campagne con l&#39;obiettivo [!UICONTROL Conversions]) Se il costo è basato su clic o impression. Il valore predefinito è clic. L’obiettivo determina il tipo di ottimizzazione della campagna; l’evento di fatturazione determina la modalità di addebito. Non puoi modificare l&#39;evento di fatturazione dopo aver salvato la campagna.

**[!UICONTROL Location Targets]:** posizioni geografiche dell&#39;utente supportate da includere come destinazioni. Per impostazione predefinita, tutte le posizioni supportate sono impostate come destinazione. Puoi restringere le destinazioni in modo da includere (ma non escludere) gli utenti in qualsiasi combinazione di posizioni.

* Per eseguire il targeting di tutte le posizioni, non selezionare alcuna posizione.

* Per includere una posizione e le relative posizioni figlio, fate clic sul cerchio adiacente.

* Per espandere una posizione nei relativi sottocomponenti, ad esempio regioni, territori o città, fare clic sul nome della posizione.

* Per cercare una posizione, immetti o incolla almeno i primi tre caratteri della posizione nel campo di input.

**[!UICONTROL Budget Type]:** Tipo di budget campagna: *Budget giornaliero* o *Durata*. Non puoi modificare il tipo di budget dopo aver salvato la campagna.

**[!UICONTROL Budget]:** Il budget per il tipo di campagna specificato.

**[!UICONTROL Conversion events]:** (Facoltativo) Qualsiasi evento di conversione esistente configurato in [!DNL ChatGPT Ads] da associare alla campagna. **Nota:** i dati sulle prestazioni per le conversioni monitorate da [!DNL OpenAI] non sono disponibili in Search, Social e Commerce. Monitora le conversioni tracciate di [!DNL OpenAI] in [!DNL ChatGPT Ads Manager].

<!-- **[!UICONTROL Start Date]:** -->

{{$include /help/_includes/start-date.md}}

<!-- **[!UICONTROL End Date]:** -->

{{$include /help/_includes/end-date.md}}

>[!MORELIKETHIS]
>
>* [Gestisci campagne](/help/search-social-commerce/new-ui/manage/campaigns/campaign-manage.md)
