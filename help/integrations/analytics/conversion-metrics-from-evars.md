---
title: "Creare metriche di conversione da Adobe Analytics [!DNL eVars] e prop"
description: "Configurare metriche evento di successo personalizzate con [!DNL eVar]- e [!DNL prop]dati a livello di."
feature: Integration with Adobe Analytics, Conversions
source-git-commit: f6f3e0b3cc867b817ce40c7ba06c76885948edbe
workflow-type: tm+mt
source-wordcount: '397'
ht-degree: 0%

---

# Creare metriche di conversione da Adobe Analytics [!DNL eVars] e [!DNL props]

*Per gli inserzionisti con una sola integrazione Adobi Advertising-Adobe Analytics*

Puoi utilizzare le metriche degli eventi di successo per ottimizzare i pacchetti DSP e le campagne Search, Social e Commerce in base ai dati del sito Adobe Analytics che si adattano meglio agli obiettivi del tuo marchio. Puoi configurare metriche evento di successo personalizzate in base a [esistente [!DNL Analytics] [!DNL eVars]](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) e [[!DNL props]](https://experienceleague.adobe.com/docs/analytics/components/dimensions/prop.html) mediante incanalamento [!DNL eVar]- e [!DNL prop]dati a livello di in un evento. Altro [!DNL Analytics] Le metriche di, comprese quelle di conversione standard, personalizzate e riservate e quelle sul traffico, sono automaticamente disponibili in DSP e in Search, Social e Commerce.

![Esempio di utilizzo](/help/integrations/assets/a4adc-conversion-evar-example.jpg "Esempio di utilizzo")

La maggior parte delle seguenti attività deve essere eseguita da un [!DNL Analytics] amministratore o un altro utente. Se hai bisogno di assistenza, contatta (utenti DSP) il team di supporto tecnico DSP all’indirizzo `adcloud_support@adobe.com` o (utenti di Search, Social e Commerce) il team del tuo account Adobe.

1. In entrata [!DNL Analytics], [creare un evento di successo segnaposto](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/conversion-variables/success-events/success-event.html?lang=en).

   Utilizza i seguenti parametri aggiuntivi:

   **Tipo:** `Counter`

   **Polarità:**  o `Up is Good` o `Up is Bad`

   **Visibilità:** `Visible Everywhere`

   **Registrazione di eventi univoci:** `Always Record Event`

   **Partecipazione:** `Enabled`

   Non è necessario implementare il nuovo evento sul sito web del brand perché utilizza dati esistenti già acquisiti.

1. Creare una regola di elaborazione in [!DNL Analytics]:

   >[!NOTE]
   >
   >Solo [!DNL Analytics] gli amministratori degli account possono creare regole di elaborazione a meno che non abbiano concesso l’autorizzazione agli utenti non amministratori.

   1. [Creare una regola di elaborazione](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/c-processing-rules/c-processing-rules-configuration/t-processing-rules.html?lang=en), utilizzando la seguente configurazione:

      * Per la condizione che deve essere soddisfatta, specifica la [!DNL eVars] o [!DNL props].

        Se necessario, puoi configurare ulteriori livelli di granularità per garantire la creazione degli eventi più precisi.

        >[!TIP]
        >
        >La best practice prevede di utilizzarne solo uno [!DNL eVar] o [!DNL prop].

      * Per eseguire l’azione, seleziona **Imposta evento** e seleziona l’evento segnaposto.

   1. In entrata [!DNL Analytics] [!DNL Analysis Workspace], [creare un progetto](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/home.html) e richiama il nuovo evento in una tabella a forma libera per garantire che i dati vengano compilati per il [!DNL eVar] o [!DNL prop] metrica.

1. Contatta il team dell’account Adobe per sincronizzare la nuova metrica in Adobi Advertising.

Una volta che la metrica è disponibile, può utilizzarla per creare un obiettivo, che puoi quindi assegnare a un portfolio Search, Social &amp; Commerce o utilizzare come [obiettivo personalizzato](/help/dsp/optimization/custom-goal-about.md) per un pacchetto DSP.

Per ulteriori informazioni sulla creazione degli obiettivi, consulta il capitolo &quot;Objectives&quot; della Guida all’ottimizzazione, disponibile in Search, Social &amp; Commerce.

>[!MORELIKETHIS]
>
>* [[!DNL Analytics] Dati in Adobe Advertising](/help/integrations/analytics/analytics-data-in-advertising.md)
<!--
>* [](/help/search-social-commerce/admin/conversion-metrics/ ????????)
-->