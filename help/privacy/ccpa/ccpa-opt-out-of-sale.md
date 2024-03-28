---
title: 'Adobe Advertising di supporto per il California Consumer Privacy Act: supporto per la rinuncia del consumatore'
description: Scopri il supporto per l’acquisizione delle richieste di rifiuto del consumatore.
feature: CCPA
role: User, Developer
exl-id: df2b8679-8a1c-4cd7-b867-cd2f53c76c8f
source-git-commit: 7378ea6e6907aa4067bd3e73160a8e71c925ec9d
workflow-type: tm+mt
source-wordcount: '988'
ht-degree: 0%

---

# Adobe Advertising di supporto per il California Consumer Privacy Act: supporto per la rinuncia del consumatore alla vendita

*Ad Adobe Advertising Demand Side Platform (DSP)*

>[!IMPORTANT]
>
>Il contenuto di questo documento non rappresenta e non intende sostituirsi a una consulenza legale. Consulta il tuo consulente legale per ricevere consigli in merito al California Consumer Privacy Act.

Il California Consumer Privacy Act (CCPA) è la nuova legge sulla privacy della California, in vigore dal 1° gennaio 2020. Il CCPA conferisce ai residenti della California nuovi diritti in merito alle loro informazioni personali e impone responsabilità in materia di protezione dei dati a determinate entità che conducono attività commerciali in California. Il CCPA garantisce ai consumatori il diritto di accedere ai propri dati e di cancellarli, nonché il diritto di non partecipare a determinate attività che possono essere considerate di &quot;vendita&quot; di informazioni personali a terzi.

In qualità di azienda, potrai determinare i dati personali che Adobe Experience Cloud tratta e archivia per tuo conto.

In qualità di fornitore di servizi, Adobi Advertising fornisce supporto alla tua azienda per l’adempimento dei suoi obblighi in virtù del CCPA applicabili all’utilizzo di prodotti e servizi di Adobe Advertising, inclusa la gestione delle richieste dei consumatori di accedere e cancellare informazioni personali e la gestione delle richieste dei consumatori di non partecipare alla vendita di informazioni personali.

In questo documento viene descritto come l&#39;DSP (Adobi Advertising Demand Side Platform), in qualità di fornitore di servizi, supporti il diritto del consumatore di rinunciare alla &quot;vendita&quot; di &quot;informazioni personali&quot;, in base a quanto definito dal CCPA. Include informazioni su come comunicare ad Adobi Advertising le richieste di rifiuto e come recuperare i rapporti sulle richieste di rifiuto dell’organizzazione.

Per informazioni su come [!DNL Advertising Search, Social, & Commerce]; Advertising Creative; e [!DNL Advertising DCO] supportare i diritti di accesso e di eliminazione delle informazioni personali dei consumatori, vedi [Adobe Advertising di supporto per il California Consumer Privacy Act: supporto per l’accesso e l’eliminazione dei dati dei consumatori](/help/privacy/ccpa/ccpa-access-delete.md).

Per ulteriori informazioni sull&#39;Adobe dei servizi per la privacy relativi al CCPA, vedere [Centro per la privacy di Adobe](https://www.adobe.com/privacy/ccpa.html).

## Comunicazione delle richieste di rifiuto del consumatore all’Adobe Advertising

Puoi comunicare le richieste di rifiuto del consumatore utilizzando:

* un segmento di rinuncia CCPA creato in Advertising DSP
* API di Adobe Experience Platform Privacy Service

### Metodo 1: comunicazione delle richieste di rifiuto del CCPA tramite [!UICONTROL CCPA Opt-Out-of-Sale] Segmento nella pubblicità DSP

>[!NOTE]
>
>Gli utenti rimangono nei segmenti di rifiuto del CCPA per un tempo indefinito.

