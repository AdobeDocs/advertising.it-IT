---
title: Supporto Adobe Advertising per il regolamento generale sulla protezione dei dati
description: Scopri i tipi di richiesta di dati supportati, i valori di configurazione e campi richiesti ed esempi di richieste di accesso API che utilizzano ID prodotto legacy e campi dati restituiti
feature: GDPR
role: User, Developer
exl-id: abf0dc51-e23b-4c9a-95aa-14e0844939bb
source-git-commit: 80072930c0506a017a927ce53eaad900a2642e92
workflow-type: tm+mt
source-wordcount: '1002'
ht-degree: 0%

---

# Supporto Adobe Advertising per il regolamento generale sulla protezione dei dati

*Per [!DNL Adobe Advertising Search, Social, & Commerce]; Adobe Advertising DSP; Adobe Advertising Creative; e Adobe Advertising DCO*

>[!IMPORTANT]
>
>Il contenuto di questo documento non rappresenta e non intende sostituirsi a una consulenza legale. Consulta l&#39;assistenza legale per ricevere consigli in merito al Regolamento generale sulla protezione dei dati.

Il Regolamento generale sulla protezione dei dati (RGPD), una legge in vigore dal 25 maggio 2018, conferisce a tutte le persone (soggetti dei dati) all&#39;interno dei confini dell&#39;Unione Europea (UE) il controllo dei loro dati personali e semplifica il contesto normativo per le aziende internazionali. Questa legge si applica a tutte le aziende (titolari del trattamento) che offrono beni o servizi, controllano il comportamento o raccolgono dati personali da individui all&#39;interno dei confini dell&#39;UE nel momento in cui i loro dati personali vengono trattati, indipendentemente dalla sede del titolare del trattamento.

Adobe Experience Cloud agisce come responsabile del trattamento per tutti i dati personali che riceve e archivia per conto dei propri clienti. In qualità di titolare del trattamento dei dati, l’utente determina i dati personali che Adobe Experience Cloud tratta e archivia per suo conto.

Questo documento descrive come [!DNL Advertising Search, Social, & Commerce]; Advertising Creative; pubblicità DSP (Demand Side Platform); e [!DNL Advertising DCO] supporta i diritti all’accesso e all’eliminazione dei dati degli interessati ai sensi del RGPD tramite l’API Adobe Experience Platform Privacy Service e l’interfaccia utente di Privacy Service.

