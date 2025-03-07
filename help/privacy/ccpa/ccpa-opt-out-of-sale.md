---
title: Supporto Adobe Advertising per il California Consumer Privacy Act &#58; Supporto per la rinuncia dei consumatori
description: Scopri il supporto per l’acquisizione delle richieste di rifiuto del consumatore.
feature: CCPA
role: User, Developer
exl-id: df2b8679-8a1c-4cd7-b867-cd2f53c76c8f
source-git-commit: 788b4ddb9b690a3f0bac93ec9b5145fc7a324719
workflow-type: tm+mt
source-wordcount: '996'
ht-degree: 0%

---

# Supporto di Adobe Advertising per il California Consumer Privacy Act: supporto per la rinuncia del consumatore alla vendita

*Per Adobe Advertising Demand Side Platform (DSP)*

>[!IMPORTANT]
>
>Il contenuto di questo documento non rappresenta e non intende sostituirsi a una consulenza legale. Consulta il tuo consulente legale per ricevere consigli in merito al California Consumer Privacy Act.

Il California Consumer Privacy Act (CCPA) è la nuova legge sulla privacy della California, in vigore dal 1° gennaio 2020. Il CCPA conferisce ai residenti della California nuovi diritti in merito alle loro informazioni personali e impone responsabilità in materia di protezione dei dati a determinate entità che conducono attività commerciali in California. Il CCPA garantisce ai consumatori il diritto di accedere ai propri dati e di cancellarli, nonché il diritto di non partecipare a determinate attività che possono essere considerate di &quot;vendita&quot; di informazioni personali a terzi.

In qualità di azienda, potrai determinare i dati personali che Adobe Experience Cloud tratta e archivia per tuo conto.

In qualità di fornitore di servizi, Adobe Advertising fornisce supporto alla tua azienda per l’adempimento dei suoi obblighi in virtù del CCPA applicabili all’utilizzo dei prodotti e dei servizi Adobe Advertising, inclusa la gestione delle richieste dei consumatori di accedere e cancellare le informazioni personali e la gestione delle richieste dei consumatori di rinunciare alla vendita di informazioni personali.

In questo documento viene descritto come Adobe Advertising Demand Side Platform (DSP), in qualità di fornitore di servizi, supporta il diritto del consumatore di rifiutare la &quot;vendita&quot; di &quot;informazioni personali&quot;, in base a quanto definito dal CCPA. Include informazioni su come comunicare ad Adobe Advertising le richieste di rifiuto e come recuperare i rapporti sulle richieste di rifiuto dell’organizzazione.

