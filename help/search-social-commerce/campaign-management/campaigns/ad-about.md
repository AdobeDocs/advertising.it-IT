---
title: Gestione annunci
description: Scopri gli annunci in Search, Social e Commerce, compresi i tipi di annunci disponibili.
exl-id: 01bd211d-fe6b-4329-90e1-0e54d626c125
feature: Search Campaign Management
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '883'
ht-degree: 0%

---

# Informazioni sugli annunci

Solo *[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads], [!DNL Yandex] e [!DNL Baidu] account esistenti*

Un annuncio può essere visualizzato su un sito Web di destinazione (per il contenuto o campagne di posizionamento); quando un utente cerca una delle parole chiave nel gruppo di annunci (per le campagne di ricerca) o per il contenuto sul sito Web (annunci di ricerca dinamica in [!DNL Google Ads] campagne di sola ricerca); o quando un utente esegue una ricerca rilevante per uno degli elementi nel proprio feed di prodotto [!DNL Google Merchant Center] o [!DNL Microsoft Merchant Center] (annunci di acquisto in [!DNL Google Ads] o annunci di prodotto in [!DNL Microsoft Advertising] campagne).

## Tipi di annunci disponibili

Puoi creare e gestire i tipi di annunci supportati per i gruppi di annunci all’interno di un account di rete di annunci sincronizzato:

* **Annunci di testo o annunci di testo espansi** per un gruppo di annunci in una campagna che esegue il targeting della rete di ricerca. Gli annunci di testo possono includere parametri di tracciamento facoltativi che sostituiscono i parametri a livello di gruppo di annunci o di campagna. A seconda della rete di annunci, puoi creare annunci di testo espansi/estesi o annunci di testo standard.

* **annunci di pubblico** nativi tra dispositivi per [!DNL Microsoft Advertising] campagne in [!DNL Microsoft Audience Network]. Sono disponibili due opzioni per gli annunci di pubblico, in base alle impostazioni della campagna:

   * Se la campagna è collegata a un negozio di centri commerciali, lascia che la rete di annunci generi automaticamente annunci basati sul feed per la campagna, utilizzando le informazioni sul prodotto del negozio. Non è necessario creare annunci basati su feed per la campagna, ma è necessario creare gruppi di annunci con targeting utente.

   * Se la campagna non è collegata a un account del centro commerciale, crea annunci di pubblico basati su immagini utilizzando il formato di annuncio reattivo, che include più risorse di testo e immagini. La rete di annunci assembla gli annunci utilizzando le combinazioni più efficaci di elementi pubblicitari e li visualizza su siti come [!DNL MSN], [!DNL Outlook.com] e [!DNL Microsoft Edge].

* **Annunci di sola chiamata** per [!DNL Google Ads] campagne nella rete di ricerca. Gli annunci di sola chiamata sono annunci di testo che includono un numero di telefono. Facoltativamente, puoi utilizzare un numero di inoltro assegnato a [!DNL Google Ads] per il reporting avanzato delle chiamate.

