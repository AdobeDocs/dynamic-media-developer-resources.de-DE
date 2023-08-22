---
title: Karte
description: Imagemap-Daten. Stellt Imagemap-Daten für diese Ebene bereit. Überschreibt alle Daten aus der Katalogzuordnung für diese Ebene.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7c1fbb50-98ec-4d9a-b608-93d60d687069
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '223'
ht-degree: 2%

---

# Karte{#map}

Imagemap-Daten. Stellt Imagemap-Daten für diese Ebene bereit. Überschreibt alle Daten aus catalog::Map für diese Ebene.

`map=[ *`Zeichenfolge`*]mapA=[ *`stringA`*]`

<table id="simpletable_2E32B25D5F6246A18A8AF817903877ED"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> Zeichenfolge</span></span> </p></td> 
  <td class="stentry"> <p>Imagemap-Daten für diese Ebene in Ebenenkoordinaten. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> stringA</span></span> </p></td> 
  <td class="stentry"> <p>Imagemap-Daten für diese Ebene in Quell-Bildkoordinaten. </p></td> 
 </tr> 
</table>

Eine leere Zeichenfolge gibt an, dass diese Ebene keine Imagemap bereitstellen sollte. Die Zeichenfolge muss ordnungsgemäß HTTP-kodiert sein, um Parsing-Probleme zu vermeiden.

Alle Zeichen von Und (&amp;), die in *`string`* muss http-kodiert sein.

while `mapA=` und `catalog::Map` Kartendaten in Quell-Bildkoordinaten angeben, `map=` geht davon aus, dass die Ebenenkoordinaten relativ zur oberen linken Ecke des Ebenenrechtecks sind (nach `rotate=` und `extend=` angewendet wurden).

Die Ausgabebildkarte wird immer auf das Ebenenrechteck gekürzt. Wenn die Variable `shape` ausgelassen oder auf `default`, wird das gesamte Ebenenrechteck als Imagemap-Bereich verwendet.

## Eigenschaften {#section-a18d9ea95c71414a905a68b8839c0843}

Ebenenattribut. Bei Anwendung auf `layer=comp`, werden die angegebenen Zuordnungsdaten hinter allen anderen Imagemaps hinterlegt. Ignoriert, außer `req=map`. Wird von Effektebenen ignoriert. `mapA=` wird ignoriert, wenn `map=` wird ebenfalls angegeben.

## Standard {#section-620c19b3f3b84ba49706062de3f12f05}

`catalog::Map` verwendet wird, wenn `map=` nicht angegeben ist.

## Beispiel {#section-cd7691c94f984222845c86dcb0051ce8}

Definieren Sie eine rechteckige Imagemap für eine einfache Textebene:

`…&layer=1&text=Scene7&map=<area%20alt=Scene7%20href=www.scene7.com>&…`

Ein `AREA` -Element mit (meist) Standardattributen wird verwendet, um den Zuordnungsbereich für das gesamte Ebenenrechteck einzufügen.

## Verwandte Themen {#section-bc1d946fdf4b47bf9742a986800aa9b5}

[Imagemaps](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-image-maps.md#reference-ff7d1bac2a064104b0c508a81316fdab), [req=map](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
