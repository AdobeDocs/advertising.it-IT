---
title: Gestire i pixel di retargeting
description: Scopri come creare e implementare pixel di retargeting da utilizzare come destinazioni per le esperienze pubblicitarie.
feature: Creative Pixels
exl-id: dcd13c5a-315d-4380-99f9-6dbab3e1e1be
source-git-commit: 1d0a1640eb2d19b8765150226e7185602bbfd495
workflow-type: tm+mt
source-wordcount: '922'
ht-degree: 0%

---

# Gestire i pixel di retargeting

<!-- Note to self: These aren't segments -- we don't create a pool of users. -->

Puoi creare un pixel di retargeting per identificare i visitatori nelle pagine di destinazione o conversione di un inserzionista utilizzando cookie dell’utente o ID universali e per acquisire attributi specifici tracciati dalle pagine per tali visitatori. Il pixel tiene traccia dell’evento più recente eseguito dal visitatore sulla pagina. Una volta creato il pixel, è possibile generare un tag pixel da inserire nelle pagine Web pertinenti per iniziare a tenere traccia dei visitatori.<!-- Note to self: surfer id=cookie or universal ID -->

Puoi quindi utilizzare il pixel come destinazione per qualsiasi contenuto creativo all’interno di un’esperienza pubblicitaria per mostrare annunci solo agli utenti con attributi specifici che hanno visitato in precedenza le pagine web associate al pixel. Ad esempio, puoi eseguire il targeting dei visitatori che guardano le scarpe rosse nella dimensione 10, se le pagine web tengono traccia di tali valori di attributo.<!-- better example? Make sure they match attribute examples below -->

I profili di retargeting vengono memorizzati per 180 giorni.

Esempio di pixel:

```
<img src="https://creative-assets-uat.efrontier.com/creative/scripts/rt.js?advId=141731&pxId=oGwrDCSZRWu5ZQKSEy8Y&ut1=--Insert Color--&ut2=--Insert Size--" />  <script src="https://creative-assets-uat.efrontier.com/creative/scripts/rt.js?advId=141731&cro=F&id5Consent=T&id5pid=--Insert ID5_PARTNER_ID--&lrConsent=T&pxId=oGwrDCSZRWu5ZQKSEy8Y&ut1=--Insert Color--&ut2=--Insert Size--"></script>
```

>[!NOTE]
>
> * [!DNL Creative] attualmente supporta ID universali solo per Advertising DSP. Una versione futura supporterà gli ID universali per DSP di terze parti.<!-- Clarify this and reword as needed  -->
>* Puoi anche utilizzare i tipi di pubblico di prime parti da Adobe Audience Manager e Adobe Analytics come [target creativi per le esperienze](/help/creative/experiences/experience-settings-targeting.md).
>* Quando utilizzi un’esperienza come annuncio all’interno di un posizionamento Advertising DSP, puoi indirizzare il posizionamento a tutti i tipi di pubblico disponibili in DSP. Puoi anche [creare tag personalizzati per i segmenti di pubblico](/help/dsp/audiences/custom-segment-create.md) per tenere traccia di tutti i visitatori su pagine di destinazione specifiche e quindi utilizzare tali segmenti come target creativi per un posizionamento.
>* I visitatori del sito web che hanno rinunciato al tracciamento per il targeting degli annunci non ricevono annunci con contenuto creativo personalizzato in base al segmento di pubblico o al profilo di retargeting.

## Creare un pixel di retargeting

1. Nel menu principale, fare clic su **[!UICONTROL Creative]** > **[!UICONTROL Creative Pixels]**.

1. Sopra la tabella dati, fare clic su **[!UICONTROL Creative]**, quindi selezionare > **[!UICONTROL Retargeting Pixel]**.

