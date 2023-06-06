---
title: Gestire le visualizzazioni predefinite e personalizzate
description: Scopri come personalizzare le viste predefinite e personalizzate.
source-git-commit: d47dca053868946cdec2d9b1418b44793393338f
workflow-type: tm+mt
source-wordcount: '2831'
ht-degree: 0%

---

# Gestire le visualizzazioni predefinite e personalizzate

Le viste predefinite e le viste personalizzate ti consentono di personalizzare i dati delle prestazioni visualizzati nelle viste dati della campagna di ricerca. Le impostazioni di visualizzazione includono le colonne da includere, i filtri, l’intervallo di date, le impostazioni di attribuzione della conversione e altre impostazioni avanzate. È possibile applicare le impostazioni temporaneamente o salvarle. (Eccezione: Non è possibile salvare i filtri per le viste predefinite). Ogni visualizzazione personalizzata predefinita e regolare è applicabile a una visualizzazione di entità specifica (ad esempio [!UICONTROL Campaigns]) e solo un account inserzionista specifico. Ogni vista personalizzata universale è applicabile tra le viste delle entità per un inserzionista specifico e pertanto non può includere colonne di proprietà (come il nome o lo stato dell’entità), che variano in base al tipo di entità.

Le viste predefinite vengono visualizzate per impostazione predefinita a ogni accesso. Puoi creare viste personalizzate aggiuntive e applicarle in qualsiasi momento. Facoltativamente, puoi condividere qualsiasi visualizzazione personalizzata creata con tutti gli altri utenti che possono visualizzare i dati dell’inserzionista. Negli elenchi di visualizzazione, ogni visualizzazione condivisa da un’altra persona viene formattata in corsivo, ad esempio &quot;*Campagne dalle prestazioni migliori*.&quot; Solo l&#39;utente che crea una visualizzazione personalizzata può eliminarla.

Ogni vista è disponibile come scelta rapida nella [!UICONTROL Custom Views] sezione del pannello sinistro.

## Applicare una visualizzazione predefinita o personalizzata

