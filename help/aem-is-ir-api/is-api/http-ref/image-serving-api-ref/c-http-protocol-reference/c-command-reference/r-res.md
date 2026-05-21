---
title: res
description: Auflösungsbasierte Bildskalierung. Skaliert das Bild auf die angeforderte Auflösung.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e8ed7b00-7bb3-463e-9aaa-47f77bd4b45e
TQID: 'https://experienceleague.adobe.com/cvzfgWpPXIxwN0HaehiHOL8vAcfb369UJnC0tVuKFFI'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 329
ht-degree: 1%

---

# res{#res}

Auflösungsbasierte Bildskalierung. Skaliert das Bild auf die angeforderte Auflösung.

` res= *`val`*`

<table id="simpletable_E69F3709266749C4A165C90FF18FF5AA"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> Val </span> </p> </td> 
  <td class="stentry"> <p>Zielauflösung; normalerweise in Pixel pro Zoll (real). </p> </td> 
 </tr> 
</table>

Der Skalierungsfaktor wird berechnet, indem *`val`* durch `catalog::Resolution` dividiert werden. Beachten Sie, dass dieser Befehl sich nicht auf die Druckauflösung des Antwortbildes auswirkt.

Um diese Funktion verwenden zu können, muss die Auflösung der Originalquellen-Bilder bekannt und in `catalog::Resolution` festgelegt sein. Je nach Anwendung können die Auflösungseinheiten variieren. Bei wiederholbaren 2D-Texturen oder Materialmustern, wie Tapeten oder Stoffen, kann die Auflösung als Pixel/Zoll oder Pixel/mm ausgedrückt werden. Luftbilder und Karten können besser mit Pixel/Meile oder Pixel/km bedient werden. In jedem Fall müssen die für die `catalog::Resolution` verwendeten Einheiten mit den für die `res=` verwendeten Einheiten übereinstimmen.

Zusätzlich zum Erhalten von Bildern mit präziser Auflösung können `res=` auch verwendet werden, um mehrere Bilder mit derselben Auflösung zu kombinieren, sodass die in diesen Bildern sichtbaren Elemente in korrektem Verhältnis zueinander stehen.

>[!NOTE]
>
>Normalerweise wird die Größe eines zusammengesetzten Bildes auf die Zielansichtsgröße (angegeben durch `wid=`, `hei=` oder `attribute::DefaultPix`) geändert, bevor es an den Client zurückgegeben wird. Um diese Größenanpassung zu verhindern und ein Bild mit der exakten Auflösung von `res=` zu erhalten, kann es erforderlich sein, die Ansichtsskalierung durch explizite Angabe von `scl=1` zu deaktivieren. Hierdurch wird der Server angewiesen, das zusammengesetzte Bild auf die Zielansichtsgröße zuzuschneiden, anstatt es zu skalieren.

## Eigenschaften {#section-fdbd16e59cff4952a3717146bc91412e}

Source-Bild-/Maskenattribut. Ignoriert von Ebenen, die nicht mit einem Quellbild oder einer Maske verknüpft sind. Angewendet auf Ebene 0 wird für `layer=comp` angegeben. Ignoriert, wenn für dieselbe Ebene entweder `scale=` oder `size=` angegeben ist.

## Standard {#section-c5f1ba6fe53d46eca32e7d0588dcdf3d}

Wenn kein Wert angegeben ist, bestimmt `scale=` oder `size=` den Skalierungsfaktor, oder wenn keiner der Werte angegeben ist, wird das Bild ohne Skalierung verwendet.

## Beispiel {#section-eb06f333e08e4247971fb1b18922597b}

Rufen Sie ein Texturbild mit einer Objektauflösung von 12 Pixeln/Zoll für die Verwendung mit Bild-Rendering oder Bild-Authoring ab. Wir spezifizieren verlustfreies PNG-Format und bessere Qualität für Resampling in bestmöglicher Qualität,

` http:// *`server`*/myTexture?res=12&fmt=png&resMode=sharp`

## Verwandte Themen {#section-1f8a8f11772e493ca803c4511f397a11}

[catalog::Resolution](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-resolution-cat.md#reference-de489f5f36b64bd0831749546f8728e1) , [attribute::DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1), [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc), [fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
