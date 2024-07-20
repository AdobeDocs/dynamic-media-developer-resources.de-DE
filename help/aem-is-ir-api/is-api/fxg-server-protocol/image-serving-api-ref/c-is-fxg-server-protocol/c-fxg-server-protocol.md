---
title: FXG-Serverprotokoll
description: Um eine Grafik zu bearbeiten, können Sie Referenzpunkte verwenden, die Kompasspunkten ähnlich sind.
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

Um eine Grafik zu bearbeiten, können Sie Referenzpunkte verwenden, die Kompasspunkten ähnlich sind.

Mit Referenzpunkten können Sie eine Grafik in Relation zu einem Referenzpunkt drehen, skalieren oder ihre Größe ändern. Die Bezugspunkte sind `northWest`, `north`, `northEast`, `west`, `center`, `east`, `southWest`, `south` und `southeast`. Beispielsweise können Sie eine Grafik mit dem mittleren Bezugspunkt um 45° drehen. Die folgende Abbildung zeigt, wo sich die Referenzpunkte befinden, eine Grafik, die um 20° vom Referenzpunkt &quot;`northWest`&quot; gedrehte Grafik und die um 20° vom Referenzpunkt &quot;`east`&quot; gedrehte Grafik.

![Bild mit Referenzpunkten ](assets/wp_ref_points.png)

* A. Referenzpunktstandorte
* B. Grafik
* C. Die um 20° vom `northWest`-Bezugspunkt gedrehte Grafik
* D. Die um 20° vom `east`-Bezugspunkt gedrehte Grafik

Die Syntax lautet:

`referencePoint <string> (northWest, north, northEast, west, center, east, southWest, south, southEast, none, inherit)`

Der Standardwert ist &quot;none&quot;. Der Wert `inherit` gibt den Wert `s7:referencePoint` von oben auf der Seite oder Gruppenebene an alle untergeordneten Elemente weiter, sofern er nicht `none` lautet. Die Einstellung &quot;`none`&quot; bedeutet, dass es keinen Referenzpunkt für das Objekt gibt und das FXG-Koordinatensystem verwendet wird.

>[!NOTE]
>
>Wenn Sie einen Referenzpunkt verwenden möchten und Verschiebungen im Objekt nach dessen Manipulierung vermeiden möchten, aktualisieren Sie die x- und y-Werte des Objekts, nachdem Sie es manipuliert haben.

Wenn ein Wert aus `s7:referencePoint` mit Gruppen (oder Pfaden, Zeilenelementen oder Elementen ohne explizite Breiten- und Höhendefinitionen) verwendet wird, gilt der Wert für den kumulativen Begrenzungsrahmen der Gruppe. Beispielsweise dient der obere linke Punkt des Begrenzungsrahmens aller Objekte in der Gruppe als `northWest`-Bezugspunkt für die Gruppe. Der untere rechte Punkt dient als `southEast`-Bezugspunkt.
