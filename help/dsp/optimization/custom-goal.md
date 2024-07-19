---
title: Obiettivi personalizzati
description: Scopri gli obiettivi personalizzati per definire gli eventi di successo in pacchetti ottimizzati per il CPA più basso o il ROAS più alto.
feature: DSP Optimization
exl-id: e40b82bc-2558-4e78-b269-9b9a3f0f5219
source-git-commit: 290eea50fe3c52a534ad6ab4fcf6d857b13230aa
workflow-type: tm+mt
source-wordcount: '1221'
ht-degree: 0%

---

# Obiettivi personalizzati

Gli obiettivi personalizzati definiscono gli eventi di successo necessari a un inserzionista per raggiungere i suoi obiettivi aziendali. Ogni pacchetto che utilizza l&#39;obiettivo di ottimizzazione &quot;[!UICONTROL Highest Return on Ad Spend (ROAS)"] o &quot;[!UICONTROL Lowest Cost per Acquisition (CPA)]&quot; deve includere un obiettivo personalizzato per consentire il raggiungimento dell&#39;obiettivo di ottimizzazione complessivo. Puoi creare obiettivi personalizzati come *obiettivi* in [!DNL Advertising Search, Social, & Commerce]. Il nome di ciascun obiettivo per l&#39;DSP deve essere preceduto dal prefisso &quot;ADSP_&quot;.

<!-- update image or omit it

![custom goals](/help/dsp/assets/objective-goals.png)
 -->

Ogni obiettivo personalizzato (obiettivo) è costituito da una o più metriche di conversione e dai relativi pesi di tali metriche. Le metriche di conversione disponibili includono tutte le metriche tracciate utilizzando il pixel di conversione di Adobe Advertising e tramite Adobe Analytics. Per gli obiettivi personalizzati dell’DSP vengono considerati solo i pesi non mobili, ma vengono utilizzati per tutti i tipi di annunci.

Ad esempio, supponiamo che tre metriche di conversione siano pertinenti per un pacchetto specifico in una delle tue campagne: &quot;Download PDF&quot; con valore 20 USD, &quot;Registrazione e-mail&quot; con valore 30 USD e &quot;Conferma ordine&quot; con valore 40 USD. Se vuoi attribuire un peso in base al valore monetario una tantum dell’azione del cliente, i pesi relativi delle metriche sono 1, 1,5 e 2.

Dopo aver [creato un obiettivo personalizzato](#custom-goal-create), puoi [assegnarlo a un pacchetto](/help/dsp/campaign-management/packages/package-settings.md) per la generazione di rapporti e l&#39;ottimizzazione algoritmica tramite Adobe Sensei.

I consigli sul peso vengono generati automaticamente per le metriche attribuite dall’DSP negli obiettivi e possono essere applicati con un solo clic. Tutte le modifiche di peso agli obiettivi con il prefisso &quot;ADSP_&quot; vengono applicate algoritmicamente all&#39;DSP entro due giorni. Per ulteriori informazioni sui consigli sul peso, consulta il capitolo della Guida all’ottimizzazione su &quot;Nuovi obiettivi (Beta)&quot;, disponibile in Search, Social e Commerce.

## Creare un obiettivo personalizzato {#custom-goal-create}

Per creare un obiettivo personalizzato, l&#39;account DSP deve essere collegato a un account [!DNL Search, Social, & Commerce] con lo stesso ID organizzazione Adobe Experience Cloud, dalle impostazioni client [!DNL Search, Social, & Commerce]. Se il tuo account DSP non è collegato a un account [!DNL Search, Social, & Commerce], contatta il team dell&#39;account Adobe.

1. Accedi a [!DNL Advertising Search, Social, & Commerce] all&#39;indirizzo [`https://enterprise-na.efrontier.com`](https://enterprise-na.efrontier.com) o [`https://enterprise-intl.efrontier.com`](https://enterprise-intl.efrontier.com) (utenti in Nord America).

1. Assicurati che le metriche da includere nell’obiettivo siano state tracciate, siano disponibili nel prodotto e includano un nome visualizzato:

   1. Nel menu principale, fare clic su **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Conversions]**.

   1. Individuare la metrica e verificare che **[!UICONTROL Show in UI and Reports]** sia abilitato per la metrica.

      >[!NOTE]
      >
      >* [!DNL Analytics] eventi personalizzati seguono questa convenzione di denominazione: `custom_event_[*event #*]_[*Analytics report suite ID*]`. Esempio: `custom_event_16_examplersid`

   1. Se la metrica non ha un valore nella colonna **[!UICONTROL Display Name]**, fare clic nella cella, immettere il nome visualizzato e fare clic su **[!UICONTROL Apply].**

