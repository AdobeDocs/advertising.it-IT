---
title: Integrazione con le soluzioni e i servizi Adobe Experience Cloud
description: Scopri le integrazioni di Search, Social e Commerce con le soluzioni e i servizi Adobe Experience Cloud.
exl-id: e8b521f5-f426-4c50-9df4-361a047c9ff0
feature: Search Introduction
source-git-commit: b730716565dfae9cb32556eaede1c3f29f316ac7
workflow-type: tm+mt
source-wordcount: '550'
ht-degree: 0%

---

# Integrazione con le soluzioni e i servizi Adobe Experience Cloud

Advertising Search, Social e Commerce è integrato con quanto segue [!DNL Adobe] prodotti.

* [Tag da Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/client/overview.html) — È possibile utilizzare [Estensione Adobe Advertising Cloud](https://exchange.adobe.com/apps/ec/100155) Adobe Experience Platform ti consente di creare Adobi Advertising di tag di tracciamento della conversione e di tag di tracciamento di terze parti per le pagine di destinazione degli annunci. (È inoltre possibile [creare tag di tracciamento delle conversioni direttamente in Search, Social &amp; Commerce](/help/search-social-commerce/tools/conversion-tag-generate.md).) Contatta il team dell’account Adobe o il team di implementazione per informazioni da includere nei tag.

* Adobe Analytics — (funzione Opt-in) Adobe Advertising e [!DNL Analytics] sono integrati nei seguenti modi:

   * ADOBE ADVERTISING e [!DNL Analytics] condividere i dati in modo semplice. [!DNL Analytics] può inviare giornalmente i dati su conversione e coinvolgimento sul sito a Search, Social e Commerce, dove i dati sono disponibili per l’ottimizzazione degli annunci e per il reporting. Inoltre, Adobi Advertising può inviare quotidianamente i dati sul traffico degli annunci, inclusi impression, clic e costi, dalle reti di annunci a [!DNL Analytics], dove i dati sono disponibili in tutti gli strumenti di reporting.

     Consulta &quot;[Inventario supportato](/help/search-social-commerce/introduction/supported-inventory.md)&quot; per ulteriori informazioni su [!DNL Analytics] supporto per ogni rete di annunci e tipo di annunci. Vedi anche &quot;[Panoramica di [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html){target="_blank"}&quot; per ulteriori informazioni sullo scambio di dati.

     Per scambiare dati, Adobe Advertising e [!DNL Analytics] deve essere inizialmente configurato. Per ulteriori informazioni sulla configurazione iniziale, contatta il team dell’account di Adobe.

     >[!NOTE]
     >
     >Per impostazione predefinita, il [!DNL Analytics] Le metriche non sono visibili nelle schermate Search, Social e Commerce. Devi specificare in modo esplicito [rendere le metriche disponibili nelle viste, nei portfolio e nei rapporti di gestione delle campagne](/help/search-social-commerce/admin/transaction-properties/transaction-property-about.md) dopo il [!DNL Adobe] il team di implementazione ha configurato alcuni eventi standard o personalizzati da passare all’Adobe Advertising. Facoltativamente, puoi modificare i nomi delle metriche visualizzate (senza modificarli in [!DNL Analytics]). Puoi rendere le metriche visualizzabili nell’interfaccia utente e rinominarle da [!UICONTROL Admin] > [!UICONTROL Transaction Properties].

   * Inserzionisti con [!DNL Analytics] ma non Audience Manager può [creare [!DNL Google Ads] audience di corrispondenza cliente](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md) da [!DNL Analytics] segmenti condivisi con Adobe Experience Cloud. Per essere idoneo, un inserzionista deve implementare [Servizio Adobe Experience Platform Identity](https://experienceleague.adobe.com/docs/id-service/using/home.html) e distribuire un tag sui propri siti web. Puoi quindi utilizzare i tipi di pubblico in [!DNL Google Ads] campagne a livello di campagna o di gruppo di annunci [target](/help/search-social-commerce/campaign-management/campaigns/audience-targets-manage.md) o [esclusioni](/help/search-social-commerce/campaign-management/campaigns/audience-exclusions-manage.md).

* Segmenti Adobe Audience Manager — (funzione Opt-in) È possibile: [creare [!DNL Google Ads] audience di corrispondenza cliente](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md) da segmenti di Audience Manager con Search, Social e Commerce come destinazione. Ciò può includere [!DNL Analytics] segmenti pubblicati in Adobe Experience Cloud e segmenti creati utilizzando la Libreria tipi di pubblico di Adobe Experience Cloud. Puoi quindi utilizzare i tipi di pubblico in [!DNL Google Ads] campagne a livello di campagna o di gruppo di annunci [target](/help/search-social-commerce/campaign-management/campaigns/audience-targets-manage.md) o [esclusioni](/help/search-social-commerce/campaign-management/campaigns/audience-exclusions-manage.md).

  Consulta &quot;[Integrazioni Adobi Advertising con Adobe Audience Manager](https://experienceleague.adobe.com/docs/advertising/integrations/audience-manager/overview.html)&quot; per ulteriori informazioni.

* Adobe Target: puoi implementare la condivisione del segnale click-through tra Search, Social e Commerce e [!DNL Target], configura un’attività di test A/B in [!DNL Target] per gli annunci, quindi utilizza [!DNL Analytics] Analysis Workspace per visualizzare i dati di test.

* Adobe Campaign — È possibile [creare e aggiornare un [!DNL Google Ads] customer match audience utilizzando un elenco e-mail all’interno di [!DNL Campaign]](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-campaign-email-list.md).

* Notifiche di Adobe Experience Cloud — (quando hai effettuato l&#39;accesso tramite Adobe Experience Cloud) Dal collegamento di notifica ([Notifiche avvisi](/help/search-social-commerce/assets/notifications-panel.png "Notifiche avvisi")) nella parte superiore di ogni pagina, puoi visualizzare tutti gli aggiornamenti di sistema, i post, le menzioni e le risorse condivise di Adobe Experience Cloud. Contatta il tuo Account Team di Adobi per informazioni sull’accesso a Adobe Experience Cloud.