Per informazioni su come [!DNL Advertising Search, Social, & Commerce], Advertising Creative e [!DNL Advertising DCO] supportano i diritti di accesso e cancellazione delle informazioni personali dei consumatori, vedere [Supporto Adobe Advertising per il California Consumer Privacy Act: Supporto per l&#39;accesso e l&#39;eliminazione dei dati dei consumatori](/help/privacy/ccpa/ccpa-access-delete.md).

Per ulteriori informazioni sui servizi di privacy Adobe per il CCPA, visitare il [Centro per la privacy Adobe](https://www.adobe.com/privacy/ccpa.html).

## Comunicazione delle richieste di rifiuto del consumatore ad Adobe Advertising

Puoi comunicare le richieste di rifiuto del consumatore utilizzando:

* un segmento di rinuncia CCPA creato in Advertising DSP
* API di Adobe Experience Platform Privacy Service

### Metodo 1: comunicare le richieste di rifiuto del CCPA utilizzando un segmento [!UICONTROL CCPA Opt-Out-of-Sale] in Advertising DSP

>[!NOTE]
>
>Gli utenti rimangono nei segmenti di rifiuto del CCPA per un tempo indefinito.

1. Accedi all&#39;account dell&#39;inserzionista in Advertising DSP all&#39;indirizzo [https://advertising.adobe.com/](https://advertising.adobe.com/).
1. [Crea un segmento di rifiuto CCPA e implementa il pixel del segmento per acquisire le richieste di rifiuto](/help/dsp/audiences/ccpa-opt-out-segment-create.md).

### Metodo 2: comunicare le richieste di rifiuto del CCPA utilizzando l’API Adobe Experience Platform Privacy Service

*Gli inserzionisti hanno assegnato solo un ID organizzazione Adobe Experience Cloud*

1. Distribuisci una libreria JavaScript per recuperare i cookie del cliente. La stessa libreria, `AdobePrivacy.js`, viene utilizzata per tutte le soluzioni Adobe Experience Cloud.

   >[!IMPORTANT]
   >
   >Le richieste ad alcune soluzioni Adobe Experience Cloud non richiedono la libreria JavaScript, ma le richieste ad Adobe Advertising lo richiedono.

   Devi distribuire la libreria sulla pagina web da cui i clienti possono inviare richieste di rifiuto della vendita, come ad esempio il portale della privacy della tua azienda. La libreria consente di recuperare i cookie di Adobe (ID spazio dei nomi: `gsurferID`) in modo da poter inviare queste identità come parte delle richieste di rifiuto tramite l&#39;API Adobe Experience Platform Privacy Service.

1. Identifica il tuo ID organizzazione Experience Cloud e assicurati che sia collegato al tuo account Adobe Advertising.

   Un ID organizzazione Experience Cloud è una stringa alfanumerica composta da 24 caratteri a cui segue &quot;@AdobeOrg.&quot; Alla maggior parte dei clienti Experience Cloud è stato assegnato un ID organizzazione. Se il team marketing o l’amministratore di sistema interno di Adobe non conosce l’ID organizzazione o non è sicuro che sia stato predisposto, contatta il team del tuo account Adobe. Per inviare richieste all&#39;API per la privacy utilizzando lo spazio dei nomi `imsOrgID` è necessario l&#39;ID organizzazione.

   >[!IMPORTANT]
   >
   >Contatta il rappresentante Adobe Advertising della tua azienda per verificare che tutti gli account Adobe Advertising della tua organizzazione, inclusi [!DNL DSP] account o inserzionisti, [!DNL Search, Social, & Commerce] account e [!DNL Creative] o [!DNL DCO] account, siano collegati al tuo ID organizzazione Experience Cloud.

1. Utilizza l&#39;API di Adobe Experience Platform Privacy Service per [inviare richieste di rifiuto](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/consent.html) ad Adobe Advertising per conto dei consumatori e per controllare lo stato delle richieste esistenti.

   Per un esempio di richiesta di rifiuto, consulta l’appendice seguente.

   >[!NOTE]
   >
   >Se la tua azienda dispone di più ID organizzazione Experience Cloud, devi inviare richieste API separate per ciascuno di essi. È tuttavia possibile effettuare una richiesta API a più soluzioni secondarie di Adobe Advertising ([!DNL Search, Social, & Commerce], [!DNL Creative], [!DNL DSP] e [!DNL DCO]), con un account per ogni soluzione secondaria.

Tutti questi passaggi sono necessari per ricevere supporto da Adobe Advertising. Per ulteriori informazioni su queste e altre attività correlate che è necessario eseguire utilizzando Adobe Experience Platform Privacy Service e dove trovare gli elementi necessari, vedere [https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html).

## Recupero dei report dei consumatori che hanno inviato richieste di rifiuto

Adobe Advertising genera rapporti mensili sugli ID inviati dai clienti per richieste di rifiuto per l’account. Ogni rapporto è disponibile come file di testo separato da tabulazioni compresso in formato GZIP. I dati consolidano le richieste acquisite utilizzando i segmenti di rifiuto del CCPA creati in Advertising DSP e tutte le richieste effettuate tramite l’API Privacy Service. Gli ID utente acquisiti nei segmenti di rifiuto del CCPA sono identificati per segmento e dall’inserzionista. I rapporti vengono generati il primo di ogni mese per il mese precedente. Ad esempio, l’elenco mensile degli utenti di giugno è disponibile il 1° luglio.

È possibile recuperare i collegamenti ai report mensili creati nei tre mesi precedenti dall&#39;interno di Advertising DSP o utilizzando Advertising DSP [!DNL Trafficking API]. Ogni collegamento è valido per sette giorni, ma viene aggiornato ogni volta che un cliente tenta di recuperarne uno.

### Metodo 1: Recuperare i rapporti sulla rinuncia del consumatore in Advertising DSP

1. Accedi all&#39;account dell&#39;inserzionista in Advertising DSP all&#39;indirizzo [https://advertising.adobe.com/](https://advertising.adobe.com/).
1. [Recupera i report](/help/dsp/audiences/ccpa-opt-out-segment-report-retrieve.md).

### Metodo 2: Recuperare i report sulla rinuncia del consumatore tramite Advertising DSP [!DNL Trafficking API]

Questa funzionalità è disponibile per le organizzazioni che utilizzano [!DNL Trafficking API]. Per ulteriori informazioni, vedere la documentazione di [!DNL Trafficking API].<!-- Add link to API doc once it's published. -->

Se la tua organizzazione non utilizza [!DNL Trafficking API] ma è interessata a ulteriori informazioni, contatta il team del tuo account Adobe.

## Appendice: esempio di richiesta [!UICONTROL CCPA Opt-Out-of-Sale] per utenti API Privacy Service

```
curl -X POST \
  https://platform.adobe.io/data/privacy/gdpr/ \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'Content-Type: application/json' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -d '{
    "companyContexts": [
      {
        "namespace": "imsOrgID",
        "value": "{IMS_ORG}"
      }
    ],
    "users": [
      {
        "key": "DavidSmith",
        "action": ["opt-out-of-sale"],
        "userIDs": [
          {
            "namespace": "email",
            "value": "dsmith@acme.com",
            "type": "standard"
          },
          {
            "namespace": "AdCloud",
            "type": "standard",
            "value":  "Wqersioejr-wdg",
          }
    ],
    "include": ["adCloud"],
    "regulation": "ccpa"
}'
```

dove, secondo le [specifiche API di Privacy Service](https://experienceleague.adobe.com/en/docs/experience-platform/privacy/api/appendix):

* `"namespace": "AdCloud"` indica lo spazio cookie `AdCloud` e il valore corrispondente è l&#39;ID cookie del cliente recuperato da `AdobePrivacy.js`
* `"include": ["adCloud"]` indica che la richiesta si applica al prodotto Adobe Advertising
