---
title: Quando vengono creati o eliminati i componenti del conto dai feed di inventario?
description: Scopri quali situazioni creano ed eliminano i componenti del conto durante la registrazione dei feed di inventario.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '855'
ht-degree: 0%

---

# Quando vengono creati o eliminati i componenti del conto dai feed di inventario?

*[!DNL Google Ads], [!DNL Microsoft® Advertising], [!DNL Yahoo! Japan Ads] (solo azioni di eliminazione), e [!DNL Yandex] solo account*

Quando un file di feed inventario viene propagato tramite un modello, i componenti conto vengono creati ed eliminati nel modo seguente.

>[!NOTE]
>
>Gli annunci duplicati non vengono mai creati all’interno di un gruppo di annunci.

| Scenario | Esempio | Azione |
|----|----|----|
| I dati dei feed includono un nuovo valore per una colonna utilizzata in un nome di campagna, un nome di gruppo di annunci, una parola chiave o un gruppo di prodotti. | File precedenti:<br>Campaign=Hats<br>Campaign=Guanti<br><br>Nuovo file:<br>Campaign=Scarpe | Se non esiste nella rete di annunci, viene creata una nuova campagna, un nuovo gruppo di annunci, una parola chiave o un nuovo gruppo di prodotti. |
| I dati dei feed contengono un nuovo valore per una colonna utilizzata in un annuncio. | File precedente: un annuncio incluso prezzo=20<br><br>Nuovo file: per lo stesso annuncio, prezzo=10 | Quando la copia dell’annuncio per [!DNL Microsoft® Advertising] annunci di testo espansi, [!DNL Yahoo! Japan ads], o [!DNL Yandex] annunci viene modificato, l’annuncio esistente viene eliminato e ne viene creato uno nuovo.<br><br>Quando la copia dell’annuncio viene modificata per altri tipi di annunci o quando la colonna applicabile viene utilizzata per un [!DNL Google Ads] parametro dell’annuncio ({param1} o {param2}) in un annuncio, l’annuncio esistente viene aggiornato. |
| Le impostazioni del modello per la campagna, il gruppo di annunci, la parola chiave o il gruppo di prodotti sono cambiate dall’ultima propagazione. | Impostazione precedente:Parola chiave=[Parola chiave]<br><br>Nuova impostazione: Parola chiave=&lt;color>[Parola chiave] | Se non esiste nella rete di annunci, viene creata una nuova campagna, un nuovo gruppo di annunci, una parola chiave o un nuovo gruppo di prodotti. |
| Le impostazioni del modello per un annuncio sono state modificate dopo l’ultima propagazione. | Impostazione precedente: Ad description=&quot;Acquista [categoria] ora.&quot;<br><br>Nuova impostazione: Ad description=&quot;Acquista [brand] ora.&quot; | Quando la copia dell’annuncio per [!DNL Microsoft® Advertising] annunci di testo espansi, [!DNL Yahoo! Japan ads], o [!DNL Yandex] annunci viene modificato, l’annuncio esistente viene eliminato e ne viene creato uno nuovo.<br><br>Quando la copia dell’annuncio viene modificata per altri tipi di annunci o quando la modifica riflette una modifica nella colonna utilizzata per un singolo [!DNL Google Ads] parametro dell’annuncio ({param1} o {param2}) in un annuncio, l’annuncio esistente viene aggiornato. |
| I nuovi dati del feed non includono una riga per una campagna o un gruppo di annunci esistente. | n/d | Le campagne e i gruppi di annunci esistenti rimangono invariati. |
| I nuovi dati del feed non includono una riga per un gruppo di annunci, un annuncio, una parola chiave o un gruppo di prodotti esistente. | n/d | Il gruppo di annunci, l’annuncio, la parola chiave o il gruppo di prodotti esistente rimane invariato, è messo in pausa o viene eliminato, a seconda della [impostazioni dei dati di feed](feed-settings-manage.md#feed-data-settings). |
| I nuovi dati di feed per un gruppo di prodotti padre esistente non includono righe per i gruppi di prodotti figlio esistenti. | n/d | Il gruppo di prodotti padre esistente rimane invariato o viene eliminato, in base alla [impostazioni dei dati di feed](feed-settings-manage.md#feed-data-settings). <b>Nota:</b> Se le impostazioni dei dati di feed sono configurate per mettere in pausa gli elementi di riga mancanti, il gruppo di prodotti principale viene comunque eliminato perché non è possibile mettere in pausa i gruppi di prodotti. |
| I nuovi dati di feed includono una riga per un gruppo di annunci, un annuncio, una parola chiave o un gruppo di prodotti che a) nei dati precedenti era stato omesso ma b) da allora ed è stato messo in pausa in base al [impostazioni dei dati di feed](feed-settings-manage.md#feed-data-settings). | n/d | Il gruppo di annunci, l’annuncio, la parola chiave o il gruppo di prodotti esistente viene riattivato, senza perdere la cronologia o il punteggio di qualità. |
| I nuovi dati di feed includono una riga per un gruppo di annunci, un annuncio, una parola chiave o un gruppo di prodotti che a) nei dati precedenti era stato omesso ma b) da allora ed è stato eliminato in base al [impostazioni dei dati di feed](feed-settings-manage.md#feed-data-settings). | n/d | Viene creato un nuovo gruppo di annunci, annunci, parole chiave o gruppi di prodotti. |
| Hai disabilitato l’opzione a livello di campagna o di gruppo di annunci in &quot;[!UICONTROL Delete negative keywords when omitted from list].&quot; | L&#39;elenco delle parole chiave negative include &quot;coupé&quot; e &quot;vettura sportiva&quot;.<br><br>Il gruppo di annunci include già la parola chiave negativa &quot;SUV&quot;. | Eventuali parole chiave negative esistenti non presenti nell&#39;elenco rimangono invariate. |
| Hai abilitato l’opzione a livello di campagna o di gruppo di annunci su &quot;[!UICONTROL Delete negative keywords when omitted from list],&quot; e le parole chiave negative non presenti nell&#39;elenco. | L&#39;elenco delle parole chiave negative include &quot;coupé&quot; e &quot;vettura sportiva&quot;.<br><br>Il gruppo di annunci include già la parola chiave negativa &quot;SUV&quot;. | Eventuali parole chiave negative non specificate create in precedenza utilizzando il modello vengono eliminate quando un file di feed viene propagato attraverso il modello. Tuttavia, qualsiasi parola chiave negativa non specificata creata utilizzando altri mezzi (ad esempio nei bulksheet normali, il [!UICONTROL Campaigns] o nell’editor pubblicitario della rete di annunci) rimangono invariate. |  | La data di fine pianificata per i componenti di un file di feed pubblicato si verifica. | n/d | Le campagne esistenti rimangono invariate. I gruppi di annunci, gli annunci e le parole chiave esistenti rimangono invariati, vengono messi in pausa o vengono eliminati in base al [impostazioni dei dati di feed](feed-settings-manage.md#feed-data-settings). |
| Il livello di magazzino di un articolo scende al di sotto di un minimo specificato nella [impostazioni dei dati di feed](feed-settings-manage.md#feed-data-settings). | File precedente: stock=10<br><br>Nuovo file: stock=0 | Le campagne esistenti rimangono invariate. I gruppi di annunci, gli annunci, le parole chiave e i gruppi di prodotti esistenti vengono messi in pausa o eliminati, in base al [impostazioni dei dati di feed](feed-settings-manage.md#feed-data-settings). |
| Il livello di stock di un articolo torna al di sopra di un minimo specificato nella [impostazioni dei dati di feed](feed-settings-manage.md#feed-data-settings). | File precedente: stock=0<br><br> Nuovo file: stock=10 | Quando gli annunci, le parole chiave o i gruppi di prodotti esistenti vengono messi in pausa, vengono riattivati senza perdere la cronologia o il punteggio di qualità. Se non esistono annunci, parole chiave o gruppi di prodotti (ad esempio, se sono stati eliminati in precedenza perché il livello delle scorte era inferiore al minimo), ne vengono creati di nuovi. |

>[!MORELIKETHIS]
>
>* [Informazioni sull’automazione della gestione degli annunci tramite i feed di inventario](inventory-feeds-about.md)
>* [Flusso di lavoro per la gestione dei dati della campagna tramite i feed di inventario](inventory-feeds-workflow.md)

