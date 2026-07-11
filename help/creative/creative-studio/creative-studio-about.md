---
title: Informazioni su Creative Studio in Advertising Creative
description: Scopri come utilizzare Creative Studio per creare contenuti pubblicitari basati sull’intelligenza artificiale in Adobe Advertising Creative.
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: d0d9f2ed-c163-44e1-97a1-4ace121416b8
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 24e27656edda50f29292cb75823ef6cacdb685fe
workflow-type: tm+mt
source-wordcount: 811
ht-degree: 0%

---

# Informazioni su [!UICONTROL Creative Studio] in [!DNL Advertising Creative]

*funzionalità Beta*

[!UICONTROL Creative Studio] è un ambiente basato sull&#39;intelligenza artificiale in cui è possibile creare, ridimensionare e perfezionare annunci display in più formati in una singola sessione. Interagisci con l’intelligenza artificiale tramite un’interfaccia chat in linguaggio naturale per generare e modificare i contenuti dell’annuncio: per i campi di contenuto non è richiesto alcun lavoro di progettazione manuale.

## Panoramica di Workspace

[!UICONTROL Creative Studio] è organizzato in tre schede:

**[!UICONTROL Creatives]**: punto di partenza per la creazione di annunci. Mostra i creativi esistenti generati da Creative Studio, organizzati in librerie creative comprimibili. Da qui puoi generare annunci display standard da modelli, creare creative display dinamiche da dati di catalogo e gestire creative esistenti (modifica, genera varianti di annunci, anteprima, duplicazione, download, eliminazione, QA e revisione dei registri di modifica). Consulta &quot;[Gestire gli annunci standard in Creative Studio](creative-studio-manage-standard-ads.md)&quot; e &quot;[Gestire gli annunci dinamici in Creative Studio](creative-studio-manage-dynamic-ads.md).&quot;

**[!UICONTROL Templates]** - Mostra tutti i modelli di annunci video e di visualizzazione disponibili per il tuo account, con filtro per origine (Tutti, Modelli di sistema, Modelli utente), stato e formato di annunci. Puoi visualizzare in anteprima, inserire i preferiti, etichettare, scaricare ed eliminare i modelli, oppure avviare una sessione di generazione di annunci direttamente da un modello di annunci display esistente. Consulta &quot;[Gestire i modelli in Creative Studio](creative-studio-manage-templates.md).&quot;

**[!UICONTROL Assets]** - Memorizza immagini, video e file audio utilizzati nei modelli e disponibili per l&#39;associazione ai messaggi di chat durante le sessioni di generazione di annunci. Puoi cercare, filtrare, caricare, scaricare ed eliminare le risorse. Vedi [Gestione delle risorse in Creative Studio](creative-studio-manage-assets.md).

## Funzionalità principali

* **Generazione di contenuti AI:** Utilizza **[!UICONTROL Ad Variations Generator]** per generare concetti e varianti di annunci tramite un&#39;interfaccia chat in linguaggio naturale. L’assistente AI può generare titoli, sottotitoli, CTA, copia del corpo e varianti di immagine di sfondo e può creare nuovi modelli di dimensioni nella stessa sessione. Possono essere attivi fino a 10 concetti per sessione.

* **Supporto di annunci video e di visualizzazione:** Crea e gestisci sia modelli di annunci video che modelli di annunci video. Quando crei un modello, scegli **[!UICONTROL Display Ad Template]** o **[!UICONTROL Video Ad Template]** per farlo corrispondere al formato della campagna.

* **Caricamento modello HTML5:** Importa modelli di annunci HTML5 esistenti caricandoli come file ZIP. La finestra di dialogo **[!UICONTROL Import Templates]** consente di assegnare un nome di inserzionista e modello prima dell&#39;importazione.

* **Supporto multi-dimensione:** ridimensionare gli annunci alle dimensioni standard IAB in un unico passaggio. L’intelligenza artificiale regola automaticamente il posizionamento e il ridimensionamento del contenuto per ogni formato, mentre i controlli dell’area di lavoro (zoom in/out, adattamento allo schermo, ripetizione delle animazioni) consentono di rivedere ogni dimensione.

