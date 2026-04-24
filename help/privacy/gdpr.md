---
title: Adobe Advertising support for the General Data Protection Regulation
description: Learn about the supported data request types, required setup and field values, and examples of API access requests using legacy product IDs and returned data fields
feature: GDPR
role: User, Developer
exl-id: abf0dc51-e23b-4c9a-95aa-14e0844939bb
TQID: https://experienceleague.adobe.com/qR5H-xgBKdtWcMYfrdGdk1y5s9PEA0-hNGZADbR6TuM
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
source-wordcount: 1046
ht-degree: 0%

---

# Adobe Advertising support for the General Data Protection Regulation

*For [!DNL Adobe Advertising Search, Social, & Commerce]; Adobe Advertising DSP; Adobe Advertising Creative; and Adobe Advertising DCO*

>[!IMPORTANT]
>
>Il contenuto di questo documento non rappresenta e non intende sostituirsi a una consulenza legale. Consult with your legal counsel for advice concerning the General Data Protection Regulation.

The General Data Protection Regulation (GDPR), a law in effect May 25, 2018, gives all individuals (data subjects) within the borders of the European Union (EU) control of their personal data and simplifies the regulatory environment for international business. This law applies to all businesses (data controllers) that offer goods or services to, monitor the behavior of, or collect personal data from individuals within the borders of the EU at the time their personal data is processed, regardless of the data controller&#39;s business location.

Adobe CX Enterprise acts as a data processor for any personal data it receives and stores on behalf of its customers. As a data controller, you determine the personal data that Adobe CX Enterprise processes and stores on your behalf.

This document describes how [!DNL Advertising Search, Social, & Commerce]; Advertising Creative; Advertising DSP (Demand Side Platform); and [!DNL Advertising DCO] support your data subjects&#39; GDPR data access and deletion rights using the Adobe Experience Platform Privacy Service API and Privacy Service UI.

