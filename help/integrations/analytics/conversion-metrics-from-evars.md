---
title: Creare metriche di conversione da Adobe Analytics [!DNL eVars] e prop
description: Configurare metriche evento di successo personalizzate utilizzando dati a livello di  [!DNL eVar] e  [!DNL prop].
feature: Integration with Adobe Analytics, Conversions
exl-id: 7717d10c-76ca-4ba9-9fbb-e34ad006619c
TQID: https://experienceleague.adobe.com/DRwNcYJ4-tv6CWhaIHc-qZ-xNsM8sSqoSNkG8AaYI2c
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
  - id: f2860a4b-f905-4545-bead-1bbc92564592
subfeature_v2:
  - id: cfd751d4-ee56-4323-8fd1-dc174b031709
  - id: fddd8d8f-3ba1-4a22-b714-69d0e4655be8
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 352
ht-degree: 0%

---

# Creare metriche di conversione da Adobe Analytics [!DNL eVars] e [!DNL props]

*Inserzionisti con una sola integrazione Adobe Advertising-Adobe Analytics*

Puoi utilizzare le metriche degli eventi di successo per ottimizzare pacchetti DSP e campagne Search, Social e Commerce in base ai dati del sito Adobe Analytics che si adattano meglio agli obiettivi del tuo marchio. Puoi configurare metriche evento di successo personalizzate in base ai tuoi [[!DNL Analytics] [!DNL eVars]](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) e [[!DNL props]](https://experienceleague.adobe.com/docs/analytics/components/dimensions/prop.html) esistenti incanalando i dati a livello di [!DNL eVar] e [!DNL prop] in un evento. Altre metriche di [!DNL Analytics], incluse le metriche di conversione standard, personalizzate e riservate e le metriche del traffico, sono automaticamente disponibili in DSP e Search, Social e Commerce.

![Esempio di utilizzo](/help/integrations/assets/a4adc-conversion-evar-example.jpg "Esempio di utilizzo")

La maggior parte delle attività seguenti deve essere eseguita da un amministratore [!DNL Analytics] o da un altro utente. Se hai bisogno di assistenza, contatta il team del tuo account Adobe.

1. In [!DNL Analytics], [crea un evento di successo segnaposto](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/conversion-variables/success-event).

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

1. Contatta il team del tuo account Adobe per sincronizzare la nuova metrica in Adobe Advertising.

Una volta che la metrica è disponibile, puoi utilizzarla per creare un obiettivo, che puoi quindi assegnare a un portfolio Search, Social e Commerce o utilizzare come [obiettivo personalizzato](/help/dsp/optimization/custom-goal.md) per un pacchetto DSP.

Per ulteriori informazioni sulla creazione degli obiettivi, consulta il capitolo della Guida all’ottimizzazione intitolato &quot;Obiettivi&quot;, disponibile in Search, Social &amp; Commerce

>[!MORELIKETHIS]
>
>* [[!DNL Analytics] Dati in Adobe Advertising](/help/integrations/analytics/analytics-data-in-advertising.md)
>* [Visualizza le metriche di conversione rilevate per un inserzionista](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-view-tracked.md)
