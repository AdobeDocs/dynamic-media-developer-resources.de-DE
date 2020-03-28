---
description: Antwortbild-Anpassungsmodus. Gibt an, wie der Skalierungsfaktor berechnet wird, mit dem das Composite-Bild auf das Antwortbild skaliert wird, wenn die Antwortgröße mit wid= und hei= und scl= angegeben ist.
seo-description: Antwortbild-Anpassungsmodus. Gibt an, wie der Skalierungsfaktor berechnet wird, mit dem das Composite-Bild auf das Antwortbild skaliert wird, wenn die Antwortgröße mit wid= und hei= und scl= angegeben ist.
seo-title: anpassen
solution: Experience Manager
title: anpassen
topic: Scene7 Image Serving - Image Rendering API
uuid: 669fe757-f3a1-4cd4-b46c-6fbe5a039ce0
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# anpassen{#fit}

Antwortbild-Anpassungsmodus. Gibt an, wie der Skalierungsfaktor berechnet wird, mit dem das Composite-Bild auf das Antwortbild skaliert wird, wenn die Antwortgröße mit wid= und hei= und scl= angegeben ist.

` fit= *``*, *`modeupscale`*`

<table id="simpletable_50FBDC6B7CB2448891DD0F491DEB5ACF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> Modus </span></span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> fit|constrain|cut|wrap|strecken|fit|vfit </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> upscale </span></span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
 </tr> 
</table>

In der folgenden Beschreibung der Modusoptionen wird davon ausgegangen, dass dies das Verhältnis der Breite des Composite-Bilds zur Breite des Antwortbilds und das Verhältnis der Höhe des Composite-Bilds zur Höhe des Antwortbilds *`xScale`* *`yScale`* ist.

<table id="table_33408ECA9D164AFAA249F8589060545E"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Parameter </th> 
   <th colname="col2" class="entry"> Definition </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> anpassen </span> </p> </td> 
   <td colname="col2"> <p>Skaliert das Composite-Bild so, dass es in den Raum passt, der mit <span class="codeph"> wid= </span> und <span class="codeph"> hei= </span>, mit minimalem Whitespace und ohne Beschneiden. Das Antwortbild hat die exakte Größe mit <span class="codeph"> wid= </span> und <span class="codeph"> hei= </span>. Es wird der kleinere Wert von <span class="varname"> xScale </span> und <span class="varname"> yScale angewendet </span> . </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> einschränken </span> </p> </td> 
   <td colname="col2"> <p>Skaliert das Composite-Bild wie <span class="codeph"> passen, </span> sodass es in den mit <span class="codeph"> wid= </span> und <span class="codeph"> hei= </span>zugewiesenen Raum passt, aber das tatsächliche Antwortbild kann kleiner sein als mit <span class="codeph"> wid= </span> und <span class="codeph"> </span> hei= angegeben, um Leerzeichen zu vermeiden. Es wird der kleinere Wert von <span class="varname"> xScale </span> und <span class="varname"> yScale angewendet </span> . </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> Zuschneiden </span> </p> </td> 
   <td colname="col2"> <p>Skaliert das Composite-Bild so, dass es das gesamte Antwortbild mit minimalem Beschneiden und ohne Leerzeichen füllt. Es wird die größere von <span class="varname"> xScale </span> und <span class="varname"> yScale angewendet </span> . </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> umbruch </span> </p> </td> 
   <td colname="col2"> <p>Skaliert das Composite-Bild wie <span class="codeph"> Zuschneiden, </span> sodass es das gesamte Antwortbild abdeckt, aber das tatsächliche Antwortbild kann größer sein als mit <span class="codeph"> wid= </span> und <span class="codeph"> </span> hei= angegeben, um das Zuschneiden zu vermeiden. Es wird die größere von <span class="varname"> xScale </span> und <span class="varname"> yScale angewendet </span>werden. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> strecken </span> </p> </td> 
   <td colname="col2"> <p>Skaliert das Composite-Bild unabhängig in x und y, um das gesamte Antwortbild ohne Beschneiden und ohne Leerzeichen zu füllen. Dadurch wird normalerweise das Seitenverhältnis des Bildes geändert. <span class="varname"> xScale </span> wird für die horizontale Skalierung und <span class="varname"> yScale </span> für die vertikale Skalierung verwendet. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> hfit </span> </p> </td> 
   <td colname="col2"> <p>Wendet <span class="varname"> xScale </span> an, um das Bild horizontal anzupassen, wobei sich der Zuschnitt oder Whitespace wahrscheinlich am oberen und/oder unteren Rand befinden. Nützlich für spezielle Anwendungen. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> vfit </span> </p> </td> 
   <td colname="col2"> <p>Wendet <span class="varname"> yScale </span> an, um das Bild vertikal anzupassen, wobei sich der Bereich wahrscheinlich links und/oder rechts befindet. Nützlich für spezielle Anwendungen. </p> </td> 
  </tr> 
 </tbody> 
</table>

Setzen Sie *`upscale`* auf &#39;1&#39;, um Upscaling zuzulassen, oder auf &#39;0&#39;, um *`xScale`*und auf 1:1 zu beschränken *`yScale`* . Wenn die Skalierung deaktiviert ist, kann es zu zusätzlichen Leerzeichen kommen, wenn das Composite-Bild kleiner als das Antwortbild ist.

Zuschneiden und Leerzeichen werden standardmäßig zentriert. ihre Position kann mit kontrolliert werden `align=`. Die Farbe und Deckkraft der Füllung von Leerzeichen wird durch `bgc=`festgelegt.

## Eigenschaften {#section-6d7a5a7e18434bca9bc2fdb236af8909}

Ansicht. Gilt unabhängig von der aktuellen Ebeneneinstellung. Es muss mindestens ein `wid=` oder `hei=` ein Fehler angegeben werden, andernfalls wird ein Fehler zurückgegeben. sowohl `wid=` als auch `hei=` müssen angegeben werden, damit sich die Anpassungsmodi wie beschrieben verhalten. Ein Fehler wird zurückgegeben, wenn `req=tmb` auch angegeben wird.

## Standard {#section-3a553b4b29ef447a8331d6954f3f06da}

`fit=fit,0`

## Verwandte Themen {#section-788f7e168da64fc5abf29d971a598b01}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) , [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96), [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc), [align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7)
