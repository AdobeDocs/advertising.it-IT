---
source-git-commit: 05b9a55e19c9f76060eedb35c41cdd2e11753c24
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 0%

---
# Aggiungi il campo Parametri nelle impostazioni account e campagna

**[!UICONTROL Append Parameters]:** (facoltativo) eventuali parametri di tracciamento aggiuntivi da aggiungere agli URL di base.<!-- When account uses setting append_param_to_tt_fus, then we add append parameters to the tracking templates OR the landing page suffixes instead (not sure how we determine which) -->. I parametri di accodamento a livello di inserzionista sono inclusi per impostazione predefinita a livello di account e di campagna, ma è possibile ignorarli entrambi.

È possibile utilizzare qualsiasi stringa di testo statico, inclusi i parametri di tracciamento di terze parti o qualsiasi [parametro di tracciamento supportato](/help/search-social-commerce/tracking/click-tracking-urls-optional-parameters.md), che inserisca un valore di dati appropriato nell&#39;URL di base.

Separa più parametri con virgole o e commerciali (&amp;). Le parentesi quadre nidificate non sono supportate.

**Note:**

* Le modifiche ai parametri di aggiunta non sono controllate dall&#39;opzione [!UICONTROL Auto Upload]. Se modifichi i parametri di accodamento per gli URL di base esistenti, i nuovi URL non vengono generati automaticamente. Aggiungere i nuovi parametri scaricando un file di bulksheet per l&#39;account o la campagna, aggiornando i campi [!UICONTROL Base URL/Final URL] e quindi caricando e pubblicando il bulksheet.

* (Reti di annunci con tracciamento parallelo) Evita l’utilizzo di macro, che non vengono sostituite dai clic provenienti da origini che abilitano il tracciamento parallelo. Se l’inserzionista deve utilizzare delle macro, il Team dell’account Adobe deve collaborare con l’Assistenza clienti o con il team di implementazione per aggiungerle.

* (Per gli inserzionisti con un&#39;integrazione Adobe Advertising-Adobe Analytics) Per includere un parametro AMO ID per inviare dati di ricerca, social e Commerce a [!DNL Analytics], vedi [formati specifici per la rete di annunci](/help/integrations/analytics/ids.md#amo-id-formats). Non è necessario aggiungere manualmente il parametro per gli account [!DNL Google Ads] e [!DNL Microsoft Advertising] con un’implementazione AMO ID lato server.
