---
title: in eine Linie bringen
description: Textur - Ausrichtung rendern. Gibt an, welcher der durch das ausgewählte Vignettenobjekt definierten Ausgangspunkte verwendet werden soll.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0b76f173-809b-4b41-bf39-6b85f77ab2db
TQID: 'https://experienceleague.adobe.com/U6V-e23e9ILdnQfTpJzGPzbCTZEICccSpcMebA-NRjA'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 70c478ebbe0b38d9e35c1bb26074a458c0197b2b
workflow-type: tm+mt
source-wordcount: 190
ht-degree: 4%

---

# in eine Linie bringen {#align}

Textur - Ausrichtung rendern. Gibt an, welcher der durch das ausgewählte Vignettenobjekt definierten Ausgangspunkte verwendet werden soll.

`align=0|1|2|3|4|5|6`

<table id="simpletable_D15233999E35488EB2F933BD72798E2F"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p></td> 
  <td class="stentry"> <p>Standard-Ursprung (zentrierte Übereinstimmung). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p></td> 
  <td class="stentry"> <p>Fortlaufende Übereinstimmung - Herkunft. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p></td> 
  <td class="stentry"> <p>Zufällige Ausrichtung. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3..6 </p></td> 
  <td class="stentry"> <p>Benutzerdefinierter Ursprung. </p></td> 
 </tr> 
</table>

Der Renderer wendet die Textur auf das Objekt an, sodass der Texturankerpunkt ( `anchor=`) mit dem angegebenen Ausgangspunkt übereinstimmt.

Jedes Objekt kann bis zu sechs Ausgangspunkte definieren (0, 1, 3, 4, 5, 6). Wenn ein `align` angegeben wird, der entsprechende Ausgangspunkt jedoch nicht durch das Vignettenobjekt definiert ist, wird der standardmäßige Ausgangspunkt (zentrierte Übereinstimmung) verwendet.

`align=2` Gibt eine zufällige Texturausrichtung an. In diesem Fall wird `anchor=` effektiv ignoriert.

Wird hauptsächlich für Polstermaterialien verwendet, möglicherweise für Bekleidungsstoffe, um die Ausrichtung der Textur zwischen benachbarten Objekten zu verwalten.

## Eigenschaften {#section-350fadc87dcf4812a8a02d1c3d6697a0}

Materialattribut. Wird ignoriert, wenn ein Wand-, Schrank-, Geräte- oder Fensterabdeckungsrahmenobjekt ausgewählt ist oder wenn das Material keine wiederholbare Textur ist.

## Standard {#section-3231c2854bae4477836b626ac208dd34}

`catalog::Alignment`, wenn das Material auf einem Katalogeintrag basiert, andernfalls 0 (zentriert).

## Verwandte Themen {#section-945d1ce275df487d9d564d4043156c79}

[catalog::align](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-alignment.md#reference-e52152e8dc244d0aa13b40c615d0f399) , [anchor=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26)

