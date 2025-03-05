---
title: Partner Ad Serving certificati
description: Visualizza tutti i server di annunci e le unità di annunci certificati.
feature: DSP Ads
exl-id: 1435efdd-8823-4f07-b9e4-65bd4789226e
source-git-commit: 97e0f562153983202a2f3641e17dd682ff3d00ea
workflow-type: tm+mt
source-wordcount: '328'
ht-degree: 0%

---

# Partner Ad Serving certificati

| Ad Server | Audio | Visualizzazione | Display ad alto impatto | Video | Requisiti speciali e note |
| --- | --- | --- | --- | --- | --- |
| [!DNL A Million Ads] | X | | | | |
| [!DNL Adacado] | | X | | | |
| [!DNL Ad Colony] | | | | X | Solo VAST mobile |
| [!DNL Adconion] | | | | X | |
| [!DNL Adform] | X | X | | X | |
| [!DNL ADITION Technologies] | | X | | | |
| [!DNL ADman Media] | X | | | | |
| [!DNL Adobe Advertising Creative] | | | | | |
| [!DNL ADventori] | | X | | | |
| [!DNL Artsai] | | X | | X | |
| [!DNL Atlas] | | | | X | |
| [!DNL Big Ads] | | | X | | Cubo (Desktop), Cubo (Mobile), Schede (Desktop), Big Reveal (Desktop), Cine-Cube (Desktop), Cinematografia (Desktop). Imposta tutti questi tipi di annunci in DSP come 300x250. Certificato solo tramite [!DNL Magnite DV+]. |
| [!DNL Bonzai] | | | X | | |
| [!DNL Contobox] | | | X | | |
| [!DNL Conversant] | | X | | | |
| [!DNL DCM] | X | X | X | X | |
| [!DNL Dotdash] | | | | X | |
| [!DNL Doubleclick] | X | X | | X | |
| [!DNL Extreme Reach] | | | | X | |
| [!DNL Eyereturn] | | X | | | |
| [!DNL Flashtalking] | X | X | | X | |
| [!DNL Frequency] | X | | | | |
| [!DNL GumGum] | | | X | | Intervallo nello slot: 21x21; video mobile in-slot: 22x22; desktop in-slot: 24x24; hoverboard nello slot: 25x25; velocità nello slot: 26x26; interfaccia super: 29x29; angolo espandibile nello schermo: 20x20 |
| [!DNL HUMAN] (In Precedenza [!DNL White Ops]) | X | X | | X | |
| [!DNL IAS] | X | X | | X | |
| [!DNL IBM] | | X | | X | |
| [!DNL Innovid] | X | X | | X | |
| [!DNL Inskin] | | | X | | Gli skin ad alto impatto (inclusi gli annunci conversazionali Cavai) devono essere serviti su un ID di offerta display 180x150 attraverso la rete di inventario Inskin. |
| [!DNL Jivox] | | X | | | |
| [!DNL Kargo] | | X | | X | 320x50 Ancoraggio, BYOC, Hover, Breakout, Breakaway, Runway e Sidekick; 300x250 Outstream, HighRise; Display desktop standard (non sono richiesti ID di plug-in di annunci specifici); Video Anchor (solo VAST); CTV tramite [!DNL Pubmatic]</br></br>Contatta il team del tuo account Adobe per assistenza nella configurazione delle unità pubblicitarie. |
| [!DNL Linkstorm] | | | X | | |
| [!DNL mCanvas] | | | X | | |
| [!DNL Medialets] | | X | | | |
| [!DNL Minute Media] | | X | | | Interfaccia del desktop (970x250) |
| [!DNL Moat] | X | X | | X | |
| [!DNL PLAYGROUND XYZ] | | | X | | |
| [!DNL Pubmatic] | | | | X | Solo VAST |
| [!DNL RevJet] | | | | X | Solo VAST |
| [!DNL Seedtag] | | X | X | | |
| [!DNL SeenThis] | | X | | | La certificazione di visualizzazione include tag video nel banner |
| [!DNL Sharethrough] | | | | | Solo CTV, Native e Outstream |
| [!DNL Sizmek] | X | X | | X | OLV e CTV</br></br>Per eseguire il rendering dei tag nell&#39;interfaccia utente, racchiudere il tag con `<a>` tag (all&#39;inizio e alla fine). Vedi il tag di esempio seguente:</br></br>`<a><script src="https://bs.serving-sys.com/Serving/adServer.bs?c=28&cn=display&pli=1074570064&w=900&h=550&ord=[timestamp]&ifrm=-1&z=0"></script> <noscript> <a href="https://bs.serving-sys.com/Serving/adServer.bs?cn=brd&pli=1074570064&Page=&Pos=-602368150" target="_blank"> <img src="https://bs.serving-sys.com/Serving/adServer.bs?c=8&cn=display&pli=1074570064&Page=&Pos=-602368150" border=0 width=900 height=550></a> </noscript><a>` |
| [!DNL Spaceback] | | X | | | |
| [!DNL Spirable] | | X | | | |
| [!DNL SUBLIME] | | | X | | |
| [!DNL SundaySky] | | | | X | |
| [!DNL Teads] | | X | | | Non è disponibile alcun supporto per VPAID sull&#39;inventario a valle. |
| [!DNL Trueffect] | | X | | | |
| [!DNL Undertone] | | | X | | Unità pubblicitaria personalizzata Page Grabber caricata come 180x150 in DSP</br></br>Quando Index Exchange supera un&#39;asta di 180x150 e presenta offerte DSP sull&#39;asta e fornisce un&#39;impression, il contenuto creativo si espande a un annuncio di visualizzazione a pagina intera.</br></br>Certificato inizialmente per le unità pubblicitarie Page Grabber, Expandable Adhesion e Screen Shift. È necessario ricertificarlo, con passaggi contrassegnati per i processi. |
| [!DNL Vox] | | | X | | [!DNL Athena] unità annuncio |
| [!DNL Wunderkind] | | X | | | |

{style="table-layout:auto"}
