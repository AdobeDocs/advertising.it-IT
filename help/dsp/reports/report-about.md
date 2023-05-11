---
title: Informazioni sui report personalizzati
description: Scopri le opzioni per la creazione manuale di rapporti personalizzati o l’utilizzo di modelli di rapporti preconfigurati.
feature: DSP Custom Reports
exl-id: 321062f3-754b-4379-9587-003862c4221b
source-git-commit: 858b00ec28158ada1edfc70a2efc3540fa46a376
workflow-type: tm+mt
source-wordcount: '711'
ht-degree: 0%

---

# Informazioni sui report personalizzati

I rapporti personalizzati ti consentono di personalizzare il contenuto e la consegna dei dati del rapporto utilizzando le dimensioni della campagna (ad esempio l’inserzionista, il posizionamento, i siti o le aree geografiche) e le metriche più importanti per te. Puoi effettuare le seguenti operazioni:

* Configura completamente i rapporti sulle prestazioni della campagna a livello granulare.
* Scegli tra modelli di report preconfigurati e, facoltativamente, personalizzali ulteriormente.

Puoi generare rapporti una volta oppure pianificarli per la generazione giornaliera, settimanale o mensile alle 03:00 nel fuso orario specificato. Una volta generato, il rapporto viene consegnato a ogni destinatario e-mail specifico o collegato [destinazioni dei rapporti](/help/dsp/reports/report-destinations/report-destination-about.md) dei seguenti tipi:

* [!DNL Amazon Simple Storage Service] ([!DNL S3])
* FTP
* SFTP
* SSL FTP (in versione beta)

>[!NOTE]
>
>Puoi anche visualizzare i dati on-demand a tutti i livelli di una campagna (campagna, pacchetto, posizionamento o annuncio) [nella vista relativa alla gestione della campagna](/help/dsp/campaign-management/reports/campaign-reports-about.md).

## Tipi di rapporti disponibili

* **[!UICONTROL Custom]:** Questo rapporto è un modello vuoto che puoi utilizzare per creare un rapporto personalizzato utilizzando la maggior parte delle dimensioni e metriche. [!UICONTROL Conversion], [!UICONTROL Device], [!UICONTROL Geo]e [!UICONTROL Site] i rapporti sono varianti di questo modello con colonne e dimensioni preselezionate per i rispettivi casi d’uso.

