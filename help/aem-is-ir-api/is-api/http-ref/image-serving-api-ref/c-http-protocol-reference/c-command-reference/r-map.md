---
description: Imagemap-Daten. Stellt Imagemap-Daten für diese Ebene bereit. Überschreibt alle Daten aus der Katalogzuordnung für diese Ebene.
seo-description: Imagemap-Daten. Stellt Imagemap-Daten für diese Ebene bereit. Überschreibt alle Daten aus der Katalogzuordnung für diese Ebene.
seo-title: Karte
solution: Experience Manager
title: Karte
topic: Scene7 Image Serving - Image Rendering API
uuid: 9c1c3323-21ab-4820-bf4e-761b82ada1ab
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Karte{#map}

Imagemap-Daten. Stellt Imagemap-Daten für diese Ebene bereit. Überschreibt alle Daten aus Katalog::Map für diese Ebene.

`map=[ *``*]mapA=[ *`stringA`*]`

<table id="simpletable_2E32B25D5F6246A18A8AF817903877ED"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> Zeichenfolge</span></span> </p></td> 
  <td class="stentry"> <p>Imagemap-Daten für diese Ebene in Ebenenkoordinaten. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> Zeichenfolge <span class="varname"> A</span></span> </p></td> 
  <td class="stentry"> <p>Imagemap-Daten für diese Ebene in Quellbildkoordinaten. </p></td> 
 </tr> 
</table>

Eine leere Zeichenfolge gibt an, dass diese Ebene keine Imagemap bereitstellen sollte. Die Zeichenfolge muss ordnungsgemäß HTTP-kodiert sein, um Analyseprobleme zu vermeiden.

Alle Zeichen mit kaufmännischem Und (&amp;) *`string`* müssen http-kodiert sein.

Beim Angeben `mapA=` und `catalog::Map` Angeben von Zuordnungsdaten in den Koordinaten des Quellbilds `map=` werden die Ebenenkoordinaten relativ zur oberen, linken Ecke des Ebenenrechtecks (nach `rotate=` und `extend=` Anwendung) angenommen.

Die Ausgabebildkarte wird immer an das Ebenenrechteck geklickt. Wenn das `shape` Attribut weggelassen oder auf `default`festgelegt wird, wird das gesamte Ebenenrechteck als Imagemap-Bereich verwendet.

## Eigenschaften {#section-a18d9ea95c71414a905a68b8839c0843}

Ebenenattribut. Bei Anwendung auf `layer=comp`werden die angegebenen Kartendaten hinter allen anderen Imagemaps angeordnet. Wird ignoriert, sofern nicht `req=map`. Von Effektebenen ignoriert. `mapA=` wird ignoriert, wenn auch angegeben `map=` wird.

## Standard {#section-620c19b3f3b84ba49706062de3f12f05}

`catalog::Map` verwendet, wenn nicht angegeben `map=` ist.

## Beispiel {#section-cd7691c94f984222845c86dcb0051ce8}

Definieren Sie eine rechteckige Imagemap für eine einfache Textebene:

`…&layer=1&text=Scene7&map=<area%20alt=Scene7%20href=www.scene7.com>&…`

Ein `AREA` Element mit (meist) Standardattributen wird verwendet, um den Kartenbereich für das gesamte Ebenenrechteck einzufügen.

## Verwandte Themen {#section-bc1d946fdf4b47bf9742a986800aa9b5}

[Imagemaps](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-image-maps.md#reference-ff7d1bac2a064104b0c508a81316fdab), [req=map](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
