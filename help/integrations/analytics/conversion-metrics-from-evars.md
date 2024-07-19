---
title: Creare metriche di conversione da Adobe Analytics [!DNL eVars] e prop
description: Configurare metriche evento di successo personalizzate utilizzando dati a livello di  [!DNL eVar] e  [!DNL prop].
feature: Integration with Adobe Analytics, Conversions
exl-id: 7717d10c-76ca-4ba9-9fbb-e34ad006619c
source-git-commit: a0d5bc1791f5d05e2cbdeab58e1943f4d494b53f
workflow-type: tm+mt
source-wordcount: '365'
ht-degree: 0%

---

# Creare metriche di conversione da Adobe Analytics [!DNL eVars] e [!DNL props]

*Inserzionisti con una sola integrazione Adobe Advertising-Adobe Analytics*

Puoi utilizzare le metriche degli eventi di successo per ottimizzare i pacchetti DSP e le campagne Search, Social e Commerce in base ai dati del sito Adobe Analytics che si adattano meglio agli obiettivi del tuo marchio. Puoi configurare metriche evento di successo personalizzate in base ai tuoi [[!DNL Analytics] [!DNL eVars]](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) e [[!DNL props]](https://experienceleague.adobe.com/docs/analytics/components/dimensions/prop.html) esistenti incanalando i dati a livello di [!DNL eVar] e [!DNL prop] in un evento. Altre metriche di [!DNL Analytics], incluse le metriche di conversione standard, personalizzate e riservate e le metriche del traffico, sono automaticamente disponibili in DSP e Search, Social e Commerce.

![Esempio di utilizzo](/help/integrations/assets/a4adc-conversion-evar-example.jpg "Esempio di utilizzo")

La maggior parte delle attività seguenti deve essere eseguita da un amministratore [!DNL Analytics] o da un altro utente. Se hai bisogno di assistenza, contatta (utenti DSP) il team del supporto tecnico DSP all&#39;indirizzo `adcloud_support@adobe.com` o (utenti Search, Social e Commerce) il tuo account team Adobe.

1. In [!DNL Analytics], [crea un evento di successo segnaposto](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/conversion-variables/success-events/success-event.html?lang=en).

   Utilizza i seguenti parametri aggiuntivi:

   **Tipo:** `Counter`

   **Polarità:** `Up is Good` o `Up is Bad`

   **Visibilità:** `Visible Everywhere`

   **Registrazione evento univoca:** `Always Record Event`

   **Partecipazione:** `Enabled`

   Non è necessario implementare il nuovo evento sul sito web del brand perché utilizza dati esistenti già acquisiti.

1. Creare e convalidare una regola di elaborazione in [!DNL Analytics]:

   >[!NOTE]
   >
   >Solo gli amministratori dell&#39;account [!DNL Analytics] possono creare regole di elaborazione a meno che non abbiano concesso l&#39;autorizzazione ai non amministratori.

   1. [Creare una regola di elaborazione](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/c-processing-rules/c-processing-rules-configuration/t-processing-rules.html?lang=en) utilizzando la configurazione seguente:

      * Per la condizione che deve essere soddisfatta, specificare [!DNL eVars] o [!DNL props] richiesti.

        Se necessario, puoi configurare ulteriori livelli di granularità per garantire la creazione degli eventi più precisi.

        >[!TIP]
        >
        >Si consiglia di utilizzare un solo [!DNL eVar] o [!DNL prop].

      * Per eseguire l&#39;azione, selezionare **Imposta evento** e selezionare l&#39;evento segnaposto.

   1. In [!DNL Analytics] [!DNL Analysis Workspace], [crea un progetto](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/home.html) e richiama il nuovo evento in una tabella a forma libera per garantire che i dati vengano popolati per la metrica [!DNL eVar] o [!DNL prop].

1. Contatta il team dell’account Adobe per sincronizzare la nuova metrica in Adobe Advertising.

Una volta che la metrica è disponibile, puoi utilizzarla per creare un obiettivo, che puoi quindi assegnare a un portfolio Search, Social e Commerce o utilizzare come [obiettivo personalizzato](/help/dsp/optimization/custom-goal.md) per un pacchetto DSP.

Per ulteriori informazioni sulla creazione degli obiettivi, consulta il capitolo della Guida all’ottimizzazione intitolato &quot;Obiettivi&quot;, disponibile in Search, Social &amp; Commerce.

>[!MORELIKETHIS]
>
>* [[!DNL Analytics] Dati in Adobe Advertising](/help/integrations/analytics/analytics-data-in-advertising.md)
>* [Visualizza le metriche di conversione rilevate per un inserzionista](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-view-tracked.md)
