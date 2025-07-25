---
title: Gestire i modelli di annunci per i feed di inventario
description: Scopri come gestire i modelli di annunci tramite i quali i dati di inventario possono essere elaborati per gestire la struttura dei conti e distribuire annunci dinamici.
exl-id: b0e540cf-8735-4812-9df5-58f488a25ba5
feature: Search Inventory Feeds
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '1423'
ht-degree: 0%

---

# Gestire i modelli di annunci per i feed di inventario

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] (elimina solo azioni) e [!DNL Yandex] account solo*

Prima o dopo il caricamento dei dati, puoi creare modelli di annunci specifici per i motori di ricerca tramite i quali elaborare i dati. È possibile creare modelli per annunci di testo e annunci di testo espansi/estesi, [!DNL Google Ads] e [!DNL Microsoft Advertising] annunci di ricerca responsive e per [!DNL Google Ads] e [!DNL Microsoft Advertising] annunci di acquisto.

È possibile associare ogni modello a un file di feed, all&#39;account [!DNL Google Merchant Center] o all&#39;account [!DNL Microsoft Merchant Center], nonché associare più modelli allo stesso file di feed o account. Un modello di annuncio può includere variabili che vengono sostituite con colonne di dati effettive da un file caricato o da un account. Nella maggior parte dei casi, le variabili possono anche includere [un gruppo di modificatori](/help/search-social-commerce/campaign-management/inventory-feeds/modifiers-manage.md) configurato in Search, Social e Commerce per creare più annunci, parole chiave, campagne o gruppi di annunci per ogni riga applicabile nel file di dati. Le opzioni del modello consentono di creare una nuova struttura dell’account (campagne, gruppi di annunci, parole chiave) per gli annunci o di mappare gli annunci alla struttura dell’account esistente.

Oltre a creare nuovi modelli da zero, è possibile crearne di nuovi duplicando quelli esistenti e modificando quelli esistenti.

Dopo aver creato un modello e averlo associato a un file di feed dati o a un account del centro commerciale, è possibile propagare i dati nel file tramite il modello per creare i dati della campagna e la struttura dell’account, creando facoltativamente un file di bulksheet per la revisione o per la pubblicazione immediata nella rete di annunci.

Qualsiasi modello può essere attivato, messo in pausa o eliminato. I dati dei feed possono essere propagati automaticamente solo tramite modelli attivi. Tuttavia, è possibile propagare manualmente i dati tramite un modello in pausa.

## Creare, clonare o modificare un modello di feed

Crea modelli separati per annunci di testo e annunci di testo espansi/estesi, annunci di ricerca responsive, [!DNL Google Ads] annunci di acquisto e [!DNL Microsoft Advertising] annunci di acquisto.

1. Nel menu principale, fare clic su **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**, che consente di aprire la scheda [!UICONTROL Templates].

1. Effettuare una delle seguenti operazioni:

   * Per creare un modello da zero, fare clic su **[!UICONTROL Create/Clone]** nella barra degli strumenti sopra la tabella dati, quindi selezionare la rete di annunci applicabile.

   * Per clonare un modello esistente:

      1. Selezionare la casella di controllo accanto al modello da copiare.

      1. Nella barra degli strumenti sopra la tabella dati, fare clic su **[!UICONTROL Create/Clone]**, quindi selezionare la rete di annunci applicabile.

   * Per modificare un modello esistente, fare clic su ![Visualizza/modifica impostazioni](/help/search-social-commerce/assets/settings.png "Visualizza/modifica impostazioni") accanto al nome del modello.

