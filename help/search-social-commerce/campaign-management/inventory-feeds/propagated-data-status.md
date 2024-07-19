---
title: Stati dei dati generati dai feed
description: Scopri gli stati dei dati generati dai feed di dati di inventario.
exl-id: 45c93fb2-0ed2-4336-9883-e150c292a7a5
feature: Search Inventory Feeds
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 0%

---

# Stati dei dati generati dai feed

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] (elimina solo azioni) e [!DNL Yandex] account solo*

Ciascun componente può avere uno dei seguenti stati:

* *[!UICONTROL New]:* Il componente non esiste nella rete di annunci e non è stato pubblicato nella rete di annunci. Se necessario, è comunque possibile modificarne le impostazioni facendo clic sul nome del componente. Quando si è pronti a pubblicare i dati, fare clic su **[!UICONTROL Post to SE]** e specificare i dati da inviare.

* *[!UICONTROL Posted]:* (solo campagne e gruppi di annunci) La campagna o il gruppo di annunci è stato pubblicato parzialmente nella rete di annunci, ma alcuni componenti non sono stati pubblicati a causa di errori. Lo stato di convalida di ogni parola chiave e annuncio mostra quali informazioni devono essere corrette. Se necessario, puoi modificare le impostazioni del componente facendo clic sul nome del componente.

* *[!UICONTROL Active]:* Il componente è già attivo nella rete di annunci e non è possibile modificarne le impostazioni qui. I componenti attivi possono includere sottocomponenti [!UICONTROL New], che possono essere pubblicati se i dati sono validi.

* *[!UICONTROL Paused]:* Il componente è già in pausa nella rete di annunci e non è possibile modificarne le impostazioni qui. I componenti in pausa possono includere sottocomponenti [!UICONTROL New], che possono essere inviati se i dati sono validi.

* *[!UICONTROL Deleted]:* Il componente è già stato eliminato nella rete di annunci e non puoi modificarne le impostazioni qui. I componenti eliminati possono includere sottocomponenti [!UICONTROL New], che possono essere inviati se i dati sono validi.

>[!MORELIKETHIS]
>
>* [Informazioni sui feed inventario](inventory-feeds-about.md)
>* [Visualizza dati generati dai feed](propagated-data-view.md)
>* [Modifica dati generati dai feed](propagated-data-edit.md)
>* [Pubblica i dati della campagna generati dai feed alle reti di annunci](propagated-data-post.md)
>* [Interrompere un processo di registrazione per i dati del feed inventario](stop-job.md)
