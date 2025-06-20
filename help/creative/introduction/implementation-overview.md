---
title: Panoramica dell’implementazione di Adobe Advertising Creative
description: Scopri il flusso di lavoro di base per l'implementazione di [!DNL Creative].
feature: Creative Introduction
source-git-commit: fbd85ce99ab177c70b95bae42166265ef9053034
workflow-type: tm+mt
source-wordcount: '998'
ht-degree: 0%

---

# Panoramica dell’implementazione di Adobe Advertising Creative

*Versione beta chiusa*

<!-- CLARIFY HOW "ad" and "creative" are delineated, if they are. If they're not, why do we have different terms scattered around? -->

Il team operativo [!DNL Creative] collabora con ogni inserzionista per configurare i creativi e le esperienze creative, implementando le esperienze pubblicitarie come annunci all&#39;interno del DSP o fornendo al team i tag pubblicitari di terze parti per implementarsi e convalidando i dati di costo, clic e conversione iniziali.

Su base continuativa, l’Account Team di Adobe, il team dell’agenzia o l’inserzionista (a seconda dei termini di service level agreement) devono monitorare ogni esperienza e modificarla in base alle esigenze per soddisfare gli obiettivi dell’inserzionista.

## Attività di configurazione iniziali per [!DNL Creative] esperienze

Il team di implementazione e/o l’agenzia collaboreranno con te per eseguire le seguenti operazioni:

1. Definisci gli obiettivi di personalizzazione (ad esempio, se personalizzare gli annunci per la ricerca di potenziali clienti o il retargeting); tutti i dati di prime, seconde e terze parti disponibili, incluse le risorse creative e i segmenti di pubblico; e la strategia per raggiungere gli obiettivi.<!-- and CRM data? used how/where? -->

1. (Nuovi account inserzionista) Imposta account amministrativi:

   1. Configura l&#39;account dell&#39;inserzionista per [!DNL Creative] e crea un account in Advertising Search, Social e Commerce.

      La configurazione dell&#39;account [!DNL Creative] è in Advertising DSP, anche se l&#39;inserzionista non utilizza il resto di DSP.

      Analogamente, anche se l&#39;inserzionista non è un cliente [!DNL Search, Social, & Commerce], l&#39;account [!DNL Search, Social, & Commerce] viene utilizzato per creare tag di tracciamento conversione e impostare colonne di conversione in [!DNL Creative].

   1. (Se necessario) Crea account utente per l’inserzionista per visualizzare e gestire i suoi creativi e le sue esperienze pubblicitarie e per generare rapporti.

1. (Facoltativo) Se desideri creare segmenti di pubblico primario da includere come target per i tuoi creativi, crea i tag in uno dei seguenti modi:

   * [Crea pixel di retargeting](/help/creative/pixels/retargeting-pixel-manage.md) per eseguire il retargeting degli annunci ai visitatori con attributi specifici per pagine di destinazione o pagine di conversione specifiche, quindi genera tag da inserire nelle pagine web pertinenti.

   * (Inserzionisti con DSP) In DSP, [crea segmenti di pubblico personalizzati](/help/dsp/audiences/custom-segment-create.md) per tenere traccia di tutti i visitatori su pagine di destinazione o pagine di conversione specifiche, quindi genera tag da inserire nelle pagine web pertinenti.

   Entrambi i tipi di tag sono tag immagine, che visualizzano un’immagine trasparente (pixel) di 1 pixel x 1 pixel, invisibile agli utenti finali, nella pagina web in cui vengono aggiunti. Successivamente, puoi configurare i creativi in un’esperienza pubblicitaria per eseguire il targeting di pixel o segmenti specifici di retargeting, in modo che gli elementi pubblicitari rilevanti vengano visualizzati solo agli utenti che hanno visitato in precedenza le pagine del sito associate al pixel o al segmento.

   Il reparto IT dell’inserzionista o un altro gruppo potrebbe dover pianificare la distribuzione dei tag o esserne informato.

   **Nota:** puoi anche utilizzare i tuoi tipi di pubblico di prime parti da Adobe Audience Manager e Adobe Analytics come target creativi. Quando un visitatore diventa idoneo per un pubblico condiviso da [!DNL Analytics], le informazioni sono utilizzabili in [!DNL Creative] in circa 24-48 ore. <!--Are times still true? -->

1. Imposta la gerarchia delle campagne all’interno delle DSP in cui implementerai le esperienze pubblicitarie. Utilizza il targeting compatibile con il targeting nelle esperienze pubblicitarie che implementerai nelle campagne.

   Il comportamento di targeting gerarchico può variare a seconda di DSP. Advertising DSP applica il targeting a livello di annuncio sul targeting a livello di posizionamento (non al suo posto). Ad esempio, se un posizionamento ha come target gli utenti in Australia e un annuncio ha come target gli utenti in Giappone, l’annuncio avrà come target il ramo &quot;Tutti gli altri&quot; per l’esperienza. Assicurati di riflettere sull’intera struttura della campagna.

