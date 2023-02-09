---
title: 'Supporto pubblicitario Adobe per il California Consumer Privacy Act : Supporto per l’accesso e l’eliminazione dei dati dei clienti'
description: Scopri i tipi di richiesta di dati supportati, i valori di configurazione e campo richiesti e alcuni esempi di richieste di accesso API utilizzando ID di prodotto legacy e i campi di dati restituiti.
feature: CCPA
exl-id: e7808411-7dc3-499c-bda1-1f5882f651b2
source-git-commit: bc0015c134406fb020370def45a8588b5032587e
workflow-type: tm+mt
source-wordcount: '1075'
ht-degree: 0%

---

# Adobe di supporto per la pubblicità per il California Consumer Privacy Act: Supporto per l’accesso e l’eliminazione dei dati dei clienti

*Per [!DNL Adobe Advertising Search]; DSP pubblicitaria Adobe; Adobe Advertising Creative; e Adobe Advertising DCO*

>[!IMPORTANT]
>
>Il contenuto di questo documento non rappresenta e non intende sostituirsi a una consulenza legale. Consulta il tuo consulente legale per ricevere consigli in merito al California Consumer Privacy Act.

Il California Consumer Privacy Act (CCPA) è la nuova legge sulla privacy della California, in vigore dal 1° gennaio 2020. Il CCPA conferisce ai residenti della California nuovi diritti in merito alle loro informazioni personali e impone responsabilità in materia di protezione dei dati a determinate entità che conducono attività commerciali in California. Il CCPA garantisce ai consumatori il diritto di accedere ai propri dati personali e di cancellarli, nonché il diritto di rinunciare a determinate attività che possono essere considerate come &quot;vendita&quot; di informazioni personali a terzi.

In qualità di azienda, puoi determinare i dati personali elaborati e archiviati da Adobe Experience Cloud per tuo conto.

In qualità di fornitore di servizi, Adobe Advertising fornisce supporto alla tua azienda per adempiere ai suoi obblighi in virtù del CCPA applicabili all&#39;uso di prodotti e servizi Adobe Advertising, inclusa la gestione delle richieste di accesso e cancellazione di informazioni personali e la gestione delle richieste di rinuncia alla vendita di informazioni personali.

Questo documento descrive come [!DNL Advertising Search]; Advertising Creative; DSP pubblicitario (Demand Side Platform); e [!DNL Advertising DCO] — in qualità di fornitori di servizi — sostenere i diritti dei consumatori di accedere e cancellare informazioni personali utilizzando l&#39;Adobe [!DNL Experience Platform Privacy Service API] e [!DNL Privacy Service UI].

Per informazioni su come Advertising DSP supporta il diritto del consumatore di rinunciare alla vendita di informazioni personali, vedi [Adobe di supporto per la pubblicità per il California Consumer Privacy Act: Supporto per rinuncia del consumatore](/help/privacy/ccpa/ccpa-opt-out-of-sale.md).

