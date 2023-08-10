---
title: Implementare [!DNL Google Ads] annunci di ricerca dinamica
description: Scopri il flusso di lavoro per la configurazione di [!DNL Google Ads] annunci di ricerca dinamica.
exl-id: 4c806824-b582-46dc-8d88-85c73bfb0944
feature: Search Campaign Management
source-git-commit: f80d05aa40fd4114e9585220fe747ca7d36a19bb
workflow-type: tm+mt
source-wordcount: '612'
ht-degree: 0%

---

# Implementare [!DNL Google Ads] annunci di ricerca dinamica

*[!DNL Google Ads]campagne di sola ricerca con solo tracciamento a livello creativo o di parola chiave e a livello creativo*

Gli annunci per ricerca dinamica utilizzano il contenuto del sito web, invece delle parole chiave, per decidere quando visualizzare gli annunci. Puoi definire le pagine dei tuoi siti web il cui contenuto viene utilizzato per eseguire il targeting degli annunci per ricerca dinamica impostando target di ricerca dinamica separati per il gruppo di annunci o scegliendo un’impostazione a livello di campagna per eseguire il targeting degli annunci utilizzando i contenuti del sito web.

È possibile impostare annunci per la ricerca dinamica singolarmente o utilizzando i bulksheet. Le istruzioni seguenti includono collegamenti alla creazione di singole entità.

## Passaggi per impostare [!DNL Google Ads] annunci di ricerca dinamica

1. [Creare una campagna](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) per gli annunci per ricerca dinamica:

   1. Inizialmente imposta il budget della campagna sul 10% della spesa giornaliera per la campagna di ricerca.

      In seguito puoi aumentare il budget dopo che gli annunci dimostreranno il loro valore.

   1. (Se si desidera [!DNL Google Ads] per visualizzare gli annunci di ricerca dinamica in base al contenuto del sito web) Specifica il dominio principale e la lingua per il dominio nel [!UICONTROL DSA Options] sezione delle impostazioni di campaign.

      >[!NOTE]
      >
      >Il dominio deve essere indicizzato da [!DNL Google Ads] indice di ricerca organica di destinazione. Inoltre, se il dominio contiene pagine in più lingue e desideri eseguirne il targeting per tutte, crea una campagna separata per ciascuna lingua.

      Se non utilizzi il dominio del sito web per eseguire il targeting degli annunci, crea destinazioni di ricerca dinamica (vedi il passaggio 4) per ogni gruppo di annunci. Puoi creare le destinazioni [singolarmente](/help/search-social-commerce/campaign-management/campaigns/dynamic-search-target-manage.md) o utilizzando [fogli di grandi dimensioni](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

   1. Assicurati che la campagna esegua il targeting del canale di ricerca e solo del [!DNL Google Ads] rete di ricerca (non la rete di visualizzazione). Queste impostazioni sono disponibili nella [!UICONTROL Networks and Devices] scheda.

   1. (Facoltativo) Escludi parole chiave sul [!UICONTROL Negatives] scheda.

   1. (Facoltativo) Configura un modello di tracciamento a livello di campagna, che sostituisce il modello di tracciamento a livello di account ma può essere sostituito ai livelli inferiori.

      (Inserzionisti con Adobe Analytics senza tracciamento lato server) Quando desideri includere il tracciamento per il feed inverso da Search, Social e Commerce ad Analytics, aggiungi il codice di tracciamento AMO ID ai parametri di aggiunta a livello di account, che aggiungono il codice all’URL finale. Consulta &quot;[Parametro di tracciamento AMO ID](/help/search-social-commerce/tracking/skwcid-tracking-parameter.md).&quot;

1. [Creare un gruppo di annunci](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md) all’interno della campagna, inclusi i seguenti passaggi:

   1. Imposta il [!UICONTROL Ad Group Type] a **[!UICONTROL Search Dynamic].**

   1. Imposta l&#39;offerta predefinita per tutti gli annunci.

      Se configuri le singole destinazioni di ricerca dinamica, puoi sovrascrivere l’offerta predefinita.

   1. (Facoltativo) Configura un modello di tracciamento a livello di gruppo di annunci, che sostituisce tutti i modelli di tracciamento a livelli superiori ma può essere sostituito a livello di annuncio.

      Se hai aggiunto il tracciamento di Adobe Analytics a livello di campagna e desideri includerlo per il gruppo di annunci, aggiungilo qui. Vedere Passaggio 1e.

1. [Creare ogni annuncio di ricerca dinamica](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md) all’interno del gruppo di annunci.

   [!DNL Google Ads] genera in modo dinamico il titolo, l’URL di visualizzazione e l’URL della pagina di destinazione per ogni annuncio. Facoltativamente, puoi aggiungere reindirizzamenti e tracciamento al modello di tracciamento a livello di annuncio, che sostituisce i modelli di tracciamento a livelli più elevati.
Se desideri escludere il tracciamento di Adobe Analytics a livelli superiori con il tracciamento a livello di annuncio, aggiungilo qui. Vedere i passaggi 1e e 2c.

1. (Obbligatorio se non includi il dominio principale e la lingua per il dominio nella sezione Opzioni DSA delle impostazioni della campagna; facoltativo in caso contrario) Crea [target di ricerca dinamica](/help/search-social-commerce/campaign-management/campaigns/dynamic-search-target-manage.md) per il gruppo di annunci. Facoltativamente, puoi sostituire l’offerta a livello di gruppo di annunci con le offerte a livello di target.

   Le destinazioni definiscono se la rete di annunci utilizza tutte o un sottoinsieme delle pagine del sito web per eseguire il targeting degli annunci di ricerca dinamica. Per tenere traccia in modo ottimale delle prestazioni, configura la campagna con un gruppo di annunci per destinazione di ricerca dinamica e includi un gruppo di annunci che esegue il targeting di tutti i criteri.

1. Se necessario, [modificare le impostazioni della campagna](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) per regolare il budget della campagna e per perfezionare il traffico escludendo parole chiave aggiuntive dalla campagna.
