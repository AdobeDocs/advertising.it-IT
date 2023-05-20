---
title: Informazioni su [!UICONTROL CCPA Opt-out-of-Sale] Segmenti e rapporti
description: Scopri come creare segmenti per tenere traccia degli ID dalle richieste di rifiuto del CCPA e come recuperare i rapporti degli ID.
feature: CCPA, DSP Segments
exl-id: 28b5e00b-a695-46f1-abbf-7bbd78f05411
source-git-commit: 7e614ecb517515217d812926f61ca10437820efd
workflow-type: tm+mt
source-wordcount: '243'
ht-degree: 0%

---

# Informazioni su [!UICONTROL CCPA Opt-out-of-Sale] Segmenti e rapporti

Puoi tenere traccia degli ID degli utenti dalle richieste di rifiuto del consumatore sul tuo sito web, in base al California Consumer Privacy Act (CCPA), mediante [creazione e implementazione di un segmento di rifiuto del CCPA](ccpa-opt-out-segment-create.md). Gli utenti rimangono nei segmenti di rifiuto del CCPA per un tempo indefinito.

Una volta implementato il tag pixel del segmento, Adobe Advertising inizierà a raccogliere un pool di ID per conto dell’inserzionista.

## Rapporti sulla rinuncia del consumatore

Adobe Advertising genera rapporti mensili sugli ID inviati dai clienti per richieste di rifiuto per l’account. I dati consolidano le richieste acquisite utilizzando i segmenti di rifiuto del CCPA creati in DSP e tutte le richieste effettuate tramite l’API Privacy Service.  I rapporti vengono generati il primo di ogni mese per il mese precedente. Ad esempio, l’elenco mensile degli utenti di giugno è disponibile il 1° luglio.

Ogni rapporto è disponibile come file di testo separato da tabulazioni compresso in formato GZIP. Gli ID utente acquisiti nei segmenti di rifiuto del CCPA sono identificati per segmento e dall’inserzionista.

È possibile [recuperare i collegamenti ai report mensili](ccpa-opt-out-segment-report-retrieve.md) che sono state create nei tre mesi precedenti, dall’interno dell’DSP o utilizzando l’DSP [!DNL Trafficking API]. Ogni collegamento è valido per sette giorni, ma viene aggiornato ogni volta che un cliente tenta di recuperarne uno.

>[!MORELIKETHIS]
>
>* [Adobe di supporto per la pubblicità per il California Consumer Privacy Act: supporto per la rinuncia del consumatore](/help/privacy/ccpa/ccpa-opt-out-of-sale.md)
>* [Creare e implementare un [!UICONTROL CCPA Opt-Out-of-Sale] Segmento](ccpa-opt-out-segment-create.md)
>* [Recuperare i rapporti sulla rinuncia del consumatore](ccpa-opt-out-segment-report-retrieve.md)
>* [Informazioni su Gestione dell&#39;audience](audience-about.md)