* **Annunci di ricerca dinamica espansi** (ora denominati solo &quot;annunci di ricerca dinamica&quot; sulle reti di annunci) per [!DNL Google Ads] e [!DNL Microsoft Advertising] gruppi di annunci di ricerca dinamica nelle campagne di ricerca. Gli annunci per ricerca dinamica utilizzano il contenuto del sito web, invece delle parole chiave, per decidere quando visualizzare gli annunci. La rete di annunci genera dinamicamente il titolo, sceglie l’URL della pagina di destinazione e l’URL di visualizzazione e genera automaticamente l’URL finale.

  Puoi definire le pagine dei tuoi siti web il cui contenuto viene utilizzato per eseguire il targeting degli annunci per ricerca dinamica impostando target di ricerca dinamica specifici per il gruppo di annunci. Per [!DNL Google Ads], è possibile creare destinazioni di ricerca dinamiche in Search, Social e Commerce; per [!DNL Microsoft Advertising], è necessario crearle entro [!DNL Microsoft Advertising]. Nelle campagne [!DNL Google Ads], è possibile specificare un dominio e una lingua del sito Web nella sezione &quot;[!DNL DSA Options]&quot; della campagna invece di, o in aggiunta a, la creazione di destinazioni di ricerca dinamica.

  Quando il termine di ricerca di un utente corrisponde esattamente a una parola chiave in una delle campagne basate su parole chiave, viene visualizzato un annuncio della campagna basata su parole chiave invece di un annuncio di ricerca dinamico. La rete di annunci mostra un annuncio di ricerca dinamico invece di un annuncio mirato a parole chiave quando il termine di ricerca dell’utente è una corrispondenza ampia o una frase corrispondente a una delle parole chiave e l’annuncio di ricerca dinamico ha un livello di annuncio più elevato.

  Per ulteriori informazioni sugli annunci per ricerca dinamica, consulta la [[!DNL Google Ads] documentazione](https://support.google.com/google-ads/answer/2471185) e la [[!DNL Microsoft Advertising] documentazione](https://help.ads.microsoft.com/#apex/ads/en/56794).

* **Annunci multimediali** per [!DNL Microsoft Advertising] campagne di ricerca. Gli annunci multimediali sono annunci di grandi dimensioni di immagini che vengono visualizzati in posizioni prominenti della linea principale e della barra laterale e viene visualizzato un solo annuncio multimediale per pagina. Possono includere più risorse di testo e immagini, come annunci reattivi, e la rete di annunci assembla gli annunci utilizzando le combinazioni più efficaci di elementi pubblicitari. Gli annunci multimediali non sostituiscono i posizionamenti degli annunci di testo.

* Righe promozione per **[!DNL Microsoft Advertising]annunci di prodotti (acquisti)** sulla rete di acquisti. Gli annunci commerciali utilizzano i prodotti nel tuo feed di prodotto [!DNL Microsoft Merchant Center] esistente, invece delle parole chiave, per decidere come e dove visualizzare gli annunci. Gli URL della copia e della pagina di destinazione dell’annuncio vengono generati automaticamente dalle informazioni sul prodotto nel feed, ma puoi facoltativamente impostare linee di promozione da includere per il gruppo di annunci.

  Puoi controllare quali prodotti vengono visualizzati con gli annunci di acquisto di [!DNL Microsoft Advertising] impostando gruppi di prodotti separati per il gruppo di annunci, dalla vista [!UICONTROL Campaigns] > [!UICONTROL Campaigns] > [!UICONTROL Product Groups].

  Per ulteriori informazioni sul flusso di lavoro per annunci di prodotti/acquisti, consulta &quot;[Implementare [!DNL Microsoft Advertising] campagne acquisti](/help/search-social-commerce/campaign-management/special-campaign-types/microsoft-shopping-campaigns.md).&quot;  Per ulteriori informazioni sugli annunci dei prodotti, consulta la [documentazione di Microsoft Advertising](https://help.ads.microsoft.com/#apex/3/en/51082).

* Annunci di ricerca reattivi per [!DNL Google Ads] e [!DNL Microsoft Advertising] campagne nella rete di ricerca. La rete di annunci assembla dinamicamente annunci di ricerca responsive basati su testo da un set di titoli e descrizioni di annunci, favorendo combinazioni con prestazioni ottimali. L’annuncio include fino a tre titoli, due descrizioni e un URL personalizzabile dall’URL di base e dai campi opzionali percorso1 e percorso2. Facoltativamente, puoi fissare i titoli e le descrizioni degli annunci a posizioni specifiche.

>[!NOTE]
>
>[!DNL Google Ads] non fornisce dati al di fuori dei suoi editor nativi sulle combinazioni di testo visualizzate come annunci. Per ulteriori informazioni sul reporting per ogni combinazione di testo, consulta la [documentazione di Google Ads](https://support.google.com/google-ads/answer/7684791).

## Visualizzazione [!UICONTROL Ads]

È possibile creare, modificare e cambiare lo stato degli annunci dalla visualizzazione [!UICONTROL Campaigns] > [!UICONTROL Campaigns] > [!UICONTROL Ads].

## Dati sulle prestazioni a livello di annuncio

I dati a livello di annuncio sono disponibili per la maggior parte dei tipi di annuncio.

Tuttavia, non è disponibile per [!DNL Google Ads] campagne Dynamic Search Ad (DSA), Prestazioni massime, Smart Shopping e [!DNL YouTube]. Sono previste discrepanze tra il totale dei dati a livello di annuncio per una campagna e il totale dei dati per la campagna.

| Rete di annunci/Campagna/Tipo di annuncio | Disponibilità dei dati |
|---|---|
| [!DNL Google Ads] annuncio di ricerca dinamica (DSA) | Campagna, gruppo di annunci |
| [!DNL Google Ads] prestazioni max | Campagna |
| [!DNL Google Ads] acquisti, acquisti avanzati | Campagna, gruppo di annunci |
| [!DNL Google Ads] [!DNL YouTube] | Campagna, gruppo di annunci |

>[!MORELIKETHIS]
>
>* [Gestione annunci](ad-manage.md)
