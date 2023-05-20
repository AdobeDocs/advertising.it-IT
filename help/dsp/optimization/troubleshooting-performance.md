---
title: Risoluzione dei problemi relativi alle prestazioni
description: Fai riferimento ai problemi di prestazioni comuni e scopri come risolverli.
feature: DSP Optimization
exl-id: b87f8556-1908-40c1-9f98-fbdc6d9b59b1
source-git-commit: 14f78b89dea8cc680756232c6116975c652feee5
workflow-type: tm+mt
source-wordcount: '516'
ht-degree: 0%

---

# Risoluzione dei problemi relativi alle prestazioni

| Problema | Possibile causa | Azioni da intraprendere |
| --- | --- | --- |
| Nessuna spesa per il posizionamento | Il posizionamento non include annunci e/o gli annunci non sono attivi. | Verifica che tutti gli annunci previsti siano allegati al posizionamento e siano approvati e attivi.<br><br>Inoltre, verifica se il posizionamento include una pianificazione degli annunci personalizzata, che può limitare il periodo di volo per ogni annuncio. Per visualizzare la pianificazione degli annunci per un posizionamento dalla vista Posizionamenti, fai clic su  **[!UICONTROL ...]** > **[!UICONTROL Ad schedule]** accanto al nome del posizionamento. |
|  | Le date interessate non rientrano nelle date di volo configurate. | Verifica che le date di volo siano valide a livello di campagna, pacchetto e &#x200B;. |
|  | L&#39;obiettivo di budget è stato raggiunto e/o non è abbastanza alto. | Controlla le impostazioni del budget a livello di campagna, pacchetto e posizionamento. |
|  | L&#39;account non dispone di fondi sufficienti. | Per verificare se il tuo account è adeguatamente finanziato, vai a **[!UICONTROL Settings]** > **[!UICONTROL Account]** e osserva la quantità di [!UICONTROL Usable Funds]. Se hai bisogno di aggiungere altri fondi, contatta il tuo Account Team Adobe. |
|  | Nessun inventario disponibile. | Verifica se le origini magazzino specificate ([!UICONTROL Public], [!UICONTROL Private], o [!UICONTROL On Demand]) sono:<ul><li>Imposta correttamente.</li><li>Attivo e invio tramite aste.</li><li>Compatibile con il tipo di annuncio e posizionamento applicabile.</li></ul><br>Se tutte le origini inventariali sono valide e attive, eseguire il targeting di altre o di tutte le origini inventariali quando possibile. |
|  | Nessun utente disponibile. | Verifica che le destinazioni del pubblico specificato includano un numero sufficiente di utenti attivi. In caso contrario, espandi le destinazioni aggiungendo più tipi di pubblico. |
| Bassa spesa per il posizionamento | Il [!UICONTROL Non Bids] La sezione del rapporto di diagnostica del posizionamento mostra i possibili motivi per cui il posizionamento non è stato offerto. | [Rivedi [!UICONTROL Non Bids] rapporto](/help/dsp/campaign-management/reports/placement-diagnostics.md) per capire perché il posizionamento non è stato offerto.  <!-- add link/edit text when file available: See the [in-depth guide to possible Non-Bid Reasons (NBR)](link) for more information. --> |
|  | Il posizionamento utilizza [filtri pre-offerta](/help/dsp/campaign-management/placements/placement-settings.md) che limitano le offerte. | Abbassa le soglie dei filtri pre-offerta del 5% per valutare il rapporto tra spesa e prestazioni. <!-- wording? and are users just supposed to manually monitor whether it makes a difference? --><br><br>Tieni presente che l’utilizzo di più target di posizionamento, come filtri pre-offerta, geos, inventario e tipi di pubblico, può limitare cumulativamente le offerte e la spesa. |
|  | Il posizionamento ha un tasso di vincita basso. | Aumenta [!UICONTROL Max Bid] per migliorare il tasso di vincita.<br><br><b>NOTA:</b> I prezzi di inventario possono variare in base al targeting del posizionamento.<br><br>Un tasso di vincita del 10% è considerato sano. |
|  | È disponibile un numero limitato di scorte. | Eseguire il targeting di tutte le origini inventario o di quelle aggiuntive, se possibile.<br><br>Tieni presente che l’utilizzo di più target di posizionamento, come filtri pre-offerta, geos, inventario e tipi di pubblico, può limitare cumulativamente le offerte e la spesa. |
|  | È disponibile un numero limitato di utenti. | Verifica che le destinazioni del pubblico specificato includano un numero sufficiente di utenti attivi. In caso contrario, espandi le destinazioni aggiungendo più tipi di pubblico.<br><br>Tieni presente che l’utilizzo di più target di posizionamento, come filtri pre-offerta, geos, inventario e tipi di pubblico, può limitare cumulativamente le offerte e la spesa. |
|  | Il pacchetto include un numero elevato di posizionamenti attivi. | Riduci il numero di posizionamenti attivi all’interno del pacchetto o aumenta il budget complessivo del pacchetto.<br><br>Se il pacchetto ha molti posizionamenti ma non abbastanza budget, l&#39;DSP potrebbe non essere in grado di allocare abbastanza budget per ogni posizionamento. Ogni posizionamento dovrebbe avere l’opportunità di spendere almeno 2 USD al giorno. Ad esempio, se il tuo pacchetto ha un budget di 10 USD al giorno, è meglio includere cinque o meno posizionamenti. &#x200B; |

{style="table-layout:auto"}

>[!MORELIKETHIS]
>
>* [Impostazioni di posizionamento](/help/dsp/campaign-management/placements/placement-settings.md)
>* [Impostazioni pacchetto](/help/dsp/campaign-management/packages/package-settings.md)
>* [Impostazioni campagna](/help/dsp/campaign-management/campaigns/campaign-settings.md)

