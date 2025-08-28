---
source-git-commit: 8c36de7ffe73f86a4e78f11e38cd84fa59134833
workflow-type: tm+mt
source-wordcount: '234'
ht-degree: 0%

---
# ID di Adobe Advertising EF

## ID di Adobe Advertising EF

L’ID EF è un token univoco utilizzato da Adobe Advertising per associare l’attività a un clic online o a un’esposizione pubblicitaria. L&#39;ID EF è memorizzato nella dimensione [an [!DNL Analytics] [!DNL eVar]](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) o [!DNL rVar] (riservato [!DNL eVar]) (ID EF di Adobe Advertising) e tiene traccia di ogni clic di annuncio o esposizione a livello di singolo browser o dispositivo. Gli ID EF fungono principalmente da chiavi per l&#39;invio di dati [!DNL Analytics] ad Adobe Advertising per il reporting e l&#39;ottimizzazione delle offerte in Adobe Advertising.

### Formato ID EF

>[!NOTE]
>
>Gli ID EF fanno distinzione tra maiuscole e minuscole. Se un&#39;implementazione di [!DNL Analytics] impone il tracciamento URL in minuscolo, Adobe Advertising non riconosce l&#39;ID EF. Questo influisce sulle offerte e sul reporting di Adobe Advertising, ma non ha alcun impatto sul reporting di Adobe Advertising entro [!DNL Analytics].

#### [!DNL Google Ads] annunci di ricerca

```
{gclid}:G:s
```

dove:

* `gclid` è [!DNL Google Click ID] (GCLID).
* `s` è il tipo di rete (&quot;s&quot; per la ricerca).

#### [!DNL Microsoft Advertising] annunci di ricerca

```
{msclkid}:G:s
```

dove:

* `msclkid` è [!DNL Microsoft Click ID] (MSCLKID).
* `s` è il tipo di rete (&quot;s&quot; per la ricerca).

#### Visualizzare annunci e annunci di ricerca su altri motori di ricerca

```
<Adobe Advertising visitor ID>:<timestamp>:<channel type>
```

dove:

* &lt;*ID visitatore Adobe Advertising*> è un ID univoco per visitatore (ad esempio, UhKVaAAABCkJ0mDt). Chiamato anche *ID surfista*.

* &lt;*timestamp*> è l&#39;ora nel formato AAAAMMGGHHMMSS (ad esempio 20190821192533 per Anno 2019, Mese 08, Giorno 21, Ora 19:25:33).

* &lt;*tipo di canale*> è il tipo di canale responsabile del clic o dell&#39;esposizione:

   * `d` per un clic su un annuncio di visualizzazione di DSP (click-through di visualizzazione)
   * `i` per un&#39;impression di un annuncio di visualizzazione DSP (view-through di visualizzazione)
   * `s` per un clic su un annuncio di ricerca (click-through di ricerca).

Esempio `EF ID: WcmibgAAAHJK1RyY:1551968087687:d`
