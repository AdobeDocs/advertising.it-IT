---
title: Crea un pubblico di  [!DNL Google Ads] customer match da un elenco e-mail di Adobe Campaign
description: Scopri come creare un pubblico di  [!DNL Google Ads] customer match da un elenco e-mail esistente di Adobe Campaign.
exl-id: 92812af2-ac31-48cd-badf-ea287799bddb
feature: Search Campaign Management
TQID: https://experienceleague.adobe.com/tEiqvHt1QzxhstsKGUsvKGgwm1JYIkv7mGr-Z8kPd0g
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 669
ht-degree: 0%

---

# Crea un pubblico di corrispondenza cliente [!DNL Google Ads] da un elenco e-mail di Adobe Campaign

*[!DNL Google Ads]account idonei solo per la corrispondenza cliente*

È possibile creare un pubblico di [!DNL Google Ads] customer match da un elenco e-mail all&#39;interno di Adobe Campaign impostando un collegamento di account e un flusso di lavoro in [!DNL Campaign].

A tale scopo, è necessario accedere all&#39;istanza [!DNL Campaign] e a un file XML contenente il flusso di lavoro richiesto, che verrà fornito dal team dell&#39;account Adobe. Le istruzioni possono variare per le diverse versioni di [!DNL Campaign]. Se necessario, il team dell&#39;account Adobe può aiutarti a configurare il flusso di lavoro in [!DNL Campaign].

1. Ottieni le credenziali per un account SFTP fornito da Advertising Search, Social e Commerce.

