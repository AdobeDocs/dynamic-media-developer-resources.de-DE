---
description: PDF-Auftragsoptionen anwenden Eine Auftragsoptionendatei oder PDF-Vorgabe ist eine Datei, die von Illustrator im Dialogfeld "PDF-Optionen speichern"oder in den PDF-Vorgaben in InDesign generiert wird.
solution: Experience Manager
title: joboption
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '236'
ht-degree: 46%

---


# joboption{#joboption}

PDF-Auftragsoptionen anwenden Eine Auftragsoptionendatei oder PDF-Vorgabe ist eine Datei, die von Illustrator im Dialogfeld &quot;PDF-Optionen speichern&quot;oder in den PDF-Vorgaben in InDesign generiert wird.

` joboption= *`Wert`*`

<table id="simpletable_BA7B58BE0B0740298D45DDEBE7832D93"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> value</span></span> </p> </td> 
  <td class="stentry"> <p>Die IPSID der Auftragsoptionendatei. </p></td> 
 </tr> 
</table>

Die Auftragsoptionendatei kann von IPS/Dynamic Media Classic hochgeladen und veröffentlicht werden. Die in der Auftragsoptionendatei enthaltenen PDF-Optionen werden beim Generieren der PDF-Datei verwendet.

Die folgenden Optionen werden derzeit unterstützt:

<table id="simpletable_7E0AE8A06AE54A02AF0107FBEDF73D61"> 
 <tr class="strow"> 
  <td class="stentry"> <p>Allgemein </p></td> 
  <td class="stentry"> <p> Kompatibilität </p> <p> Komprimierung auf Objektebene </p> <p> Miniaturansichten einbetten </p> <p> Für schnelle Webansicht optimieren </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Bilder </p></td> 
  <td class="stentry"> <p> Downsampling, Auflösung, Schwellenwert und Komprimierung für Farbe, Grau und Mono </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Schriftarten </p></td> 
  <td class="stentry"> <p> Alle Schriften einbetten </p> <p> OpenType-Schriftarten einbetten </p> <p> Subset-Schriften, wenn Prozentsatz der Zeichen kleiner ist als: </p> <p> Liste immer einbetten </p> <p> Liste niemals einbetten </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Farbe </p></td> 
  <td class="stentry"> <p> Farbstrategie („Nur Bilder für Farbmanagement kennzeichnen“ wird wie „Alles für Farbmanagement kennzeichnen“ behandelt) </p> <p> Dokument-Renderpriorität </p> <p> Nur die folgenden Arbeitsfarbräume werden für 4.2.5 unterstützt. </p> <p> 
    <ul id="ul_3F3EFDFB6A3340978AE31DEDF0FDA2C8"> 
     <li id="li_17A9FA99D6CA4C5182E383A85F0E3C90"> RGB <p> 
       <ul id="ul_1DD0C264DA1248319E751ADD18140C6D"> 
        <li id="li_B91B4D0C1D80442EB8690933AFA1F093"> e-sRGB </li> 
        <li id="li_D7F8C500DF5E4CBC8FFA4FEFB8E4E036"> scRGB mit Codierungsbereich [-4.0, 4.0] </li> 
        <li id="li_942CD69732984E16A71C2F75EC5B5245"> Lab D50 </li> 
        <li id="li_7063B9E98D1E4946AC8F0EF7BC988806"> PCS XYZ </li> 
        <li id="li_5809447576B147B68630C4B7EC2E7870"> Flat XYZ </li> 
        <li id="li_3B5DA42A04124A6BAA12343AFC19F620">Linear ROMM-RGB </li> 
        <li id="li_DEC3028FA9C34176B761D12B7179B44F">ROMM-RGB </li> 
        <li id="li_3E7E7C4A680C4E3EADE0A26048ECF1F4"> sYCC 8-Bit </li> 
        <li id="li_16A615C9A74D443AB3C63B3FE3AB5443"> e-sYCC 8-Bit </li> 
       </ul> </p> </li> 
     <li id="li_AFA6D4D8C0624AA495E2EB2F0F0C7F7B">Grau <p> 
       <ul id="ul_945389DD426F44C09EB9C7F23933CB77"> 
        <li id="li_DB0AE3DFFC184480BB91666FF1BB4776">Grau Gamma 1.8 </li> 
        <li id="li_755C556ED94740D1BD30EBE67018E074">Grau Gamma 2.2 </li> 
        <li id="li_67437440AFB54B7686333A55233AA87F">Tonwertzuwachs 10% </li> 
        <li id="li_0D6CA6004EC84048B5F2198406F4F343">Tonwertzuwachs 15% </li> 
        <li id="li_1AFD11C23AB147978559D8F00BFB3142">Tonwertzuwachs 20% </li> 
        <li id="li_6CD5ACEF6B0B49E8BACA8264FE0E9C44"> Tonwertzuwachs 25% </li> 
        <li id="li_AB5F1FA7111041BD82353E02A284A546">Tonwertzuwachs 30% </li> 
        <li id="li_7433278AE8054AD28BD38A0A6E4EF7EF"> sGray </li> 
       </ul> </p> </li> 
    </ul> </p> <p> CMYK-Werte für kalibrierte CMYK-Farbräume beibehalten </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Erweitert </p></td> 
  <td class="stentry"> <p>„OPI-Kommentare beibehalten“ ist immer aktiviert. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Standards </p></td> 
  <td class="stentry"> <p>Kompatibilitätsstandard. </p></td> 
 </tr> 
</table>

