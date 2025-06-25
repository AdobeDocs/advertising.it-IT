---
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 0%

---
# Modello di annuncio pubblicitario - Impostazioni parole chiave negative a livello di gruppo di annunci

**[!UICONTROL Delete negative keywords when omitted from list]:** (tutte le reti di annunci tranne Yandex; facoltativo) Elimina le parole chiave negative esistenti a livello di gruppo di annunci create in precedenza utilizzando il modello che non sono specificate negli elenchi seguenti. **Nota:** le parole chiave negative create con altri mezzi (ad esempio nei bulksheet normali, nelle visualizzazioni [!UICONTROL Campaigns] o nell&#39;editor annunci della rete di annunci) non vengono mai rimosse utilizzando il modello.

**[!UICONTROL Apply these negatives]:** (tutte le reti di annunci tranne [!DNL Yandex]; facoltativo) Qualsiasi parola chiave statica negativa a livello di gruppo di annunci da aggiungere. Per specificare più parole chiave o più tipi di corrispondenza per la stessa parola chiave, immetterle su righe separate. Utilizza la sintassi seguente, senza il segno meno:

* Corrispondenza ampia negativa: `keyword` (non supportata da [!DNL Microsoft Advertising])
* Corrispondenza frase negativa: `"keyword"`
* Corrispondenza esatta negativa: `[keyword]`

La sintassi abituale per i tipi di corrispondenza esatta e di frase viene utilizzata nel bulksheet generato quando si propagano i dati di feed tramite il modello. **Nota:** non è possibile visualizzare le parole chiave negative nella scheda [!UICONTROL Keywords] o nella visualizzazione [!UICONTROL Search, Social, & Commerce] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns].
