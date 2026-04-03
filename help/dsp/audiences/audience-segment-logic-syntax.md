---
title: Sintassi della logica dei segmenti di pubblico
description: Fai riferimento alla sintassi da utilizzare per definire la logica per i segmenti di pubblico.
feature: DSP Audiences
exl-id: fb73f35f-1f65-463b-b93c-90804a8d19a9
TQID: https://experienceleague.adobe.com/FPci9npdKrFxwge6tw41Fhx4XAC9VqYFc-RZhLhILLo
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2: id: fef5c122-6482-4d17-a8ce-4e70b906f1f4
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 141
ht-degree: 0%

---

# Sintassi della logica dei segmenti di pubblico

Quando crei tipi di pubblico riutilizzabili, puoi definire manualmente la logica dei segmenti utilizzando ID segmento alfanumerici (chiavi) e la sintassi seguente:

* () per indicare un gruppo
* `||` per [!DNL OR] <!-- || escaped with backticks so Jenkins doesn't think it's a Markdown table -->
* &amp;&amp; per [!DNL AND]
* ! per [!DNL NOT] (escludere)

>[!NOTE]
>
>* Tutti i gruppi di segmenti specificati sono inclusi a meno che non siano preceduti da ! (che li esclude).
>* Puoi [trovare l&#39;ID segmento per un pubblico](reusable-audience-clipboard.md) da [!UICONTROL Audiences] > [!UICONTROL All audiences].

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
>Nelle impostazioni di posizionamento, puoi utilizzare i tipi di pubblico salvati come tipi di pubblico per eseguire il targeting in modo esplicito oppure come tipi di pubblico separati per escluderli dal targeting. Assicurati che la logica del segmento rifletta lo scopo dell’utilizzo del pubblico.

>[!MORELIKETHIS]
>
>* [Copia negli Appunti la chiave del segmento per un pubblico riutilizzabile](reusable-audience-clipboard.md)
>* [Informazioni su Gestione dell&#39;audience](audience-about.md)
>* [Crea un pubblico riutilizzabile](reusable-audience-create.md)
>* [Impostazioni pubblico](audience-settings.md)
>* [Provider di dati di terze parti disponibili](third-party-data-providers.md)
