---
title: "[!UICONTROL Campaign Assist Report]"
description: Scopri di più su [!UICONTROL Campaign Assist Report].
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '849'
ht-degree: 0%

---

# Il [!UICONTROL Campaign Assist Report]

*Per gli inserzionisti con monitoraggio dei clic per ricerca, social e e commerce e con monitoraggio delle conversioni da Adobe Advertising, Adobe Analytics (con [!DNL Analytics] o forniti nei feed utilizzando un token (`ef_id`solo )*

Il [!UICONTROL Campaign Assist Report] indica quali campagne hanno supportato il processo di conversione. Il riporta come ogni modello di campagne i cui annunci hanno portato a una o più conversioni ha contribuito alle conversioni complessive. Ad esempio, puoi vedere quante conversioni si sono verificate quando gli utenti hanno visto per la prima volta un annuncio dalla campagna A, hanno fatto clic su un annuncio dalla campagna B e quindi hanno effettuato un ordine. Allo stesso modo, puoi vedere quante conversioni si sono verificate dopo che gli utenti hanno interagito con gli annunci di più di 10 campagne.

I risultati del rapporto includono dati aggregati per ogni pattern di campagne nel percorso di conversione, fino alle N campagne meno recenti, per gli eventi che si sono verificati all’interno del [fai clic sull’intervallo di lookback](/help/search-social-commerce/glossary.md#c-d) e [intervallo di lookback delle impression](/help/search-social-commerce/glossary.md#i-j). Ad esempio, se selezioni una dimensione di percorso di cinque (5), il rapporto include percorsi di conversione che includevano fino alle cinque campagne meno recenti, con una riga per ogni modello di campagne di cui sono stati tracciati gli eventi. Ogni riga mostra un modello di campagne, inclusa la prima campagna nel percorso e l’ultima campagna che ha generato conversioni (anche se l’ultima campagna non è compresa nella dimensione del percorso specificata). Per impostazione predefinita, le righe sono in ordine crescente in base al numero di campagne nel percorso.

Facoltativamente, puoi includere dati di conversione aggregati, comprese le metriche personalizzate, per ogni riga. Quando includi le colonne conversioni/ricavi nel rapporto, ogni tipo di conversione viene rappresentato in quattro colonne, mostrando a) il numero totale di conversioni, b) la percentuale di conversioni complessive attribuite a quel pattern di campagna, c) la latenza media in giorni dal primo evento (nella prima campagna) a una conversione e d) la latenza media in giorni dall’ultimo evento (nell’ultima campagna) a una conversione. Quando il percorso di conversione include più campagne della dimensione del percorso specificata, il rapporto include righe aggiuntive che aggregano i dati per le conversioni risultanti dal numero più elevato di campagne (ad esempio tutti i modelli che includevano sei campagne).

Facoltativamente, puoi anche includere la rete di annunci e/o il tipo di evento dopo il nome della campagna, ad esempio `<campaign name> (Google) click`.

Puoi visualizzare i dati relativi ai 18 mesi precedenti.

>[!TIP]
>
>Se le parole chiave del brand si trovano in una campagna diversa dalle parole chiave generiche, il rapporto indica se le parole chiave del brand contribuiscono alle conversioni.

## Colonne disponibili

Di seguito sono riportate le colonne disponibili per ogni rapporto. Le colonne predefinite vengono incluse automaticamente per impostazione predefinita. Puoi aggiungere le colonne personalizzate disponibili dalla sezione Colonne delle impostazioni del rapporto.

