---
title: Impostazioni gruppo di annunci [!DNL ChatGPT]
description: Fare riferimento alle impostazioni per [!DNL ChatGPT] gruppi di annunci.
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
source-git-commit: 52c1132246ea0cc48b6102e6d6f15be1ded32f09
workflow-type: tm+mt
source-wordcount: '480'
ht-degree: 0%
---
# Impostazioni gruppo di annunci [!DNL ChatGPT]

*Gli annunci in [!DNL ChatGPT] sono una funzionalità pilota di[!DNL OpenAI]*

## Scheda [!UICONTROL Basic Settings]

*Solo nuovi gruppi di annunci*

**[!UICONTROL Network]:** La rete di annunci.

**[!UICONTROL Account]:** L&#39;account di rete dell&#39;annuncio.

**[!UICONTROL Campaign]:** La campagna. Non puoi modificare la campagna dopo aver creato il gruppo di annunci.

## Scheda [!UICONTROL Ad Group Details]

**[!UICONTROL Ad Group name]:** Nome di un gruppo di annunci univoco all&#39;interno della campagna e che include almeno tre caratteri.

**[!UICONTROL Status]:** Lo stato di visualizzazione del gruppo di annunci: *[!UICONTROL Active]* o *[!UICONTROL Paused]*. Il valore predefinito per i nuovi gruppi di annunci è *[!UICONTROL Active]*.

**[!UICONTROL Bid strategy]:** (Campagne con obiettivo [!UICONTROL Clicks] o [!UICONTROL Conversions]) Come fare offerte per annunci nel gruppo di annunci:

* *[!UICONTROL Autobid]:* (impostazione predefinita per i nuovi gruppi di annunci) [!DNL OpenAI] regola automaticamente le offerte per ottenere il maggior numero di clic o conversioni, a seconda dell&#39;obiettivo della campagna, dal budget. Non hai inserito un importo di offerta. Questa opzione è disponibile sia per il budget giornaliero che per quello delle campagne a vita.

* *[!UICONTROL Target CPC]:* (campagne con obiettivo [!UICONTROL Clicks]) Offerte per un obiettivo di costo medio per clic. Immettere l&#39;obiettivo nel campo [!UICONTROL Target CPC].

* *[!UICONTROL Target CPA]:* (campagne con obiettivo [!UICONTROL Conversions]) Offerte per un obiettivo di costo medio per conversione. Immettere l&#39;obiettivo nel campo [!UICONTROL Target CPA].

* *[!UICONTROL Manual: Max bid]:* (solo gruppi di annunci di offerte manuali esistenti) mantiene l&#39;offerta massima esistente come importo di sola lettura. È possibile mantenere questa strategia o passare a [!UICONTROL Autobid] o alla strategia di destinazione per l&#39;obiettivo della campagna. Questa opzione non è disponibile per i nuovi gruppi di annunci o durante la modifica di gruppi di annunci che utilizzano già offerte con ID automatico o target.

I gruppi di annunci di offerta manuale esistenti non vengono modificati automaticamente in un’altra strategia. La modifica solo di un importo di destinazione o di un’impostazione non correlata non modifica una strategia di offerta di destinazione esistente.

**[!UICONTROL Target CPC]:** (gruppi di annunci con strategia di offerta [!UICONTROL Target CPC]; obbligatorio) Il costo medio per clic che si desidera ottenere, nella valuta dell&#39;account. Inserire un importo positivo. Si tratta di un obiettivo di costo medio, non di offerta massima.

**[!UICONTROL Target CPA]:** (gruppi di annunci con strategia di offerta [!UICONTROL Target CPA]; obbligatorio) Il costo medio per conversione che si desidera ottenere, nella valuta dell&#39;account. Inserire un importo positivo. Si tratta di un obiettivo di costo medio, non di offerta massima.

**[!UICONTROL Maximum CPC bid]:** (campagne con l&#39;obiettivo [!UICONTROL Clicks]; solo gruppi di annunci di offerta manualmente esistenti; sola lettura) L&#39;importo massimo esistente che pagherai per ogni clic.

**[!UICONTROL Conversion-optimized bid cap]:** (campagne con l&#39;obiettivo [!UICONTROL Conversions]; solo gruppi di annunci di offerta manualmente esistenti; sola lettura) L&#39;importo massimo esistente che si è disposti a offrire per una conversione. [!DNL OpenAI] utilizza il tasso di conversione previsto per convertire questo valore in un&#39;offerta d&#39;asta per impression.

**[!UICONTROL Maximum CPM bid]:** (Campagne con l&#39;obiettivo [!UICONTROL Reach]) L&#39;importo massimo che pagherai per mille impression, nella valuta dell&#39;account. Immetti un valore compreso tra 0.01-5000. Le campagne REACH non dispongono delle opzioni [!UICONTROL Bid strategy].

**[!UICONTROL Context hints (optional)]:** Descrizione delle conversazioni, degli argomenti o delle parole chiave per cui i prodotti o i servizi potrebbero essere rilevanti. Hint separati con virgole o interruzioni di riga. Gli hint possono essere utilizzati per guidare la corrispondenza, ma non sono regole di targeting per corrispondenza esatta. Consulta la [[!DNL ChatGPT Ads] guida su come scrivere suggerimenti di contesto efficaci](https://help.openai.com/en/articles/20001211-create-ad-groups-for-chatgpt#writing-effective-context-hints).

**[!UICONTROL Landing Page Suffix]:** (facoltativo) eventuali parametri da aggiungere alla fine degli URL della pagina di destinazione per tenere traccia delle informazioni. Esempio: `param1=value1&param2=value2`.

>[!MORELIKETHIS]
>
>* [Gestisci gruppi di annunci](ad-group-manage.md)
