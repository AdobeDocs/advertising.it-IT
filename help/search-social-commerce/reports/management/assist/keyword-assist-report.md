---
title: "[!UICONTROL Keyword Assist Report]"
description: Scopri di più su [!UICONTROL Keyword Assist Report].
source-git-commit: e2df0116f912ca9cbf3d140dec4da57536b929bd
workflow-type: tm+mt
source-wordcount: '778'
ht-degree: 0%

---

# Il [!UICONTROL Keyword Assist Report]

*Per gli inserzionisti con monitoraggio dei clic per ricerca, social e e commerce e con monitoraggio delle conversioni da Adobe Advertising, Adobe Analytics (con [!DNL Analytics] o forniti nei feed utilizzando un token (`ef_id`solo )*

Il [!UICONTROL Keyword Assist Report] indica le parole chiave o i posizionamenti su cui si fa clic. Il rapporto mostra ogni pattern di parole chiave di ricerca a pagamento o posizionamenti che hanno ricevuto clic in un percorso di conversione e indica come tale pattern ha contribuito alle conversioni complessive. Ad esempio, puoi vedere quante conversioni si sono verificate quando gli utenti hanno fatto clic per la prima volta su un annuncio risultante da una ricerca per parola chiave di &quot;scarpe di pelle&quot;, poi hanno fatto clic su un annuncio dopo aver cercato per parola chiave di &quot;scarpe scamosciate&quot; e poi hanno effettuato un ordine; oppure puoi vedere quante conversioni si sono verificate dopo che gli utenti hanno fatto clic sugli annunci risultanti da più di 10 parole chiave.

I risultati del rapporto includono dati aggregati per un massimo di N primi clic di ricerca a pagamento o di posizionamento nel percorso di conversione che si è verificato negli intervalli di lookback su clic e di lookback su impression dell’inserzionista. Ad esempio, se selezioni una dimensione di percorso di cinque (5), il rapporto è costituito da percorsi di conversione che includevano fino alle cinque prime parole chiave o posizionamenti che hanno ricevuto clic, con una riga per ogni pattern di clic tracciato. Ogni riga include la prima parola chiave o il posizionamento nel percorso e l&#39;ultima parola chiave o posizionamento che ha generato conversioni (anche se l&#39;ultima parola chiave non è compresa nella dimensione del percorso specificata). Per impostazione predefinita, le righe sono in ordine crescente in base al numero di eventi nel percorso.

>[!NOTE]
>
>Se il rapporto include posizionamenti da campagne di ricerca abilitate per il contenuto (che non includono parole chiave), il [!UICONTROL Keyword] mostra i nomi dei gruppi di annunci applicabili, ad esempio &quot;(contenuto adgroup) Nome del gruppo di annunci&quot;.

Facoltativamente, puoi includere dati di conversione aggregati per ogni riga. Quando includi le colonne conversioni/ricavi nel rapporto, ogni tipo di conversione viene rappresentato in quattro colonne, mostrando a) il numero totale di conversioni, b) la percentuale di conversioni complessive attribuite a quel pattern di parola chiave, c) la latenza media in giorni dal primo evento (sulla prima parola chiave) a una conversione e d) la latenza media in giorni dall’ultimo evento (sull’ultima parola chiave) a una conversione. Quando il percorso di conversione include più parole chiave della dimensione del percorso specificata, il rapporto include righe aggiuntive che aggregano i dati per le conversioni risultanti dal numero più elevato di parole chiave (ad esempio tutti i pattern che includevano clic su sei parole chiave).

Puoi visualizzare i dati relativi ai 18 mesi precedenti.

## Colonne disponibili

Di seguito sono riportate le colonne disponibili per ogni rapporto. Le colonne predefinite vengono incluse automaticamente per impostazione predefinita. Puoi aggiungere le colonne personalizzate disponibili dalla sezione Colonne delle impostazioni del rapporto.

