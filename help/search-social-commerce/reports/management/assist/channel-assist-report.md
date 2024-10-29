---
title: '[!UICONTROL Channel Assist Report]'
description: Informazioni su [!UICONTROL Channel Assist Report].
exl-id: 67bce347-2776-4585-adb4-e1a4d76fbadc
feature: Search Reports, Search Assist Reports
source-git-commit: 45920c6ea9d2953c963ddf6472966b3fc3a91395
workflow-type: tm+mt
source-wordcount: '684'
ht-degree: 0%

---

# [!UICONTROL Channel Assist Report]

*Inserzionisti con il tracciamento dei clic di Search, Social e Commerce e con il tracciamento delle conversioni da Adobe Advertising, Adobe Analytics (con integrazione [!DNL Analytics]) o forniti nei feed utilizzando solo un token (`ef_id`)*

[!UICONTROL Channel Assist Report] indica in che modo diversi canali di marketing (ricerca o social da Search, Social e Commerce; visualizzazione o video da Advertising DSP) hanno supportato il processo di conversione. Il rapporto mostra in che modo ogni modello di tipi di evento che ha portato a una o più conversioni ha contribuito alle conversioni complessive. Ad esempio, puoi vedere quante conversioni si sono verificate quando gli utenti hanno visto per la prima volta un’impression di un annuncio di visualizzazione, hanno fatto clic su un annuncio di ricerca e poi hanno effettuato un ordine; oppure puoi vedere quante conversioni si sono verificate dopo che gli utenti hanno interagito con più di 10 annunci. I tipi di evento includono clic di ricerca, impression di visualizzazione e clic, impression video e clic e altre impression e altri clic. <!-- [DSP metrics may show up as "Other Path Length (<length>)" or empty; we're supposed to fill in more values for DSP at some point.] -->

I risultati del report includono dati aggregati per ogni pattern di tipi di evento nel percorso di conversione, fino ai N tipi di evento meno recenti, che si sono verificati nell&#39;[intervallo di lookback su clic](/help/search-social-commerce/glossary.md#c-d) e nell&#39;[intervallo di lookback su impression](/help/search-social-commerce/glossary.md#i-j) dell&#39;inserzionista. Ad esempio, se selezioni una dimensione di percorso di cinque (5), il rapporto include percorsi di conversione che includevano fino ai cinque eventi più antichi, con una riga per ogni pattern di tipi di evento tracciato (ad esempio &quot;clic di ricerca&quot; e quindi &quot;impression di visualizzazione&quot;). Ogni riga mostra un pattern di eventi, inclusi il primo evento nel percorso e l’ultimo evento che ha generato conversioni (anche se l’ultimo evento non rientra nelle dimensioni del percorso specificate). Per impostazione predefinita, le righe sono in ordine crescente in base al numero di eventi nel percorso.

Facoltativamente, puoi includere dati di conversione aggregati per ogni riga. Quando includi le colonne conversioni/ricavi nel rapporto, ogni tipo di conversione viene rappresentato in quattro colonne, mostrando a) il numero totale di conversioni, b) la percentuale delle conversioni complessive attribuite a quel pattern di evento, c) la latenza media in giorno dal primo evento a una conversione e d) la latenza media in giorni dall’ultimo evento a una conversione. Quando il percorso di conversione include più eventi della dimensione del percorso specificata, il rapporto include righe aggiuntive che aggregano i dati per le conversioni risultanti dal numero più elevato di eventi (ad esempio tutti i modelli che includono sei tipi di eventi).

Puoi visualizzare i dati relativi ai 18 mesi precedenti.

## Colonne disponibili

Di seguito sono riportate le colonne disponibili per ogni rapporto. Le colonne predefinite vengono incluse automaticamente per impostazione predefinita. Puoi aggiungere le colonne personalizzate disponibili dalla sezione Colonne delle impostazioni del rapporto.

| Colonna | Predefinito? | Descrizione |
| ---- | ---- | ---- |
| Da [!UICONTROL 1st Event] a [!UICONTROL 5th Event] | Predefinito | I cinque primi tipi di evento nel percorso di conversione che si sono verificati nell&#39;intervallo di lookback [click](/help/search-social-commerce/glossary.md#c-d) e nell&#39;intervallo di lookback [impression](/help/search-social-commerce/glossary.md#i-j) dell&#39;inserzionista. |
| [!UICONTROL Path Size] | Predefinito | Il numero di tipi di evento nel percorso di conversione che si sono verificati nell&#39;intervallo di lookback [click](/help/search-social-commerce/glossary.md#c-d) e nell&#39;intervallo di lookback [impression](/help/search-social-commerce/glossary.md#i-j) dell&#39;inserzionista. |
| [!UICONTROL First Event Type] | Predefinito | Tipo di evento del primo evento (meno recente) nel percorso di conversione. |
| [!UICONTROL Last Event Type] | Predefinito | Il tipo di evento dell’ultimo evento che ha generato conversioni (anche se l’ultimo evento non rientra nelle dimensioni del percorso specificate). |
| \[Metriche personalizzate (derivate) specifiche dell’inserzionista\] | Personalizzato | Il valore di una metrica personalizzata creata, calcolata a partire da metriche esistenti. |
| \[Metriche di conversione specifiche per l’inserzionista\] | Personalizzato | Il numero di conversioni per una metrica di conversione o una metrica di coinvolgimento del sito specificata. |
| [!UICONTROL % of Total] \[metrica di conversione\] | Automatico | (Non disponibile nelle impostazioni del rapporto, ma incluso automaticamente nell’output del rapporto per ogni metrica di conversione inclusa) La percentuale delle conversioni complessive tra i portfolio attribuite al modello di evento. |
| Da [!UICONTROL 6th Event] a [!UICONTROL 30th Event] | Personalizzato | Tipi di evento dal sesto al trentesimo nel percorso di conversione che si sono verificati nell&#39;[intervallo di lookback su clic](/help/search-social-commerce/glossary.md#c-d) e nell&#39;[intervallo di lookback su impression](/help/search-social-commerce/glossary.md#i-j) dell&#39;inserzionista. |
| [!UICONTROL Avg. Conv. Latency (First Channel To Conversion)] \[metrica di conversione\] | Automatico | (Non disponibile nelle impostazioni del rapporto, ma incluso automaticamente nell’output del rapporto per ogni metrica di conversione inclusa) La latenza media in giorni dal primo evento a una conversione. |
| [!UICONTROL Avg. Conv. Latency (Last Channel To Conversion)] \[metrica di conversione\] | Automatico | (Non disponibile nelle impostazioni del rapporto, ma incluso automaticamente nell’output del rapporto) Latenza media in giorni dall’ultimo evento a una conversione. |
| [!UICONTROL Path Frequency] | Personalizzato | Il numero di volte in cui il percorso per questa riga si è verificato prima della conversione. |

>[!MORELIKETHIS]
>
>* [Informazioni sui report di assistenza](assist-report-about.md)
>* [I [!UICONTROL Campaign Assist Report]](campaign-assist-report.md)
>* [I [!UICONTROL Keyword Assist Report]](keyword-assist-report.md)
>* [Assist impostazioni report](assist-report-settings.md)
>* [Genera un report di assistenza](assist-report-generate.md)
