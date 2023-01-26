---
title: Creare manualmente i dettagli dell’ID offerta
description: Scopri come inserire manualmente i dettagli di un ID offerta.
feature: DSP Private Inventory, DSP Deal IDs
exl-id: 20a57919-c68f-4c9d-a8e1-f49484f74655
source-git-commit: 2fe1ee7366c84f3a7d770aa3412fdde61829fe46
workflow-type: tm+mt
source-wordcount: '405'
ht-degree: 0%

---

# Creare manualmente i dettagli dell’ID offerta

1. Nel menu principale, fai clic su **[!UICONTROL Inventory]** > **[!UICONTROL Deals].**

1. Sopra la tabella dati, fai clic su **[!UICONTROL Create]**, quindi seleziona **[!UICONTROL Deal ID]**.

1. Inserisci il [impostazioni dell&#39;offerta](deal-id-settings.md):

   1. In [!UICONTROL Deal ID basics] specifica i dettagli dell’offerta e gli inserzionisti che possono accedere all’offerta. Per le offerte garantite, devi inoltre specificare le date del volo previste e il numero stimato di impression, solo a scopo di tracciamento.

      Puoi tenere traccia della velocità delle offerte garantite includendo la colonna di spesa &quot;PG Impression Pacing&quot; nella vista Inventario > Offerte.

   1. (Solo utenti amministratori; opzionale) [!UICONTROL Technical] modificare le impostazioni predefinite in base alle esigenze.

   1. Clic **[!UICONTROL Save]**.

1. (Solo offerte garantite) Seleziona gli annunci da utilizzare per l’offerta e crea un posizionamento programmatico predefinito garantito (PG).

   I posizionamenti PG predefiniti garantiscono che l’offerta restituisca sempre un’offerta per ogni richiesta di offerta. Se non crei un posizionamento PG predefinito, tutti i posizionamenti che hanno come target l&#39;offerta non posizionano le offerte a meno che non siano impostati correttamente. È sempre necessario creare un posizionamento PG predefinito. In [!UICONTROL Placements] visualizzazione, i posizionamenti PG predefiniti hanno un [!UICONTROL Sub-type] valore colonna di &quot;[!UICONTROL PG Default].&quot;

   Facoltativamente, puoi utilizzare l’offerta come destinazione di inventario in posizionamenti aggiuntivi, ma devi impostarla correttamente per inserire le offerte.

   1. In [!UICONTROL Ad & Campaign Selection] , seleziona gli annunci che verranno utilizzati per l&#39;offerta:

      1. Seleziona l’inserzionista, la campagna e il tipo di annuncio. Facoltativamente, seleziona uno stato di annuncio in base al quale filtrare gli annunci.

      1. Dall’elenco degli annunci disponibili, seleziona la casella di controllo accanto a ciascun annuncio da utilizzare per l’offerta.

      1. Clic **[!UICONTROL Apply]**.
   1. Nella schermata delle impostazioni di posizionamento:

      1. Immettere il nome del posizionamento.

      1. (Facoltativo) Modifica il [impostazioni di posizionamento](/help/dsp/campaign-management/placements/placement-settings.md), compresa la sovrascrittura dell&#39;offerta predefinita, compilata automaticamente con il valore CPM dell&#39;operazione; modifica dell’intervallo di date; o allegando altri annunci.

      L&#39;offerta viene automaticamente indirizzata nella sezione Destinazioni di inventario . Tutte le altre opzioni di targeting non sono applicabili.

      1. Clic **[!UICONTROL Create placement]**.



Dopo aver creato l&#39;offerta, puoi utilizzare l&#39;offerta come destinazione di inventario per più posizionamenti.

>[!NOTE]
>
> Non devi inviare il tag dell’offerta all’editore per la verifica.

>[!TIP]
>
>* In [!UICONTROL Inventory] > [!UICONTROL Deals] visualizzazione [!UICONTROL Pacing & Budget] la colonna mostra il modo in cui l’accordo viene passato alla data di volo e all’obiettivo di impression specificati.
>
>* Se la consegna è in ritardo o in eccesso, contatta l’editore per stabilire il volume che sta inviando tramite l’offerta.


>[!MORELIKETHIS]
>
>* [Impostazioni ID offerta manuale](deal-id-settings.md)
>* [Imposta un accordo garantito programmatico](programmatic-guaranteed-set-up.md)
>* [Invia un annuncio per un contratto garantito a livello di programmazione con [!DNL FreeWheel]](freewheel-submit.md)
>* [Informazioni sulle offerte garantite a livello di programmazione](programmatic-guaranteed-about.md)

<!-- >* [Specify Placements and Ads for a Private Deal](deal-id-attach-placements.md)-->