---
title: Risoluzione dei problemi relativi alle prestazioni
description: Fai riferimento ai problemi di prestazioni comuni e scopri come risolverli.
feature: DSP Optimization
exl-id: b87f8556-1908-40c1-9f98-fbdc6d9b59b1
source-git-commit: 1a98b3ba7c37a768825e9e48db7d847f12daa9a0
workflow-type: tm+mt
source-wordcount: '518'
ht-degree: 0%

---

# Risoluzione dei problemi relativi alle prestazioni

| Problema | Possibile causa | Azioni da intraprendere |
| --- | --- | --- |
| Nessuna spesa per il posizionamento | Il posizionamento non include gli annunci e/o gli annunci non sono attivi. | Verifica che tutti gli annunci previsti siano collegati al posizionamento e siano approvati e attivi.<br><br>Inoltre, vedi se il posizionamento include un programma di annunci personalizzato, che può limitare il periodo di volo per ogni annuncio. Per visualizzare la pianificazione pubblicitaria di un posizionamento dalla vista Posizionamenti, fai clic su  **[!UICONTROL ...]** > **[!UICONTROL Ad schedule]** accanto al nome del posizionamento. |
|  | Le date interessate non rientrano nelle date di volo configurate. | Verifica che le date del volo siano valide a livello di campagna, pacchetto e posizionamento &#x200B; s. |
|  | L&#39;obiettivo di budget è stato raggiunto e/o non è abbastanza alto. | Controlla le impostazioni di budget a livello di campagna, pacchetto e posizionamento. |
|  | L&#39;account non ha abbastanza fondi. | Per vedere se il tuo account è adeguatamente finanziato, vai a **[!UICONTROL Settings]** > **[!UICONTROL Account]** e guarda la quantità di [!UICONTROL Usable Funds]. Se hai bisogno di aggiungere altri fondi, contatta il tuo [!DNL Adobe] team di account. |
|  | Nessun inventario disponibile. | Verifica se le origini di inventario specificate ([!UICONTROL Public], [!UICONTROL Private]oppure [!UICONTROL On Demand]) sono:<ul><li>Configurazione corretta.</li><li>Attivo e spedito attraverso le aste.</li><li>Compatibile con il tipo di annuncio e di posizionamento applicabile.</li></ul><br>Se le origini di inventario sono tutte valide e attive, eseguire il targeting di altre o di tutte le origini di inventario, se possibile. |
|  | Nessun utente disponibile. | Verifica che le destinazioni di pubblico specificate includano un numero sufficiente di utenti attivi. In caso contrario, espandi i target aggiungendo altri tipi di pubblico. |
| Riduzione della spesa per il posizionamento | La [!UICONTROL Non Bids] la sezione del report di diagnostica del posizionamento mostra possibili ragioni per cui il posizionamento non ha fatto offerte. | [Consulta la sezione [!UICONTROL Non Bids] rapporto](/help/dsp/campaign-management/reports/placement-diagnostics.md) per capire perché il posizionamento non ha fatto offerte.  <!-- add link/edit text when file available: See the [in-depth guide to possible Non-Bid Reasons (NBR)](link) for more information. --> |
|  | Il posizionamento utilizza [filtri pre-offerta](/help/dsp/campaign-management/placements/placement-settings.md) questo limita le offerte. | Abbassare del 5% le soglie dei filtri pre-offerta per valutare l’equilibrio tra spesa e prestazioni. <!-- wording? and are users just supposed to manually monitor whether it makes a difference? --><br><br>Tieni presente che l’utilizzo di più target di posizionamento, come filtri preofferta, geo, inventario e pubblico, può limitare cumulativamente le offerte e le spese. |
|  | Il posizionamento ha un basso tasso di vincita. | Aumenta il [!UICONTROL Max Bid] migliorare il tasso di vincita.<br><br><b>NOTA:</b> I prezzi di inventario possono variare in base al targeting del posizionamento.<br><br>Un tasso di vincita del 10% è considerato sano. |
|  | È disponibile un numero ridotto di scorte. | Esegui il targeting di altre o di tutte le origini di inventario, se possibile.<br><br>Tieni presente che l’utilizzo di più target di posizionamento, come filtri preofferta, geo, inventario e pubblico, può limitare cumulativamente le offerte e le spese. |
|  | Sono disponibili pochi utenti. | Verifica che le destinazioni di pubblico specificate includano un numero sufficiente di utenti attivi. In caso contrario, espandi i target aggiungendo altri tipi di pubblico.<br><br>Tieni presente che l’utilizzo di più target di posizionamento, come filtri preofferta, geo, inventario e pubblico, può limitare cumulativamente le offerte e le spese. |
|  | Il pacchetto include un gran numero di posizionamenti attivi. | Ridurre il numero di posizionamenti attivi all&#39;interno del pacchetto o aumentare il budget complessivo del pacchetto.<br><br>Se il pacchetto ha molti posizionamenti ma non abbastanza budget, DSP potrebbe non essere in grado di allocare abbastanza budget per ogni posizionamento. Ogni collocamento dovrebbe avere la possibilità di spendere almeno 2 USD al giorno. Ad esempio, se il tuo pacchetto ha un budget di 10 USD/giorno, è meglio includere cinque o meno posizionamenti. &#x200B; |

{style=&quot;table-layout:auto&quot;}

>[!MORELIKETHIS]
>
>* [Impostazioni di posizionamento](/help/dsp/campaign-management/placements/placement-settings.md)
>* [Impostazioni pacchetto](/help/dsp/campaign-management/packages/package-settings.md)
>* [Impostazioni di Campaign](/help/dsp/campaign-management/campaigns/campaign-settings.md)

