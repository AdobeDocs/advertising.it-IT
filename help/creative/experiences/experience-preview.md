---
title: Visualizzare l’anteprima di un’esperienza
description: Scopri come visualizzare in anteprima i creativi in un’esperienza di annuncio.
feature: Creative Experiences
exl-id: 2ac8f580-7d3d-4de6-ba14-5d72b30188d7
source-git-commit: 278104fb09797e781894a6894a0a53db4a8e28f8
workflow-type: tm+mt
source-wordcount: '556'
ht-degree: 0%

---

# Visualizzare l’anteprima di un’esperienza

*Versione beta chiusa*

Puoi visualizzare in anteprima i creativi con una dimensione di annuncio specifica che verrà visualizzata dagli utenti target per un’esperienza, inclusi tutti i collegamenti ipertestuali. Per le esperienze con il targeting dell’albero decisionale, puoi visualizzare in anteprima un singolo creativo, i creativi di un particolare ramo (tipo di target) o tutti i creativi nell’esperienza. Per le esperienze senza targeting della struttura decisionale, puoi visualizzare in anteprima un singolo contenuto creativo. <!-- verify -->

* Quando visualizzi l’anteprima di tutti i creativi dell’esperienza o di un ramo specifico, vengono visualizzati tutti i creativi applicabili.

* Quando visualizzi l’anteprima di un singolo contenuto creativo e di più contenuti creativi che soddisfano i criteri, il contenuto creativo visualizzato ogni volta che aggiorni l’anteprima si basa sulle impostazioni di rotazione degli annunci per l’esperienza:

   * Per la rotazione degli annunci algoritmici, il contenuto creativo viene selezionato in base all’obiettivo di ottimizzazione.

   * Per la rotazione ponderata degli annunci, il contenuto creativo viene selezionato ogni volta in base ai pesi specificati (ad esempio, una probabilità dell’80% che venga visualizzato Creative A e del 20% che venga visualizzato Creative B).

   * Per la rotazione pianificata degli annunci, viene visualizzata la prima creatività della pianificazione. È possibile continuare ad aggiornare l&#39;anteprima per continuare la sequenza.<!-- Refresh isn't there as of 2/3 -->

## Visualizzare in anteprima i creativi in un’esperienza con il targeting dell’albero decisionale

1. Nel menu principale, fare clic su **[!UICONTROL Creative]** > **[!UICONTROL Experiences]**.

1. (Facoltativo) [Personalizza la visualizzazione](/help/creative/introduction/customize-data-views.md) per includere esperienze specifiche.

1. Effettuare una delle seguenti operazioni:

   * Nella vista a schede, fai clic su **[!UICONTROL ...]** accanto al nome dell&#39;esperienza e quindi su **[!UICONTROL Preview]**.

   * Nella visualizzazione per tabella, posizionare il cursore sulla riga, fare clic su **[!UICONTROL More]** e quindi su **[!UICONTROL Preview]**.

1. Seleziona i creativi da visualizzare in anteprima:

   * Per visualizzare in anteprima un singolo contenuto creativo:

      1. Fare clic su **[!UICONTROL Creative]**.

      1. Seleziona la dimensione dell’annuncio.

      1. Nella sezione [!UICONTROL Decision Tree Targeting], seleziona la destinazione creativa.

   * Per visualizzare in anteprima i creativi di un ramo specifico:

      1. Fare clic su **[!UICONTROL Particular branch]**.

      1. Seleziona la dimensione dell’annuncio.

     <!-- I don't see this as of 2/3:
     1. Select whether to group the creatives by Rotation Type or Ad Size.
     -->

      1. Seleziona il target creativo.

   * Per visualizzare in anteprima tutti i creativi dell&#39;esperienza, fare clic su **[!UICONTROL Entire Tree]**.

     <!-- I don't see this as of 2/3:
     1. Click **[!UICONTROL Entire Tree]**.
     1. Select the ad size.
     1. Select whether to group the creatives by Rotation Type or Ad Size.
     -->

1. (Facoltativo) Per includere il nome del contenuto creativo, il tipo e la dimensione del contenuto creativo, l&#39;URL della pagina di destinazione o gli URL di clic e gli attributi flessibili sotto ogni contenuto creativo, selezionare **[!UICONTROL Display Creative Metadata]**.

1. Fare clic su **[!UICONTROL Preview]**.

1. (Anteprima solo per contenuto creativo; facoltativo) Nella barra degli strumenti, fare clic su **[!UICONTROL Refresh]** per visualizzare in anteprima eventuali contenuti creativi aggiuntivi che potrebbero essere visualizzati, in base alle impostazioni di rotazione degli annunci.<!-- I don't see this as of 2/3 -->

1. (Facoltativo) Per copiare un URL demo dell&#39;esperienza da condividere con altre persone senza accesso a [!DNL Creative]:

   1. In alto a destra nell&#39;anteprima, fai clic su ![Condividi](/help/creative/assets/share.png "Condividi").

   1. Nella finestra di dialogo [!UICONTROL Share Demo URL], fai clic su **[!UICONTROL Copy]** per copiare l&#39;URL negli Appunti e condividerlo con un altro utente.

## Visualizzare un’anteprima dei creativi in un’esperienza senza il targeting dell’albero decisionale

1. Nel menu principale, fare clic su **[!UICONTROL Creative]** > **[!UICONTROL Experiences]**.

1. (Facoltativo) [Personalizza la visualizzazione](/help/creative/introduction/customize-data-views.md) per includere esperienze specifiche.

1. Effettuare una delle seguenti operazioni:

   * Nella vista a schede, fai clic su **[!UICONTROL ...]** accanto al nome dell&#39;esperienza e quindi su **[!UICONTROL Preview]**.

   * Nella visualizzazione per tabella, posizionare il cursore sulla riga, fare clic su **[!UICONTROL More]** e quindi su **[!UICONTROL Preview]**.

1. (Facoltativo) Limita l’elenco dei creativi selezionando una dimensione creativa specifica.

   Per impostazione predefinita, sono elencate le creatività di tutte le dimensioni.

1. Fai clic sul nome di un tag annuncio per espandere la riga e visualizzare in anteprima i contenuti creati.

1. (Facoltativo) Per passare alla pagina di destinazione di un contenuto creativo, fai clic sul contenuto creativo.

   <!-- Verify:  Will the creative click be tracked like a regular ad click but not linked to a publisher and placement? Explain effect/consequences. -->

1. (Facoltativo) Per copiare un URL demo dell&#39;esperienza da condividere con altre persone senza accesso a [!DNL Creative]:

   1. In alto a destra nell&#39;anteprima, fai clic su ![Condividi](/help/creative/assets/share2.png "Condividi").

   1. Nella finestra di dialogo [!UICONTROL Share Demo URL], fai clic su **[!UICONTROL Copy]** per copiare l&#39;URL negli Appunti e condividerlo con un altro utente.

>[!MORELIKETHIS]
>
>* [Crea un&#39;esperienza con il targeting dell&#39;albero delle decisioni](experience-create-targeting.md)
>* [Crea un&#39;esperienza senza il targeting dell&#39;albero delle decisioni](/help/creative/experiences/experience-create-no-targeting.md)
