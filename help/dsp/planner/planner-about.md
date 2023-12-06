---
title: Informazioni sullo strumento DSP Planner
description: Scopri lo strumento di pianificazione per prevedere la portata unica dei posizionamenti di TV connesse (CTV) in base al budget e ai criteri di targeting specificati.
feature: DSP Planner
source-git-commit: 9799ff5464d48e6258026ec997c5d5091576b9c6
workflow-type: tm+mt
source-wordcount: '546'
ht-degree: 0%

---


# Informazioni sullo strumento DSP Planner

<!-- rename all titles/descriptions from "CTV reach planner" to "campaign reach planner" -->

*Funzione beta*

Lo strumento di pianificazione consente di prevedere la portata unica a livello domestico dei posizionamenti di televisori connessi (CTV) in base al budget e ai criteri di targeting specificati prima di iniziare a spendere in magazzino. Dopo aver valutato più piani REACH, puoi implementare il piano che si allinea al meglio ai risultati desiderati nei tuoi pacchetti e posizionamenti.

Lo strumento di pianificazione utilizza i dati storici di offerta, impression e portata degli ultimi 90 giorni per stimare la portata univoca, il CPM medio, la frequenza media e le impression per una configurazione di piano.

## Previsione planner

Ogni previsione è costituita da una curva di previsione budget portata che mostra la quantità di portata raggiungibile con le impostazioni del piano. Sposta il cursore sulla visualizzazione per visualizzare opportunità di portata incrementali con budget più elevati.

![Previsione planner](/help/dsp/assets/planner-forecast.png "Previsione planner")

L&#39;output previsionale include anche [!UICONTROL Inventory Breakdown] sezione che mostra in che modo i diversi editori contribuiscono a raggiungere una portata univoca, offrendo preziose opportunità di discovery.

>[!NOTE]
>
>* Il [!UICONTROL Inventory Breakdown] mostra i dati solo per private e [!UICONTROL On Demand] inventario.
>* La portata univoca stimata mostrata per due editori può sovrapporsi.

## Vista planner

In [!UICONTROL Planner] In, puoi visualizzare i piani CTV reach esistenti e crearne di nuovi.

È inoltre possibile modificare, duplicare, esportare, archiviare o rigenerare la previsione per qualsiasi piano.

## Domande frequenti

+++Quali tipi di inventario sono supportati dallo strumento di pianificazione?

Lo strumento di pianificazione supporta tutti i tipi di inventario, inclusi quelli programmatici garantiti (PG), quelli del mercato privato (PMP), [!UICONTROL On Demand], e pubblico. Per generare previsioni accurate, includi accordi con almeno 50.000 impression negli ultimi sette giorni.

+++

+++Perché sto vedendo&quot;[!UICONTROL Unable to generate forecast]?&quot;

Uno dei motivi più comuni di questo errore è un budget insufficiente o un&#39;offerta massima. Per ottenere risultati ottimali, utilizza un budget minimo di 5000 USD. Se il [!UICONTROL Connected TV] tipo di supporto selezionato, inserisci un&#39;offerta massima di almeno 10 USD.

Inoltre, assicurati che gli editori o le offerte inclusi siano attivi e abbiano un’attività di impression recente.

+++

+++Ho creato un posizionamento basato sulle previsioni, ma non ha raggiunto la quantità di portata univoca indicata dalle previsioni di portata. Perché?

La previsione REACH è solo una stima, e i risultati effettivi dovrebbero variare a causa di molteplici fattori che cambiano frequentemente, come la stagionalità, la competitività delle offerte e l&#39;offerta e la domanda. Non è previsto che sia completamente accurato, ma è più utile per ottenere informazioni direzionali sulle strategie delle campagne che possono potenzialmente determinare i migliori risultati.

+++

+++Il planner può generare risultati di previsione diversi con le stesse impostazioni di input?

Il planner genera previsioni basate sui dati osservati più di recente, pertanto l’output previsto potrebbe variare in momenti diversi anche se le impostazioni del piano rimangono le stesse. Si consiglia di generare più previsioni per lo stesso piano ed esportare i risultati per ciascuno di essi.

+++

+++Posso salvare l&#39;output di previsione del planner?

Sì, è possibile esportare una previsione in una [!DNL Microsoft® Excel] foglio di calcolo facendo clic **[!UICONTROL ...]** > **[!UICONTROL Export]** in alto a destra. Il foglio di calcolo acquisisce le informazioni visualizzate nella curva del budget REACH utilizzando due colonne di dati: [!UICONTROL Budget] e [!UICONTROL Reach].

>[!MORELIKETHIS]
>
>* [Informazioni sullo strumento DSP Planner](planner-about.md)
>* [Creazione di un piano di copertura TV collegata](planner-create.md)
>* [Duplicare un piano di portata TV collegato](planner-duplicate.md)
>* [Modifica di un piano di copertura TV collegato](planner-edit.md)
>* [Esportazione di un piano di copertura TV collegato](planner-export.md)
>* [Rigenerare la previsione per un piano di copertura TV collegato](planner-forecast.md)
>* [Archiviare un piano di portata TV collegato](planner-archive.md)
>* [Impostazioni per i piani di copertura TV collegati](planner-settings.md)
