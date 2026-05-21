---
title: drehen
description: Bild drehen. Dreht die Bild-, Text- oder einfarbige Ebene um den angegebenen Winkel.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9f1b2d6f-4e67-4530-9ec6-870b97687ce0
TQID: 'https://experienceleague.adobe.com/WDC8SRJEBqspJidlNPxLvwmX-HMQG1zC6wwHNJIXLK4'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 266
ht-degree: 2%

---

# drehen{#rotate}

Bild drehen. Dreht die Bild-, Text- oder einfarbige Ebene um den angegebenen Winkel.

`rotate= *`Winkel`*`

<table id="simpletable_5531ED4C2099411DB404657E12B05314"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> Winkel</span> </p> </td> 
  <td class="stentry"> <p>Drehwinkel in Grad (real). </p></td> 
 </tr> 
</table>

Positive Winkel drehen sich im Uhrzeigersinn. Der Lagenankerpunkt ( `anchor=` oder `catalog::Anchor`) dient als Drehmittelpunkt. Das Ebenenrechteck wird vergrößert und um die gedrehten Daten nach Bedarf angepasst, um das Zuschneiden zu vermeiden. Eine Drehung wird angewendet, nachdem der Hintergrundbereich des Layers mit `color=` gefüllt wurde. Mit dem Modifikator `bgColor=` können Sie dem umgebenden Rechteck nach der Drehung Hintergrundfarbe hinzufügen.

## Eigenschaften {#section-8b5a9bb9062f48dbb8d4e9953ff39e39}

Ebenenbefehl. Gilt für die aktuelle Ebene oder, falls `layer=comp`, für Ebene 0. Von Effektebenen ignoriert.

## Standard {#section-69475db636124a8a85f132b6d49bd592}

`rotate=0`, für keine Rotation.

## Beispiel {#section-e8ab3ba8a8624b43aeaaa8f089fc2f00}

Platzieren Sie in einem Bildkatalog eine Kennzeichnung „Im Angebot“ in der oberen linken Ecke. Das Etikettenbild hat bereits die korrekte Größe für die 300x300-Ansicht und sollte um 30° nach links gedreht werden. Um das Etikett zu vergrößern, füllen Sie das Textfeld mit einer weißen, halb opaken Farbe aus.

`http:// *`server`*/myRootId/myImageId?scl=1&size=300,300&origin=-0.5,-0.5 &layer=1&src=labelImage&origin=-0.5,-0.5&rotate=-30&color=ffffff40`

Wenden Sie `size=` auf Ebene 0 an, um die Ansichtsgröße festzulegen, anstatt `wid=` und `hei=` zu verwenden. Mit dieser Methode kann die Größe von `myImageId` geändert werden, ohne die endgültige Größe von `labelImage` zu ändern. Geben Sie außerdem `scl=1` an, andernfalls kann das zusammengesetzte Bild auf `attribute::DefaultPix` skaliert werden (es sei denn, dies ist auf 0,0 festgelegt). Der Modifikator `color=` fügt dem Textfeld vor der Drehung die halbopake Hintergrundfarbe hinzu.

Der Ursprung für beide Ebenen wird auf die obere linke Ecke eingestellt, um die gewünschte Ausrichtung zu erreichen. Der Ausgangspunkt für Ebene 1 gilt für `labelImage`nachdem sie gedreht wurde.

Ein Beispiel für gedrehten Text finden [&#128279;](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/r-example-a.md#reference-c78ea82e8a1646738e764fa6685dfbac)Beispiel A[&#x200B; unter Vorlagen](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## Verwandte Themen {#section-c371ee0845994b7382c02e782d1bc595}

[anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c) , [bgColor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab), [color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)
