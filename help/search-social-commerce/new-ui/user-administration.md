---
title: (Nuova interfaccia) Amministrazione utenti
description: Scopri come gestire l’accesso degli utenti.
feature: Search Introduction
exl-id: bfc43692-cfb6-468f-90df-a808a21a0c23
TQID: 'https://experienceleague.adobe.com/b28N5zmqqdZ6Yvg2swGLWv260fWsMUgjK2eW1DDn-uo'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9c0e1d04187ee5f80d4b5899ab36833f202b16a
workflow-type: tm+mt
source-wordcount: 1082
ht-degree: 0%

---

# (Nuova interfaccia utente) Amministrazione utenti per Search, Social &amp; Commerce

Alcuni utenti possono gestire l&#39;accesso alla nuova interfaccia utente di Search, Social e Commerce utilizzando [Adobe Admin Console](https://helpx.adobe.com/it/enterprise/using/admin-console.html), che è la posizione centrale per la gestione di tutte le adesioni e la gestione degli utenti di Adobe. Gli utenti sono classificati come utenti finali o amministratori. Il team del tuo account Adobe ti avvisa se sei un amministratore. Se sei un amministratore, consulta le sezioni seguenti per identificare le autorizzazioni e i flussi di lavoro per la gestione degli utenti.

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

* **[!UICONTROL Basic Optimization]:** Per gli utenti che necessitano di funzionalità standard di gestione portfolio e pianificazione con accesso alle impostazioni di base.

* **[!UICONTROL Expert Optimization]:** Per utenti esperti che necessitano di un accesso completo alle impostazioni del portfolio, inclusi controlli avanzati a livello di esperti. Include tutte le autorizzazioni relative alla pianificazione delle prestazioni, agli obiettivi, alla campagna, alla configurazione e alla gestione dei rapporti.

* **[!UICONTROL Read-Only Optimization]:** Per gli utenti che necessitano di visibilità in portfolio, simulazioni e campagne senza alcuna funzionalità di modifica o creazione.

* **[!UICONTROL \[Optimization\] Admin]:** concede l&#39;accesso completo a tutte le funzionalità disponibili e consente agli utenti di creare nuove istanze client (come gli account degli inserzionisti legacy, con una o più istanze per ID organizzazione). Non assegnare questo diritto a nessuno a meno che tu non abbia una valida giustificazione commerciale.

### Funzionalità per profilo di prodotto

<!-- These don't correspond exactly to the GUI menu -->

Un segno di spunta (✓) indica che l&#39;autorizzazione è inclusa nel profilo di prodotto.

**Gestione Portfolio**

| Autorizzazione | Base | Esperto | Sola lettura | Amministratore |
|---|---|---|---|---|
| Visualizza portfolio | ✓ | ✓ | ✓ | ✓ |
| Visualizza impostazioni Portfolio | ✓ | ✓ | ✓ | ✓ |
| Visualizza dettagli sulle prestazioni di Portfolio | ✓ | ✓ | ✓ | ✓ |
| Visualizza gruppi Portfolio | ✓ | ✓ | ✓ | ✓ |
| Modifica gruppi Portfolio | ✓ | ✓ | | ✓ |
| Modifica impostazioni Portfolio di base | ✓ | | | |
| Modifica impostazioni Expert Portfolio | | ✓ | | ✓ |

<!--
Noone has permissions as of 6/1; spelling [sic]:
| Edit Advance Portfolio Settings | | | | |
-->

**Gestione Performance Planning**

| Autorizzazione | Base | Esperto | Sola lettura | Amministratore |
|---|---|---|---|---|
| Visualizza simulazione | ✓ | ✓ | ✓ | ✓ |
| Crea simulazione | ✓ | ✓ | | ✓ |
| Visualizza consigli di spesa | | ✓ | | ✓ |
| Applica consigli di spesa | | ✓ | | ✓ |

**Gestione obiettivo**

