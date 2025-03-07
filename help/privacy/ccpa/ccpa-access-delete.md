---
title: Supporto di Adobe Advertising per il California Consumer Privacy Act &#58; Supporto per l’accesso e l’eliminazione dei dati dei consumatori
description: Scopri i tipi di richiesta di dati supportati, i valori di configurazione e campi richiesti ed esempi di richieste di accesso API che utilizzano ID prodotto legacy e campi dati restituiti.
feature: CCPA
role: User, Developer
exl-id: e7808411-7dc3-499c-bda1-1f5882f651b2
source-git-commit: a3e39ca4fa89f84ddc2669662c34bccb4425a2bb
workflow-type: tm+mt
source-wordcount: '1039'
ht-degree: 0%

---

# Supporto di Adobe Advertising per il California Consumer Privacy Act: supporto per l’accesso e l’eliminazione dei dati dei consumatori

*Per [!DNL Adobe Advertising Search, Social, & Commerce]; Adobe Advertising DSP; Adobe Advertising Creative; e Adobe Advertising DCO*

>[!IMPORTANT]
>
>Il contenuto di questo documento non rappresenta e non intende sostituirsi a una consulenza legale. Consulta il tuo consulente legale per ricevere consigli in merito al California Consumer Privacy Act.

Il California Consumer Privacy Act (CCPA) è la nuova legge sulla privacy della California, in vigore dal 1° gennaio 2020. Il CCPA conferisce ai residenti della California nuovi diritti in merito alle loro informazioni personali e impone responsabilità in materia di protezione dei dati a determinate entità che conducono attività commerciali in California. Il CCPA garantisce ai consumatori il diritto di accedere ai propri dati personali e di cancellarli, nonché il diritto di non partecipare a determinate attività che possono essere considerate di &quot;vendita&quot; di informazioni personali a terzi.

In qualità di azienda, potrai determinare i dati personali che Adobe Experience Cloud tratta e archivia per tuo conto.

In qualità di fornitore di servizi, Adobe Advertising fornisce supporto alla tua azienda per l’adempimento dei suoi obblighi in virtù del CCPA applicabili all’utilizzo dei prodotti e servizi Adobe Advertising, inclusa la gestione delle richieste di accesso e cancellazione delle informazioni personali e la gestione delle richieste di rinuncia alla vendita di tali informazioni.

In questo documento viene descritto come [!DNL Advertising Search, Social, & Commerce], Advertising Creative, Advertising DSP (Demand Side Platform) e [!DNL Advertising DCO], in qualità di provider di servizi, supportano i diritti dei consumatori per l&#39;accesso e l&#39;eliminazione di informazioni personali tramite Adobe [!DNL Experience Platform Privacy Service API] e [!DNL Privacy Service UI].

Per informazioni su come Advertising DSP supporta il diritto del consumatore di rinunciare alla vendita di informazioni personali, consulta [Supporto Adobe Advertising per il California Consumer Privacy Act: Supporto per la rinuncia del consumatore](/help/privacy/ccpa/ccpa-opt-out-of-sale.md).

