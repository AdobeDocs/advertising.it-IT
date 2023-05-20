---
title: Informazioni sugli obiettivi personalizzati
description: Scopri gli obiettivi personalizzati per definire gli eventi di successo in pacchetti ottimizzati per il CPA più basso o il ROAS più alto.
feature: DSP Optimization
exl-id: 806450b9-ce32-4f5c-a2ac-ba8e435ce36d
source-git-commit: 7f35b3f3b33ed320ac186d219cbd0f826666bb3b
workflow-type: tm+mt
source-wordcount: '267'
ht-degree: 0%

---

# Informazioni sugli obiettivi personalizzati

Gli obiettivi personalizzati definiscono gli eventi di successo necessari a un inserzionista per raggiungere i suoi obiettivi aziendali. Ogni pacchetto che utilizza gli obiettivi di ottimizzazione &quot;[!UICONTROL Highest ROAS - Custom Goal]&quot; o &quot;[!UICONTROL Lowest CPA - Custom Goal]&quot; deve includere un obiettivo personalizzato che contribuisca a raggiungere l’obiettivo di ottimizzazione generale. Puoi creare obiettivi personalizzati con *obiettivi* in [!DNL Advertising Search, Social, & Commerce].

![obiettivi personalizzati](/help/dsp/assets/objective-goals.png)

Ogni obiettivo personalizzato è costituito da una o più metriche, oppure *proprietà transazione* e le ponderazioni relative di tali proprietà di transazione. Le proprietà di transazione disponibili includono tutte le metriche tracciate utilizzando il pixel di conversione Adobe Advertising e tramite Adobe Analytics.

>[!NOTE]
>
>* [!DNL Analytics] Dimensioni e segmenti non sono disponibili, ad Adobe per l’ottimizzazione di Advertising.
>* Per utilizzare gli eventi di Analytics in DSP, collabora con il tuo account team di Adobi per configurare un’integrazione a livello di inserzionista.
>* [!DNL Analytics] gli eventi personalizzati seguono questa convenzione di denominazione: `custom_event_[*event #*]_[*Analytics report suite ID*]`. Esempio: `custom_event_16_examplersid`


Ad esempio, supponiamo che tre metriche (proprietà della transazione) siano rilevanti per un pacchetto specifico in una delle tue campagne: &quot;Download PDF&quot; con valore di 20 USD, &quot;Iscrizione e-mail&quot; con valore di 30 USD e &quot;Conferma ordine&quot; con valore di 40 USD. Se desideri assegnare un peso in base al valore monetario una tantum dell’azione del cliente, i pesi relativi delle proprietà saranno 1, 2 e 1,5.

Consulta la [best practice per la creazione di obiettivi personalizzati](custom-goal-best-practices.md) per suggerimenti su come configurare gli obiettivi personalizzati.

Una volta [creare un obiettivo personalizzato](custom-goal-create.md), è possibile [assegnarlo a un pacchetto](/help/dsp/campaign-management/packages/package-settings.md) per il reporting e l’ottimizzazione algoritmica tramite Adobe Sensei.

>[!MORELIKETHIS]
>
>* [Creare un obiettivo personalizzato](custom-goal-create.md)
>* [Best practice per la creazione di un obiettivo personalizzato](custom-goal-best-practices.md)
>* [Obiettivi di ottimizzazione e modalità di utilizzo](optimization-goals.md)
>* [Impostazioni pacchetto](/help/dsp/campaign-management/packages/package-settings.md)
> * [Come l’DSP ottimizza le campagne](optimization-how-dsp-optimizes-campaigns.md)

