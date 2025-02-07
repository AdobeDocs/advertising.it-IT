---
title: Panoramica dell’implementazione di Adobe Advertising Creative
description: Scopri il flusso di lavoro di base per l'implementazione di [!DNL Creative].
feature: Creative Introduction
source-git-commit: fd925c641bef7953aea50813725252c3913757fa
workflow-type: tm+mt
source-wordcount: '863'
ht-degree: 0%

---

# Panoramica dell’implementazione di Adobe Advertising Creative

*Versione beta chiusa*

<!-- CLARIFY HOW "ad" and "creative" are delineated, if they are. If they're not, why do we have different terms scattered around? -->

Il team operativo [!DNL Creative] collabora con ogni inserzionista per configurare i creativi e le esperienze creative, implementando le esperienze pubblicitarie come annunci all&#39;interno del tuo DSP o fornendo al tuo team i tag pubblicitari di terze parti per implementarsi e convalidando i dati di costo, clic e conversione iniziali.

Su base continuativa, il team dell’account Adobe, il team dell’agenzia o l’inserzionista (a seconda dei termini di service level agreement) devono monitorare ogni esperienza e modificarla in base alle esigenze per soddisfare gli obiettivi dell’inserzionista.

## Attività di configurazione iniziali per [!DNL Creative] campagne <!-- Experiences? "Campaigns" may be confusing now. -->

Il team di implementazione e/o l’agenzia collaboreranno con te per eseguire le seguenti operazioni:

1. Definisci gli obiettivi di personalizzazione (ad esempio, se personalizzerai gli annunci per la ricerca di potenziali clienti o il retargeting); tutti i dati di prime, seconde e terze parti disponibili, inclusi risorse creative, segmenti di pubblico e dati CRM <!-- used how/where? -->; e la tua strategia per raggiungere i tuoi obiettivi.

1. (Nuovi account inserzionista) Imposta account amministrativi:

   1. Configura l&#39;account dell&#39;inserzionista per [!DNL Creative]<!-- and/or DSP? --> e crea anche un account in Advertising Search.

      La configurazione dell&#39;account [!DNL Creative] è in Advertising DSP, anche se l&#39;inserzionista non è un cliente DSP.

      Analogamente, anche se l&#39;inserzionista non è un cliente [!DNL Search], l&#39;account [!DNL Search] viene utilizzato per creare tag di tracciamento conversione e impostare colonne di conversione in [!DNL Creative].

   1. (Se necessario) Crea account utente per l’inserzionista per visualizzare e gestire i suoi creativi e le sue esperienze pubblicitarie e per generare rapporti.

1. (Facoltativo) Se desideri creare segmenti di pubblico primario da includere come target per i tuoi creativi, crea i tag in uno dei seguenti modi:

   * [Crea pixel di retargeting](/help/creative/pixels/retargeting-pixel-manage.md) per eseguire il retargeting degli annunci ai visitatori con attributi specifici per pagine di destinazione o pagine di conversione specifiche, quindi genera tag da inserire nelle pagine web pertinenti.

   * (Inserzionisti con DSP) All&#39;interno dell&#39;DSP, [crea segmenti di pubblico personalizzati](/help/dsp/audiences/custom-segment-create.md) per tenere traccia di tutti i visitatori su pagine di destinazione o pagine di conversione specifiche, quindi genera tag da inserire nelle pagine web pertinenti.

   Entrambi i tipi di tag sono tag immagine, che visualizzano un’immagine trasparente (pixel) di 1 pixel x 1 pixel, invisibile agli utenti finali, nella pagina web in cui vengono aggiunti. Successivamente, puoi configurare i creativi in un’esperienza pubblicitaria per eseguire il targeting di pixel o segmenti specifici di retargeting, in modo che gli elementi pubblicitari rilevanti vengano visualizzati solo agli utenti che hanno visitato in precedenza le pagine del sito associate al pixel o al segmento.

   Il reparto IT dell’inserzionista o un altro gruppo potrebbe dover pianificare la distribuzione dei tag o esserne informato.

   **Nota:** puoi anche utilizzare i tuoi tipi di pubblico di prime parti da Adobe Audience Manager e Adobe Analytics come target creativi. Quando un visitatore diventa idoneo per un pubblico condiviso da [!DNL Analytics], le informazioni sono utilizzabili in [!DNL Creative] in circa 24-48 ore. <!--Still true? And what about AAM and DSP? -->

