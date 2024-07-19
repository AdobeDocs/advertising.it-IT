---
title: Crea un tag di conversione per  [!DNL Google Ads]
description: Scopri come creare un tag di conversione  [!DNL Google Ads] .
feature: Conversions
exl-id: 214611f0-bd38-499e-a7de-3a5878995fb5
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '371'
ht-degree: 0%

---

# Crea un tag di conversione per [!DNL Google Ads]

È possibile creare tag di conversione per tenere traccia delle nuove conversioni per singoli account [!DNL Google Ads], non a livello di account manager.

Per generare tag di conversione per le conversioni esistenti, utilizza l’editor della rete di annunci.

1. Nel menu principale, fare clic su **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Conversions]**.

1. Nella barra degli strumenti sopra la tabella dati, fare clic su ![Crea](/help/search-social-commerce/assets/add.png "Crea").

1. Specificare le [impostazioni tag di conversione](#conversion-tag-settings-google).

   1. Selezionare l&#39;account, quindi selezionare il tipo di conversione.

   1. Fare clic su **[!UICONTROL Next]**.

   1. Specifica le opzioni di conversione.

   1. Fare clic su **[!UICONTROL Generate]**.

1. Copia il tag di conversione e implementalo sui siti web da cui desideri tenere traccia della metrica di conversione.

   Vedere &quot;Installazione del tag [!DNL Google]&quot; nella Guida di [!DNL Google Ads] per &quot;[2. Configura il tuo tag Google](https://support.google.com/google-ads/answer/12215519).&quot;

1. Fare clic su **[!UICONTROL Done].**

Una volta aggiunti i tag al sito Web e che iniziano a essere attivati, [!DNL Google Ads] registra le conversioni nel sito Web. Search, Social e Commerce sincronizzano le conversioni ogni giorno. Per ulteriori informazioni sui dati sincronizzati, vedere &quot;[[!DNL Google Ads] dati di conversione in Search, Social e Commerce](/help/search-social-commerce/campaign-management/introduction/google-conversion-data.md).

## Impostazioni dei tag di conversione {#conversion-tag-settings-google}

**[!UICONTROL Select an Account]:** L&#39;account Google Ads applicabile.

**[!UICONTROL Type of Conversion]:** Tipo di conversione da tenere traccia: *[!UICONTROL Click on a webpage element]*, *[!UICONTROL Calls to a phone number on your website]* o *[!UICONTROL Clicks to your number on your mobile website]*.

**[!UICONTROL Conversion Name]:** Nome univoco per la metrica di conversione.

**\[Categoria conversione\]:** La categoria di conversione. Le categorie disponibili variano in base al tipo di conversione. Per *[!UICONTROL Calls to a phone number on your website]* e *[!UICONTROL Clicks to your number on your mobile website]*, &quot;[!UICONTROL Phone Call Lead]&quot; è selezionato per impostazione predefinita.

**\[Tipo azione\]:** Se l&#39;obiettivo è *[!UICONTROL Primary action used for bidding optimization]* o *[!UICONTROL Secondary action not used for bidding optimization]*.

**[!UICONTROL Value]:** Come misurare il [valore di ogni conversione](https://support.google.com/google-ads/answer/3419241):

* *[!UICONTROL Use the same value for each conversion],* che richiede di selezionare una valuta e immettere il valore per ogni conversione.

* *[!UICONTROL Use a different value for each conversion],* che richiede di selezionare una valuta e immettere un valore predefinito per ogni conversione. Puoi modificare il valore predefinito nel tag con un valore specifico per la transazione quando implementi il tag in una pagina web specifica.

* *[!UICONTROL Don't use a value for this conversion action (Not recommended)]*

**[!UICONTROL Count]:** [Quante conversioni conteggiare per clic o interazione](https://support.google.com/google-ads/answer/3438531): *[!UICONTROL Every (Recommended for every purchases because every purchase is valuable)]* o *[!UICONTROL One (Recommended for leads, sign-ups and other conversions because only the first interaction is valuable)]*.

**[!UICONTROL Click Through Conversion Window]:** il numero massimo di giorni dopo un&#39;interazione dell&#39;annuncio per i quali vengono registrate le conversioni. Per le campagne di ricerca, visualizzazione e acquisto, la finestra può essere di 1-90 giorni. Selezionare un numero o selezionare **[!UICONTROL Custom]** e immettere un numero.

**[!UICONTROL View Through Conversion Window]:** il numero massimo di giorni dopo i quali un utente visualizza i tuoi annunci e per i quali vengono registrate le conversioni view-through. Per le campagne di ricerca, visualizzazione e acquisto, la finestra può essere di 1-90 giorni. Selezionare un numero o selezionare **[!UICONTROL Custom]** e immettere un numero.

**[!UICONTROL Attribution Model]:** [Quanto credito ottiene ogni interazione pubblicitaria](https://support.google.com/google-ads/answer/6259715?sjid=8211249329930775138): *[!UICONTROL Data driven]*, *[!UICONTROL Last click]*, *[!UICONTROL First click]*, *[!UICONTROL Linear]*, *[!UICONTROL Time decay]* o *[!UICONTROL Position based]*.

>[!MORELIKETHIS]
>
>* [[!DNL Google Ads] dati di conversione in Search, Social e Commerce](/help/search-social-commerce/campaign-management/introduction/google-conversion-data.md)