1. Accedi all’account dell’inserzionista in Advertising DSP all’indirizzo [https://advertising.adobe.com/](https://advertising.adobe.com/).
1. [Creare un segmento di rifiuto CCPA e implementare il pixel del segmento per acquisire le richieste di rifiuto](/help/dsp/audiences/ccpa-opt-out-segment-create.md).

### Metodo 2: comunicare le richieste di rifiuto del CCPA utilizzando l’API Adobe Experience Platform Privacy Service

*Agli inserzionisti è assegnato solo un ID organizzazione Adobe Experience Cloud*

1. Distribuisci una libreria JavaScript per recuperare i cookie del cliente. La stessa libreria, `AdobePrivacy.js`, viene utilizzato per tutte le soluzioni Adobe Experience Cloud.

   >[!IMPORTANT]
   >
   >Le richieste ad alcune soluzioni Adobe Experience Cloud non richiedono la libreria JavaScript, ma le richieste ad Adobi Advertising la richiedono.

   Devi distribuire la libreria sulla pagina web da cui i clienti possono inviare richieste di rifiuto della vendita, come ad esempio il portale della privacy della tua azienda. La libreria ti aiuta a recuperare i cookie Adobe (ID spazio dei nomi: `gsurferID`) in modo da poter inviare queste identità come parte delle richieste di rifiuto tramite l’API Adobe Experience Platform Privacy Service.

1. Identifica l’ID organizzazione Experience Cloud e assicurati che sia collegato ai tuoi account Adobi Advertising.

   Un ID organizzazione di Experience Cloud è una stringa alfanumerica composta da 24 caratteri a cui segue &quot;@AdobeOrg.&quot; Alla maggior parte dei clienti Experience Cloud è stato assegnato un ID organizzazione. Se il team marketing o l’amministratore di Adobe interno non conosce l’ID organizzazione o non è sicuro che sia stato fornito, contatta il team dell’account Adobe. Per inviare richieste all&#39;API per la privacy utilizzando l&#39;ID organizzazione `imsOrgID` spazio dei nomi.

   >[!IMPORTANT]
   >
   >Contatta il rappresentante Adobe Advertising della tua azienda per verificare che tutti gli account Adobi Advertising della tua organizzazione, tra cui [!DNL DSP] account o inserzionisti, [!DNL Search, Social, & Commerce] conti, e [!DNL Creative] o [!DNL DCO] account — sono collegati al tuo ID organizzazione Experience Cloud.

1. Utilizza l’API Adobe Experience Platform Privacy Service per: [invia richieste di rinuncia alla vendita](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/consent.html) per Adobe Advertising a nome dei consumatori e per verificare lo stato delle richieste esistenti.

   Per un esempio di richiesta di rifiuto, consulta l’appendice seguente.

   >[!NOTE]
   >
   >Se la tua azienda dispone di più ID organizzazione Experience Cloud, devi inviare richieste API separate per ciascuno di essi. Tuttavia, puoi effettuare una richiesta API a più soluzioni secondarie Adobi Advertising ([!DNL Search, Social, & Commerce], [!DNL Creative], [!DNL DSP], e [!DNL DCO]), con un account per ogni soluzione secondaria.

Tutti questi passaggi sono necessari per ricevere supporto da Adobi Advertising. Per ulteriori informazioni su queste e altre attività correlate che è necessario eseguire utilizzando Adobe Experience Platform Privacy Service e dove trovare gli elementi necessari, vedere [https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html).

## Recupero dei report dei consumatori che hanno inviato richieste di rifiuto

Adobi Advertising genera rapporti mensili sugli ID inviati dai clienti per richieste di rifiuto per l’account. Ogni rapporto è disponibile come file di testo separato da tabulazioni compresso in formato GZIP. I dati consolidano le richieste acquisite utilizzando i segmenti di rifiuto del CCPA creati in Advertising DSP e tutte le richieste effettuate tramite l’API Privacy Service. Gli ID utente acquisiti nei segmenti di rifiuto del CCPA sono identificati per segmento e dall’inserzionista. I rapporti vengono generati il primo di ogni mese per il mese precedente. Ad esempio, l’elenco mensile degli utenti di giugno è disponibile il 1° luglio.

Puoi recuperare i collegamenti ai rapporti mensili creati nei tre mesi precedenti, dall’interno di Advertising DSP o utilizzando Advertising DSP [!DNL Trafficking API]. Ogni collegamento è valido per sette giorni, ma viene aggiornato ogni volta che un cliente tenta di recuperarne uno.

### Metodo 1: Recuperare i rapporti sulla rinuncia del consumatore in Advertising DSP

1. Accedi all’account dell’inserzionista in Advertising DSP all’indirizzo [https://advertising.adobe.com/](https://advertising.adobe.com/).
1. [Recuperare i rapporti](/help/dsp/audiences/ccpa-opt-out-segment-report-retrieve.md).

### Metodo 2: Recuperare i rapporti sulla rinuncia del consumatore utilizzando Advertising DSP [!DNL Trafficking API]

Questa funzione è disponibile per le organizzazioni che utilizzano [!DNL Trafficking API]. Consulta la documentazione per [!DNL Trafficking API] per ulteriori informazioni.<!-- Add link to API doc once it's published. -->

Se la tua organizzazione non utilizza [!DNL Trafficking API] ma è interessato a ulteriori informazioni, contatta il tuo Adobe Account Team.

## Appendice: esempio [!UICONTROL CCPA Opt-Out-of-Sale] Richiesta per utenti API di Privacy Service

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
            "namespace": "adCloud",
            "type": "standard",
            "value":  "Wqersioejr-wdg",
          }
    ],
    "include": ["adCloud"],
    "regulation": "ccpa"
}'
```

dove:

* `"namespace": "adCloud"` indica il `adCloud` cookie e il valore corrispondente è l’ID cookie del cliente come recuperato da `AdobePrivacy.js`
* `"include": ["adCloud"]` indica che la richiesta si applica a Adobi Advertising
