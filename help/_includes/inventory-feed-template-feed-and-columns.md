---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '231'
ht-degree: 0%

---
# Modello di annuncio testuale - Feed e colonne

**[!UICONTROL Feed & Columns]:** Un [file di feed](/help/search-social-commerce/campaign-management/inventory-feeds/feed-files-manage.md) o account esercente associato al modello e le colonne (intestazioni) per il file o l&#39;account selezionato:

* *[!UICONTROL Feed File]:* Caricare un file o selezionarne uno dall&#39;elenco dei file di feed disponibili.

* *[!UICONTROL Google Merchant Center]:* Seleziona un [account [!DNL Google Merchant Center] sincronizzato](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md). Search, Social e Commerce creano solo gruppi di prodotti; [!DNL Google Ads] genera automaticamente gli annunci per i gruppi di prodotti. Le colonne personalizzate non sono supportate.

* *[!UICONTROL Microsoft Merchant Center]:* ([!DNL Microsoft Advertising] solo modelli di acquisto) Seleziona un [account [!DNL Microsoft Merchant Center] sincronizzato](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md). Search, Social e Commerce creano solo gruppi di prodotti; [!DNL Microsoft Advertising] genera automaticamente gli annunci di prodotto per i gruppi di prodotti. Le colonne personalizzate non sono supportate.

L’associazione del modello a un file di feed o a un account esercente è facoltativa fino a quando non sei pronto per creare annunci utilizzando il modello.

Quando si inserisce una colonna di feed in un campo modello, il valore inserito viene indicato come `[field_name]`, dove &quot;nome_campo&quot; è il nome del campo specificato, per indicare che il valore è una variabile.

>[!NOTE]
>
>* Se modifichi il file di feed o l’account per un modello esistente, potrebbe essere necessario regolare i parametri del modello se il nuovo file contiene intestazioni diverse.
>* Se il file di feed o l’account associato al modello viene eliminato o disabilitato, viene eliminata anche l’associazione ed è necessario selezionare un nuovo file di feed prima di poter creare altri annunci utilizzando il modello. Se il nuovo file di feed o account non include le stesse intestazioni del file originale, potrebbe essere necessario modificare di conseguenza i parametri del modello.
