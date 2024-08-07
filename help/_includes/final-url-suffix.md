---
source-git-commit: 6e5d79eb9c04a12813c42e33a2228c69f2adbaae
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 0%

---
# Definizione finale suffisso URL

<!-- Used in many places; in inventory feed templates, it's actually called "Campaign Final URL Suffix," but leaving this generic anyway since it's a paragraph-level include file -->

**[!UICONTROL Final URL Suffix]:** ([!DNL Google Ads] e [!DNL Microsoft Advertising] account solo; facoltativo) Qualsiasi parametro da aggiungere alla fine degli URL finali per tenere traccia delle informazioni; include tutti i parametri che l&#39;azienda deve monitorare. Esempio:`param1=value1&param2=value2`

Negli account che utilizzano il tracciamento delle conversioni di Adobe Advertising, il suffisso deve includere l&#39;identificatore di clic della rete di annunci (`msclkid` per [!DNL Microsoft Advertising]; `gclid` per [!DNL Google Ads]).

Gli account con integrazione Adobe Analytics devono utilizzare il parametro [AMO ID](/help/integrations/analytics/ids.md). Se l’account dispone di un’implementazione AMO ID lato server, il parametro viene aggiunto automaticamente quando un utente fa clic su un annuncio; in caso contrario, devi aggiungerlo manualmente qui. Vedere i [formati di suffisso richiesti per [!DNL Google Ads]](/help/search-social-commerce/tracking/formats-click-tracking-google.md) e [formati di suffisso richiesti per [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md).

>[!NOTE]
>
>* Questo campo non è aggiornato dall&#39;impostazione di tracciamento [!UICONTROL Auto Upload].
>* I suffissi URL finali ai livelli inferiori sovrascrivono il suffisso a livello di account. Per una manutenzione più semplice, utilizza solo il suffisso a livello di account, a meno che non sia necessario un tracciamento diverso per i singoli componenti dell’account. Per configurare un suffisso a livello di gruppo di annunci o inferiore, utilizza l’editor della rete di annunci.
