---
title: Macro per la pubblicità DSP
description: Fai riferimento alle macro disponibili per il tracciamento generale e per tenere traccia dei clic sugli annunci di visualizzazione di terze parti.
feature: DSP Ads
exl-id: e31cc2e5-ad1f-4555-a87b-0e4c3731fe5f
source-git-commit: 1c13874967ec4ad264e5fa6a5e0dfeb6120f53cc
workflow-type: tm+mt
source-wordcount: '929'
ht-degree: 0%

---

# Macro per la pubblicità DSP

Una macro è un comando breve o abbreviato per un&#39;istruzione e in genere segue il formato `${MACRO_NAME}`. Le macro incluse nel codice creativo o gli URL di click-through si espandono in una stringa di codice più lunga comprensibile al server di annunci. Il server di annunci DSP esegue le macro quando l’annuncio viene servito o fai clic su di esso.

Le macro del server di annunci sono utili per trasmettere informazioni importanti a DSP o a server di annunci di terze parti. Le macro vengono utilizzate più comunemente durante il traffico di codice creativo o metadati di terze parti e personalizzati (come i pixel di terze parti).

È possibile inserire manualmente una macro in qualsiasi punto, ad esempio in un tag VAST, in qualsiasi URL o in un pixel evento DSP o di terze parti. Tuttavia, ogni client DSP e partner ha un formato di tag annuncio diverso e le macro devono essere inserite in punti diversi nel tag di conseguenza. Ogni volta che si lavora con un nuovo client o partner, chiedere loro la documentazione su dove inserire le macro nei tag degli annunci che DSP traffici.

## Macro per il tracciamento generale

Utilizza le macro di tracciamento generali per tutti i tipi di annunci e tag per restituire dati specifici, a seconda delle necessità.

| Macro | Descrizione sostitutiva | Tipo |
| ----- | ----------------------- | ---- |
| `${TM_ACCOUNT_ID}` | ID account. | integer |
| `${TM_AD_ID}` | Il codice ad (adKey). | string |
| `${TM_AD_ID_NUM}` | L&#39;ID dell&#39;annuncio. | integer |
| `${TM_ADVERTISER_ID}` | ID dell&#39;inserzionista. | integer |
| `${TM_CAMPAIGN_ID}` | Chiave della campagna. | string |
| `${TM_CAMPAIGN_ID_NUM}` | ID della campagna. | integer |
| ` ${TM_CLICK_URL}` | L&#39;URL di reindirizzamento, che consente ai server di annunci di tenere traccia e contare i clic sugli annunci. Quando l&#39;annuncio viene servito, se l&#39;utente lo fa clic, la macro viene attivata e il clic viene registrato e conteggiato a scopo di reporting. | string |
| ` ${TM_CLICK_URL_URLENC}` | L’URL di reindirizzamento codificato, che consente ai server di annunci di tenere traccia e contare i clic sugli annunci. Quando l&#39;annuncio viene servito, se l&#39;utente lo fa clic, la macro viene attivata e il clic viene registrato e conteggiato a scopo di reporting. Non utilizzare questa macro a meno che non si creino annunci di terze parti e il fornitore non richieda la codifica URL. | string |
| `${TM_FEED_ID}` | Chiave per il posizionamento del contenuto multimediale (feedKey). | string |
| `${TM_FEED_ID_NUM}` | ID del posizionamento del contenuto multimediale. | integer |
| ` ${TM_MACRO_PLACEMENT_SITE_KEY` | Chiave del sito per il posizionamento. Obbligatorio per [!DNL AppsFlyer] fai clic su tracker per annunci di installazione app mobile.<!-- should map to placement_site_key column of placement_site table --> | string |
| `${TM_PLACEMENT_ID}` | Chiave di posizionamento (cpKey). | string |
| `${TM_PLACEMENT_ID_NUM}` | ID di posizionamento. | integer |
| `${TM_RANDOM}` | Cachebuster: un numero casuale compreso tra 1 e 1000000. | long |
| `${TM_SESSION_ID}` | L&#39;ID della sessione, che corrisponde a un singolo recupero del tag dell&#39;annuncio. | string |
| `${TM_SITE_DOMAIN_URLENC}` | Il sottodominio della pagina analizzato dall’URL nella richiesta di offerta; URL-encoded. Non supportato per gli annunci in-banner, clic per la riproduzione. | string |
| ` ${TM_SITE_NAME}` | Nome del sito per il posizionamento. | string |
| `${TM_SITE_URL_URLENC}` | L’URL trasmesso nella richiesta di offerta; URL-encoded. Non supportato per gli annunci in-banner, clic per la riproduzione. | string |
| `${TM_SITE_ID_NUM}` | ID del sito per il posizionamento. | integer |
| `${TM_TIMESTAMP}` | La marca temporale Unix che indica il numero di secondi trascorsi dalla mezzanotte (00:00 UTC) del 1o gennaio 1970. | long |
| ` ${TM_VIDEO_DURATION}` | La durata del video dell’annuncio in secondi. | integer |

