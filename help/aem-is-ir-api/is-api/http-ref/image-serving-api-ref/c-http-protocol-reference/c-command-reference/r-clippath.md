---
title: clipPath
description: Layer-Clip-Pfad. Legt einen Clip-Pfad für die aktuelle Ebene fest.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 86c87cd1-6e08-40cb-80e6-35a9f49b6572
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '533'
ht-degree: 0%

---

# clipPath{#clippath}

Layer-Clip-Pfad. Legt einen Clip-Pfad für die aktuelle Ebene fest.

`clipPath= *`pathDefinition`*`

`clipPathE= *`pathName`*&#42;[, *`pathName`*]`

<table id="simpletable_275E2A5FAB804C6388BD110D2ACA3C82"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pathDefinition</span> </span> </p> </td> 
  <td class="stentry"> <p>Pfaddaten. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pathName</span></span> </p> </td> 
  <td class="stentry"> <p>Name des Pfads, der in das Ebenenquellbild eingebettet ist (nur ASCII). </p></td> 
 </tr> 
</table>

Alle Teile der Ebene, die außerhalb des durch `clipPath=` definierten Bereichs liegen, werden transparent dargestellt.

`*`pathName`*` ist der Name eines Pfads, der in das Ebenenquellbild eingebettet ist. Der Pfad wird automatisch transformiert, um die relative Ausrichtung mit dem Bildinhalt beizubehalten. Wenn mehr als ein `*`pathName`*` angegeben ist, schneidet der Server das Bild an die Schnittmenge dieser Pfade an. Alle `*`pathName`*`, die nicht im Quellbild gefunden wurden, werden ignoriert.

>[!NOTE]
>
>Für „pathName“ werden nur `*` ASCII-Zeichenfolgen `*`.

`*`pathDefinition`*` ermöglicht die Angabe expliziter Pfaddaten in Pixel-Koordinaten der Ebene.

Wenn `size=` und nicht 0,0 angegeben ist, wird die Ebene vorab skaliert. In diesem Fall sind die Pfadkoordinaten relativ zur linken oberen Ecke des Ebenenrechtecks, und die Ebene wird basierend auf `origin=` oder seiner Standardeinstellung positioniert. Alle Bereiche des Pfads außerhalb des Ebenenrechtecks bleiben transparent.

Wenn `size=` für eine Vollbild- oder Textebene nicht angegeben ist, wird die Ebene mit der Größe des Pfads als selbstskalierend betrachtet. Wenn `origin=` nicht angegeben ist, wird standardmäßig (0,0) des Pfad-Koordinatenraums verwendet. Dieser Workflow-Prozess ermöglicht effektiv die Angabe von Pfadkoordinaten relativ zum Ursprung von Ebene 0.

>[!NOTE]
>
>`scale=`-, `rotate=`- und `anchor=`-Befehle sind für einfarbige Ebenen mit automatischer Größenanpassung nicht zulässig.

`*`pathDefinition`*` akzeptiert eine Zeichenfolge, die dem Wert des `d=`-Attributs des SVG-`<path>` ähnelt, mit dem Unterschied, dass zum Trennen von Werten Kommas anstelle von Leerzeichen verwendet werden. `*`pathDefinition`*` kann einen oder mehrere Unterpfade in geschlossener Schleife enthalten.

Die folgenden Pfadbefehle werden in „pathDefinition`*` unterstützt`*`:

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
   <td> <b> M</b> <span class="varname"> x,y</span> </td> 
   <td> <p> In absolute Werte verschieben </p> </td> 
   <td> <p> Beginnen Sie einen neuen Unterpfad mit x,y. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> M</b> <span class="varname"> X,Y</span> </td> 
   <td> <p> MoveTo-Relativ </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> L</b> *{<span class="varname"> x,y</span>} </td> 
   <td> <p> lineto absolut </p> </td> 
   <td> <p> Ziehe eine Linie von der aktuellen Position zu x,y. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> L</b> *{<span class="varname"> x,y</span>} </td> 
   <td> <p> lineto relativ </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> C</b> *{<span class="varname"> x1,y1,x2,y2,x,y</span>} </td> 
   <td> <p> Kurve zu absolut </p> </td> 
   <td> <p> Zeichnen Sie eine Bézierkurve von der aktuellen Position auf x,y. x1,y1 ist der Steuerpunkt am Anfang der Kurve und x2,y2 ist der Steuerpunkt am Ende der Kurve. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> C</b> *{<span class="varname"> x1,y1,x2,y2,x,y</span>} </td> 
   <td> <p> Kennlinie </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> Z</b> | <b>Z</b> </td> 
   <td> <p> closePath </p> </td> 
   <td> <p> Schließt den aktuellen Unterpfad mit einer geraden Linie. </p> </td> 
  </tr> 
 </tbody> 
</table>

Großbuchstaben geben an, dass sich die Koordinatenwerte in absoluten Pixelpositionen befinden (relativ zur oberen linken Ecke des Ebenenrechtecks). Pixel-Offsets folgen relativ zur aktuellen Position den Befehlen in Kleinbuchstaben.

„m“ oder „M“ startet immer einen neuen Unterpfad. Unterpfade werden automatisch geschlossen (mit gerader Linie), wenn am Ende kein „Z“ oder „z“ angegeben ist.

Wenn ein Unterpfad mit einem relativen Moveto (&#39;m&#39;) beginnt, ist er relativ zu einem der folgenden:

* Der Startpunkt des vorherigen Unterpfads, wenn er mit „z“ oder „Z“ geschlossen wurde.
* Der Endpunkt des vorherigen Unterpfads, wenn er nicht explizit geschlossen wurde.
* 0,0, wenn es der erste Unterpfad ist.

## Eigenschaften {#section-d4127db0dac54e3cbd44f7ea1e001960}

Ebenenattribut. Gilt für die aktuelle Ebene oder das zusammengesetzte Bild, falls `layer=comp`. Effektebenen ignorieren sie.

Der Modifikator `clipPathE=` wird ignoriert, wenn im Ebenenquellbild kein Pfad mit dem angegebenen Namen gefunden wird oder wenn die Ebenenquelle kein Bild ist.

## Standard {#section-076c35ea37fa4a44ada253b4c2dec1dd}

Keine, für kein zusätzliches Beschneiden der Ebene.

## Verwandte Themen {#section-dd8110fb6f5c45eba6284c5ec5f49056}

[clipXpath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clipxpath.md#reference-17e5e4da3e044943af8f963f58a45f53) , [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef) , [extension=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)