1. Specifica le impostazioni per il [modello di annuncio testuale](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/template-text-rsa.md), [[!DNL Google Ads] modello di annuncio acquisti](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/template-google-shopping.md) o [[!DNL Microsoft Advertising] modello di annuncio acquisti](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/template-microsoft-shopping.md):

   1. Nella parte superiore della finestra delle impostazioni del modello, specifica il nome del modello e l’account applicabile.

      Quando cloni un modello esistente, rinomina il nuovo modello in modo che gli annunci creati dal nuovo modello non siano associati agli annunci creati dal modello di origine.

   1. (Facoltativo) Nella colonna a sinistra, specifica il file di feed del prodotto o l’account del centro commerciale i cui dati verranno propagati tramite il modello:

      * (Per i file di feed del prodotto) Per selezionare un file caricato in precedenza, fai clic su ![freccia giù](/help/search-social-commerce/assets/arrow-down-dropdown.png "freccia giù") e seleziona un file dall&#39;elenco dei file di feed disponibili. Per caricare un nuovo file, specificare il file immettendo il percorso completo e il nome del file oppure facendo clic su **[!UICONTROL Browse]** per individuare il file sul dispositivo o sulla rete, quindi fare clic su **[!UICONTROL Upload]**.

      * (Per un account del centro commerciale sincronizzato) Seleziona il nome dell’account.

      Vengono visualizzate le colonne per il file o l&#39;account selezionato.

   1. Nella scheda **[!UICONTROL Account Structure]** specificare le impostazioni della struttura dell&#39;account.

   1. (Solo annunci di testo) Fai clic sulla scheda **[!UICONTROL Keywords]** e specifica le impostazioni delle parole chiave.

   1. (Solo testo e annunci di ricerca responsive) Fare clic sulla scheda **[!UICONTROL Ads]** ed eseguire una delle operazioni seguenti:

      >[!NOTE]
      >
      >* Puoi includere fino a quattro modelli di varianti di annunci per modello di annunci di testo standard, cinque modelli di varianti di annunci per modello di annunci di testo espanso/esteso e tre modelli di varianti di annunci per modello di annunci di ricerca responsive.
      >* Ogni gruppo di annunci può includere fino a tre annunci di ricerca responsive abilizzati.
      >* Non è possibile modificare le varianti di annunci di testo standard esistenti e i modelli esistenti non generano più annunci di testo standard.
      >* Se modifichi un modello di variante di annuncio, gli annunci esistenti possono essere eliminati e nuovi possono essere creati quando propaghi i dati tramite il modello, [a seconda del tipo di annuncio e della rete di annunci](/help/search-social-commerce/campaign-management/inventory-feeds/when-are-components-created-deleted.md).

      * Per aggiungere una variante di annuncio, effettua le seguenti operazioni:

         1. Fare clic su **[!UICONTROL Add Ad Variation]** per creare un annuncio di testo, su **[!UICONTROL Add ETA Variation]** per creare un annuncio di testo espanso/esteso o su **[!UICONTROL Add RSA Variation]** per creare un annuncio di testo reattivo.

            Una volta specificato il tipo di annuncio, è possibile crearlo solo con il modello.

         1. Specifica le impostazioni dell’annuncio.

            Per gli annunci di ricerca responsive, puoi includere 3-15 titoli e 2-4 descrizioni.

         1. (Facoltativo) Per precompilare tutti i campi della copia dell&#39;annuncio alternativi con il testo dei campi della copia dell&#39;annuncio originale, selezionare la casella di controllo accanto a **[!UICONTROL Prefill]**.

         1. (Facoltativo) Per aggiungere un altro set di copie di annunci a un annuncio, che può essere utilizzato se una delle righe della copia dell&#39;annuncio originale supera la lunghezza massima dopo che i parametri dinamici sono stati sostituiti con i dati durante la propagazione, fare clic su **[!UICONTROL Add Alternate]** e quindi aggiungere i valori alternativi.

            >[!NOTE]
            >
            >* Se è selezionata l&#39;opzione [!UICONTROL Prefill], i campi alternativi vengono precompilati con quelli originali e puoi modificarli in base alle esigenze.
            >* Solo i campi della copia dell’annuncio che superano la lunghezza massima vengono sostituiti con il valore alternativo. Ad esempio, se solo un titolo o titolo originale è troppo lungo, la variante di annuncio generata utilizza il titolo o il titolo alternativo e le descrizioni originali. Assicurati pertanto che la copia dell’annuncio alternativa sia appropriata quando combinata con la copia dell’annuncio originale.
            >* Se la copia dell’annuncio originale soddisfa i requisiti di lunghezza del motore di ricerca, la copia dell’annuncio alternativa viene eliminata.
            >* Puoi specificare fino a quattro alternative per ogni campo della copia dell’annuncio.

         * Per modificare una variante di annuncio, effettua le seguenti operazioni:

            1. Modifica le impostazioni dell’annuncio.

               Per gli annunci di ricerca responsive, puoi includere 3-15 titoli e 2-4 descrizioni.

            1. (Facoltativo) Per precompilare tutti i campi della copia dell&#39;annuncio alternativi con il testo dei campi della copia dell&#39;annuncio originale, selezionare la casella di controllo accanto a **[!UICONTROL Prefill]**.

            1. (Facoltativo) Per aggiungere un altro set di copie di annunci a un annuncio, che può essere utilizzato se una delle righe della copia dell&#39;annuncio originale supera la lunghezza massima dopo che i parametri dinamici sono stati sostituiti con i dati durante la propagazione, fare clic su **[!UICONTROL Add Alternate]** e quindi aggiungere i valori alternativi.

               >[!NOTE]
               >
               >* Se è selezionata l&#39;opzione [!UICONTROL Prefill], i campi alternativi vengono precompilati con quelli originali e puoi modificarli in base alle esigenze.
               >* Solo i campi della copia dell’annuncio che superano la lunghezza massima vengono sostituiti con il valore alternativo. Ad esempio, se solo un titolo o titolo originale è troppo lungo, la variante di annuncio generata utilizza il titolo o il titolo alternativo e le descrizioni originali. Assicurati pertanto che la copia dell’annuncio alternativa sia appropriata quando combinata con la copia dell’annuncio originale.
               >* Se la copia dell’annuncio originale soddisfa i requisiti di lunghezza del motore di ricerca, la copia dell’annuncio alternativa viene eliminata.
               >* Puoi specificare fino a quattro alternative per ogni campo della copia dell’annuncio.

         * Per rimuovere una variante di annuncio, fai clic su **[!UICONTROL Remove ETA Variation]** (per annunci di testo espansi/estesi) o **[!UICONTROL Remove RSA Variation]** (per annunci di ricerca responsive) accanto alla variante dell&#39;annuncio, a seconda dei casi.

   1. (Solo modelli di acquisto) Fare clic sulla scheda **[!UICONTROL Product Groups]** e quindi specificare le informazioni sui gruppi di prodotti di destinazione.

   1. (Facoltativo) Fare clic sulla scheda **[!UICONTROL Feed Filters]**, quindi specificare le righe del file di feed da propagare.

   1. (Facoltativo) Fai clic su **[!UICONTROL Label Classifications tab]**, quindi specifica i valori di classificazione delle etichette da assegnare ai diversi componenti della campagna creati:

      1. Fare clic sulla casella di controllo accanto a **[!DNL \[Component\] Label Classifications]**.

      1. Per ogni classificazione di etichetta da assegnare al componente, effettua le seguenti operazioni:

         1. Fare clic su **[!UICONTROL Add Label Classification]**.

         1. Seleziona la classificazione dell’etichetta, quindi seleziona un valore esistente o inserisci un nuovo valore.

