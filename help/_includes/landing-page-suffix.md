---
source-git-commit: a1a8c1b563d419090ddbefacc55be869c1ee7bcf
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 0%

---
# Campo Suffisso pagina di destinazione nelle impostazioni dell’account GGL e MS, nelle impostazioni della campagna e in alcune impostazioni degli annunci

**[!UICONTROL Landing Page Suffix]:** ([!DNL Google Ads] e [!DNL Microsoft Advertising] account solo; facoltativo) Qualsiasi parametro da aggiungere alla fine degli URL finali per tenere traccia delle informazioni; include tutti i parametri che l&#39;azienda deve monitorare. Esempio: `param1=value1&param2=value2`

Gli account che utilizzano il tracciamento delle conversioni di Adobe Advertising devono includere nel suffisso l&#39;identificatore di clic (`gclid` per [!DNL Google Ads] o `msclkid` per [!DNL Microsoft Advertising]) della rete di annunci.

Gli account con un’integrazione Adobe Analytics devono utilizzare il parametro s_kwcid. Se l’account dispone di un’implementazione s_kwcid lato server, il parametro viene aggiunto automaticamente quando un utente fa clic su un annuncio; in caso contrario, è necessario aggiungerlo manualmente qui. Consulta i [formati suffisso richiesti per Google Ads](/help/search-social-commerce/tracking/formats-click-tracking-google.md) e [formati suffisso richiesti per Microsoft Advertising](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md).

**Note:**

* Questo campo non è aggiornato dall&#39;impostazione di tracciamento [!UICONTROL Auto Upload].

* I suffissi della pagina di destinazione ai livelli inferiori sovrascrivono il suffisso a livello di account. Per una manutenzione più semplice, utilizza solo il suffisso a livello di account, a meno che non sia necessario un tracciamento diverso per i singoli componenti dell’account. Per configurare un suffisso a livello di gruppo di annunci o inferiore, utilizza l’editor della rete di annunci.
