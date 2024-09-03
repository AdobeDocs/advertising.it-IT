---
title: Implementa [!DNL Google Ads] annunci per ricerca dinamica
description: Scopri il flusso di lavoro per la configurazione di  [!DNL Google Ads] annunci per ricerca dinamica.
exl-id: 69e5069f-3f82-4ee3-841a-0c1292677223
feature: Search Campaign Management
source-git-commit: 283fced2b3faa64b6383b6ab2a41696cba0da06f
workflow-type: tm+mt
source-wordcount: '614'
ht-degree: 0%

---

# Implementa [!DNL Google Ads] annunci per ricerca dinamica

*[!DNL Google Ads]campagne di sola ricerca con solo tracciamento a livello creativo o di parola chiave e a livello creativo*

Gli annunci per ricerca dinamica utilizzano il contenuto del sito web, invece delle parole chiave, per decidere quando visualizzare gli annunci. Puoi definire le pagine dei tuoi siti web il cui contenuto viene utilizzato per eseguire il targeting degli annunci per ricerca dinamica impostando target di ricerca dinamica separati per il gruppo di annunci o scegliendo un’impostazione a livello di campagna per eseguire il targeting degli annunci utilizzando i contenuti del sito web.

È possibile impostare annunci per la ricerca dinamica singolarmente o utilizzando i bulksheet. Le istruzioni seguenti includono collegamenti alla creazione di singole entità.

## Passaggi per impostare [!DNL Google Ads] annunci per ricerca dinamica

1. [Crea una campagna](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) per annunci di ricerca dinamica:

   1. Inizialmente imposta il budget della campagna sul 10% della spesa giornaliera per la campagna di ricerca.

      In seguito puoi aumentare il budget dopo che gli annunci dimostreranno il loro valore.

   1. Se desideri che [!DNL Google Ads] mostri gli annunci per ricerca dinamica in base al contenuto del sito Web, specifica il dominio principale e la lingua per il dominio nella sezione [!UICONTROL DSA Options] delle impostazioni della campagna.

      >[!NOTE]
      >
      >Il dominio deve essere indicizzato dall&#39;indice di ricerca organica [!DNL Google Ads] per essere destinato. Inoltre, se il dominio contiene pagine in più lingue e desideri eseguirne il targeting per tutte, crea una campagna separata per ciascuna lingua.

      Se non utilizzi il dominio del sito web per eseguire il targeting degli annunci, crea destinazioni di ricerca dinamica (vedi il passaggio 4) per ogni gruppo di annunci. Puoi creare le destinazioni [singolarmente](/help/search-social-commerce/campaign-management/campaigns/dynamic-search-target-manage.md) o utilizzando [fogli collettivi](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

   1. Verificare che la campagna sia indirizzata al canale di ricerca e solo alla rete di ricerca [!DNL Google Ads] (non alla rete di visualizzazione). Queste impostazioni sono disponibili nella scheda [!UICONTROL Networks and Devices].

   1. (Facoltativo) Escludere le parole chiave nella scheda [!UICONTROL Negatives].

   1. (Facoltativo) Configura un modello di tracciamento a livello di campagna, che sostituisce il modello di tracciamento a livello di account ma può essere sostituito ai livelli inferiori.

      (Inserzionisti con Adobe Analytics senza tracciamento lato server) Quando desideri includere il tracciamento per il feed inverso da Search, Social e Commerce ad Analytics, aggiungi il codice di tracciamento AMO ID ai parametri di aggiunta a livello di account, che aggiungono il codice all’URL finale. Vedi &quot;[ID Adobe Advertising utilizzati da [!DNL Analytics]](/help/integrations/analytics/ids.md).&quot;

1. [Crea un gruppo di annunci](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md) all&#39;interno della campagna, inclusi i seguenti passaggi:

   1. Imposta [!UICONTROL Ad Group Type] su **[!UICONTROL Search Dynamic].**

   1. Imposta l&#39;offerta predefinita per tutti gli annunci.

      Se configuri le singole destinazioni di ricerca dinamica, puoi sovrascrivere l’offerta predefinita.

   1. (Facoltativo) Configura un modello di tracciamento a livello di gruppo di annunci, che sostituisce tutti i modelli di tracciamento a livelli superiori ma può essere sostituito a livello di annuncio.

      Se hai aggiunto il tracciamento di Adobe Analytics a livello di campagna e desideri includerlo per il gruppo di annunci, aggiungilo qui. Vedere Passaggio 1e.

1. [Crea ogni annuncio di ricerca dinamica](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md) all&#39;interno del gruppo di annunci.

   [!DNL Google Ads] genera in modo dinamico il titolo, l&#39;URL di visualizzazione e l&#39;URL della pagina di destinazione per ogni annuncio. Facoltativamente, puoi aggiungere reindirizzamenti e tracciamento al modello di tracciamento a livello di annuncio, che sostituisce i modelli di tracciamento a livelli più elevati.
Se desideri escludere il tracciamento di Adobe Analytics a livelli superiori con il tracciamento a livello di annuncio, aggiungilo qui. Vedere i passaggi 1e e 2c.

1. (Obbligatorio se non si includono il dominio radice e la lingua per il dominio nella sezione Opzioni DSA delle impostazioni della campagna; facoltativo in caso contrario) Crea [destinazioni di ricerca dinamica](/help/search-social-commerce/campaign-management/campaigns/dynamic-search-target-manage.md) per il gruppo di annunci. Facoltativamente, puoi sostituire l’offerta a livello di gruppo di annunci con le offerte a livello di target.

   Le destinazioni definiscono se la rete di annunci utilizza tutte o un sottoinsieme delle pagine del sito web per eseguire il targeting degli annunci di ricerca dinamica. Per tenere traccia in modo ottimale delle prestazioni, configura la campagna con un gruppo di annunci per destinazione di ricerca dinamica e includi un gruppo di annunci che esegue il targeting di tutti i criteri.

1. Se necessario, [modifica le impostazioni della campagna](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) per regolare il budget della campagna e per perfezionare il traffico escludendo altre parole chiave dalla campagna.
