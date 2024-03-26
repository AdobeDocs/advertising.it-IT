---
title: 'Adobe Advertising di supporto per il California Consumer Privacy Act: supporto per l’accesso e l’eliminazione dei dati dei consumatori'
description: Scopri i tipi di richiesta di dati supportati, i valori di configurazione e campi richiesti ed esempi di richieste di accesso API che utilizzano ID prodotto legacy e campi dati restituiti.
feature: CCPA
role: User, Developer
exl-id: e7808411-7dc3-499c-bda1-1f5882f651b2
source-git-commit: 5edcd810c86f3b3ae65ccc92748177fa8cd0765e
workflow-type: tm+mt
source-wordcount: '1042'
ht-degree: 0%

---

# Adobe Advertising di supporto per il California Consumer Privacy Act: supporto per l’accesso e l’eliminazione dei dati dei consumatori

*Per [!DNL Adobe Advertising Search, Social, & Commerce]; Adobe Advertising DSP; Adobe Advertising Creative; e Adobe Advertising DCO*

>[!IMPORTANT]
>
>Il contenuto di questo documento non rappresenta e non intende sostituirsi a una consulenza legale. Consulta il tuo consulente legale per ricevere consigli in merito al California Consumer Privacy Act.

Il California Consumer Privacy Act (CCPA) è la nuova legge sulla privacy della California, in vigore dal 1° gennaio 2020. Il CCPA conferisce ai residenti della California nuovi diritti in merito alle loro informazioni personali e impone responsabilità in materia di protezione dei dati a determinate entità che conducono attività commerciali in California. Il CCPA garantisce ai consumatori il diritto di accedere ai propri dati personali e di cancellarli, nonché il diritto di non partecipare a determinate attività che possono essere considerate di &quot;vendita&quot; di informazioni personali a terzi.

In qualità di azienda, potrai determinare i dati personali che Adobe Experience Cloud tratta e archivia per tuo conto.

In qualità di fornitore di servizi, Adobi Advertising fornisce supporto alla tua azienda per l’adempimento dei suoi obblighi in virtù del CCPA applicabili all’utilizzo di prodotti e servizi di Adobe Advertising, inclusa la gestione delle richieste di accesso e cancellazione delle informazioni personali e la gestione delle richieste di rinuncia alla vendita di tali informazioni.

Questo documento descrive come [!DNL Advertising Search, Social, & Commerce]; Advertising Creative; pubblicità DSP (Demand Side Platform); e [!DNL Advertising DCO] — in qualità di fornitori di servizi — sostenere il diritto dei consumatori di accedere alle informazioni personali e di cancellarle utilizzando l&#39;Adobe [!DNL Experience Platform Privacy Service API] e [!DNL Privacy Service UI].

Per informazioni su come Advertising DSP supporta il diritto del consumatore di non partecipare alla vendita di informazioni personali, consulta [Adobe Advertising di supporto per il California Consumer Privacy Act: supporto per la rinuncia del consumatore](/help/privacy/ccpa/ccpa-opt-out-of-sale.md).

Per ulteriori informazioni sull&#39;Adobe dei servizi per la privacy relativi al CCPA, vedere [Centro per la privacy di Adobe](https://www.adobe.com/privacy/ccpa.html).

## Tipi di richieste di dati supportati per Adobe Advertising

Adobe Experience Platform consente alle aziende di completare le seguenti attività:

* Accedere ai dati a livello di cookie di un consumatore o ai dati a livello di ID del dispositivo (per gli annunci nelle app mobili) in [!DNL Search, Social, & Commerce], [!DNL Creative], [!DNL DSP], o [!DNL DCO].
* Eliminare i dati a livello di cookie memorizzati in [!DNL Search, Social, & Commerce], [!DNL Creative], [!DNL DSP], o [!DNL DCO] per i consumatori che utilizzano un browser; o eliminare i dati a livello di ID memorizzati in [!DNL DSP] per i consumatori che utilizzano app su dispositivi mobili.
* Controlla lo stato di una o tutte le richieste esistenti.

## Configurazione necessaria per inviare richieste per Adobe Advertising

Per richiedere l’accesso e la cancellazione delle informazioni personali dei consumatori da Adobi Advertising, è necessario:

