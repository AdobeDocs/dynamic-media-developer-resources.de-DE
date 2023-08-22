---
title: res
description: Auflösungsbasierte Bildskalierung. Skaliert das Bild auf die angeforderte Auflösung.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e8ed7b00-7bb3-463e-9aaa-47f77bd4b45e
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '323'
ht-degree: 1%

---

# res{#res}

Auflösungsbasierte Bildskalierung. Skaliert das Bild auf die angeforderte Auflösung.

` res= *`val`*`

<table id="simpletable_E69F3709266749C4A165C90FF18FF5AA"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val </span> </p> </td> 
  <td class="stentry"> <p>Target-Auflösung, normalerweise in Pixel pro Zoll (real). </p> </td> 
 </tr> 
</table>

Der Skalierungsfaktor wird durch Division berechnet *`val`* von `catalog::Resolution`. Beachten Sie, dass dieser Befehl keine Auswirkungen auf die Druckauflösung des Antwortbilds hat.

Um diese Funktion verwenden zu können, muss die Auflösung der ursprünglichen Quellbilder bekannt sein und unter `catalog::Resolution`. Je nach Anwendung können die Auflösungseinheiten variieren. Bei wiederholbaren 2D-Texturen oder Materialmustern wie Wallpaper oder Gewebe kann die Auflösung in Pixel/Zoll oder Pixel/mm ausgedrückt werden. Luftaufnahmen und -karten können besser von Pixel/Meile oder Pixeln/km bedient werden. In jedem Fall werden die Einheiten für `catalog::Resolution` muss mit den Einheiten übereinstimmen, die für `res=`.

Zusätzlich zum Abrufen von Bildern mit genauen Auflösungen, `res=` kann auch verwendet werden, um mehrere Bilder mit der gleichen Auflösung zu kombinieren, sodass die in diesen Bildern sichtbaren Elemente in einem angemessenen Verhältnis zueinander stehen.

>[!NOTE]
>
>Normalerweise wird die Größe eines zusammengesetzten Bildes auf die Zielansichtsgröße (angegeben durch `wid=`, `hei=`oder `attribute::DefaultPix`), bevor sie an den Client zurückgegeben wird. Um diese Größenanpassung zu vermeiden und ein Bild mit der exakten Auflösung zu erhalten, die von `res=`kann es erforderlich sein, die Anzeige-Skalierung zu deaktivieren, indem Sie explizit `scl=1`. Dadurch wird der Server angewiesen, das zusammengesetzte Bild auf die Zielansichtsgröße zuzuschneiden, anstatt es zu skalieren.

## Eigenschaften {#section-fdbd16e59cff4952a3717146bc91412e}

Quellbild-/Maskenattribut. Ignoriert durch Ebenen, die nicht mit einem Quellbild oder einer Quellmaske verknüpft sind. Wird auf Ebene 0 angewendet, ist spezifiziert für `layer=comp`. Ignoriert , wenn `scale=` oder `size=` wird für dieselbe Ebene angegeben.

## Standard {#section-c5f1ba6fe53d46eca32e7d0588dcdf3d}

Falls nicht angegeben, `scale=` oder `size=` bestimmt den Skalierungsfaktor oder, wenn keines angegeben ist, wird das Bild ohne Skalierung verwendet.

## Beispiel {#section-eb06f333e08e4247971fb1b18922597b}

Rufen Sie ein Texturbild mit einer Objektauflösung von 12 Pixel/Zoll für die Verwendung mit Image Rendering oder Image Authoring ab. Wir geben verlustfreies PNG-Format und eine bessere Qualität der Neuberechnung für bestmögliche Qualität an.

` http:// *`Server`*/myTexture?res=12&fmt=png&resMode=sharp`

## Verwandte Themen {#section-1f8a8f11772e493ca803c4511f397a11}

[catalog::Resolution](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-resolution-cat.md#reference-de489f5f36b64bd0831749546f8728e1) , [attribute::DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1), [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc), [fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
