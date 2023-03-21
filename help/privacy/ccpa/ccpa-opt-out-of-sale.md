---
title: 'Supporto pubblicitario Adobe per il California Consumer Privacy Act : Supporto per rinuncia alla vendita da parte del consumatore'
description: Scopri il supporto per l’acquisizione delle richieste di rinuncia del consumatore.
feature: CCPA
exl-id: df2b8679-8a1c-4cd7-b867-cd2f53c76c8f
source-git-commit: 7f35b3f3b33ed320ac186d219cbd0f826666bb3b
workflow-type: tm+mt
source-wordcount: '1003'
ht-degree: 0%

---

# Adobe di supporto per la pubblicità per il California Consumer Privacy Act: Supporto per rinuncia alla vendita da parte del consumatore

*Ad Adobe, Demand Side Platform Pubblicitario (DSP)*

>[!IMPORTANT]
>
>Il contenuto di questo documento non rappresenta e non intende sostituirsi a una consulenza legale. Consulta il tuo consulente legale per ricevere consigli in merito al California Consumer Privacy Act.

Il California Consumer Privacy Act (CCPA) è la nuova legge sulla privacy della California, in vigore dal 1° gennaio 2020. Il CCPA conferisce ai residenti della California nuovi diritti in merito alle loro informazioni personali e impone responsabilità in materia di protezione dei dati a determinate entità che conducono attività commerciali in California. Il CCPA garantisce ai consumatori il diritto di accedere ai propri dati e di cancellarli, nonché il diritto di rinunciare a determinate attività che possono essere considerate come &quot;vendita&quot; di informazioni personali a terzi.

In qualità di azienda, puoi determinare i dati personali elaborati e archiviati da Adobe Experience Cloud per tuo conto.

In qualità di fornitore di servizi, Adobe Advertising fornisce supporto alla tua azienda per adempiere ai suoi obblighi in virtù del CCPA applicabili all&#39;uso di prodotti e servizi Adobe Advertising, inclusa la gestione delle richieste dei consumatori di accedere e cancellare informazioni personali e la gestione delle richieste dei consumatori di rinunciare alla vendita di informazioni personali.

Questo documento descrive come Adobe Advertising Demand Side Platform (DSP), in qualità di fornitore di servizi, supporti il diritto del consumatore di rinunciare alla &quot;vendita&quot; di &quot;informazioni personali&quot;, in quanto ogni termine è definito dal CCPA. Include informazioni su come comunicare le richieste di rinuncia alla vendita ad Adobe Advertising e su come recuperare i rapporti delle richieste di rinuncia alla vendita della tua organizzazione.

Per informazioni su come [!DNL Advertising Search, Social, & Commerce]; Advertising Creative; e [!DNL Advertising DCO] supportare i diritti di accesso e cancellazione delle informazioni personali dei consumatori, vedi [Adobe di supporto per la pubblicità per il California Consumer Privacy Act: Supporto per l’accesso e l’eliminazione dei dati dei clienti](/help/privacy/ccpa/ccpa-access-delete.md).

