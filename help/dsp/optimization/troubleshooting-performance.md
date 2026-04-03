---
title: Risoluzione dei problemi relativi alle prestazioni
description: Fai riferimento ai problemi di prestazioni comuni e scopri come risolverli.
feature: DSP Optimization
exl-id: b87f8556-1908-40c1-9f98-fbdc6d9b59b1
TQID: https://experienceleague.adobe.com/CLEAjCOYzIKDaAbH4-mZxna7MK5jmpvaCjdhGScwzQs
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2:
  - id: af280ddc-b4d0-4416-86be-8f3ea3c6ebe7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 519
ht-degree: 0%

---

# Risoluzione dei problemi relativi alle prestazioni

| Problema | Possibile causa | Azioni da intraprendere |
| --- | --- | --- |
| Nessuna spesa per il posizionamento | Il posizionamento non include annunci e/o gli annunci non sono attivi. | Verifica che tutti gli annunci previsti siano allegati al posizionamento e siano approvati e attivi.<br><br>Inoltre, verifica se il posizionamento include una pianificazione pubblicitaria personalizzata, che può limitare il periodo di volo per ogni annuncio. Per visualizzare la pianificazione degli annunci per un posizionamento dalla vista Posizionamenti, fai clic su **[!UICONTROL ...]** > **[!UICONTROL Ad schedule]** accanto al nome del posizionamento. |
| | Le date interessate non rientrano nelle date di volo configurate. | Verifica che le date di volo siano valide a livello di campagna, pacchetto e &#x200B;. |
| | L&#39;obiettivo di budget è stato raggiunto e/o non è abbastanza alto. | Controlla le impostazioni del budget a livello di campagna, pacchetto e posizionamento. |
| | L&#39;account non dispone di fondi sufficienti. | Per verificare se l&#39;account è adeguatamente finanziato, passa a **[!UICONTROL Settings]** > **[!UICONTROL Account]** e controlla l&#39;importo di [!UICONTROL Usable Funds]. Se hai bisogno di aggiungere altri fondi, contatta il team del tuo account Adobe. |
| | Nessun inventario disponibile. | Verificare se le origini inventario specificate ([!UICONTROL Public], [!UICONTROL Private] o [!UICONTROL On Demand]) sono:<ul><li>Imposta correttamente.</li><li>Attivo e invio tramite aste.</li><li>Compatibile con il tipo di annuncio e posizionamento applicabile.</li></ul><br>Se tutte le origini inventariali sono valide e attive, eseguire il targeting di altre origini inventario o di tutte le origini inventariali quando possibile. |
| | Nessun utente disponibile. | Verifica che le destinazioni del pubblico specificato includano un numero sufficiente di utenti attivi. In caso contrario, espandi le destinazioni aggiungendo più tipi di pubblico. |
| Bassa spesa per il posizionamento | La sezione [!UICONTROL Non Bids] del report di diagnostica del posizionamento mostra i possibili motivi per cui il posizionamento non è stato offerto. | [Rivedi il rapporto [!UICONTROL Non Bids]](/help/dsp/campaign-management/reports/placement-diagnostics.md) per capire perché il posizionamento non ha fatto un&#39;offerta.  <!-- add link/edit text when file available: See the [in-depth guide to possible Non-Bid Reasons (NBR)](link) for more information. --> |
| | Il posizionamento utilizza [filtri pre-offerta](/help/dsp/campaign-management/placements/placement-settings.md) che limitano le offerte. | Abbassa le soglie dei filtri pre-offerta del 5% per valutare il rapporto tra spesa e prestazioni. <!-- wording? and are users just supposed to manually monitor whether it makes a difference? --><br><br>Tieni presente che l&#39;utilizzo di più destinazioni di posizionamento, come filtri pre-offerta, geos, inventario e pubblico, può limitare cumulativamente le offerte e la spesa. |
| | Il posizionamento ha un tasso di vincita basso. | Aumenta [!UICONTROL Max Bid] per migliorare il tasso di vincita.<br><br><b>NOTA:</b> i prezzi di inventario possono variare in base al targeting del posizionamento.<br><br>Una percentuale di vincita del 10% è considerata valida. |
| | È disponibile un numero limitato di scorte. | Eseguire il targeting di tutte le origini inventario o di quelle aggiuntive, se possibile.<br><br>Tieni presente che l&#39;utilizzo di più destinazioni di posizionamento, come filtri pre-offerta, geos, inventario e pubblico, può limitare cumulativamente le offerte e la spesa. |
| | È disponibile un numero limitato di utenti. | Verifica che le destinazioni del pubblico specificato includano un numero sufficiente di utenti attivi. In caso contrario, espandi le destinazioni aggiungendo più tipi di pubblico.<br><br>Tieni presente che l&#39;utilizzo di più destinazioni di posizionamento, come filtri pre-offerta, geos, inventario e pubblico, può limitare cumulativamente le offerte e la spesa. |
| | Il pacchetto include un numero elevato di posizionamenti attivi. | Riduci il numero di posizionamenti attivi all’interno del pacchetto o aumenta il budget complessivo del pacchetto.<br><br>Se il pacchetto contiene molti posizionamenti ma il budget non è sufficiente, DSP potrebbe non essere in grado di allocare un budget sufficiente per ogni posizionamento. Ogni posizionamento dovrebbe avere l’opportunità di spendere almeno 2 USD al giorno. Ad esempio, se il tuo pacchetto ha un budget di 10 USD al giorno, è meglio includere cinque o meno posizionamenti. &#x200B; |

{style="table-layout:auto"}

>[!MORELIKETHIS]
>
>* [Impostazioni posizionamento](/help/dsp/campaign-management/placements/placement-settings.md)
>* [Impostazioni pacchetto](/help/dsp/campaign-management/packages/package-settings.md)
>* [Impostazioni campagna](/help/dsp/campaign-management/campaigns/campaign-settings.md)
