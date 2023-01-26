---
title: Impostazioni ID offerta manuale
description: Consulta le descrizioni delle impostazioni per gli ID offerta immessi manualmente.
feature: DSP Private Inventory, DSP Deal IDs
exl-id: 0cd5e9e8-2b13-4b1e-a2e0-b8b492f75acf
source-git-commit: 1c13874967ec4ad264e5fa6a5e0dfeb6120f53cc
workflow-type: tm+mt
source-wordcount: '520'
ht-degree: 0%

---

# Impostazioni ID offerta manuale

| Sezione | Parametro | Descrizione | Obbligatorio | Modificabile |
|---------|-----------|-------------|----------|----------|
| [Dettagli sulle offerte] | [!UICONTROL Deal name] | Nome per identificare il tuo [!UICONTROL Deal ID] nella DSP pubblicitaria. Immettere un nome o selezionare **[!UICONTROL Auto-name]** DSP generare un nome in base ai dettagli dell’offerta.<br><br>Esempio di nome generato automaticamente: `[!DNL 24159708 - Deal ID - Guaranteed Fixed - USD - 5 - 24Kitchen - Private]` | Sì | Sì |
|  | [!UICONTROL External deal ID] | L’ID utilizzato dall’editore e dalla SSP per identificare l’offerta. | Sì | No |
|  | [!UICONTROL Publisher] | Nome dell&#39;editore che vende l&#39;inventario. | Sì | No |
|  | [!UICONTROL SSP] | Piattaforma lato fornitura (SSP) attraverso la quale viene eseguito questo accordo. | Sì | No |
|  | [!UICONTROL Media type] | Il tipo di media acquistato tramite questa operazione: *[!UICONTROL Desktop video]*, *[!UICONTROL Mobile video]*, *[!UICONTROL Connected TV]*, *[!UICONTROL Display]* oppure *[!UICONTROL Audio]*. Le opzioni variano in base alla SSP.<br><br> Se l&#39;offerta consente più tipi di supporti, seleziona il tipo di supporto per il posizionamento predefinito quando crei l&#39;offerta. In seguito, puoi modificare il valore oppure [allegare un nuovo posizionamento con il tipo di supporto aggiuntivo](deal-id-attach-placements.md).<!-- It would be ideal if this field was multi-select rather than a radio button, so you don't have to "change" the value later. --> | Sì | No |
|  | [!UICONTROL Deal type] | L&#39;impegno dell&#39;accordo e la struttura dei prezzi:<br><ul><li>*[!UICONTROL Non guaranteed (floor)]*: Tu e l’editore non vi siete impegnati su un numero fisso di consegne di impression. L&#39;operazione specifica il prezzo minimo per l&#39;inventario, anche se il CPM può variare e aumentare a seconda delle condizioni di mercato.</li><li>*[!UICONTROL Non guaranteed (fixed)]*: Tu e l’editore non vi siete impegnati su un numero fisso di consegne di impression. I prezzi sono a tasso fisso negoziato.</li><li>*[!UICONTROL Guaranteed (fixed)]*: Tu ed l’editore avete concordato un numero predefinito di impression, targeting, date del volo e prezzo fisso.<br><br><b>Nota:</b> Le offerte garantite richiedono date di volo e un numero specifico di impression nel [!UICONTROL Tracking] sezione . È inoltre necessario creare un posizionamento programmatico predefinito garantito (PG) per l&#39;offerta e, facoltativamente, è possibile utilizzare l&#39;offerta per altri posizionamenti.</li></ul> | Sì | No |
|  | [!UICONTROL CPM] | Costo negoziato per 1000 impression (CPM). | Sì | Sì |
|  | [Valuta] | La valuta dell&#39;accordo.<br><br>Tutte le SSP accettano offerte in USD. Quando la SSP accetta la valuta per il tuo account DSP, è disponibile anche quella valuta. | Sì | No |
|  | [!UICONTROL Billing method] | Tutti gli ID offerta sono [!DNL Adobe]- finanziati e fatturati. DSP paga tutti i fornitori di supporti disponibili in base all&#39;utilizzo, gestisce le discrepanze con i fornitori e invia una fattura consolidata all&#39;account. Questa opzione comporta costi aggiuntivi come descritto nella scheda del conto. | Sì | No |
| [!UICONTROL Advertisers] | [!UICONTROL Account email] | L’indirizzo e-mail dell’account utente che può accedere all’offerta. | No | Sì |
|  | [!UICONTROL Advertisers that can access this deal] | Gli inserzionisti specifici dell&#39;account che possono accedere a questa offerta.<br><br><b>Nota:</b> Puoi condividere l’accordo con gli inserzionisti in account aggiuntivi da [!UICONTROL Deals] visualizza. Nella riga dell&#39;offerta, fai clic su **[!UICONTROL #]**, fai clic su **[!UICONTROL share]**, quindi condividi l’accordo con un indirizzo e-mail. | Sì | Sì |
| [!UICONTROL Tracking] | [!UICONTROL Flight Dates] | Le date di inizio e di fine del traffico che utilizzano questa offerta. Queste date sono solo a scopo di tracciamento e non influiscono sulla consegna degli annunci.<br><br><b>Suggerimento:</b> In [!UICONTROL Inventory] > [!UICONTROL Deals] visualizzazione [!UICONTROL Pacing & Budget] la colonna mostra il modo in cui l’accordo viene passato alla data di volo e all’obiettivo di impression specificati. Se la consegna è in ritardo o in eccesso, contatta l’editore per stabilire il volume che sta inviando tramite l’offerta. | Offerte garantite: Sì<br>Offerte non garantite: No | Sì |
|  | [!UICONTROL Impressions] | (Facoltativo per le offerte non garantite) Il numero stimato di impression che si prevede di eseguire utilizzando questa offerta. Questo valore è solo a scopo di tracciamento; l’editore controlla la consegna degli annunci. | Offerte garantite: Sì<br>Offerte non garantite: No | Sì |

{style=&quot;table-layout:auto&quot;}

>[!MORELIKETHIS]
>
>* [Creare manualmente i dettagli dell’ID offerta](deal-id-create.md)
>* [Partner SSP](ssp-partners.md)
>* [Informazioni su Inventario privato](private-inventory-about.md)

