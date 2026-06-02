---
title: (Nuova interfaccia) Crea un'azione di conversione per una conversione  [!DNL Google Ads]  avanzata per i lead
description: Scopri come creare un'azione di conversione  [!DNL Google Ads]  per una conversione avanzata per i lead.
feature: Conversions
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
  - id: e6916c1b-e939-4e0b-99f5-768e83e1e99f
subfeature_v2:
  - id: d068b149-b9d1-421c-9033-a51495366ddc
source-git-commit: 0bfee2b52410b5cab8e9b3dfba35effc36fc40e1
workflow-type: tm+mt
source-wordcount: 510
ht-degree: 0%

---

# (Nuova interfaccia) Crea un&#39;azione di conversione per una conversione avanzata di [!DNL Google Ads] per i lead

*funzionalità Beta*

Solo *[!DNL Google Ads]account*

È possibile creare azioni di conversione per [!DNL Google Ads] conversioni avanzate per i lead da monitorare per singoli account [!DNL Google Ads], non per le conversioni a livello di account manager.

Dopo aver creato l&#39;azione di conversione e aver implementato un tag di tracciamento della conversione, puoi [caricare i dati di conversione offline acquisiti dalla tua organizzazione](conversions-upload-offline-enhanced-conversions.md) e attribuirli all&#39;azione di conversione.

Supporto non disponibile per gli account [!DNL Microsoft Advertising].

## Creare un’azione di conversione

1. Nel menu principale, fare clic su **[!UICONTROL Goals]>[!UICONTROL Conversions]**.

1. Sopra la tabella dati, fare clic su **[!UICONTROL Set up Conversion]**.

1. Specificare le [impostazioni dell&#39;azione di conversione](#conversion-action-settings-google).

   1. Selezionare [!UICONTROL Setup Method] *[!UICONTROL Create Conversion]*.

   1. Selezionare l&#39;account, quindi selezionare il tipo di conversione: *[!UICONTROL Import conversion]*.

   1. Fare clic su **[!UICONTROL Next]**.

   1. Specifica le opzioni dell’azione di conversione.

   1. Fare clic su **[!UICONTROL Review and Save]** per rivedere le impostazioni.

   1. Fare clic su **[!UICONTROL Generate]**.

1. Leggi le informazioni sulla creazione di un tag di tracciamento per la conversione avanzata per i lead, quindi fai clic su **[!UICONTROL Next]**.

   Devi creare il tag di conversione e implementarlo in base alle esigenze sui siti web dai quali desideri tenere traccia della metrica di conversione. Sarà inoltre necessario abilitare conversioni avanzate per i lead e accettare i termini e le condizioni per i dati dei clienti. Per istruzioni, vedere le istruzioni [!DNL Google Ads] per &quot;[Configurare il tag [!DNL Google] per le conversioni avanzate per i lead](https://support.google.com/google-ads/answer/11021502).&quot;

   Se desideri tenere traccia dei valori di conversione specifici per le transazioni, [personalizza il frammento di evento](https://support.google.com/google-ads/answer/6095947).

1. Fare clic su **[!UICONTROL Close].**

## Impostazioni delle azioni di conversione {#conversion-action-settings-google}

### Sezione Percorso di configurazione

**[!UICONTROL Setup Method]:** Tipo di azione: *[!UICONTROL Create Conversion]*

**[!UICONTROL Platform]:** La rete di annunci: *[!UICONTROL Google]*.

### Sezione Dettagli conversione

**[!UICONTROL Select Account]:** L&#39;account [!DNL Google Ads] applicabile.

**[!UICONTROL Type of conversions]:** Il tipo di conversione da tenere traccia: Seleziona *[!UICONTROL Import conversion]*. Tutti gli altri tipi vengono utilizzati per creare tag di tracciamento delle conversioni (non azioni di conversione) per altri tipi di conversioni.

### Sezione Impostazioni di conversione

**[!UICONTROL Conversion Name]:** Nome univoco per l&#39;azione di conversione.

**[!UICONTROL Goal Category]:** La categoria di conversione, ad esempio *Lead qualificato* o *Iscrizione*.

**[!UICONTROL Preferred Action optimization]:** Se l&#39;obiettivo è un *[!UICONTROL Primary action used for bidding optimization]* o un *[!UICONTROL Secondary action not used for bidding optimization]*.

**[!UICONTROL Conversion Value]:** Come misurare il [valore di ogni conversione](https://support.google.com/google-ads/answer/13064207):

* *[!UICONTROL Use the same value for each conversion],* che richiede di selezionare una valuta e immettere il valore per ogni conversione.

* *[!UICONTROL Use different values for each conversion],* che richiede di selezionare una valuta e immettere un valore predefinito per ogni conversione. Puoi modificare il valore predefinito nel tag con un valore specifico per la transazione quando implementi il tag in una pagina web specifica.

* *[!UICONTROL Don't use a value for this conversion action (Not recommended)]*

**[!UICONTROL Count]:** [Quante conversioni conteggiare per clic o interazione](https://support.google.com/google-ads/answer/3438531): *[!UICONTROL Every (Recommended for every purchases because every purchase is valuable)]* o *[!UICONTROL One (Recommended for leads, sign-ups and other conversions for which only the first interaction is valuable)]*.

**[!UICONTROL Click-Through Conversion Window]:** il numero massimo di giorni dopo un&#39;interazione dell&#39;annuncio per i quali vengono registrate le conversioni. Per le campagne di ricerca, visualizzazione e acquisto, la finestra può essere di 1-90 giorni. Selezionare un numero o selezionare **[!UICONTROL Custom]** e immettere un numero.

**[!UICONTROL View-Through Conversion Window]:** il numero massimo di giorni dopo i quali un utente visualizza i tuoi annunci e per i quali vengono registrate le conversioni view-through. Per le campagne di ricerca, visualizzazione e acquisto, la finestra può essere di 1-90 giorni. Selezionare un numero o selezionare **[!UICONTROL Custom]** e immettere un numero.

**[!UICONTROL Attribution Model]:** [Il modello di attribuzione che determina il credito ottenuto da ogni interazione annuncio](https://support.google.com/google-ads/answer/6259715?sjid=8211249329930775138): *[!UICONTROL Data driven]* o *[!UICONTROL Last click]*.

>[!MORELIKETHIS]
>
>* [(Nuova interfaccia) Carica dati di conversione offline per conversioni avanzate](/help/search-social-commerce/admin/conversion-metrics/upload-data-offline-conversions.md)
>* [Carica dati di conversione offline per conversioni avanzate](/help/search-social-commerce/admin/conversion-metrics/upload-data-offline-conversions.md)
>* [Implementa [!DNL Google Ads] conversioni avanzate per lead](/help/search-social-commerce/campaign-management/special-workflows/google-enhanced-conversions-leads.md)
