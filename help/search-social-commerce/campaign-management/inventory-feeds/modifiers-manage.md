---
title: Gestione modificatori
description: Scopri come configurare e gestire i modificatori per i modelli di annunci per i feed di dati di inventario.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '375'
ht-degree: 0%

---

# Gestione dei modificatori

*[!DNL Google Ads], [!DNL Microsoft® Advertising], [!DNL Yahoo! Japan Ads] (solo azioni di eliminazione), e [!DNL Yandex] solo account*

I modificatori sono aggettivi o avverbi che possono essere aggiunti o rimossi da una frase senza modificare la struttura di base della frase. Puoi creare gruppi di modificatori da utilizzare come variabili in vari campi di dati nei modelli di dati dei feed. Includendo modificatori nei campi della struttura dell’account (campagna e gruppo di annunci), nelle parole chiave, negli URL di base e negli annunci, puoi creare un valore per ogni valore di modificatore associato. Ad esempio, se utilizzi una variabile di gruppo di modificatori in un titolo di un annuncio e il gruppo di modificatori include tre modificatori (&quot;a buon mercato&quot;, &quot;sconto&quot; e &quot;a buon mercato&quot;), vengono creati tre annunci separati per ogni riga di dati nel feed di dati, uno per ogni modificatore. Allo stesso modo, se includi un gruppo di modificatori con più valori nell’URL di base di un gruppo di annunci, viene creato un set di parole chiave per ciascuno degli URL di base risultanti.

Ogni gruppo di modificatori può includere tutti i modificatori desiderati. Ogni modello può utilizzare un solo gruppo di modificatori.

## Creare un gruppo di modificatori

1. Nel menu principale, fai clic su **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**.

1. Nella barra degli strumenti sopra la tabella dati, fai clic su **[!UICONTROL Modifiers]**.

1. Sopra l&#39;elenco dei gruppi di modificatori, fare clic su **[!UICONTROL Create]**.

1. Specificare le impostazioni del gruppo di modificatori:

   **[!UICONTROL Name]:** Nome del gruppo di modificatori.

   **[!UICONTROL Modifiers]:** I valori del modificatore per il gruppo (uno per riga).

1. Clic **[!UICONTROL Save]**.

## Modificare un gruppo di modificatori

1. Nel menu principale, fai clic su **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**.

1. Nella barra degli strumenti sopra la tabella dati, fai clic su **[!UICONTROL Modifiers]**.

1. Nell&#39;elenco dei gruppi di modificatori fare clic sul nome del gruppo di modificatori.

1. Modificare le impostazioni del gruppo di modificatori:

   **[!UICONTROL Name]:** Nome del gruppo di modificatori.

   **[!UICONTROL Modifiers]:** I valori del modificatore per il gruppo (uno per riga).

1. Clic **[!UICONTROL Save]**.

## Elimina gruppi di modificatori

>[!IMPORTANT]
>
>Quando eliminate un gruppo di modificatori, rimuovete tutte le variabili per quel gruppo di modificatori (indicato come `<modifier_group_name>`) dai campi dei modelli esistenti. Se si tenta di propagare i dati tramite un modello utilizzando variabili per modificatori non esistenti, il processo non riesce1.

1. Nel menu principale, fai clic su **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**.

1. Nella barra degli strumenti sopra la tabella dati, fai clic su **[!UICONTROL Modifiers]**.

1. Selezionare la casella di controllo accanto a ogni gruppo di modificatori che si desidera eliminare.

1. Sopra l&#39;elenco dei gruppi di modificatori, fare clic su **[!UICONTROL Delete]**.

1. Nel messaggio di conferma, fai clic su **[!UICONTROL Yes]**.

1. (Se necessario) [Rimuovi riferimenti al modificatore](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/ad-template-manage.md) da tutti i modelli applicabili.

>[!MORELIKETHIS]
>
>* [Informazioni sui feed di inventario](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md)
>* [Gestire i modelli di annunci](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/ad-template-manage.md)

