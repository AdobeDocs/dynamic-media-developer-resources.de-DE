---
description: IS bietet Mechanismen zur Vereinfachung der Verwendung von HTML-Imagemaps. Die JAVA-basierten und Flash-basierten Viewer in IS bieten außerdem eine eingeschränkte Unterstützung für Imagemaps.
seo-description: IS bietet Mechanismen zur Vereinfachung der Verwendung von HTML-Imagemaps. Die JAVA-basierten und Flash-basierten Viewer in IS bieten außerdem eine eingeschränkte Unterstützung für Imagemaps.
seo-title: Imagemaps
solution: Experience Manager
title: Imagemaps
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 2b7b620b-712b-4110-ba38-993a354c09d3
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '402'
ht-degree: 0%

---


# Imagemaps{#image-maps}

IS bietet Mechanismen zur Vereinfachung der Verwendung von HTML-Imagemaps. Die JAVA-basierten und Flash-basierten Viewer in IS bieten außerdem eine eingeschränkte Unterstützung für Imagemaps.

Quellbildzuordnungen werden entweder über den Befehl `catalog::Map` oder über den Befehl `map=` bereitgestellt und verarbeitete Maps werden mit dem Befehl `req=map` abgerufen.

Eine Imagemap besteht aus einem oder mehreren HTML-AREA-Elementen, die ordnungsgemäß mit &quot;&lt;&quot;und &quot;>&quot;getrennt sind. Bei Bereitstellung über catalog::Map werden alle Pixelkoordinatenwerte in der Originalbildauflösung und relativ zur oberen linken Ecke des (unveränderten) Quellbilds angenommen. Bei Bereitstellung über einen Befehl `map=` werden die Koordinatenwerte relativ zur oberen linken Ecke der Ebene (nach `rotate=` und `extend=`) als Ebenenkoordinaten angenommen.

>[!NOTE]
>
>%-Koordinaten sind derzeit nicht zulässig und können falsch verarbeitet werden.

IS erzeugt eine Composite-Imagemap aus den Quellbildkarten der einzelnen konstituierenden Ebenen, indem die räumlichen Transformationen (z. B. Skalierung und Drehung) auf die Kartenkoordinaten angewendet werden und dann die verarbeiteten Ebenenzuordnungen in der entsprechenden Z-Reihenfolge (von vorne nach hinten) und mit der entsprechenden Positionierung zusammengestellt werden.

Die folgenden Befehle werden für die Verarbeitung von Imagemaps berücksichtigt, wenn sie in Verbindung mit `req=map` bereitgestellt werden (entweder direkt in der Anforderung, über Katalogvorlagen oder in `catalog::Modifier`-Zeichenfolgen):

* `align=`
* `wid=`
* `hei=`
* `scl=`
* `crop=`
* `flip=`
* `rotate=`
* `scale=`
* `layer=`
* `size=`
* `extend=`
* `origin=`
* `pos=`
* `anchor=`
* `src=`
* `map=`

Alle anderen Befehle werden effektiv ignoriert.

Die Attribute `SHAPE` und `COORDS` eines `AREA` können während der Verarbeitung einer `req=map`-Anforderung modifiziert werden. Alle anderen Attribute des `AREA`-Elements werden ohne Änderung weitergeleitet. In den meisten Fällen umfasst dies die Änderung des Werts `SHAPE` von `DEFAULT` in `RECT` (dies würde auch das Attribut `COORDS` hinzufügen) oder die Änderung der Werte `COORDS`.

Alle `AREA`-Elemente, die während der Verarbeitung leer werden, werden vollständig entfernt. Wenn eine Map mit `layer=comp` verknüpft ist, wird sie hinter allen anderen Maps platziert. Die Daten werden im Textformular eines oder mehrerer HTML `AREA`-Elemente zurückgegeben. Eine leere Antwortzeichenfolge weist darauf hin, dass für die angegebenen Objekte keine Imagemap vorhanden ist.

Ebenentransparenz wird bei der Kartenverarbeitung nicht berücksichtigt. Eine vollständig transparente Ebene kann dennoch mit einer Imagemap verknüpft sein. Die Karte einer teilweise transparenten Ebene wird nicht auf die transparenten Bereiche beschnitten.

## Verwandte Themen {#see-also}

[map=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-map.md#reference-8f96545f196b4b7caa616e15c2363f06) ,  [catalog::Map](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-map-cat.md),  [HTML 4.01-Spezifikation](http://www.w3.org/TR/html401/)