1. In [!DNL Campaign], configurare la consegna dell&#39;elenco e-mail ad Advertising Search, Social e Commerce:

   1. Crea un [account esterno](https://experienceleague.adobe.com/docs/campaign-standard/using/administrating/application-settings/external-accounts.html) per collegare l&#39;account SFTP fornito da Search, Social e Commerce:

      1. Dal menu a sinistra, vai a **\[Adobe Campaign v6\] > [!UICONTROL Platform] >[!UICONTROL External Accounts]**.

      1. Fai clic su ![Crea account](/help/search-social-commerce/assets/campaign-create-account.png "Crea account").

      1. Immettere un&#39;etichetta per l&#39;account e selezionare **[!UICONTROL SFTP]** come tipo di account.

      1. Immettere l&#39;URL e il numero di porta per il server SFTP [!DNL Adobe] e il nome della cartella, il nome utente e la password dell&#39;inserzionista.

      1. Fare clic su **[!UICONTROL Save]**.

   1. In [!DNL Campaign Client], installare il pacchetto di dati che include il flusso di lavoro necessario per inviare i dati e-mail:

      1. Dalla barra dei menu, vai a **[!UICONTROL Tools]> [!UICONTROL Advanced] >[!UICONTROL Import Package]**.

      1. Selezionare **[!UICONTROL Install a package from a file]**, quindi fare clic su **[!UICONTROL Next]**.

      1. Individuare il file del pacchetto dati (`AMO_Workflow.xml`) sul dispositivo o sulla rete, quindi fare clic su **[!UICONTROL Next]**.

      1. Fare clic su **[!UICONTROL Start]** e attendere l&#39;installazione del flusso di lavoro.

   1. Modifica il flusso di lavoro installato per modificare facoltativamente i filtri per la query di dati e per identificare il nuovo nome del pubblico e l’account SFTP esterno:

      1. Vai a **[!UICONTROL Administration]> [!UICONTROL Configuration] > [!UICONTROL Package management] >[!UICONTROL Installed packages]** e apri il pacchetto.

      1. (Facoltativo) Modifica uno dei filtri per i dati:

         * Nel flusso di lavoro, fai doppio clic sull’attività query (ad esempio ForkTransition 1).

         * Modifica le espressioni filtro.

         * Fare clic su **[!UICONTROL Finish]**.

      1. Denomina il segmento:

         * Nel flusso di lavoro fare doppio clic sull&#39;attività **[!UICONTROL Data extraction (File)]**.

         * Nella scheda **[!UICONTROL Data extraction (File)]**, immettere nel campo **[!UICONTROL File name]** il nome del segmento con estensione &quot;`.added`&quot;, ad esempio PaidSubscribers.ADDED.

           Il nome del segmento non deve esistere già. Il nome del segmento distingue tra maiuscole e minuscole e deve essere costituito da caratteri ASCII ma non può includere caratteri di sottolineatura (`_`).

           Tuttavia, se si desidera aggiungere il segmento a un account [!DNL Google Ad] specifico, aggiungere il nome del segmento con un carattere di sottolineatura e l&#39;ID [!UICONTROL User SE Account ID] (Search, Social &amp; Commerce&#39;s ID per l&#39;account [!DNL Google Ads], non l&#39;ID account della rete):

           `_<User SE Account ID>`

           Esempio: Paid_Subscribers_1234.ADDED

           >[!NOTE]
           >
           >Si tratta di un&#39;eccezione alla regola che vieta i caratteri di sottolineatura nel nome del file.

           In caso contrario, il segmento viene aggiunto a tutti gli account [!DNL Google Ads] che Search, Social e Commerce stanno sincronizzando per l&#39;inserzionista.

         * Lascia selezionata l&#39;opzione per **[!UICONTROL Generate an outbound transition]**.

         * Fare clic su **[!UICONTROL Ok]**.

      1. Specifica l’account esterno a cui inviare i dati:

         * Nel flusso di lavoro fare doppio clic sull&#39;attività **[!UICONTROL File Transfer]**.

         * Nella sezione **[!UICONTROL File Transfer]** della scheda **[!UICONTROL Remote server]** selezionare l&#39;opzione per **[!UICONTROL Use an external account]**.

         * Nel campo **[!UICONTROL External account]**, seleziona l’etichetta per l’account esterno creato al passaggio 2.

         * Nel campo **[!UICONTROL Server folder]**, selezionare il valore per il campo [!UICONTROL Account] per l&#39;account esterno.

         * (Facoltativo) Nella scheda **[!UICONTROL Schedule]**, specificare una pianificazione diversa per il trasferimento di file.

           Per impostazione predefinita, il flusso di lavoro viene eseguito alle ore 00:00 (mezzanotte), in modo da garantire che tutti i record vengano elaborati. Per ridurre al minimo la latenza, pianifica l&#39;esecuzione del flusso di lavoro entro il 18:00.

         * Fare clic su **[!UICONTROL Ok]**.

Search, Social e Commerce controllano la directory ogni 30 minuti (alle ore NN:30 e NN:59 nel fuso orario dell&#39;inserzionista) e spostano tutti i file trovati in un&#39;altra posizione, quindi creano automaticamente un pubblico dai dati e lo inviano a Google alle ore 22:00 (22:00). Search, Social e Commerce continuano a verificare la presenza di aggiornamenti (aggiunte e sottrazioni) all&#39;elenco e-mail ogni 30 minuti e aggiornano il pubblico il [!DNL Google Ads] di conseguenza alle 22:00 al giorno.

>[!NOTE]
>
>* Se si caricano più versioni di un file tra un ciclo di elaborazione e l&#39;altro, viene utilizzato il file più recente.
>
>* Search, Social e Commerce non memorizzano i dati dei clienti dagli elenchi e-mail utilizzati per creare o modificare un pubblico [!DNL Google Ads].
>
>* [!DNL Google Ads] potrebbe impiegare del tempo per elaborare gli aggiornamenti a un pubblico.
>
>* Consulta la [[!DNL Google Ads] documentazione sul funzionamento e le limitazioni della corrispondenza con i clienti](https://support.google.com/displayvideo/answer/9539301).

>[!MORELIKETHIS]
>
>* [Informazioni sui tipi di pubblico](audience-about.md)
>* [Crea [!DNL Google Ads] audience corrispondenti ai clienti da [!DNL Adobe] audience](google-audience-from-adobe-audience.md)
>* [Gestire i tipi di pubblico in base ai clienti utilizzando gli elenchi di dati dei clienti](audience-from-customer-data-list.md)
>* [Gestione dei tipi di pubblico di remarketing dinamico](audience-dynamic-remarketing-manage.md)
