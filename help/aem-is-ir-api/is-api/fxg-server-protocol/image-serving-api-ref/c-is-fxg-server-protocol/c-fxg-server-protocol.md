---
title: FXG-Serverprotokoll
description: Um eine Grafik zu bearbeiten, können Sie Referenzpunkte verwenden, die Kompasspunkten ähneln.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 57d9ba37-819e-455f-9b22-bd7aabffe007
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 18%

---

# FXG-Serverprotokoll{#fxg-server-protocol}

Um eine Grafik zu bearbeiten, können Sie Referenzpunkte verwenden, die Kompasspunkten ähneln.

Mit Referenzpunkten können Sie eine Grafik in Relation zu einem Referenzpunkt drehen, skalieren oder ihre Größe ändern. Die Referenzpunkte sind `northWest`, `north`, `northEast`, `west`, `center`, `east`, `southWest`, `south` und `southeast`. Beispielsweise können Sie eine Grafik mithilfe des Bezugspunkts des Mittelpunkts um 45° in der Mitte drehen. Die folgende Abbildung zeigt, wo sich die Referenzpunkte befinden, eine Grafik, die Grafik um 20° von ihrem `northWest` Referenzpunkt gedreht, und die Grafik um 20° von ihrem `east` Referenzpunkt gedreht.

![Referenzpunktbild](assets/wp_ref_points.png)

* A. Positionen der Referenzpunkte
* B. Grafik
* C. Die Grafik rotierte um 20° von ihrem `northWest` Bezugspunkt
* D. Die Grafik rotierte um 20° von ihrem `east` Bezugspunkt

Die Syntax lautet:

`referencePoint <string> (northWest, north, northEast, west, center, east, southWest, south, southEast, none, inherit)`

Der Standardwert ist „Ohne“. Der `inherit`-Wert übergibt den `s7:referencePoint`-Wert, sofern er nicht `none` ist, vom oberen Rand der Seiten- oder Gruppenebene an alle untergeordneten Elemente. Die `none` bedeutet, dass es keinen Referenzpunkt für das Objekt gibt und das FXG-Koordinatensystem verwendet wird.

>[!NOTE]
>
>Wenn Sie einen Referenzpunkt verwenden möchten und Verschiebungen im Objekt nach dessen Manipulierung vermeiden möchten, aktualisieren Sie die x- und y-Werte des Objekts, nachdem Sie es manipuliert haben.

Wenn ein Wert aus `s7:referencePoint` für Gruppen (oder Pfade, Linienelemente oder Elemente ohne explizite Breiten- und Höhendefinitionen) verwendet wird, gilt der Wert für den kumulativen Begrenzungsrahmen der Gruppe. Beispielsweise dient der obere linke Punkt des Begrenzungsrahmens aller Objekte in der Gruppe als `northWest` Referenzpunkt für die Gruppe; der untere rechte Punkt dient als `southEast` Referenzpunkt.
