---
title: Tecniche consigliate per la creazione di un obiettivo personalizzato
description: Scopri le best practice per la creazione di obiettivi personalizzati per definire gli eventi di successo.
feature: DSP Optimization, DSP Best Practices
exl-id: 54b16325-4b72-48a3-a2e0-4e342229211c
source-git-commit: 1c13874967ec4ad264e5fa6a5e0dfeb6120f53cc
workflow-type: tm+mt
source-wordcount: '573'
ht-degree: 0%

---

# Tecniche consigliate per la creazione di un obiettivo personalizzato

## Obiettivi personalizzati con una singola proprietà

Gli esempi seguenti mostrano come configurare obiettivi per una singola proprietà (metrica).

### Esempio per una campagna con &quot;[!UICONTROL Highest ROAS - Custom Goal]&quot; Obiettivo di ottimizzazione

Se l&#39;obiettivo della campagna è il fatturato ([!UICONTROL Highest ROAS - Custom Goal]), quindi l&#39;obiettivo personalizzato (obiettivo) includerà il[!UICONTROL Revenue]&quot; proprietà con un peso di uno (1).

![esempio di obiettivo personalizzato ROAS con una singola proprietà](/help/dsp/assets/custom-goal-roas.png)

>[!NOTE]
>
> A [!UICONTROL Property Weight] di uno equivale a un valore per ogni $ 1 dei ricavi tracciati.
>
> Ad esempio, una conversione da $ 250 con un peso di $ 250 viene indicata come $ 250. Se alla metrica di conversione viene assegnato un peso di 0,5, la conversione da $ 250 viene indicata come $ 125 nella pubblicità di Adobe ($250 Conversione * 0,5 [!UICONTROL Property Weight] = $ 125).

### Esempio per una campagna con &quot;[!UICONTROL Lowest CPA - Custom Goal]&quot; Obiettivo di ottimizzazione

Se l&#39;obiettivo della campagna è il costo minimo per acquisizione (CPA) e richiede un solo evento di successo, includerai quella metrica (nell&#39;esempio seguente, &quot;Invio applicazione&quot;). La migliore pratica è quella di impostare il peso come uno (1).

![esempio di obiettivo personalizzato CPA con una singola proprietà](/help/dsp/assets/custom-goal-roas.png)

>[!NOTE]
>
> A [!UICONTROL Property Weight] di uno equivale a un valore di uno per ogni conversione tracciata.
>
> Ad esempio, se si tiene traccia di 10 conversioni di invio dell’applicazione, vengono segnalate 10 conversioni di invio dell’applicazione.  Se alla metrica di conversione viene assegnato un peso di 0,5, le 10 conversioni sono riportate come cinque (5) in Adobe Advertising (10 Conversioni * 0,5 [!UICONTROL Property Weight] = 5).

## Obiettivi personalizzati con più proprietà

Esistono due scenari in cui si utilizzerebbero più proprietà in un obiettivo personalizzato:

* L&#39;obiettivo della campagna dispone di più eventi di successo. Ad esempio, forse stai pubblicizzando più di un’azione in loco e sono tutti attribuiti all’obiettivo del tuo CPA. L’obiettivo di esempio seguente include tre proprietà separate (Download di PDF, Contatti e Iscrizione e-mail), ciascuna con un peso di un (1), che indica al [!DNL Adobe Sensei] algoritmo che ciascuna delle proprietà ha uguale importanza. Se si includono proprietà con costi o importanza variabili, è possibile regolare di conseguenza i rispettivi pesi relativi.

   ![esempio di obiettivo personalizzato con più proprietà](/help/dsp/assets/custom-goal-multiple-properties.png)

* La singola proprietà nell’obiettivo personalizzato non raggiunge il minimo di 10 conversioni al giorno necessarie per le prestazioni ottimizzate. Questo può verificarsi a causa della spesa minima giornaliera del pacchetto o un numero limitato di conversioni naturali. L’aggiunta di proprietà di supporto aggiuntive all’obiettivo personalizzato può aiutarti a raggiungere la soglia di 10 conversioni al giorno. Dieci eventi di supporto possono aiutare un pacchetto a raggiungere la soglia di 10/giorno, anche quando ciascuno dei loro pesi è inferiore a uno (1). Ma potrebbe non essere necessario aggiungere così tanti eventi.

   Quando aggiungi le proprietà di supporto a un obiettivo personalizzato, ponderale in base alla loro importanza relativa all’evento di successo principale e tieni presente la quantità di punti dati. Questo consente all’algoritmo di Adobe Sensei di bilanciare più proprietà e di ottimizzarle in base all’obiettivo.

   L&#39;obiettivo di esempio seguente include tre proprietà, ciascuna con un peso diverso: Invio applicazione = 1, Avvio applicazione = 0.1 e Pagina di destinazione inserzionista = 0.01. Ciò significa che ogni conversione Invia applicazione ha lo stesso valore per la tua azienda in media di 10 conversioni Inizio applicazione e 100 conversioni Pagina di destinazione inserzionista.

   ![esempio di obiettivo personalizzato con più proprietà](/help/dsp/assets/custom-goal-multiple-properties2.png)

   Se, invece, ponderate le visite a pagina di destinazione in modo uguale a Invio di applicazioni, la quantità naturalmente più elevata di visite a pagina di destinazione potrebbe superare l’obiettivo e distorcere le visite alla pagina di destinazione.<!--reword-->

>[!MORELIKETHIS]
>
>* [Informazioni sugli obiettivi personalizzati](custom-goal-about.md)
>* [Creare un obiettivo personalizzato](custom-goal-create.md)
>* [Obiettivi di ottimizzazione e come utilizzarli](optimization-goals.md)
>* [Impostazioni pacchetto](/help/dsp/campaign-management/packages/package-settings.md)
> * [Ottimizzazione DSP campagne](optimization-how-dsp-optimizes-campaigns.md)