1. Salva il modello:

   * Per salvare semplicemente il modello, fare clic su **[!UICONTROL Save]** e quindi di nuovo su **[!UICONTROL Save]**.

   * Per salvare il modello e propagare il file di dati specificato tramite il modello, fare clic su **[!UICONTROL Save]** e quindi su **[!UICONTROL Save & Propagate]**.

## Modificare lo stato dei modelli di feed

Puoi attivare qualsiasi modello di feed dati in pausa o sospendere qualsiasi modello di feed dati attivo.

>[!NOTE]
>
>È possibile propagare manualmente i dati tramite un modello in pausa, ma i dati non vengono propagati automaticamente attraverso di esso.

1. Nel menu principale, fare clic su **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**, che consente di aprire la scheda [!UICONTROL Templates].

1. Selezionare la casella di controllo accanto a ogni modello di cui si desidera modificare lo stato.

1. Nella barra degli strumenti sopra la tabella dati fare clic su **[!UICONTROL Change Status]** e quindi su **[!UICONTROL Activate]** o **[!UICONTROL Pause]**.

## Eliminare i modelli di feed

1. Nel menu principale, fare clic su **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**, che consente di aprire la scheda [!UICONTROL Templates].

1. Selezionare la casella di controllo accanto a ogni modello che si desidera eliminare.

1. Nella barra degli strumenti sopra la tabella dati, fare clic su **[!UICONTROL Delete]**.

1. Nel messaggio di conferma, fare clic su **[!UICONTROL Yes]**.

>[!MORELIKETHIS]
>
>* [Informazioni sull&#39;automazione della gestione degli annunci tramite i feed di inventario](../inventory-feeds-about.md)
>* [Impostazioni del modello di annunci di ricerca responsive e di testo](template-text-rsa.md)
>* [[!DNL Google Ads] impostazioni del modello di annuncio acquisti](template-google-shopping.md)
>* [[!DNL Microsoft Advertising] impostazioni del modello di annuncio acquisti](template-microsoft-shopping.md)
>* [Propagazione dei dati di feed tramite modelli](../feed-data-propagate.md)
