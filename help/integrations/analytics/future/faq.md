---
title: Domande frequenti
description: xxx
source-git-commit: 1c13874967ec4ad264e5fa6a5e0dfeb6120f53cc
workflow-type: tm+mt
source-wordcount: '367'
ht-degree: 0%

---

# Domande frequenti xxx

## titolo

https://adobeadcloud.zendesk.com/agent/tickets/14214 Per impostazione predefinita, Adobe Analytics segnala tutti gli eventi acquisiti in ogni rapporto. &quot;[!UICONTROL Unspecified]&quot;Gli eventi rappresentano eventi di completamento dei moduli che non erano collegati a Adobe Advertising. Ad esempio, nel rapporto Ad Platform, le conversioni organiche o guidate da una campagna e-mail rientrano in &quot;non specificato&quot;.

Puoi utilizzare il filtro per rimuovere eventi non specificati dai rapporti rimuovendo il segno di spunta dall’opzione &quot;Includi non specificato (nessuno)&quot;. <!-- Not sure if this is in DSP or in Analytics Workspace -->

## titolo

https://adobeadcloud.zendesk.com/agent/tickets/24323 Posiziona i tag evento di Analytics negli stessi punti dei pixel di Ad Cloud per assicurarti che XXX corrisponda.

## titolo

https://adobeadcloud.zendesk.com/agent/tickets/24323

D: Durante il controllo di sicurezza interno, alcune funzioni sono state segnalate come problemi di sicurezza che sono stati abilitati quando abbiamo integrato Ad Cloud nell’installazione di Adobe Analytics esistente.

L’integrazione in questione è tra AdCloud e Adobe Audience Manager. Questa funzione aumenta la percentuale di corrispondenza per l’ID visitatore tra AdCloud e Adobe Audience Manager. A tale scopo, invia richieste di rete a pagead.l.doubleclick.net, star-mini.c10r.facebook.com e pug88000nf.pubmatic.com per determinare se questi servizi dispongono di un ID esistente per il visitatore che può essere utilizzato. Si tratta delle richieste di rete che sono state contrassegnate come rischi per la sicurezza e che si verificano per tutti i visitatori del sito.

Il nostro auditor ci chiede di disattivare questa funzione. Cosa succede se blocchiamo queste richieste di rete?

R: Abbiamo controllato con il nostro prodotto e hanno indicato che i pixel in questione sono allo scopo di aumentare le percentuali di corrispondenza dei cookie tra Ad Cloud, partner specifici di inventario/SSP (rispetto a DSP) e AAM.  Se vengono rimossi, il cliente potrebbe notare un certo livello di riduzione del tasso di corrispondenza tra AAC/AAM e i partner di inventario a cui fanno riferimento i rispettivi pixel, ma non si aspetterebbe che sia sostanziale.

Per Ad Cloud Search, vediamo che l’ID organizzazione dell’Experience Cloud dell’inserzionista è configurato per Mathworks, ma che il nostro team di prodotto non visualizza la configurazione di Mathworks per attivare i tipi di pubblico in Ad Cloud. Stai utilizzando Adobe Audience Manager per inviare tipi di pubblico ad Ad Cloud Search? In caso contrario, la loro rimozione non avrà alcun impatto sul flusso di lavoro corrente. L’Assistenza clienti AAM può aiutarti a rimuovere questi pixel se non desideri che vengano attivati.

