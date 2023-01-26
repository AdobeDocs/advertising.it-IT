---
title: Creare un obiettivo personalizzato
description: Creare un obiettivo personalizzato
feature: DSP Optimization
exl-id: 440ded21-92d3-41ad-839f-ebc8376aa932
source-git-commit: 7055a9b9d3a68ef2f690e146128d6946e713586a
workflow-type: tm+mt
source-wordcount: '504'
ht-degree: 0%

---

# Creare un obiettivo personalizzato

Puoi creare obiettivi personalizzati come *obiettivi* entro [!DNL Adobe Advertising Search].

Per creare un obiettivo personalizzato, l’account DSP deve essere collegato a un [!DNL Search] account con lo stesso ID organizzazione Adobe Experience Cloud, da [!DNL Search] impostazioni client. Se il tuo account DSP non è collegato a un [!DNL Search] account, contatta il tuo [!DNL Adobe] team di account.

>[!TIP]
>
>Consulta la sezione [best practice per la creazione di obiettivi personalizzati](custom-goal-best-practices.md) per suggerimenti su come configurare gli obiettivi personalizzati.

1. Accedi a [!DNL Adobe Advertising Search] at (aziende statunitensi) [`https://enterprise-na.efrontier.com`](https://enterprise-na.efrontier.com) o (società di tutti gli altri paesi) [`https://enterprise-intl.efrontier.com`](https://enterprise-intl.efrontier.com).
1. Assicurati che le metriche da includere nell&#39;obiettivo siano state tracciate, disponibili nel prodotto e includano un nome visualizzato:
   1. Nel menu principale, fai clic su **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Transaction Properties]**.
   1. Individua la metrica e assicurati che **[!UICONTROL Show in UI and Reports]** è abilitato per la metrica.
   1. Se la metrica non ha un valore nel **[!UICONTROL Display Name]** fare clic nella cella, immettere il nome visualizzato e quindi fare clic su **[!UICONTROL Apply].**
1. Crea l’obiettivo personalizzato come *obiettivo*:
   1. Nel menu principale, fai clic su **[!UICONTROL Search]> [!UICONTROL Optimization] >[!UICONTROL Objectives]**.
   1. Nella barra degli strumenti, fai clic su **[!UICONTROL Create objective].**
   1. Immettere le impostazioni dell&#39;obiettivo:
      1. In **[!UICONTROL Change Objective Name]** immettere il nome dell&#39;obiettivo.

         Il nome dell&#39;obiettivo verrà visualizzato nella [!UICONTROL Custom Goals] nelle impostazioni del pacchetto DSP.

      1. Associare le proprietà all&#39;obiettivo:

         >[!NOTE]
         >
         > Tutte le proprietà di transazione tracciate per l’inserzionista sono elencate per impostazione predefinita in [!UICONTROL Available Properties] elenco.

         * Per importare un file CSV con le relative proprietà e i relativi pesi, fai clic su **[!UICONTROL Import]** e individuare il file da importare.

            Le proprietà importate devono esistere già per l&#39;inserzionista; i nomi non sono sensibili a maiuscole e minuscole.

            Le proprietà importate sostituiscono le proprietà esistenti specificate.

         * Per specificare manualmente la prima proprietà con il peso predefinito (1), seleziona da un elenco di tutte le proprietà di transazione tracciate per l’inserzionista.

         * Per aggiungere manualmente un&#39;altra proprietà con lo spessore predefinito (1), fai clic su **[!UICONTROL +]** .

            >[!TIP]
            >
            > Per cercare una proprietà nell’elenco, immettere una stringa da qualsiasi punto del nome della proprietà.

         * Per aggiungere manualmente più proprietà, fai clic su **[!UICONTROL Add Multiple Properties].** Per ogni proprietà che desideri aggiungere, fai clic sul nome della proprietà nel [!UICONTROL Available Properties] e trascinarlo nella colonna [!UICONTROL Added Properties] colonna. Al termine dell’aggiunta delle proprietà, fai clic su **[!UICONTROL Add]**.

            >[!TIP]
            >
            >* Per cercare una proprietà nell’elenco, immetti una stringa da un punto qualsiasi all’interno del nome della proprietà nel campo di input.
            >* Per filtrare l’elenco ed escludere le proprietà escluse nei rapporti, seleziona l’opzione **[!UICONTROL Hide properties excluded from reports].**


         * (Quando l&#39;obiettivo contiene più proprietà) Per modificare il peso di una proprietà rispetto alle altre proprietà dell&#39;obiettivo, immettere i valori nel campo **[!UICONTROL Weight]** campi.
      1. Nella parte inferiore delle impostazioni, fai clic su **[!UICONTROL Save]**.


Una volta creato un obiettivo, puoi assegnarlo a un pacchetto DSP come obiettivo personalizzato quando l&#39;obiettivo di ottimizzazione è &quot;[!UICONTROL Highest ROAS - Custom Goal]&quot; o &quot;[!UICONTROL Lowest CPA - Custom Goal].&quot;

>[!TIP]
>
>Per ottenere prestazioni ottimali, le metriche combinate nell’obiettivo personalizzato (obiettivo) devono contenere almeno dieci conversioni al giorno. In caso contrario, la best practice prevede l’aggiunta all’obiettivo di eventi di supporto aggiuntivi (proprietà della transazione), come le pagine di prodotto o l’avvio dell’applicazione. Vedi [Tecniche consigliate per la creazione di un obiettivo personalizzato](custom-goal-best-practices.md) per le linee guida.

>[!MORELIKETHIS]
>
>* [Informazioni sugli obiettivi personalizzati](custom-goal-about.md)
>* [Tecniche consigliate per la creazione di un obiettivo personalizzato](custom-goal-best-practices.md)
>* [Obiettivi di ottimizzazione e come utilizzarli](optimization-goals.md)
>* [Impostazioni pacchetto](/help/dsp/campaign-management/packages/package-settings.md)
> * [Ottimizzazione DSP campagne](optimization-how-dsp-optimizes-campaigns.md)

