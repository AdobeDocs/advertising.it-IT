---
title: Domande frequenti
description: xxx
source-git-commit: 1c13874967ec4ad264e5fa6a5e0dfeb6120f53cc
workflow-type: tm+mt
source-wordcount: '367'
ht-degree: 0%

---

# Domande frequenti xxx

## title

https://adobeadcloud.zendesk.com/agent/tickets/14214 Per impostazione predefinita, Adobe Analytics riporta tutti gli eventi acquisiti in ogni rapporto. &quot;[!UICONTROL Unspecified]&quot; gli eventi rappresentano gli eventi di completamento del modulo che non erano collegati ad Adobe Advertising. Ad esempio, nel rapporto Ad Platform , le conversioni organiche o guidate da una campagna e-mail diventerebbero &quot;non specificate&quot;.

Puoi usare il filtro per rimuovere eventi non specificati dai rapporti rimuovendo il segno di spunta dall’opzione &quot;Includi non specificato (nessuno)&quot;. <!-- Not sure if this is in DSP or in Analytics Workspace -->

## title

https://adobeadcloud.zendesk.com/agent/tickets/24323 Inserisci i tag evento di Analytics negli stessi punti dei pixel di Ad Cloud per assicurarti che XXX corrisponda.

## title

https://adobeadcloud.zendesk.com/agent/tickets/24323

D: Durante il nostro controllo interno sulla sicurezza, alcune funzioni sono state contrassegnate come problematiche relative alla sicurezza che abbiamo attivato quando abbiamo integrato Ad Cloud nella nostra installazione Adobe Analytics esistente.

L’integrazione in questione è tra AdCloud e Adobe Audience Manager. Questa funzione aumenta la percentuale di corrispondenza per l’ID visitatore tra AdCloud e Adobe Audience Manager. Per farlo, invia richieste di rete a pagead.l.doubleclick.net, star-mini.c10r.facebook.com e pug88000nf.pubmatic.com per determinare se questi servizi hanno un ID esistente per il visitatore che può essere sfruttato. Si tratta delle richieste di rete contrassegnate come un rischio per la sicurezza e che si verificano per tutti i visitatori del sito.

Il nostro revisore ci chiede di disabilitare questa funzione. Cosa succede se blocchiamo quelle richieste di rete?

R: Abbiamo verificato con il nostro prodotto e ci hanno detto che i pixel in questione sono allo scopo di aumentare le percentuali di corrispondenza dei cookie tra Ad Cloud, specifici partner di inventario/SSP (rispetto a DSP) e AAM.  Se vengono rimossi, il cliente potrebbe vedere un certo livello di percentuale di corrispondenza ridotta tra AAC/AAM e i partner di inventario per cui sono utilizzati i rispettivi pixel, ma non si aspetterebbe che sia sostanziale.

Per Ad Cloud Search, vediamo che l’ID organizzazione Experience Cloud dell’inserzionista è configurato per Mathworks, ma il nostro team di prodotto non vede la configurazione di Mathworks per attivare i tipi di pubblico in Ad Cloud. Stai utilizzando Adobe Audience Manager per inviare tipi di pubblico a Ad Cloud Search? In caso contrario, la loro rimozione non avrà un impatto sul flusso di lavoro corrente. AAM l’Assistenza clienti può aiutarti a rimuovere questi pixel se non desideri che vengano attivati.

