---
title: Best practice per la creazione di un obiettivo personalizzato
description: Scopri le best practice per la creazione di obiettivi personalizzati per definire gli eventi di successo.
feature: DSP Optimization, DSP Best Practices
exl-id: 8b1247cd-083d-4c8c-8588-9e8c03c4cc67
source-git-commit: 6aa81fe4fd5ea6cb188b7f18b1574c26ddfcbb92
workflow-type: tm+mt
source-wordcount: '604'
ht-degree: 0%

---

# Best practice per la creazione di un obiettivo personalizzato

## Obiettivi personalizzati con una singola proprietà

Gli esempi seguenti mostrano come configurare obiettivi per il targeting di una singola metrica di conversione.

### Esempio di una campagna con &quot;[!UICONTROL Highest Return on Ad Spend (ROAS)]&quot; Obiettivo di ottimizzazione

Se l&#39;obiettivo della campagna è il profitto ([!UICONTROL Highest Return on Ad Spend (ROAS)]), l’obiettivo personalizzato (obiettivo) includerà la &quot;[!UICONTROL Revenue]&quot;metrica con un peso di uno (1).

![esempio di obiettivo personalizzato ROAS con una singola metrica di conversione](/help/dsp/assets/custom-goal-roas.png)

>[!NOTE]
>
> A [!UICONTROL Property Weight] di uno equivale a un valore di uno per ogni $ 1 di ricavo tracciato.
>
> Ad esempio, una conversione da 250 $ con un peso di uno viene segnalata come 250 $. Se alla metrica di conversione viene assegnato un peso di 0,5, la conversione di 250 $ viene segnalata come Adobe Advertising di 125 $ ($250 Conversione * 0,5 [!UICONTROL Property Weight] = $125).

### Esempio di una campagna con &quot;[!UICONTROL Lowest Cost per Acquisition (CPA)]&quot; Obiettivo di ottimizzazione

Se l’obiettivo della campagna è il costo più basso per acquisizione (CPA) e richiede un solo evento di successo, includerai tale metrica (nell’esempio seguente, &quot;Invio applicazione&quot;). La best practice prevede di impostare il peso come uno (1).

![esempio di obiettivo personalizzato CPA con una singola metrica di conversione](/help/dsp/assets/custom-goal-roas.png)

>[!NOTE]
>
> A [!UICONTROL Property Weight] di uno equivale a un valore di uno per ogni conversione tracciata.
>
> Ad esempio, se vengono tracciate 10 conversioni di invio di applicazioni, vengono segnalate 10 conversioni di invio di applicazioni.  Se alla metrica di conversione viene assegnato un peso di 0,5, allora le 10 conversioni sono segnalate come cinque (5) in Adobe Advertising (10 conversioni * 0,5 [!UICONTROL Property Weight] = 5).

## Obiettivi personalizzati con più proprietà

Esistono due scenari in cui puoi utilizzare più proprietà in un obiettivo personalizzato:

* L’obiettivo della campagna prevede più eventi di successo. Ad esempio, puoi fare pubblicità a più di un’azione nel sito attribuendole tutte all’obiettivo CPA. L’obiettivo dell’esempio seguente include tre proprietà separate (Download PDF, Contattaci e Iscrizione e-mail), ciascuna con un peso di uno (1), che indica al [!DNL Adobe Sensei] algoritmo in base al quale ciascuna proprietà ha la stessa importanza. Se includi proprietà con costi o importanza variabili, puoi adeguare di conseguenza i loro pesi relativi.

  ![esempio di obiettivo personalizzato con più proprietà](/help/dsp/assets/custom-goal-multiple-properties.png)

* La singola metrica di conversione nell’obiettivo personalizzato non raggiunge il minimo di 10 conversioni al giorno necessarie per prestazioni ottimizzate. Ciò può verificarsi a causa di una spesa minima giornaliera per i pacchetti o di un numero limitato di conversioni naturali. L’aggiunta di proprietà di supporto aggiuntive all’obiettivo personalizzato può aiutarti a raggiungere la soglia di 10 conversioni al giorno. Dieci eventi di supporto possono aiutare un pacchetto a raggiungere la soglia di 10/die, anche quando ciascuno dei loro pesi è inferiore a uno (1). Ma potresti non aver bisogno di aggiungere tanti eventi.

  Quando aggiungi proprietà di supporto a un obiettivo personalizzato, ponderale in base alla loro importanza relativa per l’evento di successo principale e tieni presente la quantità di punti dati. Questo consente all’algoritmo Adobe Sensei di bilanciare più proprietà e ottimizzarle per il raggiungimento dell’obiettivo.

  L&#39;obiettivo di esempio seguente include tre proprietà, ciascuna con un peso diverso: Invio applicazione = 1, Inizio applicazione = 0,1 e Pagina di destinazione inserzionista = 0,01. Ciò significa che ogni conversione Invio applicazione ha lo stesso valore per la tua azienda come media di 10 conversioni di Avvio applicazione e 100 conversioni di Pagina di destinazione inserzionista.

  ![esempio di obiettivo personalizzato con più proprietà](/help/dsp/assets/custom-goal-multiple-properties2.png)

  Se, invece, le visite della pagina di destinazione venissero ponderate allo stesso modo degli invii di applicazioni, la quantità naturalmente maggiore di visite alla pagina di destinazione potrebbe sopraffare l’obiettivo e distorcere le visite alla pagina di destinazione.<!--reword-->

>[!MORELIKETHIS]
>
>* [Informazioni sugli obiettivi personalizzati](custom-goal-about.md)
>* [Creare un obiettivo personalizzato](custom-goal-create.md)
>* [Obiettivi di ottimizzazione e modalità di utilizzo](optimization-goals.md)
>* [Impostazioni pacchetto](/help/dsp/campaign-management/packages/package-settings.md)
> * [Come l’DSP ottimizza le campagne](optimization-how-dsp-optimizes-campaigns.md)
