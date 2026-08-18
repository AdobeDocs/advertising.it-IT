---
title: Metadati C2PA in Creative Studio
description: Scopri come i metadati C2PA vengono automaticamente allegati al contenuto generato o modificato con intelligenza artificiale generativa in Creative Studio.
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: d0d9f2ed-c163-44e1-97a1-4ace121416b8
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: d335c890ccc3ff8b2d391881660a71d10fcba53a
workflow-type: tm+mt
source-wordcount: 414
ht-degree: 2%

---

# Metadati C2PA in [!UICONTROL Creative Studio]

[!UICONTROL Creative Studio] allega automaticamente i metadati C2PA al contenuto generato o modificato con IA generativa, in modo che la provenienza del contenuto dell&#39;annuncio venga registrata come metadati durevoli e invisibili. I metadati seguono lo standard della [coalizione per la provenza e l&#39;autenticità dei contenuti](https://c2pa.org/) (C2PA).

## Tipi di contenuto e ambito {#cc-content-types}

| Tipo di contenuto | Supportato? | Servizio di intelligenza artificiale che genera il contenuto | Modello che genera le credenziali |
| --- | --- | --- | --- |
| Immagini | Sì. I metadati C2PA vengono allegati quando le immagini vengono generate o modificate con l’intelligenza artificiale generativa e vengono conservati mediante le operazioni di ritaglio e ridimensionamento eseguite dall’Assistente AI. | [!DNL Adobe Firefly C2PA] | [!DNL Gemini Flash] |

## Azioni che associano metadati C2PA

Nella tabella seguente viene riepilogato quando si allegano metadati C2PA, in base all&#39;azione eseguita nell&#39;Assistente di IA per l&#39;archiviazione di [!UICONTROL Creative Studio].

| Azione | Descrizione | Metadati C2PA allegati? | Esempio di caso d’uso |
| --- | --- | --- | --- |
| **Generare un&#39;immagine** | Creare una nuova immagine utilizzando un prompt di testo | Sempre, perché l’immagine è generata dall’intelligenza artificiale generativa. | Un prompt di testo consente di generare una nuova immagine o un nuovo logo di sfondo per un modello di annuncio.<br><br>Utilizzi un prompt di testo per sostituire l&#39;immagine predefinita in un concetto di annuncio con una risorsa caricata dalla libreria.<br><br>Viene utilizzato un prompt di testo per generare varianti di un&#39;immagine di sfondo in un modello di annuncio. |

## Cosa succede quando il contenuto si sposta? {#cc-content-moves}

La catena di provenienza completa viene mantenuta quando un utente scarica un file di immagine o viene inviato per essere servito in un annuncio.

## Cosa includono i metadati C2PA?

Per ogni generazione o modifica GenAI, i metadati C2PA includono quanto segue. Se una risorsa viene modificata più volte, ogni operazione viene visualizzata nei metadati C2PA.

* Informazioni su nome e versione del sistema di IA utilizzato ([!DNL Adobe Firefly C2PA])
* Modello di IA utilizzato ([!DNL Gemini Flash])
* Utilizzo: se è stato generato o modificato utilizzando GenAI
* Ora e data di creazione e/o modifica dei contenuti con strumenti di intelligenza artificiale generativi
* Identificatore univoco (che può essere utilizzato per distinguere ogni utilizzo di IA generativa)

## Come posso visualizzare i metadati C2PA per un’immagine?

Per visualizzare la cronologia completa delle risorse di un&#39;immagine:

* Apri il file di immagine in uno strumento di ispezione dell’autenticità dei contenuti, ad esempio https://contentauthenticity.adobe.com/inspect o https://verify.contentauthenticity.org/.

* Visualizzare i metadati dell&#39;immagine.

* Visualizzare il codice immagine utilizzando lo strumento di ispezione del codice del browser (spesso denominato [!DNL Inspect]).

![Esempio di metadati C2PA per un&#39;immagine](/help/creative/assets/cs-content-credentials-example.png "Metadati C2PA per un&#39;immagine")

## Risorse aggiuntive

* [[!DNL Adobe] linee guida utente di IA generativa](https://www.adobe.com/it/legal/licenses-terms/adobe-gen-ai-user-guidelines.html)

>[!MORELIKETHIS]
>
>* [Informazioni su Creative Studio](/help/creative/creative-studio/creative-studio-about.md)