1. Distribuisci una libreria JavaScript per recuperare e rimuovere i cookie del cliente. La stessa libreria, `AdobePrivacy.js`, viene utilizzato per tutte le soluzioni Adobe Experience Cloud.

   >[!IMPORTANT]
   >
   >Le richieste ad alcune soluzioni Experience Cloud non richiedono la libreria JavaScript, ma le richieste ad Adobi Advertising la richiedono.

   Devi distribuire la libreria sulla pagina web da cui i clienti possono inviare richieste di accesso ed eliminazione, come ad esempio il portale della privacy della tua azienda. La libreria ti aiuta a recuperare i cookie Adobe (ID spazio dei nomi: `gsurferID`) in modo da poter inviare queste identità come parte delle richieste di accesso ed eliminazione tramite [!DNL Adobe Experience Platform Privacy Service API].

   Quando il cliente chiede di eliminare i dati personali, la libreria elimina anche il cookie del cliente dal browser del cliente.

   >[!NOTE]
   >
   >L’eliminazione dei dati personali è diversa dalla rinuncia, che interrompe il targeting di un utente finale con segmenti di pubblico. Tuttavia, quando un consumatore chiede di cancellare dati personali da [!DNL Creative], [!DNL DSP], o [!DNL DCO], la libreria invia anche una richiesta ad Adobi Advertising per rifiutare il cliente dal targeting dei segmenti. Per gli inserzionisti con [!DNL Search, Social, & Commerce], si consiglia di fornire ai clienti un collegamento a [https://www.adobe.com/privacy/opt-out.html#customeruse](https://www.adobe.com/privacy/opt-out.html#customeruse), che spiega come rinunciare al targeting dei segmenti di pubblico.

1. Identifica l’ID organizzazione Experience Cloud e assicurati che sia collegato ai tuoi account Adobi Advertising.

   Un ID organizzazione di Experience Cloud è una stringa alfanumerica composta da 24 caratteri a cui segue &quot;@AdobeOrg.&quot; Alla maggior parte dei clienti Experience Cloud è stato assegnato un ID organizzazione. Se il team marketing o interno [!DNL Adobe] l’amministratore di sistema non conosce il tuo ID organizzazione o non è sicuro che sia stato eseguito il provisioning, quindi contatta il team del tuo account Adobe. Per inviare richieste all&#39;API per la privacy utilizzando l&#39;ID organizzazione `imsOrgID` spazio dei nomi.

   >[!IMPORTANT]
   >
   >Contatta il rappresentante Adobe Advertising della tua azienda per verificare che tutti gli account Adobi Advertising della tua organizzazione, tra cui [!DNL DSP] account o inserzionisti, [!DNL Search, Social, & Commerce] conti, e [!DNL Creative] o [!DNL DCO] account — sono collegati al tuo ID organizzazione Experience Cloud.

1. Utilizza il [API ADOBE EXPERIENCE PLATFORM PRIVACY SERVICE](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/privacy-jobs.html) (per le richieste automatizzate) o [Interfaccia utente di Privacy Service](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html?lang=it) (per richieste ad hoc) di inviare richieste di accesso e cancellazione di informazioni personali agli Adobi Advertising per conto dei consumatori e di verificare lo stato delle richieste esistenti.

   Per gli inserzionisti che dispongono di un’app mobile per interagire con i clienti e avviare campagne con [!DNL DSP], ad Experience Cloud, dovrai scaricare gli SDK per dispositivi mobili predisposti per la privacy. Gli SDK di Mobile consentono alle aziende di impostare flag di stato per la rinuncia e recuperare l’ID dispositivo del consumatore (ID spazio dei nomi: `deviceID`) e invia richieste all’API Privacy Service. La tua app mobile richiederà una versione SDK 4.15.0 o successiva.

   Quando invii una richiesta di accesso consumer, l’API Privacy Service restituisce le informazioni di un consumatore in base al cookie o all’ID dispositivo specificato, che devono quindi essere restituiti al consumatore.

   Quando invii una richiesta di cancellazione del consumatore, l’ID del cookie o dell’ID del dispositivo e tutti i dati relativi a costi, clic e ricavi associati al cookie vengono eliminati dal server.

   >[!NOTE]
   >
   >Se la tua azienda dispone di più ID organizzazione Experience Cloud, devi inviare richieste API separate per ciascuno di essi. Tuttavia, puoi effettuare una richiesta API a più soluzioni secondarie Adobi Advertising ([!DNL Search, Social, & Commerce], [!DNL Creative], [!DNL DSP], e [!DNL DCO]), con un account per ogni soluzione secondaria.

Tutti questi passaggi sono necessari per ricevere supporto da Adobi Advertising. Per ulteriori informazioni su queste e altre attività correlate che è necessario eseguire utilizzando Adobe Experience Platform Privacy Service e dove trovare gli elementi necessari, vedere [https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html).

## Valori campo obbligatori nelle richieste JSON Adobi Advertising

`"company context":`

* `"namespace": **imsOrgID**`
* `"value":` &lt;*il tuo ID organizzazione Experience Cloud*>

&quot;users&quot; (utenti):

* `"key":` &lt;*di solito il nome del cliente*>

* `"action":` o `**access**` o `**delete**`

* `"user IDs":`

   * `"namespace": **411**` (che indica il [!DNL adcloud] spazio cookie)

   * `"value":` &lt;*il valore ID cookie del cliente effettivo recuperato da`AdobePrivacy.js`*>

* `"include": **adCloud**` (che è il [!DNL Adobe] prodotto applicabile alla richiesta)

* `"regulation": **ccpa**` (regolamento sulla privacy applicabile alla richiesta)

## Esempio di richiesta inviata da un consumatore utilizzando un ID utente Adobe Advertising recuperato da AdobePrivacy.js

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
    "regulation":"ccpa"
}
```

## Campi dati restituiti per le richieste di accesso

Di seguito è riportato un esempio di risposta di accesso alle informazioni personali, ad Adobe Advertising.

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
