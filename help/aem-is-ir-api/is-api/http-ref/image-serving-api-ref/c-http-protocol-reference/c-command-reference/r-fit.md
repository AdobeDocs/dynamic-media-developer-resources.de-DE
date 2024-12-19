---
title: Anpassen
description: Anpassungsmodus des Antwortbildes. Gibt an, wie der Skalierungsfaktor berechnet wird. Dieser wird verwendet, um das zusammengesetzte Bild auf das Antwortbild zu skalieren, wenn die Antwortgröße mit wid= und hei= und scl= nicht vorhanden ist.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d2939f86-5dab-471d-ba59-70d91ae1e4fd
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '490'
ht-degree: 1%

---

# Anpassen{#fit}

Anpassungsmodus des Antwortbildes. Gibt an, wie der Skalierungsfaktor berechnet wird. Dieser wird verwendet, um das zusammengesetzte Bild auf das Antwortbild zu skalieren, wenn die Antwortgröße mit wid= und hei= und scl= nicht vorhanden ist.

` fit= *`mode`*, *`upscale`*`

<table id="simpletable_50FBDC6B7CB2448891DD0F491DEB5ACF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> Modus </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> Anpassen|Einschränken|Zuschneiden|Umbrechen|Dehnen|Hfit|Vfit </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> Upscale </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
 </tr> 
</table>

Bei der folgenden Beschreibung der Modusoptionen wird davon ausgegangen, dass *`xScale`* das Verhältnis der zusammengesetzten Bildbreite zur Antwortbildbreite und *`yScale`* das Verhältnis der zusammengesetzten Bildhöhe zur Antwortbildhöhe ist.

<table id="table_33408ECA9D164AFAA249F8589060545E"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Parameter </th> 
   <th colname="col2" class="entry"> Definition </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> Fit </span> </p> </td> 
   <td colname="col2"> <p>Skaliert das zusammengesetzte Bild so, dass es in den mit <span class="codeph"> wid= </span> und <span class="codeph"> hei= </span> belegten Raum passt, mit minimalem Leerraum und ohne Zuschneiden. Das Antwortbild hat die exakte Größe, die mit <span class="codeph"> wid= </span> und <span class="codeph"> hei= </span> angegeben wurde. Der kleinere von <span class="varname"> xScale-</span> und <span class="varname"> yScale-</span> wird angewendet. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> </span> <span class="codeph"> </p> </td> 
   <td colname="col2"> <p>Skaliert das zusammengesetzte Bild wie <span class="codeph"> Fit </span>, sodass es in den mit <span class="codeph"> wid= </span> und <span class="codeph"> hei= </span> belegten Raum passt, aber das tatsächliche Antwortbild kann kleiner sein als mit <span class="codeph"> wid= </span> und <span class="codeph"> hei= </span> angegeben, um Leerzeichen zu vermeiden. Der kleinere von <span class="varname"> xScale-</span> und <span class="varname"> yScale-</span> wird angewendet. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Skaliert das zusammengesetzte Bild, sodass es das gesamte Antwortbild ausfüllt, mit minimalem Zuschnitt und ohne Leerzeichen. Der größere Wert <span class="varname"> xScale-</span> und <span class="varname"> yScale-</span> wird angewendet. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> Wrap </span> </p> </td> 
   <td colname="col2"> <p>Skaliert das zusammengesetzte Bild wie <span class="codeph"> Beschneidungs-</span>, sodass es das gesamte Antwortbild abdeckt. Das tatsächliche Antwortbild kann jedoch größer sein als mit <span class="codeph"> wid= </span> und <span class="codeph"> hei= </span> angegeben, um ein Beschneiden zu vermeiden. Der größere <span class="varname"> xScale-</span> und <span class="varname"> yScale-</span> wird angewendet. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Skaliert das zusammengesetzte Bild unabhängig in x und y, um das gesamte Antwortbild auszufüllen, ohne Zuschnitt und ohne Leerzeichen. Dadurch wird normalerweise das Seitenverhältnis des Bildes geändert. <span class="varname"> xScale-</span> wird für die horizontale Skalierung und <span class="varname"> yScale-</span> für die vertikale Skalierung verwendet. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> HFIT </span> </p> </td> 
   <td colname="col2"> <p>Wendet <span class="varname"> xScale-</span> an, um das Bild horizontal genau anzupassen, mit wahrscheinlichem Zuschnitt oder Leerzeichen oben und/oder unten. Nützlich für spezielle Anwendungen. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> vfit </span> </p> </td> 
   <td colname="col2"> <p>Wendet <span class="varname"> yScale-</span> an, um das Bild vertikal genau anzupassen, mit wahrscheinlichem Zuschnitt oder Leerzeichen links und/oder rechts. Nützlich für spezielle Anwendungen. </p> </td> 
  </tr> 
 </tbody> 
</table>

*`upscale`* auf „1“ festgelegt, um eine Hochskalierung zu ermöglichen, oder auf „0“, um *`xScale`* zu beschränken, und *`yScale`* auf 1:1 beschränkt werden. Wenn Hochskalieren deaktiviert ist, können zusätzliche Leerzeichen vorhanden sein, wenn das zusammengesetzte Bild kleiner ist als das Antwortbild.

Zuschneiden und Leerzeichen sind standardmäßig zentriert. Ihre Position kann mit `align=` gesteuert werden. Farbe und Deckkraft der Leerraumfüllung werden durch `bgc=` bestimmt.

## Eigenschaften {#section-6d7a5a7e18434bca9bc2fdb236af8909}

Attribut anzeigen. Wird unabhängig von der aktuellen Ebeneneinstellung angewendet. Mindestens einer der Werte `wid=` oder `hei=` muss ebenfalls angegeben werden. Andernfalls wird ein Fehler zurückgegeben. `wid=` und `hei=` müssen angegeben werden, damit sich die Anpassungsmodi wie beschrieben verhalten. Ein Fehler wird zurückgegeben, wenn auch `req=tmb` angegeben wird.

## Standard {#section-3a553b4b29ef447a8331d6954f3f06da}

`fit=fit,0`

## Verwandte Themen {#section-788f7e168da64fc5abf29d971a598b01}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) , [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96), [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc), [align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7)
