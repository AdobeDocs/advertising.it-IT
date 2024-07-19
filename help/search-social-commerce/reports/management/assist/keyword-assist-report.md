---
title: '[!UICONTROL Keyword Assist Report]'
description: Informazioni su [!UICONTROL Keyword Assist Report].
exl-id: 24e5854c-5696-43cd-ac21-64209f9f57d4
feature: Search Reports, Search Assist Reports
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '781'
ht-degree: 0%

---

# [!UICONTROL Keyword Assist Report]

*Inserzionisti con il tracciamento dei clic di Search, Social e Commerce e con il tracciamento delle conversioni da Adobe Advertising, Adobe Analytics (con integrazione [!DNL Analytics]) o forniti nei feed utilizzando solo un token (`ef_id`)*

[!UICONTROL Keyword Assist Report] indica le parole chiave o i posizionamenti su cui si fa clic. Il rapporto mostra ogni pattern di parole chiave di ricerca a pagamento o posizionamenti che hanno ricevuto clic in un percorso di conversione e indica come tale pattern ha contribuito alle conversioni complessive. Ad esempio, puoi vedere quante conversioni si sono verificate quando gli utenti hanno fatto clic per la prima volta su un annuncio risultante da una ricerca per parola chiave di &quot;scarpe di pelle&quot;, poi hanno fatto clic su un annuncio dopo aver cercato per parola chiave di &quot;scarpe scamosciate&quot; e poi hanno effettuato un ordine; oppure puoi vedere quante conversioni si sono verificate dopo che gli utenti hanno fatto clic sugli annunci risultanti da più di 10 parole chiave.

I risultati del rapporto includono dati aggregati per un massimo di N primi clic di ricerca a pagamento o di posizionamento nel percorso di conversione che si è verificato all’interno dell’inserzionista
fai clic su intervalli di lookback e di lookback di impression. Ad esempio, se selezioni una dimensione di percorso di cinque (5), il rapporto è costituito da percorsi di conversione che includevano fino alle cinque prime parole chiave o posizionamenti che hanno ricevuto clic, con una riga per ogni pattern di clic tracciato. Ogni riga include la prima parola chiave o il posizionamento nel percorso e l&#39;ultima parola chiave o posizionamento che ha generato conversioni (anche se l&#39;ultima parola chiave non è compresa nella dimensione del percorso specificata). Per impostazione predefinita, le righe sono in ordine crescente in base al numero di eventi nel percorso.

>[!NOTE]
>
>Se il rapporto include posizionamenti da campagne di ricerca abilitate per il contenuto (che non includono parole chiave), la colonna [!UICONTROL Keyword] mostra i nomi dei gruppi di annunci applicabili, ad esempio &quot;(contenuto adgroup) Nome del gruppo di annunci.&quot;

Facoltativamente, puoi includere dati di conversione aggregati per ogni riga. Quando includi le colonne conversioni/ricavi nel rapporto, ogni tipo di conversione viene rappresentato in quattro colonne, mostrando a) il numero totale di conversioni, b) la percentuale di conversioni complessive attribuite a quel pattern di parola chiave, c) la latenza media in giorni dal primo evento (sulla prima parola chiave) a una conversione e d) la latenza media in giorni dall’ultimo evento (sull’ultima parola chiave) a una conversione. Quando il percorso di conversione include più parole chiave rispetto alla dimensione del percorso specificata, il rapporto include righe aggiuntive che aggregano i dati per le conversioni risultanti dal numero più elevato di parole chiave (ad esempio tutti i pattern che includevano clic su sei parole chiave).

Puoi visualizzare i dati relativi ai 18 mesi precedenti.

## Colonne disponibili

Di seguito sono riportate le colonne disponibili per ogni rapporto. Le colonne predefinite vengono incluse automaticamente per impostazione predefinita. Puoi aggiungere le colonne personalizzate disponibili dalla sezione Colonne delle impostazioni del rapporto.

