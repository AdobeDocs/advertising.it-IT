---
title: Supporto di Adobe Advertising per il Regolamento generale sulla protezione dei dati
description: Scopri i tipi di richiesta di dati supportati, i valori di configurazione e campi richiesti ed esempi di richieste di accesso API che utilizzano ID prodotto legacy e campi dati restituiti
feature: GDPR
role: User, Developer
exl-id: abf0dc51-e23b-4c9a-95aa-14e0844939bb
source-git-commit: 8e9dac77b4f687fb175adaf27a4e726fa80ca7b4
workflow-type: tm+mt
source-wordcount: '997'
ht-degree: 0%

---

# Supporto di Adobe Advertising per il Regolamento generale sulla protezione dei dati

*Per [!DNL Adobe Advertising Search, Social, & Commerce]; Adobe Advertising DSP; Adobe Advertising Creative; e Adobe Advertising DCO*

>[!IMPORTANT]
>
>Il contenuto di questo documento non rappresenta e non intende sostituirsi a una consulenza legale. Consulta l&#39;assistenza legale per ricevere consigli in merito al Regolamento generale sulla protezione dei dati.

Il Regolamento generale sulla protezione dei dati (RGPD), una legge in vigore dal 25 maggio 2018, conferisce a tutte le persone (soggetti dei dati) all&#39;interno dei confini dell&#39;Unione Europea (UE) il controllo dei loro dati personali e semplifica il contesto normativo per le aziende internazionali. Questa legge si applica a tutte le aziende (titolari del trattamento) che offrono beni o servizi, controllano il comportamento o raccolgono dati personali da individui all&#39;interno dei confini dell&#39;UE nel momento in cui i loro dati personali vengono trattati, indipendentemente dalla sede del titolare del trattamento.

Adobe Experience Cloud agisce come responsabile del trattamento per tutti i dati personali che riceve e archivia per conto dei propri clienti. In qualità di titolare del trattamento dei dati, l’utente determina i dati personali che Adobe Experience Cloud tratta e archivia per suo conto.

In questo documento viene descritto come [!DNL Advertising Search, Social, & Commerce], Advertising Creative, Advertising DSP (Demand Side Platform) e [!DNL Advertising DCO] supportano i diritti all&#39;accesso e all&#39;eliminazione dei dati degli interessati ai sensi del RGPD tramite l&#39;API Adobe Experience Platform Privacy Service e l&#39;interfaccia utente di Privacy Service.

