---
title: Sintassi della logica dei segmenti di pubblico
description: Fai riferimento alla sintassi da utilizzare per definire la logica per i segmenti di pubblico.
feature: DSP Audiences
exl-id: fb73f35f-1f65-463b-b93c-90804a8d19a9
source-git-commit: 7e614ecb517515217d812926f61ca10437820efd
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 0%

---

# Sintassi della logica dei segmenti di pubblico

Quando crei tipi di pubblico riutilizzabili, puoi definire manualmente la logica dei segmenti utilizzando ID segmento alfanumerici (chiavi) e la sintassi seguente:

* () per indicare un gruppo
* `||` per [!DNL OR] <!-- || escaped with backticks so Jenkins doesn't think it's a Markdown table -->
* &amp;&amp; per [!DNL AND]
* ! per [!DNL NOT] (escludi)

>[!NOTE]
>
>* Tutti i gruppi di segmenti specificati sono inclusi a meno che non siano preceduti da ! (che li esclude).
>* È possibile [trovare l’ID segmento di un pubblico](reusable-audience-clipboard.md) da [!UICONTROL Audiences] > [!UICONTROL All audiences].


Ad esempio, la logica seguente:

```
(X5vUk1cNvZxvBJ3jMjTt) || (sfvXrmQkk77PL5OtHpLH) && !(SMWSjTZFiy9hR1bKm1vw || x08UReA0IcP9HAJdcGVe)
```

significa (in inglese)

```
[!DNL INCLUDE] Segment ID X5vUk1cNvZxvBJ3jMjTt [!DNL OR] INCLUDE Segment ID sfvXrmQkk77PL5OtHpLH [!DNL AND EXCLUDE] (Segment ID SMWSjTZFiy9hR1bKm1vw AND Segment ID x08UReA0IcP9HAJdcGVe)
```

>[!NOTE]
>
>Nelle impostazioni di posizionamento, puoi utilizzare i tipi di pubblico salvati come tipi di pubblico per eseguire il targeting in modo esplicito oppure come tipi di pubblico separati per escluderli dal targeting. Assicurati che la logica del segmento rifletta lo scopo per cui utilizzerai il pubblico.

>[!MORELIKETHIS]
>
>* [Copiare negli Appunti la chiave del segmento di un pubblico riutilizzabile](reusable-audience-clipboard.md)
>* [Informazioni su Gestione dell&#39;audience](audience-about.md)
>* [Creare un pubblico riutilizzabile](reusable-audience-create.md)
>* [Impostazioni pubblico](audience-settings.md)
>* [Provider di dati di terze parti disponibili](third-party-data-providers.md)

