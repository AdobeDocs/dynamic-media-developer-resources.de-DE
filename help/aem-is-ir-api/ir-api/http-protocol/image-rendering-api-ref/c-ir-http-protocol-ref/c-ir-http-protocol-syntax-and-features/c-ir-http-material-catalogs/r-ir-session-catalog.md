---
title: Sitzungskatalog
description: Der Sitzungskatalog ist der Materialkatalog, der Sitzungsattribute für die Anforderung und einen standardmäßigen catId-Wert für alle Befehle src=, vignette= und icc= bereitstellt.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 36e0571e-7451-423f-a1df-540680381902
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 0%

---

# Sitzungskatalog{#session-catalog}

Der Sitzungskatalog ist der Materialkatalog, der Sitzungsattribute für die Anfrage und einen standardmäßigen catId-Wert für alle Befehle `src=`, `vignette=` und `icc=` bereitstellt.

Der Sitzungskatalog wird als erstes Pfadelement des HTTP-Anfragepfads angegeben (unmittelbar nach dem Servernamen). Wenn das erste Pfadelement nicht mit attribute::RootId eines beliebigen Katalogs übereinstimmt, wird der Standardkatalog als Sitzungskatalog verwendet.

Der Sitzungskatalog enthält die folgenden Sitzungsstandardwerte:

<table id="table_DB5E0DD8E9B440A4964A1326433597C8"> 
 <thead> 
  <tr> 
   <th class="entry"> <p>Attribut </p> </th> 
   <th class="entry"> <p>Anmerkungen </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::RootPath</span> </p> </td> 
   <td> <p> Stammpfad für Materialdatendateien </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::VignettePath</span> </p> </td> 
   <td> <p> Stammpfad für Vignettendateien </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::IccProfileRgb</span> </p> </td> 
   <td> <p> Standardarbeitsfarbraum, wenn eine Vignette kein ICC-Profil einbettet </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::RootUrl</span> </p> </td> 
   <td> <p> Stamm-URL für relative HTTP-Dateipfade in <span class="codeph"> src=</span> Befehlen </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::ShowOverlapObjs</span> </p> </td> 
   <td> <p> Anfänglicher Einblenden/Ausblenden-Status für überlappende Objekte </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::Expiration</span> </p> </td> 
   <td> <p> Time-to-Live-Wert des Antwortbilds für Proxy-Server- und Browser-Caches </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::MaxPix</span> </p> </td> 
   <td> <p> Maximal zulässige Breite und Höhe des Antwortbilds </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::DefaultPix</span> </p> </td> 
   <td> <p> Standardwerte für <span class="codeph"> wid=</span> und <span class="codeph"> hei=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::Format</span> </p> </td> 
   <td> <p> Standardwert für <span class="codeph"> fmt=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::JpegQuality</span> </p> </td> 
   <td> <p> Standardwert für <span class="codeph"> qlt=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::TiffEncoding</span> </p> </td> 
   <td> <p> Komprimierungstyp für TIFF-Bildausgabe </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::Sharpen</span> </p> </td> 
   <td> <p> Standardwert für <span class="codeph"> sharpen=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::OnFailSel</span> </p> </td> 
   <td> <p> Gibt das Verhalten an, wenn ein Befehl <span class="codeph"> sel=</span> fehlschlägt </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::OnFailObj</span> </p> </td> 
   <td> <p> Gibt das Verhalten an, wenn ein Befehl <span class="codeph"> obj=</span> fehlschlägt </p> </td> 
  </tr> 
 </tbody> 
</table>
