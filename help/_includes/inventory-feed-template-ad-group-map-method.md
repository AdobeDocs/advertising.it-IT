---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 0%

---
# Modello di annuncio testuale - Metodo mappa gruppo di annunci

**[!UICONTROL Map Method]:** (Quando [!UICONTROL Map Only] è abilitato per i gruppi di annunci; tutte le reti di annunci eccetto [!DNL Yandex]) Il metodo con cui le nuove parole chiave e gli annunci vengono mappati ai gruppi di annunci esistenti:

* *[!UICONTROL Contains Anywhere]:* Aggiunge dati a un gruppo di annunci esistente il cui nome include la stringa specificata, se esistente.

* *[!UICONTROL Contains Exactly]:* Aggiunge dati a un gruppo di annunci esistente il cui nome include la stringa specificata, se esistente.

* *[!UICONTROL Exactly Matches]* (impostazione predefinita): aggiunge dati a un gruppo di annunci esistente con lo stesso nome, se esistente.

Se non viene trovata alcuna corrispondenza, tutti i dati per il gruppo di annunci vengono ignorati. Se i dati del gruppo di annunci nel feed non includono i dati della campagna, il gruppo di annunci viene mappato su un gruppo di annunci con lo stesso nome in qualsiasi campagna, se ne esiste uno. Se vengono trovate più corrispondenze di gruppi di annunci, le parole chiave e gli annunci vengono mappati a tutti.
