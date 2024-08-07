---
title: Informazioni su [!UICONTROL CCPA Opt-out-of-Sale] segmenti e rapporti
description: Scopri come creare segmenti per tenere traccia degli ID dalle richieste di rifiuto del CCPA e come recuperare i rapporti degli ID.
feature: CCPA, DSP Segments
exl-id: 28b5e00b-a695-46f1-abbf-7bbd78f05411
source-git-commit: 4b9cc5956d573b346eacdf71a8ea490c162b4660
workflow-type: tm+mt
source-wordcount: '243'
ht-degree: 0%

---

# Informazioni su [!UICONTROL CCPA Opt-out-of-Sale] segmenti e rapporti

Puoi tenere traccia degli ID degli utenti dalle richieste di rifiuto del consumatore sul tuo sito web, in base al California Consumer Privacy Act (CCPA), [creando e implementando un segmento di rifiuto del CCPA](ccpa-opt-out-segment-create.md). Gli utenti rimangono nei segmenti di rifiuto del CCPA per un tempo indefinito.

Una volta implementato il tag pixel del segmento, Adobe Advertising inizia a raccogliere un pool di ID per conto dell’inserzionista.

## Rapporti sulla rinuncia del consumatore

Adobe Advertising genera rapporti mensili sugli ID inviati dai clienti per richieste di rifiuto per l’account. I dati consolidano le richieste acquisite utilizzando i segmenti di rifiuto del CCPA creati in DSP e tutte le richieste effettuate tramite l’API Privacy Service.  I rapporti vengono generati il primo di ogni mese per il mese precedente. Ad esempio, l’elenco mensile degli utenti di giugno è disponibile il 1° luglio.

Ogni rapporto è disponibile come file di testo separato da tabulazioni compresso in formato GZIP. Gli ID utente acquisiti nei segmenti di rifiuto del CCPA sono identificati per segmento e dall’inserzionista.

È possibile [recuperare i collegamenti ai report mensili](ccpa-opt-out-segment-report-retrieve.md) creati nei tre mesi precedenti dall&#39;DSP o utilizzando l&#39;DSP [!DNL Trafficking API]. Ogni collegamento è valido per sette giorni, ma viene aggiornato ogni volta che un cliente tenta di recuperarne uno.

>[!MORELIKETHIS]
>
>* [Supporto di Adobe Advertising per il California Consumer Privacy Act: Consumer Opt-out Support](/help/privacy/ccpa/ccpa-opt-out-of-sale.md)
>* [Crea e implementa un segmento [!UICONTROL CCPA Opt-Out-of-Sale]](ccpa-opt-out-segment-create.md)
>* [Recupera report sulla rinuncia del consumatore](ccpa-opt-out-segment-report-retrieve.md)
>* [Informazioni su Gestione dell&#39;audience](audience-about.md)
