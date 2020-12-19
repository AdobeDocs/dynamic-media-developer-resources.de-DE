---
description: Auflösungsbasierte Bildskalierung. Skaliert das Bild auf die gewünschte Auflösung.
seo-description: Auflösungsbasierte Bildskalierung. Skaliert das Bild auf die gewünschte Auflösung.
seo-title: res
solution: Experience Manager
title: res
topic: Scene7 Image Serving - Image Rendering API
uuid: ab0c8329-5d40-4233-a122-8cb8ca01b500
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '334'
ht-degree: 1%

---


# res{#res}

Auflösungsbasierte Bildskalierung. Skaliert das Bild auf die gewünschte Auflösung.

` res= *`val`*`

<table id="simpletable_E69F3709266749C4A165C90FF18FF5AA"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val  </span> </p> </td> 
  <td class="stentry"> <p>Lösung der Zielgruppe; normalerweise in Pixel pro Zoll (real). </p> </td> 
 </tr> 
</table>

Der Skalierungsfaktor wird durch Division von *`val`* durch `catalog::Resolution` berechnet. Beachten Sie, dass dieser Befehl sich nicht auf die Druckauflösung des Antwortbilds auswirkt.

Um diese Funktion verwenden zu können, muss die Auflösung der Originalbilder bekannt sein und in `catalog::Resolution` eingestellt werden. Je nach Anwendung können die Auflösungseinheiten variieren. Bei wiederholbaren 2D-Texturen oder Materialfeldern wie Hintergrundbildern oder Stoffen kann die Auflösung in Pixel/Zoll oder Pixel/mm ausgedrückt werden. Luftbilder und Landkarten können besser mit Pixeln/Meilen oder Pixeln/km versorgt werden. In jedem Fall müssen die für `catalog::Resolution` verwendeten Einheiten mit den für `res=` verwendeten Einheiten übereinstimmen.

Zusätzlich zum Abrufen von Bildern mit präzisen Auflösungen können auch `res=` verwendet werden, um mehrere Bilder mit derselben Auflösung zu kombinieren, sodass die in diesen Bildern sichtbaren Elemente exakt proportional zueinander sind.

>[!NOTE]
>
>Normalerweise wird die Größe eines Composite-Bildes auf die Ansicht der Zielgruppe angepasst (angegeben von `wid=`, `hei=` oder `attribute::DefaultPix`), bevor es an den Client zurückgegeben wird. Um zu verhindern, dass die Bildgröße verändert wird, und um ein Bild mit der exakten Auflösung zu erhalten, die von `res=` angegeben wird, muss die Skalierung der Ansicht ggf. deaktiviert werden, indem explizit `scl=1` angegeben wird. Dadurch wird der Server angewiesen, das Composite-Bild auf die Ansicht der Zielgruppe zu beschneiden, anstatt es zu skalieren.

## Eigenschaften {#section-fdbd16e59cff4952a3717146bc91412e}

Quellenbild/Maskenattribut. Wird von Ebenen ignoriert, die keinem Quellbild oder einer Quellmaske zugeordnet sind. Für `layer=comp` wird Ebene 0 angewendet. Wird ignoriert, wenn für dieselbe Ebene `scale=` oder `size=` angegeben ist.

## Standard {#section-c5f1ba6fe53d46eca32e7d0588dcdf3d}

Ist kein Wert angegeben, bestimmt `scale=` oder `size=` den Skalierungsfaktor oder, wenn keines der beiden Werte nicht angegeben ist, wird das Bild ohne Skalierung verwendet.

## Beispiel {#section-eb06f333e08e4247971fb1b18922597b}

Rufen Sie ein Texturbild mit einer Objektauflösung von 12 Pixel/Zoll ab, um es mit dem Image Rendering oder dem Image Authoring zu verwenden. Wir legen verlustfreies PNG-Format und eine bessere Qualität der Neuberechnung für eine bestmögliche Qualität,

` http:// *`Server`*/myTexture?res=12&fmt=png&resMode=sharp`

## Verwandte Themen {#section-1f8a8f11772e493ca803c4511f397a11}

[Katalog::Resolution](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-resolution-cat.md#reference-de489f5f36b64bd0831749546f8728e1) ,  [Attribut::DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1),  [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc),  [fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
