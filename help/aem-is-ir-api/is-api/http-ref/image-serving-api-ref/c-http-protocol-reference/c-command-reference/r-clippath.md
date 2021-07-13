---
description: Ebenenbeschneidungspfad. Gibt einen Clip-Pfad für die aktuelle Ebene an.
solution: Experience Manager
title: clipPath
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 86c87cd1-6e08-40cb-80e6-35a9f49b6572
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '549'
ht-degree: 1%

---

# clipPath{#clippath}

Ebenenbeschneidungspfad. Gibt einen Clip-Pfad für die aktuelle Ebene an.

`clipPath= *`pathDefinition`*`

`clipPathE= *``*&#42;[, *`pathNamepathName`*]`

<table id="simpletable_275E2A5FAB804C6388BD110D2ACA3C82"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pathDefinition</span> </span> </p> </td> 
  <td class="stentry"> <p>Path data. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pathName</span></span> </p> </td> 
  <td class="stentry"> <p>Name des Pfades, der in das Ebenenquellbild eingebettet ist (nur ASCII). </p></td> 
 </tr> 
</table>

Alle Teile der Ebene, die außerhalb des von `clipPath=` definierten Bereichs liegen, werden transparent dargestellt.

`*``*` pathNames ist der Name eines Pfades, der in das Ebenenquellbild eingebettet ist. Der Pfad wird automatisch umgewandelt, um die relative Ausrichtung an den Bildinhalten zu gewährleisten. Wenn mehr als ein `*`pathName`*` angegeben ist, schneidet der Server das Bild an die Schnittmenge dieser Pfade. Alle `*`pathName`*`, die nicht im Quellbild gefunden werden, werden ignoriert.

>[!NOTE]
>
>Für `*`pathName`*` werden nur ASCII-Zeichenfolgen unterstützt.

`*``*` pathDefinitionermöglicht die Angabe expliziter Pfaddaten in Ebenenpixelkoordinaten.

Wenn `size=` und nicht 0,0 angegeben ist, wird die Ebene vorskaliert. In diesem Fall beziehen sich die Pfadkoordinaten auf die obere linke Ecke des Ebenenrechtecks und die Ebene wird basierend auf `origin=` oder ihrer Standardeinstellung positioniert. Alle Bereiche des Pfads außerhalb des Ebenenrechtecks bleiben transparent.

Wenn `size=` nicht für eine durchgehende Farbe oder Textebene angegeben ist, wird die Ebene als eigenständig skaliert betrachtet, wobei der Umfang des Pfads dessen Größe bestimmt. Wenn `origin=` nicht angegeben ist, wird standardmäßig der Pfad-Koordinatenraum (0,0) verwendet. Auf diese Weise können Pfadkoordinaten relativ zum Ursprung der Ebene 0 angegeben werden.

>[!NOTE]
>
>`scale=`,  `rotate=`und  `anchor=` Befehle sind nicht für die Selbstdimensionierung von Farbschichten zulässig.

`*``*` pathDefinitionakzeptiert eine Zeichenfolge, die dem Wert des  `d=` Attributs des SVG- `<path>` Elements ähnelt, mit der Ausnahme, dass Kommas anstelle von Leerzeichen verwendet werden, um Werte zu trennen. `*``*` pathDefinition kann einen oder mehrere geschlossene Schleifenunterpfade enthalten.

Die folgenden Pfadbefehle werden in `*`pathDefinition`*` unterstützt:

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
   <td> <p> Starten Sie einen neuen Unterpfad bei x,y. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> </b> <span class="varname"> mx,y</span> </td> 
   <td> <p> Verschieben relativ </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> L</b> *{<span class="varname"> x,y</span>} </td> 
   <td> <p> linear zu absolut </p> </td> 
   <td> <p> Zeichnen Sie eine Linie von der aktuellen Position auf x,y. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> l</b> *{<span class="varname"> x,y</span>} </td> 
   <td> <p> linear to relative </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> C</b> *{<span class="varname"> x1,y1,x2,y2,x,y</span>} </td> 
   <td> <p> curveto absolut </p> </td> 
   <td> <p> Zeichnen Sie eine Bézier-Kurve von der aktuellen Position auf x,y. x1,y1 ist der Kontrollpunkt am Anfang der Kurve und x2,y2 der Kontrollpunkt am Ende der Kurve. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> c</b> *{<span class="varname"> x1,y1,x2,y2,x,y</span>} </td> 
   <td> <p> curveto relativ </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> Z</b> |  <b>z</b> </td> 
   <td> <p> closepath </p> </td> 
   <td> <p> Schließen Sie den aktuellen Unterpfad mit einer geraden Linie. </p> </td> 
  </tr> 
 </tbody> 
</table>

Großbuchstaben-Befehle weisen darauf hin, dass die Koordinatenwerte in absoluten Pixelpositionen liegen (relativ zum linken oberen Rand des Ebenenrechtecks). Pixel-Offsets folgen kleingeschriebenen Befehlen relativ zur aktuellen Position.

&quot;m&quot;oder &quot;M&quot;startet immer einen neuen Unterpfad. Unterpfade werden automatisch geschlossen (mit gerader Linie), wenn &quot;Z&quot;oder &quot;z&quot;am Ende nicht angegeben ist.

Wenn ein Unterpfad mit einer relativen Verschiebung (&#39;m&#39;) beginnt, ist er relativ zu einem der folgenden Werte:

* Der Ausgangspunkt des vorherigen Unterpfads, wenn er mit &quot;z&quot;oder &quot;Z&quot;geschlossen wurde.
* Der Endpunkt des vorherigen Unterpfads, wenn er nicht explizit geschlossen wurde.
* 0,0, wenn dies der erste Unterpfad ist.

## Eigenschaften {#section-d4127db0dac54e3cbd44f7ea1e001960}

Ebenenattribut. Gilt für die aktuelle Ebene oder für das zusammengesetzte Bild, wenn `layer=comp` Effektebenen ignorieren dies.

`clipPathE=` wird ignoriert, wenn kein Pfad mit dem angegebenen Namen im Ebenenquellenbild gefunden wird oder wenn die Ebenenquelle kein Bild ist.

## Standard {#section-076c35ea37fa4a44ada253b4c2dec1dd}

Keine, kein zusätzliches Beschneiden der Ebene.

## Verwandte Themen {#section-dd8110fb6f5c45eba6284c5ec5f49056}

[clipXpath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clipxpath.md#reference-17e5e4da3e044943af8f963f58a45f53) ,  [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef) ,  [extend=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)
