---
title: Copiare nodi secondari in un altro nodo di destinazione allo stesso livello
description: Scopri come copiare tutti i nodi secondari di un nodo di destinazione principale in un altro nodo di destinazione allo stesso livello
feature: Creative Experiences
exl-id: b3705689-57b6-41ce-9e00-2358bd195c93
TQID: https://experienceleague.adobe.com/KLKVrggOQ8V99Cd-2PcFEdwImKvLYkskSD-DPDvpwu0
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 286
ht-degree: 0%

---

# Copiare nodi secondari in un altro nodo di destinazione allo stesso livello

*Esperienze con targeting solo per la struttura decisionale*

Puoi copiare tutti i nodi secondari di un nodo di destinazione principale (inclusi tutti i target secondari e i bundle creativi loro assegnati) in un altro nodo di destinazione allo stesso livello. È possibile copiare i nodi a) aggiungendo i nodi copiati al framework esistente oppure b) sostituendo completamente il framework esistente. <!-- Give the main use case or an example to explain. -->

Questa funzionalità non influisce sulla destinazione specificata per il nodo padre, ma solo sui nodi figlio.

<!-- 1. [ways to get to the decision tree] -->

1. Fai clic sul nodo principale di cui desideri copiare gli elementi secondari, fai clic su ![Aggiungi](/help/creative/assets/add.png "Aggiungi"), quindi seleziona a\) **[!UICONTROL Copy Children ctrl+c]** o b\) immetti **[!UICONTROL Ctrl+C]** ([!DNL Microsoft Windows]) o **[!UICONTROL Command-C]** ([!DNL Apple Macintosh]) sulla tastiera.

1. Effettuare una delle seguenti operazioni:

   * Per sostituire tutti i nodi figlio e i creativi di un nodo, fare clic sul nodo in cui si desidera incollare le informazioni copiate, fare clic su **...**, quindi selezionare **[!UICONTROL Replace ctrl+shift+v]** o b\) immettere **[!UICONTROL Ctrl+Shift+V]** ([!DNL Microsoft Windows]) o **[!UICONTROL Command-Shift-V]** ([!DNL Apple Macintosh]) sulla tastiera.

   * (Nodi con più destinazioni secondarie, nessun nodo &quot;All&quot; e nessun solo creativo) Per aggiungere tutti i nodi secondari e i creativi a un nodo, senza eliminare quelli esistenti, fare clic sul nodo in cui si desidera incollare le informazioni copiate, fare clic su **...** e selezionare **[!UICONTROL Add ctrl+v]** **&#x200B; o b\) immettere &#x200B;** [!UICONTROL Ctrl+V] **&#x200B; ([!DNL Microsoft Windows]) o &#x200B;** [!UICONTROL Command-V]** ([!DNL Apple Macintosh]) sulla tastiera.

<!--
1. (Optional) To save the experience, click **[!UICONTROL Save]**, and then do the following.
...

These formatted steps are inserted automatically from text in the following file in the _includes folder, which reused in multiple places.
-->

{{$include /help/_includes/experience-save.md}}

>[!MORELIKETHIS]
>
>* [Aggiungere un nodo di destinazione al livello finale](experience-target-node-add-final.md)
>* [Inserire un nodo di destinazione tra i nodi](experience-target-node-add-inner.md)
>* [Aggiungere un nodo di destinazione di pari livello tra nodi](experience-target-node-add-sibling.md)
>* [Assegna creatività a un nodo finale](experience-assign-creative-bundles.md)
>* [Eliminare un nodo di destinazione o un nodo foglia creativo](/help/creative/experiences/experience-target-node-delete.md)
>* [Crea un&#39;esperienza con il targeting dell&#39;albero delle decisioni](experience-create-targeting.md)
>* [Modifica un&#39;esperienza con il targeting dell&#39;albero delle decisioni](experience-edit-targeting.md)
>* [Impostazioni esperienza di destinazione](experience-settings-targeting.md)
