---
title: Pubblicità delle macro dell’DSP
description: Fai riferimento alle macro disponibili per il tracciamento generale e per tenere traccia dei clic sugli annunci display di terze parti.
feature: DSP Ads
exl-id: 7058c988-c544-4a61-84dd-eec4ce88ceba
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '941'
ht-degree: 0%

---

# Pubblicità delle macro dell’DSP

Una macro è un comando breve o una scorciatoia per un&#39;istruzione e in genere segue il formato `${MACRO_NAME}`. Le macro incluse nel codice creativo o negli URL di click-through si espandono in una stringa di codice più lunga che il server dell’annuncio può comprendere. Il server di annunci DSP esegue le macro quando l’annuncio viene distribuito o su cui si fa clic.

Le macro del server di annunci sono utili per trasmettere informazioni importanti all’DSP o a server di annunci di terze parti. Le macro sono più comunemente utilizzate durante il traffico di codice creativo o metadati di terze parti e personalizzati (come i pixel di terze parti).

È possibile inserire manualmente una macro in qualsiasi punto, ad esempio in un tag VAST, in qualsiasi URL oppure in un DSP o in un pixel evento di terze parti. Tuttavia, ogni client e partner DSP ha un formato di tag annuncio diverso e le macro devono essere inserite in punti diversi del tag di conseguenza. Ogni volta che si lavora con un nuovo cliente o partner, chiedere loro la documentazione su dove inserire le macro nei loro tag pubblicitari che vengono trafficate da DSP.

## Macro di tracciamento generali

Utilizza le macro di tracciamento generali per tutti i tipi di annunci e tag per restituire dati specifici, in base alle esigenze.

| Macro | Descrizione sostituzione | Tipo |
| ----- | ----------------------- | ---- |
| `${TM_ACCOUNT_ID}` | L’ID account. | numero intero |
| `${TM_AD_ID}` | Chiave annuncio (adKey). | stringa |
| `${TM_AD_ID_NUM}` | L’ID dell’annuncio. | numero intero |
| `${TM_ADVERTISER_ID}` | ID inserzionista. | numero intero |
| `${TM_CAMPAIGN_ID}` | Chiave della campagna. | stringa |
| `${TM_CAMPAIGN_ID_NUM}` | ID della campagna. | numero intero |
| ` ${TM_CLICK_URL}` | L’URL di reindirizzamento, che consente ai server di annunci di tenere traccia e contare i clic degli annunci. Quando l’annuncio viene distribuito, se l’utente fa clic su di esso, la macro viene attivata e il clic viene registrato e conteggiato a scopo di reporting. | stringa |
| ` ${TM_CLICK_URL_URLENC}` | L’URL di reindirizzamento codificato, che consente ai server di annunci di tenere traccia e contare i clic degli annunci. Quando l’annuncio viene distribuito, se l’utente fa clic su di esso, la macro viene attivata e il clic viene registrato e conteggiato a scopo di reporting. Non utilizzare questa macro a meno che non si creino annunci di terze parti e il fornitore non richieda la codifica URL. | stringa |
| `${TM_FEED_ID}` | Chiave per il posizionamento dei contenuti multimediali (feedKey). | stringa |
| `${TM_FEED_ID_NUM}` | ID del posizionamento multimediale. | numero intero |
| ` ${TM_MACRO_PLACEMENT_SITE_KEY` | Chiave del sito per il posizionamento. Obbligatorio per [!DNL AppsFlyer] fai clic su tracker per gli annunci per l’installazione di app mobili.<!-- should map to placement_site_key column of placement_site table --> | stringa |
| `${TM_PLACEMENT_ID}` | La chiave di posizionamento (cpKey). | stringa |
| `${TM_PLACEMENT_ID_NUM}` | ID del posizionamento. | numero intero |
| `${TM_RANDOM}` | Cachebuster: un numero casuale compreso tra 1 e 1000000. | long |
| `${TM_SESSION_ID}` | L’ID della sessione, che corrisponde a un singolo recupero del tag dell’annuncio. | stringa |
| `${TM_SITE_DOMAIN_URLENC}` | Il sottodominio della pagina analizzato dall’URL nella richiesta di offerta; codificato in URL. Non supportato per annunci in banner e click-to-play. | stringa |
| ` ${TM_SITE_NAME}` | Il nome del sito per il posizionamento. | stringa |
| `${TM_SITE_URL_URLENC}` | URL passato nella richiesta di offerta; codifica URL. Non supportato per annunci in banner e click-to-play. | stringa |
| `${TM_SITE_ID_NUM}` | ID del sito per il posizionamento. | numero intero |
| `${TM_TIMESTAMP}` | La marca temporale Unix che indica il numero di secondi trascorsi dalla mezzanotte (00:00 UTC) del 1° gennaio 1970. | long |
| ` ${TM_VIDEO_DURATION}` | La durata del video dell’annuncio in secondi. | numero intero |