For more information about what GDPR means for your business, see [GDPR and Your Business](https://www.adobe.com/privacy/general-data-protection-regulation.html).

## Supported data request types for Adobe Advertising

Adobe Experience Platform provides the ability for businesses to complete the following tasks:

* Access a data subject&#39;s cookie-level data or device ID-level data (for ads in mobile apps) within [!DNL Search, Social, & Commerce], [!DNL Creative], [!DNL DSP], or [!DNL DCO].
* Delete cookie-level data stored within [!DNL Search, Social, & Commerce], [!DNL Creative], [!DNL DSP], or [!DNL DCO] for data subjects using a browser; or delete ID-level data stored within [!DNL DSP] for data subjects using apps on mobile devices.
* Check the status of one or all existing requests.

## Required setup to send requests for Adobe Advertising

To make requests to access and delete data for Adobe Advertising, you must:

1. Deploy a JavaScript library to retrieve and remove your data subject cookies. The same library, `AdobePrivacy.js`, is used for all Adobe CX Enterprise solutions.

   >[!IMPORTANT]
   >
   >Le richieste ad alcune soluzioni CX Enterprise non richiedono la libreria JavaScript, ma le richieste ad Adobe Advertising lo richiedono.

   È necessario distribuire la libreria nella pagina Web da cui le persone interessate possono inviare richieste di accesso ed eliminazione, ad esempio il portale della privacy della società. La libreria ti consente di recuperare i cookie [!DNL Adobe] (ID spazio dei nomi: `gsurferID`) in modo da poter inviare queste identità come parte delle richieste di accesso ed eliminazione tramite l&#39;API Adobe Experience Platform Privacy Service.

   Quando l’interessato chiede di cancellare dati personali, la libreria elimina anche il cookie dell’interessato dal browser dell’interessato.

   >[!NOTE]
   >
   >L’eliminazione dei dati personali è diversa dalla rinuncia, che interrompe il targeting di un utente finale con segmenti di pubblico. Tuttavia, quando un interessato richiede di eliminare i dati personali da [!DNL Creative], [!DNL DSP] o [!DNL DCO], la libreria invia anche una richiesta ad Adobe Advertising per rifiutare l&#39;interessato dal targeting dei segmenti. Per gli inserzionisti con [!DNL Search, Social, & Commerce], si consiglia di fornire agli interessati un collegamento a [https://www.adobe.com/privacy/opt-out.html](https://www.adobe.com/privacy/opt-out.html), che spiega come rinunciare al targeting dei segmenti di pubblico.

1. Identifica l’ID organizzazione CX Enterprise e assicurati che sia collegato ai tuoi account Adobe Advertising.

   Un ID organizzazione CX Enterprise è una stringa alfanumerica composta da 24 caratteri a cui segue &quot;@AdobeOrg.&quot; Alla maggior parte dei clienti CX Enterprise è stato assegnato un ID organizzazione. Se il team marketing o l&#39;amministratore di sistema interno di [!DNL Adobe] non conosce l&#39;ID organizzazione o non è sicuro che sia stato eseguito il provisioning, contatta l&#39;Assistenza clienti Adobe all&#39;indirizzo gdprsupport@adobe.com. Per inviare richieste all&#39;API per la privacy utilizzando lo spazio dei nomi `imsOrgID` è necessario l&#39;ID organizzazione.

   >[!IMPORTANT]
   >
   >Contatta il rappresentante Adobe Advertising della tua azienda per verificare che tutti gli account Adobe Advertising della tua organizzazione, inclusi [!DNL DSP] account o inserzionisti, [!DNL Search, Social, & Commerce] account e [!DNL Creative] o [!DNL DCO] account, siano collegati al tuo ID organizzazione CX Enterprise.

1. Utilizza l&#39;[API Adobe Experience Platform Privacy Service](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/privacy-jobs.html?lang=it) (per le richieste automatizzate) o la [interfaccia utente Privacy Service](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html?lang=it) (per le richieste ad hoc) per inviare richieste di accesso ed eliminazione ad Adobe Advertising per conto delle persone interessate e per controllare lo stato delle richieste esistenti.

   Per gli inserzionisti che dispongono di un’app mobile per interagire con le persone interessate e avviare campagne con DSP, devi scaricare gli SDK per dispositivi mobili predisposti per la privacy per CX Enterprise. Gli SDK di Mobile consentono ai titolari del trattamento dei dati di impostare flag di stato per la rinuncia, recuperare l&#39;ID dispositivo dell&#39;interessato (ID spazio dei nomi: `deviceID`) e inviare richieste all&#39;API Privacy Service. La tua app mobile richiederà una versione di SDK 4.15.0 o successiva.

   Quando invii la richiesta di accesso di una persona interessata, l’API di Privacy Service restituisce le informazioni di tale persona in base al cookie o all’ID dispositivo specificato, che devono quindi essere restituiti alla persona interessata.

   Quando invii la richiesta di cancellazione di una persona interessata, l’ID cookie o l’ID dispositivo e tutti i dati relativi a costi, clic e ricavi associati al cookie vengono eliminati dal server.

   >[!NOTE]
   >
   >Se la tua azienda dispone di più ID organizzazione CX Enterprise, devi inviare richieste API separate per ciascuno di essi. È tuttavia possibile effettuare una richiesta API a più soluzioni secondarie di Adobe Advertising ([!DNL Search, Social, & Commerce], [!DNL Creative], [!DNL DSP] e [!DNL DCO]), con un account per ogni soluzione secondaria.

Tutti i passaggi sono necessari per Adobe Advertising. Per ulteriori informazioni su queste e altre attività correlate che è necessario eseguire utilizzando Adobe Experience Platform Privacy Service e dove trovare gli elementi necessari, vedere &quot;[Panoramica di Privacy Service](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html?lang=it).&quot;

## Valori campo obbligatori nelle richieste JSON di Adobe Advertising

`"company context":`

* `"namespace": **imsOrgID**`
* `"value":` &lt;*ID organizzazione CX Enterprise*>

`"users":`

* `"key":` &lt;*in genere il nome dell&#39;interessato*>

* `"action":` `**access**` o `**delete**`

* `"user IDs":`

   * `"namespace": **411**` (che indica lo spazio cookie [!DNL adcloud])

   * `"value":` &lt;*il valore ID cookie effettivo dell&#39;interessato recuperato da`AdobePrivacy.js`*>

* `"include": **adCloud**` (prodotto [!DNL Adobe] applicabile alla richiesta)

* `"regulation": **gdpr**` (normativa sulla privacy applicabile alla richiesta)

## Esempio di richiesta inviata dall&#39;interessato utilizzando un ID utente di Adobe Advertising recuperato da `AdobePrivacy.js`

```
{
"companyContexts":[
    {
        "namespace":"imsOrgID",
        "value":"5AB13068374019BC@AdobeOrg"
      }
   ],
   "users": [
{
 "key": "John Doe",
 "action":["access"],
 "userIDs":[
      { 
        "namespace":"411",
        "value":"Wqersioejr-wdg",
        "type":"namespaceId",
        "deletedClientSide":false
      }
   ]
}
],
"include":[
      "adCloud"
   ],
    "regulation":"gdpr"
}
```

## Campi dati restituiti per le richieste di accesso

Di seguito è riportato un esempio di risposta di accesso per Adobe Advertising.

```
{
    "jobId":"12345AD43E",
    "action":"access",
    "product":"adCloud",
    "status":"complete",
    "results":{
        "userIDs":[
            {
                "namespace":"411",
                "userID":" Wqersioejr-wdg "
            }
        ],
        "receiptData":{
            "impressionCount":"100",
            "clickCount":5,
            "geo":[
                "United States of America",
                "San Francisco CA"
            ],
            "profile":[
                {
                    "pixelid":"111",
                    "ut1":"abc",
                    "ut2":"def",
                    "ut3":"ghi",
                    "ut4":"jkl",
                    "ut5":"mno"
                },
                {
                    "pixelid":"123",
                    "ut1":"abc",
                    "ut2":"def",
                    "ut3":"ghi",
                    "ut4":"jkl",
                    "ut5":"mno"
                }
            ],
            "matchingSegments":[
                {
                    "segmentName":"AP4 - Art/Culture - In-Market",
                    "segmentID":"kV1mPa2aqPNWKSNtf325",
                    "serviceProvider":"Adobe"
                },
                {
                    "segmentName":"eXelate Australia Demographic - Jobs & Education - Job Seekers",
                    "segmentID":"2213789",
                    "serviceProvider":"exelate"
                }
            ]
        }
    }
}
```

<!-- Changed example from BlueKai (no longer supported) to Exelate -->
