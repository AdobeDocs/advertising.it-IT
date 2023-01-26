---
title: Sintassi per la logica del segmento di pubblico
description: Fai riferimento alla sintassi da utilizzare per definire la logica per i segmenti di pubblico.
feature: DSP Audiences
exl-id: 3a51b1b5-1eef-453b-9be5-0694e27491a8
source-git-commit: 1c13874967ec4ad264e5fa6a5e0dfeb6120f53cc
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 0%

---

# Sintassi per la logica del segmento di pubblico

Quando crei tipi di pubblico riutilizzabili, puoi definire manualmente la logica dei segmenti utilizzando gli ID (chiavi) dei segmenti alfanumerici e la seguente sintassi:

* () per indicare un gruppo
* `||` per [!DNL OR] <!-- || escaped with backticks so Jenkins doesn't think it's a Markdown table -->
* &amp; per [!DNL AND]
* ! per [!DNL NOT] (escludere)

>[!NOTE]
>
>* Sono inclusi tutti i gruppi di segmenti specificati a meno che non siano preceduti da ! (che li esclude).
>* È possibile [trova l’ID del segmento per un pubblico](reusable-audience-clipboard.md) da [!UICONTROL Audiences] > [!UICONTROL All audiences].


Ad esempio, la logica seguente:

```
(X5vUk1cNvZxvBJ3jMjTt) || (sfvXrmQkk77PL5OtHpLH) && !(SMWSjTZFiy9hR1bKm1vw || x08UReA0IcP9HAJdcGVe)
```

significa (in inglese semplice)

```
[!DNL INCLUDE] Segment ID X5vUk1cNvZxvBJ3jMjTt [!DNL OR] INCLUDE Segment ID sfvXrmQkk77PL5OtHpLH [!DNL AND EXCLUDE] (Segment ID SMWSjTZFiy9hR1bKm1vw AND Segment ID x08UReA0IcP9HAJdcGVe)
```

>[!NOTE]
>
>Nelle impostazioni di posizionamento, puoi utilizzare i tipi di pubblico salvati sia come pubblico per eseguire esplicitamente il targeting o come pubblico separato da escludere dal targeting. Assicurati che la logica dei segmenti rifletta lo scopo per cui utilizzerai il pubblico.

>[!MORELIKETHIS]
>
>* [Copia negli Appunti la chiave di segmento per un pubblico riutilizzabile](reusable-audience-clipboard.md)
>* [Informazioni sulla gestione dell&#39;audience](audience-about.md)
>* [Creare un pubblico riutilizzabile](reusable-audience-create.md)
>* [Impostazioni del pubblico](audience-settings.md)
>* [Fornitori di dati di terze parti disponibili](third-party-data-providers.md)

