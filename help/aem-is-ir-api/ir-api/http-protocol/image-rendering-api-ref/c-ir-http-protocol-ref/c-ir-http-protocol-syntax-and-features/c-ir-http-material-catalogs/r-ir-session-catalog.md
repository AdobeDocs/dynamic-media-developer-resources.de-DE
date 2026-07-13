---
title: Sitzungskatalog
description: Der Sitzungskatalog ist der Materialkatalog, der Sitzungsattribute für die Anfrage sowie einen Standard-catId-Wert für alle Befehle src=, vignette= und icc= bereitstellt.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 36e0571e-7451-423f-a1df-540680381902
TQID: 'https://experienceleague.adobe.com/--3F69i8XdliFxf5IhMPbUThRzMNyIDjtW4-Y-SBCFE'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4339f336345d7d7f3c05c7f5a18fbd28bcfd382b
workflow-type: tm+mt
source-wordcount: 235
ht-degree: 0%

---

# Sitzungskatalog{#session-catalog}

Der Sitzungskatalog ist der Materialkatalog, der Sitzungsattribute für die Anfrage sowie einen Standard-catId-Wert für alle `src=`-, `vignette=`- und `icc=` bereitstellt.

Der Sitzungskatalog wird als erstes Pfadelement des HTTP-Anfragepfads (unmittelbar nach dem Servernamen) angegeben. Wenn das erste Pfadelement nicht mit dem Attribut::rootId eines Katalogs übereinstimmt, wird der Standardkatalog als Sitzungskatalog verwendet.

Der Sitzungskatalog stellt die folgenden Sitzungsstandardwerte bereit:

<table id="table_DB5E0DD8E9B440A4964A1326433597C8"> 
 <thead> 
  <tr> 
   <th class="entry"> <p>Attribut </p> </th> 
   <th class="entry"> <p>Anmerkungen </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph">::RootPath</span> </p> </td> 
   <td> <p> Stammverzeichnis der Materialdatendateien </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">::VignettePath</span> </p> </td> 
   <td> <p> Stammverzeichnis der Vignettendateien </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">::IccProfileRgb</span> </p> </td> 
   <td> <p> Standardarbeitsfarbraum, wenn in eine Vignette kein ICC-Profil eingebettet ist </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">::RootUrl</span> </p> </td> 
   <td> <p> Stamm-URL für relative HTTP-Dateipfade in <span class="codeph"> Befehlen src=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">::ShowOverlapObjs</span> </p> </td> 
   <td> <p> Anfangs-Einblendungs-/Ausblendungsstatus für Überlappungsobjekte </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">::Expiration</span> </p> </td> 
   <td> <p> Wert für „Time-to-Live“ des Antwortbildes für Proxy-Server- und Browser-Caches </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">::MaxPix</span> </p> </td> 
   <td> <p> Die maximal zulässige Breite und Höhe des Antwortbildes </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">::DefaultPix</span> </p> </td> 
   <td> <p> Standardwerte für <span class="codeph"> wid=</span> und <span class="codeph"> hei=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">::Format</span> </p> </td> 
   <td> <p> Standardwert für <span class="codeph"> fmt=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">::JpegQuality</span> </p> </td> 
   <td> <p> Standardwert für <span class="codeph"> qlt=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">-Attribut::TiffEncoding</span> </p> </td> 
   <td> <p> Komprimierungstyp für die TIFF-Bildausgabe </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">::Sharpen</span> </p> </td> 
   <td> <p> Standardwert für <span class="codeph"> Scharfzeichnung=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">::OnFailSel</span> </p> </td> 
   <td> <p> Gibt das Verhalten an, wenn ein <span class="codeph"> Befehl sel=</span> fehlschlägt </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">::OnFailObj</span> </p> </td> 
   <td> <p> Gibt das Verhalten an, wenn ein <span class="codeph"> obj=</span>-Befehl fehlschlägt </p> </td> 
  </tr> 
 </tbody> 
</table>

