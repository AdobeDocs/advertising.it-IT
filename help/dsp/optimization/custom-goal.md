---
title: Best practice per gli obiettivi personalizzati
description: Scopri le best practice per la definizione di obiettivi personalizzati per pacchetti ottimizzati per il CPA più basso o il ROAS più alto.
feature: DSP Optimization
exl-id: e40b82bc-2558-4e78-b269-9b9a3f0f5219
TQID: https://experienceleague.adobe.com/xSM4vyVErtNbVqF3eMDeHpgEWaMK6hBwQpvijHEs0dc
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2:
  - id: af280ddc-b4d0-4416-86be-8f3ea3c6ebe7
  - id: fddd8d8f-3ba1-4a22-b714-69d0e4655be8
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: e2746d58fa512f032a1e4ff851d23876cd63fc93
workflow-type: tm+mt
source-wordcount: 700
ht-degree: 0%

---

# Best practice per gli obiettivi personalizzati

Gli obiettivi personalizzati definiscono gli eventi di successo necessari a un inserzionista per raggiungere i suoi obiettivi aziendali. Ogni pacchetto che utilizza l&#39;obiettivo di ottimizzazione &quot;[!UICONTROL Highest Return on Ad Spend (ROAS)"] o &quot;[!UICONTROL Lowest Cost per Acquisition (CPA)]&quot; deve includere un obiettivo personalizzato per consentire il raggiungimento dell&#39;obiettivo di ottimizzazione complessivo. Puoi creare obiettivi personalizzati come *[obiettivi personalizzati](/help/dsp/admin/custom-objectives-manage.md)*.

<!--
 update image or omit it

![custom goals](/help/dsp/assets/objective-goals.png)
 -->

Ogni obiettivo personalizzato (obiettivo) è costituito da una o più metriche di conversione da tracciare e ottimizzare, con i relativi pesi di tali metriche. È possibile [assegnare un obiettivo personalizzato a un pacchetto](/help/dsp/campaign-management/packages/package-settings.md) per il reporting e l&#39;ottimizzazione algoritmica utilizzando [!DNL Adobe AI].

Per creare e gestire obiettivi personalizzati, vedere &quot;[Gestione obiettivi personalizzati](/help/dsp/admin/custom-objectives-manage.md).&quot;

## Obiettivi personalizzati con una singola metrica

Gli esempi seguenti mostrano come configurare obiettivi per il targeting di una singola metrica di conversione.

### Esempio per una campagna con l&#39;obiettivo di ottimizzazione &quot;[!UICONTROL Highest Return on Ad Spend (ROAS)]&quot;

Se l&#39;obiettivo della campagna è il ricavo ([!UICONTROL Highest Return on Ad Spend (ROAS)]) e il ricavo da tutti i tipi di dispositivi è altrettanto importante, includere la metrica &quot;[!UICONTROL Revenue]&quot; con un peso di uno (1). Selezionare il tipo di metrica *[!UICONTROL Goal]*.

<!--
 update image or delete 

![example of a ROAS custom goal with a single conversion metric](/help/dsp/assets/custom-goal-roas.png)

-->

>[!NOTE]
>
> Un peso di uno (1) equivale a un valore di uno (1) per ogni $ 1 di ricavo tracciato per gli annunci display su qualsiasi dispositivo. Ad esempio, una conversione da 250 $ con un peso di uno (1) viene segnalata come 250 $ per le conversioni. Se alla metrica di conversione viene assegnato un peso di 0,5, la conversione di 250 dollari viene segnalata come 125 dollari in Adobe Advertising (conversione di 250 dollari * 0,5 [!UICONTROL weight] = 125 dollari).

### Esempio per una campagna con l&#39;obiettivo di ottimizzazione &quot;[!UICONTROL Lowest Cost per Acquisition (CPA)]&quot;

Se l&#39;obiettivo della campagna è il costo più basso per acquisizione (CPA) e richiede un solo evento di successo (ad esempio &quot;Invio applicazione&quot;), includi quella metrica e specifica il tipo di metrica *[!UICONTROL Goal]*. La best practice prevede di impostare il peso come uno (1).

