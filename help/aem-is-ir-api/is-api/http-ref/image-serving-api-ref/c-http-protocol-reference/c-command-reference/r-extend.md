---
title: ausdehnen
description: Ebene erweitern. Fügt einer Ebene Ränder hinzu oder schneidet das Ebenenrechteck zu.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 03db6555-6851-49d4-b0de-5570bf56ad76
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 1%

---

# ausdehnen{#extend}

Ebene erweitern. Fügt einer Ebene Ränder hinzu oder schneidet das Ebenenrechteck zu.

`extend= *`links`*, *`oben`*, *`rechts`*, *`unten`*`

`extendN= *`leftN`*, *`topN`*, *`rightN`*, *`bottomN`*`

<table id="simpletable_1DCCD469712B423C8154630127DC5F54"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> links,oben,unten,rechts</span></span> </p></td> 
  <td class="stentry"> <p>Anzahl der Pixel, die der linken, oberen, rechten und unteren Kante der Ebene hinzugefügt (oder daraus entfernt werden sollen, wenn der Wert negativ ist) werden sollen (int, int, int, int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> linksN,topN,bottomN,rightN</span></span> </p></td> 
  <td class="stentry"> <p>Der Raum, der der linken, oberen, rechten und unteren Kante der Ebene rect hinzugefügt (oder daraus entfernt werden soll, wenn der Wert negativ ist) werden als normalisierte Beträge im Verhältnis zur Größe der ursprünglichen Ebene rect (real, real, real, real) ausgedrückt. </p></td> 
 </tr> 
</table>

`extend=` wird auf die Ebene *nachdem* das Bild abgeschnitten wurde ( `crop=`) und alle Ebenentransformationen, einschließlich `rotate=`, wurden angewendet.

Der erweiterte Bereich ist mit `bgColor=` ausgefüllt oder bleibt, falls nicht anders angegeben, transparent.

Die Argumentwerte für `extendN=` werden anhand der Größe der Ebene normalisiert, die nach der Ebenentransformation (einschließlich `rotate=`) angewendet wurde.

## Eigenschaften {#section-8fc94de871f841f3bf5e1df135972ca9}

Ebenenattribut. Gilt für Ebene 0, falls `layer=comp`. Von Effektebenen ignoriert.

## Standard {#section-de7473649cb9406b8d99028c74c4b8dc}

`extend=0,0,0,0`, für keine Änderung des Ebenenrechtecks.

## Beispiele {#section-cc6d8e76f3dd4607ac31cb095d86c9fe}

**Beschneiden Sie ein Bild und fügen Sie dann einen 5 Pixel breiten, roten Rahmen hinzu:**

`…&cropN=.2,.3,.8,.9&extend=5,5,5,5&bgColor=255,0,0&…`

**Skalieren Sie ein Bild auf eine Breite von 200 Pixeln und fügen Sie Titeltext in einen Rand von 30 Pixeln über dem Bild ein.**

Beachten Sie, dass die Höhe des zusammengesetzten Bildes je nach Seitenverhältnis des Bildes variiert.

`http://server/myRootId/myImageId?size=200,0&extend=0,30,0,0&origin=0,0 layer=1&text=title-text&origin=0,0`

## Verwandte Themen {#section-2d9572be32ca4602b60920b3810f3638}

[Crop=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab) , [color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md), [size=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b), [origin=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md#reference-e11c7ac06e2240cc884c3fec98f05138), [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)