1. Imposta le esperienze pubblicitarie in base ai tuoi obiettivi pubblicitari:

   * **Flusso di lavoro di automazione:** il team delle operazioni di [!DNL Creative] può creare annunci dinamici per la tua organizzazione utilizzando modelli di annunci e feed di dati.

     Per ulteriori informazioni, contatta il team del tuo account Adobe.

     <!-- LATER, in a later phase: (Advertisers with Adobe Experience Manager; optional) Configure access to image assets in the Experience Manager account. --><!-- I think this will be automatic based on their IMS organization. But I'm not sure if they need to be logged in via SSO using their Adobe login or if it will also work using their legacy DSP login. -->

   * **Flusso di lavoro manuale:** Imposta manualmente le esperienze annuncio:

      1. [Configura le creatività standard da utilizzare nelle esperienze](/help/creative/creative-libraries/creative-add-standard.md):

         * Per i creativi che [!DNL Creative] ospiteranno, caricali. Può includere risorse di immagini in un account Adobe Experience Manager.

         * Per i creativi in hosting su un server di annunci di terze parti supportato, seleziona i file creativi.

      1. (Facoltativo) [Raggruppa i creativi in bundle](/help/creative/creative-libraries/bundle-manage.md) da allegare alle esperienze mirate in un solo passaggio.

      1. Configura [esperienze annuncio](/help/creative/experiences/experience-about.md):

         * Per [esperienze pubblicitarie mirate](/help/creative/experiences/experience-create-targeting.md), sequenze creative e destinazioni pubblicitarie facoltative.

           Le destinazioni degli annunci possono includere pixel di retargeting creati in [!DNL Creative], segmenti di pubblico in Adobe Experience Cloud (incluso in DSP, Audience Manager o [!DNL Analytics]), destinazioni geografiche o trigger di dati specifici sulla pagina web (ad esempio SKU=01234567890123 o Cart=empty).

         * Per [esperienze pubblicitarie non mirate](/help/creative/experiences/experience-create-no-targeting.md), crea impostazioni generali di esperienza.

           Le destinazioni degli annunci possono includere pixel di retargeting creati in [!DNL Creative], segmenti di pubblico in Adobe Experience Cloud (incluso in DSP, Audience Manager o [!DNL Analytics]), destinazioni geografiche o trigger di dati specifici sulla pagina web (ad esempio SKU=01234567890123 o Cart=empty).













1. Configura il tracciamento delle conversioni per le esperienze pubblicitarie:


Imposta il tracciamento delle conversioni. A seconda dell’implementazione, potrebbe essere necessario aggiungere
i tag di tracciamento delle conversioni nelle pagine web dell’inserzionista e/o l’impostazione di una
perdita di feed per i dati di conversione raccolti separatamente dall’inserzionista.


Puoi generare i tag di tracciamento delle conversioni di Adobe Advertising in Advertising Search, Social e Commerce o in Adobe Dynamic Tag Manager (precedentemente denominato Dynamic Tag Manager).
Nota: è necessario utilizzare i tag di conversione di JavaScript, non i tag immagine.


Il reparto IT dell&#39;inserzionista o un altro gruppo potrebbe dover pianificare o essere informato
informazioni su, la distribuzione di tag.


(Facoltativo) In Ricerca, Social e Commerce, esegui ogni conversione (proprietà transazione)
disponibile come singolo set di colonne nelle visualizzazioni dati e nei rapporti.


Una conversione (proprietà transazione) è elencata in Search, Social e Commerce dopo at
è stato tracciato almeno un evento di conversione.


Se non rendi disponibili metriche specifiche, tutte le conversioni vengono consolidate
in una colonna &quot;Conversioni&quot;.


Convalida i dati tracciati.


(Facoltativo) Configura la consegna di rapporti pianificati a indirizzi e-mail specifici.


Per istruzioni, consulta il capitolo della guida su &quot;Rapporti&quot;.


Imposta le campagne pubblicitarie su Advertising DSP o un altro DSP e fornisci JavaScript
o i tag iframe per le esperienze pubblicitarie all’inserzionista, che può implementarli come
annunci di terze parti in DSP.


Monitora le prestazioni delle esperienze annuncio completate visualizzando i predefiniti
dettagli sulle prestazioni per singole esperienze o creazione di rapporti sulle prestazioni personalizzati.


(Se necessario) Aggiorna le esperienze pubblicitarie in base alle prestazioni e alla messaggistica aggiornata.






>[!MORELIKETHIS]
>
>* [Informazioni su Adobe Advertising Creative](/help/creative/introduction/creative-about.md)
>* [Organizzazione dell&#39;interfaccia utente](/help/creative/introduction/ui.md)
