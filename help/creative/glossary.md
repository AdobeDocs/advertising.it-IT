---
title: Glossario
description: Cfr. definizioni dei termini chiave.
feature: Creative Introduction
source-git-commit: 4e61ce32862411a7a83c66773e41d032770ad861
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 0%

---

# Glossario {#glossary}

*Versione beta chiusa*

<!-- more feature metadata?? -->

<!-- ## A-B {#a-b} -->

<!-- not sure I need these "x-through" terms since that we're not creating conversion pixels in this UI, but see if they come up in other text -->

**click-through:** clic su un annuncio che genera una conversione.

**destinazione passaggio dati:** le destinazioni passaggio dati consentono la selezione di elementi annuncio in base ai dati forniti in tempo reale da DSP, publisher o partner. Può includere dati di terze parti.

<!-- verify this -->In un’esperienza pubblicitaria, ogni destinazione di passaggio di dati può includere fino a cinque coppie chiave-valore; puoi specificare le chiavi e almeno un valore nel primo nodo di destinazione a quel livello e le stesse chiavi sono disponibili per i nodi di destinazione di pari livello. Ciascuna coppia chiave-valore viene aggiunta come macro al tag annuncio per questa esperienza. Al momento dell’ad impression, DSP, l’editore o il partner è responsabile della sostituzione dei valori con dati specifici per tale impression. Le informazioni vengono passate a [!DNL Creative] in modo che possa mostrare un&#39;esperienza pubblicitaria appropriata in base alle regole definite nell&#39;esperienza.

Ad esempio, per indirizzare uno o più possibili creativi a visualizzatori di sesso femminile che si trovano nel segmento 1234, puoi configurare le destinazioni del passaggio dati `gender=female` e `segment=1234` per il nodo di destinazione. Il DSP che trasmette l’impression compila il tag con le informazioni su genere e segmento e i visitatori che soddisfano i requisiti specificati vengono visualizzati come uno dei creativi associati.

**engagement-through:** un impegno pubblicitario (ad esempio lo scorrimento di un annuncio carosello o l&#39;espansione di un annuncio) che genera una conversione. Questo tipo di evento è diverso dal clic sull’annuncio per raggiungere una pagina di destinazione o un evento nella pagina di destinazione.

<!-- or flexible html5 creative variation? Not sure we need to mention this since there's no place to view the different variations per se:

**variation of a flexible HTML5 creative:** A derivation of a flexible HTML5 creative asset in your [!UICONTROL Creative Libraries], which is generated when you assign the creative to an experience and change any of the default attributes within the experience.
-->

**view-through:** un&#39;impression pubblicitaria, o una stringa di impression, che determina una conversione senza che l&#39;utente faccia clic su un annuncio.
