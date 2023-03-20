---
title: Domande frequenti su Campaign Management
description: Ulteriori informazioni sulla gestione delle campagne, compreso il periodo di latenza per le modifiche e ciò che accade quando apporti modifiche al budget durante un volo.
feature: DSP Packages, DSP Placements
exl-id: 8a443543-ebb1-4273-a007-afef07d32d8c
source-git-commit: 2fb3f227d74d8c8893a3cb042ea91121a0fae7c0
workflow-type: tm+mt
source-wordcount: '401'
ht-degree: 0%

---

# Domande frequenti su Campaign Management

<!-- Most of this information should be moved into the relevant topics (especially editing topics). -->

## Latenza delle modifiche dell&#39;impostazione

* Quando modifichi un posizionamento o un’impostazione di pacchetto, quando la modifica avrà effetto?

   Le modifiche alle impostazioni di solito hanno effetto immediato ma possono richiedere fino a 12 ore.

   Se si tratta del giorno finale di consegna, apporta modifiche all’inizio della giornata in modo che DSP tempo sufficiente per ricalibrare il pacchetto in base alle modifiche apportate. Ad esempio, se si passa dalla velocità pari alla velocità di consegna anticipata, DSP necessario rivedere come distribuirà la spesa per tutto il resto del volo. Non fare quel tipo di cambiamento se ti rimane solo un&#39;ora per consegnarlo l&#39;ultimo giorno del volo.

## Aggiornamenti budget Mid-Flight

* Quando apporti una modifica a un posizionamento, quanto tempo DSP per riallocare il budget del pacchetto?

   L&#39;allocazione del budget si basa sulle prestazioni di posizionamento, che vengono valutate utilizzando una media di 14 giorni. Le modifiche apportate a un posizionamento determinano modifiche all&#39;allocazione di budget solo quando causano cambiamenti nelle prestazioni durante la media di 14 giorni.

   Quando si verificano modifiche alle prestazioni, DSP ridistribuisce il budget del pacchetto tra i posizionamenti di conseguenza durante il successivo ciclo di ottimizzazione del budget, che si verifica a circa mezzanotte (00:00) nel fuso orario della campagna.

* Come viene riallocato il budget quando un posizionamento viene rimosso da un pacchetto e aggiunto a un altro pacchetto?

   L’intera cronologia di spesa di un posizionamento viene associata al posizionamento e si sposta con esso da pacchetto a pacchetto.

   Quando rimuovi un posizionamento da un pacchetto, il pacchetto non ha più alcuna cronologia della spesa del posizionamento. Il budget del pacchetto diventerà (budget pacchetto - budget di posizionamento rimosso) / intervallo di tempo rimanente in volo. Il budget del pacchetto viene quindi assegnato ai posizionamenti rimanenti nel pacchetto.

   Allo stesso modo, se aggiungi lo stesso posizionamento a un pacchetto diverso, DSP considera la cronologia di spesa del posizionamento quando alloca il budget per tutti i posizionamenti nel nuovo pacchetto.

* Come cambia il ritmo del pacchetto nell&#39;ultimo giorno di un volo?

   L&#39;ultimo giorno del volo viene ridotto da 24 ore a 23 ore in modo che il budget del pacchetto non venga superato. Inoltre, la strategia di riempimento del pacchetto cambia automaticamente in &quot;[!UICONTROL Frontload],&quot; anche se è impostato su &quot;[!UICONTROL even].&quot; Ciò significa che il 65% del budget giornaliero dovrebbe essere consegnato entro le ore 11:30 EST.

>[!MORELIKETHIS]
>
>* [Impostazioni pacchetto](/help/dsp/campaign-management/packages/package-settings.md)
>* [Impostazioni di posizionamento](/help/dsp/campaign-management/placements/placement-settings.md)
>* [Tecniche consigliate per l’impostazione di campagne sulle prestazioni](/help/dsp/optimization/campaign-best-practices-performance.md)

