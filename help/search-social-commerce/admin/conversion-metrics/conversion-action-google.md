---
title: Crea un'azione di conversione per una conversione  [!DNL Google Ads]  avanzata per i lead
description: Scopri come creare un'azione di conversione  [!DNL Google Ads]  per una conversione avanzata per i lead.
feature: Conversions
source-git-commit: 5eb6ed5b42e74f424fc8499f6df0dbe3f2430ab2
workflow-type: tm+mt
source-wordcount: '459'
ht-degree: 0%

---

# Crea un&#39;azione di conversione per una conversione avanzata [!DNL Google Ads] per i lead

Solo *[!DNL Google Ads]account*

È possibile creare azioni di conversione per [!DNL Google Ads] conversioni avanzate per i lead da monitorare per singoli account [!DNL Google Ads], non per le conversioni a livello di account manager.

1. Nel menu principale, fare clic su **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Conversions]**, che apre la scheda **[!UICONTROL Summary]**.

1. Nella barra degli strumenti sopra la tabella dati, fare clic su ![Crea](/help/search-social-commerce/assets/add.png "Crea").

1. Specificare le [impostazioni dell&#39;azione di conversione](#conversion-action-settings-google).

   1. Selezionare l&#39;account, quindi selezionare il tipo di conversione: *[!UICONTROL Import conversion]*.

   1. Fare clic su **[!UICONTROL Next]**.

   1. Specifica le opzioni dell’azione di conversione.

   1. Fare clic su **[!UICONTROL Generate]**.

1. Leggi le informazioni sulla creazione di un tag di tracciamento per la conversione avanzata per i lead, quindi fai clic su **[!UICONTROL Next]**.

   Crea il tag di conversione e implementalo secondo necessità sui siti web da cui desideri tenere traccia della metrica di conversione. Per istruzioni, vedere:

   * Per utilizzare il tag [!DNL Google], vedere le istruzioni [!DNL Google Ads] per &quot;Configurare le impostazioni tag [!DNL Google]&quot; in &quot;[Configurare conversioni avanzate per i lead con il tag  [!DNL Google] tag](https://support.google.com/google-ads/answer/11347292).&quot;

   * Per utilizzare [!DNL Google Tag Manager], vedere le istruzioni [!DNL Google Ads] per &quot;Configurare le impostazioni dei tag [!DNL Google]&quot; e &quot;Verificare la configurazione e pubblicare il contenitore&quot; in &quot;[Configurare conversioni avanzate per i lead con [!DNL Google Tag Manager]](https://support.google.com/google-ads/answer/11021502?#configure).&quot;

1. Fare clic su **[!UICONTROL Done].**

Dopo aver creato l’azione di conversione e aver implementato un tag di tracciamento della conversione, puoi caricare i dati di conversione offline acquisiti dalla tua organizzazione e attribuirli all’azione di conversione. Consulta &quot;[Caricare dati di conversione offline per conversioni avanzate](/help/search-social-commerce/admin/conversion-metrics/upload-data-offline-conversions.md).&quot;

## Impostazioni delle azioni di conversione {#conversion-action-settings-google}

**[!UICONTROL Select an Account]:** L&#39;account Google Ads applicabile.

**[!UICONTROL Type of Conversion]:** Il tipo di conversione da tenere traccia: Seleziona *[!UICONTROL Import conversion]*. Tutti gli altri tipi vengono utilizzati per creare tag di tracciamento delle conversioni (non azioni di conversione) per altri tipi di conversioni.

**[!UICONTROL Conversion Name]:** Nome univoco per l&#39;azione di conversione.

**\[Categoria conversione\]:** La categoria di conversione, ad esempio *Lead qualificato* o *Iscrizione*.

**\[Tipo azione\]:** Se l&#39;obiettivo è *[!UICONTROL Primary action used for bidding optimization]* o *[!UICONTROL Secondary action not used for bidding optimization]*.

**[!UICONTROL Value]:** Come misurare il [valore di ogni conversione](https://support.google.com/google-ads/answer/13064207):

* *[!UICONTROL Use the same value for each conversion],* che richiede di selezionare una valuta e immettere il valore per ogni conversione.

* *[!UICONTROL Use a different value for each conversion],* che richiede di selezionare una valuta e immettere un valore predefinito per ogni conversione. Puoi modificare il valore predefinito nel tag con un valore specifico per la transazione quando implementi il tag in una pagina web specifica.

* *[!UICONTROL Don't use a value for this conversion action (Not recommended)]*

**[!UICONTROL Count]:** [Quante conversioni conteggiare per clic o interazione](https://support.google.com/google-ads/answer/3438531): *[!UICONTROL Every (Recommended for every purchases because every purchase is valuable)]* o *[!UICONTROL One (Recommended for leads, sign-ups and other conversions because only the first interaction is valuable)]*.

**[!UICONTROL Click Through Conversion Window]:** il numero massimo di giorni dopo un&#39;interazione dell&#39;annuncio per i quali vengono registrate le conversioni. Per le campagne di ricerca, visualizzazione e acquisto, la finestra può essere di 1-90 giorni. Selezionare un numero o selezionare **[!UICONTROL Custom]** e immettere un numero.

**[!UICONTROL View Through Conversion Window]:** il numero massimo di giorni dopo i quali un utente visualizza i tuoi annunci e per i quali vengono registrate le conversioni view-through. Per le campagne di ricerca, visualizzazione e acquisto, la finestra può essere di 1-90 giorni. Selezionare un numero o selezionare **[!UICONTROL Custom]** e immettere un numero.

**[!UICONTROL Attribution Model]:** [Quanto credito riceve ogni interazione pubblicitaria](https://support.google.com/google-ads/answer/6259715?sjid=8211249329930775138): *[!UICONTROL Data driven]* o *[!UICONTROL Last click]*.

>[!MORELIKETHIS]
>
>* [Carica dati di conversione offline per conversioni avanzate](/help/search-social-commerce/admin/conversion-metrics/upload-data-offline-conversions.md)
>* [Implementa [!DNL Google Ads] conversioni avanzate per lead](/help/search-social-commerce/campaign-management/special-workflows/google-enhanced-conversions-leads.md)
