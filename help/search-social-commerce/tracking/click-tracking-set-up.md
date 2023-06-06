---
title: Configurare il tracciamento dei clic basato su cookie
description: Scopri come impostare e convalidare i tag di tracciamento dei clic.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '541'
ht-degree: 0%

---

# Configurare il tracciamento dei clic basato su cookie

Affinché Search, Social e Commerce possano tenere traccia dei clic, è necessario configurare e convalidare i seguenti elementi.

1. (Adobe Account Team) Imposta l’inserzionista come cliente pixel.

1. [Specifica le opzioni di tracciamento corrette per ciascuno degli account e delle campagne della rete di annunci dell’inserzionista](#set-up-click-tracking-options).

1. Se necessario, [generare URL di tracciamento e caricarli](#generate-upload-tracking-urls) per alcuni elementi della campagna.

1. [Convalida il formato di alcuni degli URL di tracciamento dei clic e testali per verificare che venga aperta la pagina di destinazione corretta](#validate-tracking-urls).

## Configurare le opzioni di tracciamento per gli account e le campagne della rete di annunci {#set-up-click-tracking-options}

*Account manager dell’agenzia, [!DNL Adobe] solo ruoli utente amministratore e responsabile account*

1. Per ogni account di rete di annunci, effettua le seguenti operazioni:

   1. Nel menu principale, fai clic su **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Nei sottomenu, fare clic su **[!UICONTROL Live]>[!UICONTROL Accounts]**.

   1. Posizionare il cursore sul nome dell&#39;account e fare clic su ![Icona menu](/help/search-social-commerce/assets/arrow-dropdown-menu.png "Icona menu"), quindi selezionare **[!UICONTROL Edit]**.

   1. Clic **[!UICONTROL Set Account Tracking]**.

   1. Per [!UICONTROL Tracking Type] impostazione, seleziona **[!UICONTROL EF Redirect]**.

   1. (per consentire a Search, Social e Commerce di scambiare dati con Adobe Analytics o di tenere traccia delle conversioni che si verificano in [!DNL Apple Safari]a) Selezionare [!UICONTROL Redirect Type] opzione **[!UICONTROL Token]**.

   1. (Facoltativo) Attiva il **[!UICONTROL Auto Upload]** opzione per caricare automaticamente nuovi URL di tracciamento nella rete di annunci alla successiva sincronizzazione tra Search, Social e Commerce. Questo valore viene ereditato come predefinito per tutte le campagne nell’account, ma può essere sostituito a livello di campagna.

1. Per ogni campagna, effettua le seguenti operazioni:

   1. Nel menu principale, fai clic su **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Nei sottomenu, fare clic su **[!UICONTROL Live]>[!UICONTROL Campaigns]**.

   1. Posiziona il cursore sul nome della campagna e fai clic su ![Icona menu](/help/search-social-commerce/assets/arrow-dropdown-menu.png "Icona menu"), quindi selezionare **[!UICONTROL Edit]**.

   1. Clic **[!UICONTROL Set Campaign Tracking]**. Quindi seleziona l’opzione per **[!UICONTROL Override Account Tracking]**.

   1. Per [!UICONTROL Tracking Type] impostazione, seleziona **[!UICONTROL EF Redirect]**.

   1. (per consentire a Search, Social e Commerce di scambiare dati con Adobe Analytics o di tenere traccia delle conversioni che si verificano in [!DNL Apple Safari]a) Selezionare [!UICONTROL Redirect Type] opzione **[!UICONTROL Token]**.

   1. (Facoltativo) Attiva il **[!UICONTROL Auto Upload]** opzione per caricare automaticamente nuovi URL di tracciamento nella rete di annunci alla successiva sincronizzazione tra Search, Social e Commerce. Questo valore viene ereditato come predefinito per tutte le campagne nell’account, ma può essere sostituito a livello di campagna.

## Generare e caricare gli URL di tracciamento {#generate-upload-tracking-urls}

Consulta &quot;[Quando e come generare URL di tracciamento dei clic](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md).&quot;

### Verificare il formato degli URL di tracciamento dei clic {#validate-tracking-urls}

Verifica che venga visualizzata la pagina di destinazione corretta per l’URL di tracciamento dei clic.

1. Imita un clic dell’annuncio inviando il traffico all’ambiente di staging dell’inserzionista:

   1. In un editor di testo, incolla un URL di tracciamento dei clic, modifica l’URL della pagina di destinazione in modo che punti alla stessa pagina nell’ambiente di staging dell’inserzionista, quindi incolla il nuovo URL nella barra degli indirizzi del browser e premi **[!DNL Enter]** chiave.

   1. Cerca il cookie nei cookie memorizzati del browser.

   1. Completa una transazione sul sito di staging e verifica che la pagina di successo attivi il pixel corretto. I parametri effettivi tracciati dal pixel variano a seconda dell’inserzionista e dell’URL di tracciamento. Nell’esempio seguente, l’inserzionista desidera tenere traccia del numero di nuove applicazioni e dell’importo dei nuovi ricavi:

      Per un nuovo utente finale (con un nuovo cookie), deve essere attivato il seguente pixel:

      `< img width="1" height="1" src="http://pixel-user-everesttech.net/<Advertising_Cloud_UserID>/p?ev_transid=<applicationid>&ev_new_application=1&ev_new_amount=<loanamount>" / >`

      Se il cookie non è nuovo, viene attivato il seguente pixel:

      `< img width="1"height="1" src="http://pixel-user-everesttech.net/<Advertising_Cloud_UserID>/p?ev_transid=<applicationid>&ev_previous_application=1&ev_new_amount=<loanamount>" / >`


1. Ripeti l’operazione per diversi URL di tracciamento dei clic nel dominio.

1. Ripeti il passaggio 1 per ogni dominio, utilizzando di conseguenza una pagina di destinazione diversa.

1. Se necessario, verifica che Search, Social e Commerce possano visualizzare i pixel degli ID transazione (`ev_transid`) generato durante il test.

>[!MORELIKETHIS]
>
>* [Quando e come generare URL di tracciamento dei clic](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md)

