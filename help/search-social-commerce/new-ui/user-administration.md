---
title: (Nuova interfaccia) Amministrazione utenti
description: Scopri come gestire l’accesso degli utenti.
feature: Search Introduction
source-git-commit: c198b5ea2f8ef125b1a5d25616158d57950ce3b0
workflow-type: tm+mt
source-wordcount: '975'
ht-degree: 0%

---

# (Nuova interfaccia utente) Amministrazione utenti per Search, Social &amp; Commerce

Alcuni utenti possono gestire l&#39;accesso alla nuova interfaccia utente di Search, Social e Commerce utilizzando [Adobe Admin Console](https://helpx.adobe.com/it/enterprise/using/admin-console.html), che è la posizione centrale per la gestione di tutte le adesioni e la gestione degli utenti di Adobe. Gli utenti sono classificati come utenti finali o amministratori. Il team del tuo account Adobe ti invierà una notifica se sei un amministratore. Se sei un amministratore, consulta le sezioni seguenti per identificare le autorizzazioni e i flussi di lavoro per la gestione degli utenti.

## Tipi di amministratori

Admin Console fornisce diversi tipi di amministratori. Per Search, Social e Commerce sono necessari i tipi di amministratore e le autorizzazioni seguenti. È possibile aggiungere altri tipi se si desidera delegare le attività di gestione utenti.

**Amministratore di sistema:** utente privilegiato che gestisce tutti i prodotti per l&#39;organizzazione, incluse tutte le istanze client per l&#39;organizzazione. (Le istanze client sono le stesse degli account inserzionisti legacy, con una o più istanze per ID organizzazione). Un amministratore di sistema può eseguire tutte le attività amministrative in Admin Console per l’organizzazione e delegare le funzionalità amministrative ad altri utenti per qualsiasi prodotto dell’organizzazione.

**Amministratore prodotto:** gestisce l&#39;accesso a un prodotto [!DNL Adobe] specifico (ad esempio Search, Social e Commerce) e le adesioni utente a tale prodotto. Gli amministratori di prodotto possono creare profili di prodotto per il prodotto, creare (ma non rimuovere) utenti e gruppi di utenti per il prodotto, aggiungere o rimuovere utenti e gruppi di utenti dai profili di prodotto e aggiungere o rimuovere altri amministratori di prodotto dal prodotto.