| Colonna | Predefinito? | Descrizione |
|----|----|
| [!UICONTROL 1st Campaign] a [!UICONTROL 5th Campaign] | Predefinito | Le cinque prime campagne nel percorso di conversione che si sono verificate nel file dell’inserzionista [fai clic sull’intervallo di lookback](/help/search-social-commerce/glossary.md#c-d) e [intervallo di lookback delle impression](/help/search-social-commerce/glossary.md#i-j).<br><br>Se hai incluso una delle opzioni di rapporto per indicare la rete di annunci, il nome account o il tipo di evento dopo il nome dell’entità, tali informazioni vengono incluse dopo il nome della campagna (ad esempio `"<"campaign name> [Google] [Account1] [impression]`&quot;). |
| [!UICONTROL Path Size] | Predefinito | Il numero di campagne nel percorso di conversione che si sono verificate all’interno dell’inserzionista [fai clic sull’intervallo di lookback](/help/search-social-commerce/glossary.md#c-d) e [intervallo di lookback delle impression](/help/search-social-commerce/glossary.md#i-j). |
| [!UICONTROL First Campaign] | Predefinito | La prima campagna nel percorso di conversione. |
| [!UICONTROL Last Campaign] | Predefinito | L’ultima campagna che ha generato conversioni (anche se l’ultima parola chiave non rientra nelle dimensioni del percorso specificate).<br><br>Se hai incluso una delle opzioni di rapporto per indicare la rete di annunci, il nome account o il tipo di evento dopo il nome dell’entità, tali informazioni vengono incluse dopo il nome della campagna (ad esempio `"<"campaign name> [Google] [Account1] [impression]`&quot;). |
| \[Metriche personalizzate (derivate) specifiche dell’inserzionista\] | Personalizzato | Il valore di una metrica personalizzata creata, calcolata a partire da metriche esistenti. |
| \[Proprietà transazione specifiche dell&#39;inserzionista\] | Personalizzato | Il numero di conversioni per una proprietà di transazione o una metrica di coinvolgimento del sito specificata. |
| [!UICONTROL % of Total] \[proprietà transazione\] | Automatico | (Non disponibile nelle impostazioni del report, ma incluso automaticamente nell&#39;output del report per ogni proprietà di transazione inclusa) Il numero di conversioni per una proprietà di transazione specificata risultanti dal modello della campagna. |
| [!UICONTROL 6th Campaign] a [!UICONTROL 20th Campaign] | Personalizzato | Dalla sesta alla ventesima campagna nel percorso di conversione che si è verificato all’interno dell’inserzionista [fai clic sull’intervallo di lookback](/help/search-social-commerce/glossary.md#c-d) e [intervallo di lookback delle impression](/help/search-social-commerce/glossary.md#i-j).<br><br>Se hai incluso una delle opzioni di rapporto per indicare la rete di annunci, il nome account o il tipo di evento dopo il nome dell’entità, tali informazioni vengono incluse dopo il nome della campagna (ad esempio `"<"campaign name> [Baidu] [Account1] [click]`&quot;). |
| [!UICONTROL Avg. Conv. Latency (First Campaign To Conversion)] \[proprietà transazione\] | Automatico | (Non disponibile nelle impostazioni del rapporto, ma incluso automaticamente nell’output del rapporto per ogni proprietà di transazione inclusa) Latenza media in giorni dal primo evento (nella prima campagna) a una conversione. |
| [!UICONTROL Avg. Conv. Latency (Last Campaign To Conversion)] \[proprietà transazione\] | Automatico | (Non disponibile nelle impostazioni del rapporto, ma incluso automaticamente nell’output del rapporto) Latenza media in giorni dall’ultimo evento (nell’ultima campagna) a una conversione. |
| [!UICONTROL EF Campaign ID] | Personalizzato | ID numerico assegnato alla campagna da Search, Social e Commerce. |
| [!UICONTROL EF Portfolio Group ID] | Personalizzato | L’ID numerico del gruppo di portfolio a cui appartiene il portfolio. |
| [!UICONTROL EF Search Engine ID] | Personalizzato | ID numerico assegnato da Search, Social e Commerce alla rete di annunci: <i>[!UICONTROL 3]</i> per [!DNL Google Ads], <i>[!UICONTROL 10]</i> per [!DNL Microsoft® Advertising], <i>[!UICONTROL 45]</i> per [!DNL Meta], <i>[!UICONTROL 86]</i> per [!DNL Yahoo! Display Network], <i>[!UICONTROL 87]</i> per [!DNL Naver], <i>[!UICONTROL 88]</i> per [!DNL Baidu], <i>[!UICONTROL 90]</i> per [!DNL Yandex], <i>[!UICONTROL 94]</i> per [!DNL Yahoo! Japan Ads], <i>[!UICONTROL 105]</i> per [!DNL Yahoo Native] (obsoleto), oppure <i>[!UICONTROL 106]</i> per [!DNL Pinterest] (obsoleto). |
| [!UICONTROL Portfolio ID] | L’ID numerico del portfolio. |
| [!UICONTROL User SE Account ID] | ID numerico assegnato da Search, Social e Commerce alla rete di annunci. |

<table style="table-layout:auto">

>[!MORELIKETHIS]
>
>* [Informazioni sui rapporti di assistenza](assist-report-about.md)
>* [Il [!UICONTROL Channel Assist Report]](channel-assist-report.md)
>* [Il [!UICONTROL Keyword Assist Report]](keyword-assist-report.md)
>* [Impostazioni dei rapporti di assistenza](assist-report-settings.md)
>* [Generare un rapporto di assistenza](assist-report-generate.md)

