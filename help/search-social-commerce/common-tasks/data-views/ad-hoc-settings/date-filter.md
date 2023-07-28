---
title: Filtra dati per intervallo di date
description: Scopri come utilizzare il filtro dell’intervallo di date globale.
exl-id: e67e843a-1a73-4ab1-9ef7-c97afeb999f6
feature: Search Common Tasks, Search Custom Data Views
source-git-commit: 9c4dcb19e386d8e1eea541776f5b92c9d500ae9f
workflow-type: tm+mt
source-wordcount: '395'
ht-degree: 0%

---

# Filtra dati per intervallo di date

Lo stesso filtro globale per l’intervallo di date viene applicato alla maggior parte delle visualizzazioni dati della campagna, a tutti gli inserzionisti, fatta eccezione per le visualizzazioni predefinite e personalizzate per le quali sono stati salvati intervalli di date specifici. L’intervallo di date predefinito del sistema per le visualizzazioni di gestione delle campagne è &quot;Ieri&quot;.

Le impostazioni dell’intervallo di date vengono salvate in un cookie specifico del browser, pertanto tutte le modifiche al filtro dell’intervallo di date vengono utilizzate per tutti gli inserzionisti ogni volta che effettui l’accesso utilizzando la stessa applicazione del browser fino a quando non modifichi il filtro o elimini il cookie. Ogni applicazione browser utilizzata memorizzerà le impostazioni del filtro per l’intervallo di date in un cookie diverso.

Quando si salva un intervallo di date specifico per una visualizzazione predefinita o personalizzata, tale intervallo viene applicato ogni volta che si applica la visualizzazione, indipendentemente dall&#39;applicazione browser in uso.

>[!NOTE]
>
>* Puoi visualizzare i dati per i 13 mesi precedenti, ma qualsiasi vista personalizzata esistente può includere dati solo per i 180 giorni precedenti.
>* Per visualizzare i dati precedenti, passare alla [[!UICONTROL Reports] visualizza](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-about.md) ed esegui un report di base.
>* È inoltre possibile salvare un intervallo di date per un [visualizzazione predefinita o personalizzata](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md).

## Modificare il filtro data globale nelle visualizzazioni della campagna

1. Sopra qualsiasi tabella di dati in Ricerca \> Campagne \> Campagne, fai clic sull’intervallo di date corrente.

1. In **[!UICONTROL Date Range]** , specificare l&#39;intervallo:

   * Per un intervallo predefinito: seleziona dall’elenco degli incrementi di tempo comuni, compresi tra *[!UICONTROL Today]* a *[!UICONTROL Last 180 Days]*. Il valore predefinito è *[!UICONTROL Yesterday]*.

   * Per un intervallo specifico: Seleziona **[!UICONTROL Custom Date Range]** e quindi specificare la data di inizio e la data di fine.

     Immettere le date nel formato MM/GG/AAAA o MM-GG-AAAA oppure fare clic su ![Icona Calendario](/help/search-social-commerce/assets/calendar.png "Icona Calendario") accanto a ogni campo per aprire il calendario e selezionare una data.

1. (Facoltativo) Confronta i dati per l’intervallo di date specificato con i dati per un secondo intervallo di date:

   1. Sposta il **[!UICONTROL Comparison]** cursore su *[!UICONTROL On]*.

      Quando selezioni questa opzione, vengono aggiunte due colonne aggiuntive per ogni colonna di dati regolare. Ad esempio, invece di includere una sola colonna per &quot;[!UICONTROL Impressions],&quot; la tabella include colonne per &quot;[!UICONTROL Impressions R1],&quot; &quot;[!UICONTROL Impressions R2],&quot; e &quot;[!UICONTROL Impressions Diff].&quot;  Se esporti i dati, le stesse colonne vengono indicate come &quot;[!UICONTROL Impressions Range 1],&quot; &quot;[!UICONTROL Impressions Range 2],&quot; e &quot;[!UICONTROL Impressions Difference].&quot;

   1. Specifica il secondo intervallo di date.

   1. Scegli come esprimere la differenza tra i dati nei due intervalli di date selezionati nel &quot;\[_Campo dati_\] Differenza&quot;:

      * *[!UICONTROL Variance]* (impostazione predefinita): mostra la differenza come valore numerico.

      * *[!UICONTROL % Change]:*  Mostra la differenza come percentuale.

1. Clic **[!UICONTROL Apply]**.