{style="table-layout:auto"}

<!-- Removed because not found in code base:
|` ${TM_MACRO_PROMOTED_AD_KEY}` | The promoted ad key for the placement. Required for [!DNL AppsFlyer] click trackers for mobile app install ads. | string |
 -->

## Macro specifiche per dispositivi mobili

| Macro | Descrizione sostituzione | Tipo |
| ----- | ----------------------- | ---- |
| `${CS_PLATFORM_ID}` | ([!DNL ComScore]) L&#39;ID piattaforma, che corrisponde al sistema operativo del dispositivo:<ul><li>`ios` = [!DNL Apple iOS]</li><li>`android` = [!DNL Google Android]</li><li>`windows` = [!DNL Windows Mobile]</li><li>`blackberry` = [!DNL Blackberry]</li> <li>`other` quando la piattaforma non è nessuna delle precedenti</li></ul> | varchar(50) |
| `${CS_DEVICE_MODEL}` | ([!DNL ComScore]a) Il nome del modello del dispositivo, con codifica URL. | stringa |
| `${CS_IMPLEMENTATION_TYPE}` | ([!DNL ComScore]) Ambiente in cui è stato distribuito l’annuncio:<ul><li>`a` = app mobile</li><li>`b` = sito Web mobile</li></ul> | stringa (`a` o `b`) |
| `${NS_PLATFORM_ID}` | ([!DNL Nielsen]) L&#39;ID piattaforma, che corrisponde al sistema operativo del dispositivo:<ul><li>`ios`= [!DNL Apple iOS]</li><li>`android` = [!DNL Google Android]</li><li>`windows` = [!DNL Windows Mobile]</li><li>`blackberry` = [!DNL Blackberry]</li> <li>`other` quando la piattaforma non è nessuna delle precedenti</li></ul> | stringa |
| `${NS_DEVICE_GROUPING}` | ([!DNL Nielsen]) Il tipo di dispositivo su cui l’annuncio era visualizzatore:<ul><li>`TAB` = tablet</li><li>`PHN` = mobile</li><li>`computer` = computer</li></ul> | stringa |
| `${UOO}` | ([!DNL Nielsen]) Se l’utente ha rinunciato o meno al tracciamento degli annunci:<ul><li>`1` (Flag DNT = 1) = l’utente ha rinunciato al tracciamento degli annunci</li><li>`0` (Flag DNT = 0) = l’utente ha acconsentito al tracciamento degli annunci</li></ul> | numero intero (`0` o `1`) |
| `${TM_BUNDLE}` | Il [!DNL iOS] o [!DNL Android] ID del bundle dell’app store. Esempi: com.zynga.wwf2.free o id804379658 | stringa |
| `gdpr=${GDPR_ENFORCED}&gdpr_consent=${GDPR_CONSENT}` | `gdpr=${GDPR_ENFORCED}` indica se l’offerente determina che la richiesta di offerta proviene dall’Unione Europea e richiede l’applicazione del RGPD:<ul><li>`1` = il RGPD deve essere applicato</li><li>`0` = il RGPD non deve essere applicato</li></ul>`gdpr_consent=${GDPR_CONSENT}` è il valore di consenso passato dal partner di fornitura nella richiesta di offerta in entrata:<ul><li>Nella maggior parte dei casi, si tratta di una stringa di consenso con codifica base64url, o daisybit (ad esempio: BN5lERiOMYEdiAKAWXEND1HoSBE6CAFAApAMgBkIDIgM0AgOJxAnQA)</li><li>`0` = nessun consenso</li><li>`1` = consenso</li></ul> | daisybit o numero intero |

