---
source-git-commit: 546e391745b1469efbcc9c2024dfc193224f0ed0
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 0%

---
# ID di Adobe Advertising EF

## ID di Adobe Advertising EF

L’ID EF è un token univoco utilizzato da Adobe Advertising per associare l’attività a un clic online o a un’esposizione pubblicitaria a livello di singolo browser o dispositivo. Gli ID EF fungono principalmente da chiavi per l&#39;invio di dati [!DNL Analytics] e di dati Customer Journey Analytics ad Adobe Advertising per la generazione di rapporti e l&#39;ottimizzazione delle offerte in Adobe Advertising.

Per [!DNL Analytics], l&#39;ID EF è memorizzato nella dimensione [an [!DNL Analytics] [!DNL eVar]](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) o [!DNL rVar] (riservata [!DNL eVar]) (ID EF Adobe Advertising).

Per Customer Journey Analytics, l&#39;ID EF è memorizzato nella proprietà `trackingIdentities` dell&#39;oggetto `conversionDetails`, che fa parte di [l&#39;oggetto [!UICONTROL Adobe Advertising Cloud ExperienceEvent Full Extension]](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/field-groups/event/advertising-full-extension).

### Formati ID EF {#ef-id-formats}

Vedere i [formati per gli elementi dimensione ID EF](https://experienceleague.adobe.com/en/docs/analytics/components/dimensions/amo-ef-id#dimension-items) nella &quot;Guida ai componenti di Adobe Analytics&quot;.

>[!NOTE]
>
>Gli ID EF fanno distinzione tra maiuscole e minuscole. Se un&#39;implementazione di [!DNL Analytics] o Customer Journey Analytics forza il tracciamento URL in minuscolo, Adobe Advertising non riconosce l&#39;ID EF. Questo influisce sulle offerte e sul reporting di Adobe Advertising, ma non ha alcun impatto sul reporting di Adobe Advertising in [!DNL Analytics] o Customer Journey Analytics.

<!-- Legacy content:

#### [!DNL Google Ads] search ads

```
{gclid}:G:s
```

where:

* `gclid` is the [!DNL Google Click ID] (GCLID).
* `s` is the network type ("s" for search).

#### [!DNL Microsoft Advertising] search ads

```
{msclkid}:G:s
```

where:

* `msclkid` is the [!DNL Microsoft Click ID] (MSCLKID).
* `s` is the network type ("s" for search).

#### Display ads and search ads on other search engines 

```
<Adobe Advertising visitor ID>:<timestamp>:<channel type>
```

where:

* <*Adobe Advertising visitor ID*> is a unique ID per visitor (such as UhKVaAAABCkJ0mDt). Also called the *surfer ID*.

* <*timestamp*> is the time in the format YYYYMMDDHHMMSS (such as 20190821192533 for Year 2019, Month 08, Day 21, Time 19:25:33).

* <*channel type*> is the channel type responsible for the click or exposure:

    * `d` for a click on a DSP display ad (display click-through)
    * `i` for an impression of a DSP display ad (display view-through)
    * `s` for a click on a Search ad (search click-through).

Example `EF ID: WcmibgAAAHJK1RyY:1551968087687:d`

-->