Per ulteriori informazioni sul significato del RGPD per la tua attività, consulta [Il RGPD e la tua azienda](https://www.adobe.com/privacy/general-data-protection-regulation.html).

## Tipi di richieste di dati supportati per Adobe Advertising

Adobe Experience Platform consente alle aziende di completare le seguenti attività:

* Accedere ai dati a livello di cookie di una persona interessata o ai dati a livello di ID del dispositivo (per gli annunci nelle app mobili) in [!DNL Search, Social, & Commerce], [!DNL Creative], [!DNL DSP], o [!DNL DCO].
* Eliminare i dati a livello di cookie memorizzati in [!DNL Search, Social, & Commerce], [!DNL Creative], [!DNL DSP], o [!DNL DCO] per gli interessati che utilizzano un browser; o eliminare i dati a livello di ID memorizzati in [!DNL DSP] per gli interessati che utilizzano app su dispositivi mobili.
* Controlla lo stato di una o tutte le richieste esistenti.

## Configurazione necessaria per inviare richieste per Adobe Advertising

Ad Adobe Advertising, per richiedere l’accesso e l’eliminazione dei dati devi effettuare le seguenti operazioni:

1. Distribuisci una libreria JavaScript per recuperare e rimuovere i cookie dell’interessato. La stessa libreria, `AdobePrivacy.js`, viene utilizzato per tutte le soluzioni Adobe Experience Cloud.

   >[!IMPORTANT]
   >
   >Le richieste ad alcune soluzioni Experience Cloud non richiedono la libreria JavaScript, ma le richieste ad Adobi Advertising la richiedono.

   È necessario distribuire la libreria nella pagina Web da cui le persone interessate possono inviare richieste di accesso ed eliminazione, ad esempio il portale della privacy della società. La libreria ti aiuta a recuperare [!DNL Adobe] cookie (ID spazio dei nomi: `gsurferID`) in modo da poter inviare queste identità come parte delle richieste di accesso ed eliminazione tramite l’API Adobe Experience Platform Privacy Service.

   Quando l’interessato chiede di cancellare dati personali, la libreria elimina anche il cookie dell’interessato dal browser dell’interessato.

   >[!NOTE]
   >
   >L’eliminazione dei dati personali è diversa dalla rinuncia, che interrompe il targeting di un utente finale con segmenti di pubblico. Tuttavia, quando un interessato chiede di cancellare dati personali da [!DNL Creative], [!DNL DSP], o [!DNL DCO], la libreria invia anche una richiesta ad Adobi Advertising affinché rifiuti l’interessato dal targeting dei segmenti. Per gli inserzionisti con [!DNL Search, Social, & Commerce], si consiglia di fornire alle persone interessate un collegamento a [https://www.adobe.com/privacy/opt-out.html](https://www.adobe.com/privacy/opt-out.html), che spiega come rinunciare al targeting dei segmenti di pubblico.

1. Identifica l’ID organizzazione Experience Cloud e assicurati che sia collegato ai tuoi account Adobi Advertising.

   Un ID organizzazione di Experience Cloud è una stringa alfanumerica composta da 24 caratteri a cui segue &quot;@AdobeOrg.&quot; Alla maggior parte dei clienti Experience Cloud è stato assegnato un ID organizzazione. Se il team marketing o interno [!DNL Adobe] l’amministratore di sistema non conosce il tuo ID organizzazione o non è sicuro che sia stato eseguito il provisioning, quindi contatta l’Assistenza clienti Adobe all’indirizzo gdprsupport@adobe.com. Per inviare richieste all&#39;API per la privacy utilizzando l&#39;ID organizzazione `imsOrgID` spazio dei nomi.

   >[!IMPORTANT]
   >
   >Contatta il rappresentante Adobe Advertising della tua azienda per verificare che tutti gli account Adobi Advertising della tua organizzazione, tra cui [!DNL DSP] account o inserzionisti, [!DNL Search, Social, & Commerce] conti, e [!DNL Creative] o [!DNL DCO] account — sono collegati al tuo ID organizzazione Experience Cloud.

1. Utilizza il [API ADOBE EXPERIENCE PLATFORM PRIVACY SERVICE](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/privacy-jobs.html) (per le richieste automatizzate) o [Interfaccia utente di Privacy Service](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html?lang=it) (per le richieste ad hoc) di inviare le richieste di accesso e di cancellazione all’Adobi Advertising per conto delle persone interessate e di verificare lo stato delle richieste esistenti.

   Per gli inserzionisti che dispongono di un’app mobile per interagire con le persone interessate e avviare campagne con l’DSP, ad Experience Cloud dovrai scaricare gli SDK per dispositivi mobili predisposti per la privacy. Gli SDK di Mobile consentono ai titolari del trattamento dei dati di impostare i flag di stato per la rinuncia e di recuperare l’ID dispositivo dell’interessato (ID spazio dei nomi: `deviceID`) e invia richieste all’API Privacy Service. La tua app mobile richiederà una versione SDK 4.15.0 o successiva.

   Quando invii la richiesta di accesso di una persona interessata, l’API Privacy Service restituisce le informazioni di tale persona in base al cookie o all’ID dispositivo specificato, che dovranno quindi essere restituiti alla persona interessata.

   Quando invii la richiesta di cancellazione di una persona interessata, l’ID cookie o l’ID dispositivo e tutti i dati relativi a costi, clic e ricavi associati al cookie vengono eliminati dal server.

   >[!NOTE]
   >
   >Se la tua azienda dispone di più ID organizzazione Experience Cloud, devi inviare richieste API separate per ciascuno di essi. Tuttavia, puoi effettuare una richiesta API a più soluzioni secondarie Adobi Advertising ([!DNL Search, Social, & Commerce], [!DNL Creative], [!DNL DSP], e [!DNL DCO]), con un account per ogni soluzione secondaria.

Tutti questi passaggi sono necessari, ad Adobe Advertising. Per ulteriori informazioni su queste e altre attività correlate che è necessario eseguire utilizzando Adobe Experience Platform Privacy Service e dove trovare gli elementi necessari, vedere &quot;[Panoramica di Privacy Service](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html).&quot;

## Valori campo obbligatori nelle richieste JSON Adobi Advertising

`"company context":`

* `"namespace": **imsOrgID**`
* `"value":` &lt;*il tuo ID organizzazione Experience Cloud*>

`"users":`

* `"key":` &lt;*in genere il nome dell’interessato*>

* `"action":` o `**access**` o `**delete**`

* `"user IDs":`

   * `"namespace": **411**` (che indica il [!DNL adcloud] spazio cookie)

   * `"value":` &lt;*il valore ID cookie effettivo dell’interessato recuperato da`AdobePrivacy.js`*>

* `"include": **adCloud**` (che è il [!DNL Adobe] prodotto applicabile alla richiesta)

* `"regulation": **gdpr**` (regolamento sulla privacy applicabile alla richiesta)

## Esempio di richiesta inviata dall’interessato utilizzando un ID utente Adobe Advertising recuperato da `AdobePrivacy.js`

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

Di seguito è riportato un Adobe Advertising di risposta di accesso.

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
