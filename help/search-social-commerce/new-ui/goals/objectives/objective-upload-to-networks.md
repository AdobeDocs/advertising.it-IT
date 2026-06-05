---
title: (Nuova interfaccia utente) Abilita il caricamento degli obiettivi nelle reti di annunci
description: Scopri come caricare gli obiettivi per i portfolio ibridi in Google Ads e Microsoft Advertising.
feature: Search Objectives, Search Optimization
hide: true
source-git-commit: b9388f691c8e804cece8d9f1eeb1bdc4f352dd11
workflow-type: tm+mt
source-wordcount: '722'
ht-degree: 0%

---

# (Nuova interfaccia utente) Abilita il caricamento degli obiettivi nelle reti di annunci

*funzionalità Beta*

*Inserzionisti con [!DNL Google Ads] e solo [!DNL Microsoft Advertising] account*

*Inserzionisti abilitati solo per l&#39;ottimizzazione ibrida*

Search, Social e Commerce possono caricare gli obiettivi per i portfolio di un account inserzionista in [!DNL Google Ads] e [!DNL Microsoft Advertising] in modo da poterli utilizzare per l&#39;ottimizzazione ibrida. Gli obiettivi caricati sono disponibili come azioni di conversione per gli obiettivi di conversione personalizzati a livello di account e di campagna.

L’abilitazione di questa opzione attiva automaticamente un caricamento per gli obiettivi nei portfolio che contengono campagne con strategie di offerta intelligenti. Search, Social e Commerce creano una conversione sulla rete di annunci per ogni obiettivo applicabile. La conversione rappresenta tutte le metriche di conversione ponderate nell’obiettivo a livello di ID EF (click ID). Per [!DNL Google Ads] clic, l&#39;ID EF è [!DNL Google Ads] `gclid`; per [!DNL Microsoft Advertising] clic, l&#39;ID EF è [!DNL Microsoft Advertising] `msclkid`. A causa di questo ID clic, i dati di conversione possono essere mappati sulla parola chiave specifica e sul tempo di clic.

Ogni conversione caricata ha il seguente nome:

`O_ACS_OBJ_<network_ID>_<objective_ID>_<network_account_ID>`

dove `<network_ID>` è l&#39;ID numerico utilizzato da Search, Social e Commerce per la rete di annunci, `<objective_ID>` è l&#39;ID obiettivo numerico e `<network_account_ID>` è l&#39;ID numerico per l&#39;account di gestione o l&#39;account di gestione della rete di annunci.

I caricamenti in [!DNL Google Ads] e [!DNL Microsoft Advertising] si verificano nell&#39;arco della giornata, in genere ogni ora. Per gli inserzionisti con account di grandi dimensioni o configurazioni personalizzate, i caricamenti si verificano almeno tre volte al giorno.

>[!IMPORTANT]
>
>Le conversioni tracciate da [!DNL Google Ads] e dal tag UET (Universal Event Tracking) di [!DNL Microsoft Advertising] non vengono ricaricate nelle reti di annunci. Se li includi all’interno di un obiettivo, devi aggiungerli agli obiettivi della campagna nell’editor della rete di annunci.

1. Nel menu principale, fare clic su **[!UICONTROL Goals]** > **[!UICONTROL Objectives]**.

1. Nella barra degli strumenti fare clic su **[!UICONTROL Upload Objective]**.

1. Nella finestra di dialogo [!UICONTROL Objective Upload Setup], imposta l&#39;interruttore **[!UICONTROL Enable Objective Upload]** su **[!UICONTROL On]**.

1. (Inserzionisti con account [!DNL Google Ads] che svolgono attività commerciali nello Spazio economico europeo (SEE) o nel Regno Unito (UK); facoltativo) Se hai raccolto il consenso degli utenti di EEA e UK a caricare i loro dati a scopo pubblicitario, seleziona la casella di controllo per confermare che i consensi degli utenti di EEA e UK sono stati raccolti. Questo invia lo stato del consenso come **[!UICONTROL GRANTED]** a [!DNL Google Ads] e [!DNL Microsoft Advertising]. Se non è selezionata, lo stato del consenso viene inviato come **[!UICONTROL UNSPECIFIED]**.

