---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 0%

---
# Modello di annuncio pubblicitario - Impostazioni parole chiave negative a livello di gruppo di annunci

**[!UICONTROL Delete negative keywords when omitted from list]:** (Tutte le reti di annunci tranne Yandex; facoltativo) Elimina le parole chiave negative esistenti a livello di gruppo di annunci create in precedenza utilizzando il modello che non sono specificate negli elenchi seguenti. **Nota:** Parole chiave negative create utilizzando altri mezzi (ad esempio nei bulksheet normali, il [!UICONTROL Campaigns] o nell’editor di annunci della rete di annunci) non vengono mai rimosse utilizzando il modello.

**[!UICONTROL Apply these negatives]:** (Tutte le reti pubblicitarie tranne [!DNL Yandex]; facoltativo) qualsiasi parola chiave negativa statica a livello di gruppo di annunci da aggiungere. Per specificare più parole chiave o più tipi di corrispondenza per la stessa parola chiave, immetterle su righe separate. Utilizza la sintassi seguente, senza il segno meno:

* Corrispondenza ampia negativa: `keyword` (non supportato da [!DNL Microsoft Advertising])
* Corrispondenza frase negativa: `"keyword"`
* Corrispondenza esatta negativa: `[keyword]`

La sintassi abituale per i tipi di corrispondenza esatta e di frase viene utilizzata nel bulksheet generato quando si propagano i dati di feed tramite il modello. **Nota:** Non è possibile visualizzare le parole chiave negative in [!UICONTROL Keywords] o nella scheda [!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] visualizzazione.
