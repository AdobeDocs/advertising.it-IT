---
title: Amministrazione utenti
description: Scopri come .
feature: Search Introduction
source-git-commit: 5a4c608d8c8371c24cf220cc5eed9a39989dc850
workflow-type: tm+mt
source-wordcount: '904'
ht-degree: 0%

---

# (Nuova interfaccia utente) Amministrazione utenti per Search, Social &amp; Commerce

Alcuni utenti possono gestire l’accesso alla nuova interfaccia utente di Search, Social e Commerce utilizzando Adobe Admin Console, che è la posizione centrale per la gestione di tutte le adesioni e la gestione degli utenti di Adobe. Gli utenti sono classificati come utenti finali o amministratori. Il team del tuo account Adobe ti invierà una notifica se sei un amministratore. Se sei un amministratore, consulta le sezioni seguenti per identificare le autorizzazioni e i flussi di lavoro per la gestione degli utenti.<!-- How can you see what your user role is, or will your Adobe Account Team tell you? -->

## Tipi di amministratori interessati

Admin Console offre diversi tipi di amministratori, ma solo i tipi e le autorizzazioni di amministratore seguenti sono rilevanti per Search, Social e Commerce.

**Amministratore di sistema:** utente privilegiato per l&#39;organizzazione. Un amministratore di sistema può eseguire tutte le attività amministrative in Admin Console per l’organizzazione e delegare le funzionalità amministrative ad altri utenti (amministratori di prodotto).&lt;!amministratori di profili di prodotto e di gruppi di utenti.  — Penso che PER NOI SIANO SOLO AMMINISTRATORI DI PRODOTTO?  Verifica. —>

**Amministratore prodotto:** gestisce l&#39;accesso a un prodotto [!DNL Adobe] specifico (ad esempio Search, Social e Commerce) e le autorizzazioni degli utenti a tale prodotto. Gli amministratori di prodotto possono creare profili di prodotto per il prodotto, creare (ma non rimuovere) utenti e gruppi di utenti, aggiungere o rimuovere utenti e gruppi di utenti dai profili di prodotto e aggiungere o rimuovere altri amministratori di prodotto dal prodotto.

