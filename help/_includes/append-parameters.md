---
source-git-commit: 05b9a55e19c9f76060eedb35c41cdd2e11753c24
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 0%

---
# Aggiungi il campo Parametri nelle impostazioni account e campagna

**[!UICONTROL Append Parameters]:** (Facoltativo) Eventuali parametri di tracciamento aggiuntivi da aggiungere agli URL di base.<!-- When account uses setting append_param_to_tt_fus, then we add append parameters to the tracking templates OR the landing page suffixes instead (not sure how we determine which) -->. I parametri di accodamento a livello di inserzionista sono inclusi per impostazione predefinita a livello di account e di campagna, ma è possibile ignorarli entrambi.

Puoi utilizzare qualsiasi stringa di testo statica, inclusi i parametri di tracciamento di terze parti, o qualsiasi [parametri di tracciamento supportati](/help/search-social-commerce/tracking/click-tracking-urls-optional-parameters.md), che inseriscono un valore di dati appropriato nell&#39;URL di base.

Separa più parametri con virgole o e commerciali (&amp;). Le parentesi quadre nidificate non sono supportate.

**Note:**

* Le modifiche ai parametri di accodamento non sono controllate da [!UICONTROL Auto Upload] opzione. Se modifichi i parametri di accodamento per gli URL di base esistenti, i nuovi URL non vengono generati automaticamente. Aggiungi i nuovi parametri scaricando un file di bulksheet per l’account o la campagna, aggiornando il [!UICONTROL Base URL/Final URL] e quindi caricare e registrare il bulksheet.

* (Reti di annunci con tracciamento parallelo) Evita l’utilizzo di macro, che non vengono sostituite dai clic provenienti da origini che abilitano il tracciamento parallelo. Se l’inserzionista deve utilizzare delle macro, il Team dell’account Adobe deve collaborare con l’Assistenza clienti o con il team di implementazione per aggiungerle.

* (Per gli inserzionisti con un’integrazione Adobi Advertising-Adobe Analytics) Per includere un parametro AMO ID per inviare dati di ricerca, social e commerce a [!DNL Analytics], vedere [formati specifici della rete di annunci](/help/integrations/analytics/ids.md#amo-id-formats). Non è necessario aggiungere manualmente il parametro per [!DNL Google Ads] e [!DNL Microsoft Advertising] account con implementazione AMO ID lato server.
