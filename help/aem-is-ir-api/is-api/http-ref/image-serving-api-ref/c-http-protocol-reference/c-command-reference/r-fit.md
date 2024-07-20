---
title: fit
description: Antwortbild-Fit-Modus. Gibt an, wie der Skalierungsfaktor berechnet wird, der verwendet wird, um das zusammengesetzte Bild auf das Antwortbild zu skalieren, wenn die Antwortgröße mit wid= und hei= und scl= angegeben ist.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d2939f86-5dab-471d-ba59-70d91ae1e4fd
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '490'
ht-degree: 1%

---

# fit{#fit}

Antwortbild-Fit-Modus. Gibt an, wie der Skalierungsfaktor berechnet wird, der verwendet wird, um das zusammengesetzte Bild auf das Antwortbild zu skalieren, wenn die Antwortgröße mit wid= und hei= und scl= angegeben ist.

` fit= *`mode`*, *`upscale`*`

<table id="simpletable_50FBDC6B7CB2448891DD0F491DEB5ACF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> mode </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> fit|constrain|crop|wrap|gestreckch|hfit|vfit </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> upscale </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
 </tr> 
</table>

In der folgenden Beschreibung der Modusoptionen wird davon ausgegangen, dass *`xScale`* das Verhältnis zwischen der Breite des zusammengesetzten Bildes und der Breite des Antwortbilds und *`yScale`* das Verhältnis der Höhe des zusammengesetzten Bildes zur Höhe des Antwortbilds ist.

<table id="table_33408ECA9D164AFAA249F8589060545E"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Parameter </th> 
   <th colname="col2" class="entry"> Definition </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> fit </span> </p> </td> 
   <td colname="col2"> <p>Skaliert das zusammengesetzte Bild so, dass es in den mit <span class="codeph"> wid= </span> und <span class="codeph"> hei= </span> zugewiesenen Platz passt, wobei nur minimale Leerzeichen und kein Zuschneiden vorhanden sind. Das Antwortbild hat die exakte Größe, die mit <span class="codeph"> wid= </span> und <span class="codeph"> hei= </span> angegeben ist. Der kleinere Wert von <span class="varname"> xScale </span> und <span class="varname"> yScale </span> wird angewendet. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> constrain </span> </p> </td> 
   <td colname="col2"> <p>Skaliert das zusammengesetzte Bild wie <span class="codeph"> fit </span>, sodass es in den mit <span class="codeph"> wid= </span> und <span class="codeph"> hei= </span> zugewiesenen Platz passt, das tatsächliche Antwortbild jedoch kleiner sein kann als mit <span class="codeph"> wid= </span> und <span class="codeph"> hei= </span> angegeben, um Leerzeichen zu vermeiden. Der kleinere Wert von <span class="varname"> xScale </span> und <span class="varname"> yScale </span> wird angewendet. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> Zuschneiden </span> </p> </td> 
   <td colname="col2"> <p>Skaliert das zusammengesetzte Bild so, dass es das gesamte Antwortbild mit minimalem Zuschnitt und ohne Leerzeichen füllt. Der größere Wert von <span class="varname"> xScale </span> und <span class="varname"> yScale </span> wird angewendet. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> wrap </span> </p> </td> 
   <td colname="col2"> <p>Skaliert das zusammengesetzte Bild wie <span class="codeph"> Zuschneiden </span>, sodass es das gesamte Antwortbild abdeckt, das tatsächliche Antwortbild jedoch größer sein kann als mit <span class="codeph"> wid= </span> und <span class="codeph"> hei= </span> angegeben, um Zuschnitte zu vermeiden. Der größere Wert von <span class="varname"> xScale </span> und <span class="varname"> yScale </span> wird angewendet. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> gestreckt </span> </p> </td> 
   <td colname="col2"> <p>Skaliert das zusammengesetzte Bild unabhängig in x und y, um das gesamte Antwortbild ohne Zuschneiden und ohne Leerzeichen zu füllen. Dadurch wird normalerweise das Seitenverhältnis des Bildes geändert. <span class="varname"> xScale </span> wird für die horizontale Skalierung und <span class="varname"> yScale </span> für die vertikale Skalierung verwendet. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> hfit </span> </p> </td> 
   <td colname="col2"> <p>Wendet <span class="varname"> xScale </span> an, um das Bild horizontal anzupassen, wobei sich wahrscheinlich der Zuschnitt oder der Leerraum oben und/oder unten befindet. Nützlich für spezielle Anwendungen. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> vfit </span> </p> </td> 
   <td colname="col2"> <p>Wendet <span class="varname"> yScale </span> an, um das Bild vertikal anzupassen, wobei sich wahrscheinlich der Zuschnitt oder der Leerraum links und/oder rechts befindet. Nützlich für spezielle Anwendungen. </p> </td> 
  </tr> 
 </tbody> 
</table>

Setzen Sie *`upscale`* auf &quot;1&quot;, um die Upskalierung zuzulassen, oder auf &quot;0&quot;, um die *`xScale`*und *`yScale`* auf 1:1 zu beschränken. Wenn die Upskalierung deaktiviert ist, kann es zu zusätzlichen Leerzeichen kommen, wenn das zusammengesetzte Bild kleiner als das Antwortbild ist.

Zuschnitt und Leerzeichen werden standardmäßig zentriert; ihre Position kann mit `align=` gesteuert werden. Die Farbe und Deckkraft der Whitespace-Füllung wird durch `bgc=` bestimmt.

## Eigenschaften {#section-6d7a5a7e18434bca9bc2fdb236af8909}

Attribut anzeigen. Gilt unabhängig von der aktuellen Ebeneneinstellung. Mindestens einer von `wid=` oder `hei=` muss ebenfalls angegeben werden, andernfalls wird ein Fehler zurückgegeben. Sowohl `wid=` als auch `hei=` müssen angegeben werden, damit sich die Anpassungsmodi wie beschrieben verhalten. Wenn auch `req=tmb` angegeben ist, wird ein Fehler zurückgegeben.

## Standard {#section-3a553b4b29ef447a8331d6954f3f06da}

`fit=fit,0`

## Verwandte Themen {#section-788f7e168da64fc5abf29d971a598b01}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) , [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96), [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc), [align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7)