* **Uscite allineate al marchio:** Quando viene applicato il tuo [profilo marchio](/help/creative/brands/brand-manage.md), l&#39;intelligenza artificiale utilizza i logo, le palette di colori, le linee guida vocali, gli standard di immagine e le linee guida per il canale del tuo marchio per mantenere i contenuti generati sul marchio.

* **Accesso alla libreria risorse:** allega immagini e altre risorse direttamente ai messaggi di chat di IA selezionando dalla libreria risorse, mantenendo il contesto visivo disponibile durante la generazione del contenuto.

* **Integrazione feed:** per le campagne pubblicitarie dinamiche, connetti un catalogo di prodotti o contenuti per generare annunci su larga scala, quindi utilizza l&#39;agente di intelligenza artificiale per filtrare, visualizzare in anteprima e verificare la qualità delle combinazioni pubblicitarie generate dal catalogo.

* **Organizzazione del modello:** Contrassegna i modelli come preferiti, applica etichette e filtra per stato, formato o origine per mantenere organizzata la libreria dei modelli.

## Flussi di lavoro per la creazione di annunci

| Flusso di lavoro | Quando utilizzare |
| --- | --- |
| [Genera annunci standard da un modello](creative-studio-manage-standard-ads.md) | Selezionare un modello di visualizzazione o video e utilizzare [!UICONTROL Ad Variations Generator] per creare varianti di contenuto generato da IA. Consigliato quando un modello esiste già e desideri generare contenuti basati sull’intelligenza artificiale. |
| [Gestisci creatività dinamica](creative-studio-manage-dynamic-ads.md) | Connetti un catalogo di prodotti o contenuti a un modello, mappa i campi del catalogo con gli elementi del modello, quindi utilizza l’agente di intelligenza artificiale per visualizzare in anteprima e verificare tutte le combinazioni di annunci generate. Ideale per campagne su larga scala basate su catalogo. |
| Crea un nuovo modello | Inizia da un’area di lavoro vuota per creare un modello di visualizzazione o video. Consigliato quando nessun modello esistente soddisfa le tue esigenze. |
| Carica modelli HTML5 | Importa uno o più modelli di annunci HTML5 inseriti come file ZIP. Ottimo quando i creativi HTML5 pronti per la produzione sono generati al di fuori di [!DNL Advertising Creative]. |

## Annunci standard e annunci dinamici

[!UICONTROL Creative Studio] supporta due modelli di contenuto di annunci che determinano il comportamento dell&#39;agente di IA:

**Annunci standard**: vengono forniti o generati tutti i contenuti degli annunci. L’agente IA può generare, modificare o sostituire qualsiasi campo di contenuto (titoli, CTA, immagini, colori, copia tonalità) all’interno dei vincoli del layout del modello. Gli annunci standard completati vengono salvati in una libreria creativa selezionando un inserzionista e una libreria, con un’opzione per allegarli ai bundle. Gli annunci standard sono ideali per le campagne di messaggistica personalizzata.

**Annunci dinamici**: il contenuto è gestito da un catalogo di prodotti o contenuti. Un flusso di lavoro guidato in quattro passaggi illustra come selezionare un modello, mappare i campi del catalogo agli elementi del modello e configurare il set di annunci. Dopo la configurazione, l’agente di intelligenza artificiale passa a un ruolo di controllo qualità e anteprima: può filtrare gli annunci in base ai campi del catalogo, segnalare i problemi di qualità (limiti dei caratteri, overflow del contenuto, immagini interrotte, conformità) e analizzare le combinazioni in tutto il catalogo, ma non può modificare direttamente il contenuto originato dal catalogo. Per modificare il contenuto degli annunci dinamici, aggiorna il catalogo sorgente.

>[!MORELIKETHIS]
>
>* [Gestione di annunci standard in Creative Studio](creative-studio-manage-standard-ads.md)
>* [Gestione di creatività dinamiche in Creative Studio](creative-studio-manage-dynamic-ads.md)
>* [Gestione dei modelli in Creative Studio](creative-studio-manage-templates.md)
>* [Gestione risorse in Creative Studio](creative-studio-manage-assets.md)
>* [Gestione dei profili del brand in Advertising Creative](/help/creative/brands/brand-manage.md)
