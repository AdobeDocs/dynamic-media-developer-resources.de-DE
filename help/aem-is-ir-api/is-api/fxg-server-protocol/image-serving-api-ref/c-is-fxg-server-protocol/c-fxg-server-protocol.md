---
description: Zur Manipulation von Grafiken können Sie Referenzpunkte verwenden, die den Orientierungspunkten auf einem Kompass gleichen.
seo-description: Zur Manipulation von Grafiken können Sie Referenzpunkte verwenden, die den Orientierungspunkten auf einem Kompass gleichen.
seo-title: FXG-Serverprotokoll
solution: Experience Manager
title: FXG-Serverprotokoll
topic: Scene7 Image Serving - Image Rendering API
uuid: 5cb123ca-2274-4ddb-8fa1-ab22a19172f6
translation-type: tm+mt
source-git-commit: 26fb6212c3106deb7b088020d9f2993e40dec20b
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 86%

---


# FXG-Serverprotokoll{#fxg-server-protocol}

Zur Manipulation von Grafiken können Sie Referenzpunkte verwenden, die den Orientierungspunkten auf einem Kompass gleichen.

Mit Referenzpunkten können Sie eine Grafik in Relation zu einem Referenzpunkt drehen, skalieren oder ihre Größe ändern. Die Referenzpunkte sind `northWest`, `north`, `northEast`, `west`, `center`, `east`, `southWest`, `south` und `southeast`. Beispielsweise können Sie eine Grafik auf ihrem Mittelpunkt 45 Grad drehen, indem Sie den Referenzpunkt center verwenden. Auf der nachfolgenden Abbildung werden die Positionen der Referenzpunkte gezeigt, eine Grafik, die auf Basis des Referenzpunkts `northWest` um 20 Grad gedrehte Grafik und die auf Basis des Referenzpunkts `east` um 20 Grad gedrehte Grafik.

![](assets/wp_ref_points.png)

* A. Positionen von Referenzpunkten
* B. Eine Grafik
* C. Die um 20 Grad gedrehte Grafik vom `northWest`-Bezugspunkt
* D. Die um 20 Grad gedrehte Grafik ab ihrem `east` Referenzpunkt

Die Syntax lautet:

`referencePoint <string> (northWest, north, northEast, west, center, east, southWest, south, southEast, none, inherit)`

Der Standardwert ist none. Der Wert `inherit` leitet den Wert `s7:referencePoint` vom Seitenanfang oder der übergeordneten Gruppenebene an alle untergeordneten Elemente weiter, sofern der Wert nicht `none` lautet. Die Einstellung `none` bedeutet, dass kein Referenzpunkt für das Objekt festgelegt wurde und das FXG-Koordinatensystem verwendet wird.

>[!NOTE]
>
>Wenn Sie einen Referenzpunkt verwenden möchten und Verschiebungen im Objekt nach dessen Manipulierung vermeiden möchten, aktualisieren Sie die x- und y-Werte des Objekts, nachdem Sie es manipuliert haben.

Wenn ein Wert aus `s7:referencePoint` mit Gruppen (oder Pfaden, Linienelementen oder Elementen, die über keine explizite Breiten- und Höhendefinition verfügen) verwendet wird, gilt der Wert für den gesamten Begrenzungsrahmen der Gruppe. So dient beispielsweise die obere linke Ecke des Begrenzungsrahmens aller Objekte der Gruppe als Referenzpunkt `northWest` für die Gruppe; die rechte untere Ecke dient als Referenzpunkt `southEast`.

