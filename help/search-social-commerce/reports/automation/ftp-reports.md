---
title: Accesso FTP ai rapporti
description: Scopri come ricevere i rapporti in una posizione FTP di sola lettura.
exl-id: eca9f033-5b1b-4afa-926b-b4c31e2dede3
feature: Search Reports
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '428'
ht-degree: 0%

---

# Accesso FTP ai rapporti

Facoltativamente, è possibile ricevere i rapporti in una posizione FTP di sola lettura, da cui è possibile recuperare i file per ulteriori processi automatizzati (ad esempio, per analizzare i dati con un altro programma). Tutti i report di base tranne [!UICONTROL Search Engine Account Report] e tutti i rapporti avanzati possono essere inviati a una posizione FTP come file TSV compressi (impostazione predefinita) o file CSV, con estensione .ZIP. Tutte le intestazioni di file TSV o CSV sono incluse e non possono essere eliminate.

L&#39;accesso FTP ai rapporti richiede l&#39;accesso a un account FTP specificato ed è necessario impostare i modelli di rapporto utilizzando una convenzione di denominazione specifica e una pianificazione.

## Configurare un account FTP per l&#39;accesso ai rapporti

* Contatta il team dell’account Adobe per configurare un account FTP per l’accesso ai rapporti.

  Il team ti fornirà nome utente e password.

## Configurare modelli di rapporto per la consegna FTP

Per generare rapporti nella directory FTP designata, crea un [modello di report](templates/template-create.md) con le seguenti convenzioni di denominazione e pianificazione.

>[!NOTE]
>
>Tutti i report avanzati e tutti i report di base ad eccezione di [!UICONTROL Search Engine Account Report] può essere recapitato a un percorso FTP.

1. Nel modello di report, includere le seguenti informazioni in qualsiasi punto del nome del modello:

   * `FTP` (in lettere maiuscole).

   * (Facoltativo) Una qualsiasi delle tre date di sistema, utilizzando la seguente sintassi con distinzione tra maiuscole e minuscole, comprese le parentesi:

      * `[TODAY]` — Per includere la data, l&#39;ora e il minuto in cui è stato eseguito il report. Poiché include l’ora esatta, lo stesso modello può essere eseguito più volte al giorno senza sovrascrivere il rapporto precedente.

      * `[SDATE]` — Per includere la data di inizio dell&#39;intervallo di date del rapporto.

      * `[EDATE]` — Per includere la data di fine dell&#39;intervallo di date del rapporto.

   * (Facoltativo) `[CSV]` (in lettere maiuscole e racchiuse tra parentesi quadre) per creare file in formato CSV anziché in formato TSV predefinito.

   Esempio: `[TODAY]-Portfolio-FTP-[SDATE]-[EDATE]-[CSV]` creerebbe un file come 202305051656-Portfoli-FTP-20230428-20110504.csv.

1. Pianifica l’esecuzione del rapporto a un’ora specifica.

   I report vengono consegnati all&#39;account FTP entro un&#39;ora dal completamento.

>[!NOTE]
>
>* Per inviare i rapporti completati per e-mail, è sufficiente inserire gli indirizzi di tutti i destinatari e-mail quando si genera il rapporto o il modello.
>* I report vengono eseguiti in base alle pianificazioni specificate e vengono consegnati all&#39;account FTP entro un&#39;ora dal completamento.

## Accedere ai rapporti in un archivio FTP

Per accedere ai rapporti, connettiti a uno dei seguenti host FTP, utilizzando l’accesso per il tuo account FTP (`amo<userID>rpt`, ad esempio amo1234rpt) e una password o una chiave di connessione privata, se impostata:

* Clienti internazionali: `ftp3.adobe.net`
* Clienti USA: `ftp5.adobe.net`

>[!NOTE]
>
>L’archivio dei rapporti è di sola lettura e viene eliminato ogni 15 giorni.


>[!MORELIKETHIS]
>
>* [Creare un modello di rapporto](/help/search-social-commerce/reports/automation/templates/template-create.md)
