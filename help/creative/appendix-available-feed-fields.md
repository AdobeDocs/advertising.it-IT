---
title: Campi disponibili per i file di feed di annunci dinamici
description: Scopri i campi che puoi includere nei file di feed utilizzati per creare annunci dinamici.
feature: Creative Dynamic Creatives
source-git-commit: 67ee38860ac5cb7e9340f8e9d4667353e509b1ec
workflow-type: tm+mt
source-wordcount: '348'
ht-degree: 0%

---

# Appendice: campi disponibili per i file di feed di annunci dinamici

I seguenti campi di feed sono disponibili nel backend di Advertising Creative. Puoi caricare un [file di feed](/help/creative/feeds/asset-manage.md) che utilizza nomi di campo specifici per la tua organizzazione. Tuttavia, prima di poter creare un [catalogo](/help/creative/feeds/catalog-manage.md) dal file di feed, è necessario mappare ogni campo nel file di feed a uno dei seguenti campi nel [modello di feed](/help/creative/feeds/feed-template-manage.md) che verrà utilizzato per creare il catalogo.

L&#39;unico campo che deve avere un equivalente nel file di feed è `PART_NUM`.

<!-- Questions:

What are these?
Rank
PROFILE_FILTER fields



Do geo fields need be populated as follows:
Country: 2 Letter country code (example: US)
State: state code_2 letter country code (example: CA_US)
City: City name_State code_2 letter country code (example: San Jose_CA_US)
DMA: DMA _2 letter country code (example: 201_US)
Zipcode: Zip code_2 letter country code (example: 94086_US)


TRUE?   GEO fields(Country/State/City/DMA/Zip), UT fields (UT1/UT2/UT3/UT4/UT5) [do we have an equivalent now?], Filtering fields(F1/F2/F3/F4/F5) can have comma separated values. We can have upto 2K characters.

TRUE FOR CSV AND TSV? character encoding on text format files should be UTF-8 -- If yes, then add that with feed file requirements.

-->

| Nome campo | Tipo di dati | Obbligatorio |
|------------|-----------|-----------|
| PART_NUM | varchar(64) | SÌ |
| PRODUCT_NAME | text | NO |
| URL_PRODOTTO | text | NO |
| PREZZO | decimal(10,2) | NO |
| PREZZO_SCONTO | decimal(10,2) | NO |
| IMMAGINE | varchar(1024) | NO |
| IMAGE_HEIGHT | int | NO |
| LARGHEZZA_IMMAGINE | int | NO |
| IMAGE_1 | varchar(1024) | NO |
| IMAGE_2 | varchar(1024) | NO |
| IMAGE_3 | varchar(1024) | NO |
| IMAGE_4 | varchar(1024) | NO |
| IMAGE_5 | varchar(1024) | NO |
| IMAGE_6 | varchar(1024) | NO |
| IMAGE_7 | varchar(1024) | NO |
| IMAGE_8 | varchar(1024) | NO |
| IMAGE_9 | varchar(1024) | NO |
| IMAGE_10 | varchar(1024) | NO |
| TESTO_1 | text | NO |
| TESTO_2 | text | NO |
| TESTO_3 | text | NO |
| TESTO_4 | text | NO |
| TESTO_5 | text | NO |
| TESTO_6 | text | NO |
| TESTO_7 | text | NO |
| TESTO_8 | text | NO |
| TESTO_9 | text | NO |
| TESTO_10 | text | NO |
| TESTO_11 | text | NO |
| TEXT_12 | text | NO |
| TEXT_13 | text | NO |
| TEXT_14 | text | NO |
| TEXT_15 | text | NO |
| ADDITIONAL_PRICE_1 | decimal(10,2) | NO |
| ADDITIONAL_PRICE_2 | decimal(10,2) | NO |
| ADDITIONAL_PRICE_3 | decimal(10,2) | NO |
| AD_SIZE | varchar(32) | NO |
| CLASSIFICA | int | NO |
| PAESE | text | NO |
| STATO | text | NO |
| CITTÀ | text | NO |
| ZIP | text | NO |
| DMA | text | NO |
| PROFILE_FILTER_1 | text | NO |
| PROFILE_FILTER_2 | text | NO |
| PROFILE_FILTER_3 | text | NO |
| PROFILE_FILTER_4 | text | NO |
| PROFILE_FILTER_5 | text | NO |
| DATAPASS_FILTER_1 | text | NO |
| DATAPASS_FILTER_2 | text | NO |
| DATAPASS_FILTER_3 | text | NO |
| DATAPASS_FILTER_4 | text | NO |
| DATAPASS_FILTER_5 | text | NO |
| AUDIENCE_SEGMENT | text | NO |
| LINGUA | text | NO |
| CREATIVE_ATTRIBUTE_1 | varchar(256) | NO |
| CREATIVE_ATTRIBUTE_2 | varchar(256) | NO |
| CREATIVE_ATTRIBUTE_3 | varchar(256) | NO |
| CREATIVE_ATTRIBUTE_4 | varchar(256) | NO |
| CREATIVE_ATTRIBUTE_5 | varchar(256) | NO |
| CREATIVE_ATTRIBUTE_6 | varchar(256) | NO |
| CREATIVE_ATTRIBUTE_7 | varchar(256) | NO |
| CREATIVE_ATTRIBUTE_8 | varchar(256) | NO |
| CREATIVE_ATTRIBUTE_9 | varchar(256) | NO |
| CREATIVE_ATTRIBUTE_10 | varchar(256) | NO |
| IS_DEFAULT | enum | NO |

>[!MORELIKETHIS]
>
>* [Flussi di lavoro per annunci dinamici](/help/creative/introduction/workflow-dynamic-ads.md)
>* [Gestione file risorse](/help/creative/feeds/asset-manage.md)
>* [Gestisci modelli di feed](/help/creative/feeds/feed-template-manage.md)
>* [Gestisci cataloghi](/help/creative/feeds/catalog-manage.md)