{style="table-layout:auto"}

## Fare clic su Macro per gli annunci visualizzati di terze parti

Per tenere traccia con precisione dei clic per gli annunci che utilizzano tag di visualizzazione di terze parti, l’DSP richiede una macro di clic di visualizzazione. È necessaria una sola versione della macro; la macro pertinente dipende dal tipo di tag.

| Macro | Descrizione sostituzione | Tipo |
| ----- | ----------------------- | ---- |
| `${TM_CLICK_URL}` | L’URL di reindirizzamento che consente ai server di annunci di tenere traccia e contare i clic degli annunci nella piattaforma. | stringa |
| `${TM_CLICK_URL_URLENC}` | L’URL di reindirizzamento che abilita i server di annunci che richiedono la codifica URL per tenere traccia e contare i clic degli annunci nella piattaforma. | stringa |

{style="table-layout:auto"}

DSP inserisce automaticamente le macro di clic di visualizzazione in un tag di visualizzazione di terze parti quando:

* Esportare i tag annuncio da un partner di ad server <!-- [Needs PM confirmation.] -->
* Caricamento in blocco [!DNL Flashtalking] o [!DNL Google DoubleClick for Advertisers] tag pubblicitari direttamente nell’DSP

DSP Se durante la creazione di un annuncio pubblicitario non viene visualizzata una macro di clic, viene visualizzato un messaggio di avviso che richiede di inserire manualmente la macro di clic di visualizzazione appropriata nell&#39;area corretta del tag.

## [!DNL Analytics for Advertising] Macro

Per ulteriori macro disponibili in modo specifico per [[!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) clienti, consulta &quot;[Aggiungi [!DNL Analytics for Advertising] Macro per [!DNL Flashtalking] Tag annuncio](/help/integrations/analytics/macros-flashtalking.md)&quot; e &quot;[Aggiungi [!DNL Analytics for Advertising] Macro per [!DNL Google Campaign Manager 360] Tag annuncio](/help/integrations/analytics/macros-google-campaign-manager.md).&quot;

## Risoluzione dei problemi relativi agli errori delle macro

Quando si aggiungono macro al codice, assicurarsi di utilizzare la sintassi esatta della macro. Durante la convalida delle macro, DSP verifica che la macro corrisponda esattamente a una delle macro valide.

Se all&#39;inizio o alla fine del nome della macro mancano dei caratteri, vengono generati errori. Ad esempio, viene visualizzato un messaggio di errore se:

* Si dimenticano uno o più caratteri all&#39;inizio del nome della macro, ad esempio `${`. Se non si include la sintassi completa, la voce non verrà riconosciuta come macro valida.
* La macro non termina con un set di caratteri valido, ad esempio `}`.

>[!MORELIKETHIS]
>
>* [Impostazioni annuncio audio](/help/dsp/campaign-management/ads/ad-settings-audio.md)
>* [Impostazioni annuncio TV collegato](/help/dsp/campaign-management/ads/ad-settings-connected-tv.md)
>* [Visualizza impostazioni annuncio](/help/dsp/campaign-management/ads/ad-settings-display.md)
>* [Impostazioni annuncio mobile](/help/dsp/campaign-management/ads/ad-settings-mobile.md)
>* [Impostazioni annuncio nativo](/help/dsp/campaign-management/ads/ad-settings-native.md)
>* [Impostazioni annuncio pre-roll](/help/dsp/campaign-management/ads/ad-settings-pre-roll.md)
>* [Impostazioni annuncio video universale](/help/dsp/campaign-management/ads/ad-settings-universal-video.md)
