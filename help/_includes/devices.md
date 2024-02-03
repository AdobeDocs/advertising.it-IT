---
source-git-commit: 24aa1afe9611ca6ae46795c9bca2964e1d9c4f97
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 0%

---
# Campo Dispositivi nelle impostazioni della campagna GGL e MS e del gruppo di annunci

**[!UICONTROL Devices]:** (Facoltativo; non disponibile per [!DNL Google Ads] le campagne con le massime prestazioni o [!DNL Microsoft Advertising] video o annunci video CTV) Configura le regolazioni delle offerte per diversi tipi di dispositivi, come percentuali dell’offerta a livello di parola chiave. Ad esempio, se l’offerta a livello di parola chiave è 1 USD e la regolazione dell’offerta per gli smartphone è del 50%, l’offerta per lo smartphone è di 1,50 USD. Per impostazione predefinita, non viene immesso alcun valore (regolazione offerta=0) e tutti i dispositivi vengono offerti in corrispondenza dell’offerta a livello di parola chiave.

Per [!DNL Google Ads], le percentuali valide possono includere -100 per smartphone e tablet (per non fare offerte per il tipo di dispositivo) e da -90 a 900 per tutti i tipi di dispositivo.

Per [!DNL Microsoft Advertising], le percentuali valide possono includere:

* Smartphone e tablet: -100 (per non fare offerte per il tipo di dispositivo) e da -90 a 900
* Desktop: da 0 a 900

>[!NOTE]
>* Le impostazioni a livello di gruppo di annunci sostituiscono le impostazioni a livello di campagna. Tuttavia, se escludi un dispositivo a livello di campagna, non puoi ignorare l’esclusione a livello di gruppo di annunci.
>* Se assegni questa campagna a un portfolio ottimizzato standard, Search, Social e Commerce determina automaticamente l’offerta a livello di parola chiave di base per aiutare il portfolio a raggiungere il suo obiettivo. La rete di annunci regola quindi l’offerta come specificato per diversi tipi di dispositivi.
>* (Per tutte le campagne/gruppi di annunci eccetto [!DNL Microsoft Advertising] gruppi di annunci nella rete del pubblico) Se assegni questa campagna a un portfolio ottimizzato standard configurato per&quot;[!UICONTROL Auto-optimize Bid Adjustment Values],&quot; la funzionalità di ottimizzazione cambia le regolazioni delle offerte per i dispositivi specificate a livello di gruppo di annunci, purché il valore ideale calcolato sia compreso nei valori minimo e massimo specificati nelle impostazioni del portfolio e il gruppo di annunci non escluda le offerte per il tipo di dispositivo.
