---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '313'
ht-degree: 0%

---
# Modello di annuncio pubblicitario - Impostazioni parole chiave negative a livello di campagna

**[!UICONTROL Delete negative keywords when omitted from list]:** (tutte le reti di annunci tranne Yandex; facoltativo) Elimina le parole chiave negative esistenti a livello di campagna create in precedenza utilizzando il modello che non sono specificate negli elenchi seguenti. **Nota:** le parole chiave negative create con altri mezzi (ad esempio nei bulksheet normali, nelle visualizzazioni [!UICONTROL Campaigns] o nell&#39;editor annunci della rete di annunci) non vengono mai rimosse utilizzando il modello.

**[!UICONTROL Set negative keywords by campaign name condition]:** (tutte le reti di annunci tranne Yandex; facoltativo) Consente di specificare parole chiave negative per le campagne il cui nome include una stringa specificata. Quando selezioni questa opzione, puoi aggiungere fino a tre stringhe di nome della campagna e parole chiave corrispondenti.

Per ogni stringa, fare clic su **[!UICONTROL Add (Up to 3)]** e immettere le informazioni seguenti:

* **[!UICONTROL If campaign name contains]:** Stringa di testo da cercare in un punto qualsiasi del nome della campagna. La query fa distinzione tra maiuscole e minuscole, ad esempio &quot;[!DNL Car]&quot; corrisponde al nome della campagna &quot;[!DNL Car Parts]&quot; ma non a &quot;[!DNL INTERIOR CAR ACCESSORIES]&quot;.

* **[!UICONTROL Apply these negatives]:** Qualsiasi parola chiave negativa statica a livello di campagna da aggiungere per le campagne il cui nome include la stringa specificata. Per specificare più parole chiave o più tipi di corrispondenza per la stessa parola chiave, immetterle su righe separate. Utilizza la sintassi seguente, senza il segno meno:

   * Corrispondenza ampia negativa: `keyword` (non supportata da [!DNL Microsoft Advertising])
   * Corrispondenza frase negativa: `"keyword"`
   * Corrispondenza esatta negativa: `[keyword]`

La sintassi abituale per i tipi di corrispondenza esatta e di frase viene utilizzata nel bulksheet generato quando si propagano i dati di feed tramite il modello. **Nota:** non è possibile visualizzare le parole chiave negative nella scheda [!UICONTROL Keywords] o nella visualizzazione [!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns].

**[!UICONTROL All other campaigns: Apply these negatives]:** (tutte le reti di annunci tranne [!DNL Yandex]; facoltativo) Qualsiasi parola chiave statica negativa a livello di campagna da aggiungere per campagne il cui nome non corrisponde a una stringa specificata. Per specificare più parole chiave o più tipi di corrispondenza per la stessa parola chiave, immetterle su righe separate. Utilizza la sintassi seguente, senza il segno meno:

* Corrispondenza ampia negativa: `keyword` (non supportata da [!DNL Microsoft Advertising])
* Corrispondenza frase negativa: `"keyword"`
* Corrispondenza esatta negativa: `[keyword]`

La sintassi abituale per i tipi di corrispondenza esatta e di frase viene utilizzata nel bulksheet generato quando si propagano i dati di feed tramite il modello. **Nota:** non è possibile visualizzare le parole chiave negative nella scheda [!UICONTROL Keywords] o nella visualizzazione [!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns].
