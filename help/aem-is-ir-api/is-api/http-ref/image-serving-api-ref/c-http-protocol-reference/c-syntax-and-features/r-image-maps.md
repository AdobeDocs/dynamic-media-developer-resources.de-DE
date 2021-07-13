---
description: IS bietet Mechanismen zur Vereinfachung der Verwendung von HTML-Imagemaps. Die JAVA-basierten und Flash-basierten Viewer in IS bieten außerdem eingeschränkte Unterstützung für Imagemaps.
solution: Experience Manager
title: Imagemaps
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9a685f9d-205d-43b3-b5fe-3ae324fe153e
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 0%

---

# Imagemaps{#image-maps}

IS bietet Mechanismen zur Vereinfachung der Verwendung von HTML-Imagemaps. Die JAVA-basierten und Flash-basierten Viewer in IS bieten außerdem eingeschränkte Unterstützung für Imagemaps.

Quellbildzuordnungen werden entweder über `catalog::Map` oder mit dem Befehl `map=` an IS übermittelt und verarbeitete Zuordnungen werden mit dem Befehl `req=map` abgerufen.

Eine Imagemap besteht aus einem oder mehreren HTML-Bereichselementen, die ordnungsgemäß mit &#39;&lt;&#39; und &#39;>&#39; getrennt sind. Bei Bereitstellung über catalog::Map wird angenommen, dass alle Pixelkoordinatenwerte in der Originalbildauflösung und relativ zur oberen linken Ecke des (nicht modifizierten) Quellbilds liegen. Wenn die Koordinatenwerte über einen Befehl `map=` bereitgestellt werden, werden sie als Ebenenkoordinaten im Verhältnis zur oberen linken Ecke der Ebene (nach `rotate=` und `extend=`) angenommen.

>[!NOTE]
>
>%-Koordinaten sind derzeit nicht erlaubt und können falsch verarbeitet werden.

IS generiert eine zusammengesetzte Imagemap aus den Quellbildkarten jeder einzelnen Schicht, indem die räumlichen Transformationen (z. B. Skalierung und Rotation) auf die Kartenkoordinaten angewendet und dann die verarbeiteten Ebenenkarten in der entsprechenden z-Reihenfolge (von vorne nach hinten) und mit der entsprechenden Positionierung zusammengestellt werden.

Die folgenden Befehle werden bei der Verarbeitung von Imagemaps berücksichtigt, wenn sie in Verbindung mit `req=map` bereitgestellt werden (entweder direkt in der Anforderung, über Katalogvorlagen oder in `catalog::Modifier` -Zeichenfolgen):

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

Die Attribute `SHAPE` und `COORDS` eines `AREA` können während der Verarbeitung einer `req=map`-Anfrage geändert werden. Alle anderen Attribute des Elements `AREA` werden ohne Änderung übergeben. In den meisten Fällen umfasst dies eine Änderung des `SHAPE` -Werts von `DEFAULT` in `RECT` (dadurch würde auch das `COORDS` -Attribut hinzugefügt) oder eine Änderung der `COORDS` -Werte.

Alle `AREA`-Elemente, die während der Verarbeitung leer werden, werden vollständig entfernt. Wenn eine Karte mit `layer=comp` verknüpft ist, wird sie hinter allen anderen Karten platziert. Die Daten werden im Text von einem oder mehreren HTML `AREA` -Elementen zurückgegeben. Eine leere Antwortzeichenfolge gibt an, dass für die angegebenen Objekte keine Imagemap vorhanden ist.

Ebenentransparenz wird bei der Kartenverarbeitung nicht berücksichtigt. Eine vollständig transparente Ebene kann weiterhin mit einer Imagemap verknüpft sein. Die Karte einer teilweise transparenten Ebene wird nicht auf die transparenten Bereiche beschnitten.

## Verwandte Themen {#see-also}

[map=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-map.md#reference-8f96545f196b4b7caa616e15c2363f06) ,  [catalog::Map](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-map-cat.md),  [HTML 4.01 Specification](http://www.w3.org/TR/html401/)
