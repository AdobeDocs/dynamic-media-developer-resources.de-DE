---
description: Ebene erweitern. Fügt Ränder zu einer Ebene hinzu oder beschneidet das Ebenenrechteck.
solution: Experience Manager
title: erweitern
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 03db6555-6851-49d4-b0de-5570bf56ad76
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '240'
ht-degree: 2%

---

# erweitern{#extend}

Ebene erweitern. Fügt Ränder zu einer Ebene hinzu oder beschneidet das Ebenenrechteck.

`extend= *``*, *``*, *``*, *`linfttoprightbottom`*`

`extendN= *``*, *``*, *``*, *`leftNtopNrightNbottomN`*`

<table id="simpletable_1DCCD469712B423C8154630127DC5F54"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> left,top,bottom,right</span></span> </p></td> 
  <td class="stentry"> <p>Anzahl der Pixel, die zum linken, oberen, rechten und unteren Rand der Ebene (int, int, int, int) hinzugefügt (bzw. daraus entfernt werden sollen, wenn der Wert negativ ist). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> leftN,topN,bottomN,rightN</span></span> </p></td> 
  <td class="stentry"> <p>Der Abstand, der zum linken, oberen, rechten und unteren Rand des Ebenen-Rects hinzugefügt (oder daraus entfernt werden soll, wenn der Wert negativ ist), ausgedrückt als normalisierte Beträge in Bezug auf die Größe der ursprünglichen Ebene rect (real, real, real, real). </p></td> 
 </tr> 
</table>

`extend=` wird auf die Ebene angewendet,  ** nachdem das Bild beschnitten (  `crop=`) und alle Ebenentransformationen, einschließlich  `rotate=`, angewendet wurden.

Der erweiterte Bereich wird mit `bgColor=` gefüllt oder, falls nicht angegeben, bleibt transparent.

Die Argumentwerte für `extendN=` werden relativ zur Größe des Layer Rect normalisiert, nachdem Ebenentransformationen einschließlich `rotate=` angewendet wurden.

## Eigenschaften {#section-8fc94de871f841f3bf5e1df135972ca9}

Ebenenattribut. Gilt für Ebene 0, wenn `layer=comp`. Wird von Effektebenen ignoriert.

## Standard {#section-de7473649cb9406b8d99028c74c4b8dc}

`extend=0,0,0,0`, um das Ebenenrechteck nicht zu ändern.

## Beispiele {#section-cc6d8e76f3dd4607ac31cb095d86c9fe}

**Beschneiden Sie ein Bild und fügen Sie dann einen 5 Pixel breiten, roten Rahmen hinzu:**

`…&cropN=.2,.3,.8,.9&extend=5,5,5,5&bgColor=255,0,0&…`

**Skalieren Sie ein Bild auf eine Breite von 200 Pixel und fügen Sie Titeltext in einen 30-Pixel-Rand über dem Bild hinzu.**

Beachten Sie, dass die Höhe des zusammengesetzten Bildes vom Seitenverhältnis des Bildes abhängt.

`http://server/myRootId/myImageId?size=200,0&extend=0,30,0,0&origin=0,0 layer=1&text=title-text&origin=0,0`

## Verwandte Themen {#section-2d9572be32ca4602b60920b3810f3638}

[crop=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab) ,  [color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md),  [size=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b),  [origin=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md#reference-e11c7ac06e2240cc884c3fec98f05138),  [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)
