---
title: Supporto pubblicitario Adobe per il regolamento generale sulla protezione dei dati
description: Scopri i tipi di richiesta di dati supportati, i valori di configurazione e campo richiesti e gli esempi di richieste di accesso API utilizzando ID di prodotto legacy e i campi di dati restituiti
feature: GDPR
exl-id: abf0dc51-e23b-4c9a-95aa-14e0844939bb
source-git-commit: 7f35b3f3b33ed320ac186d219cbd0f826666bb3b
workflow-type: tm+mt
source-wordcount: '1033'
ht-degree: 0%

---

# Supporto pubblicitario Adobe per il regolamento generale sulla protezione dei dati

*Per [!DNL Adobe Advertising Search, Social, & Commerce]; DSP pubblicitaria Adobe; Adobe Advertising Creative; e Adobe Advertising DCO*

>[!IMPORTANT]
>
>Il contenuto di questo documento non rappresenta e non intende sostituirsi a una consulenza legale. Consulta il tuo consulente legale per ricevere consigli sul Regolamento generale sulla protezione dei dati.

Il Regolamento generale sulla protezione dei dati (RGPD), una legge in vigore dal 25 maggio 2018, conferisce a tutte le persone (soggetti dei dati) all’interno dei confini dell’Unione Europea (UE) il controllo dei propri dati personali e semplifica il contesto normativo per le imprese internazionali. La presente legge si applica a tutte le aziende (titolari del trattamento dei dati) che offrono beni o servizi, che controllano il comportamento o raccolgono dati personali da persone all&#39;interno dei confini dell&#39;UE al momento del trattamento dei loro dati personali, indipendentemente dalla sede del titolare del trattamento.

Adobe Experience Cloud agisce come responsabile del trattamento dei dati personali ricevuti e archiviati per conto dei propri clienti. In qualità di titolare del trattamento dei dati, l’utente determina i dati personali elaborati e archiviati da Adobe Experience Cloud per suo conto.

Questo documento descrive come [!DNL Advertising Search, Social, & Commerce]; Advertising Creative; DSP pubblicitario (Demand Side Platform); e [!DNL Advertising DCO] supporta i diritti di accesso e cancellazione dei dati degli interessati in base al RGPD tramite l’API di Adobe Experience Platform Privacy Service e l’interfaccia utente di Privacy Service.

