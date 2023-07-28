---
title: Prerequisiti per la configurazione di un [!DNL Google Analytics] origine dati
description: Scopri i passaggi da completare prima di configurare una [!DNL Google Analytics] origine dati.
role: User, Admin
exl-id: cbb2ad6d-8494-4fa4-928c-238b25bda3a6
feature: Search Admin, Search Data Sources
source-git-commit: 9c4dcb19e386d8e1eea541776f5b92c9d500ae9f
workflow-type: tm+mt
source-wordcount: '417'
ht-degree: 0%

---

# Prerequisiti per la configurazione di un [!DNL Google Analytics] origine dati

Prima di configurare un [!DNL Google Analytics] origine dati, è necessario stabilire il parametro della stringa di query Search, Social &amp; Commerce &quot;ef_id&quot; come chiave primaria da cui trasmettere i dati [!DNL Google Analytics] in Search, Social e Commerce. Imposta la chiave primaria per ogni [!DNL Google Analytics] combinazione di account e proprietà per cui si desidera sincronizzare i dati. Altre persone nella tua organizzazione potrebbero dover completare queste attività; consulta di seguito per ulteriori informazioni.

Se gli URL della pagina di destinazione per gli annunci o le parole chiave non includono già i reindirizzamenti a Search, Social e Commerce, aggiungili prima.

## Prerequisito 1: implementare un token di ricerca, social e commerce (parametro della stringa di query &quot;ef_id&quot;) negli URL della pagina di destinazione per tutti gli account pubblicitari applicabili

A ogni clic di ricerca a pagamento per le campagne pertinenti, viene visualizzato un messaggio univoco `ef_id` deve essere generato e aggiunto all’URL della pagina di destinazione come stringa di query, ad esempio `https://www.adobe.com?someParam=123&ef_id=abcde:123456789:s`, dove `&ef_id=abcde:123456789:s` è il simbolo di aggiunta, `ef_id` chiave, e `ef_id` valore. Per includere un ef_id, gli account e le campagne di ad network pertinenti devono avere [!UICONTROL Tracking Type] &quot;[!UICONTROL EF Redirect]&quot; e [!UICONTROL Redirect Type] &quot;[!UICONTROL Token].&quot;

Per gli account e le campagne esistenti, l’ef_id è probabilmente già implementato.

Se ef_id non è incluso, chiedi assistenza al team del tuo account Adobe.

Una volta completati tutti i prerequisiti, `ef_id` viene utilizzato come chiave primaria da cui trasmettere i dati [!DNL Google Analytics] in Search, Social e Commerce.

## Prerequisito 2: acquisisci il token di ricerca, social e commerce (parametro della stringa di query &quot;ef_id&quot;) in una dimensione personalizzata per ogni pertinente [!DNL Google Analytics] proprietà

Ripeti le seguenti attività per ogni [!DNL Google Analytics] combinazione di account e proprietà per cui si desidera sincronizzare i dati. Consulta [[!DNL Google Analytics] documentazione sulla creazione e l’implementazione di dimensioni personalizzate](https://support.google.com/analytics/answer/2709829?hl=en#zippy=%2Cin-this-article) per informazioni su queste attività.

1. In entrata [!DNL Google Analytics], crea una dimensione personalizzata denominata &quot;`ef_id`&quot;. Imposta l&#39;ambito della dimensione su [!DNL User]e impostare la dimensione su attiva.

   >[!NOTE]
   >
   >Questo prerequisito richiede l’autorizzazione di modifica per le proprietà pertinenti.

1. Aggiorna il tuo [!DNL Google Analytics] codice di tracciamento per acquisire il valore del parametro della stringa di query ef_id quando è presente nell’URL della pagina di destinazione e memorizzarlo nella dimensione personalizzata ef_id.

   >[!NOTE]
   >
   >L’ef_id deve trovarsi solo negli URL della pagina di destinazione.

   Ad esempio, se l’URL della pagina di destinazione è `https://www.adobe.com?someParam=123&ef_id=abcde:123456789:s&anotherParam=asdf`, quindi il valore della dimensione ef_id in [!DNL Google Analytics] è `abcde:123456789:s`.

   >[!NOTE]
   >
   >Questo prerequisito deve essere completato da uno sviluppatore qualificato.

>[!MORELIKETHIS]
>
>* [Informazioni sulla sincronizzazione [!DNL Google Analytics] metriche di conversione](data-source-about.md)
>* [Configurare un [!DNL Google Analytics] visualizzare come origine dati](data-source-configure.md)
>* [Modifica un [!DNL Google Analytics] origine dati](data-source-edit.md)
>* [Sospendere la sincronizzazione di un&#39;origine dati](data-source-pause.md)
>* [Autentica di nuovo un [!DNL Google Analytics] origine dati](data-source-reauthenticate.md)
>* [[!DNL Google Analytics] impostazioni origine dati](data-source-settings.md)
>* [Appendice - Disponibile [!DNL Google Analytics] metriche](data-source-ga-metrics.md)
