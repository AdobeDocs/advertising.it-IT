---
title: Supporto Adobe Advertising per il California Consumer Privacy Act &#58; Supporto per la rinuncia del consumatore
description: Scopri il supporto per l’acquisizione delle richieste di rifiuto del consumatore.
feature: CCPA
role: User, Developer
exl-id: df2b8679-8a1c-4cd7-b867-cd2f53c76c8f
TQID: https://experienceleague.adobe.com/16JkyKVsVoBIGKEbhEIH7HWZ-H-XkjBad7yq9-NhY3s
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 7845129ba6566c1aaaf160cc6f9ad33bf1731f75
workflow-type: tm+mt
source-wordcount: 1101
ht-degree: 0%

---

# Supporto di Adobe Advertising per il California Consumer Privacy Act: supporto per la rinuncia del consumatore alla vendita

*Per Adobe Advertising Demand Side Platform (DSP)*

>[!IMPORTANT]
>
>Il contenuto di questo documento non rappresenta e non intende sostituirsi a una consulenza legale. Consulta il tuo consulente legale per ricevere consigli in merito al California Consumer Privacy Act.

Il California Consumer Privacy Act (CCPA) è la nuova legge sulla privacy della California, in vigore dal 1° gennaio 2020. Il CCPA conferisce ai residenti della California nuovi diritti in merito alle loro informazioni personali e impone responsabilità in materia di protezione dei dati a determinate entità che conducono attività commerciali in California. Il CCPA garantisce ai consumatori il diritto di accedere ai propri dati e di cancellarli, nonché il diritto di non partecipare a determinate attività che possono essere considerate di &quot;vendita&quot; di informazioni personali a terzi.

In qualità di azienda, potrai determinare i dati personali che Adobe CX Enterprise tratta e archivia per tuo conto.

In qualità di fornitore di servizi, Adobe Advertising fornisce supporto alla tua azienda per l’adempimento dei suoi obblighi in virtù del CCPA applicabili all’utilizzo dei prodotti e dei servizi Adobe Advertising, inclusa la gestione delle richieste dei consumatori di accedere e cancellare le informazioni personali e la gestione delle richieste dei consumatori di rinunciare alla vendita di informazioni personali.

In questo documento viene descritto come Adobe Advertising Demand Side Platform (DSP), in qualità di fornitore di servizi, supporta il diritto del consumatore di rifiutare la &quot;vendita&quot; di &quot;informazioni personali&quot;, in base a quanto definito dal CCPA. Include informazioni su come comunicare ad Adobe Advertising le richieste di rifiuto e come recuperare i rapporti sulle richieste di rifiuto dell’organizzazione.

