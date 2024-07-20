---
title: drehen
description: Bild drehen. Dreht die Bild-, Text- oder einfarbige Farbschicht um den angegebenen Winkel.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9f1b2d6f-4e67-4530-9ec6-870b97687ce0
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 2%

---

# drehen{#rotate}

Bild drehen. Dreht die Bild-, Text- oder einfarbige Farbschicht um den angegebenen Winkel.

`rotate= *`angle`*`

<table id="simpletable_5531ED4C2099411DB404657E12B05314"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> Winkel</span> </p> </td> 
  <td class="stentry"> <p>Drehwinkel in Grad (real). </p></td> 
 </tr> 
</table>

Positive Winkel drehen den Uhrzeigersinn. Der Ebenenankerpunkt ( `anchor=` oder `catalog::Anchor`) dient als Drehmittelpunkt. Das Ebenenrechteck wird nach Bedarf vergrößert und um die gedrehten Daten herum angepasst, um das Zuschneiden zu vermeiden. Die Rotation wird angewendet, nachdem der Hintergrundbereich der Ebene mit `color=` gefüllt wurde. Der Modifikator `bgColor=` kann verwendet werden, um dem Begrenzungsrechteck nach der Drehung Hintergrundfarbe hinzuzufügen.

## Eigenschaften {#section-8b5a9bb9062f48dbb8d4e9953ff39e39}

Ebenenbefehl. Gilt für die aktuelle Ebene oder für Ebene 0, wenn `layer=comp`. Wird von Effektebenen ignoriert.

## Standard {#section-69475db636124a8a85f132b6d49bd592}

`rotate=0`, für keine Drehung.

## Beispiel {#section-e8ab3ba8a8624b43aeaaa8f089fc2f00}

Platzieren Sie in einem Bildkatalog in der oberen linken Ecke der Bilder eine Beschriftung &quot;Bei Verkauf&quot;. Das Titelbild wird für die 300x300-Ansicht bereits korrekt skaliert und sollte um 30° nach links gedreht werden. Um die Beschriftung zu verbessern, füllen Sie das Textfeld mit einer weißen, halb undurchsichtigen Farbe.

`http:// *`server`*/myRootId/myImageId?scl=1&size=300,300&origin=-0.5,-0.5 &layer=1&src=labelImage&origin=-0.5,-0.5&rotate=-30&color=ffffff40`

Wenden Sie `size=` auf Ebene 0 an, um die Anzeigegröße festzulegen, anstatt `wid=` und `hei=` zu verwenden. Mit dieser Methode kann die Größe von `myImageId` geändert werden, ohne dass die endgültige Größe von `labelImage` geändert wird. Geben Sie außerdem `scl=1` an. Andernfalls kann das zusammengesetzte Bild auf `attribute::DefaultPix` skaliert werden (es sei denn, dies ist auf 0,0 festgelegt). Der Modifikator `color=` fügt dem Textfeld vor der Drehung die halbopak Hintergrundfarbe hinzu.

Der Ausgangspunkt für beide Ebenen ist auf die obere linke Ecke eingestellt, um die gewünschte Ausrichtung zu erreichen. Der Ausgangspunkt für Ebene 1 gilt für `labelImage`nach dem Drehen.

Ein Beispiel für gedrehten Text finden Sie unter [Beispiel A](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/r-example-a.md#reference-c78ea82e8a1646738e764fa6685dfbac) in [Vorlagen](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e) .

## Verwandte Themen {#section-c371ee0845994b7382c02e782d1bc595}

[anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c) , [bgColor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab), [color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)