1. (Se le conversioni vengono tracciate a livello di account manager) [Aggiungi le credenziali per l&#39;account manager](/help/search-social-commerce/new-ui/set-up/accounts/api-accounts/manager-account-manage.md) prima di salvare.

1. Fare clic su **[!UICONTROL Save]**.

1. Verificare che ogni obiettivo, denominato `O_ACS_OBJ_<network_ID>_<objective_ID>_<network_account_ID>`, venga visualizzato entro due giorni sulla rete di annunci.

   Nell&#39;editor [!DNL Google Ads], cerca le [azioni di conversione](https://support.google.com/google-ads/answer/11461796){target="_blank"}. Nell&#39;editor [!DNL Microsoft Advertising], cerca i tuoi [obiettivi di conversione](https://help.ads.microsoft.com/#apex/ads/en/56709){target="_blank"}.

   Se necessario, aggiorna l’intervallo di date per includere la data di caricamento.

## Modalità di calcolo dell&#39;obiettivo ponderato

L&#39;obiettivo ponderato passato alla rete di annunci è la somma di tutti i valori delle metriche raccolti, ad eccezione delle conversioni tracciate da [!DNL Google Ads] o dal tag UET (Universal Event Tracking) di [!DNL Microsoft Advertising]. Il valore viene calcolato utilizzando il metodo di attribuzione impostato per l’account Search, Social e Commerce dell’inserzionista.

Ad esempio, supponiamo che la metrica di obiettivo dell’obiettivo sia Aggiunte al carrello con un peso di 25, e che le metriche di assistenza includano GGL_Lead e Revenue con un peso di 1 e Downloads con un peso di 0,5.

![Esempio di obiettivo ponderato](/help/search-social-commerce/assets/objective-example.png "Esempio di obiettivo ponderato")

Supponiamo che una parola chiave abbia prodotto le seguenti azioni per il portfolio:

* 10 Aggiunte al carrello
* 500 dollari di ricavi
* 50 download
* 5 GGL_Lead

GGL_Lead non è incluso nel calcolo/caricamento perché è una metrica tracciata da Google Ads. Pertanto il valore obiettivo ponderato è calcolato come [(10 x 25) + (500 x 1) + (50 x 0,5)] = 775.

>[!TIP]
>
>Puoi visualizzare i dati per i ricavi ponderati di Adobe Advertising nei rapporti della rete di annunci. Come best practice, confronta i ricavi ponderati con il [!DNL Google Ads] &quot;All conv. (di conv. time)&quot; o la metrica [!DNL Microsoft Advertising] &quot;All conv. revenue&quot;, segmentato con la metrica O_ACS_OBJ*.

## Risoluzione dei problemi relativi agli obiettivi mancanti

Se l&#39;obiettivo, denominato `O_ACS_OBJ_<network_ID>_<objective_ID>_<network_account_ID>`, per uno dei portfolio non viene visualizzato nella rete di annunci, verificare quanto segue:

* ([!DNL Google Ads]) Verificare se le conversioni devono essere caricate a livello di account o manager. Se devono essere caricati a livello di manager:

   * Verificare se sono state fornite le credenziali per l&#39;account manager [!DNL Google Ads]. Se necessario, [aggiungi le credenziali per l&#39;account manager](/help/search-social-commerce/new-ui/set-up/accounts/api-accounts/manager-account-manage.md).

   * Verifica se l’account di rete dell’annuncio include già lo stesso nome di metrica. In caso contrario, rinomina la metrica in modo da poter creare la proprietà corretta a livello di manager.

* Verifica che sia selezionata l’opzione &quot;ibrida&quot; del portfolio e che l’obiettivo abbia ricavi validi.

>[!MORELIKETHIS]
>
>* [Informazioni sugli obiettivi](objective-about.md)
>* [Gestire le metriche di conversione di un inserzionista](/help/search-social-commerce/new-ui/goals/conversions/conversion-metrics-manage.md)
>* [Gestione credenziali per [!DNL Google Ads] account manager](/help/search-social-commerce/new-ui/set-up/accounts/api-accounts/manager-account-manage.md)

<!--
I don't see this yet in new UI:
>* [Upload Search, Social, & Commerce-tracked conversion metrics to [!DNL Google Ads]](/help/search-social-commerce/tools/conversion-metrics-upload-to-google.md)
-->