Per informazioni su come [!DNL Advertising Search, Social, & Commerce], Advertising Creative e [!DNL Advertising DCO] supportano i diritti di accesso e cancellazione delle informazioni personali dei consumatori, vedere [Supporto di Adobe Advertising per il California Consumer Privacy Act: supporto per l&#39;accesso e l&#39;eliminazione dei dati dei consumatori](/help/privacy/ccpa/ccpa-access-delete.md).

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

*Gli inserzionisti hanno assegnato solo un ID organizzazione Adobe CX Enterprise*

1. Distribuisci una libreria JavaScript per recuperare i cookie del cliente. La stessa libreria, `AdobePrivacy.js`, viene utilizzata per tutte le soluzioni Adobe CX Enterprise.

   >[!IMPORTANT]
   >
   >Le richieste ad alcune soluzioni Adobe CX Enterprise non richiedono la libreria JavaScript, ma le richieste ad Adobe Advertising lo richiedono.

   Devi distribuire la libreria sulla pagina web da cui i clienti possono inviare richieste di rifiuto della vendita, come ad esempio il portale della privacy della tua azienda. La libreria consente di recuperare i cookie di Adobe (ID spazio dei nomi: `gsurferID`) in modo da poter inviare queste identità come parte delle richieste di rifiuto tramite l&#39;API Adobe Experience Platform Privacy Service.

1. Identifica l’ID organizzazione CX Enterprise e assicurati che sia collegato ai tuoi account Adobe Advertising.

   Un ID organizzazione CX Enterprise è una stringa alfanumerica composta da 24 caratteri a cui segue &quot;@AdobeOrg.&quot; Alla maggior parte dei clienti CX Enterprise è stato assegnato un ID organizzazione. Se il team marketing o l’amministratore di sistema interno di Adobe non conosce l’ID organizzazione o non è sicuro che sia stato predisposto, contatta il team del tuo account Adobe. Per inviare richieste all&#39;API per la privacy utilizzando lo spazio dei nomi `imsOrgID` è necessario l&#39;ID organizzazione.

   >[!IMPORTANT]
   >
   >Contatta il rappresentante Adobe Advertising della tua azienda per verificare che tutti gli account Adobe Advertising della tua organizzazione, inclusi [!DNL DSP] account o inserzionisti, [!DNL Search, Social, & Commerce] account e [!DNL Creative] o [!DNL DCO] account, siano collegati al tuo ID organizzazione CX Enterprise.

1. Utilizza l&#39;API di Adobe Experience Platform Privacy Service per [inviare richieste di rifiuto](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/consent.html) ad Adobe Advertising per conto dei consumatori e per controllare lo stato delle richieste esistenti.

   Per un esempio di richiesta di rifiuto, consulta l’appendice seguente.

   >[!NOTE]
   >
   >Se la tua azienda dispone di più ID organizzazione CX Enterprise, devi inviare richieste API separate per ciascuno di essi. È tuttavia possibile effettuare una richiesta API a più soluzioni secondarie di Adobe Advertising ([!DNL Search, Social, & Commerce], [!DNL Creative], [!DNL DSP] e [!DNL DCO]), con un account per ogni soluzione secondaria.

Tutti questi passaggi sono necessari per ricevere supporto da Adobe Advertising. Per ulteriori informazioni su queste e altre attività correlate che è necessario eseguire utilizzando Adobe Experience Platform Privacy Service e dove trovare gli elementi necessari, vedere [https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html).

## Recupero dei rapporti dei consumatori che hanno presentato richieste di rifiuto

Adobe Advertising genera rapporti mensili sugli ID inviati dai clienti per richieste di rifiuto per l’account. Each report is available as a tab-separated text file compressed into GZIP format. The data consolidates requests captured using CCPA opt-out-of-sale segments that were created in Advertising DSP and any submissions made via the Privacy Service API. User IDs captured in CCPA opt-out-of-sale segments are identified by segment and by advertiser. Reports are generated on the first of each month for the previous month. For example, the monthly user list for June is available on July 1.

You can retrieve links to the monthly reports that were created in the previous three months, either from within Advertising DSP or by using the Advertising DSP [!DNL Trafficking API]. Each link is valid for seven days but refreshes each time a customer attempts to retrieve one.

### Method 1: Retrieve consumer opt-out-of-sale reports within Advertising DSP

1. Accedi all&#39;account dell&#39;inserzionista in Advertising DSP all&#39;indirizzo [https://advertising.adobe.com/](https://advertising.adobe.com/).

1. [Retrieve the reports](/help/dsp/audiences/ccpa-opt-out-segment-report-retrieve.md).

### Method 2: Retrieve consumer opt-out-of-sale reports using the Advertising DSP [!DNL Trafficking API]

This feature is available to organizations that use the [!DNL Trafficking API]. See the documentation for the [!DNL Trafficking API] for more information.<!-- Add link to API doc once it's published. -->

If your organization doesn&#39;t use the [!DNL Trafficking API] but is interested in more information, contact your Adobe Account Team.

## Appendix: Example [!UICONTROL CCPA Opt-Out-of-Sale] request for Privacy Service API users

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

where, per the [Privacy Service API specifications](https://experienceleague.adobe.com/en/docs/experience-platform/privacy/api/appendix):

* `"namespace": "AdCloud"` indicates the `AdCloud` cookie space, and the corresponding value is the customer’s cookie ID as retrieved from `AdobePrivacy.js`
* `"include": ["adCloud"]` indicates that the request applies to the product Adobe Advertising
