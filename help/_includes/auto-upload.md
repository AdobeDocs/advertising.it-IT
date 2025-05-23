---
source-git-commit: bef353542ee73d32b8ac53e6abd3265528be154f
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 0%

---
# Campo Caricamento automatico nelle impostazioni account e campagna

**[!UICONTROL Auto Upload]:** (solo per le campagne sincronizzate con [!UICONTROL EF Redirect]) carica automaticamente quanto segue nella rete di annunci alla successiva sincronizzazione di Search, Social e Commerce: (a) parametri di tracciamento di Search, Social e Commerce per i modelli di tracciamento e gli stessi parametri aggiunti agli URL finali oppure (b) nuovi URL di destinazione incorporati con il codice di tracciamento di Search, Social e Commerce. Per gli inserzionisti con un&#39;integrazione [Adobe Advertising-Adobe Analytics](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html?lang=it) e una configurazione AMO ID (s_kwcid) lato server, il caricamento include anche [parametri AMO ID](/help/integrations/analytics/ids.md#amo-id) per gli account [!DNL Google Ads] e [!DNL Microsoft Advertising]. L&#39;impostazione predefinita a livello di account viene ereditata dalle impostazioni di tracciamento dell&#39;inserzionista. Puoi sovrascrivere l’impostazione a livello di account a livello di campagna.

**Nota:** gli URL di tracciamento vengono aggiornati ogni giorno solo per le entità non sincronizzate, ovvero nuove entità aggiunte ed entità esistenti le cui proprietà sono state modificate. Pertanto, se modifichi questa impostazione da disabilitato a abilitato per un inserzionista/account/campagna esistente, gli URL di tracciamento non vengono aggiornati per le entità esistenti già sincronizzate. Per aggiungere il tracciamento agli URL delle entità sincronizzate esistenti, contatta il team dell’account Adobe e richiedi un processo di sincronizzazione manuale una tantum. Il processo di caricamento automatico gestirà le modifiche future.
