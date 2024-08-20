---
title: Informazioni sui report personalizzati
description: Scopri le opzioni per la creazione manuale di rapporti personalizzati o l’utilizzo di modelli di rapporto preconfigurati.
feature: DSP Custom Reports
exl-id: 321062f3-754b-4379-9587-003862c4221b
source-git-commit: 81c9590d134214e1ed860c2f8116ff66882000be
workflow-type: tm+mt
source-wordcount: '792'
ht-degree: 0%

---

# Informazioni sui report personalizzati

I rapporti personalizzati ti consentono di personalizzare il contenuto e la consegna dei dati del rapporto utilizzando le dimensioni della campagna (ad esempio inserzionista, posizionamento, siti o geos) e le metriche più importanti per te. Puoi effettuare le seguenti operazioni:

* Configurare completamente i rapporti sulle prestazioni delle campagne a livello granulare.
* Scegli uno dei modelli di rapporto preconfigurati e, facoltativamente, personalizzali ulteriormente.

Puoi generare i rapporti una volta o pianificarli in modo che vengano generati ogni giorno, ogni settimana o ogni mese alle 03:00 nel fuso orario specificato. Una volta generato, il report viene consegnato a ogni destinatario e-mail specificato o a [destinazioni report](/help/dsp/reports/report-destinations/report-destination-about.md) collegate dei seguenti tipi:

* [!DNL Amazon Simple Storage Service] ([!DNL S3])
* FTP
* SFTP
* FTP SSL (in versione beta)

>[!NOTE]
>
>È inoltre possibile visualizzare i dati on-demand a tutti i livelli di una campagna (campagna, pacchetto, posizionamento o annuncio) [nella visualizzazione gestione campagne pertinente](/help/dsp/campaign-management/reports/campaign-reports-about.md).

## Tipi di rapporti disponibili

* **[!UICONTROL Custom]:** Questo report è un modello vuoto che è possibile utilizzare per creare un report personalizzato utilizzando la maggior parte delle dimensioni e delle metriche. I report [!UICONTROL Conversion], [!UICONTROL Device], [!UICONTROL Geo] e [!UICONTROL Site] sono varianti di questo modello con colonne e dimensioni preselezionate per i rispettivi casi d&#39;uso.

