---
description: Der Sitzungskatalog ist der Materialkatalog, der Sitzungsattribute für die Anforderung sowie einen standardmäßigen catId-Wert für alle Befehle src=, vignette= und icc= bereitstellt.
seo-description: Der Sitzungskatalog ist der Materialkatalog, der Sitzungsattribute für die Anforderung sowie einen standardmäßigen catId-Wert für alle Befehle src=, vignette= und icc= bereitstellt.
seo-title: Sitzungskatalog
solution: Experience Manager
title: Sitzungskatalog
topic: Scene7 Image Serving - Image Rendering API
uuid: 69c0f6cd-dfaf-47bf-bdd9-7abb4e6f7465
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Sitzungskatalog{#session-catalog}

Der Sitzungskatalog ist der Materialkatalog, der Sitzungsattribute für die Anforderung sowie einen standardmäßigen catId-Wert für alle Befehle src=, vignette= und icc= bereitstellt.

Der Sitzungskatalog wird als erstes Pfadelement des HTTP-Anforderungspfads (unmittelbar nach dem Servernamen) angegeben. Wenn das erste Pfadelement nicht mit attribute::RootId eines Katalogs übereinstimmt, wird der Standardkatalog als Sitzungskatalog verwendet.

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
   <td> <p> Standardarbeitsfarbraum, wenn keine Vignette ein ICC-Profil einbettet </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::RootUrl</span> </p> </td> 
   <td> <p> Stamm-URL für relative HTTP-Dateipfade in <span class="codeph"> src=</span> -Befehlen </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::ShowOverlapObjs</span> </p> </td> 
   <td> <p> Status "Anfänglich ein-/ausblenden"für überlappende Objekte </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::Expiration</span> </p> </td> 
   <td> <p> Time-to-live-Wert des Antwortbilds für Proxyserver- und Browser-Caches </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::MaxPix</span> </p> </td> 
   <td> <p> Die maximal zulässige Breite und Höhe des Antwortbilds </p> </td> 
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
   <td> <p> <span class="codeph"> attribute:Sharpen</span> </p> </td> 
   <td> <p> Standardwert für <span class="codeph"> sharpen=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::OnFailSel</span> </p> </td> 
   <td> <p> Gibt Verhalten an, wenn der Befehl <span class="codeph"> sel=</span> fehlschlägt </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::OnFailObj</span> </p> </td> 
   <td> <p> Gibt Verhalten an, wenn ein <span class="codeph"> Befehl "obj=</span> "fehlschlägt </p> </td> 
  </tr> 
 </tbody> 
</table>

