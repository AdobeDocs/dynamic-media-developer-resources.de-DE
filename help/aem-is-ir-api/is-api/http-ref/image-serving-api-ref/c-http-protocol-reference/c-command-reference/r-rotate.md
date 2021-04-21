---
description: Bild drehen Dreht die Bild-, Text- oder Volltonfarbebene um den angegebenen Winkel.
solution: Experience Manager
title: drehen
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '266'
ht-degree: 3%

---


# rotate{#rotate}

Bild drehen Dreht die Bild-, Text- oder Volltonfarbebene um den angegebenen Winkel.

`rotate= *`Winkel`*`

<table id="simpletable_5531ED4C2099411DB404657E12B05314"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> Winkel</span> </p> </td> 
  <td class="stentry"> <p>Drehwinkel in Grad (real). </p></td> 
 </tr> 
</table>

Positive Winkel drehen im Uhrzeigersinn. Der Verankerungspunkt der Ebene ( `anchor=` oder `catalog::Anchor`) dient als Drehmittelpunkt. Das Ebenenrechteck wird nach Bedarf vergrößert und um die gedrehten Daten angepasst, um das Beschneiden zu vermeiden. Die Drehung wird durchgeführt, nachdem der Hintergrundbereich der Ebene mit `color=` gefüllt wurde. `bgColor=` kann verwendet werden, um dem Begrenzungsrechteck nach der Drehung eine Hintergrundfarbe hinzuzufügen.

## Eigenschaften {#section-8b5a9bb9062f48dbb8d4e9953ff39e39}

Ebene, Befehl. Gilt für die aktuelle Ebene oder für Ebene 0, wenn `layer=comp`. Von Effektebenen ignoriert.

## Standard {#section-69475db636124a8a85f132b6d49bd592}

`rotate=0`, ohne Drehung.

## Beispiel {#section-e8ab3ba8a8624b43aeaaa8f089fc2f00}

Platzieren Sie die Beschriftung &quot;On Sale&quot;links oben in einem Bildkatalog. Das Beschriftungsbild wird für die Ansicht 300 x 300 bereits korrekt skaliert und sollte um 30 Grad nach links gedreht werden. Füllen Sie das Textfeld mit einer weißen, halbtransparenten Farbe, um die Beschriftung zu verbessern.

`http:// *`Server`*/myRootId/myImageId?scl=1&size=300,300&origin=-0.5,-0.5 &layer=1&src=labelImage&origin=-0.5,-0.5&rotate=-30&color=ffffff40`

Wir wenden `size=` auf Ebene 0 an, um die Ansicht festzulegen, anstatt `wid=` und `hei=` zu verwenden. Dadurch kann die Größe von `myImageId` ohne Änderung der endgültigen Größe von `labelImage` geändert werden. Wir müssen auch `scl=1` angeben, andernfalls kann das Composite-Bild auf `attribute::DefaultPix` skaliert werden (es sei denn, dies ist auf 0,0 eingestellt). `color=` fügt dem Textfeld vor der Drehung die halbundurchsichtige Hintergrundfarbe hinzu.

Die Herkunft für beide Ebenen wird auf die obere linke Ecke eingestellt, um die gewünschte Ausrichtung zu erzielen. Beachten Sie, dass der Herkunft-Punkt für Ebene 1 für `labelImage`gilt, nachdem er gedreht wurde.

Ein Beispiel für gedrehten Text finden Sie unter [Beispiel A](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/r-example-a.md#reference-c78ea82e8a1646738e764fa6685dfbac) in [Vorlagen](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## Verwandte Themen {#section-c371ee0845994b7382c02e782d1bc595}

[anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c) ,  [bgColor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab),  [color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)