1. Crea l&#39;obiettivo personalizzato come *obiettivo*:

   1. Nel menu principale, fare clic su **[!UICONTROL Search]** > **[!UICONTROL Optimization]>[!UICONTROL New Objectives Beta]**.

   1. Nella barra degli strumenti, fai clic su ![Crea](/help/dsp/assets/create-search-ui.png "Crea").

   1. Immettere le impostazioni dell&#39;obiettivo, incluse le metriche associate e il relativo peso numerico per i dispositivi non mobili, quindi salvare l&#39;obiettivo. Considera quanto segue:

      * Per gli obiettivi utilizzati per i pacchetti Advertising DSP, il nome dell’obiettivo deve essere preceduto da &quot;ADSP_&quot;, ad esempio &quot;ADSP_Registrations&quot;. Il prefisso non fa distinzione tra maiuscole e minuscole.

      * Includi solo le metriche attribuite all’DSP. Tutte le metriche attribuite a Search, Social e Commerce o a qualsiasi altra rete di annunci vengono ignorate.

      * Almeno una metrica deve avere il tipo *[!UICONTROL Goal]*.

      * L’DSP utilizza i pesi non mobili per tutti gli annunci. Eventuali pesi dei dispositivi mobili specificati vengono ignorati.

      >[!NOTE]
      >
      >* [!DNL Analytics] eventi personalizzati seguono questa convenzione di denominazione: `custom_event_[*event #*]_[*Analytics report suite ID*]`. Esempio: `custom_event_16_examplersid`
      >* [!DNL Analytics] dimensioni e segmenti non sono disponibili, ad Adobe Advertising per l&#39;ottimizzazione.

      >[!TIP]
      >
      >Per prestazioni ottimali, le metriche combinate nell’obiettivo personalizzato (obiettivo) devono raggiungere un totale di almeno dieci conversioni al giorno. In caso contrario, la best practice prevede di aggiungere all’obiettivo ulteriori metriche di conversione di supporto, come pagine di prodotti o avvii dell’applicazione. Consulta [Best practice per la creazione di un obiettivo personalizzato](#custom-goal-best-practices) per le linee guida.

Nelle impostazioni del pacchetto DSP per i pacchetti che utilizzano l&#39;obiettivo di ottimizzazione &quot;[!UICONTROL Highest Return on Ad Spend (ROAS)"] o &quot;[!UICONTROL Lowest Cost per Acquisition (CPA)]&quot;, il nome dell&#39;obiettivo è ora incluso nell&#39;elenco [!UICONTROL Custom Goals]. Quando si seleziona l&#39;obiettivo come obiettivo personalizzato per un pacchetto, l&#39;elenco [!UICONTROL Conversion Metric] include tutte le metriche dell&#39;obiettivo.

## Best practice per la creazione di un obiettivo personalizzato {#custom-goal-best-practices}

### Obiettivi personalizzati con una singola metrica

Gli esempi seguenti mostrano come configurare obiettivi per il targeting di una singola metrica di conversione.

#### Esempio per una campagna con obiettivo di ottimizzazione &quot;[!UICONTROL Highest Return on Ad Spend (ROAS)]&quot;

Se l&#39;obiettivo della campagna è il ricavo ([!UICONTROL Highest Return on Ad Spend (ROAS)]) e il ricavo da tutti i tipi di dispositivi è ugualmente importante per te, includi la metrica &quot;[!UICONTROL Revenue]&quot; con un peso non mobile di uno (1); il peso del dispositivo mobile viene ignorato. Selezionare il tipo di metrica *[!UICONTROL Goal]*.

<!-- update image or delete 

![example of a ROAS custom goal with a single conversion metric](/help/dsp/assets/custom-goal-roas.png)

-->

>[!NOTE]
>
> Un peso non mobile di uno (1) equivale a un valore di uno (1) per ogni $ 1 di ricavo tracciato per gli annunci display su qualsiasi dispositivo. Ad esempio, una conversione da 250 $ con un peso non mobile di uno (1) viene segnalata come 250 $ per le conversioni. Se alla metrica di conversione viene assegnato un peso non mobile di 0,5, la conversione di 250 $ viene segnalata come Adobe Advertising di 125 $ ($250 Conversione * 0,5 [!UICONTROL Non-mobile Weight] = $125).

#### Esempio per una campagna con obiettivo di ottimizzazione &quot;[!UICONTROL Lowest Cost per Acquisition (CPA)]&quot;

Se l&#39;obiettivo della campagna è il costo più basso per acquisizione (CPA) e richiede un solo evento di successo (ad esempio &quot;Invio applicazione&quot;), includi quella metrica e specifica il tipo di metrica *[!UICONTROL Goal]*. La best practice prevede di impostare il peso del dispositivo non mobile su uno (1); il peso del dispositivo mobile viene ignorato.

<!-- update image or delete 

![example of a CPA custom goal with a single conversion metric](/help/dsp/assets/custom-goal-roas.png)

-->

>[!NOTE]
>
> Un peso non mobile di uno (1) equivale a un valore di uno (1) per ogni conversione tracciata per gli annunci display su qualsiasi dispositivo. Ad esempio, se vengono tracciate 10 conversioni di invio di applicazioni, vengono segnalate 10 conversioni di invio di applicazioni. Tuttavia, se alla metrica di conversione viene assegnato un peso non mobile di 0,5, le 10 conversioni vengono riportate come cinque (5) nell’Adobe Advertising (10 conversioni * 0,5 [!UICONTROL Non-mobile Weight] = 5).

### Obiettivi personalizzati con più metriche

Esistono due scenari in cui puoi utilizzare più metriche in un obiettivo personalizzato:

* L’obiettivo della campagna prevede più eventi di successo. Ad esempio, puoi promuovere più di un’azione nel sito (Download di PDF, Contattaci e Iscrizione e-mail) e tutte queste azioni contribuiscono al tuo obiettivo CPA. Se l&#39;obiettivo include le tre metriche separate, ciascuna con un peso non mobile di uno (1), l&#39;algoritmo [!DNL Adobe Sensei] tratta ciascuna delle metriche e i tipi di dispositivi utente con la stessa importanza. Se le diverse metriche hanno costi o importanza diversi, puoi regolare di conseguenza i loro pesi relativi.

<!-- update image or delete it and adjust the wording above

   ![example of a custom goal with multiple metrics](/help/dsp/assets/custom-goal-multiple-properties.png)

-->

* La singola metrica di conversione nell’obiettivo personalizzato non raggiunge il minimo di 10 conversioni al giorno necessarie per prestazioni ottimizzate. Ciò può verificarsi a causa di una spesa minima giornaliera per i pacchetti o di un numero limitato di conversioni naturali. L’aggiunta di metriche di supporto aggiuntive all’obiettivo personalizzato può aiutarti a raggiungere la soglia di 10 conversioni al giorno. Dieci eventi di supporto possono aiutare un pacchetto a raggiungere la soglia di 10/die, anche quando ciascuno dei loro pesi è inferiore a uno (1). Ma potresti non aver bisogno di aggiungere tanti eventi.

  Quando aggiungi metriche di supporto a un obiettivo personalizzato, ponderale in base alla loro importanza relativa per l’evento di successo principale e tieni presente la quantità di punti dati. Questo consente all’algoritmo Adobe Sensei di bilanciare più metriche e ottimizzarle per il raggiungimento dell’obiettivo.

  L’obiettivo dell’esempio seguente include tre metriche, ciascuna con un peso non mobile diverso: invio applicazione = 1, inizio applicazione = 0.1 e pagina di destinazione inserzionista = 0.01. Ciò significa che ogni conversione Invio applicazione ha lo stesso valore per la tua azienda come media di 10 conversioni di Avvio applicazione e 100 conversioni di Pagina di destinazione inserzionista.

<!-- update image or delete it and adjust the wording above

   ![example of a custom goal with multiple metrics](/help/dsp/assets/custom-goal-multiple-properties2.png)

-->

Se invece le visite della pagina di destinazione vengono ponderate allo stesso modo degli invii di applicazioni, la quantità naturalmente maggiore di visite alla pagina di destinazione potrebbe superare l&#39;obiettivo e distorcere le visite alla pagina di destinazione.<!--reword-->

>[!MORELIKETHIS]
>
>* [Obiettivi di ottimizzazione e modalità di utilizzo](optimization-goals.md)
>* [Impostazioni pacchetto](/help/dsp/campaign-management/packages/package-settings.md)
> * [Come DSP Ottimizza Le Campagne](optimization-how-dsp-optimizes-campaigns.md)
