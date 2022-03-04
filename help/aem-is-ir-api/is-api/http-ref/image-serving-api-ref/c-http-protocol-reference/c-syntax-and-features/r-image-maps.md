---
description: IS bietet Mechanismen zur Vereinfachung der Verwendung von HTML-Imagemaps. Die JAVA-basierten und Flash-basierten Viewer in IS bieten außerdem eingeschränkte Unterstützung für Imagemaps.
solution: Experience Manager
title: Imagemaps
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9a685f9d-205d-43b3-b5fe-3ae324fe153e
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '375'
ht-degree: 0%

---

# Imagemaps{#image-maps}

IS bietet Mechanismen zur Vereinfachung der Verwendung von HTML-Imagemaps. Die JAVA-basierten und Flash-basierten Viewer in IS bieten außerdem eingeschränkte Unterstützung für Imagemaps.

Quellbildkarten werden entweder über `catalog::Map` oder mit `map=` und verarbeitete Maps werden mit dem `req=map` Befehl.

Eine Imagemap besteht aus einem oder mehreren HTML-AREA-Elementen, die durch &#39;&lt;&#39; und &#39;>&#39; ordnungsgemäß getrennt sind. Bei Bereitstellung über catalog::Map wird angenommen, dass alle Pixelkoordinatenwerte in der Originalbildauflösung und relativ zur oberen linken Ecke des (nicht modifizierten) Quellbilds liegen. Wenn über eine `map=` angegeben ist, werden die Koordinatenwerte als Ebenenkoordinaten relativ zur oberen linken Ecke der Ebene angenommen (nach `rotate=` und `extend=`).

>[!NOTE]
>
>%-Koordinaten sind derzeit nicht erlaubt und können falsch verarbeitet werden.

IS generiert eine zusammengesetzte Imagemap aus den Quellbildkarten jeder einzelnen Schicht, indem die räumlichen Transformationen (z. B. Skalierung und Rotation) auf die Kartenkoordinaten angewendet und dann die verarbeiteten Ebenenkarten in der entsprechenden z-Reihenfolge (von vorne nach hinten) und mit der entsprechenden Positionierung zusammengestellt werden.

Die folgenden Befehle werden bei der Verarbeitung von Imagemaps berücksichtigt, wenn sie in Verbindung mit `req=map` (entweder direkt in der Anfrage, über Katalogvorlagen oder in `catalog::Modifier` Zeichenfolgen):

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

Die `SHAPE` und `COORDS` -Attributen eines `AREA` während der Verarbeitung eines `req=map` -Anfrage, alle anderen Attribute der `AREA` -Element ohne Änderung übergeben werden. In den meisten Fällen umfasst dies das Ändern der `SHAPE` Wert aus `DEFAULT` nach `RECT` (Dadurch würde auch die `COORDS` -Attribut) oder ändern Sie die `COORDS` -Werte.

Alle `AREA` -Elemente, die während der Verarbeitung leer werden, werden vollständig entfernt. Wenn eine Zuordnung mit `layer=comp` es wird hinter allen anderen Karten platziert. Die Daten werden in Textform von einem als oder mehreren HTML zurückgegeben `AREA` -Elemente. Eine leere Antwortzeichenfolge gibt an, dass für die angegebenen Objekte keine Imagemap vorhanden ist.

Ebenentransparenz wird bei der Kartenverarbeitung nicht berücksichtigt. Eine vollständig transparente Ebene kann weiterhin mit einer Imagemap verknüpft sein. Die Karte einer teilweise transparenten Ebene wird nicht auf die transparenten Bereiche beschnitten.

## Verwandte Themen {#see-also}

[map=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-map.md#reference-8f96545f196b4b7caa616e15c2363f06) , [Katalog::Map](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-map-cat.md), [HTML 4.01 Spezifikation](https://www.w3.org/TR/html401/)
