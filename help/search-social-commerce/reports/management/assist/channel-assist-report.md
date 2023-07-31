---
title: '[!UICONTROL Channel Assist Report]'
description: Scopri di più su [!UICONTROL Channel Assist Report].
exl-id: 49616327-72e9-49c6-90b9-91c7486e8417
feature: Search Reports, Search Assist Reports
source-git-commit: 97111c6cd38098cac72b8773390afd254a017d1d
workflow-type: tm+mt
source-wordcount: '681'
ht-degree: 0%

---

# Il [!UICONTROL Channel Assist Report]

*Per gli inserzionisti con tracciamento dei clic per ricerche, social e e commerce e con tracciamento delle conversioni da Adobi Advertising, Adobe Analytics (con [!DNL Analytics] o forniti nei feed utilizzando un token (`ef_id`solo )*

Il [!UICONTROL Channel Assist Report] indica in che modo vari canali di marketing (ricerca o social da Search, Social e Commerce; o visualizzazione o video da Advertising DSP) hanno assistito il processo di conversione. Il rapporto mostra in che modo ogni modello di tipi di evento che ha portato a una o più conversioni ha contribuito alle conversioni complessive. Ad esempio, puoi vedere quante conversioni si sono verificate quando gli utenti hanno visto per la prima volta un’impression di un annuncio di visualizzazione, hanno fatto clic su un annuncio di ricerca e poi hanno effettuato un ordine; oppure puoi vedere quante conversioni si sono verificate dopo che gli utenti hanno interagito con più di 10 annunci. I tipi di evento includono clic di ricerca, impression di visualizzazione e clic, impression video e clic e altre impression e altri clic. <!-- [DSP metrics may show up as "Other Path Length (<length>)" or empty; we're supposed to fill in more values for DSP at some point.] -->

I risultati del report includono dati aggregati per ogni pattern di tipi di evento nel percorso di conversione, fino ai N tipi di evento più recenti, che si sono verificati all&#39;interno del [fai clic sull’intervallo di lookback](/help/search-social-commerce/glossary.md#c-d) e [intervallo di lookback delle impression](/help/search-social-commerce/glossary.md#i-j). Ad esempio, se selezioni una dimensione di percorso di cinque (5), il rapporto include percorsi di conversione che includevano fino ai cinque eventi più antichi, con una riga per ogni pattern di tipi di evento tracciato (ad esempio &quot;clic di ricerca&quot; e quindi &quot;impression di visualizzazione&quot;). Ogni riga mostra un pattern di eventi, inclusi il primo evento nel percorso e l’ultimo evento che ha generato conversioni (anche se l’ultimo evento non rientra nelle dimensioni del percorso specificate). Per impostazione predefinita, le righe sono in ordine crescente in base al numero di eventi nel percorso.

Facoltativamente, puoi includere dati di conversione aggregati per ogni riga. Quando includi le colonne conversioni/ricavi nel rapporto, ogni tipo di conversione viene rappresentato in quattro colonne, mostrando a) il numero totale di conversioni, b) la percentuale delle conversioni complessive attribuite a quel pattern di evento, c) la latenza media in giorno dal primo evento a una conversione e d) la latenza media in giorni dall’ultimo evento a una conversione. Quando il percorso di conversione include più eventi della dimensione del percorso specificata, il rapporto include righe aggiuntive che aggregano i dati per le conversioni risultanti dal numero più elevato di eventi (ad esempio tutti i modelli che includono sei tipi di eventi).

Puoi visualizzare i dati relativi ai 18 mesi precedenti.

## Colonne disponibili

Di seguito sono riportate le colonne disponibili per ogni rapporto. Le colonne predefinite vengono incluse automaticamente per impostazione predefinita. Puoi aggiungere le colonne personalizzate disponibili dalla sezione Colonne delle impostazioni del rapporto.

| Colonna | Predefinito? | Descrizione |
| ---- | ---- | ---- |
| [!UICONTROL 1st Event] a [!UICONTROL 5th Event] | Predefinito | I cinque primi tipi di evento nel percorso di conversione che si sono verificati all&#39;interno dell&#39;inserzionista [fai clic sull’intervallo di lookback](/help/search-social-commerce/glossary.md#c-d) e [intervallo di lookback delle impression](/help/search-social-commerce/glossary.md#i-j). |
| [!UICONTROL Path Size] | Predefinito | Il numero di tipi di evento nel percorso di conversione che si sono verificati all&#39;interno del [fai clic sull’intervallo di lookback](/help/search-social-commerce/glossary.md#c-d) e [intervallo di lookback delle impression](/help/search-social-commerce/glossary.md#i-j). |
| [!UICONTROL First Event Type] | Predefinito | Tipo di evento del primo evento (meno recente) nel percorso di conversione. |
| [!UICONTROL Last Event Type] | Predefinito | Il tipo di evento dell’ultimo evento che ha generato conversioni (anche se l’ultimo evento non rientra nelle dimensioni del percorso specificate). |
| \[Metriche personalizzate (derivate) specifiche dell’inserzionista\] | Personalizzato | Il valore di una metrica personalizzata creata, calcolata a partire da metriche esistenti. |
| \[Proprietà transazione specifiche dell&#39;inserzionista\] | Personalizzato | Il numero di conversioni per una proprietà di transazione o una metrica di coinvolgimento del sito specificata. |
| [!UICONTROL % of Total] \[proprietà transazione\] | Automatico | (Non disponibile nelle impostazioni del rapporto, ma incluso automaticamente nell’output del rapporto per ogni proprietà di transazione inclusa) La percentuale delle conversioni complessive tra i portfolio attribuite al modello di evento. |
| [!UICONTROL 6th Event] a [!UICONTROL 30th Event] | Personalizzato | Dal sesto al trentesimo tipo di evento nel percorso di conversione che si è verificato all’interno del [fai clic sull’intervallo di lookback](/help/search-social-commerce/glossary.md#c-d) e [intervallo di lookback delle impression](/help/search-social-commerce/glossary.md#i-j). |
| [!UICONTROL Avg. Conv. Latency (First Channel To Conversion)] \[proprietà transazione\] | Automatico | (Non disponibile nelle impostazioni del rapporto, ma incluso automaticamente nell’output del rapporto per ogni proprietà di transazione inclusa) Latenza media in giorni dal primo evento a una conversione. |
| [!UICONTROL Avg. Conv. Latency (Last Channel To Conversion)] \[proprietà transazione\] | Automatico | (Non disponibile nelle impostazioni del rapporto, ma incluso automaticamente nell’output del rapporto) Latenza media in giorni dall’ultimo evento a una conversione. |
| [!UICONTROL Path Frequency] | Personalizzato | Il numero di volte in cui il percorso per questa riga si è verificato prima della conversione. |

>[!MORELIKETHIS]
>
>* [Informazioni sui rapporti di assistenza](assist-report-about.md)
>* [Il [!UICONTROL Campaign Assist Report]](campaign-assist-report.md)
>* [Il [!UICONTROL Keyword Assist Report]](keyword-assist-report.md)
>* [Impostazioni dei rapporti di assistenza](assist-report-settings.md)
>* [Generare un rapporto di assistenza](assist-report-generate.md)