{style=&quot;table-layout:auto&quot;}

<!-- Removed because not found in code base:
|` ${TM_MACRO_PROMOTED_AD_KEY}` | The promoted ad key for the placement. Required for [!DNL AppsFlyer] click trackers for mobile app install ads. | string |
 -->

## Macro per dispositivi mobili

| Macro | Descrizione sostitutiva | Tipo |
| ----- | ----------------------- | ---- |
| `${CS_PLATFORM_ID}` | ([!DNL ComScore]) L&#39;ID della piattaforma, che corrisponde al sistema operativo del dispositivo:<ul><li>`ios` = [!DNL Apple iOS]</li><li>`android` = [!DNL Google Android]</li><li>`windows` = [!DNL Windows Mobile]</li><li>`blackberry` = [!DNL Blackberry]</li> <li>`other` quando la piattaforma non è compresa in nessuno dei</li></ul> | varchar(50) |
| `${CS_DEVICE_MODEL}` | ([!DNL ComScore]) Il nome del modello di dispositivo, codificato in URL. | string |
| `${CS_IMPLEMENTATION_TYPE}` | ([!DNL ComScore]) L&#39;ambiente in cui è stato servito l&#39;annuncio:<ul><li>`a` = app mobile</li><li>`b` = sito web mobile</li></ul> | string (`a` o `b`) |
| `${NS_PLATFORM_ID}` | ([!DNL Nielsen]) L&#39;ID della piattaforma, che corrisponde al sistema operativo del dispositivo:<ul><li>`ios`= [!DNL Apple iOS]</li><li>`android` = [!DNL Google Android]</li><li>`windows` = [!DNL Windows Mobile]</li><li>`blackberry` = [!DNL Blackberry]</li> <li>`other` quando la piattaforma non è compresa in nessuno dei</li></ul> | string |
| `${NS_DEVICE_GROUPING}` | ([!DNL Nielsen]) Il tipo di dispositivo su cui l&#39;annuncio era visualizzatore:<ul><li>`TAB` = tablet</li><li>`PHN` = mobile</li><li>`computer` = computer</li></ul> | string |
| `${UOO}` | ([!DNL Nielsen]) Se l&#39;utente ha rinunciato o meno al tracciamento degli annunci:<ul><li>`1` (flag DNT = 1) = l’utente ha rinunciato al tracciamento degli annunci</li><li>`0` (flag DNT = 0) = l’utente ha acconsentito al tracciamento degli annunci</li></ul> | integer`0` o `1`) |
| `${TM_BUNDLE}` | La [!DNL iOS] o [!DNL Android] ID bundle dell&#39;app store. Esempi: com.zynga.wwf2.free o id804379658 | string |
| `gdpr=${GDPR_ENFORCED}&gdpr_consent=${GDPR_CONSENT}` | `gdpr=${GDPR_ENFORCED}` indica se l’offerente determina che la richiesta di offerta proviene dall’origine dell’Unione europea e richiede l’applicazione del RGPD:<ul><li>`1` = Il RGPD deve essere applicato</li><li>`0` = Il RGPD non deve essere applicato</li></ul>`gdpr_consent=${GDPR_CONSENT}` è il valore di consenso trasmesso dal partner fornitore nella richiesta di offerta in entrata:<ul><li>Nella maggior parte dei casi, si tratta di una stringa di consenso con codifica base64url, o daisybit (ad esempio: BN5lERiOMYEdiAKAWXEND1HoSBE6CAFAApAMgBkIDIgM0AgOJxAnQA)</li><li>`0` = nessun consenso</li><li>`1` = consenso</li></ul> | daisybit o integer |