| Colonna | Predefinito? | Descrizione |
| ---- | ---- | ---- |
| [!UICONTROL 1st Keyword] a [!UICONTROL 5th Keyword] | Predefinito | La prima parola chiave di ricerca a pagamento o i primi cinque clic di posizionamento nel percorso di conversione che si sono verificati all’interno dell’inserzionista [fai clic sull’intervallo di lookback](/help/search-social-commerce/glossary.md#c-d) e [intervallo di lookback delle impression](/help/search-social-commerce/glossary.md#i-j).<br><br><b>Nota:</b> Se il rapporto include posizionamenti da campagne di ricerca abilitate per il contenuto (che non includono parole chiave), queste colonne mostrano i nomi dei gruppi di annunci applicabili, ad esempio &quot;(contenuto adgroup) Nome del gruppo di annunci&quot;. |
| [!UICONTROL Path Size] | Predefinito | Il numero di parole chiave e/o posizionamenti nel percorso di conversione che si sono verificati all&#39;interno del [fai clic sull’intervallo di lookback](/help/search-social-commerce/glossary.md#c-d) e [intervallo di lookback delle impression](/help/search-social-commerce/glossary.md#i-j). |
| [!UICONTROL First Keyword] | Predefinito | La prima parola chiave o posizione nel percorso di conversione. |
| [!UICONTROL Last Keyword] | Predefinito | Ultima parola chiave o posizionamento che ha generato conversioni (anche se l&#39;ultima parola chiave non è compresa nella dimensione del percorso specificata). |
| \[Metriche personalizzate (derivate) specifiche dell’inserzionista\] | Personalizzato | Il valore di una metrica personalizzata creata, calcolata a partire da metriche esistenti. |
| \[Proprietà transazione specifiche dell&#39;inserzionista\] | Personalizzato | Il numero di conversioni per una proprietà di transazione o una metrica di coinvolgimento del sito specificata. |
| [!UICONTROL % of Total] \[proprietà transazione\] | Automatico | (Non disponibile nelle impostazioni del rapporto, ma incluso automaticamente nell’output del rapporto per ogni proprietà di transazione inclusa) La percentuale delle conversioni complessive tra i portfolio attribuite alla parola chiave e/o al pattern di posizionamento. |
| [!UICONTROL 6th Keyword] a [!UICONTROL 10th Keyword] | Personalizzato | La sesta fino alla decima parola chiave di ricerca a pagamento o i clic di posizionamento nel percorso di conversione che si sono verificati all’interno dell’inserzionista [fai clic sull’intervallo di lookback](/help/search-social-commerce/glossary.md#c-d) e [intervallo di lookback delle impression](/help/search-social-commerce/glossary.md#i-j).<br><br><b>Nota:</b> Se il rapporto include posizionamenti da campagne di ricerca abilitate per il contenuto (che non includono parole chiave), queste colonne mostrano i nomi dei gruppi di annunci applicabili, ad esempio &quot;(contenuto adgroup) Nome del gruppo di annunci&quot;. |
| [!UICONTROL Avg. Conv. Latency (First Channel To Conversion)] \[proprietà transazione\] | Automatico | (Non disponibile nelle impostazioni del rapporto, ma incluso automaticamente nell’output del rapporto per ogni proprietà di transazione inclusa) Latenza media in giorni dal primo evento (sulla prima parola chiave o posizionamento) a una conversione. |
| [!UICONTROL Avg. Conv. Latency (Last Channel To Conversion)] \[proprietà transazione\] | Automatico | (Non disponibile nelle impostazioni del rapporto, ma incluso automaticamente nell’output del rapporto) La latenza media in giorni dall’ultimo evento (sull’ultima parola chiave o posizionamento) a una conversione. |
| [!UICONTROL Path Frequency] | Personalizzato | Il numero di volte in cui il percorso per questa riga si è verificato prima della conversione. |

<table style="table-layout:auto">

>[!MORELIKETHIS]
>
>* [Informazioni sui rapporti di assistenza](assist-report-about.md)
>* [Il [!UICONTROL Campaign Assist Report]](campaign-assist-report.md)
>* [Il [!UICONTROL Channel Assist Report]](channel-assist-report.md)
>* [Impostazioni dei rapporti di assistenza](assist-report-settings.md)
>* [Generare un rapporto di assistenza](assist-report-generate.md)