1. Specifica le [impostazioni pixel di retargeting](#retargeting-pixel-settings).

1. Fare clic su **[!UICONTROL Save]**.

1. [Genera il tag pixel](#retargeting-pixel-generate) da fornire all&#39;inserzionista o al contatto del sito Web.

   Il tag pixel di retargeting deve essere l&#39;ultima azione sulla pagina.<!-- verify here and below -->

   Il reparto IT dell’inserzionista o un altro gruppo potrebbe dover pianificare la distribuzione dei tag o esserne informato.

## Modificare un pixel di retargeting

1. Nel menu principale, fare clic su **[!UICONTROL Creative]** > **[!UICONTROL Creative Pixels]**.

1. Tenere premuto il cursore sul nome del pixel e fare clic su **[!UICONTROL Edit]**.

1. Modifica le [impostazioni pixel di retargeting](#retargeting-pixel-settings).

1. Fare clic su **[!UICONTROL Save]**.

1. [Generare il tag pixel](#retargeting-pixel-generate) da fornire all&#39;inserzionista o al contatto del sito Web in modo che possano sostituire il tag originale.

   Il tag pixel di retargeting deve essere l’ultima azione sulla pagina di destinazione.

   Il reparto IT dell’inserzionista o un altro gruppo potrebbe dover pianificare la distribuzione dei tag o esserne informato.

## Generare un tag per un pixel di retargeting {#retargeting-pixel-generate}

1. Nel menu principale, fare clic su **[!UICONTROL Creative]** > **[!UICONTROL Creative Pixels]**.

1. Tenere premuto il cursore sul nome del pixel e fare clic su **[!UICONTROL Generate Tag]**.

1. Fare clic su **[!UICONTROL Copy to Clipboard]** per copiare il tag negli Appunti del computer, da cui è possibile incollare il testo in un file da salvare.

1. Nel tag pixel, specificare un valore per ogni attributo nelle sezioni `<img src>` e `<script src>` sostituendo ogni &quot;`Insert <attribute>`&quot; con un valore. Se il tag acquisisce un ID universale, specifica un ID partner ID5.

   Se aggiungi manualmente attributi aggiuntivi, devi includere la codifica URL.

   Ad esempio, se hai incluso gli attributi &quot;category&quot;, &quot;color&quot; e &quot;size&quot; e acquisisci ID5 ID universali, il tag pixel include i seguenti parametri: `&ut1=--Insert category--&ut2=--Insert color--&ut3=--Insert size--` e `&id5pid=--Insert ID5_PARTNER_ID--`. Per eseguire il targeting degli utenti che selezionano sandali rossi nella dimensione 10, ad esempio, modifica i parametri sia nel tag immagine che nel tag script in `&ut1=sandals&ut2=red&ut3=10` e immetti anche l&#39;ID partner ID5 nel tag script, ad esempio `&id5pid=0123456789`.

   `<img src="https://creative-assets-uat.efrontier.com/creative/scripts/rt.js?advId=141731&pxId=oGwrDCSZRWu5ZQKSEy8Y&ut1=--sandals--&ut2=--red--&ut3=--10--" />  <script src="https://creative-assets-uat.efrontier.com/creative/scripts/rt.js?advId=141731&cro=F&id5Consent=T&id5pid=--0123456789--&lrConsent=T&pxId=oGwrDCSZRWu5ZQKSEy8Y&ut1=--sandals--&ut2=--red--&ut3=--10--"></script>`

1. Fornisci il tag pixel completato all’inserzionista o al contatto del sito web, insieme a un elenco delle pagine di destinazione pertinenti in cui inserirlo.

   Il tag pixel di retargeting deve essere l’ultima azione sulla pagina di destinazione.

   Il reparto IT dell’inserzionista o un altro gruppo potrebbe dover pianificare la distribuzione dei tag o esserne informato.

## Eliminare un pixel di retargeting

1. Nel menu principale, fare clic su **[!UICONTROL Creative]** > **[!UICONTROL Creative Pixels]**.

1. Tenere premuto il cursore sul nome del pixel e fare clic su **[!UICONTROL Delete]**.

1. Nel messaggio di conferma, fare clic su **[!UICONTROL Delete]**.

## Impostazioni dei pixel di retargeting {#retargeting-pixel-settings}

**[!UICONTROL Pixel Name]:** Il nome del pixel. **Nota:** il tag pixel include l&#39;ID pixel (`pxId=<ID>`), non il nome pixel.

**[!UICONTROL Advertiser]:** (sola lettura per pixel esistenti) L&#39;inserzionista per il quale viene tracciato il pixel.

**[!UICONTROL Attribute 1]:** attributo da includere nel tag pixel, ad esempio &quot;SKU&quot;, &quot;category&quot;, &quot;size&quot; o altri attributi della pagina o del prodotto visualizzato nella pagina. Specifica un valore per l’attributo nel tag pixel prima di inserirlo nelle pagine web pertinenti.

Quando esegui il targeting di esperienze pubblicitarie per utenti esposti al pixel, le impostazioni di targeting specificano i valori di attributo che devono essere presenti per visualizzare i creativi.

**[!UICONTROL Attribute 2]**, **[!UICONTROL Attribute 3]**, **[!UICONTROL Attribute 4]**, **[!UICONTROL Attribute 5]:** (Facoltativo) Attributi aggiuntivi da includere nel tag pixel. Specifica un valore per ogni attributo aggiuntivo nel tag pixel prima di inserirlo nelle pagine Web pertinenti.

Quando esegui il targeting di esperienze pubblicitarie per utenti esposti al pixel, le impostazioni di targeting specificano i valori di attributo che devono essere presenti per visualizzare i creativi.

**[!UICONTROL Advanced]** > **[!UICONTROL Universal IDs]:** (solo nuovi pixel; facoltativo) Tipi di ID universali per il tag pixel da tracciare:

* *[!UICONTROL ID5]:* Il tag pixel traccia [!DNL ID5] ID. Non viene applicata alcuna tariffa per le impression consegnate agli ID universali.

* *[!UICONTROL Ramp ID]:* Il tag pixel traccia [!DNL Ramp IDs]. Non viene applicata alcuna tariffa per le impression consegnate agli ID universali.

DSP Per utilizzare questa funzione, prima di poter utilizzare gli ID universali per un nuovo tipo di ID, è necessario accettare i termini del contratto di servizio per l&#39;utilizzo degli ID universali una sola volta. Per i clienti con contratti di assistenza gestiti, il team dell’account Adobe riceverà il consenso e accetterà le condizioni per conto della tua organizzazione. Per leggere i termini, fare clic su **[!UICONTROL Terms of Service]**. Per accettare i termini, scorrere fino alla fine dei termini e fare clic su **[!UICONTROL Accept]**.

>[!MORELIKETHIS]
>
>* [Impostazioni esperienza annuncio di destinazione](/help/creative/experiences/experience-settings-targeting.md)
>* [Informazioni sulle esperienze pubblicitarie](/help/creative/experiences/experience-about.md)