<!--
**Product profile admin:** Manages assigned product profiles for individual products. A product profile admin can add (but not remove) users and user groups to the organization; add or remove users and user groups from product profiles; and assign or revoke permissions from product profiles. [I don't think this is applicable: and manage the product roles for product profiles.]

**User group admin:** Manages assigned user groups and their access rights. A user group admin can add or remove users from groups and add or remove user group admins from groups.
-->

## Profili di prodotto predefiniti

I profili di prodotto, simili ai ruoli, danno diritto agli utenti con servizi specifici per un prodotto specifico.

La nuova interfaccia utente di Search, Social &amp; Commerce dispone dei seguenti profili di prodotto predefiniti, che forniscono diversi sottoinsiemi di funzioni e servizi. Non puoi modificare le autorizzazioni prodotto per i profili di prodotto predefiniti né eliminare i profili di prodotto predefiniti. Tuttavia, se necessario, gli amministratori di prodotto, gli amministratori dei profili di prodotto e gli amministratori di sistema possono creare e gestire profili di prodotto aggiuntivi con diversi sottoinsiemi di autorizzazioni disponibili.

* **[!UICONTROL Basic Optimization]:** Questo profilo fornisce le funzionalità seguenti:

   * [!UICONTROL Objectives]: Accesso completo

   * [!UICONTROL Simulations]: Accesso completo

   * [!UICONTROL Portfolio Groups]: Accesso completo

   * [!UICONTROL Portfolios]: crea/modifica l&#39;accesso alle impostazioni del portfolio per [!UICONTROL Objectives], [!UICONTROL Campaigns] e Spesa [!UICONTROL Management]; accesso in sola lettura alle impostazioni del portfolio rimanenti.

   * [!UICONTROL Campaigns]: accesso in sola lettura alle impostazioni della campagna (non sono disponibili funzioni di creazione, modifica o eliminazione); accesso completo alle assegnazioni di vincoli e portfolio

   * [!UICONTROL Ad Groups]: accesso in sola lettura alle impostazioni dei gruppi di annunci (non sono disponibili funzioni di creazione, modifica o eliminazione); accesso completo alle assegnazioni di vincoli e portfolio

  Questo livello di accesso è preferito per gli utenti che stanno ancora imparando a utilizzare Search, Social e Commerce.

* **[!UICONTROL Expert Optimization]:** Questo profilo fornisce le funzionalità seguenti:

   * [!UICONTROL Objectives]: Accesso completo

   * [!UICONTROL Simulations]: Accesso completo

   * [!UICONTROL Portfolio Groups]: Accesso completo

   * [!UICONTROL Portfolios]: Accesso completo

   * [!UICONTROL Campaigns]: accesso in sola lettura all&#39;elenco delle campagne (non sono ancora disponibili le funzioni di creazione, modifica o eliminazione della campagna); accesso completo alle assegnazioni di vincoli e portfolio

   * [!UICONTROL Ad Groups]: accesso in sola lettura all&#39;elenco dei gruppi di annunci (non sono ancora disponibili le funzioni di creazione, modifica o eliminazione della campagna); accesso completo alle assegnazioni di vincoli e portfolio

  Questo livello di accesso è consigliato agli utenti esperti di Search, Social e Commerce.

* **[!UICONTROL Read-Only]:** Questo profilo fornisce le funzionalità seguenti:

   * [!UICONTROL Objectives]: accesso in sola lettura

   * [!UICONTROL Simulations]: accesso in sola lettura

   * [!UICONTROL Portfolio Groups]: accesso in sola lettura

   * [!UICONTROL Portfolios]: accesso in sola lettura

   * [!UICONTROL Campaigns]: accesso in sola lettura

   * [!UICONTROL Ad Groups]: accesso in sola lettura

* **[!UICONTROL Admin]:** Questo profilo concede l&#39;accesso completo a tutte le funzionalità disponibili e consente agli utenti di creare nuove istanze client (come gli account degli inserzionisti legacy, con una o più istanze per ID organizzazione). Non assegnare questo diritto a nessuno a meno che tu non abbia una valida giustificazione commerciale.

## Attività per amministratori

### Accedi a Adobe Admin Console e aprilo in Search, Social e Commerce

>[!PREREQUISITES]
>
>Per accedere a Admin Console è necessario disporre di un tipo di accesso amministratore a Search, Social e Commerce.

1. Vai su https://adminconsole.adobe.com/enterprise/.

1. (Se non hai effettuato l’accesso ad Experience Cloud) Accedi ad Experience Cloud:

   1. Immetti l&#39;ID [!DNL Adobe] e fai clic su **[!UICONTROL Continue]**.

   1. Selezionare **[!UICONTROL Personal Account]&quot; o &#x200B;** [!UICONTROL Company or School Account]**.<!-- Will it necessarily be "Company or School Account?" -->

   1. Seleziona l’organizzazione Experience Cloud applicabile.

      Admin Console si apre sulla scheda [!UICONTROL Overview].

   1. In [!UICONTROL Product & services], fare clic su &quot;[!UICONTROL Adobe Advertising, Search, Social, & Commerce — Org Name]&quot;.

      La pagina del prodotto si apre sulla scheda [!UICONTROL Product profiles] per Ricerca, Social e Commerce. Schede aggiuntive includono [!UICONTROL Users] e [!UICONTROL Product Admins].

### Flusso di lavoro per gli amministratori di sistema

Segui questo flusso di lavoro per ogni istanza client di Search, Social e Commerce.

1. [Accedi a Adobe Admin Console e aprilo in Search, Social e Commerce](#open-admin-console).

1. (Facoltativo) [Aggiungere un altro amministratore di sistema](https://helpx.adobe.com/enterprise/using/admin-roles.html#enterprise) come backup.

1. Delega la gestione di prodotti e utenti [aggiungendo amministratori di prodotti](https://helpx.adobe.com/enterprise/using/admin-roles.html#enterprise).

### Flusso di lavoro per gli amministratori di prodotto

Segui questo flusso di lavoro per ogni istanza client di Search, Social e Commerce.

1. [Accedi a Adobe Admin Console e aprilo in Search, Social e Commerce](#open-admin-console).

1. Se necessario, creare gli utenti finali [singolarmente](https://helpx.adobe.com/enterprise/using/manage-users-individually.html) o [in blocco](https://helpx.adobe.com/enterprise/using/bulk-upload-users.html).

1. (Facoltativo) Crea [gruppi di utenti](https://helpx.adobe.com/enterprise/using/user-groups.html) per l&#39;istanza e assegna gli utenti a ciascun gruppo di utenti.

   Se l’istanza ha molti utenti, crea gruppi di utenti per garantire che agli utenti siano assegnati i profili giusti in base al loro livello di esperienza. Consulta il Passaggio 4 per assegnare gruppi di utenti ai profili di prodotto. Puoi creare gruppi di utenti in base alla linea di business, alle esigenze di accesso degli utenti, alla data di assunzione dell’utente o ad altri criteri.

   >[!IMPORTANT]
   >
   >I nomi dei gruppi di utenti devono comunicare chiaramente i diritti che devono essere assegnati al gruppo. Ad esempio, se si desidera creare un gruppo di utenti con diritti di sola lettura, includere &quot;Sola lettura&quot; nel nome del gruppo di utenti, ad esempio &quot;Acme_Uk_ReadOnly&quot; o &quot;Acme_ReadOnly&quot;.

1. (Facoltativo) [Crea profili di prodotto personalizzati](https://helpx.adobe.com/enterprise/using/manage-product-profiles.html) con set di autorizzazioni definiti.

   I profili personalizzati si aggiungono ai quattro profili di prodotto predefiniti già disponibili.

   Ogni profilo di prodotto di un’organizzazione deve avere un nome univoco. Se la tua organizzazione utilizza più istanze Search, Social e Commerce (ad esempio, Acme_US e Acme_JP), non puoi duplicare il nome di un profilo di prodotto in più istanze. **Best practice:** utilizza la convenzione di denominazione `<Name>_<Instance>,`, ad esempio &quot;Simulation_Only_JP&quot;.

   **Attenzione:** le autorizzazioni del prodotto sono molto granulari. Presta attenzione quando configuri profili di prodotto personalizzati o potresti omettere le funzionalità che desideri includere.

1. [Assegnare ogni utente o gruppo di utenti al relativo profilo di prodotto](https://helpx.adobe.com/enterprise/using/manage-product-profiles.html) manualmente o in blocco.

## Guida completa all’amministrazione degli utenti e collegamenti aggiuntivi

* Per ulteriori informazioni sull&#39;amministrazione degli utenti tramite Adobe Admin Console, vedere &quot;[Adobe Enterprise &amp; Teams Administration Guide](https://helpx.adobe.com/enterprise/admin-guide.html)&quot;, inclusa la [panoramica di Admin Console](https://helpx.adobe.com/it/enterprise/using/admin-console.html).

* Admin Console: [https://adminconsole.adobe.com](https://adminconsole.adobe.com)
