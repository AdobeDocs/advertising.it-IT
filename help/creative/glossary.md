---
title: Glossario
description: Cfr. definizioni dei termini chiave.
feature: Creative Introduction
source-git-commit: fd925c641bef7953aea50813725252c3913757fa
workflow-type: tm+mt
source-wordcount: '286'
ht-degree: 0%

---

# Glossario {#glossary}

*Versione beta chiusa*

<!-- more feature metadata?? -->

<!-- ## A-B {#a-b} -->

<!-- not sure I need these "x-through" terms since that we're not creating conversion pixels in this UI, but see if they come up in other text -->

**click-through:** clic su un annuncio che genera una conversione.

**destinazione passaggio dati:** le destinazioni passaggio dati consentono di selezionare elementi annuncio in base ai dati forniti in tempo reale dall&#39;DSP, dall&#39;editore o dal partner. Può includere dati di terze parti.

<!-- verify this -->In un’esperienza pubblicitaria, ogni destinazione di passaggio di dati può includere fino a cinque coppie chiave-valore; puoi specificare le chiavi e almeno un valore nel primo nodo di destinazione a quel livello e le stesse chiavi sono disponibili per i nodi di destinazione di pari livello. Ciascuna coppia chiave-valore viene aggiunta come macro al tag annuncio per questa esperienza. Al momento dell’ad impression, l’DSP, l’editore o il partner è responsabile della sostituzione dei valori con dati specifici per tale impression. Le informazioni vengono passate a [!DNL Creative] in modo che possa mostrare un&#39;esperienza pubblicitaria appropriata in base alle regole definite nell&#39;esperienza.

Ad esempio, per indirizzare uno o più possibili creativi a visualizzatori di sesso femminile che si trovano nel segmento 1234, puoi configurare le destinazioni del passaggio dati `gender=female` e `segment=1234` per il nodo di destinazione. L’DSP che trasmette l’impression popola il tag con le informazioni su genere e segmento, e i visitatori che soddisfano i requisiti specificati vengono visualizzati come uno dei creativi associati.

**engagement-through:** un impegno pubblicitario (ad esempio, guardare un video o espandere un annuncio) che genera una conversione.

<!-- or flexible html5 creative variation? -->
**variante di un contenuto creativo flessibile di HTML5:** derivazione di una risorsa creativa flessibile di HTML5 in [!UICONTROL Creative Libraries], generata quando si assegna il contenuto creativo a un&#39;esperienza e si modifica uno qualsiasi degli attributi predefiniti all&#39;interno dell&#39;esperienza.

<!-- Not sure if this will be implemented, and how:
You can view all derived creatives, including not only the base creatives you've added but also each child creative derivation, in the card view in [!UICONTROL Creative] > [!UICONTROL Libraries]. In the toolbar, click __?__ , and then select Derived Creatives. [Clarify how to tell which have variations. I can't find any now.]
-->

**view-through:** un&#39;impression pubblicitaria, o una stringa di impression, che determina una conversione senza che l&#39;utente faccia clic su un annuncio.
