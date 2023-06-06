---
title: Operazioni eseguibili nei bulksheet
description: Fai riferimento a informazioni generali sull’aggiunta, la modifica e l’eliminazione di dati di campagne utilizzando i bulksheet.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 0%

---

# Operazioni eseguibili nei bulksheet

È possibile aggiungere, modificare ed eliminare dati della campagna tramite bulksheet per [reti pubblicitarie supportate](../bulksheet-about.md#bulksheet-functionality-by-network).

Includi una riga di dati separata per ciascun componente della campagna (campagna, gruppo di annunci, parola chiave o annuncio di testo) che desideri aggiungere, modificare o eliminare o di cui desideri aggiungere, modificare o eliminare le proprietà. Ad esempio, per creare una campagna con un gruppo di annunci, una parola chiave e un annuncio, per un totale di quattro componenti, sono necessarie quattro righe di dati separate. Per modificare [!UICONTROL Ad Group Name] per un gruppo di annunci (un componente), tuttavia, è necessaria una sola riga. Allo stesso modo, per modificare quattro proprietà diverse per un gruppo di annunci (un componente), è necessaria una sola riga.

Le seguenti regole si applicano all’utilizzo dei componenti della campagna e delle relative proprietà.

* Aggiunta di:

   * Per aggiungere un componente, includi tutti i campi necessari per aggiungerlo e, facoltativamente, includi i campi per una qualsiasi delle proprietà del componente.

   * Per aggiungere una proprietà per un componente esistente, ad esempio [!UICONTROL Ad Group End Date] per un gruppo di annunci, includi tutti i campi necessari per modificare tale componente (gruppo di annunci) più il campo per la proprietà ([!UICONTROL Ad Group End Date]).

* Per modificare una proprietà per un componente esistente, includi tutti i campi necessari per modificare tale componente e il campo della proprietà.

   Se si lascia vuoto il campo proprietà, il valore esistente viene mantenuto.

* Eliminazione di:

   * Per eliminare un componente esistente, includi tutti i campi necessari per modificarlo e cambiarne lo stato in [!UICONTROL Deleted]. Ad esempio, per eliminare un [!DNL Google Ads] gruppo di annunci, devi includere [!UICONTROL Campaign Name], [!UICONTROL Ad Group Name], [!UICONTROL Ad Group Status] con un valore di <i>[!UICONTROL Deleted]</i>, e [!UICONTROL Ad Group ID].

   * ([!UICONTROL Param1], [!UICONTROL Param2], e [!UICONTROL Param3] solo valori) Per eliminare un [!DNL paramN] per una parola chiave, includi tutti i campi necessari per modificare la parola chiave ed elimina anche il [!DNL paramN] valore immettendo il valore `[delete]` (comprese le parentesi) nel campo corrispondente.

   * (Campi delle proprietà consentiti) Per eliminare un valore di proprietà esistente per un componente, includi tutti i campi necessari per modificare tale componente ed elimina anche il valore della proprietà immettendo il valore `[delete]` (comprese le parentesi). I campi consentiti includono:

      * ([!UICONTROL Google Ads] solo ) [!UICONTROL Description Line 1], [!UICONTROL Description Line 2]

      * ([!DNL Google Ads] e [!DNL Microsoft® Advertising] solo ) [!UICONTROL Product Scope Filter], [!UICONTROL Base URL/Final URL], [!UICONTROL Tracking Template]

>[!NOTE]
>
>Quando si include un valore in un campo non applicabile all&#39;azione, qualsiasi valore immesso nel campo viene ignorato.

>[!MORELIKETHIS]
>
>* [Informazioni sulla gestione dei dati della campagna tramite bulksheet](../bulksheet-about.md)
>* [Formati di file di bulksheet supportati](bulksheet-file-formats.md)
>* [Appendice - Errori di bulksheet](../bulksheet-errors.md)
>* [Scaricare/creare un file bulksheet](../bulksheet-download.md)