1. Imposta le esperienze pubblicitarie in base ai tuoi obiettivi pubblicitari:

   * **Flusso di lavoro di automazione:** il team delle operazioni di [!DNL Creative] può creare annunci dinamici per la tua organizzazione utilizzando modelli di annunci e feed di dati.

     Per ulteriori informazioni, rivolgiti al team del tuo account Adobe.

     <!-- LATER, in a later phase: (Advertisers with Adobe Experience Manager; optional) Configure access to image assets in the Experience Manager account. -->

   * **Flusso di lavoro manuale:** Imposta manualmente le esperienze annuncio:

      1. Configura i creativi da utilizzare nelle esperienze:

         * Per i creativi che [!DNL Creative] ospiteranno, caricali.<!-- Add x-ref and reword if necessary to cover all cases -->

         * Per i creativi in hosting su un server di annunci di terze parti supportato, [selezionare i file creativi](/help/creative/creative-libraries/creative-third-party-manage.md).

      1. (Facoltativo) [Raggruppa i creativi in bundle](/help/creative/creative-libraries/bundle-manage.md) da allegare alle esperienze in un solo passaggio.

      1. Sequenza di creative e destinazioni di annunci facoltativi come [esperienze di annunci](/help/creative/experiences/experience-about.md).<!-- maybe change x-ref once that chapter is done -->

     Le destinazioni degli annunci possono includere pixel di retargeting creati in [!DNL Creative], segmenti di pubblico in Adobe Experience Cloud (inclusi DSP, Audience Manager o [!DNL Analytics]), target geografici o trigger di dati specifici sulla pagina web (ad esempio SKU=01234567890123 o Cart=empty).&lt;!— Non vedo i segmenti di pubblico disponibili, e vedo target di raggio (che non funziona) ma non altri target geografici — verificate tutti questi. —>

1. Configura il tracciamento delle conversioni per le esperienze pubblicitarie:


Imposta il tracciamento delle conversioni. A seconda dell’implementazione, potrebbe essere necessario aggiungere
i tag di tracciamento delle conversioni nelle pagine web dell’inserzionista e/o l’impostazione di una
perdita di feed per i dati di conversione raccolti separatamente dall’inserzionista.


Puoi generare tag di tracciamento delle conversioni di Advertising Cloud in Advertising Cloud
Effettua ricerche in Adobe Dynamic Tag Manager (precedentemente denominato Dynamic Tag Manager).
Nota: è necessario utilizzare i tag di conversione di JavaScript, non i tag immagine.


Il reparto IT dell&#39;inserzionista o un altro gruppo potrebbe dover pianificare o essere informato
informazioni su, la distribuzione di tag.


(Facoltativo) All’interno di Advertising Cloud Search, effettua ogni conversione (proprietà transazione)
disponibile come singolo set di colonne nelle visualizzazioni dati e nei rapporti.


Una conversione (proprietà transazione) viene elencata in Advertising Cloud Search dopo at
è stato tracciato almeno un evento di conversione.


Se non rendi disponibili metriche specifiche, tutte le conversioni vengono consolidate
in una colonna &quot;Conversioni&quot;.


Convalida i dati tracciati.


(Facoltativo) Configura la consegna di rapporti pianificati a indirizzi e-mail specifici.


Per istruzioni, consulta il capitolo della guida su &quot;Rapporti&quot;.


Configurare campagne pubblicitarie su Advertising Cloud DSP o un altro DSP e fornire JavaScript
o i tag iframe per le esperienze pubblicitarie all’inserzionista, che può implementarli come
annunci di terze parti nel DSP.


Monitora le prestazioni delle esperienze annuncio completate visualizzando i predefiniti
dettagli sulle prestazioni per singole esperienze o creazione di rapporti sulle prestazioni personalizzati.


(Se necessario) Aggiorna le esperienze pubblicitarie in base alle prestazioni e alla messaggistica aggiornata.






>[!MORELIKETHIS]
>
>* [Informazioni sull&#39;Adobe Advertising Creative](/help/creative/introduction/creative-about.md)
>* [Organizzazione dell&#39;interfaccia utente](/help/creative/introduction/ui.md)
