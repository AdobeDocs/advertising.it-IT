---
title: Stati dei dati generati dai feed
description: Scopri gli stati dei dati generati dai feed di dati di inventario.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 0%

---

# Stati dei dati generati dai feed

*[!DNL Google Ads], [!DNL Microsoft® Advertising], [!DNL Yahoo! Japan Ads] (solo azioni di eliminazione), e [!DNL Yandex] solo account*

Ciascun componente può avere uno dei seguenti stati:

* *[!UICONTROL New]:* Il componente non esiste nella rete di annunci e non è stato pubblicato nella rete di annunci. Se necessario, puoi comunque modificarne le impostazioni facendo clic sul nome del componente. Quando sei pronto a pubblicare i dati, fai clic su **[!UICONTROL Post to SE]** e specifica i dati da inviare.

* *[!UICONTROL Posted]:* (Solo campagne e gruppi di annunci) La campagna o il gruppo di annunci è stato pubblicato parzialmente nella rete di annunci, ma alcuni componenti non sono stati pubblicati a causa di errori. Lo stato di convalida di ogni parola chiave e annuncio mostra quali informazioni devono essere corrette. Se necessario, puoi modificare le impostazioni del componente facendo clic sul nome del componente.

* *[!UICONTROL Active]:* Il componente è già attivo nella rete di annunci e non puoi modificarne le impostazioni qui. I componenti attivi possono includere sottocomponenti [!UICONTROL New], che può essere pubblicato se i dati sono validi.

* *[!UICONTROL Paused]:* Il componente è già in pausa nella rete pubblicitaria e non puoi modificarne le impostazioni qui. I componenti in pausa possono includere sottocomponenti [!UICONTROL New], che può essere pubblicato se i dati sono validi.

* *[!UICONTROL Deleted]:* Il componente è già stato eliminato nella rete di annunci e non puoi modificarne le impostazioni qui. I componenti eliminati possono includere sottocomponenti [!UICONTROL New], che può essere pubblicato se i dati sono validi.

>[!MORELIKETHIS]
>
>* [Informazioni sui feed di inventario](inventory-feeds-about.md)
>* [Visualizzare i dati generati dai feed](propagated-data-view.md)
>* [Modificare i dati generati dai feed](propagated-data-edit.md)
>* [Pubblicare i dati della campagna generati dai feed nelle reti di annunci](propagated-data-post.md)
>* [Interrompere un processo di registrazione per i dati di feed inventario](stop-job.md)

