---
title: Creare un tag di conversione per [!DNL Google Ads]
description: Scopri come creare un [!DNL Google Ads] tag di conversione.
feature: Conversions
source-git-commit: 395421c69214c3b0370523909047a924af23ea55
workflow-type: tm+mt
source-wordcount: '379'
ht-degree: 0%

---

# Creare un tag di conversione per [!DNL Google Ads]

Puoi creare tag di conversione per tenere traccia delle nuove conversioni per singoli utenti [!DNL Google Ads] account, non tracciati a livello di account manager.

Per generare tag di conversione per le conversioni esistenti, utilizza l’editor della rete di annunci.

1. Nel menu principale, fai clic su **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Conversions]**.

1. Nella barra degli strumenti sopra la tabella dati, fai clic su ![Crea](/help/search-social-commerce/assets/add.png "Crea").

1. Specifica la [impostazioni tag di conversione](#conversion-tag-settings-google).

   1. Selezionare l&#39;account, quindi selezionare il tipo di conversione.

   1. Clic **[!UICONTROL Next]**.

   1. Specifica le opzioni di conversione.

   1. Clic **[!UICONTROL Generate]**.

1. Copia il tag di conversione e implementalo sui siti web da cui desideri tenere traccia della metrica di conversione.

   Consulta &quot;Installazione di [!DNL Google] tag&quot; nella [!DNL Google Ads] Aiuto per &quot;[2. Configurare il tag Google](https://support.google.com/google-ads/answer/12215519).&quot;

1. Clic **[!UICONTROL Done].**

Una volta aggiunti i tag al sito web e che iniziano a essere attivati, [!DNL Google Ads] registra le conversioni sul sito web. Search, Social e Commerce sincronizzano le conversioni ogni giorno. Per ulteriori informazioni sui dati sincronizzati, vedi &quot;[[!DNL Google Ads] dati di conversione in Search, Social e Commerce](/help/search-social-commerce/campaign-management/introduction/google-conversion-data.md).

## Impostazioni dei tag di conversione {#conversion-tag-settings-google}

**[!UICONTROL Select an Account]:** L’account Google Ads applicabile.

**[!UICONTROL Type of Conversion]:** Tipo di conversione da tracciare: *[!UICONTROL Click on a webpage element]*, *[!UICONTROL Calls to a phone number on your website]*, o *[!UICONTROL Clicks to your number on your mobile website]*.

**[!UICONTROL Conversion Name]:** Un nome univoco per la metrica di conversione.

**\[Categoria conversione\]:** La categoria di conversione. Le categorie disponibili variano in base al tipo di conversione. Per *[!UICONTROL Calls to a phone number on your website]* e *[!UICONTROL Clicks to your number on your mobile website]*, &quot;[!UICONTROL Phone Call Lead]&quot; è selezionato per impostazione predefinita.

**\[Tipo azione\]:** Se l’obiettivo è un *[!UICONTROL Primary action used for bidding optimization]* o un *[!UICONTROL Secondary action not used for bidding optimization]*.

**[!UICONTROL Value]:** Come misurare il [valore di ciascuna conversione](https://support.google.com/google-ads/answer/3419241):

* *[!UICONTROL Use the same value for each conversion],* che richiede di selezionare una valuta e di inserire il valore per ogni conversione.

* *[!UICONTROL Use a different value for each conversion],* che richiede di selezionare una valuta e di immettere un valore predefinito per ogni conversione. Puoi modificare il valore predefinito nel tag con un valore specifico per la transazione quando implementi il tag in una pagina web specifica.

* *[!UICONTROL Don't use a value for this conversion action (Not recommended)]*

**[!UICONTROL Count]:** [Quante conversioni contare per clic o interazione](https://support.google.com/google-ads/answer/3438531): *[!UICONTROL Every (Recommended for every purchases because every purchase is valuable)]* o *[!UICONTROL One (Recommended for leads, sign-ups and other conversions because only the first interaction is valuable)]*.

**[!UICONTROL Click Through Conversion Window]:** Il numero massimo di giorni dopo un’interazione pubblicitaria per i quali vengono registrate le conversioni. Per le campagne di ricerca, visualizzazione e acquisto, la finestra può essere di 1-90 giorni. Seleziona un numero o seleziona **[!UICONTROL Custom]** e inserisci un numero.

**[!UICONTROL View Through Conversion Window]:** Il numero massimo di giorni dopo i quali un utente visualizza gli annunci per i quali vengono registrate le conversioni view-through. Per le campagne di ricerca, visualizzazione e acquisto, la finestra può essere di 1-90 giorni. Seleziona un numero o seleziona **[!UICONTROL Custom]** e inserisci un numero.

**[!UICONTROL Attribution Model]:** [Quanto credito ottiene ogni interazione pubblicitaria](https://support.google.com/google-ads/answer/6259715?sjid=8211249329930775138): *[!UICONTROL Data driven]*, *[!UICONTROL Last click]*, *[!UICONTROL First click]*, *[!UICONTROL Linear]*, *[!UICONTROL Time decay]*, o *[!UICONTROL Position based]*.

>[!MORELIKETHIS]
>
>* [[!DNL Google Ads] dati di conversione in Search, Social e Commerce](/help/search-social-commerce/campaign-management/introduction/google-conversion-data.md)
