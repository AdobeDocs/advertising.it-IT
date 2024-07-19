---
title: Integrazione con le soluzioni e i servizi Adobe Experience Cloud
description: Scopri le integrazioni Search, Social e Commerce con le soluzioni e i servizi Adobe Experience Cloud.
exl-id: 26456f60-937a-4f39-b5cf-a71c1c1b4833
feature: Search Introduction
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '523'
ht-degree: 0%

---

# Integrazione con le soluzioni e i servizi Adobe Experience Cloud

Advertising Search, Social e Commerce sono integrati con i seguenti prodotti [!DNL Adobe].

* [Tag da Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/client/overview.html): è possibile utilizzare l&#39;estensione [Adobe Advertising Cloud](https://exchange.adobe.com/apps/ec/100155) per Adobe Experience Platform per creare Adobi Advertising tag di tracciamento delle conversioni e tag di tracciamento di terze parti per le pagine di destinazione degli annunci. (Puoi anche [creare tag di tracciamento della conversione direttamente in Search, Social e Commerce](/help/search-social-commerce/tools/conversion-tag-generate.md).) Contatta il team dell’account Adobe o il team di implementazione per informazioni da includere nei tag.

* Adobe Analytics — (funzione Opt-in) Adobe Advertising e [!DNL Analytics] sono integrati nei seguenti modi:

   * Adobe Advertising e [!DNL Analytics] condividono i dati in modo semplice. [!DNL Analytics] può inviare quotidianamente i dati su conversione e coinvolgimento sul sito a Search, Social e Commerce, dove i dati sono disponibili per l&#39;ottimizzazione degli annunci e per il reporting. Adobe Advertising può inoltre inviare quotidianamente i dati sul traffico pubblicitario, inclusi impression, clic e costi, dalle reti pubblicitarie a [!DNL Analytics], dove i dati sono disponibili in tutti gli strumenti di reporting.

     Per ulteriori informazioni sul supporto di [!DNL Analytics] per ogni rete di annunci e tipo di annuncio, vedere &quot;[Inventario supportato](/help/search-social-commerce/introduction/supported-inventory.md)&quot;. Vedere anche &quot;[Panoramica di [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html){target="_blank"}&quot; per ulteriori informazioni sullo scambio di dati.

     Per scambiare i dati, è necessario configurare inizialmente sia Adobe Advertising che [!DNL Analytics]. Per ulteriori informazioni sulla configurazione iniziale, contatta il team dell’account di Adobe.

     >[!NOTE]
     >
     >Per impostazione predefinita, le metriche [!DNL Analytics] non sono visibili nelle schermate Search, Social e Commerce. È necessario [rendere le metriche disponibili in modo esplicito nelle visualizzazioni di gestione delle campagne, nei portfolio e nei report](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md) dopo che il team di implementazione di [!DNL Adobe] ha configurato gli eventi standard o personalizzati selezionati da passare all&#39;Adobe Advertising. Facoltativamente, è possibile modificare i nomi delle metriche visualizzate (senza modificarli in [!DNL Analytics]). È possibile rendere le metriche visualizzabili nell&#39;interfaccia utente e rinominare le metriche da [!UICONTROL Admin] > [!UICONTROL Conversions].

   * Gli inserzionisti con [!DNL Analytics] ma non Audience Manager possono [creare [!DNL Google Ads] audience di corrispondenza cliente](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md) da [!DNL Analytics] segmenti condivisi con Adobe Experience Cloud. Per essere idoneo, un inserzionista deve implementare il [servizio Adobe Experience Platform Identity](https://experienceleague.adobe.com/docs/id-service/using/home.html) e distribuire un tag sui propri siti Web. Puoi quindi utilizzare i tipi di pubblico nelle campagne [!DNL Google Ads] come [destinazioni](/help/search-social-commerce/campaign-management/campaigns/audience-targets-manage.md) o [esclusioni](/help/search-social-commerce/campaign-management/campaigns/audience-exclusions-manage.md) a livello di campagna o di gruppo di annunci.

* Segmenti di Adobe Audience Manager — (funzione Opt-in) È possibile [creare [!DNL Google Ads] tipi di pubblico corrispondenti ai clienti](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md) da segmenti di Audience Manager con Search, Social e Commerce come destinazione. Possono essere inclusi [!DNL Analytics] segmenti pubblicati in Adobe Experience Cloud e segmenti creati utilizzando la Libreria tipi di pubblico di Adobe Experience Cloud. Puoi quindi utilizzare i tipi di pubblico nelle campagne [!DNL Google Ads] come [destinazioni](/help/search-social-commerce/campaign-management/campaigns/audience-targets-manage.md) o [esclusioni](/help/search-social-commerce/campaign-management/campaigns/audience-exclusions-manage.md) a livello di campagna o di gruppo di annunci.

  Per ulteriori informazioni, vedere &quot;[Integrazioni Adobe Advertising con Adobe Audience Manager](https://experienceleague.adobe.com/docs/advertising/integrations/audience-manager/overview.html)&quot;.

* Adobe Target: è possibile implementare la condivisione del segnale di click-through tra Search, Social e Commerce e [!DNL Target], impostare un&#39;attività di test A/B in [!DNL Target] per gli annunci, quindi utilizzare l&#39;Analysis Workspace [!DNL Analytics] per visualizzare i dati di test.

* Adobe Campaign: è possibile [creare e aggiornare un pubblico di tipo  [!DNL Google Ads] customer match utilizzando un elenco e-mail entro [!DNL Campaign]](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-campaign-email-list.md).

* Notifiche di Adobe Experience Cloud — (quando hai effettuato l&#39;accesso tramite Adobe Experience Cloud) Dal collegamento di notifica ([Notifiche di avviso](/help/search-social-commerce/assets/notifications-panel.png "Notifiche avvisi")) nella parte superiore di ogni pagina, puoi visualizzare tutti gli aggiornamenti di sistema, i post, le menzioni e le risorse condivise di Adobe Experience Cloud. Contatta il tuo Account Team di Adobi per informazioni sull’accesso a Adobe Experience Cloud.
