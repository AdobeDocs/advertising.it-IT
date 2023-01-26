---
title: Informazioni sugli obiettivi personalizzati
description: Scopri gli obiettivi personalizzati per definire i tuoi eventi di successo in pacchetti ottimizzati per il CPA più basso o il ROAS più alto.
feature: DSP Optimization
exl-id: 623cb1ef-85ab-4535-aa3a-8e6ec8ae15ee
source-git-commit: 1c13874967ec4ad264e5fa6a5e0dfeb6120f53cc
workflow-type: tm+mt
source-wordcount: '266'
ht-degree: 0%

---

# Informazioni sugli obiettivi personalizzati

Gli obiettivi personalizzati definiscono gli eventi di successo richiesti da un inserzionista per raggiungere i suoi obiettivi aziendali. Ogni pacchetto che utilizza gli obiettivi di ottimizzazione &quot;[!UICONTROL Highest ROAS - Custom Goal]&quot; o &quot;[!UICONTROL Lowest CPA - Custom Goal]&quot; deve includere un obiettivo personalizzato che contribuisca a raggiungere l&#39;obiettivo di ottimizzazione generale. Puoi creare obiettivi personalizzati come *obiettivi* in [!DNL Adobe Advertising Search].

![obiettivi personalizzati](/help/dsp/assets/objective-goals.png)

Ogni obiettivo personalizzato è costituito da una o più metriche, oppure *proprietà della transazione* e i pesi relativi di tali proprietà della transazione. Le proprietà di transazione disponibili includono tutte le metriche tracciate utilizzando il pixel di conversione di Adobe Advertising e tramite Adobe Analytics.

>[!NOTE]
>
>* [!DNL Analytics] dimensioni e segmenti non sono disponibili per Adobe l’ottimizzazione per la pubblicità.
>* Per utilizzare gli eventi di Analytics in DSP, utilizza le [!DNL Adobe] per configurare un’integrazione a livello di inserzionista.
>* [!DNL Analytics] gli eventi personalizzati seguono questa convenzione di denominazione: `custom_event_[*event #*]_[*Analytics report suite ID*]`. Esempio: `custom_event_16_examplersid`


Ad esempio, supponiamo che tre metriche (proprietà transazione) siano rilevanti per un pacchetto specifico in una delle campagne: &quot;PDF Download&quot; valutato a 20 USD, &quot;Email Registrup&quot; valutato a 30 USD e &quot;Order Confirmation&quot; valutato a 40 USD. Se si desidera dare peso in base al valore monetario una tantum dell&#39;azione del cliente, i pesi relativi delle proprietà saranno 1, 2 e 1,5.

Consulta la sezione [best practice per la creazione di obiettivi personalizzati](custom-goal-best-practices.md) per suggerimenti su come configurare gli obiettivi personalizzati.

Una volta [creare un obiettivo personalizzato](custom-goal-create.md), puoi [assegnarlo a un pacchetto](/help/dsp/campaign-management/packages/package-settings.md) per la generazione di rapporti e l’ottimizzazione algoritmica con Adobe Sensei.

>[!MORELIKETHIS]
>
>* [Creare un obiettivo personalizzato](custom-goal-create.md)
>* [Tecniche consigliate per la creazione di un obiettivo personalizzato](custom-goal-best-practices.md)
>* [Obiettivi di ottimizzazione e come utilizzarli](optimization-goals.md)
>* [Impostazioni pacchetto](/help/dsp/campaign-management/packages/package-settings.md)
> * [Ottimizzazione DSP campagne](optimization-how-dsp-optimizes-campaigns.md)

