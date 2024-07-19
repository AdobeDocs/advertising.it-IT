---
title: Gestire i sitelink condivisi
description: Scopri come creare e gestire le estensioni di sitelink condivise.
exl-id: e510f53b-f48c-4129-887c-351a840b8398
feature: Search Campaign Management
source-git-commit: c3b8e387cfc38d195e77761791e689fd094d8f39
workflow-type: tm+mt
source-wordcount: '928'
ht-degree: 0%

---

# Gestire i sitelink condivisi

Solo *[!DNL Google Ads]e [!DNL Microsoft Advertising]*

Crea e gestisci sitelink condivisi a livello di account per qualsiasi account [!DNL Google Ads] o [!DNL Microsoft Advertising] sincronizzato dalla libreria [!UICONTROL Extensions] > [!UICONTROL Sitelinks].

## Creare un sitelink condiviso

1. Nel menu principale, fare clic su **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Nei sottomenu, fare clic su **[!UICONTROL Live]> [!UICONTROL Extensions] >[!UICONTROL Sitelinks]**.

1. Nella barra degli strumenti sopra la tabella dati, fare clic su ![Crea](/help/search-social-commerce/assets/add.png "Crea").

1. Selezionare la rete di annunci e il nome account, quindi fare clic su **[!UICONTROL Continue]**.

