---
title: Impostazioni ID offerta manuale
description: Consulta le descrizioni delle impostazioni per gli ID offerta immessi manualmente.
feature: DSP Private Inventory, DSP Deal IDs
exl-id: 9d3417cb-8b44-4f1c-afc4-eea6a2e5b9d7
source-git-commit: badf6a1d7059b9e7e261165b19e00f09573b9e53
workflow-type: tm+mt
source-wordcount: '518'
ht-degree: 0%

---

# Impostazioni ID offerta manuale

| Sezione | Parametro | Descrizione | Obbligatorio | Modificabile |
|---------|-----------|-------------|----------|----------|
| [Dettagli offerta] | [!UICONTROL Deal name] | Nome per identificare [!UICONTROL Deal ID] in Advertising DSP. Immettere un nome o selezionare **[!UICONTROL Auto-name]** per consentire a DSP di generare un nome in base ai dettagli dell&#39;offerta.<br><br>Esempio di nome generato automaticamente: `[!DNL 24159708 - Deal ID - Guaranteed Fixed - USD - 5 - 24Kitchen - Private]` | Sì | Sì |
| | [!UICONTROL External deal ID] | ID utilizzato dall&#39;editore e dal provider di servizi condivisi per identificare l&#39;operazione. | Sì | No |
| | [!UICONTROL Publisher] | Nome dell&#39;editore che sta vendendo questo inventario. | Sì | No |
| | [!UICONTROL SSP] | La piattaforma lato fornitura (SSP, Supply Side Platform) attraverso la quale viene eseguita l&#39;operazione. | Sì | No |
| | [!UICONTROL Media type] | Tipo di supporto acquistato tramite questa offerta: *[!UICONTROL Desktop video]*, *[!UICONTROL Mobile video]*, *[!UICONTROL Connected TV]*, *[!UICONTROL Display]*, *[!UICONTROL Audio]* o *[!UICONTROL Publisher Managed]*. Le opzioni variano in base alla SSP.<br><br> Se l&#39;offerta consente più tipi di file multimediali, selezionare il tipo di file multimediale per il posizionamento predefinito al momento della creazione dell&#39;offerta. In seguito, sarà possibile modificare il valore oppure solo [allegare un nuovo posizionamento con il tipo di supporto aggiuntivo](deal-id-attach-placements.md).<!-- It would be ideal if this field was multi-select rather than a radio button, so you don't have to "change" the value later. --> | Sì | No |
| | [!UICONTROL Deal type] | L&#39;impegno dell&#39;operazione e la struttura dei prezzi:<br><ul><li>*[!UICONTROL Non guaranteed (floor)]*: tu e l&#39;editore non avete eseguito il commit di un numero fisso di consegne di impression. L&#39;operazione specifica il prezzo minimo per l&#39;inventario, anche se il CPM può fluttuare e aumentare a seconda delle condizioni di mercato.</li><li>*[!UICONTROL Non guaranteed (fixed)]*: tu e l&#39;editore non avete eseguito il commit di un numero fisso di consegne di impression. La determinazione dei prezzi avviene a un tasso fisso negoziato.</li><li>*[!UICONTROL Guaranteed (fixed)]*: tu e l&#39;editore avete concordato un numero predefinito di impression, targeting, date di volo e prezzo fisso.<br><br><b>Nota:</b> le offerte garantite richiedono date di volo e un numero specificato di impression nella sezione [!UICONTROL Tracking]. Inoltre, devi creare un posizionamento programmatico garantito (PG) predefinito per l’offerta e, facoltativamente, puoi utilizzare l’offerta per altri posizionamenti.</li></ul> | Sì | No |
| | [!UICONTROL CPM] | Il costo negoziato per 1000 impression (CPM). | Sì | Sì |
| | [Valuta] | La valuta per l&#39;affare.<br><br>Tutti i provider di servizi condivisi accettano offerte in USD. Quando il provider di servizi condivisi accetta la valuta per il proprio conto DSP, è disponibile anche tale valuta. | Sì | No |
| | [!UICONTROL Billing method] | Tutti gli ID offerta sono finanziati e fatturati da [!DNL Adobe]. L&#39;DSP paga tutti i fornitori di supporti disponibili in base all&#39;utilizzo, gestisce le discrepanze con i fornitori e invia una fattura consolidata al conto. Questa opzione comporta costi aggiuntivi come indicato nella scheda tariffaria del conto. | Sì | No |
| [!UICONTROL Advertisers] | [!UICONTROL Account email] | L’indirizzo e-mail dell’account utente che può accedere all’offerta. | No | Sì |
| | [!UICONTROL Advertisers that can access this deal] | Gli inserzionisti specifici nell’account che possono accedere a questa offerta.<br><br><b>Nota:</b> è possibile condividere l&#39;offerta con gli inserzionisti in account aggiuntivi dalla visualizzazione [!UICONTROL Deals]. Nella riga dell&#39;offerta, fare clic su **[!UICONTROL #]**, fare clic su **[!UICONTROL share]** e quindi condividere l&#39;offerta con un indirizzo di posta elettronica. | Sì | Sì |
| [!UICONTROL Tracking] | [!UICONTROL Flight Dates] | Le date di inizio e fine del traffico che utilizza questa offerta. Queste date sono solo a scopo di tracciamento e non influiscono sulla consegna degli annunci.<br><br><b>Suggerimento:</b> Nella visualizzazione [!UICONTROL Inventory] > [!UICONTROL Deals], la colonna [!UICONTROL Pacing & Budget] mostra il ritmo dell&#39;offerta fino alla data di volo e all&#39;obiettivo di impression specificati. Se la consegna è al di sotto o al di sopra del ritmo, contatta l’editore per regolare il volume inviato tramite l’offerta. | Offerte garantite: Sì<br>Offerte non garantite: No | Sì |
| | [!UICONTROL Impressions] | (Facoltativo per offerte non garantite) Il numero stimato di impression che si prevede di eseguire utilizzando questa offerta. Questo valore è solo a scopo di tracciamento; l’editore controlla la consegna degli annunci. | Offerte garantite: Sì<br>Offerte non garantite: No | Sì |

{style="table-layout:auto"}

>[!MORELIKETHIS]
>
>* [Crea manualmente dettagli ID offerta](deal-id-create.md)
>* [Partner SSP](ssp-partners.md)
>* [Informazioni Sull&#39;Inventario Privato](private-inventory-about.md)