Per ulteriori informazioni sul significato del RGPD per la tua azienda, consulta [RGPD e la tua azienda](https://www.adobe.com/privacy/general-data-protection-regulation.html).

## Tipi di richieste di dati supportati per Adobe Advertising

Adobe Experience Platform consente alle aziende di completare le seguenti attività:

* Accedi ai dati a livello di cookie o ai dati a livello di ID dispositivo di un interessato (per gli annunci nelle app mobili) in [!DNL Search, Social, & Commerce], [!DNL Creative], [!DNL DSP] o [!DNL DCO].
* Eliminare i dati a livello di cookie archiviati in [!DNL Search, Social, & Commerce], [!DNL Creative], [!DNL DSP] o [!DNL DCO] per gli interessati tramite un browser oppure eliminare i dati a livello di ID archiviati in [!DNL DSP] per gli interessati tramite app su dispositivi mobili.
* Controlla lo stato di una o tutte le richieste esistenti.

## Configurazione necessaria per inviare richieste per Adobe Advertising

Per richiedere l’accesso e l’eliminazione dei dati per Adobe Advertising, è necessario:

1. Distribuisci una libreria JavaScript per recuperare e rimuovere i cookie dell’interessato. La stessa libreria, `AdobePrivacy.js`, viene utilizzata per tutte le soluzioni Adobe Experience Cloud.

   >[!IMPORTANT]
   >
   >Le richieste ad alcune soluzioni Experience Cloud non richiedono la libreria JavaScript, ma le richieste ad Adobe Advertising lo richiedono.

   È necessario distribuire la libreria nella pagina Web da cui le persone interessate possono inviare richieste di accesso ed eliminazione, ad esempio il portale della privacy della società. La libreria ti consente di recuperare i cookie [!DNL Adobe] (ID spazio dei nomi: `gsurferID`) in modo da poter inviare queste identità come parte delle richieste di accesso ed eliminazione tramite l&#39;API Adobe Experience Platform Privacy Service.

   Quando l’interessato chiede di cancellare dati personali, la libreria elimina anche il cookie dell’interessato dal browser dell’interessato.

   >[!NOTE]
   >
   >L’eliminazione dei dati personali è diversa dalla rinuncia, che interrompe il targeting di un utente finale con segmenti di pubblico. Tuttavia, quando un interessato richiede di eliminare i dati personali da [!DNL Creative], [!DNL DSP] o [!DNL DCO], la libreria invia anche una richiesta ad Adobe Advertising per rifiutare l&#39;interessato dal targeting dei segmenti. Per gli inserzionisti con [!DNL Search, Social, & Commerce], si consiglia di fornire agli interessati un collegamento a [https://www.adobe.com/privacy/opt-out.html](https://www.adobe.com/privacy/opt-out.html), che spiega come rinunciare al targeting dei segmenti di pubblico.

1. Identifica il tuo ID organizzazione Experience Cloud e assicurati che sia collegato al tuo account Adobe Advertising.

   Un ID organizzazione Experience Cloud è una stringa alfanumerica composta da 24 caratteri a cui segue &quot;@AdobeOrg.&quot; Alla maggior parte dei clienti Experience Cloud è stato assegnato un ID organizzazione. Se il team marketing o l&#39;amministratore di sistema interno di [!DNL Adobe] non conosce l&#39;ID organizzazione o non è sicuro che sia stato eseguito il provisioning, contatta l&#39;Assistenza clienti Adobe all&#39;indirizzo gdprsupport@adobe.com. Per inviare richieste all&#39;API per la privacy utilizzando lo spazio dei nomi `imsOrgID` è necessario l&#39;ID organizzazione.

   >[!IMPORTANT]
   >
   >Contatta il rappresentante Adobe Advertising della tua azienda per verificare che tutti gli account Adobe Advertising della tua organizzazione, inclusi [!DNL DSP] account o inserzionisti, [!DNL Search, Social, & Commerce] account e [!DNL Creative] o [!DNL DCO] account, siano collegati al tuo ID organizzazione Experience Cloud.

1. Utilizza l&#39;[API Adobe Experience Platform Privacy Service](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/privacy-jobs.html) (per le richieste automatizzate) o la [interfaccia utente Privacy Service](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html?lang=it) (per le richieste ad hoc) per inviare richieste di accesso ed eliminazione ad Adobe Advertising per conto delle persone interessate e per controllare lo stato delle richieste esistenti.

   Gli inserzionisti che dispongono di un’app mobile per interagire con gli interessati e avviare campagne con DSP devono scaricare gli SDK per dispositivi mobili compatibili con la privacy per Experience Cloud. Gli SDK di Mobile consentono ai titolari del trattamento dei dati di impostare flag di stato per la rinuncia, recuperare l&#39;ID dispositivo dell&#39;interessato (ID spazio dei nomi: `deviceID`) e inviare richieste all&#39;API Privacy Service. La tua app mobile richiederà una versione di SDK 4.15.0 o successiva.

   Quando invii la richiesta di accesso di una persona interessata, l’API di Privacy Service restituisce le informazioni di tale persona in base al cookie o all’ID dispositivo specificato, che devono quindi essere restituiti alla persona interessata.

   Quando invii la richiesta di cancellazione di una persona interessata, l’ID cookie o l’ID dispositivo e tutti i dati relativi a costi, clic e ricavi associati al cookie vengono eliminati dal server.

   >[!NOTE]
   >
   >Se la tua azienda dispone di più ID organizzazione Experience Cloud, devi inviare richieste API separate per ciascuno di essi. È tuttavia possibile effettuare una richiesta API a più soluzioni secondarie di Adobe Advertising ([!DNL Search, Social, & Commerce], [!DNL Creative], [!DNL DSP] e [!DNL DCO]), con un account per ogni soluzione secondaria.

Tutti i passaggi sono necessari per Adobe Advertising. Per ulteriori informazioni su queste e altre attività correlate che è necessario eseguire utilizzando Adobe Experience Platform Privacy Service e dove trovare gli elementi necessari, vedere &quot;[Panoramica di Privacy Service](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html).&quot;

## Valori campo obbligatori nelle richieste JSON di Adobe Advertising

`"company context":`

* `"namespace": **imsOrgID**`
* `"value":` &lt;*ID organizzazione Experience Cloud*>

`"users":`

* `"key":` &lt;*in genere il nome dell&#39;interessato*>

* `"action":` `**access**` o `**delete**`

* `"user IDs":`

   * `"namespace": **411**` (che indica lo spazio cookie [!DNL adcloud])

   * `"value":` &lt;*valore ID cookie effettivo dell&#39;interessato recuperato da`AdobePrivacy.js`*>

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
