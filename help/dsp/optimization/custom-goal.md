---
title: Obiettivi personalizzati
description: Scopri gli obiettivi personalizzati per definire gli eventi di successo in pacchetti ottimizzati per il CPA più basso o il ROAS più alto.
feature: DSP Optimization
source-git-commit: f05d0f909cda6248260eaafd2fd24a8eca7f47e5
workflow-type: tm+mt
source-wordcount: '1105'
ht-degree: 0%

---

# Obiettivi personalizzati

Gli obiettivi personalizzati definiscono gli eventi di successo necessari a un inserzionista per raggiungere i suoi obiettivi aziendali. Ogni pacchetto che utilizza l’obiettivo di ottimizzazione &quot;[!UICONTROL Highest Return on Ad Spend (ROAS)"] o &quot;[!UICONTROL Lowest Cost per Acquisition (CPA)]&quot; deve includere un obiettivo personalizzato che contribuisca a raggiungere l’obiettivo di ottimizzazione generale. Puoi creare obiettivi personalizzati con *obiettivi* in [!DNL Advertising Search, Social, & Commerce].

<!-- update image or omit it

![custom goals](/help/dsp/assets/objective-goals.png)
 -->

Ogni obiettivo personalizzato è costituito da una o più metriche di conversione e dai relativi pesi di tali metriche. Le metriche di conversione disponibili includono tutte le metriche tracciate utilizzando il pixel di conversione di Adobi Advertising e tramite Adobe Analytics.

Ad esempio, supponiamo che tre metriche di conversione siano pertinenti per un pacchetto specifico in una delle tue campagne: &quot;Download PDF&quot; con valore 20 USD, &quot;Registrazione e-mail&quot; con valore 30 USD e &quot;Conferma ordine&quot; con valore 40 USD. Se vuoi attribuire un peso in base al valore monetario una tantum dell’azione del cliente, i pesi relativi delle metriche sono 1, 1,5 e 2.

Una volta [creare un obiettivo personalizzato](#custom-goal-create), è possibile [assegnarlo a un pacchetto](/help/dsp/campaign-management/packages/package-settings.md) per il reporting e l’ottimizzazione algoritmica tramite Adobe Sensei.

## Creare un obiettivo personalizzato {#custom-goal-create}

Per creare un obiettivo personalizzato, l’account DSP deve essere collegato a un [!DNL Search, Social, & Commerce] con lo stesso ID organizzazione Adobe Experience Cloud, dall&#39;interno del [!DNL Search, Social, & Commerce] impostazioni client. Se il tuo account DSP non è collegato a un [!DNL Search, Social, & Commerce] , quindi contatta il tuo Account Team Adobe.

1. Accedi a [!DNL Advertising Search, Social, & Commerce] at (utenti in Nord America) [`https://enterprise-na.efrontier.com`](https://enterprise-na.efrontier.com) o (tutti gli altri utenti) [`https://enterprise-intl.efrontier.com`](https://enterprise-intl.efrontier.com).

1. Assicurati che le metriche da includere nell’obiettivo siano state tracciate, siano disponibili nel prodotto e includano un nome visualizzato:

   1. Nel menu principale, fai clic su **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Conversions]**.

   1. Individua la metrica e assicurati che **[!UICONTROL Show in UI and Reports]** è abilitato per la metrica.

      >[!NOTE]
      >
      >* [!DNL Analytics] gli eventi personalizzati seguono questa convenzione di denominazione: `custom_event_[*event #*]_[*Analytics report suite ID*]`. Esempio: `custom_event_16_examplersid`

   1. Se la metrica non ha un valore in **[!UICONTROL Display Name]** , quindi fare clic nella cella, immettere il nome visualizzato e fare clic su **[!UICONTROL Apply].**

1. Creare l’obiettivo personalizzato come *obiettivo*:

   1. Nel menu principale, fai clic su **[!UICONTROL Search]** > **[!UICONTROL Optimization]>[!UICONTROL New Objectives Beta]**.

   1. Nella barra degli strumenti, fai clic su ![Crea](/help/dsp/assets/create-search-ui.png "Crea").

   1. Immetti le impostazioni dell&#39;obiettivo, incluse le metriche associate e il relativo peso numerico per dispositivi non mobili e dispositivi mobili, quindi salva l&#39;obiettivo.

      Almeno una metrica deve avere il tipo di metrica *[!UICONTROL Goal]*.

      >[!NOTE]
      >
      >* [!DNL Analytics] gli eventi personalizzati seguono questa convenzione di denominazione: `custom_event_[*event #*]_[*Analytics report suite ID*]`. Esempio: `custom_event_16_examplersid`
      >* [!DNL Analytics] dimensioni e segmenti non sono disponibili per l’ottimizzazione di Adobi Advertising.

Nelle impostazioni del pacchetto DSP per i pacchetti che utilizzano l’obiettivo di ottimizzazione &quot;[!UICONTROL Highest Return on Ad Spend (ROAS)"] o &quot;[!UICONTROL Lowest Cost per Acquisition (CPA)],&quot; il nome dell’obiettivo è ora incluso nel [!UICONTROL Custom Goals] elenco. Quando selezioni l’obiettivo come obiettivo personalizzato per un pacchetto, il [!UICONTROL Conversion Metric] L’elenco include tutte le metriche dell’obiettivo.

>[!TIP]
>
>Per prestazioni ottimali, le metriche combinate nell’obiettivo personalizzato (obiettivo) devono raggiungere un totale di almeno dieci conversioni al giorno. In caso contrario, la best practice prevede di aggiungere all’obiettivo ulteriori metriche di conversione di supporto, come pagine di prodotti o avvii dell’applicazione. Consulta [Best practice per la creazione di un obiettivo personalizzato](custom-goal-best-practices.md) per le linee guida.

## Best practice per la creazione di un obiettivo personalizzato [#custom-goal-best-practices]

### Obiettivi personalizzati con una singola metrica

Gli esempi seguenti mostrano come configurare obiettivi per il targeting di una singola metrica di conversione.

#### Esempio di una campagna con &quot;[!UICONTROL Highest Return on Ad Spend (ROAS)]&quot; Obiettivo di ottimizzazione

Se l&#39;obiettivo della campagna è il profitto ([!UICONTROL Highest Return on Ad Spend (ROAS)]), e i ricavi da tutti i tipi di dispositivi sono ugualmente importanti per te, quindi includi il &quot;[!UICONTROL Revenue]&quot; metrica con un peso non mobile (per conversioni da un dispositivo non mobile) di uno (1) e un peso mobile (per conversioni da un dispositivo mobile) di uno (1). Seleziona il tipo di metrica *[!UICONTROL Goal]*.

<!-- update image or delete 

![example of a ROAS custom goal with a single conversion metric](/help/dsp/assets/custom-goal-roas.png)

-->

>[!NOTE]
>
> Un peso per dispositivi mobili o non mobili pari a uno (1) equivale a un valore di uno (1) per ogni $ 1 di ricavo tracciato.
>
> Ad esempio, una conversione da 250 $ con un peso non mobile di uno (1) viene segnalata come 250 $ per le conversioni. Se alla metrica di conversione viene assegnato un peso non mobile di 0,5, la conversione di $ 250 da un dispositivo non mobile viene segnalata come $ 125 in Adobe Advertising (conversione $ 250 * 0,5 [!UICONTROL Non-mobile Weight] = $125).

#### Esempio di una campagna con &quot;[!UICONTROL Lowest Cost per Acquisition (CPA)]&quot; Obiettivo di ottimizzazione

Se l’obiettivo della campagna è il costo più basso per acquisizione (CPA) e richiede un solo evento di successo (ad esempio &quot;Invio applicazione&quot;), includi tale metrica e specifica il tipo di metrica come *[!UICONTROL Goal]*. La best practice prevede di impostare sia il peso non mobile che il peso mobile come uno (1).

<!-- update image or delete 

![example of a CPA custom goal with a single conversion metric](/help/dsp/assets/custom-goal-roas.png)

-->

>[!NOTE]
>
> Un peso mobile o non mobile di uno (1) equivale al valore di uno (1) per ogni conversione tracciata. Ad esempio, se vengono tracciate 10 conversioni di invio di applicazioni, vengono segnalate 10 conversioni di invio di applicazioni. Tuttavia, se alla metrica di conversione è assegnato un peso non mobile di 0,5, allora le 10 conversioni non mobili sono segnalate come cinque (5) nell’Adobe Advertising (10 conversioni * 0,5 [!UICONTROL Non-mobile Weight] = 5).

### Obiettivi personalizzati con più metriche

Esistono due scenari in cui puoi utilizzare più metriche in un obiettivo personalizzato:

* L’obiettivo della campagna prevede più eventi di successo. Ad esempio, puoi promuovere più di un’azione nel sito (Download di PDF, Contattaci e Iscrizione e-mail) e tutte queste azioni contribuiscono al tuo obiettivo CPA. Se l’obiettivo include le tre metriche separate, ciascuna con un peso di uno (1) non mobile e mobile, il valore [!DNL Adobe Sensei] Ogni metrica e tipo di dispositivo dell’utente riceverà lo stesso livello di importanza dall’algoritmo. Se le diverse metriche e i diversi tipi di dispositivi hanno costi o importanza diversi, è necessario regolare di conseguenza i loro pesi relativi.

<!-- update image or delete it and adjust the wording above

   ![example of a custom goal with multiple metrics](/help/dsp/assets/custom-goal-multiple-properties.png)

-->

* La singola metrica di conversione nell’obiettivo personalizzato non raggiunge il minimo di 10 conversioni al giorno necessarie per prestazioni ottimizzate. Ciò può verificarsi a causa di una spesa minima giornaliera per i pacchetti o di un numero limitato di conversioni naturali. L’aggiunta di metriche di supporto aggiuntive all’obiettivo personalizzato può aiutarti a raggiungere la soglia di 10 conversioni al giorno. Dieci eventi di supporto possono aiutare un pacchetto a raggiungere la soglia di 10/die, anche quando ciascuno dei loro pesi è inferiore a uno (1). Ma potresti non aver bisogno di aggiungere tanti eventi.

  Quando aggiungi metriche di supporto a un obiettivo personalizzato, ponderale in base alla loro importanza relativa per l’evento di successo principale e tieni presente la quantità di punti dati. Questo consente all’algoritmo Adobe Sensei di bilanciare più metriche e ottimizzarle per il raggiungimento dell’obiettivo.

  L’obiettivo dell’esempio seguente include tre metriche, ciascuna con un peso non mobile diverso: invio applicazione = 1, inizio applicazione = 0.1 e pagina di destinazione inserzionista = 0.01. Ciò significa che ogni conversione di invio applicazione da dispositivi non mobili ha lo stesso valore per la tua azienda come media di 10 conversioni di avvio applicazione da dispositivi non mobili e 100 conversioni di pagina di destinazione inserzionista da dispositivi non mobili.

<!-- update image or delete it and adjust the wording above

   ![example of a custom goal with multiple metrics](/help/dsp/assets/custom-goal-multiple-properties2.png)

-->

Se, invece, hai ponderato le visite della pagina di destinazione allo stesso modo degli invii di applicazioni, allora la quantità naturalmente più elevata di visite della pagina di destinazione potrebbe sopraffare l’obiettivo e distorcere le visite della pagina di destinazione.<!--reword-->

>[!MORELIKETHIS]
>
>* [Obiettivi di ottimizzazione e modalità di utilizzo](optimization-goals.md)
>* [Impostazioni pacchetto](/help/dsp/campaign-management/packages/package-settings.md)
> * [Come l’DSP ottimizza le campagne](optimization-how-dsp-optimizes-campaigns.md)
