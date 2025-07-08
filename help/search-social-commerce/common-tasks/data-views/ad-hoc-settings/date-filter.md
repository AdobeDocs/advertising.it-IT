---
title: Filtra dati per intervallo di date
description: Scopri come utilizzare il filtro dell’intervallo di date globale.
exl-id: 35c0f63f-84ae-4e8e-8a48-acae7ff24498
feature: Search Common Tasks, Search Custom Data Views
source-git-commit: a438e0c24f9ff83941710f890c55c94b74d4d0f3
workflow-type: tm+mt
source-wordcount: '398'
ht-degree: 0%

---

# Filtra dati per intervallo di date

<!-- The same in new UI and legacy CM views -->

Lo stesso filtro globale per l’intervallo di date viene applicato alla maggior parte delle visualizzazioni dati, a tutti gli inserzionisti, fatta eccezione per le visualizzazioni predefinite e personalizzate per le quali sono stati salvati intervalli di date specifici. L’intervallo di date predefinito del sistema per le visualizzazioni di gestione delle campagne è &quot;Ieri&quot;.

Le impostazioni dell’intervallo di date vengono salvate in un cookie specifico del browser, pertanto tutte le modifiche al filtro dell’intervallo di date vengono utilizzate per tutti gli inserzionisti ogni volta che effettui l’accesso utilizzando la stessa applicazione del browser fino a quando non modifichi il filtro o non elimini il cookie. Ogni applicazione browser utilizzata memorizza le impostazioni del filtro per l’intervallo di date in un cookie diverso.

Quando si salva un intervallo di date specifico per una visualizzazione predefinita o personalizzata, tale intervallo viene applicato ogni volta che si applica la visualizzazione, indipendentemente dall&#39;applicazione browser in uso.

>[!NOTE]
>
>* Puoi visualizzare i dati per i 13 mesi precedenti, ma qualsiasi vista personalizzata esistente può includere dati solo per i 180 giorni precedenti.
>* Per visualizzare i dati precedenti, passare alla visualizzazione [[!UICONTROL Reports]](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-about.md) ed eseguire un report di base.
>* È inoltre possibile salvare un intervallo di date per una [visualizzazione predefinita o personalizzata](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md).

## Modificare il filtro data globale nelle visualizzazioni della campagna

1. Sopra qualsiasi tabella di dati in Ricerca \> Campagne \> Campagne, fai clic sull’intervallo di date corrente.

1. Nel campo **[!UICONTROL Date Range]**, specificare l&#39;intervallo:

   * Per un intervallo predefinito: selezionare dall&#39;elenco degli incrementi di tempo comuni, compresi tra *[!UICONTROL Today]* e *[!UICONTROL Last 180 Days]*. Il valore predefinito è *[!UICONTROL Yesterday]*.

   * Per un intervallo specifico: selezionare **[!UICONTROL Custom Date Range]**, quindi specificare la data di inizio e la data di fine.

     Immettere le date nel formato MM/GG/AAAA o MM-GG-AAAA oppure fare clic su ![Icona Calendario](/help/search-social-commerce/assets/calendar.png "Icona Calendario") accanto a ogni campo per aprire il calendario e selezionare una data.

1. (Facoltativo) Confronta i dati per l’intervallo di date specificato con i dati per un secondo intervallo di date:

   1. Spostare il dispositivo di scorrimento **[!UICONTROL Comparison]** nella posizione &quot;on&quot;.

      Quando selezioni questa opzione, vengono aggiunte due colonne aggiuntive per ogni colonna di dati regolare. Ad esempio, invece di includere solo una colonna per &quot;[!UICONTROL Impressions]&quot;, la tabella include colonne per &quot;[!UICONTROL Impressions R1],&quot; &quot;[!UICONTROL Impressions R2]&quot; e &quot;[!UICONTROL Impressions Diff]&quot;.&quot;  Se si esportano i dati, le stesse colonne vengono indicate come &quot;[!UICONTROL Impressions Range 1]&quot;, &quot;[!UICONTROL Impressions Range 2]&quot; e &quot;[!UICONTROL Impressions Difference]&quot;.&quot;

   1. Specifica il secondo intervallo di date.

   1. Scegli come esprimere la differenza tra i dati nei due intervalli di date selezionati nella colonna &quot;\[_Campo dati_\] Differenza&quot;:

      * *[!UICONTROL Variance]* (impostazione predefinita): mostra la differenza come valore numerico.

      * *[!UICONTROL % Change]:* mostra la differenza come percentuale.

1. Fare clic su **[!UICONTROL Apply]**.