{style=&quot;table-layout:auto&quot;}

## Fare clic su Macro per annunci di visualizzazione di terze parti

Per tracciare con precisione i clic per gli annunci utilizzando tag di visualizzazione di terze parti, DSP necessario una macro di clic di visualizzazione. È necessaria una sola versione della macro; la macro pertinente dipende dal tipo di tag.

| Macro | Descrizione sostitutiva | Tipo |
| ----- | ----------------------- | ---- |
| `${TM_CLICK_URL}` | URL di reindirizzamento che consente ai server di annunci di tenere traccia e contare i clic sugli annunci nella piattaforma. | string |
| `${TM_CLICK_URL_URLENC}` | URL di reindirizzamento che consente ai server di annunci che richiedono la codifica URL di tracciare e contare i clic sugli annunci nella piattaforma. | string |

{style=&quot;table-layout:auto&quot;}

DSP inserisce automaticamente le macro di clic di visualizzazione in un tag di visualizzazione di terze parti quando:

* Esportare i tag degli annunci da un partner ad server <!-- [Needs PM confirmation.] -->
* Caricamento in blocco [!DNL Flashtalking] o [!DNL Google DoubleClick for Advertisers] tag di annunci direttamente in DSP

Se manca una macro di clic quando si crea un annuncio di visualizzazione, DSP visualizzato un messaggio di avviso che richiede di inserire manualmente la macro di clic di visualizzazione appropriata nell&#39;area corretta del tag.

## Risoluzione dei problemi relativi agli errori delle macro

Quando si aggiungono macro al codice, assicurarsi di utilizzare la sintassi esatta della macro. Durante la convalida delle macro, DSP controlla che la macro corrisponda esattamente a una delle macro valide.

Gli errori vengono generati se mancano caratteri dall&#39;inizio o dalla fine del nome della macro. Ad esempio, viene visualizzato un messaggio di errore se:

* Si dimenticano uno o più caratteri all&#39;inizio del nome della macro, ad esempio `${`. Se non si include la sintassi completa, la voce non viene riconosciuta come macro valida.
* La macro non termina con un set valido di caratteri, ad esempio `}`.

>[!MORELIKETHIS]
>
>* [Impostazioni annuncio audio](/help/dsp/campaign-management/ads/ad-settings-audio.md)
>* [Impostazioni degli annunci TV collegati](/help/dsp/campaign-management/ads/ad-settings-connected-tv.md)
>* [Visualizza impostazioni annuncio](/help/dsp/campaign-management/ads/ad-settings-display.md)
>* [Impostazioni degli annunci mobili](/help/dsp/campaign-management/ads/ad-settings-mobile.md)
>* [Impostazioni annunci native](/help/dsp/campaign-management/ads/ad-settings-native.md)
>* [Impostazioni annuncio pre-roll](/help/dsp/campaign-management/ads/ad-settings-pre-roll.md)
>* [Impostazioni degli annunci video universali](/help/dsp/campaign-management/ads/ad-settings-universal-video.md)