* Modelli di rapporto preconfigurati

   * **[!UICONTROL Billing]:** Utilizza questo rapporto per comprendere le metriche di fatturazione chiave, come le metriche di spesa per la fatturazione dei contenuti multimediali per campagna.

      >[!NOTE]
      >
      >Questo rapporto include dati sul segmento di fatturazione. Se a un utente o a un dispositivo viene distribuita un’impression che appartiene a più segmenti, l’impression viene accreditata solo a un segmento fatturabile.

   * **[!UICONTROL Conversion]:** Usa questo rapporto per capire le prestazioni delle campagne in base alle metriche di conversione acquisite utilizzando il tracciamento delle conversioni di Adobe Advertising. Questo rapporto include l’attribuzione multi-touch.

   * **[!UICONTROL Device]:** Utilizza questo modello precompilato per visualizzare le metriche chiave per dimensioni relative al dispositivo.

   * **[!UICONTROL Frequency (by Impression)]:** Utilizza questo rapporto per comprendere la distribuzione delle impression mostrate a visualizzatori unici (ad esempio, quanti visualizzatori unici hanno visto un’impression, due impression, tre impression e così via). I dati sono disponibili per posizionamento o campagna.

      >[!NOTE]
      >
      >* I dati sono disponibili dopo il 1° marzo 2019.
      >* La frequenza è stimata sulla base di un campionamento dei dati.
      >* Per alcune scorte, gli editori non trasmettono un identificatore del dispositivo, il che impedisce il tracciamento delle frequenze. Questo rapporto include solo le impression per le quali era disponibile un identificatore dispositivo.


   * **[!UICONTROL Frequency (by App/Site)]:** Usa questo rapporto per capire quanti utenti univoci sono stati raggiunti dall’app o dal sito. Puoi anche vedere quanti utenti univoci sono stati raggiunti solo tramite una particolare app o sito (&quot;utenti univoci distinti&quot;).

      >[!NOTE]
      >
      >* I dati sono disponibili dopo il 15 novembre 2018.
      >* Per alcune scorte private, gli editori non trasmettono un identificatore del dispositivo, il che impedisce il tracciamento delle frequenze.


   * **[!UICONTROL Geo]**: Utilizza questo modello precompilato per visualizzare le metriche chiave per dimensioni geografiche.

   * **[!UICONTROL Margin]:** Utilizza questo rapporto per visualizzare metriche chiave come margine, profitto e altre metriche di spesa per campagna o posizionamento.

   * **[!UICONTROL Segment]:** Utilizza questo modello precompilato per visualizzare le metriche chiave per segmento.

      >[!NOTE]
      >
      >* Questo rapporto ha lo scopo di mostrare le prestazioni dei diversi segmenti di destinazione. Utilizza i dati di appartenenza al segmento. Quando viene trasmessa un’impression a una persona o a un dispositivo appartenente a due o più segmenti di destinazione, questo rapporto include una riga per ciascun segmento. Per questo motivo, i totali in questo rapporto potrebbero non corrispondere alla consegna effettiva.
      >* Le metriche di conversione e i dati dell’obiettivo personalizzato per i segmenti sono disponibili dopo il 2 agosto 2019. Tutti gli altri dati per i segmenti sono disponibili a partire dal 1° giugno 2018.


   * **[!UICONTROL Site]:** Per impostazione predefinita, include metriche standard, spesa media totale netta e spesa totale fatturabile netta per sito.

   * **[!UICONTROL Household]:** Utilizza questo rapporto per visualizzare impression, portata e frequenza per una singola dimensione in tutti i formati di annunci a livello di famiglia in base all’indirizzo IP, anziché a livello di dispositivo/cookie. Utilizza le informazioni per ottimizzare il mix multimediale, migliorare le prestazioni e identificare le opportunità di portata incrementale. Vedere &quot;[Domande frequenti sui rapporti relativi alle famiglie](/help/dsp/reports/faq-household-report.md)&quot; per ulteriori informazioni.

## Reporting tra account {#cross-account-reporting}

Qualsiasi organizzazione con più account DSP può facoltativamente abilitare i dati tra account nei rapporti personalizzati, in base alle esigenze dell&#39;organizzazione. Ad esempio, puoi concedere l&#39;accesso A al conto B e l&#39;accesso B ai dati del conto C (ma non del conto A). Per abilitare e configurare questa funzione, contatta il team dell’account Adobe.

Una volta che la funzione è abilitata per la tua organizzazione, puoi [filter](report-settings.md) uno dei seguenti tipi di rapporti per account:  [!UICONTROL Custom], [!UICONTROL Site], [!UICONTROL Segment], [!UICONTROL Geo], [!UICONTROL Device], [!UICONTROL Frequency (by Impression)]e [!UICONTROL Conversion].

Le impostazioni dell&#39;account in [!UICONTROL Settings] > [!UICONTROL Account] indicare a) gli altri account i cui dati sono disponibili per il tuo account e b) gli altri account che possono accedere ai dati del tuo account.

>[!MORELIKETHIS]
>
>* [Creare un rapporto personalizzato](/help/dsp/reports/report-create.md)
>* [Impostazioni report personalizzate](/help/dsp/reports/report-settings.md)
>* [Domande frequenti sulle [!UICONTROL Household] Rapporto](/help/dsp/reports/faq-household-report.md)
>* [Informazioni sui report in-Platform](/help/dsp/campaign-management/reports/campaign-reports-about.md)
>* [Colonne dei rapporti disponibili](/help/dsp/reports/report-columns.md)
>* [Informazioni [!UICONTROL Report Destinations]](/help/dsp/reports/report-destinations/report-destination-about.md)

