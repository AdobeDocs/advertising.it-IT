---
title: Modifica impostazioni feed report foglio di calcolo
description: Scopri come modificare le impostazioni per i feed di fogli di calcolo.
exl-id: 8ca36006-4038-404b-aaf9-66dc3e9ddcf6
feature: Search Reports
TQID: https://experienceleague.adobe.com/xsq7qkYTc5p7Q4Q-LKHeCX7-W8DRW80ET6ylOWocYG0
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 317
ht-degree: 0%

---

# Modifica impostazioni feed report foglio di calcolo

*Solo per report di base e report di precisione modello*

È possibile modificare il modello di report, il modello [!DNL Microsoft Excel] e altri parametri utilizzati per un feed di foglio di calcolo.

>[!NOTE]
>
> Se si modificano le colonne nel modello di report o si utilizza un modello di report nuovo o aggiornato, è necessario aggiornare il modello [!DNL Excel] di conseguenza e caricarlo nuovamente.

1. Nel menu principale, fare clic su **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Insights & Reports] >[!UICONTROL Spreadsheet Feeds]**.

1. (Facoltativo) Per aggiornare il modello di report o il modello [!DNL Excel] utilizzato per il feed del foglio di calcolo:

   * (Facoltativo) Per utilizzare un modello di report diverso o aggiornato per il feed, [crea un nuovo [!DNL Excel] modello per il modello di report](spreadsheet-feed-create-excel-template.md).

     Nel passaggio successivo, sarà necessario caricare sia il modello di report che il nuovo file [!DNL Excel].

   * (Facoltativo) Per aggiungere semplicemente colonne personalizzate al modello [!DNL Excel], inserire le colonne a destra delle colonne dal modello di report, quindi salvare il file come foglio di calcolo [!DNL Excel] in formato XLSX. Caricare il nuovo file [!DNL Excel] nel passaggio successivo.

1. Modificare le impostazioni del feed del foglio di calcolo:

   * Nel menu principale, fare clic su **[!UICONTROL Reports]>[!UICONTROL Spreadsheet Feeds]**.

   * Accanto al nome del feed del foglio di calcolo, fare clic su ![Pulsante Visualizza/modifica impostazioni](/help/search-social-commerce/assets/settings.png "Pulsante Visualizza/modifica impostazioni").

   * Nella finestra di dialogo [!UICONTROL Edit Spreadsheet Feed], modifica le [impostazioni feed foglio di calcolo](spreadsheet-feed-settings.md).

   * Fare clic su **[!UICONTROL Submit]**.

   * (Facoltativo) Una volta che il feed [!UICONTROL Update Status] è *[!UICONTROL Finished]*, fai clic su **[!UICONTROL XLSX]** accanto al feed, quindi apri o salva il file in base alla normale procedura del browser.

     >[!NOTE]
     >
     > Se il modello di rapporto associato al feed viene successivamente eliminato, anche il feed viene eliminato.

     I feed dei fogli di calcolo vengono aggiornati automaticamente alle ore 08:00 di ogni giorno nel fuso orario dell&#39;inserzionista. Se il modello di rapporto include indirizzi per qualsiasi destinatario e-mail, tali indirizzi ricevono notifiche quando il foglio di calcolo viene aggiornato.

>[!MORELIKETHIS]
>
>* [Informazioni sui feed di report del foglio di calcolo](spreadsheet-feed-about.md)
>* [Creare un feed di report per fogli di calcolo](spreadsheet-feed-create.md)
>* [Creare un  [!DNL Excel] modello per un feed di report di foglio di calcolo](spreadsheet-feed-create-excel-template.md)
>* [Modifica impostazioni feed report foglio di calcolo](spreadsheet-feed-edit.md)
>* [Impostazioni feed report foglio di calcolo](spreadsheet-feed-settings.md)
>* [Visualizzare o salvare un file di feed di report del foglio di calcolo](spreadsheet-feed-view-or-save.md)
>* [Aggiorna manualmente i feed dei report del foglio di calcolo](spreadsheet-feed-refresh.md)