| Autorizzazione | Base | Esperto | Sola lettura | Amministratore |
|---|---|---|---|---|
| Visualizza obiettivo | ✓ | ✓ | ✓ | ✓ |
| Modifica obiettivo | ✓ | ✓ | | ✓ |
| Visualizza regole valore di conversione | ✓ | ✓ | ✓ | ✓ |
| Modifica regole valore di conversione | | ✓ | | ✓ |
| Visualizza conversioni | | ✓ | | ✓ |
| Modifica conversioni | | ✓ | | ✓ |
| Visualizza visibilità conversioni | | ✓ | | ✓ |

**Gestione campagne**

| Autorizzazione | Base | Esperto | Sola lettura | Amministratore |
|---|---|---|---|---|
| Visualizza campagne | ✓ | ✓ | ✓ | ✓ |
| Modifica campagne | ✓ | ✓ | | ✓ |
| Visualizza gruppi di annunci | ✓ | ✓ | ✓ | ✓ |
| Modifica gruppi di annunci | ✓ | ✓ | | ✓ |
| Visualizzazione annunci | ✓ | ✓ | ✓ | ✓ |
| Modifica annunci | | ✓ | | ✓ |
| Visualizzazione parole chiave | ✓ | ✓ | ✓ | ✓ |
| Visualizzazione Tipi di pubblico | ✓ | ✓ | ✓ | ✓ |
| Visualizzazione destinazioni automatiche | ✓ | ✓ | ✓ | ✓ |
| Vista creatività | ✓ | ✓ | ✓ | ✓ |
| Visualizzazione estensioni | ✓ | ✓ | ✓ | ✓ |
| Visualizzazione Classificazioni etichette | ✓ | ✓ | ✓ | ✓ |
| Visualizzazione Posizionamenti | ✓ | ✓ | ✓ | ✓ |
| Visualizzazione Consigli | ✓ | ✓ | ✓ | ✓ |
| Visualizza bulksheet | | ✓ | | ✓ |
| Modifica bulksheet | ✓ | ✓ | ✓ | ✓ |

**Gestione report**

| Autorizzazione | Base | Esperto | Sola lettura | Amministratore |
|---|---|---|---|---|
| Visualizza registri cronologia | ✓ | ✓ | ✓ | ✓ |
| Visualizza i Report Programmati | ✓ | ✓ | ✓ | ✓ |
| Modifica i Report Programmati | | ✓ | | ✓ |

**Gestione installazione**

| Autorizzazione | Base | Esperto | Sola lettura | Amministratore |
|---|---|---|---|---|
| Visualizza account | ✓ | ✓ | ✓ | ✓ |
| Modifica account | | ✓ | | ✓ |
| Visualizza account MCC | ✓ | ✓ | ✓ | ✓ |
| Modifica account MCC | | ✓ | | ✓ |

## Attività per amministratori

### Accedi a Adobe Admin Console e aprilo in Search, Social e Commerce

>[!PREREQUISITES]
>
>Per accedere a Admin Console è necessario disporre di un tipo di accesso amministratore a Search, Social e Commerce.

1. Vai su https://adminconsole.adobe.com/enterprise/.

1. (Se non si è connessi a CX Enterprise) Accedere a CX Enterprise:

   1. Immetti l&#39;ID [!DNL Adobe] e fai clic su **[!UICONTROL Continue]**.

   1. Selezionare **[!UICONTROL Personal Account]&quot; o &#x200B;** [!UICONTROL Company or School Account]**.<!-- Will it necessarily be "Company or School Account?" -->

   1. Selezionare l&#39;organizzazione CX Enterprise applicabile.

      Admin Console si apre sulla scheda [!UICONTROL Overview].

   1. In [!UICONTROL Product & services], fare clic su &quot;[!UICONTROL Adobe Advertising, Search, Social, & Commerce — Org Name]&quot;.

      La pagina del prodotto si apre sulla scheda [!UICONTROL Product profiles] per Ricerca, Social e Commerce. Schede aggiuntive includono [!UICONTROL Users] e [!UICONTROL Product Admins].

