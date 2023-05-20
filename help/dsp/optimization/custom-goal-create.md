---
title: Creare un obiettivo personalizzato
description: Creare un obiettivo personalizzato
feature: DSP Optimization
exl-id: 81b0acfa-085d-495b-9516-576b952b1307
source-git-commit: 7f35b3f3b33ed320ac186d219cbd0f826666bb3b
workflow-type: tm+mt
source-wordcount: '505'
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
   1. Nel menu principale, fai clic su **[!UICONTROL Search]** > **[!UICONTROL Admin]>[!UICONTROL Transaction Properties]**.
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
         > Tutte le proprietà di transazione tracciate per l&#39;inserzionista sono elencate per impostazione predefinita nel [!UICONTROL Available Properties] elenco.

         * Per importare un file CSV con le proprietà e i relativi pesi, fai clic su **[!UICONTROL Import]** e individuare il file da importare.

            Le proprietà importate devono già esistere per l&#39;inserzionista; i nomi non fanno distinzione tra maiuscole e minuscole.

            Le proprietà importate sostituiscono tutte le proprietà esistenti specificate.

         * Per specificare manualmente la prima proprietà con lo spessore predefinito (1), selezionarla da un elenco di tutte le proprietà di transazione rilevate per l&#39;inserzionista.

         * Per aggiungere manualmente un&#39;altra proprietà con lo spessore predefinito (1), fare clic su **[!UICONTROL +]** .

            >[!TIP]
            >
            > Per cercare una proprietà nell&#39;elenco, immettere una stringa da un punto qualsiasi all&#39;interno del nome della proprietà.

         * Per aggiungere manualmente più proprietà, fai clic su **[!UICONTROL Add Multiple Properties].** Per ogni proprietà che desideri aggiungere, fai clic sul nome della proprietà nella [!UICONTROL Available Properties] e trascinarlo nella [!UICONTROL Added Properties] colonna. Dopo aver aggiunto le proprietà, fai clic su **[!UICONTROL Add]**.

            >[!TIP]
            >
            >* Per cercare una proprietà nell&#39;elenco, immettere una stringa da un punto qualsiasi all&#39;interno del nome della proprietà nel campo di input.
            >* Per filtrare l’elenco per escludere le proprietà escluse nei rapporti, seleziona l’opzione **[!UICONTROL Hide properties excluded from reports].**


         * (Quando l&#39;obiettivo contiene più proprietà) Per modificare il peso di una proprietà rispetto alle altre proprietà dell&#39;obiettivo, immettere i valori nel campo **[!UICONTROL Weight]** campi.
      1. Nella parte inferiore delle impostazioni, fai clic su **[!UICONTROL Save]**.


Una volta creato un obiettivo, puoi assegnarlo a un pacchetto DSP come obiettivo personalizzato quando l’obiettivo di ottimizzazione è &quot;[!UICONTROL Highest ROAS - Custom Goal]&quot; o &quot;[!UICONTROL Lowest CPA - Custom Goal].&quot;

>[!TIP]
>
>Per prestazioni ottimali, le metriche combinate nell’obiettivo personalizzato (obiettivo) devono raggiungere un totale di almeno dieci conversioni al giorno. In caso contrario, la best practice prevede l’aggiunta di ulteriori eventi di supporto (proprietà di transazione), come pagine di prodotti o avvii dell’applicazione, all’obiettivo. Consulta [Best practice per la creazione di un obiettivo personalizzato](custom-goal-best-practices.md) per le linee guida.

>[!MORELIKETHIS]
>
>* [Informazioni sugli obiettivi personalizzati](custom-goal-about.md)
>* [Best practice per la creazione di un obiettivo personalizzato](custom-goal-best-practices.md)
>* [Obiettivi di ottimizzazione e modalità di utilizzo](optimization-goals.md)
>* [Impostazioni pacchetto](/help/dsp/campaign-management/packages/package-settings.md)
> * [Come l’DSP ottimizza le campagne](optimization-how-dsp-optimizes-campaigns.md)