* Modelli di rapporto preconfigurati

   * **[!UICONTROL Billing]:** Utilizzare questo report per comprendere le metriche di fatturazione chiave, ad esempio le metriche di spesa per la fatturazione dei contenuti multimediali per campagna. I dati non sono disponibili per i posizionamenti mirati agli ID universali.

     >[!NOTE]
     >
     >Questo rapporto include dati sul segmento di fatturazione. Se a un utente o a un dispositivo viene trasmessa un’impression che appartiene a più segmenti, a un solo segmento fatturabile viene attribuita l’impression.

   * **[!UICONTROL Conversion]:** Utilizza questo rapporto per comprendere le prestazioni delle campagne in base alle metriche di conversione acquisite utilizzando il tracciamento delle conversioni di Adobe Advertising. Questo rapporto include l’attribuzione multi-touch.

   * **[!UICONTROL Device]:** Utilizzare questo modello precompilato per visualizzare le metriche chiave per le dimensioni relative al dispositivo.

   * **[!UICONTROL Frequency (by Impression)]:** Utilizzare questo report per comprendere la distribuzione delle impression mostrate a visualizzatori univoci (ad esempio, quanti visualizzatori univoci hanno visto una impression, due impression, tre impression e così via). I dati sono disponibili per posizionamento o campagna.

     >[!NOTE]
     >
     >* I dati sono disponibili dopo il 1° marzo 2019.
     >* La frequenza è stimata sulla base di un campionamento di dati.
     >* Per alcuni inventari, gli editori non trasmettono un identificatore di dispositivo, impedendo così il tracciamento della frequenza. Questo rapporto include solo le impression per le quali era disponibile un identificatore di dispositivo.

   * **[!UICONTROL Frequency (by App/Site)]:** Utilizzare questo report per capire quanti utenti univoci sono stati raggiunti dall&#39;app o dal sito. Puoi anche vedere quanti utenti univoci sono stati raggiunti solo tramite un’app o un sito particolare (&quot;utenti univoci distinti&quot;).

     >[!NOTE]
     >
     >* I dati sono disponibili dopo il 15 novembre 2018.
     >* Per alcuni inventari privati, gli editori non trasmettono un identificatore di dispositivo, impedendo così il tracciamento della frequenza.

   * **[!UICONTROL Geo]**: utilizzare questo modello precompilato per visualizzare le metriche chiave per dimensioni geografiche.

   * **[!UICONTROL Margin]:** Utilizzare questo report per visualizzare metriche chiave come margine, profitto e altre metriche di spesa per campagna o posizionamento. I dati non sono disponibili per i posizionamenti mirati agli ID universali.

   * **[!UICONTROL Segment]:** Utilizzare questo modello precompilato per visualizzare le metriche chiave per segmento.

     >[!NOTE]
     >
     >* Questo rapporto ha lo scopo di mostrare le prestazioni di diversi segmenti target. Utilizza i dati di appartenenza ai segmenti. Quando un’impression viene trasmessa a una persona o a un dispositivo appartenente a due o più segmenti target, questo rapporto include una riga per ciascun segmento. Per questo motivo, i totali in questo rapporto potrebbero non corrispondere alla consegna effettiva.
     >* Le metriche di conversione e i dati di obiettivo personalizzati per i segmenti sono disponibili dopo il 2 agosto 2019. Tutti gli altri dati per i segmenti sono disponibili a partire dal 1° giugno 2018.

   * **[!UICONTROL Site]:** Per impostazione predefinita, include le metriche standard, la spesa netta totale dei supporti e la spesa netta totale fatturabile per sito.

   * **[!UICONTROL Household Reach & Frequency]:** Utilizzare questo report per visualizzare impression, portata e frequenza per una singola dimensione in più formati di annunci a livello di famiglia in base all&#39;indirizzo IP, anziché a livello di dispositivo/cookie. Utilizza le informazioni per ottimizzare il mix di contenuti multimediali, migliorare le prestazioni e identificare opportunità di portata incrementale. Per ulteriori informazioni, consulta &quot;[Domande frequenti sui rapporti sulla famiglia](/help/dsp/reports/faq-household-report.md)&quot;. I dati non sono disponibili per i posizionamenti mirati agli ID universali.

   * **[!UICONTROL Household Conversions]:** Utilizzare questo report per visualizzare le conversioni view-through a livello di famiglia in base all&#39;indirizzo IP anziché a livello di dispositivo/cookie. Utilizza le informazioni per misurare e ottimizzare le prestazioni della campagna. Per ulteriori informazioni, consulta &quot;[Domande frequenti sui rapporti sulla famiglia](/help/dsp/reports/faq-household-report.md)&quot;. I dati non sono disponibili per i posizionamenti mirati agli ID universali.

## Reporting tra account {#cross-account-reporting}

Qualsiasi organizzazione con più account DSP può facoltativamente abilitare i dati tra account diversi nei rapporti personalizzati, in base alle esigenze dell’organizzazione. Ad esempio, puoi concedere all’account A l’accesso ai dati dell’account B e all’account B l’accesso ai dati dell’account C (ma non dell’account A). Per abilitare e configurare questa funzione, contatta il team del tuo account di Adobe.

Una volta abilitata la funzionalità per la tua organizzazione, puoi [filtrare](report-settings.md) uno qualsiasi dei seguenti tipi di report per account: [!UICONTROL Custom], [!UICONTROL Site], [!UICONTROL Segment], [!UICONTROL Geo], [!UICONTROL Device], [!UICONTROL Frequency (by Impression)] e [!UICONTROL Conversion].

Le impostazioni dell&#39;account in [!UICONTROL Settings] > [!UICONTROL Account] indicano a) gli altri account i cui dati sono disponibili per il tuo account e b) gli altri account che possono accedere ai dati del tuo account.

>[!MORELIKETHIS]
>
>* [Crea un report personalizzato](/help/dsp/reports/report-create.md)
>* [Impostazioni report personalizzati](/help/dsp/reports/report-settings.md)
>* [Domande frequenti sui report domestici](/help/dsp/reports/faq-household-report.md)
>* [Tipi di report sulle prestazioni nelle visualizzazioni di Campaign Management](/help/dsp/campaign-management/reports/campaign-reports-about.md)
>* [Colonne report disponibili](/help/dsp/reports/report-columns.md)
>* [Informazioni su [!UICONTROL Report Destinations]](/help/dsp/reports/report-destinations/report-destination-about.md)