* (Visualizzazioni predefinite) Nel menu principale, fai clic su **[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**. Nei sottomenu, fare clic su **[!UICONTROL Live]** \> **\[tipo di entità\]**.

* (Visualizzazioni personalizzate) Dal pannello di navigazione a sinistra:

   1. Nel pannello a sinistra, fai clic su **[!UICONTROL Custom Views]** per espanderlo.

      Le visualizzazioni sono ordinate in base all’entità applicabile.

   1. Espandere i menu disponibili.

      &quot;[!UICONTROL Universal Views]&quot; include visualizzazioni personalizzate che possono essere utilizzate in tutte le visualizzazioni di entità. Tutte le altre viste personalizzate sono raggruppate per tipo di entità.

   1. Fare clic sul nome della visualizzazione.

      Se la vista è universale o si applica all&#39;entità corrente, la tabella dati viene visualizzata nuovamente in base alla configurazione della vista. Se la vista si applica a un&#39;entità diversa, i dati per l&#39;entità applicabile vengono visualizzati in base alla configurazione della vista.

## Creare una visualizzazione personalizzata {#create-custom-view}

Le visualizzazioni personalizzate sono applicabili solo alle visualizzazioni di gestione delle campagne.

>[!NOTE]
>
>Oltre alle impostazioni di visualizzazione specificate per la visualizzazione personalizzata, viene salvato anche l&#39;ordinamento delle colonne corrente.

1. Nella parte destra della barra degli strumenti sopra la tabella dati, fare clic sul nome della visualizzazione corrente (che potrebbe essere &quot;[!UICONTROL Default]&quot;).

1. Specifica la [impostazioni di visualizzazione personalizzata](#view-settings):

   1. (Facoltativo) Per rendere le impostazioni dei dati disponibili in tutte le visualizzazioni di entità (per [!UICONTROL Campaigns], [!UICONTROL Ads]e così via), seleziona **[!UICONTROL Universal View]**.

      Dopo aver attivato o disattivato questa opzione, non è possibile salvare la modifica nella vista esistente, ma è possibile crearne una nuova con la modifica.

   1. (Facoltativo) Per rendere la visualizzazione disponibile a tutti gli altri utenti che possono visualizzarne i dati, spostare il **[!UICONTROL Shared]** cursore su *[!UICONTROL Yes]*.

   1. (Facoltativo) Il **[!UICONTROL Columns]** , modificare le colonne disponibili per la scheda, il relativo ordine e l&#39;ordinamento delle righe.

   1. (Facoltativo) Fai clic su **[!UICONTROL Filters]** e quindi specificare i filtri da applicare.

      L’applicazione dei filtri restituisce le righe solo quando il valore di una metrica soddisfa i criteri specificati, indipendentemente dal fatto che la metrica venga inclusa o meno come colonna nel rapporto.

   1. (Facoltativo) Fai clic su **[!UICONTROL Date]** e modificare le impostazioni di data predefinite.

   1. (Facoltativo) Fai clic su **[!UICONTROL Additional Settings]** e modificare le impostazioni.

1. Clic **[!UICONTROL Save as New]**.

1. Immettere il nome della nuova visualizzazione e quindi fare clic su **[!UICONTROL Save]**.

   >[!TIP]
   >
   >Utilizza un nome che ti aiuti a identificare la scheda e le informazioni a cui si applica (ad esempio &quot;Campagne in pausa&quot; o &quot;Primi 50 annunci&quot;).

### Modificare una visualizzazione predefinita o personalizzata

1. Apri le impostazioni di visualizzazione:

   * Se la visualizzazione è già stata applicata, sul lato destro della barra degli strumenti sopra la tabella dati fare clic sul nome della visualizzazione corrente (che potrebbe essere &quot;[!UICONTROL Default]&quot;).

   * (Visualizzazioni personalizzate non applicate) Nel pannello a sinistra, fai clic su ![Visualizzazioni personalizzate](/help/search-social-commerce/assets/custom-views-left-rail_icon.png "Visualizzazioni personalizzate") per espandere [!UICONTROL Custom Views] menu. Fare clic sul nome della visualizzazione personalizzata.

1. Modifica il [impostazioni di visualizzazione](#view-settings):

   1. (Facoltativo) Per abilitare o disabilitare le impostazioni dei dati in tutte le visualizzazioni delle entità di ricerca (per [!UICONTROL Campaigns], [!UICONTROL Ad Groups]e così via), seleziona o deseleziona **[!UICONTROL Universal View]**.

      Non è possibile salvare la modifica nella vista esistente, ma è possibile creare una nuova vista con la modifica.

   1. (Facoltativo; solo visualizzazioni personalizzate create dall&#39;utente) Se la visualizzazione non è già pubblica, renderla disponibile a tutti gli altri utenti che possono visualizzare i dati dell&#39;inserzionista spostando il **[!UICONTROL Shared]** cursore su *[!UICONTROL Yes]*.

   1. (Facoltativo) Il **[!UICONTROL Columns]** , modificare le colonne disponibili per la scheda, il relativo ordine e l&#39;ordinamento delle righe.

   1. (Facoltativo) Fai clic su **[!UICONTROL Filters]** e quindi modificare i filtri da applicare.

      L’applicazione dei filtri restituisce le righe solo quando il valore di una metrica soddisfa i criteri specificati, indipendentemente dal fatto che la metrica venga inclusa o meno come colonna nel rapporto.

      >[!NOTE]
      >
      >È possibile applicare ai filtri le modifiche alle impostazioni di visualizzazione predefinite, ma non salvarle.

   1. (Facoltativo) Fai clic su **[!UICONTROL Date]** e modificare le impostazioni di data predefinite.

   1. (Facoltativo) Fai clic su **[!UICONTROL Additional Settings]** e modificare le impostazioni.

1. Applica o salva le impostazioni:

   * Per applicare temporaneamente le impostazioni senza salvarle nella visualizzazione, fare clic su **[!UICONTROL Apply]**.

      Le impostazioni vengono applicate alla scheda fino a quando non ci si allontana dalla vista di gestione di livello superiore o (se applicabile) [visualizza dati per un altro inserzionista](/help/search-social-commerce/common-tasks/change-advertiser.md).

   * (Per le viste predefinite e personalizzate create) Per salvare le impostazioni nella vista corrente, fare clic su **[!UICONTROL Save]**.

   * Per salvare le impostazioni in una nuova visualizzazione personalizzata, fare clic su **[!UICONTROL Save As]**. In [!UICONTROL Enter New Custom View Name] , immettere il nome della nuova visualizzazione e quindi fare clic su **[!UICONTROL Save]**.

## Ripristinare le impostazioni predefinite di sistema di una vista predefinita

Il ripristino delle impostazioni di visualizzazione predefinite comporta la rimozione di tutte le impostazioni salvate e la riapplicazione delle impostazioni predefinite di sistema.

Le impostazioni predefinite del sistema variano in base alla scheda. Per la maggior parte delle schede, la vista predefinita del sistema mostra i dati relativi al giorno precedente per gli elementi nei conti attivati e attivi (ad esempio, solo i gruppi di annunci attivi nelle campagne attive), con i dati ordinati in base al costo e con i dati di conversione basati sulla data della transazione.

1. Nel pannello a sinistra, fai clic su ![Visualizzazioni personalizzate](/help/search-social-commerce/assets/custom-views-left-rail_icon.png "Visualizzazioni personalizzate") per espandere [!UICONTROL Custom Views] menu.

   Le visualizzazioni sono ordinate in base all’entità applicabile.

1. Accanto al nome della visualizzazione, fare clic su ![Ripristina le impostazioni predefinite](/help/search-social-commerce/assets/revert.png "Ripristina le impostazioni predefinite").

## Eliminare una visualizzazione personalizzata

È possibile eliminare qualsiasi visualizzazione personalizzata creata.

Se si elimina una visualizzazione personalizzata applicata alla scheda corrente, la scheda continua a mostrare la visualizzazione personalizzata fino a quando non si esce dal set di visualizzazioni, ad esempio dalle visualizzazioni all&#39;interno del [!UICONTROL Search] menu per [!UICONTROL Reports] (quando applicabile) quando [visualizza dati per un altro inserzionista](/help/search-social-commerce/common-tasks/change-advertiser.md).

1. Nel pannello a sinistra, fai clic su ![Visualizzazioni personalizzate](/help/search-social-commerce/assets/custom-views-left-rail_icon.png "Visualizzazioni personalizzate") per espandere [!UICONTROL Custom Views] menu.

1. Tenere premuto il cursore sul nome della visualizzazione personalizzata e quindi fare clic su ![Elimina](/help/search-social-commerce/assets/delete.png "Elimina").

1. Nel messaggio di conferma, fai clic su **[!UICONTROL Continue]**.

## Impostazioni di visualizzazione predefinite e personalizzate {#view-settings}

| **Linguetta** | **Campo** | **Descrizione** |
| --- | --- | --- |
| [Sopra tutte le schede] | Nome | Nome univoco per la visualizzazione. Non è possibile modificare il nome di una visualizzazione predefinita. <p><b>Suggerimento</b> Utilizza un nome che ti aiuti a identificare la scheda e le informazioni a cui si applica (ad esempio &quot;Campagne in pausa&quot; o &quot;Primi 50 annunci&quot;). |
|  | Visualizzazione universale | Rende le impostazioni dei dati disponibili in tutte le visualizzazioni di entità (per Campagne, Annunci e così via). Le viste universali possono includere colonne di classificazione di metriche ed etichette, ma non colonne di proprietà (come il nome e lo stato dell’entità) in quanto differiscono per il tipo di entità, nonché tutti gli altri attributi della vista. Tutti i criteri di filtro vengono applicati alla vista entità quando applicabile e vengono ignorati in caso contrario. Tutti i filtri delle metriche vengono valutati localmente (ad esempio, per i clic \> 1000, la vista Campagne mostra le campagne con più di 1000 clic e la vista Gruppi di annunci mostra i gruppi di annunci con più di 1000 clic).<p>Le colonne di proprietà per una vista universale vengono estratte dalla vista predefinita dell’entità. È possibile modificare le colonne delle proprietà predefinite per un&#39;entità specifica nelle impostazioni di visualizzazione predefinite.<p>Dopo aver attivato o disattivato questa opzione, non è possibile salvare la modifica nella vista esistente, ma è possibile crearne una nuova con la modifica. |
|  | Condividi | (Solo visualizzazioni personalizzate; facoltativo) Rende la visualizzazione disponibile a tutti gli altri utenti che possono visualizzare i dati dell&#39;inserzionista. Gli altri utenti non possono modificare o eliminare la visualizzazione, ma possono crearne una nuova dalle impostazioni.Negli elenchi delle visualizzazioni, ogni visualizzazione condivisa da un altro utente è in corsivo, ad esempio &quot;_Campagne dalle prestazioni migliori_.&quot; |
| Colonne | Colonne selezionate e ordinamento | Colonne di dati visualizzate e relativo ordine:<ul><li> (Per aggiungere una colonna) Nell&#39;elenco Colonne disponibili fare clic sul nome di una colonna, quindi trascinarlo nell&#39;elenco Colonne selezionate e ordinamento o fare clic su ![freccia destra](/help/search-social-commerce/assets/chevron-right.png) per spostarlo lì.</li><li>(Per modificare la posizione orizzontale di una colonna) Nell&#39;elenco Colonne selezionate e ordinamento fare clic sul nome della colonna, quindi trascinarlo nella posizione desiderata o fare clic su ![freccia su](/help/search-social-commerce/assets/chevron-up.png) o ![freccia giù](/help/search-social-commerce/assets/chevron-down.png) per spostarlo lì. Il nome della colonna superiore verrà visualizzato nella colonna sinistra.</li><li>(Per rimuovere una colonna) Nell&#39;elenco Colonne selezionate e ordinamento fare clic sul nome di una colonna, quindi trascinarlo nell&#39;elenco Colonne disponibili oppure fare clic su ![freccia sinistra](/help/search-social-commerce/assets/chevron-left.png) per spostarlo lì.</li></ul><b>Filtrare i dati</b><p>Per elencare solo un tipo specifico di dati, fai clic su una delle icone accanto all’elenco:<ul><li>![icona proprietà](/help/search-social-commerce/assets/properties-icon.png) per nomi di proprietà e ID per componenti di ricerca, come Stato</li><li>![icona traffico](/help/search-social-commerce/assets/traffic-metrics-icon.png) per le metriche di traffico standard, come impression e clic</li><li>![icona ricavi](/help/search-social-commerce/assets/revenue-metrics-icon.png) (per le metriche di ricavo/proprietà di transazione tracciate per l’inserzionista, comprese le metriche di conversione e di coinvolgimento del sito sincronizzate da Analytics)</li><li>![icona personalizzata](/help/search-social-commerce/assets/custom-metrics-icon.png) (per metriche derivate personalizzate create dall’inserzionista)</li><li>![icona di classificazione](/help/search-social-commerce/assets/classifications-icon.png) (per le classificazioni delle etichette).</li></ul> <b>Note aggiuntive:</b><ul><li>Per aggiungere, creare o modificare nuove metriche, vedi &quot;Creare una metrica personalizzata&quot;, &quot;Modificare una metrica personalizzata&quot; ed &quot;Eliminare una metrica personalizzata&quot;.</li><li>Se il rapporto include dati per conti con valute diverse, i totali non vengono inclusi per le colonne basate su valuta (come Costo e CPC).</li><li>È possibile [modifica temporaneamente la serie di colonne dal menu dell’intestazione di colonna](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-set-edit-column-heading.md), e [modifica e ordina il set di colonne da [!UICONTROL Columns] icona](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-set-edit-sort-icon.md). (![Icona Colonne](/help/search-social-commerce/assets/custom-columns.png "Icona Colonne")).</li></ul> |
|  | Ordina per | Colonna in base alla quale ordinare i dati. Il valore predefinito è diverso per ogni tipo di rapporto. |
|  | Ordinamento | Specifica se ordinare i dati in **Crescente** o **Decrescente** ordine. Spostare il dispositivo di scorrimento per selezionare un&#39;opzione. |
| Filtri | [Definizioni dei filtri] | Filtri da applicare ai dati (facoltativo). L’applicazione dei filtri restituisce le righe solo quando il valore di una colonna soddisfa i criteri specificati.<p>Per ciascun filtro da applicare:<ol><li>Nel menu Aggiungi filtro, seleziona un nome di colonna. L’elenco include tutte le colonne disponibili ed è ordinato per tipo di colonna, con le colonne di proprietà in primo luogo.</li><li>Definisci il filtro per la colonna</li></ol>(Filtri con campi di input) Seleziona un operatore dal secondo menu, quindi inserisci il valore applicabile. I valori non fanno distinzione tra maiuscole e minuscole. Clic ![icona di spunta](/help/search-social-commerce/assets/select.png) quando hai finito.<p>Ad esempio, se hai selezionato la colonna &quot;Clic&quot; e desideri restituire solo le righe con più di 100 clic, seleziona _\>_ e immetti `100` nel campo di input.<p>A seconda del tipo di dati, gli operatori disponibili possono includere <i>maggiore di</i>, <i>minore di</i>, <i>è uguale a</i>, <i>contiene</i>, <i>non contiene</i>, <i>inizia con</i>, <i>termina con</i>,<i>nessun valore</i>, o <i>ha valore</i> <i>prima di</i>, <i>dopo</i>,oppure <i>nessuna data</i>.<p>(Filtri senza campi di input) Fai clic su ![freccia giù](/help/search-social-commerce/assets/arrow-down-expand.png) accanto al menu Seleziona voci di elenco, quindi selezionare le caselle di controllo accanto a ciascun valore da includere. Clic ![icona di spunta](/help/search-social-commerce/assets/select.png) quando hai finito.<p><b>Note:</b><ul><li>È possibile applicare ai filtri le modifiche alle impostazioni di visualizzazione predefinite, ma non salvarle.</li><li>È inoltre possibile: [modificare temporaneamente i filtri applicabili](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-toolbar.md) all&#39;interno della vista.</li></ul> |
|  | Includi solo righe con dati sulle prestazioni | (Solo visualizzazioni Gruppi di annunci, Parole chiave, Gruppi di prodotti, Posizionamenti e Destinazioni automatiche) <p>Include solo le righe con dati sulle prestazioni nelle date specificate. Per impostazione predefinita, questa opzione è selezionata per ridurre il tempo di caricamento della pagina. <p><b>Avvertenza</b>: se deselezioni l’opzione e la vista include molte entità senza dati sulle prestazioni, la visualizzazione dei dati richiederà più tempo.<p> <b>Nota</b>: puoi applicare ai filtri le impostazioni di visualizzazione predefinite, ma non salvarle. Le viste predefinite mostrano sempre solo le entità con dati sulle prestazioni. |
| Data | Intervallo date | (Quando &quot;Includi intervallo date&quot; è selezionato)<p>L’intervallo di date per il quale generare i dati. Scegliere un&#39;opzione:<ul><li><i>[Intervallo predefinito]</i>: elenco di incrementi di tempo comuni, da <i>Oggi</i> a <i>Ultimi 180 giorni</i>. Sceglietene uno dall&#39;elenco; il valore predefinito è <i>Ieri</i>. Nota: <i>Mese scorso</i>, <i>Ultimi 3 mesi</i>, e <i>Ultimi 6 mesi</i> mostra i dati per i mesi di calendario precedenti.</li><li><i>Intervallo date personalizzato:</i> Specifica la data di inizio e di fine. Immettere le date nel formato MM/GG/AAAA o M/G/AAAA oppure fare clic su ![icona calendario](/help/search-social-commerce/assets/calendar.png) accanto a un campo e seleziona una data.</li></ul> |
|  | Confronto | Confronta i dati per l’intervallo di date specificato con i dati per un secondo intervallo di date. Quando selezioni questa opzione, verranno aggiunte due colonne aggiuntive per ogni colonna di dati regolare. Ad esempio, invece di includere una sola colonna per &quot;Impression&quot;, il rapporto includerà le colonne per &quot;Intervallo di impression 1&quot;, &quot;Intervallo di impression 2&quot; e &quot;Differenza di impression&quot;.<p><b>Note:</b><ul><li>La colonna delle differenze non viene visualizzata per le metriche derivate.</li><li>La generazione di rapporti che confrontano intervalli di date di grandi dimensioni potrebbe richiedere più tempo.</li></ul> |
|  | Formato di confronto | Come esprimere la differenza tra i dati nei due intervalli di date selezionati nel &quot;[_Campo dati_] Differenza&quot;. Scegliere un&#39;opzione:<ul><li><i>Varianza</i> (impostazione predefinita): mostra la differenza come valore numerico.</li><li><i>% modifica</i>: mostra la differenza come percentuale.</li></ul> |
| Impostazioni aggiuntive | Usa predefinito | Applica le impostazioni di attribuzione specificate nelle impostazioni di attribuzione di conversione a livello di inserzionista. |
|  | Regola di attribuzione | (Solo per gli inserzionisti con il servizio di tracciamento delle conversioni basato su pixel di Adobe Advertising) All’interno della scheda, come attribuire i dati di conversione, potenzialmente tra più canali di annunci e portfolio, in una serie di eventi che portano a una conversione. Per impostazione predefinita, viene selezionata la regola specificata nelle impostazioni di attribuzione di conversione a livello di inserzionista.<ul><li> <i>Primo evento</i>: attribuisce la conversione al primo clic a pagamento nella serie nell’intervallo di lookback su clic dell’inserzionista o, se non si è verificato alcun clic a pagamento, all’ultima impression nell’intervallo di lookback su impression dell’inserzionista.</li><li><i>Spessore primo evento Altro</i>: attribuisce la conversione a tutti gli eventi della serie che si sono verificati nell’intervallo di lookback su clic e nell’intervallo di lookback su impression dell’inserzionista, ma attribuisce il maggior peso al primo evento e successivamente meno peso ai seguenti eventi. Quando la conversione è preceduta sia da clic che da impression a pagamento, il peso di override delle impression specificato viene ulteriormente applicato alle impression. Quando la conversione è preceduta solo dalle impression, le impression vengono ponderate in base al peso view-through dell’inserzionista anziché al peso override dell’impression.</li><li><i>Distribuzione uniforme</i>: attribuisce la conversione in modo uniforme a ogni evento della serie che si è verificato nell’intervallo di lookback su clic e nell’intervallo di lookback su impression dell’inserzionista. Quando la conversione è preceduta sia da clic che da impression a pagamento, il peso di override delle impression specificato viene ulteriormente applicato alle impression. Quando la conversione è preceduta solo dalle impression, le impression vengono ponderate in base al peso view-through dell’inserzionista anziché al peso override dell’impression.</li><li><i>Spessore ultimo evento Altro</i>: attribuisce la conversione a tutti gli eventi della serie che si sono verificati nell’intervallo di lookback su clic e nell’intervallo di lookback su impression dell’inserzionista, ma attribuisce il maggior peso all’ultimo evento e successivamente meno peso agli eventi precedenti. Quando la conversione è preceduta sia da clic che da impression a pagamento, il peso di override delle impression specificato viene ulteriormente applicato alle impression. Quando la conversione è preceduta solo dalle impression, le impression vengono ponderate in base al peso view-through dell’inserzionista anziché al peso override dell’impression.</li><li><i>Ultimo evento</i> (impostazione predefinita): attribuisce la conversione all’ultimo clic a pagamento della serie nell’intervallo di lookback su clic dell’inserzionista o, se non si è verificato alcun clic a pagamento, all’ultima impression nell’intervallo di lookback su impression dell’inserzionista.</li><li><i>A forma di U</i>: attribuisce la conversione a tutti gli eventi della serie che si sono verificati nell’intervallo di lookback su clic e nell’intervallo di lookback su impression dell’inserzionista, ma attribuisce il maggior peso al primo evento e agli ultimi eventi, con un peso progressivamente inferiore agli eventi nel mezzo del percorso di conversione. Quando la conversione è preceduta sia da clic che da impression a pagamento, il peso di override delle impression specificato viene ulteriormente applicato alle impression. Quando la conversione è preceduta solo dalle impression, le impression vengono ponderate in base al peso view-through dell’inserzionista anziché al peso override dell’impression.</li></ul><p><b>Note:</b><ul><li>Tutte le regole di attribuzione oltre a Ultimo evento sono disponibili solo per gli inserzionisti con tracciamento dei clic di Adobe Advertising e con tracciamento delle conversioni da Adobe Advertising o Adobe Analytics (con un’integrazione di Analytics).</li><li>Le regole di attribuzione si applicano ai clic sugli annunci a pagamento in qualsiasi canale. Non si applicano alle impression per gli annunci di ricerca a pagamento, che non possono essere tracciati a livello di evento.</li><li>Quando rapporti i dati di conversione utilizzando qualsiasi regola di attribuzione eccetto una delle regole &quot;Last Event&quot; (Ultimo evento), gli eventi che portano alla conversione possono verificarsi in più portfolio. In questo caso, la visualizzazione includerà i dati per la conversione solo quando gli annunci o le parole chiave in tali portfolio sono inclusi nella visualizzazione.</li><li>Per le viste predefinite, consigliamo di mantenere la regola di attribuzione predefinita, che viene utilizzata per calcolare il ricavo ponderato per ogni unità di offerta durante l’ottimizzazione delle offerte.</li></ul> |
|  | Conversioni basate su | Come segnalare i dati di conversione:<ul><li><i>Data transazione</i> (impostazione predefinita): consente di visualizzare le transazioni la cui data di transazione si è verificata nel periodo di tempo specificato. Indica l&#39;importo dei ricavi ottenuti nel periodo di tempo specificato.</li><li><i>Data di clic</i>: per visualizzare le transazioni risultanti da un clic che si è verificato durante il periodo di tempo specificato. Quando un portfolio presenta un ritardo significativo tra clic e transazioni, questa opzione è utile per calcolare il ricavo storico per clic per il portfolio, che indica i comportamenti di ricavo da prevedere nel tempo. |