Per ulteriori informazioni sul significato del RGPD per la tua azienda, consulta [RGPD e la tua azienda](https://www.adobe.com/privacy/general-data-protection-regulation.html).

## Tipi di richieste di dati supportati per Adobe Advertising

Adobe Experience Platform consente alle aziende di completare le seguenti attività:

* Accedi ai dati a livello di cookie di una persona interessata o ai dati a livello di ID dispositivo (per gli annunci nelle app mobili) all&#39;interno di [!DNL Search, Social, & Commerce], [!DNL Creative], [!DNL DSP]oppure [!DNL DCO].
* Elimina i dati a livello di cookie memorizzati in [!DNL Search, Social, & Commerce], [!DNL Creative], [!DNL DSP]oppure [!DNL DCO] per le persone interessate che utilizzano un browser; o elimina i dati a livello di ID memorizzati in [!DNL DSP] per le persone interessate che utilizzano app su dispositivi mobili.
* Controlla lo stato di una o tutte le richieste esistenti.

## Configurazione necessaria per inviare richieste per Adobe di pubblicità

Per richiedere l’accesso e l’eliminazione di dati per Adobe Advertising, è necessario:

1. Distribuisci una libreria JavaScript per recuperare e rimuovere i cookie dell’interessato dei dati. La stessa libreria, `AdobePrivacy.js`, viene utilizzato per tutte le soluzioni Adobe Experience Cloud.

   >[!IMPORTANT]
   >
   >Le richieste ad alcune soluzioni Adobe Experience Cloud non richiedono la libreria JavaScript, ma richieste ad Adobe Advertising lo richiedono.

   Devi distribuire la libreria sulla pagina web dalla quale gli interessati possono inviare le richieste di accesso ed eliminazione, ad esempio il portale per la privacy della tua azienda. La libreria consente di recuperare i cookie di Adobe (ID dello spazio dei nomi: `gsurferID`) per poter inviare queste identità come parte delle richieste di accesso ed eliminazione tramite l’API Adobe Experience Platform Privacy Service.

   Quando l’interessato chiede di eliminare i dati personali, la libreria elimina anche il cookie dell’interessato dal browser dell’interessato.

   >[!NOTE]
   >
   >L’eliminazione dei dati personali è diversa dalla rinuncia, che interrompe il targeting di un utente finale con segmenti di pubblico. Tuttavia, quando una persona interessata chiede di cancellare i dati personali da [!DNL Creative], [!DNL DSP]oppure [!DNL DCO], la libreria invia anche una richiesta ad Adobe Advertising per rifiutare la persona interessata dal targeting dei segmenti. Per gli inserzionisti con [!DNL Search, Social, & Commerce], ti consigliamo di fornire alle persone interessate un collegamento a [https://www.adobe.com/privacy/opt-out.html](https://www.adobe.com/privacy/opt-out.html), che spiega come rinunciare al targeting per segmenti di pubblico.

1. Identifica l’ID organizzazione Experience Cloud e accertati che sia collegato ai tuoi account Adobe Advertising.

   Un ID organizzazione Experience Cloud è una stringa alfanumerica composta da 24 caratteri, con l&#39;aggiunta di &quot;@AdobeOrg.&quot; Alla maggior parte dei clienti di Experience Cloud è stato assegnato un ID organizzazione. Se il team di marketing o l’amministratore di sistema di Adobe interno non conosce l’ID organizzazione o se non è sicuro che sia stato eseguito il provisioning, contatta l’Assistenza clienti Adobe all’indirizzo gdprsupport@adobe.com. Per inviare richieste all’API Privacy è necessario l’ID organizzazione tramite l’ `imsOrgID` spazio dei nomi.

   >[!IMPORTANT]
   >
   >Contatta il rappresentante pubblicitario Adobe della tua azienda per confermare che tutti gli account pubblicitari Adobi della tua organizzazione, compresi [!DNL DSP] account o inserzionisti, [!DNL Search, Social, & Commerce] conti e [!DNL Creative] o [!DNL DCO] account - sono collegati all&#39;ID organizzazione Experience Cloud.

1. Utilizza [API Adobe Experience Platform Privacy Service](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/privacy-jobs.html) (per le richieste automatizzate) o [Interfaccia utente di Privacy Service](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html) (per richieste ad hoc) per inviare le richieste di accesso ed eliminazione ad Adobe Advertising per conto delle persone interessate e per controllare lo stato delle richieste esistenti.

   Per gli inserzionisti che dispongono di un’app mobile per interagire con gli interessati e avviare campagne con DSP, dovrai scaricare ad Experience Cloud gli SDK per dispositivi mobili pronti per la privacy. Gli SDK di Mobile consentono ai titolari del trattamento di impostare i flag di stato della rinuncia, recuperare l’ID dispositivo dell’interessato (ID namespace: deviceID) e invia richieste all’API di Privacy Service. La tua app mobile richiederà una versione SDK 4.15.0 o successiva.

   Quando invii una richiesta di accesso della persona interessata, l’API di Privacy Service restituisce le informazioni della persona interessata in base al cookie o all’ID dispositivo specificati, che devi quindi restituire alla persona interessata.

   Quando invii una richiesta di cancellazione dell’interessato, l’ID cookie o l’ID dispositivo e tutti i dati relativi a costi, clic e ricavi associati al cookie vengono eliminati dal server.

   >[!NOTE]
   Se la tua azienda dispone di più ID organizzazione Experience Cloud, devi inviare richieste API separate per ciascuna di esse. Tuttavia puoi effettuare una richiesta API a più soluzioni secondarie di Adobe Advertising ([!DNL Search, Social, & Commerce], [!DNL Creative], [!DNL DSP]e [!DNL DCO]), con un account per soluzione secondaria.

Tutti questi passaggi sono necessari per Adobe la pubblicità. Per ulteriori informazioni su queste e altre attività correlate che devi eseguire utilizzando Adobe Experience Platform Privacy Service e su dove trovare gli elementi necessari, vedi [www.adobe.io/apis/cloudplatform/gdpr.html](https://www.adobe.io/apis/experienceplatform/gdpr.html).

## Valori campo obbligatori nelle richieste JSON per pubblicità Adobe

&quot;&quot;contesto aziendale&quot;:

* `"namespace": **imsOrgID**`
* `"value":` &lt;*valore ID organizzazione IMS*>

`"users":`

* `"key":` &lt;*in genere il nome della persona interessata*>

* `"action":` o `**access**` o `**delete**`

* `"user IDs":`

   * `"namespace": **411**` (che indica [!DNL adcloud] spazio dei cookie)

   * `"value":` &lt;*il valore ID cookie dell’interessato effettivo come recuperato da`AdobePrivacy.js`*>

* `"include": **adCloud**` (che è il prodotto Adobe che si applica alla richiesta)

* `"regulation": **gdpr**` (regolamento sulla privacy applicabile alla richiesta)

## Esempio di richiesta inviata dall’interessato utilizzando un ID utente pubblicitario Adobe recuperato da `AdobePrivacy.js`

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
                    "segmentName":"EMEA - UK - Health Food Buyers",
                    "segmentID":"eP2oJ2UPsfsDVDhvlGewx",
                    "serviceProvider":"BlueKai"
                }
            ]
        }
    }
}
```
