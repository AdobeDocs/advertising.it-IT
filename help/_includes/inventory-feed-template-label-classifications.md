---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '237'
ht-degree: 0%

---
# Modello di annuncio testuale - Classificazioni etichette

**\[Componente\] [!UICONTROL Label Classifications] > \[Classificazione e valore etichetta\]:** (Facoltativo) Valori per un massimo di cinque classificazioni di etichette esistenti da assegnare ai diversi componenti della campagna creati o modificati utilizzando il modello. I valori delle etichette vengono ereditati dalle entità figlio (comprese le entità figlio create in seguito), pertanto non è necessario immettere valori per le entità figlio a meno che non si desideri ignorare i valori ereditati. Le classificazioni delle etichette per i gruppi di prodotti vengono applicate al livello di unità (più granulare).

Per ogni componente della campagna a cui desideri assegnare le classificazioni delle etichette:

1. Fai clic sulla casella di controllo accanto a **\[Componente\][!UICONTROL Label Classifications]**.

1. Configura i valori di classificazione delle etichette per il modello:

   * Per ogni classificazione e valore di etichetta da assegnare al componente, effettua le seguenti operazioni:

      1. Clic **[!UICONTROL Add Label Classification]**.

      1. Selezionare la classificazione dell&#39;etichetta esistente, quindi selezionare un valore esistente o immettere un nuovo valore.

         La lunghezza massima di ogni valore è di 100 caratteri e può includere caratteri ASCII e non ASCII.

         Per inserire un nome di colonna come parametro dinamico per un valore di classificazione di etichetta, fare clic nel campo di input (il secondo campo) e quindi fare clic sul nome di una colonna nell&#39;elenco delle colonne.

         Puoi includere un solo valore per classificazione per componente della campagna. Ad esempio, una campagna può avere Color=Red ma non Color=Red e Color=Blue.
   * Per modificare un valore di classificazione delle etichette esistente, selezionare o immettere un nuovo valore.

   * Per rimuovere un valore di classificazione di etichetta esistente, fai clic su **[!UICONTROL X]** accanto al valore.
