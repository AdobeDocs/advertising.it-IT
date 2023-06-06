---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 0%

---
# Campo Tipo di tracciamento nelle impostazioni dell’account e della campagna

**[!UICONTROL Tracking Type]:** Metodo di generazione degli URL:

* *[!UICONTROL EF Redirect]* (impostazione predefinita): per i clienti che desiderano utilizzare il servizio di tracciamento delle conversioni di Adobe Advertising. Questo metodo genera ID univoci di tracciamento dei clic e reindirizza gli utenti al server Adobe Advertising a scopo di tracciamento prima di inviarli alla pagina di destinazione del cliente.

   Questo metodo dispone di opzioni di tracciamento predefinite che puoi personalizzare facoltativamente e che puoi anche specificare parametri da aggiungere a ogni URL.

* *[!UICONTROL No EF Redirect]:* Per i clienti che desiderano utilizzare solo i propri codici di tracciamento dei clic. Search, Social e Commerce non forniscono ID di tracciamento dei clic o codici di reindirizzamento. Per gli account con URL di destinazione, ogni URL di destinazione è uguale all’URL di base.

   **Note:**

   * Questo valore può essere modificato solo dagli utenti con privilegi di account manager di agenzia, account manager di Adobe e amministratore.
   * Se modifichi il metodo di tracciamento, devi rigenerare gli URL di tracciamento per l’account.
   * Le opzioni di tracciamento a livello di campagna sostituiscono le impostazioni a livello di account.