| Colonna | Predefinito? | Descrizione |
| ---- | ---- | ---- |
| Da [!UICONTROL 1st Keyword] a [!UICONTROL 5th Keyword] | Predefinito | I primi cinque clic di posizionamento o parola chiave di ricerca a pagamento nel percorso di conversione che si sono verificati nell&#39;[intervallo di lookback dei clic](/help/search-social-commerce/glossary.md#c-d) e nell&#39;[intervallo di lookback delle impression](/help/search-social-commerce/glossary.md#i-j) dell&#39;inserzionista.<br><br><b>Nota:</b> se il report include posizionamenti da campagne di ricerca abilitate per il contenuto (che non includono parole chiave), queste colonne mostrano i nomi dei gruppi di annunci applicabili, ad esempio &quot;(contenuto adgroup) Nome del gruppo di annunci&quot;. |
| [!UICONTROL Path Size] | Predefinito | Il numero di parole chiave e/o posizionamenti nel percorso di conversione che si sono verificati all&#39;interno dell&#39;[intervallo di lookback click](/help/search-social-commerce/glossary.md#c-d) e dell&#39;[intervallo di lookback impression](/help/search-social-commerce/glossary.md#i-j) dell&#39;inserzionista. |
| [!UICONTROL First Keyword] | Predefinito | La prima parola chiave o posizione nel percorso di conversione. |
| [!UICONTROL Last Keyword] | Predefinito | Ultima parola chiave o posizionamento che ha generato conversioni (anche se l&#39;ultima parola chiave non è compresa nella dimensione del percorso specificata). |
| \[Metriche personalizzate (derivate) specifiche dell’inserzionista\] | Personalizzato | Il valore di una metrica personalizzata creata, calcolata a partire da metriche esistenti. |
| \[Metriche di conversione specifiche per l’inserzionista\] | Personalizzato | Il numero di conversioni per una metrica di conversione o una metrica di coinvolgimento del sito specificata. |
| [!UICONTROL % of Total] \[metrica di conversione\] | Automatico | (Non disponibile nelle impostazioni del rapporto, ma incluso automaticamente nell’output del rapporto per ogni metrica di conversione inclusa) La percentuale delle conversioni complessive tra i portfolio attribuite alla parola chiave e/o al pattern di posizionamento. |
| Da [!UICONTROL 6th Keyword] a [!UICONTROL 10th Keyword] | Personalizzato | La sesta fino alla decima parola chiave di ricerca a pagamento o il posizionamento fa clic nel percorso di conversione che si è verificato all&#39;interno dell&#39;[intervallo di lookback su clic](/help/search-social-commerce/glossary.md#c-d) e dell&#39;[intervallo di lookback su impression](/help/search-social-commerce/glossary.md#i-j) dell&#39;inserzionista.<br><br><b>Nota:</b> se il report include posizionamenti da campagne di ricerca abilitate per il contenuto (che non includono parole chiave), queste colonne mostrano i nomi dei gruppi di annunci applicabili, ad esempio &quot;(contenuto adgroup) Nome del gruppo di annunci&quot;. |
| [!UICONTROL Avg. Conv. Latency (First Channel To Conversion)] \[metrica di conversione\] | Automatico | (Non disponibile nelle impostazioni del rapporto, ma incluso automaticamente nell’output del rapporto per ogni metrica di conversione inclusa) La latenza media in giorni dal primo evento (sulla prima parola chiave o posizionamento) a una conversione. |
| [!UICONTROL Avg. Conv. Latency (Last Channel To Conversion)] \[metrica di conversione\] | Automatico | (Non disponibile nelle impostazioni del rapporto, ma incluso automaticamente nell’output del rapporto) La latenza media in giorni dall’ultimo evento (sull’ultima parola chiave o posizionamento) a una conversione. |
| [!UICONTROL Path Frequency] | Personalizzato | Il numero di volte in cui il percorso per questa riga si è verificato prima della conversione. |

>[!MORELIKETHIS]
>
>* [Informazioni sui report di assistenza](assist-report-about.md)
>* [I [!UICONTROL Campaign Assist Report]](campaign-assist-report.md)
>* [I [!UICONTROL Channel Assist Report]](channel-assist-report.md)
>* [Assist impostazioni report](assist-report-settings.md)
>* [Genera un report di assistenza](assist-report-generate.md)