<!--
**Product profile admin:** Manages assigned product profiles for individual products. A product profile admin can add (but not remove) users and user groups to the organization; add or remove users and user groups from product profiles; and assign or revoke permissions from product profiles. [I don't think this is applicable: and manage the product roles for product profiles.]

**User group admin:** Manages assigned user groups and their access rights. A user group admin can add or remove users from groups and add or remove user group admins from groups.
-->

## Profili di prodotto predefiniti

I profili di prodotto, simili ai ruoli, danno diritto agli utenti con servizi specifici per un prodotto specifico.

La nuova interfaccia utente di Search, Social &amp; Commerce dispone dei seguenti profili di prodotto predefiniti, che forniscono diversi sottoinsiemi di funzioni e servizi. Non puoi modificare o eliminare i profili di prodotto predefiniti. Tuttavia, se necessario, gli amministratori di sistema possono creare e gestire profili di prodotto aggiuntivi con diversi sottoinsiemi di autorizzazioni.

* **Ottimizzazione di base:** Questo profilo offre le funzionalità seguenti:

   * Obiettivi: accesso completo

   * Simulazioni: accesso completo

   * Portfolio Groups: accesso completo

   * Portfolio: consente di creare/modificare l&#39;accesso alle impostazioni del portfolio per Objective, Campaigns e Spend Management; l&#39;accesso in sola lettura alle restanti impostazioni del portfolio.

   * Campagne: accesso in sola lettura alle impostazioni della campagna (non sono disponibili funzioni di creazione, modifica o eliminazione); accesso completo alle assegnazioni di vincoli e portfolio<!-- Is that the correct wording? -->

   * Gruppi di annunci: accesso in sola lettura alle impostazioni dei gruppi di annunci (non sono disponibili funzioni di creazione, modifica o eliminazione); accesso completo alle assegnazioni di vincoli e portfolio<!-- Is that the correct wording? -->

  Questo livello di accesso è preferito per gli utenti che stanno ancora imparando a utilizzare Search, Social e Commerce.

* **Ottimizzazione avanzata:** Questo profilo offre le funzionalità seguenti:

   * Obiettivi: accesso completo

   * Simulazioni: accesso completo

   * Portfolio Groups: accesso completo

   * Portfolio: accesso completo

   * Campagne: accesso in sola lettura all&#39;elenco delle campagne (non sono ancora disponibili le funzioni di creazione, modifica o eliminazione della campagna); accesso completo alle assegnazioni di vincoli e portfolio<!-- Is that the correct wording? -->

   * Gruppi di annunci: accesso in sola lettura all&#39;elenco dei gruppi di annunci (non sono ancora disponibili funzioni di creazione, modifica o eliminazione di campagne); accesso completo alle assegnazioni di vincoli e portfolio<!-- Is that the correct wording? -->

  Questo livello di accesso è consigliato agli utenti esperti di Search, Social e Commerce.

* **Sola lettura:** Questo profilo offre le funzionalità seguenti:

   * Obiettivi: accesso in sola lettura

   * Simulazioni: accesso in sola lettura

   * Portfolio Groups: accesso in sola lettura

   * Portfolio: accesso in sola lettura

   * Campagne: accesso in sola lettura

   * Ad Groups: accesso in sola lettura

* **Amministratore:** questo profilo consente l&#39;accesso completo a tutte le funzionalità disponibili e consente agli utenti di creare nuove istanze client. Non assegnare questo diritto a nessuno a meno che tu non abbia una valida giustificazione commerciale.

<!-- Do I need to include this? If so, adjust wording as needed

## Product-specific instances

 -->

## Attività per amministratori

### Accedi a Adobe Admin Console e aprilo in Search, Social e Commerce

>[!PREREQUISITES]
>
>Devi disporre dell&#39;accesso come amministratore&lt;!— di che tipo? Amministratore del prodotto, amministratore di sistema, ma sono sicuro che anche amministratore del profilo di prodotto o amministratore del gruppo di utenti (che potrebbe essere un gruppo interno — segno di spunta) —> a Search, Social, &amp; Commerce.

1. Vai su https://adminconsole.adobe.com/enterprise/.

1. (Se non hai effettuato l’accesso ad Experience Cloud) Accedi ad Experience Cloud:

   1. Immetti l&#39;ID [!DNL Adobe] e fai clic su **[!UICONTROL Continue]**.

   1. Selezionare **[!UICONTROL Personal Account]&quot; o &#x200B;** [!UICONTROL Company or School Account]**.<!-- Will it necessarily be "Company or School Account?" -->

   1. Seleziona l’organizzazione Experience Cloud applicabile.

   1. In Prodotti e servizi fare clic su &quot;[!UICONTROL Adobe Advertising, Search, Social, & Commerce — Org Name]&quot;.

   Per impostazione predefinita, la pagina prodotto viene aperta nella scheda [!UICONTROL Product profiles] per Ricerca, Social e Commerce. Schede aggiuntive includono [!UICONTROL Users] e [!UICONTROL Product Admins].

### Flusso di lavoro per gli amministratori di sistema

1. [Accedi a Adobe Admin Console e aprilo in Search, Social e Commerce](#open-admin-console).

1. Delega la gestione di prodotti e utenti [aggiungendo amministratori di prodotti](https://helpx.adobe.com/it/enterprise/using/admin-roles.html#enterprise).

<!-- what else? -->

### Flusso di lavoro per gli amministratori di prodotto

1. [Accedi a Adobe Admin Console e aprilo in Search, Social e Commerce](#open-admin-console).

1. Se necessario, creare gli utenti finali [singolarmente](https://helpx.adobe.com/it/enterprise/using/manage-users-individually.html) o [in blocco](https://helpx.adobe.com/it/enterprise/using/bulk-upload-users.html).

1. (Facoltativo) Crea [gruppi di utenti](https://helpx.adobe.com/it/enterprise/using/user-groups.html) per ogni istanza di prodotto e assegna gli utenti a ciascun gruppo di utenti.

   Se l’istanza ha molti utenti, crea gruppi di utenti per garantire che agli utenti siano assegnati i profili giusti in base al loro livello di esperienza. Consulta il Passaggio 4 per assegnare gruppi di utenti ai profili di prodotto. Puoi creare gruppi di utenti in base alla linea di business, alle esigenze di accesso degli utenti, alla data di assunzione dell’utente o ad altri criteri.

   >[!IMPORTANT]
   >
   >I nomi dei gruppi di utenti devono comunicare chiaramente i diritti che devono essere assegnati al gruppo. Ad esempio, se si desidera creare un gruppo di utenti con diritti di sola lettura, includere &quot;Sola lettura&quot; nel nome del gruppo di utenti, ad esempio &quot;Acme_Uk_ReadOnly&quot; o &quot;Acme_ReadOnly&quot;.

1. (Facoltativo) [Crea profili di prodotto personalizzati](https://helpx.adobe.com/it/enterprise/using/manage-product-profiles.html) con set di autorizzazioni definiti.

   I profili personalizzati si aggiungono ai quattro profili di prodotto predefiniti già disponibili.

   Ogni profilo di prodotto di un’organizzazione deve avere un nome univoco. Se la tua organizzazione utilizza più istanze Search, Social e Commerce (ad esempio, Acme_US e Acme_JP), non puoi duplicare il nome di un profilo di prodotto in più istanze. **Best practice:** utilizza la convenzione di denominazione `<Name>_<Instance>,`, ad esempio &quot;Simulation_Only_JP&quot;.

1. [Assegnare ogni utente o gruppo di utenti al relativo profilo di prodotto](https://helpx.adobe.com/it/enterprise/using/manage-product-profiles.html) manualmente o in blocco.

## Guida completa all’amministrazione degli utenti e collegamenti aggiuntivi

* Per ulteriori informazioni sull&#39;amministrazione degli utenti tramite Adobe Admin Console, vedere &quot;[Adobe Enterprise &amp; Teams Administration Guide](https://helpx.adobe.com/it/enterprise/admin-guide.html)&quot;, inclusa la [panoramica di Admin Console](https://helpx.adobe.com/it/enterprise/using/admin-console.html).

* Admin Console: [https://adminconsole.adobe.com](https://adminconsole.adobe.com)
