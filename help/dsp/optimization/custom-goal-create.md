---
title: Creare un obiettivo personalizzato
description: Creare un obiettivo personalizzato
feature: DSP Optimization
exl-id: 81b0acfa-085d-495b-9516-576b952b1307
source-git-commit: 6aa81fe4fd5ea6cb188b7f18b1574c26ddfcbb92
workflow-type: tm+mt
source-wordcount: '514'
ht-degree: 0%

---

# Creare un obiettivo personalizzato

Puoi creare obiettivi personalizzati con *obiettivi* entro [!DNL Advertising Search, Social, & Commerce].

Per creare un obiettivo personalizzato, l’account DSP deve essere collegato a un [!DNL Search, Social, & Commerce] con lo stesso ID organizzazione Adobe Experience Cloud, dall&#39;interno del [!DNL Search, Social, & Commerce] impostazioni client. Se il tuo account DSP non è collegato a un [!DNL Search, Social, & Commerce] account, contatta il tuo Account Team Adobe.

>[!TIP]
>
>Consulta la [best practice per la creazione di obiettivi personalizzati](custom-goal-best-practices.md) per suggerimenti su come configurare gli obiettivi personalizzati.

1. Accedi a [!DNL Advertising Search, Social, & Commerce] at (utenti in Nord America) [`https://enterprise-na.efrontier.com`](https://enterprise-na.efrontier.com) o (tutti gli altri utenti) [`https://enterprise-intl.efrontier.com`](https://enterprise-intl.efrontier.com).
1. Assicurati che le metriche da includere nell’obiettivo siano state tracciate, siano disponibili nel prodotto e includano un nome visualizzato:
   1. Nel menu principale, fai clic su **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Conversions]**.
   1. Individua la metrica e assicurati che **[!UICONTROL Show in UI and Reports]** è abilitato per la metrica.
   1. Se la metrica non ha un valore in **[!UICONTROL Display Name]** , fare clic nella cella, immettere il nome visualizzato e quindi fare clic su **[!UICONTROL Apply].**
1. Creare l’obiettivo personalizzato come *obiettivo*:
   1. Nel menu principale, fai clic su **[!UICONTROL Search]** > **[!UICONTROL Optimization]>[!UICONTROL Objectives]**.
   1. Nella barra degli strumenti, fai clic su **[!UICONTROL Create objective].**
   1. Immettere le impostazioni obiettivo:
      1. In **[!UICONTROL Change Objective Name]** immettere il nome dell&#39;obiettivo.

         Il nome dell&#39;obiettivo verrà visualizzato nel [!UICONTROL Custom Goals] nelle impostazioni del pacchetto DSP.

      1. Associa proprietà all&#39;obiettivo:

         >[!NOTE]
         >
         > Tutte le metriche di conversione tracciate per l’inserzionista sono elencate per impostazione predefinita nella [!UICONTROL Available Properties] elenco.

         * Per importare un file CSV con le metriche di conversione e i relativi pesi, fai clic su **[!UICONTROL Import]** e individuare il file da importare.

           Le metriche di conversione importate devono esistere già per l&#39;inserzionista; i nomi non fanno distinzione tra maiuscole e minuscole.

           Le metriche di conversione importate sostituiscono eventuali proprietà esistenti specificate.

         * Per specificare manualmente la prima metrica di conversione con lo spessore predefinito (1), selezionala da un elenco di tutte le metriche di conversione tracciate per l’inserzionista.

         * Per aggiungere manualmente un’altra metrica di conversione con lo spessore predefinito (1), fai clic su **[!UICONTROL +]** .

           >[!TIP]
           >
           > Per cercare una metrica nell’elenco, immetti una stringa da un punto qualsiasi all’interno del nome della metrica.

         * Per aggiungere manualmente più metriche di conversione, fai clic su **[!UICONTROL Add Multiple Properties].** Per ogni metrica di conversione che desideri aggiungere, fai clic sul nome della metrica nella [!UICONTROL Available Properties] e trascinarlo nella [!UICONTROL Added Properties] colonna. Dopo aver aggiunto le metriche, fai clic su **[!UICONTROL Add]**.

           >[!TIP]
           >
           >* Per cercare una metrica nell’elenco, immetti una stringa da un punto qualsiasi all’interno del nome della metrica nel campo di input.
           >* Per filtrare l’elenco in modo da escludere le metriche escluse nei rapporti, seleziona l’opzione **[!UICONTROL Hide properties excluded from reports].**

         * (Quando l’obiettivo contiene più metriche di conversione) Per modificare il peso di una metrica rispetto alle altre metriche dell’obiettivo, immetti i valori nella **[!UICONTROL Weight]** campi.

      1. Nella parte inferiore delle impostazioni, fai clic su **[!UICONTROL Save]**.

Una volta creato un obiettivo, puoi assegnarlo a un pacchetto DSP come obiettivo personalizzato quando l’obiettivo di ottimizzazione è[!UICONTROL Highest Return on Ad Spend (ROAS)"] o &quot;[!UICONTROL Lowest Cost per Acquisition (CPA)].&quot;

>[!TIP]
>
>Per prestazioni ottimali, le metriche combinate nell’obiettivo personalizzato (obiettivo) devono raggiungere un totale di almeno dieci conversioni al giorno. In caso contrario, la best practice prevede di aggiungere all’obiettivo ulteriori metriche di conversione di supporto, come pagine di prodotti o avvii dell’applicazione. Consulta [Best practice per la creazione di un obiettivo personalizzato](custom-goal-best-practices.md) per le linee guida.

>[!MORELIKETHIS]
>
>* [Informazioni sugli obiettivi personalizzati](custom-goal-about.md)
>* [Best practice per la creazione di un obiettivo personalizzato](custom-goal-best-practices.md)
>* [Obiettivi di ottimizzazione e modalità di utilizzo](optimization-goals.md)
>* [Impostazioni pacchetto](/help/dsp/campaign-management/packages/package-settings.md)
> * [Come l’DSP ottimizza le campagne](optimization-how-dsp-optimizes-campaigns.md)
