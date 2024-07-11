---
title: Abilita il caricamento degli obiettivi nelle reti di annunci
description: Scopri come caricare gli obiettivi per i portfolio ibridi in [!DNL Google Ads] e [!DNL Microsoft Advertising].
exl-id: 09ab0b7a-b6ea-45ad-a82c-2c40d518d2e7
feature: Search Tools
source-git-commit: aaad3eb6cd33f4342c46ffb244227a00fbcb4e44
workflow-type: tm+mt
source-wordcount: '774'
ht-degree: 0%

---

# Abilita il caricamento degli obiettivi nelle reti di annunci

*Inserzionisti con [!DNL Google Ads] e [!DNL Microsoft Advertising] solo account*

*Inserzionisti abilitati solo per l’ottimizzazione ibrida*

Search, Social e Commerce possono caricare gli obiettivi per i portfolio di un account inserzionista in [!DNL Google Ads] e [!DNL Microsoft Advertising] in modo da poterle utilizzare per l’ottimizzazione ibrida. Gli obiettivi caricati sono disponibili come azioni di conversione per gli obiettivi di conversione personalizzati a livello di account e di campagna.

L’abilitazione di questa opzione attiva automaticamente un caricamento per gli obiettivi nei portfolio che contengono campagne con strategie di offerta intelligenti. Search, Social e Commerce creano una conversione sulla rete di annunci per ogni obiettivo applicabile. La conversione rappresenta tutte le metriche di conversione ponderate nell’obiettivo a livello di ID EF (click ID). Per [!DNL Google Ads] clic, l&#39;ID EF è il [!DNL Google Ads] `gclid`; per [!DNL Microsoft Advertising] clic, l&#39;ID EF è il [!DNL Microsoft Advertising] `msclkid`. A causa di questo ID clic, i dati di conversione possono essere mappati sulla parola chiave specifica e sul tempo di clic.

Ciascuna conversione caricata ha uno dei seguenti nomi:

* `O_ACS_OBJ_<network_ID>_<objective_ID>_<network_account_ID>`

  dove `<network_ID>` è l’ID numerico utilizzato da Search, Social e Commerce per la rete di annunci, `<objective_id>` è l&#39;ID obiettivo numerico, e `<network_account_ID>` è l&#39;ID numerico dell&#39;account di ad network o dell&#39;account manager.

* (Vecchio formato che in futuro diventerà obsoleto) `ACS_OBJ_SID_<portfolio_id>_<se_acctid/conversion_manager_se_acctid>`

  dove `<portfolio_id>` è l’ID numerico del portfolio e `<se_acctid/conversion_manager_se_acctid>` è l&#39;ID numerico dell&#39;account di ad network o dell&#39;account manager.

  Il team dell’account Adobe collaborerà con te per migrare i nomi delle azioni di conversione esistenti all’interno della rete di annunci prima che il vecchio formato venga dichiarato obsoleto. Durante il periodo di migrazione, i caricamenti del vecchio e del nuovo formato verranno eseguiti in parallelo. La modellazione e l’ottimizzazione non sono interessate, perché le nuove azioni di conversione appaiono inizialmente con lo stato &quot;secondario&quot; (non ottimizzato) e con 90 giorni di dati di retrocompilazione.

Carica in [!DNL Google Ads] si verifica ogni giorno alle 06:00 nel fuso orario dell&#39;inserzionista. Carica in [!DNL Microsoft Advertising] si verifica ogni giorno alle 09:00 nel fuso orario dell&#39;inserzionista.

>[!IMPORTANT]
>
>Le conversioni tracciate da Google Ads e dal tag UET (Universal Event Tracking) di Microsoft Advertising non vengono ricaricate nelle reti di annunci. Se li includi all’interno di un obiettivo, devi aggiungerli agli obiettivi della campagna nell’editor della rete di annunci.

1. Nel menu principale, fai clic su **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Conversion Upload Setup]**.

1. Seleziona la casella di controllo accanto a **[!UICONTROL Enable Objective Upload]**.

1. (Per gli inserzionisti che [!DNL Google Ads] account che svolgono attività commerciali nello Spazio economico europeo (SEE) o nel Regno Unito (UK); facoltativo) Se hai raccolto il consenso degli utenti di EEA e UK a caricare i loro dati a scopo pubblicitario, seleziona la casella di controllo accanto a **[!UICONTROL If you are doing business in EEA and/or UK, check this box to send consent status as GRANTED for the user data sent to [!DNL Google Ads] for advertising purposes. If left unchecked, we will send consent status as UNSPECIFIED for the user data sent to [!DNL Google Ads] for advertising purposes.]**

1. Clic **[!UICONTROL Save]**.

1. (Se le conversioni vengono tracciate a livello di account manager) [Aggiungi le credenziali per l’account manager](/help/search-social-commerce/admin/manager-accounts.md) a **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**.

1. Verificare che ogni obiettivo, denominato `O_ACS_OBJ_<network_ID>_<objective_ID>_<network_account_ID>` — viene visualizzato entro due giorni sulla rete pubblicitaria.

   In [!DNL Google Ads] editor, cerca il [azioni di conversione](https://support.google.com/google-ads/answer/11461796). In [!DNL Microsoft Advertising] editor, cerca il [obiettivi di conversione](https://help.ads.microsoft.com/#apex/ads/en/56709).

   Se necessario, aggiorna l’intervallo di date per includere la data di caricamento.

## Modalità di calcolo dell&#39;obiettivo ponderato

L’obiettivo ponderato passato alla rete di annunci è la somma di tutti i valori delle metriche raccolti, ad eccezione delle conversioni tracciate da [!DNL Google Ads] o dal [!DNL Microsoft Advertising] tag di tracciamento degli eventi universali (UET). Il valore viene calcolato utilizzando il metodo di attribuzione impostato per l’account Search, Social e Commerce dell’inserzionista.

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
>Puoi visualizzare i dati per gli Adobi Advertising di ricavi ponderati nei rapporti della rete di annunci. Come best practice, confronta i ricavi ponderati con [!DNL Google Ads] &quot;Tutte le conv. (di conv. tempo)&quot; o la [!DNL Microsoft Advertising] metrica &quot;All conv. revenue&quot;, segmentato con la metrica O_ACS_OBJ*.<!--clarify -->

nell’editor del network pubblicitario

## Risoluzione dei problemi relativi agli obiettivi mancanti

Se l’obiettivo — denominato `O_ACS_OBJ_<network_ID>_<objective_ID>_<network_account_ID>` — per uno dei tuoi portfolio non viene visualizzato sulla rete di annunci, quindi verifica quanto segue:

* ([!DNL Google Ads]) Verifica se le conversioni devono essere caricate a livello di account o manager. Se devono essere caricati a livello di manager:

   * Controlla se le credenziali per [!DNL Google Ads] l&#39;account del manager è fornito all&#39;indirizzo **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**. Se necessario, [aggiungi le credenziali per l’account manager](/help/search-social-commerce/admin/manager-accounts.md).

   * Verifica se l’account di rete dell’annuncio include già lo stesso nome di metrica. In caso affermativo, rinomina la metrica in modo da poter creare la proprietà corretta a livello di manager.

* Verifica che sia selezionata l’opzione &quot;ibrida&quot; del portfolio e che l’obiettivo abbia ricavi validi.

>[!MORELIKETHIS]
>
>* [Informazioni sulla gestione delle metriche di conversione di un inserzionista](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md)
>* [Carica metriche di conversione in [!DNL Google Ads]](conversion-metrics-upload-to-google.md)