Per ulteriori informazioni sull’Adobe dei servizi di privacy per il CCPA, consulta la sezione [Centro per la privacy Adobe](https://www.adobe.com/privacy/ccpa.html).

## Tipi di richieste di dati supportati per Adobe Advertising

Adobe Experience Platform consente alle aziende di completare le seguenti attività:

* Accedi ai dati a livello di cookie di un consumatore o ai dati a livello di ID dispositivo (per gli annunci nelle app mobili) all&#39;interno di [!DNL Search], [!DNL Creative], [!DNL DSP]oppure [!DNL DCO].
* Elimina i dati a livello di cookie memorizzati in [!DNL Search], [!DNL Creative], [!DNL DSP]oppure [!DNL DCO] per i consumatori che utilizzano un browser; o elimina i dati a livello di ID memorizzati in [!DNL DSP] per i consumatori che utilizzano app su dispositivi mobili.
* Controlla lo stato di una o tutte le richieste esistenti.

## Configurazione necessaria per inviare richieste per Adobe di pubblicità

Per richiedere l’accesso e l’eliminazione delle informazioni personali dei consumatori da Adobe Advertising, è necessario:

1. Distribuisci una libreria JavaScript per recuperare e rimuovere i cookie del cliente. La stessa libreria, `AdobePrivacy.js`, viene utilizzato per tutte le soluzioni Adobe Experience Cloud.

   >[!IMPORTANT]
   >
   >Le richieste ad alcune soluzioni Experience Cloud non richiedono la libreria JavaScript, ma richieste ad Adobe Advertising lo richiedono.

   Devi distribuire la libreria sulla pagina web da cui i clienti possono inviare le richieste di accesso ed eliminazione, ad esempio il portale per la privacy della tua azienda. La libreria consente di recuperare i cookie di Adobe (ID dello spazio dei nomi: `gsurferID`) per poter inviare queste identità come parte delle richieste di accesso ed eliminazione tramite la [!DNL Adobe Experience Platform Privacy Service API].

   Quando il cliente richiede di eliminare i dati personali, la libreria elimina anche il cookie del cliente dal browser del cliente.

   >[!NOTE]
   >
   >L’eliminazione dei dati personali è diversa dalla rinuncia, che interrompe il targeting di un utente finale con segmenti di pubblico. Tuttavia, quando un consumatore chiede di cancellare i dati personali da [!DNL Creative], [!DNL DSP]oppure [!DNL DCO], la libreria invia anche una richiesta ad Adobe Advertising per rifiutare il targeting del cliente per segmenti. Per gli inserzionisti con [!DNL Search], consigliamo di fornire ai clienti un collegamento a [https://www.adobe.com/privacy/opt-out.html#customeruse](https://www.adobe.com/privacy/opt-out.html#customeruse), che spiega come rinunciare al targeting per segmenti di pubblico.

1. Identifica l’ID organizzazione Experience Cloud e assicurati che sia collegato ai tuoi account Adobe Advertising.

   Un ID organizzazione Experience Cloud è una stringa alfanumerica composta da 24 caratteri, con l&#39;aggiunta di &quot;@AdobeOrg.&quot; Alla maggior parte dei clienti di Experience Cloud è stato assegnato un ID organizzazione. Se il team di marketing o l’amministratore di sistema di Adobe interno non conosce l’ID organizzazione o se non è sicuro che sia stato eseguito il provisioning, contatta l’Assistenza clienti Adobe all’indirizzo gdprsupport@adobe.com. Per inviare richieste all’API Privacy è necessario l’ID organizzazione tramite l’ `imsOrgID` spazio dei nomi.

   >[!IMPORTANT]
   >
   >Contatta il rappresentante pubblicitario Adobe della tua azienda per confermare che tutti gli account pubblicitari Adobi della tua organizzazione, compresi [!DNL DSP] account o inserzionisti, [!DNL Search] conti e [!DNL Creative] o [!DNL DCO] account - sono collegati all&#39;ID organizzazione Experience Cloud.

1. Utilizza [API Adobe Experience Platform Privacy Service](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/privacy-jobs.html) (per le richieste automatizzate) o [Interfaccia utente di Privacy Service](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html) (per richieste ad hoc) per inviare richieste di accesso e cancellazione di informazioni personali ad Adobe Advertising per conto dei consumatori e per controllare lo stato delle richieste esistenti.

   Per gli inserzionisti che dispongono di un’app mobile per interagire con i clienti e avviare campagne con [!DNL DSP], ad Experience Cloud, dovrai scaricare gli SDK per dispositivi mobili compatibili con la privacy. Gli SDK di Mobile consentono alle aziende di impostare i flag di stato della rinuncia, recuperare l’ID dispositivo del consumatore (ID namespace: `deviceID`) e invia richieste all’API di Privacy Service. La tua app mobile richiederà una versione SDK 4.15.0 o successiva.

   Quando invii una richiesta di accesso del consumatore, l’API di Privacy Service restituisce le informazioni di un consumatore in base al cookie o all’ID dispositivo specificato, che devi quindi restituire al consumatore.

   Quando invii una richiesta di cancellazione del consumatore, l’ID cookie o l’ID dispositivo e tutti i dati relativi a costi, clic e ricavi associati al cookie vengono eliminati dal server.

   >[!NOTE]
   Se la tua azienda dispone di più ID organizzazione Experience Cloud, devi inviare richieste API separate per ciascuna di esse. Tuttavia puoi effettuare una richiesta API a più soluzioni secondarie di Adobe Advertising ([!DNL Search], [!DNL Creative], [!DNL DSP]e [!DNL DCO]), con un account per soluzione secondaria.

Tutti questi passaggi sono necessari per ricevere il supporto da Adobe Advertising. Per ulteriori informazioni su queste e altre attività correlate che devi eseguire utilizzando Adobe Experience Platform Privacy Service e su dove trovare gli elementi necessari, vedi [https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html).

## Valori campo obbligatori nelle richieste JSON per pubblicità Adobe

`"company context":`

* `"namespace": **imsOrgID**`
* `"value":` &lt;*l&#39;ID organizzazione Experience Cloud*>

&quot;utenti&quot;:

* `"key":` &lt;*di solito il nome del cliente*>

* `"action":` o `**access**` o `**delete**`

* `"user IDs":`

   * `"namespace": **411**` (che indica lo spazio dei cookie adcloud)

   * `"value":` &lt;*il valore effettivo dell’ID cookie del cliente recuperato da`AdobePrivacy.js`*>

* `"include": **adCloud**` (che è il prodotto Adobe che si applica alla richiesta)

* `"regulation": **ccpa**` (regolamento sulla privacy applicabile alla richiesta)

## Esempio di richiesta inviata da un consumatore utilizzando un ID utente pubblicitario Adobe recuperato da AdobePrivacy.js

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
}
```

## Campi dati restituiti per le richieste di accesso

Di seguito è riportato un esempio di risposta di accesso alle informazioni personali per Adobe Advertising.

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
