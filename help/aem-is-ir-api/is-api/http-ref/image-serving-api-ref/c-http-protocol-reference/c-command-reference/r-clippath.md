---
description: Pfad des Ebenenclips. Gibt einen Clip-Pfad für die aktuelle Ebene an.
seo-description: Pfad des Ebenenclips. Gibt einen Clip-Pfad für die aktuelle Ebene an.
seo-title: clipPath
solution: Experience Manager
title: clipPath
topic: Scene7 Image Serving - Image Rendering API
uuid: fe84cf7a-63af-47d3-ae4f-2122f2f0a262
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '556'
ht-degree: 1%

---


# clipPath{#clippath}

Pfad des Ebenenclips. Gibt einen Clip-Pfad für die aktuelle Ebene an.

`clipPath= *`pathDefinition`*`

`clipPathE= *``*&#42;[, *`pathNamepathName`*]`

<table id="simpletable_275E2A5FAB804C6388BD110D2ACA3C82"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pathDefinition</span> </span> </p> </td> 
  <td class="stentry"> <p>Path data. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pathName</span></span> </p> </td> 
  <td class="stentry"> <p>Name des Pfads, der in das Ebenenquellbild eingebettet ist (nur ASCII). </p></td> 
 </tr> 
</table>

Alle Teile der Ebene, die außerhalb des durch `clipPath=` definierten Bereichs liegen, werden transparent dargestellt.

` *``*` pathNames ist der Name eines Pfads, der im Quellbild der Ebene eingebettet ist. Der Pfad wird automatisch transformiert, um die relative Ausrichtung am Bildinhalt beizubehalten. Wenn mehr als ein ` *`pathName`*` angegeben ist, beschneidet der Server das Bild an den Schnittpunkt dieser Pfade. Alle ` *`pathName`*`, die nicht im Quellbild gefunden wurden, werden ignoriert.

>[!NOTE]
>
>Für ` *`pathName`*` werden nur ASCII-Zeichenfolgen unterstützt.

` *`Mit `*` pathDefinition können explizite Pfaddaten in Pixel-Koordinaten der Ebene angegeben werden.

Wenn `size=` angegeben ist und nicht 0,0, wird die Ebene vorab skaliert. In diesem Fall sind die Pfadkoordinaten relativ zur oberen linken Ecke des Ebenenrechtecks und die Ebene wird basierend auf `origin=` oder deren Standard positioniert. Sämtliche Bereiche des Pfades außerhalb des Rechtecks der Ebene bleiben transparent.

Wenn `size=` nicht für eine Volltonfarbe oder Textebene angegeben ist, wird die Ebene als selbstformatierend betrachtet, wobei die Größe des Pfades bestimmt wird. Wenn `origin=` nicht angegeben ist, wird standardmäßig (0,0) des Pfadkoordinatenraums verwendet. Auf diese Weise können Pfadkoordinaten relativ zur Herkunft der Ebene 0 angegeben werden.

>[!NOTE]
>
>`scale=`,  `rotate=`und  `anchor=` Befehle sind nicht zulässig, um Farbflächenebenen selbst zu skalieren.

` *``*` pathDefinitionakzeptiert eine Zeichenfolge, die dem Wert des  `d=` Attributs des SVG- `<path>` Elements ähnlich ist, mit der Ausnahme, dass zur Trennung von Werten Kommas anstelle von Leerzeichen verwendet werden. ` *``*` pathDefinition kann einen oder mehrere Unterpfade mit geschlossener Schleife enthalten.

Die folgenden Pfadbefehle werden in ` *`pathDefinition`*` unterstützt:

<table id="table_A74DD7A48B1C417D9D4BA46BECEAB981"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> Befehl</b> </th> 
   <th class="entry"> <b> Name</b> </th> 
   <th class="entry"> <b> Beschreibung</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td> <b> </b> <span class="varname"> Mx,y</span> </td> 
   <td> <p> moveto absolut </p> </td> 
   <td> <p> Beginn eines neuen Unterpfads bei x,y. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> </b> <span class="varname"> mx,y</span> </td> 
   <td> <p> moveto relative </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> L</b> *{<span class="varname"> x,y</span>} </td> 
   <td> <p> linear to absolute </p> </td> 
   <td> <p> Zeichnen Sie eine Linie von der aktuellen Position zu x,y. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> l</b> *{<span class="varname"> x,y</span>} </td> 
   <td> <p> linear relativ </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> C</b> *{<span class="varname"> x1,y1,x2,y2,x,y</span>} </td> 
   <td> <p> curveto absolut </p> </td> 
   <td> <p> Zeichnen Sie eine Bézier-Kurve von der aktuellen Position zu x,y. x1,y1 ist der Kontrollpunkt am Anfang der Kurve und x2,y2 ist der Kontrollpunkt am Ende der Kurve. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> c</b> *{<span class="varname"> x1,y1,x2,y2,x,y</span>} </td> 
   <td> <p> curveto relative </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> Z</b> |  <b>z</b> </td> 
   <td> <p> closepath </p> </td> 
   <td> <p> Schließen Sie den aktuellen Unterpfad mit einer geraden Linie. </p> </td> 
  </tr> 
 </tbody> 
</table>

Großbuchstaben-Befehle geben an, dass die Koordinatenwerte in absoluten Pixelpositionen stehen (relativ zur oberen linken Ecke des Ebenenrechtecks). Pixel-Offsets folgen kleinen Befehlen relativ zur aktuellen Position.

&#39;m&#39; oder &#39;M&#39; Beginn immer einen neuen Unterpfad. Unterpfade werden automatisch geschlossen (mit gerader Linie), wenn am Ende nicht &quot;Z&quot;oder &quot;z&quot;angegeben ist.

Wenn ein Unterpfad mit einer relativen Umschalt (&#39;m&#39;) beginnt, ist er relativ zu einem der folgenden:

* Der Startpunkt des vorherigen Unterpfads, wenn er mit &#39;z&#39; oder &#39;Z&#39; geschlossen wurde.
* Der Endpunkt des vorherigen Unterpfads, wenn er nicht explizit geschlossen wurde.
* 0,0, wenn dies der erste Unterpfad ist.

## Eigenschaften {#section-d4127db0dac54e3cbd44f7ea1e001960}

Ebenenattribut. Gilt für die aktuelle Ebene oder für das Composite-Bild, wenn `layer=comp`. Effektebenen ignorieren dies.

`clipPathE=` wird ignoriert, wenn im Quellbild der Ebene kein Pfad mit dem angegebenen Namen gefunden wird oder wenn die Ebenenquelle kein Bild ist.

## Standard {#section-076c35ea37fa4a44ada253b4c2dec1dd}

Ohne, damit die Ebene nicht weiter beschnitten wird.

## Verwandte Themen {#section-dd8110fb6f5c45eba6284c5ec5f49056}

[clipXpath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clipxpath.md#reference-17e5e4da3e044943af8f963f58a45f53) ,  [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef) ,  [extended=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)