Per ulteriori informazioni sull’Adobe dei servizi di privacy per il CCPA, consulta la sezione [Centro per la privacy Adobe](https://www.adobe.com/privacy/ccpa.html).

## Comunicazione delle richieste di rinuncia del consumatore ad Adobe della pubblicità

Puoi comunicare le richieste di rinuncia del consumatore utilizzando:

* un segmento di rifiuto del CCPA creato in Advertising DSP
* API di Adobe Experience Platform Privacy Service

### Metodo 1: Comunicazione delle richieste di rinuncia CCPA tramite un [!UICONTROL CCPA Opt-Out-of-Sale] Segmento in Advertising DSP

>[!NOTE]
>
>Gli utenti rimangono a tempo indefinito nei segmenti di rifiuto del CCPA.

1. Accedi all&#39;account dell&#39;inserzionista in Advertising DSP all&#39;indirizzo [https://advertising.adobe.com/](https://advertising.adobe.com/).
1. [Crea un segmento di rinuncia CCPA e implementa il pixel del segmento per acquisire le richieste di rinuncia](/help/dsp/audiences/ccpa-opt-out-segment-create.md).

### Metodo 2: Comunicazione delle richieste di rinuncia al CCPA tramite l’API di Adobe Experience Platform Privacy Service

*Gli inserzionisti hanno assegnato un solo ID organizzazione Adobe Experience Cloud*

1. Distribuisci una libreria JavaScript per recuperare i cookie del cliente. La stessa libreria, `AdobePrivacy.js`, viene utilizzato per tutte le soluzioni Adobe Experience Cloud.

   >[!IMPORTANT]
   >
   >Le richieste ad alcune soluzioni Adobe Experience Cloud non richiedono la libreria JavaScript, ma richieste ad Adobe Advertising lo richiedono.

   Devi distribuire la libreria sulla pagina web da cui i clienti possono inviare le richieste di rinuncia, ad esempio il portale per la privacy della tua azienda. La libreria consente di recuperare i cookie di Adobe (ID dello spazio dei nomi: `gsurferID`) per poter inviare queste identità come parte delle richieste di rinuncia alla vendita tramite l’API Adobe Experience Platform Privacy Service.

1. Identifica l’ID organizzazione Experience Cloud e assicurati che sia collegato ai tuoi account Adobe Advertising.

   Un ID organizzazione Experience Cloud è una stringa alfanumerica composta da 24 caratteri, con l&#39;aggiunta di &quot;@AdobeOrg.&quot; Alla maggior parte dei clienti di Experience Cloud è stato assegnato un ID organizzazione. Se il team di marketing o l’amministratore di sistema di Adobe interno non conosce l’ID organizzazione o se non è sicuro che sia stato eseguito il provisioning, contatta l’Assistenza clienti Adobe all’indirizzo gdprsupport@adobe.com. Per inviare richieste all’API Privacy è necessario l’ID organizzazione tramite l’ `imsOrgID` spazio dei nomi.

   >[!IMPORTANT]
   >
   >Contatta il rappresentante pubblicitario Adobe della tua azienda per confermare che tutti gli account pubblicitari Adobi della tua organizzazione, compresi [!DNL DSP] account o inserzionisti, [!DNL Search, Social, & Commerce] conti e [!DNL Creative] o [!DNL DCO] account - sono collegati all&#39;ID organizzazione Experience Cloud.

1. Utilizza l’API di Adobe Experience Platform Privacy Service per [inviare richieste di rinuncia alla vendita](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/consent.html) Adobe della pubblicità per conto dei consumatori e verifica lo stato delle richieste esistenti.

   Vedi l&#39;Appendice seguente per un esempio di richiesta di rinuncia alla vendita.

   >[!NOTE]
   Se la tua azienda dispone di più ID organizzazione Experience Cloud, devi inviare richieste API separate per ciascuna di esse. Tuttavia puoi effettuare una richiesta API a più soluzioni secondarie di Adobe Advertising ([!DNL Search, Social, & Commerce], [!DNL Creative], [!DNL DSP]e [!DNL DCO]), con un account per soluzione secondaria.

Tutti questi passaggi sono necessari per ricevere il supporto da Adobe Advertising. Per ulteriori informazioni su queste e altre attività correlate che devi eseguire utilizzando Adobe Experience Platform Privacy Service e su dove trovare gli elementi necessari, vedi [https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html).

## Recupero dei rapporti dei consumatori che hanno inviato richieste di rinuncia alla vendita

Adobe Advertising genera rapporti mensili sugli ID inviati dai clienti per richieste di rinuncia alla vendita per l’account. Ogni rapporto è disponibile come file di testo separato da tabulazioni compresso in formato GZIP. I dati consolidano le richieste acquisite utilizzando i segmenti di rifiuto del CCPA creati in Advertising DSP e gli eventuali invii effettuati tramite l’API Privacy Service. Gli ID utente acquisiti nei segmenti di rifiuto del CCPA vengono identificati per segmento e per inserzionista. I rapporti vengono generati il primo di ogni mese per il mese precedente. Ad esempio, l’elenco degli utenti mensili per giugno è disponibile il 1° luglio.

Puoi recuperare i collegamenti ai rapporti mensili creati nei tre mesi precedenti, sia da Advertising DSP che utilizzando il DSP Pubblicitario. [!DNL Trafficking API]. Ogni collegamento è valido per sette giorni, ma viene aggiornato ogni volta che un cliente tenta di recuperarlo.

### Metodo 1: Recuperare I Rapporti Di Rinuncia Del Consumatore All’Interno Di Advertising DSP

1. Accedi all&#39;account dell&#39;inserzionista in Advertising DSP all&#39;indirizzo [https://advertising.adobe.com/](https://advertising.adobe.com/).
1. [Recuperare i rapporti](/help/dsp/audiences/ccpa-opt-out-segment-report-retrieve.md).

### Metodo 2: Recupera i rapporti di rinuncia del consumatore utilizzando il DSP pubblicitario [!DNL Trafficking API]

Questa funzione è disponibile per le organizzazioni che utilizzano [!DNL Trafficking API]. Consulta la documentazione per [!DNL Trafficking API] per ulteriori informazioni.

Se la tua organizzazione non utilizza il [!DNL Trafficking API] ma è interessato a ulteriori informazioni, contatta il team dell&#39;account Adobe.

## Appendice: Esempio [!UICONTROL CCPA Opt-Out-of-Sale] Richiesta per gli utenti API di Privacy Service

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
    "include": ["AdCloud"],
    "regulation": "ccpa"
}'
```

dove:

* `"namespace": "AdCloud"` indica la `AdCloud` cookie space e il valore corrispondente è l’ID cookie del cliente recuperato da `AdobePrivacy.js`
* `"include": ["AdCloud"]` indica che la richiesta si applica ad Adobe Advertising