<!--
 update image or delete 

![example of a CPA custom goal with a single conversion metric](/help/dsp/assets/custom-goal-roas.png)

-->

>[!NOTE]
>
> Un peso di uno (1) equivale a un valore di uno (1) per ogni conversione tracciata per gli annunci display su qualsiasi dispositivo. Ad esempio, se vengono tracciate 10 conversioni di invio di applicazioni, vengono segnalate 10 conversioni di invio di applicazioni. Tuttavia, se alla metrica di conversione viene assegnato un peso di 0,5, le 10 conversioni vengono riportate come cinque (5) in Adobe Advertising (10 conversioni * 0,5 [!UICONTROL weight] = 5).

## Obiettivi personalizzati con più metriche

Esistono due scenari in cui puoi utilizzare più metriche in un obiettivo personalizzato:

* L’obiettivo della campagna prevede più eventi di successo. Ad esempio, puoi promuovere più di un’azione nel sito (Download da PDF, Contattaci e Iscrizione e-mail) e tutte le azioni contribuiscono al tuo obiettivo CPA. Se l&#39;obiettivo include le tre metriche separate, ciascuna con il peso di una (1), l&#39;algoritmo basato su [!DNL Adobe AI] tratta ciascuna delle metriche e dei tipi di dispositivi utente con la stessa importanza. Se le diverse metriche hanno costi o importanza diversi, regola di conseguenza i loro pesi relativi.

<!--
 update image or delete it and adjust the wording above

   ![example of a custom goal with multiple metrics](/help/dsp/assets/custom-goal-multiple-properties.png)

-->

* La singola metrica di conversione nell’obiettivo personalizzato non raggiunge il minimo di 10 conversioni al giorno necessarie per prestazioni ottimizzate. Un numero inferiore di conversioni può verificarsi a causa di una spesa minima giornaliera per i pacchetti o di un numero limitato di conversioni naturali. L’aggiunta di metriche di supporto aggiuntive all’obiettivo personalizzato può aiutarti a raggiungere la soglia di 10 conversioni al giorno. Dieci eventi di supporto possono aiutare un pacchetto a raggiungere la soglia di 10/die, anche quando ciascuno dei loro pesi è inferiore a uno (1). Ma potresti non aver bisogno di aggiungere tanti eventi.

  Quando aggiungi metriche di supporto a un obiettivo personalizzato, ponderale in base alla loro importanza relativa per l’evento di successo principale e tieni presente la quantità di punti dati. Questo consente all&#39;algoritmo basato su [!DNL Adobe AI] di bilanciare più metriche e ottimizzarle in base all&#39;obiettivo.

  L’obiettivo dell’esempio seguente include tre metriche, ciascuna con un peso diverso: Invio applicazione = 1, Inizio applicazione = 0.1 e Pagina di destinazione inserzionista = 0.01. Ciò significa che ogni conversione Invio applicazione ha lo stesso valore per la tua azienda come media di 10 conversioni di Avvio applicazione e 100 conversioni di Pagina di destinazione inserzionista.

<!--
 update image or delete it and adjust the wording above

   ![example of a custom goal with multiple metrics](/help/dsp/assets/custom-goal-multiple-properties2.png)

-->

Se, invece, hai ponderato le visite della pagina di destinazione allo stesso modo degli invii di applicazioni, allora la quantità naturalmente più elevata di visite della pagina di destinazione potrebbe sopraffare l’obiettivo e distorcere l’ottimizzazione verso le visite della pagina di destinazione.

>[!MORELIKETHIS]
>
>* [Gestisci obiettivi personalizzati](/help/dsp/admin/custom-objectives-manage.md)
>* [Obiettivi di ottimizzazione e modalità di utilizzo](optimization-goals.md)
>* [Impostazioni pacchetto](/help/dsp/campaign-management/packages/package-settings.md)
>* [Come DSP ottimizza le campagne](optimization-how-dsp-optimizes-campaigns.md)