### Flusso di lavoro per gli amministratori di sistema

Segui questo flusso di lavoro per ogni istanza client di Search, Social e Commerce.

1. [Accedi a Adobe Admin Console e aprilo in Search, Social e Commerce](#open-admin-console).

1. (Facoltativo) [Aggiungere un altro amministratore di sistema](https://helpx.adobe.com/it/enterprise/using/admin-roles.html#enterprise) come backup.

1. Delega la gestione di prodotti e utenti [aggiungendo amministratori di prodotti](https://helpx.adobe.com/it/enterprise/using/admin-roles.html#enterprise).

### Flusso di lavoro per gli amministratori di prodotto

Segui questo flusso di lavoro per ogni istanza client di Search, Social e Commerce.

1. [Accedi a Adobe Admin Console e aprilo in Search, Social e Commerce](#open-admin-console).

1. Se necessario, creare gli utenti finali [singolarmente](https://helpx.adobe.com/it/enterprise/using/manage-users-individually.html) o [in blocco](https://helpx.adobe.com/it/enterprise/using/bulk-upload-users.html).

1. (Facoltativo) Crea [gruppi di utenti](https://helpx.adobe.com/it/enterprise/using/user-groups.html) per l&#39;istanza e assegna gli utenti a ciascun gruppo di utenti.

   Se l’istanza ha molti utenti, crea gruppi di utenti per garantire che agli utenti siano assegnati i profili giusti in base al loro livello di esperienza. Consulta il Passaggio 4 per assegnare gruppi di utenti ai profili di prodotto. Puoi creare gruppi di utenti in base alla linea di business, alle esigenze di accesso degli utenti, alla data di assunzione dell’utente o ad altri criteri.

   >[!IMPORTANT]
   >
   >I nomi dei gruppi di utenti devono comunicare chiaramente i diritti che devono essere assegnati al gruppo. Ad esempio, se si desidera creare un gruppo di utenti con diritti di sola lettura, includere &quot;Sola lettura&quot; nel nome del gruppo di utenti, ad esempio &quot;Acme_Uk_ReadOnly&quot; o &quot;Acme_ReadOnly&quot;.

1. (Facoltativo) [Crea profili di prodotto personalizzati](https://helpx.adobe.com/it/enterprise/using/manage-product-profiles.html) con set di autorizzazioni definiti.

   I profili personalizzati si aggiungono ai quattro profili di prodotto predefiniti già disponibili.

   Ogni profilo di prodotto di un’organizzazione deve avere un nome univoco. Se la tua organizzazione utilizza più istanze Search, Social e Commerce (ad esempio, Acme_US e Acme_JP), non puoi duplicare il nome di un profilo di prodotto in più istanze. **Best practice:** utilizza la convenzione di denominazione `<Name>_<Instance>,`, ad esempio &quot;Simulation_Only_JP&quot;.

   **Attenzione:** le autorizzazioni del prodotto sono molto granulari. Presta attenzione quando configuri profili di prodotto personalizzati o potresti omettere le funzionalità che desideri includere.

1. [Assegnare ogni utente o gruppo di utenti al relativo profilo di prodotto](https://helpx.adobe.com/it/enterprise/using/manage-product-profiles.html) manualmente o in blocco.

## Guida completa all’amministrazione degli utenti e collegamenti aggiuntivi

* Per ulteriori informazioni sull&#39;amministrazione degli utenti tramite Adobe Admin Console, vedere &quot;[Adobe Enterprise &amp; Teams Administration Guide](https://helpx.adobe.com/it/enterprise/admin-guide.html)&quot;, inclusa la [panoramica di Admin Console](https://helpx.adobe.com/it/enterprise/using/admin-console.html).

* Admin Console: [https://adminconsole.adobe.com](https://adminconsole.adobe.com)