1. Immetti le [impostazioni del collegamento a sito condiviso](#shared-sitelink-settings).

1. Fare clic su **[!UICONTROL Post]**.

Dopo aver creato un sitelink, puoi [assegnarlo a un account, una campagna o un gruppo di annunci](sitelink-extension-associate.md).

## Modifica impostazioni sitelink condiviso

Puoi modificare un sitelink condiviso alla volta.

1. Nel menu principale, fare clic su **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Nei sottomenu, fare clic su **[!UICONTROL Live]> [!UICONTROL Extensions] >[!UICONTROL Sitelinks]**.

1. Seleziona la casella di controllo accanto al sitelink da modificare.

1. Nella barra degli strumenti sopra la tabella dati, fare clic su ![Modifica](/help/search-social-commerce/assets/edit.png "Modifica").

1. Modifica le [impostazioni di collegamento a sito condiviso](#shared-sitelink-settings).

1. Fare clic su **[!UICONTROL Post]**.

## Eliminare i sitelink condivisi

1. Nel menu principale, fare clic su **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Nei sottomenu, fare clic su **[!UICONTROL Live]> [!UICONTROL Extensions] >[!UICONTROL Sitelinks]**.

1. Selezionare la casella di controllo accanto a ogni sitelink condiviso che si desidera eliminare.

   Per suggerimenti sulla selezione di più righe, vedere &quot;[Selezionare più righe](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

1. Nella barra degli strumenti, fare clic su ![Altro](/help/search-social-commerce/assets/more.png "Altro") e selezionare **[!UICONTROL Delete]**.

1. Nel messaggio di conferma, fare clic su **[!UICONTROL Delete]**.

## Impostazioni del sitelink condiviso {#shared-sitelink-settings}

Per ulteriori criteri e motivi di disapprovazione del sitelink, vedere i requisiti di estensione del sitelink [[!DNL Google Ads]](https://support.google.com/adspolicy/answer/1054210) e [[!DNL Microsoft Advertising]](https://help.ads.microsoft.com/#apex/ads/en/ext60206).

### [!UICONTROL Sitelink]

**[!UICONTROL Link Name]:** Testo da visualizzare per il collegamento. Può contenere fino a 25 caratteri a byte singolo o 12 caratteri a byte doppio. Il testo del collegamento deve essere univoco all’interno dell’account o della campagna.

>[!NOTE]
>
>([!DNL Google Ads]) Il testo esistente di 35 caratteri viene visualizzato negli annunci di desktop e tablet, ma non nei dispositivi mobili.

**[!UICONTROL Status]:** Lo stato di visualizzazione del sitelink: *[!UICONTROL Active]* o *[!UICONTROL Deleted]* (solo sitelink esistenti). Il valore predefinito per i nuovi sitelink è *[!UICONTROL Active]*.

**[!UICONTROL Description Line 1], [!UICONTROL Description Line 2]:** Testo aggiuntivo che il motore di ricerca potrebbe visualizzare sotto il testo del collegamento. Per includere una descrizione, immettere i valori per entrambi i campi. Ogni campo di descrizione può includere fino a 35 caratteri a byte singolo o 17 caratteri a byte doppio.

**[!UICONTROL Start Date]:** (solo campagne con sitelink legacy esistenti o senza sitelink; facoltativo) La prima data in cui il sitelink può essere visualizzato con gli annunci nella campagna. Il valore predefinito per i nuovi sitelink è il giorno corrente. Per specificare una data di inizio futura, immettere una data nel formato MM/GG/AAAA o M/GG/AAAA oppure fare clic su   e seleziona una data.

**[!UICONTROL End Date]:** (facoltativo) ultima data in cui il sitelink può essere visualizzato con gli annunci nella campagna. Per impostazione predefinita, il sitelink può essere visualizzato indefinitamente. Per specificare una data di fine, immettere una data nel formato MM/GG/AAAA o M/GG/AAAA oppure fare clic su   e seleziona una data.

**[!UICONTROL Mobile Preference]:** (facoltativo) consente alla rete di provare a visualizzare l&#39;estensione dell&#39;annuncio agli utenti di dispositivi mobili anziché agli utenti di desktop o tablet. Per impostazione predefinita, l’opzione non è abilitata e l’estensione dell’annuncio viene visualizzata su qualsiasi tipo di dispositivo.

>[!NOTE]
>
>La rete non garantisce che l’estensione dell’annuncio verrà visualizzata sul tipo di dispositivo preferito.

### [!UICONTROL Tracking URLs]

**[!UICONTROL Base URL]** L&#39;URL della pagina di destinazione a cui vengono indirizzati gli utenti dei motori di ricerca quando fanno clic sull&#39;annuncio. Includi eventuali parametri che determinano il contenuto della pagina. Se inserisci un valore, questo sovrascrive l’URL di base dell’annuncio.

Dopo aver salvato il record, l’URL di base include tutti i parametri di aggiunta configurati per la campagna o l’account.

>[!NOTE]
>
>* (Account con URL finali) L’URL di base può contenere reindirizzamenti all’interno del dominio o del sottodominio della pagina di destinazione, ma non reindirizzamenti all’esterno del dominio della pagina di destinazione. La rete di annunci estrae il dominio da questo URL e aggiunge eventuali percorsi di visualizzazione facoltativi per l’annuncio, per creare l’URL di visualizzazione per l’annuncio.
>* ([!DNL Google Ads]) Ogni sitelink in una campagna o in un gruppo di annunci deve avere una pagina di destinazione univoca e il contenuto di ogni pagina di destinazione di sitelink deve avere circa l&#39;80% di contenuto univoco. Ad esempio, non puoi avere sitelink con collegamenti a più ancoraggi all&#39;interno della stessa pagina.
>* ([!DNL Google Ads]) Evitare l&#39;utilizzo di macro, che non vengono sostituite dai clic provenienti da origini che abilitano il tracciamento parallelo. Se l’inserzionista deve utilizzare delle macro, il Team dell’account Adobe deve collaborare con l’Assistenza clienti o con il team di implementazione per aggiungerle.

**[!UICONTROL Tracking Template]:** (Facoltativo) Il modello di tracciamento o l&#39;URL di tracciamento, che specifica tutti i reindirizzamenti del dominio di destinazione e i parametri di tracciamento e incorpora anche l&#39;URL della pagina finale/di destinazione in un parametro. Esempio: `{lpurl}?source={network}&id=5` o `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5` per includere un reindirizzamento.

* Ad Adobe Advertising, il tracciamento delle conversioni, che viene applicato quando le impostazioni della campagna includono &quot;[!UICONTROL EF Redirect]&quot; e &quot;Caricamento automatico&quot;, Ricerca, Social e Commerce, al salvataggio del record aggiunge automaticamente i prefissi al proprio codice di tracciamento dei clic.

* Per i parametri supportati per incorporare l&#39;URL finale, vedere i parametri [[!DNL Microsoft Advertising] documentation](https://help.ads.microsoft.com/#apex/3/en/56799) o ([!DNL Google Ads] only) &quot;Tracking template only&quot; nella sezione su &quot;Available [!DNL ValueTrack] Parameters&quot; in [[!DNL Google Ads] documentation](https://support.google.com/google-ads/answer/6305348).[!DNL Microsoft Advertising]

* Facoltativamente, puoi includere i parametri URL ed eventuali parametri personalizzati definiti per la campagna, separati da e commerciali (&amp;), ad esempio `{lpurl}?matchtype={matchtype}&device={device}`.

* Facoltativamente, puoi aggiungere reindirizzamenti e tracciamento di terze parti.

>[!NOTE]
>
>* Quando le impostazioni della campagna includono &quot;[!UICONTROL EF Redirect]&quot; e &quot;[!UICONTROL Auto Upload]&quot;, Search, Social e Commerce applicano automaticamente i prefissi al proprio codice di reindirizzamento e di tracciamento quando si salva il record.
>* Il modello di tracciamento al livello più granulare sostituisce i valori a tutti i livelli superiori. Ad esempio, se sia le impostazioni dell’account che quelle delle parole chiave includono un valore, questo viene applicato.
>* ([!DNL Google Ads]) Se si aggiorna un modello di tracciamento a livello di sitelink o di parola chiave, gli annunci pertinenti vengono nuovamente inviati per la revisione. Puoi aggiornare i modelli di tracciamento a livello di account, campagna o gruppo di annunci senza inviare nuovamente gli annunci per l’approvazione.
>* ([!DNL Microsoft Advertising]) È possibile aggiornare i modelli di tracciamento a qualsiasi livello senza inviare nuovamente gli annunci per l&#39;approvazione.
>* Per [!DNL Google Ads], evitare l&#39;utilizzo di macro, che non vengono sostituite dai clic provenienti da origini che abilitano il tracciamento parallelo. Se l’inserzionista deve utilizzare delle macro, l’Account Team Adobe deve collaborare con l’Assistenza clienti o con il team di implementazione per aggiungerle.

>[!MORELIKETHIS]
>
>* [Informazioni sulle estensioni sitelink](sitelink-extension-about.md)
>* [Associa collegamenti a siti condivisi ad account, campagne e gruppi di annunci](sitelink-extension-associate.md)
