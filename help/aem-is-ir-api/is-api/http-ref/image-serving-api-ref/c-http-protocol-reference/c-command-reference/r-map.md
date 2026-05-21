---
title: Karte
description: Imagemap-Daten. Stellt Imagemap-Daten für diese Ebene bereit. Überschreibt alle Daten aus der Katalogzuordnung für diese Ebene.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7c1fbb50-98ec-4d9a-b608-93d60d687069
TQID: 'https://experienceleague.adobe.com/9JJUVcw5-wl0B-rP-m6DC1c1DGIqxaV2UgboocFGGV8'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 224
ht-degree: 2%

---

# Karte{#map}

Imagemap-Daten. Stellt Imagemap-Daten für diese Ebene bereit. Überschreibt alle Daten aus catalog:map für diese Ebene.

`map=[ *`string`*]mapA=[ *`stringA`*]`

<table id="simpletable_2E32B25D5F6246A18A8AF817903877ED"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> Zeichenfolge</span></span> </p></td> 
  <td class="stentry"> <p>Imagemap-Daten für diese Ebene in Ebenenkoordinaten. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> ZeichenfolgeA</span></span> </p></td> 
  <td class="stentry"> <p>Imagemap-Daten für diese Ebene in Quell-Bildkoordinaten. </p></td> 
 </tr> 
</table>

Eine leere Zeichenfolge bedeutet, dass diese Ebene keine Imagemap bereitstellen sollte. Die Zeichenfolge muss ordnungsgemäß HTTP-kodiert sein, um Parsing-Probleme zu vermeiden.

Alle kaufmännischen Und-Zeichen (&amp;), die in *`string`* vorkommen, müssen HTTP-kodiert sein.

Während `mapA=` und `catalog::Map` Zuordnungsdaten in den Koordinaten des Quellbilds angeben, geht `map=` von Ebenenkoordinaten relativ zur oberen linken Ecke des Ebenenrechtecks aus (nach `rotate=` und `extend=`).

Die Ausgabebildkarte wird immer auf das Ebenenrechteck abgeschnitten. Wenn das Attribut `shape` ausgelassen oder auf `default` gesetzt wird, wird das gesamte Ebenenrechteck als Imagemap-Bereich verwendet.

## Eigenschaften {#section-a18d9ea95c71414a905a68b8839c0843}

Ebenenattribut. Bei Anwendung auf `layer=comp` werden die angegebenen Kartendaten hinter allen anderen Imagemaps geschichtet. Ignoriert, sofern nicht `req=map`. Von Effektebenen ignoriert. `mapA=` wird ignoriert, wenn auch `map=` angegeben ist.

## Standard {#section-620c19b3f3b84ba49706062de3f12f05}

`catalog::Map` wird verwendet, wenn `map=` nicht angegeben ist.

## Beispiel {#section-cd7691c94f984222845c86dcb0051ce8}

Definieren Sie eine rechteckige Imagemap für eine einfache Textebene:

`…&layer=1&text=Scene7&map=<area%20alt=Scene7%20href=www.scene7.com>&…`

Ein `AREA` mit (meist) Standardattributen wird verwendet, um den Zuordnungsbereich für das gesamte Ebenenrechteck einzufügen.

## Verwandte Themen {#section-bc1d946fdf4b47bf9742a986800aa9b5}

[Imagemaps](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-image-maps.md#reference-ff7d1bac2a064104b0c508a81316fdab), [req=map](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
