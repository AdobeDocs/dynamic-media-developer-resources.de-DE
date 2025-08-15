---
description: IS bietet Mechanismen zur Vereinfachung der Verwendung von HTML-Imagemaps. Die JAVA- und Flash-basierten Viewer in IIS bieten auch eingeschränkte Unterstützung für Imagemaps.
solution: Experience Manager
title: Imagemaps
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9a685f9d-205d-43b3-b5fe-3ae324fe153e
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '379'
ht-degree: 0%

---

# Imagemaps{#image-maps}

IS bietet Mechanismen zur Vereinfachung der Verwendung von HTML-Imagemaps. Die JAVA- und Flash-basierten Viewer in IIS bieten auch eingeschränkte Unterstützung für Imagemaps.

Source-Imagemaps werden dem IS entweder über `catalog::Map` oder mit dem Befehl `map=` bereitgestellt und verarbeitete Karten werden mit dem Befehl `req=map` abgerufen.

Eine Imagemap besteht aus einem oder mehreren HTML-AREA-Elementen, die ordnungsgemäß mit &quot;&lt;&quot; und &quot;>&quot; abgegrenzt sind. Bei Angabe über catalog:map werden alle Pixelkoordinatenwerte in der Originalbildauflösung und relativ zur oberen linken Ecke des (unveränderten) Quellbilds angenommen. Bei Bereitstellung über einen `map=` werden die Koordinatenwerte als Ebenenkoordinaten relativ zur linken oberen Ecke der Ebene angenommen (nach `rotate=` und `extend=`).

>[!NOTE]
>
>%-Koordinaten sind derzeit nicht zulässig und können falsch verarbeitet werden.

IS erzeugt aus den Quell-Imagemaps jeder Einzelschicht eine zusammengesetzte Imagemap, indem die räumlichen Transformationen (wie Skalierung und Rotation) auf die Map-Koordinaten angewendet werden und dann die verarbeiteten Layer-Maps in der entsprechenden z-Reihenfolge (von vorne nach hinten) und mit der entsprechenden Positionierung zusammengestellt werden.

Die folgenden Befehle werden für die Verarbeitung von Imagemaps berücksichtigt, wenn sie in Verbindung mit `req=map` bereitgestellt werden (entweder direkt in der Anfrage, über Katalogvorlagen oder in `catalog::Modifier` Zeichenfolgen):

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

Die `SHAPE`- und `COORDS`-Attribute eines `AREA` können während der Verarbeitung einer `req=map`-Anfrage geändert werden. Alle anderen Attribute des `AREA`-Elements werden unverändert weitergeleitet. In den meisten Fällen umfasst dies das Ändern des `SHAPE` von `DEFAULT` in `RECT` (dies würde auch das Attribut `COORDS` hinzufügen) oder das Ändern der `COORDS`.

Alle `AREA` Elemente, die während der Verarbeitung leer werden, werden vollständig entfernt. Wenn eine Karte mit `layer=comp` verknüpft ist, wird sie hinter allen anderen Karten platziert. Die Daten werden im Textformular als ein oder mehrere HTML-`AREA` zurückgegeben. Eine leere Antwortzeichenfolge gibt an, dass für das/die angegebene(n) Objekt(e) keine Imagemap vorhanden ist.

Ebenentransparenz wird bei der Kartenverarbeitung nicht berücksichtigt. Einer vollständig transparenten Ebene kann immer noch eine Imagemap zugeordnet sein. Die Karte einer teilweise transparenten Ebene wird nicht auf die transparenten Bereiche abgeschnitten.

## Verwandte Themen {#see-also}

[map=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-map.md#reference-8f96545f196b4b7caa616e15c2363f06) , [catalog::Map](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-map-cat.md), [Spezifikation für HTML 4.01](https://www.w3.org/TR/html401/)
