---
title: Gestire i sitelink condivisi
description: Scopri come creare e gestire le estensioni di sitelink condivise.
exl-id: 33d52179-b968-4eab-a1b9-b10ff20948e3
feature: Search Campaign Management
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '936'
ht-degree: 0%

---

# Gestire i sitelink condivisi

*[!DNL Google Ads]e [!DNL Microsoft Advertising] solo*

Creare e gestire collegamenti a siti condivisi a livello di account per qualsiasi sito sincronizzato [!DNL Google Ads] o [!DNL Microsoft Advertising] account da [!UICONTROL Extensions] > [!UICONTROL Sitelinks] libreria.

## Creare un sitelink condiviso

1. Nel menu principale, fai clic su **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Nei sottomenu, fare clic su **[!UICONTROL Live]> [!UICONTROL Extensions] >[!UICONTROL Sitelinks]**.

1. Nella barra degli strumenti sopra la tabella dati, fai clic su ![Crea](/help/search-social-commerce/assets/add.png "Crea").

1. Seleziona la rete di annunci e il nome dell’account, quindi fai clic su **[!UICONTROL Continue]**.

1. Inserisci il [impostazioni del sitelink condiviso](#shared-sitelink-settings).

1. Clic **[!UICONTROL Post]**.

Una volta creato un sitelink, puoi [assegnarlo a un account, una campagna o un gruppo di annunci](sitelink-extension-associate.md).

## Modifica impostazioni sitelink condiviso

Puoi modificare un sitelink condiviso alla volta.

1. Nel menu principale, fai clic su **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Nei sottomenu, fare clic su **[!UICONTROL Live]> [!UICONTROL Extensions] >[!UICONTROL Sitelinks]**.

1. Seleziona la casella di controllo accanto al sitelink da modificare.

1. Nella barra degli strumenti sopra la tabella dati, fai clic su ![Modifica](/help/search-social-commerce/assets/edit.png "Modifica").

1. Modifica il [impostazioni del sitelink condiviso](#shared-sitelink-settings).

1. Clic **[!UICONTROL Post]**.

## Eliminare i sitelink condivisi

1. Nel menu principale, fai clic su **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Nei sottomenu, fare clic su **[!UICONTROL Live]> [!UICONTROL Extensions] >[!UICONTROL Sitelinks]**.

1. Selezionare la casella di controllo accanto a ogni sitelink condiviso che si desidera eliminare.

   Per suggerimenti sulla selezione di più righe, vedere &quot;[Seleziona più righe](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).&quot;

1. Nella barra degli strumenti, fai clic su ![Altro](/help/search-social-commerce/assets/more.png "Altro") e seleziona **[!UICONTROL Delete]**.

1. Nel messaggio di conferma, fai clic su **[!UICONTROL Delete]**.

## Impostazioni del sitelink condiviso {#shared-sitelink-settings}

Per ulteriori criteri e motivi di disapprovazione del sitelink, vedi [[!DNL Google Ads]](https://support.google.com/adspolicy/answer/1054210) e [[!DNL Microsoft Advertising]](https://about.ads.microsoft.com/en-us/resources/policies/ad-extensions-policies) requisiti dell&#39;estensione sitelink.

### [!UICONTROL Sitelink]

**[!UICONTROL Link Name]:** Testo da visualizzare per il collegamento. Può contenere fino a 25 caratteri a byte singolo o 12 caratteri a byte doppio. Il testo del collegamento deve essere univoco all’interno dell’account o della campagna.

>[!NOTE]
>
>([!DNL Google Ads]) Il testo esistente di 35 caratteri viene visualizzato negli annunci su desktop e tablet ma non su dispositivi mobili.

**[!UICONTROL Status]:** Stato di visualizzazione del sitelink:  *[!UICONTROL Active]* o *[!UICONTROL Deleted]* (solo sitelink esistenti). Il valore predefinito per i nuovi sitelink è *[!UICONTROL Active]*.

**[!UICONTROL Description Line 1], [!UICONTROL Description Line 2]:** Testo aggiuntivo che il motore di ricerca può visualizzare sotto il testo del collegamento. Per includere una descrizione, immettere i valori per entrambi i campi. Ogni campo di descrizione può includere fino a 35 caratteri a byte singolo o 17 caratteri a byte doppio.

**[!UICONTROL Start Date]:** (Campagne con sitelink legacy esistenti o solo sitelink; facoltativo) La prima data in cui il sitelink può essere visualizzato con gli annunci nella campagna. Il valore predefinito per i nuovi sitelink è il giorno corrente. Per specificare una data di inizio futura, immettere una data nel formato MM/GG/AAAA o M/GG/AAAA oppure fare clic su e selezionare una data.

**[!UICONTROL End Date]:** (Facoltativo) L&#39;ultima data in cui il sitelink può essere visualizzato con gli annunci nella campagna. Per impostazione predefinita, il sitelink può essere visualizzato indefinitamente. Per specificare una data di fine, immettere una data nel formato MM/GG/AAAA o M/GG/AAAA oppure fare clic su e selezionare una data.

**[!UICONTROL Mobile Preference]:** (Facoltativo) Consente alla rete di provare a visualizzare l&#39;estensione dell&#39;annuncio agli utenti di dispositivi mobili anziché agli utenti di desktop o tablet. Per impostazione predefinita, l’opzione non è abilitata e l’estensione dell’annuncio viene visualizzata su qualsiasi tipo di dispositivo.

>[!NOTE]
>
>La rete non garantisce che l’estensione dell’annuncio verrà visualizzata sul tipo di dispositivo preferito.

### [!UICONTROL Tracking URLs]

**[!UICONTROL Base URL]** L’URL della pagina di destinazione a cui vengono indirizzati gli utenti dei motori di ricerca quando fanno clic sull’annuncio. Includi eventuali parametri che determinano il contenuto della pagina. Se inserisci un valore, questo sovrascrive l’URL di base dell’annuncio.

Dopo aver salvato il record, l’URL di base include tutti i parametri di aggiunta configurati per la campagna o l’account.

>[!NOTE]
>
>* (Account con URL finali) L’URL di base può contenere reindirizzamenti all’interno del dominio o del sottodominio della pagina di destinazione, ma non reindirizzamenti all’esterno del dominio della pagina di destinazione. La rete di annunci estrae il dominio da questo URL e aggiunge eventuali percorsi di visualizzazione facoltativi per l’annuncio, per creare l’URL di visualizzazione per l’annuncio.
>* ([!DNL Google Ads]) Ogni sitelink in una campagna o in un gruppo di annunci deve avere una pagina di destinazione univoca e il contenuto di ogni pagina di destinazione sitelink deve avere circa l&#39;80% di contenuto univoco. Ad esempio, non puoi avere sitelink con collegamenti a più ancoraggi all&#39;interno della stessa pagina.
>* ([!DNL Google Ads]) Evita l&#39;uso di macro, che non vengono sostituite dai clic provenienti da origini che abilitano il tracciamento parallelo. Se l’inserzionista deve utilizzare delle macro, il Team dell’account Adobe deve collaborare con l’Assistenza clienti o con il team di implementazione per aggiungerle.

**[!UICONTROL Tracking Template]:** (Facoltativo) Il modello di tracciamento o l’URL di tracciamento, che specifica tutti i reindirizzamenti e i parametri di tracciamento dei domini di destinazione e incorpora anche l’URL finale/della pagina di destinazione in un parametro. Esempio: `{lpurl}?source={network}&id=5` o `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5` per includere un reindirizzamento.

* Ad Adobe Advertising, il tracciamento delle conversioni, che viene applicato quando le impostazioni della campagna includono &quot;[!UICONTROL EF Redirect]&quot; e &quot;Caricamento automatico&quot;, Ricerca, Social e Commerce inseriscono automaticamente un prefisso nel codice di tracciamento dei clic quando si salva il record.

* Per i parametri supportati per incorporare l’URL finale, consulta la sezione ([!DNL Microsoft Advertising] solo ) [[!DNL Microsoft Advertising] documentazione](https://help.ads.microsoft.com/#apex/3/en/56799) o ([!DNL Google Ads] solo) i parametri &quot;Solo modello di tracciamento&quot; nella sezione su &quot;Disponibile [!DNL ValueTrack] Parameters&quot; nella sezione [[!DNL Google Ads] documentazione](https://support.google.com/google-ads/answer/6305348).

* Facoltativamente, puoi includere i parametri URL ed eventuali parametri personalizzati definiti per la campagna, separati da e commerciali (&amp;), ad esempio `{lpurl}?matchtype={matchtype}&device={device}`.

* Facoltativamente, puoi aggiungere reindirizzamenti e tracciamento di terze parti.

>[!NOTE]
>
>* Quando le impostazioni della campagna includono &quot;[!UICONTROL EF Redirect]&quot; e &quot;[!UICONTROL Auto Upload],&quot; Search, Social e Commerce aggiunge automaticamente il prefisso al proprio codice di reindirizzamento e di tracciamento quando si salva il record.
>* Il modello di tracciamento al livello più granulare sostituisce i valori a tutti i livelli superiori. Ad esempio, se sia le impostazioni dell’account che quelle delle parole chiave includono un valore, questo viene applicato.
>* ([!DNL Google Ads]) Se aggiorni un modello di tracciamento a livello di sitelink o di parola chiave, gli annunci pertinenti vengono nuovamente inviati per la revisione. Puoi aggiornare i modelli di tracciamento a livello di account, campagna o gruppo di annunci senza inviare nuovamente gli annunci per l’approvazione.
>* ([!DNL Microsoft Advertising]) Puoi aggiornare i modelli di tracciamento a qualsiasi livello senza inviare nuovamente gli annunci per l’approvazione.
>* Per [!DNL Google Ads], evita di utilizzare macro che non vengono sostituite dai clic provenienti da origini che abilitano il tracciamento parallelo. Se l’inserzionista deve utilizzare delle macro, l’Account Team Adobe deve collaborare con l’Assistenza clienti o con il team di implementazione per aggiungerle.

>[!MORELIKETHIS]
>
>* [Informazioni sulle estensioni sitelink](sitelink-extension-about.md)
>* [Associa collegamenti a siti condivisi ad account, campagne e gruppi di annunci](sitelink-extension-associate.md)
