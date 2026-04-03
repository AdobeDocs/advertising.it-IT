---
title: Domande frequenti sulla gestione delle campagne
description: Ulteriori informazioni sulla gestione delle campagne, compreso il periodo di latenza per le modifiche e cosa accade quando si apportano modifiche al budget durante un volo.
feature: DSP Packages, DSP Placements
exl-id: 8a443543-ebb1-4273-a007-afef07d32d8c
TQID: https://experienceleague.adobe.com/PgO4aktP20KQzNe6SG6Vw7ahvYqHTSISQ10FCum-vQg
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2:
  - id: a4886037-b6d8-40e1-aeab-edeb7649d7d3
  - id: fddd8d8f-3ba1-4a22-b714-69d0e4655be8
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 405
ht-degree: 0%

---

# Domande frequenti sulla gestione delle campagne

<!-- Most of this information should be moved into the relevant topics (especially editing topics). -->

## Latenza delle modifiche alle impostazioni

* Quando modificate un posizionamento o un&#39;impostazione di pacchetto, quando ha effetto la modifica?

  Le modifiche alle impostazioni in genere hanno effetto immediato, ma possono richiedere fino a 12 ore.

  Se si tratta dell’ultimo giorno di consegna, apporta le modifiche all’inizio della giornata in modo che DSP abbia tutto il tempo di ricalibrare il pacchetto in base alle modifiche. Ad esempio, se si passa da una velocità pari a quella della consegna anticipata, DSP deve rivalutare la modalità di distribuzione della spesa per la parte restante del volo. Non fare questo tipo di cambiamento se ti resta solo un&#39;ora per la consegna nell&#39;ultimo giorno del volo.

## Aggiornamenti budget a metà volo

* Quando si apporta una modifica a un posizionamento, quanto tempo ci vuole DSP per riallocare il budget del pacchetto?

  L’allocazione del budget si basa sulle prestazioni del posizionamento, valutate in base a una media di 14 giorni. Le modifiche apportate a un posizionamento determinano modifiche all&#39;allocazione del budget solo quando causano modifiche nelle prestazioni durante la media di 14 giorni.

  Quando si verificano modifiche delle prestazioni, DSP ridistribuisce il budget del pacchetto tra i posizionamenti di conseguenza durante il successivo ciclo di ottimizzazione del budget, che si verifica circa a mezzanotte (00:00) nel fuso orario della campagna.

* Come viene riallocato il budget quando un posizionamento viene rimosso da un pacchetto e aggiunto a un altro pacchetto?

  L’intera cronologia di spesa di un posizionamento viene associata al posizionamento e si sposta con esso da un pacchetto all’altro.

  Quando si rimuove un posizionamento da un pacchetto, il pacchetto non ha più alcuna cronologia della spesa del posizionamento. Il budget del pacchetto diventa (budget pacchetto - budget posizionamento rimosso) / intervallo di tempo rimanente in volo. Il budget del pacchetto viene quindi allocato ai posizionamenti rimanenti nel pacchetto.

  Allo stesso modo, se aggiungi lo stesso posizionamento a un pacchetto diverso, DSP considera la cronologia di spesa del posizionamento quando alloca il budget per tutti i posizionamenti nel nuovo pacchetto.

* Come cambia la velocità del pacchetto nell’ultimo giorno di un volo?

  Nell&#39;ultimo giorno di un volo, il giorno viene ridotto da 24 a 23 ore in modo da non superare il budget previsto per il pacchetto. Inoltre, la strategia di riempimento della velocità del pacchetto cambia automaticamente in &quot;[!UICONTROL Frontload]&quot;, anche se è impostata su &quot;[!UICONTROL even]&quot;. Ciò significa che il 65% del budget giornaliero deve essere consegnato entro le ore 11:0&rbrace; EST.:30

>[!MORELIKETHIS]
>
>* [Impostazioni pacchetto](/help/dsp/campaign-management/packages/package-settings.md)
>* [Impostazioni posizionamento](/help/dsp/campaign-management/placements/placement-settings.md)
>* [Best practice per la configurazione delle campagne sulle prestazioni](/help/dsp/optimization/campaign-best-practices-performance.md)
