---
title: Prerequisiti per la configurazione di un'origine dati  [!DNL Google Analytics]
description: Scopri i passaggi da completare prima di configurare un'origine dati  [!DNL Google Analytics] .
role: User, Admin
exl-id: 97b0c149-5f82-4a1e-a5d9-aeab43cbd88f
feature: Search Admin, Search Data Sources
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '402'
ht-degree: 0%

---

# Prerequisiti per configurare un&#39;origine dati [!DNL Google Analytics]

Prima di configurare un&#39;origine dati [!DNL Google Analytics], è necessario stabilire il parametro &quot;ef_id&quot; della stringa di query Search, Social e Commerce come chiave primaria per passare i dati da [!DNL Google Analytics] a Search, Social e Commerce. Impostare la chiave primaria per ogni combinazione di account e proprietà [!DNL Google Analytics] per la quale si desidera sincronizzare i dati. Altre persone nella tua organizzazione potrebbero dover completare queste attività; consulta di seguito per ulteriori informazioni.

Se gli URL della pagina di destinazione per gli annunci o le parole chiave non includono già i reindirizzamenti a Search, Social e Commerce, aggiungili prima.

## Prerequisito 1: implementare un token Search, Social e Commerce (parametro della stringa di query &quot;ef_id&quot;) negli URL della pagina di destinazione per tutti gli account pubblicitari applicabili

A ogni clic di ricerca a pagamento per le campagne rilevanti, è necessario generare un `ef_id` univoco e aggiungerlo all&#39;URL della pagina di destinazione come stringa di query, ad esempio `https://www.adobe.com?someParam=123&ef_id=abcde:123456789:s`, dove `&ef_id=abcde:123456789:s` è il simbolo di aggiunta, la chiave `ef_id` e il valore `ef_id`. Per includere un ef_id, gli account e le campagne di rete degli annunci pertinenti devono avere [!UICONTROL Tracking Type] &quot;[!UICONTROL EF Redirect]&quot; e [!UICONTROL Redirect Type] &quot;[!UICONTROL Token].&quot;

Per gli account e le campagne esistenti, l’ef_id è probabilmente già implementato.

Se ef_id non è incluso, chiedi assistenza al team del tuo account Adobe.

Una volta completati tutti i prerequisiti, `ef_id` viene utilizzato come chiave primaria per passare i dati da [!DNL Google Analytics] a Search, Social e Commerce.

## Prerequisito 2: acquisisci il token di ricerca, social e Commerce (parametro della stringa di query &quot;ef_id&quot;) in una dimensione personalizzata per ogni proprietà [!DNL Google Analytics] rilevante

Ripetere le seguenti attività per ogni combinazione di account [!DNL Google Analytics] e proprietà per cui si desidera sincronizzare i dati. Per informazioni su queste attività, consulta la [[!DNL Google Analytics] documentazione sulla creazione e l&#39;implementazione di dimensioni personalizzate](https://support.google.com/analytics/answer/2709829?hl=en#zippy=%2Cin-this-article).

1. In [!DNL Google Analytics], creare una dimensione personalizzata denominata &quot;`ef_id`&quot;. Impostare l&#39;ambito della dimensione su [!DNL User] e impostare la dimensione su attiva.

   >[!NOTE]
   >
   >Questo prerequisito richiede l’autorizzazione di modifica per le proprietà pertinenti.

1. Aggiorna il codice di tracciamento [!DNL Google Analytics] per acquisire il valore del parametro della stringa di query ef_id quando è presente nell&#39;URL della pagina di destinazione e memorizzarlo nella dimensione personalizzata ef_id.

   >[!NOTE]
   >
   >L’ef_id deve trovarsi solo negli URL della pagina di destinazione.

   Ad esempio, se l&#39;URL della pagina di destinazione è `https://www.adobe.com?someParam=123&ef_id=abcde:123456789:s&anotherParam=asdf`, il valore della dimensione ef_id in [!DNL Google Analytics] è `abcde:123456789:s`.

   >[!NOTE]
   >
   >Questo prerequisito deve essere completato da uno sviluppatore qualificato.

>[!MORELIKETHIS]
>
>* [Informazioni sulla sincronizzazione [!DNL Google Analytics] metriche di conversione](data-source-about.md)
>* [Configurare una visualizzazione  [!DNL Google Analytics] come origine dati](data-source-configure.md)
>* [Modifica origine dati [!DNL Google Analytics] ](data-source-edit.md)
>* [Sospendi la sincronizzazione di un&#39;origine dati](data-source-pause.md)
>* [Autentica nuovamente un&#39;origine dati [!DNL Google Analytics] ](data-source-reauthenticate.md)
>* [[!DNL Google Analytics] impostazioni origine dati](data-source-settings.md)
>* [Appendice - Disponibile [!DNL Google Analytics] metriche](data-source-ga-metrics.md)