Per ulteriori informazioni sui servizi di privacy Adobe per il CCPA, visitare il [Centro per la privacy Adobe](https://www.adobe.com/privacy/ccpa.html).

## Tipi di richieste di dati supportati per Adobe Advertising

Adobe Experience Platform consente alle aziende di completare le seguenti attività:

* Accedere ai dati a livello di cookie o ai dati a livello di ID dispositivo di un consumatore (per gli annunci nelle app mobili) in [!DNL Search, Social, & Commerce], [!DNL Creative], [!DNL DSP] o [!DNL DCO].
* Eliminare i dati a livello di cookie archiviati in [!DNL Search, Social, & Commerce], [!DNL Creative], [!DNL DSP] o [!DNL DCO] per i consumatori che utilizzano un browser oppure eliminare i dati a livello di ID archiviati in [!DNL DSP] per i consumatori che utilizzano app su dispositivi mobili.
* Controlla lo stato di una o tutte le richieste esistenti.

## Configurazione necessaria per inviare richieste per Adobe Advertising

Per richiedere l’accesso e la cancellazione delle informazioni personali dei consumatori da Adobe Advertising, è necessario:

1. Implementa una libreria JavaScript per recuperare e rimuovere i cookie del cliente. La stessa libreria, `AdobePrivacy.js`, viene utilizzata per tutte le soluzioni Adobe Experience Cloud.

   >[!IMPORTANT]
   >
   >Le richieste ad alcune soluzioni Experience Cloud non richiedono la libreria JavaScript, ma le richieste ad Adobe Advertising lo richiedono.

   Devi distribuire la libreria sulla pagina web da cui i clienti possono inviare richieste di accesso ed eliminazione, come ad esempio il portale della privacy della tua azienda. La libreria consente di recuperare i cookie di Adobe (ID spazio dei nomi: `gsurferID`) in modo da poter inviare queste identità come parte delle richieste di accesso ed eliminazione tramite [!DNL Adobe Experience Platform Privacy Service API].

   Quando il cliente chiede di eliminare i dati personali, la libreria elimina anche il cookie del cliente dal browser del cliente.

   >[!NOTE]
   >
   >L’eliminazione dei dati personali è diversa dalla rinuncia, che interrompe il targeting di un utente finale con segmenti di pubblico. Tuttavia, quando un consumatore richiede di eliminare i dati personali da [!DNL Creative], [!DNL DSP] o [!DNL DCO], la libreria invia anche una richiesta ad Adobe Advertising per negare al cliente il targeting dei segmenti. Per gli inserzionisti con [!DNL Search, Social, & Commerce], ti consigliamo di fornire ai clienti un collegamento a [https://www.adobe.com/privacy/opt-out.html#customeruse](https://www.adobe.com/privacy/opt-out.html#customeruse), che spiega come rinunciare al targeting dei segmenti di pubblico.

1. Identifica il tuo ID organizzazione Experience Cloud e assicurati che sia collegato al tuo account Adobe Advertising.

   Un ID organizzazione Experience Cloud è una stringa alfanumerica composta da 24 caratteri a cui segue &quot;@AdobeOrg.&quot; Alla maggior parte dei clienti Experience Cloud è stato assegnato un ID organizzazione. Se il team marketing o l&#39;amministratore di sistema interno di [!DNL Adobe] non conosce l&#39;ID organizzazione o non è sicuro che sia stato eseguito il provisioning, contatta il team dell&#39;account Adobe. Per inviare richieste all&#39;API per la privacy utilizzando lo spazio dei nomi `imsOrgID` è necessario l&#39;ID organizzazione.

   >[!IMPORTANT]
   >
   >Contatta il rappresentante Adobe Advertising della tua azienda per verificare che tutti gli account Adobe Advertising della tua organizzazione, inclusi [!DNL DSP] account o inserzionisti, [!DNL Search, Social, & Commerce] account e [!DNL Creative] o [!DNL DCO] account, siano collegati al tuo ID organizzazione Experience Cloud.

1. Utilizza l&#39;[API Adobe Experience Platform Privacy Service](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/privacy-jobs.html) (per le richieste automatizzate) o la [interfaccia utente Privacy Service](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html?lang=it) (per le richieste ad hoc) per inviare richieste di accesso ed eliminazione di informazioni personali ad Adobe Advertising per conto dei consumatori e per controllare lo stato delle richieste esistenti.

   Per gli inserzionisti che dispongono di un&#39;app mobile per interagire con i clienti e avviare campagne con [!DNL DSP], è necessario scaricare gli SDK per dispositivi mobili predisposti per la privacy per Experience Cloud. Gli SDK di Mobile consentono alle aziende di impostare flag di stato per la rinuncia, recuperare l&#39;ID dispositivo del consumatore (ID spazio dei nomi: `deviceID`) e inviare richieste all&#39;API Privacy Service. La tua app mobile richiederà una versione di SDK 4.15.0 o successiva.

   Quando invii una richiesta di accesso del consumatore, l’API di Privacy Service restituisce le informazioni di un consumatore in base al cookie o all’ID dispositivo specificato, che devono quindi essere restituiti al consumatore.

   Quando invii una richiesta di cancellazione del consumatore, l’ID del cookie o dell’ID del dispositivo e tutti i dati relativi a costi, clic e ricavi associati al cookie vengono eliminati dal server.

   >[!NOTE]
   >
   >Se la tua azienda dispone di più ID organizzazione Experience Cloud, devi inviare richieste API separate per ciascuno di essi. È tuttavia possibile effettuare una richiesta API a più soluzioni secondarie di Adobe Advertising ([!DNL Search, Social, & Commerce], [!DNL Creative], [!DNL DSP] e [!DNL DCO]), con un account per ogni soluzione secondaria.

Per ricevere supporto da Adobe Advertising, sono necessari tutti i passaggi necessari. Per ulteriori informazioni su queste e altre attività correlate che è necessario eseguire utilizzando Adobe Experience Platform Privacy Service e dove trovare gli elementi necessari, vedere [https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html).

## Valori campo obbligatori nelle richieste JSON di Adobe Advertising

`"company context":`

* `"namespace": **imsOrgID**`
* `"value":` &lt;*ID organizzazione Experience Cloud*>

&quot;users&quot; (utenti):

* `"key":` &lt;*in genere il nome del cliente*>

* `"action":` `**access**` o `**delete**`

* `"user IDs":`

   * `"namespace": **411**` (che indica lo [[!DNL AdCloud] spazio cookie](https://experienceleague.adobe.com/en/docs/experience-platform/privacy/api/appendix))

   * `"value":` &lt;*valore ID cookie del cliente effettivo recuperato da`AdobePrivacy.js`*>

* `"include": **adCloud**` (che è il [[!DNL Adobe] prodotto](https://experienceleague.adobe.com/en/docs/experience-platform/privacy/api/appendix) che si applica alla richiesta)

* `"regulation": **ccpa**` (normativa sulla privacy applicabile alla richiesta)

## Esempio di richiesta inviata da un consumatore utilizzando un ID utente di Adobe Advertising recuperato da AdobePrivacy.js

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
                    "segmentName":"eXelate Australia Demographic - Jobs & Education - Job Seekers",
                    "segmentID":"2213789",
                    "serviceProvider":"exelate"
                }
            ]
        }
    }
}
```
