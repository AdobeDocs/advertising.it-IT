---
title: Crea un pubblico di  [!DNL Google Ads] customer match da un elenco e-mail di Adobe Campaign
description: Scopri come creare un pubblico di  [!DNL Google Ads] customer match da un elenco e-mail esistente di Adobe Campaign.
exl-id: 92812af2-ac31-48cd-badf-ea287799bddb
feature: Search Campaign Management
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '670'
ht-degree: 0%

---

# Crea un pubblico di corrispondenza cliente [!DNL Google Ads] da un elenco e-mail di Adobe Campaign

*[!DNL Google Ads]account idonei solo per la corrispondenza cliente*

È possibile creare un pubblico di [!DNL Google Ads] customer match da un elenco e-mail all&#39;interno di Adobe Campaign impostando un collegamento di account e un flusso di lavoro in [!DNL Campaign].

A tale scopo, è necessario accedere all&#39;istanza [!DNL Campaign] e a un file XML contenente il flusso di lavoro richiesto, che verrà fornito dal team dell&#39;account Adobe. Le istruzioni possono variare per le diverse versioni di [!DNL Campaign]. Se necessario, il team dell&#39;account Adobe può aiutarti a configurare il flusso di lavoro in [!DNL Campaign].

1. Ottieni le credenziali per un account SFTP fornito da Advertising Search, Social e Commerce.

1. In [!DNL Campaign], configurare la consegna dell&#39;elenco e-mail ad Advertising Search, Social e Commerce:

   1. Crea un [account esterno](https://experienceleague.adobe.com/docs/campaign-standard/using/administrating/application-settings/external-accounts.html?lang=it) per collegare l&#39;account SFTP fornito da Search, Social e Commerce:

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

         * Nella sezione **[!UICONTROL Remote server]** della scheda **[!UICONTROL File Transfer]** selezionare l&#39;opzione per **[!UICONTROL Use an external account]**.

         * Nel campo **[!UICONTROL External account]**, seleziona l’etichetta per l’account esterno creato al passaggio 2.

         * Nel campo **[!UICONTROL Server folder]**, selezionare il valore per il campo [!UICONTROL Account] per l&#39;account esterno.

         * (Facoltativo) Nella scheda **[!UICONTROL Schedule]**, specificare una pianificazione diversa per il trasferimento di file.

           Per impostazione predefinita, il flusso di lavoro viene eseguito alle 00:00 (mezzanotte), in modo da garantire che tutti i record vengano elaborati. Per ridurre al minimo la latenza, pianifica l’esecuzione del flusso di lavoro entro le 18:00.

         * Fare clic su **[!UICONTROL Ok]**.

Search, Social &amp; Commerce controlla la directory ogni 30 minuti (alle NN:30 e NN:59 nel fuso orario dell’inserzionista) e sposta i file che trova in un’altra posizione, quindi crea automaticamente un pubblico dai dati e lo invia a Google alle 22:00 (22:00). Search, Social e Commerce continuano a verificare la presenza di aggiornamenti (aggiunte e sottrazioni) all&#39;elenco e-mail ogni 30 minuti e aggiornano il pubblico il [!DNL Google Ads] di conseguenza alle 22:00 ogni giorno.

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
