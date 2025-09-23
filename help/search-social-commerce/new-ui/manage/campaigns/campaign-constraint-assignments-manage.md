---
title: Gestire le assegnazioni dei vincoli per le campagne
description: Scopri come assegnare vincoli alle campagne.
feature: Search Optimization, Search Campaign Management
hide: true
exl-id: d886a228-24d7-4d8e-b68a-76e56b4304ed
source-git-commit: df5d34c7d86174107278e0cd4f5a99329a21ca61
workflow-type: tm+mt
source-wordcount: '430'
ht-degree: 0%

---

# (Nuova interfaccia) Gestire le assegnazioni dei vincoli per le campagne

*funzionalità Beta*

Puoi assegnare e rimuovere vincoli di offerta per le seguenti entità di ricerca: campagna, gruppo di annunci, parola chiave, posizionamento, gruppo di prodotti a livello di unità e destinazione di ricerca dinamica. Ogni entità può avere un solo vincolo.

I vincoli vengono ereditati dalle entità figlio, pertanto non è necessario assegnare vincoli alle entità figlio a meno che non si desideri sostituire i valori ereditati.

L’annullamento dell’assegnazione di un vincolo rimuove l’associazione con i componenti conto e tutti i relativi componenti figlio e i dati del rapporto relativi al vincolo non sono più disponibili per tali componenti. L’annullamento dell’assegnazione di un vincolo non comporta l’eliminazione del vincolo né dei componenti dell’account.

>[!NOTE]
>
>* Se successivamente modificate una parola chiave o la copia dell&#39;annuncio per un annuncio, creando in tal modo una nuova parola chiave o un nuovo annuncio, il vincolo non viene assegnato alla nuova entità.
>* I vincoli attivi limitano le offerte solo per le unità di offerta assegnate nei portfolio legacy ottimizzati a livello di parola chiave. Vengono ignorate per le unità di offerta presenti in portafogli attivi, in portafogli ibridi o che non appartengono a portafogli.

## Assegna un vincolo alle campagne selezionate dalla nuova visualizzazione [!UICONTROL Campaigns]

Puoi assegnare un singolo vincolo a una o più campagne.

1. Nel menu principale, fare clic su **[!UICONTROL Manage]>[!UICONTROL Campaigns]**.

1. Seleziona la casella di controllo accanto a ciascuna campagna a cui assegnare un singolo vincolo.

1. Nella barra degli strumenti delle azioni in blocco, fare clic su **+[!UICONTROL Assign]** > **[!UICONTROL Constraint]**.

1. Selezionate il vincolo.

1. Fare clic su **[!UICONTROL Assign Now]**.

## Assegna un vincolo alle unità di offerta di ricerca selezionate dalle viste legacy [!UICONTROL Campaigns]

1. In **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**, selezionare la visualizzazione del componente account.

1. Selezionare la casella di controllo accanto a ogni riga pertinente.

   Per suggerimenti sulla selezione di più righe, vedere &quot;[Selezionare più righe](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

1. Nella barra degli strumenti sopra la tabella dati fare clic su **[!UICONTROL More]** e quindi su **[!UICONTROL Assign]** > **[!UICONTROL Constraint]**.

1. Selezionare il vincolo applicabile.

1. (Facoltativo) Immettere ulteriori dettagli:

   1. Accanto a [!UICONTROL Additional Details], fare clic su **[!UICONTROL Open]** per espandere i dettagli.

   1. Immettere un **[!UICONTROL Project Name]** facoltativo e/o un **[!UICONTROL Description]** facoltativo.

1. Fare clic su **[!UICONTROL Save]**.

## Annulla l&#39;assegnazione dei vincoli dalle campagne selezionate dalla nuova visualizzazione [!UICONTROL Campaigns]

1. Nel menu principale, fare clic su **[!UICONTROL Manage]>[!UICONTROL Campaigns]**.

1. Seleziona la casella di controllo accanto a ciascuna campagna da cui annullare l’assegnazione dei vincoli.

1. Nella barra degli strumenti Azioni in blocco fare clic su **-[!UICONTROL Unassign]** > **[!UICONTROL Constraint]**.

1. Fare clic su **[!UICONTROL Confirm]**.

## Annulla l&#39;assegnazione di vincoli alle unità di offerta di ricerca dalle viste legacy [!UICONTROL Campaigns]

>[!NOTE]
>
>Per eliminare un vincolo rendendolo non disponibile per utilizzi futuri, vedere &quot;Eliminare i vincoli per le unità di offerta di ricerca&quot; nel capitolo della Guida all&#39;ottimizzazione relativo a &quot;Vincoli di offerta&quot;, disponibile all&#39;interno di Search, Social e Commerce.<!-- verify convention for referencing Optimization Guide here -->

1. In **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**, selezionare la visualizzazione del componente account.

1. Selezionare la casella di controllo accanto a ogni componente da cui si desidera rimuovere il vincolo.

   Per suggerimenti sulla selezione di più righe, vedere &quot;[Selezionare più righe](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

1. Nella barra degli strumenti sopra la tabella dati fare clic su **[!UICONTROL More]** e quindi su **[!UICONTROL Unassign]** > **[!UICONTROL Constraint]**.

1. Nella finestra di dialogo di conferma, selezionare **[!UICONTROL Yes, Unassign]**.

>[!MORELIKETHIS]
>
>* [Gestisci assegnazioni vincoli per gruppi di annunci](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-constraint-assignments-manage.md)
